# Drone Mission Simulation and GPS Obstacles
[Video Link](https://drive.google.com/file/d/1moXG_2tSXZLbZNRTZD53cwrM68VSTf4P/view?usp=sharing) -- Here is the Link to Task1 Video.

## Objective
In this task, our objective is to simulate a drone mission using Mission Planner. Mission Planner provides the capability to set waypoints along with specific commands such as TAKEOFF, RETURN TO LAUNCH, and others. The drone will follow these waypoints and successfully complete the mission.  

## GPS Obstacles and Fences
Regarding the  GPS obstacles, Mission Planner offers a feature called "Fences." This feature allows us to define specific GPS locations. If the drone enters any of these locations, it will immediately execute a different command such as Return to Launch or Land. However, Mission Planner lacks an option to instruct the drone to stop before entering the specified GPS location. To create a safety margin, we can increase the radius of the GPS location and reduce the speed of the drone, but this approach may not be entirely reliable.

## Utilizing DroneKit API
To overcome the limitations of Mission Planner, we explored the DroneKit API. This API provides the functionality we need to set up these particular GPS locations for avoidance purposes. However, during our attempts to use DroneKit with Linux and connect it to Mission Planner, we encountered multiple errors. Unfortunately, our progress was hindered when our Linux system crashed, preventing us from continuing the process.

## Code Example
### For Arming and Simulating the drone:  

```
from __future__ import print_function
import time
from dronekit import connect, VehicleMode, LocationGlobalRelative


# Set up option parsing to get connection string
import argparse
parser = argparse.ArgumentParser(description='Commands vehicle using vehicle.simple_goto.')
parser.add_argument('--connect',
                    help="Vehicle connection target string. If not specified, SITL automatically started and used.")
args = parser.parse_args()

connection_string = args.connect
sitl = None


# Start SITL if no connection string specified
if not connection_string:
    import dronekit_sitl
    sitl = dronekit_sitl.start_default()
    connection_string = sitl.connection_string()


# Connect to the Vehicle
print('Connecting to vehicle on: %s' % connection_string)
vehicle = connect(connection_string, wait_ready=True)


def arm_and_takeoff(aTargetAltitude):
    """
    Arms vehicle and fly to aTargetAltitude.
    """

    print("Basic pre-arm checks")
    # Don't try to arm until autopilot is ready
    while not vehicle.is_armable:
        print(" Waiting for vehicle to initialise...")
        time.sleep(1)

    print("Arming motors")
    # Copter should arm in GUIDED mode
    vehicle.mode = VehicleMode("GUIDED")
    vehicle.armed = True

    # Confirm vehicle armed before attempting to take off
    while not vehicle.armed:
        print(" Waiting for arming...")
        time.sleep(1)

    print("Taking off!")
    vehicle.simple_takeoff(aTargetAltitude)  # Take off to target altitude

    # Wait until the vehicle reaches a safe height before processing the goto
    #  (otherwise the command after Vehicle.simple_takeoff will execute
    #   immediately).
    while True:
        print(" Altitude: ", vehicle.location.global_relative_frame.alt)
        # Break and return from function just below target altitude.
        if vehicle.location.global_relative_frame.alt >= aTargetAltitude * 0.95:
            print("Reached target altitude")
            break
        time.sleep(1)


arm_and_takeoff(10)

print("Set default/target airspeed to 3")
vehicle.airspeed = 3

print("Going towards first point for 30 seconds ...")
point1 = LocationGlobalRelative(-35.361354, 149.165218, 20)
vehicle.simple_goto(point1)

# sleep so we can see the change in map
time.sleep(30)

print("Going towards second point for 30 seconds (groundspeed set to 10 m/s) ...")
point2 = LocationGlobalRelative(-35.363244, 149.168801, 20)
vehicle.simple_goto(point2, groundspeed=10)

# sleep so we can see the change in map
time.sleep(30)

print("Returning to Launch")
vehicle.mode = VehicleMode("RTL")

# Close vehicle object before exiting script
print("Close vehicle object")
vehicle.close()

# Shut down simulator if it was started.
if sitl:
    sitl.stop()
```
### For avoing specific GPS locations:  

![Screenshot 2023-09-28 183445](https://github.com/AhmedSaleh627/Eagles_MegaProject/assets/88249795/158ccdc2-77d9-4114-b53e-d5bf2844852d)


Please note that the specific versions required for successful integration are pymavlink version 2.4.8, and Python version 3.6 or 2.7.

Although we were unable to complete the process, this README provides an overview of our intended approach and the challenges we encountered.
