# Task 3
## The Cube Orange+ (Pixhawk)
It is an advanced autopilot system used in unmanned aerial vehicles, It serves as the main flight controller, managing flight stabilization, navigation, and control, It features a powerful microcontroller, supports sensor integration, offers redundancy and safety features, and has multiple connectivity options.

<img src="https://github.com/AhmedSaleh627/Eagles_MegaProject/assets/88249795/d2698a1f-602e-40ea-81cc-0f257f7fb859 " width="400" height="400" />  

<br>Features:

*	Compatible With ArduPilot Software.
*	User-Friendly as there are many available online resources for instructions.
*	It is designed to be used with a domain-specific carrier board in order to reduce the wiring, improve reliability, and ease of assembly. 
*	The ability to carry out fully written missions in autonomous flight mode.
*	ROS compatibility enables communication and collaboration between obstacle avoidance algorithms, ODCL, and air drop.
*	Multiple Sensors as: Accelerometer, Gyroscope, Compass and Barometric Pressure Sensor
*	Peripherals that are compatible with most of the sensors on the market such as Lidar, Pitot-Static Tube, GPS and more.
*	Various communication protocol supports such as USB, CAN, I2C and SPI.

## Jetson Nano ( on-board computer )  

An effective, low-power, and small platform for integrating AI and computer vision functionalities . For UAV applications that need extensive onboard processing and autonomous decision-making, it's an excellent option thanks to its GPU acceleration, neural network inference capabilities, and developer support.  

<img src="https://github.com/AhmedSaleh627/Eagles_MegaProject/assets/88249795/c295744a-02ee-4da6-bd47-435c9b274b29" width="400" height="400" />  

<br>Features:
*	Power Efficiency: The Jetson Nano is designed to provide high computing power while being energy-efficient. This is crucial for UAV applications, as power constraints are common due to limited battery capacity. 
*	GPU Acceleration: The Jetson Nano comes with a powerful integrated GPU (Graphics Processing Unit) based on NVIDIA's CUDA architecture. This GPU acceleration enables efficient parallel processing of tasks such as computer vision, image processing, and artificial intelligence algorithms. 
*	Compact Size and Weight: The Jetson Nano is compact and lightweight, making it suitable for integration into small UAV platforms with limited payload capacity.
*	 Supports popular software frameworks and libraries used in the field of machine learning and artificial intelligence. This includes TensorFlow, PyTorch, OpenCV, and others, making it easier to develop and deploy advanced AI algorithms on the UAV.

Possible Connections between the Pixhawk and the jetson nano:  

1-UART Connection:
The Jetson Nano can be connected to the Cube Orange+ Pixhawk using UART (Universal Asynchronous Receiver-Transmitter) communication. The UART connection utilizes the serial ports available on both devices for data exchange.
This is the connection I found most suitable for the UAV.
Reasons for Choosing the UART Connection:
*	Lightweight Connection: UART connection requires fewer resources and is suitable for applications where space and weight considerations are critical, such as small UAVs.
*	Low Latency: UART communication offers low latency, making it suitable for time-critical applications that require fast data transfer.
*	Compatibility: Both the Jetson Nano and Pixhawk typically have UART ports available, allowing for direct hardware-level communication.

2-USB Connection:
The Jetson Nano can be connected to the Cube Orange+ Pixhawk using a USB cable. The USB connection provides a simple and direct link between the two devices. The Jetson Nano can be powered via USB and can communicate with the Pixhawk for data exchange.
The USB connection is easy to set up and requires minimal additional hardware and offers reliable and high-speed data transfer between the Jetson Nano and Pixhawk.  

3-Telemetry Connection:
Using a telemetry module or radio, the Jetson Nano can establish a wireless connection with the Pixhawk, allowing bidirectional data transmission between the two devices, but we won’t need this connection as the jetson nano is our on-board computer and its close to the Pixhawk.

## Ubiquiti BULLET AC
Ubiquiti Bullet AC is a wireless radio with an integrated Type N RF connector . It works great on any distance, is weatherproof and allows real TCP/IP throughput of up to 300Mbps.  
A Wireless transmission link will be constructed between The Ground Control Station and the Ubiquiti Bullet Ac with a 5GHz of frequency.  

<img src="https://github.com/AhmedSaleh627/Eagles_MegaProject/assets/88249795/b6e7f037-52bd-4b22-9178-a1540ccf358a" width="400" height="400" />    

<br>Features:  
*	Supports data transfer rates of 300+ Mb/s on the 5 GHz frequency.
*	equipped with a single Gigabit Ethernet port.
*	equipped with a single N-Type antenna connector.
*	supports PoE connectivity, eliminating the need to run a dedicated power supply to the radio.
*	Features a weatherproof design. Made from a high-grade, powder-coated aluminum, the casing can withstand nature's harshest outdoor elements.

## Ubiquiti Airmax NanoStation AC
The Ubiquiti AirMax NanoStation AC is an indoor/outdoor, compact, high-performance CPE, featuring a dedicated Wi-Fi radio for management.  
It will be on our ground station and connected to the Ubiquiti Bullet Ac through the Wireless transmission link of 5GHz frequency.  

<img src="https://github.com/AhmedSaleh627/Eagles_MegaProject/assets/88249795/d15516f0-d5cd-4426-83c7-4499edf7da79" width="400" height="400" />   

<br>Features:
*	Frequency 5GHz
*	Throughput 450+ Mbps
*	Range 15+ km
*	Management Radio
*	UNMS App Compatible

## Telemetry RFD900+  
The RFD900+ is a high-performance 900MHz, It is designed for long range serial communication applications requiring best in class radio link performance.  
It will be connected to the Pixhawk on our UAV, and we will have another telemetry on the ground control station to establish our communication. 

<img src="https://github.com/AhmedSaleh627/Eagles_MegaProject/assets/88249795/473cc84a-7a15-4f5c-b78b-f2d43918e5f7" width="400" height="400" />   

<br>Features
*	Long range : More than 40km.
*	Open-source firmware, field upgradeable and easy to configure.
*	Small in size and light weight so good for our UAV.
*	GPIO: 6 General purpose IO (Digital, ADC, PWM capable). 

## GPS HERE3+
The Here3+ GPS is a cost-efficient GNSS system that supports RTK mode with positioning accuracy down to centimeter-level in an ideal environment, in which we will use it to determine the position of the UAV. 

<img src="https://github.com/AhmedSaleh627/Eagles_MegaProject/assets/88249795/fb73886a-f632-481e-8acc-f89a61be8c58" width="400" height="400" />   

<br>Features:
*	Real-time features from the Drone CAN protocol.
*	It is also designed to be dust-proof and splash-proof. 
*	Support from ground control software
*	Complete built-in set of Inertial Measurement Units (compass, gyroscope, and accelerometer), which satisfy advanced navigation needs.
*	More accurate positioning, faster response, and colorful LED lights for visible indications of UAV status.
*	Upgradeability, Noise immunity, high data rate.

## RP Lidar
The Lidar will help us in avoinding the obstacles as it enables autonomous vehicles to “see” by generating and measuring millions of data points in real time, creating a precise map of its ever-changing surroundings for safe navigation.


<img src="https://github.com/AhmedSaleh627/Eagles_MegaProject/assets/88249795/fc532299-f255-41b4-bab3-fdd3cf301f79" width="400" height="400" />   

<br>Features:
*	Compatible with ArduCopter.
*	360-degree full-scan detection of the surrounding environment and the creation of a map of the region.
*	8 Meters Range.
*	Comparison Under Different Conditions.
*	Configurable Scan Rate from 2-10Hz.
*	Ideal for Robot Navigation and Localization
*	Easy to use.

## TAROT GIMBAL
A gimbal is a device that uses motors and sensors to counteract the movements of your camera and keep it level and steady, and we need it since it is very important that we get clear images.  

<img src="https://github.com/AhmedSaleh627/Eagles_MegaProject/assets/88249795/82c6329c-e2ca-41da-9bb4-18af7e5891c5" width="400" height="400" />   

<br>Features:
*	First-person view mode (FPV).
*	Wide range voltage input
*	Point follow mode (PF)
*	Built-in independent IMU modules

## Camera
We need a camera in order to complete our computer vision tasks , It is recommended that we use the Sony α6000 Camera for its high resolution, high shutter speed in order to prevent blurring and considerably low price compared to the other cameras.  

<img src="https://github.com/AhmedSaleh627/Eagles_MegaProject/assets/88249795/daeaec53-2eff-4c01-b45e-4c0c60a46f65" width="400" height="400" /> 

<br>Features:
*	Approx. 24.3 megapixels.
*	25mm lens focal length.
*	Up to 11 fps.
*	E-mount.

## Other Components that can be useful for us
### RadioMaster Tx16S
In case we want to control the UAV manually we need the RadioMaster Tx16S which is a remote control multiprotocol transmitter.  

<img src="https://github.com/AhmedSaleh627/Eagles_MegaProject/assets/88249795/8539de2c-e3f4-4bb9-b97b-cd3c1efc3af1" width="400" height="400" /> 

<br>Features:
*	OpenTX Firmware: an open-source operating system specifically developed for RC transmitters.
*	Hall Sensor Gimbals: The remote control is equipped with high-precision hall sensor gimbals, which offer smooth and precise control inputs.
*	Telemetry and Voice Alerts: The TX16S supports telemetry integration, allowing users to receive real-time data and information from their RC models.

### FrySky X8R Reciever
This will be our reciever which will maintain the communication with the radiomaster tx16s.  

<img src="https://github.com/AhmedSaleh627/Eagles_MegaProject/assets/88249795/50bcb7be-cc80-4602-bfa9-944e6eda90f8" width="400" height="400" />  

<br>Features:
* Support for Telemetry: The X8R receiver features built-in telemetry capabilities that let you keep an eye on crucial flight information like battery power, signal strength, and more. This can offer useful information for tracking and guaranteeing the efficiency and performance of our aircraft.
* Long Range: The X8R receiver is known for its long-range capabilities, enabling dependable signal transmission even over considerable distances.
* Number of Channels: The X8R receiver has a maximum of 16 channels, which is plenty. 

### IR LOCK Sensor
The IR-LOCK sensor is a modified version of the Pixy camera, which comes pre-configured to work as an IR beacon detector. It can be very useful to ensure  precise landing and safe landings in tight spaces.
The IRLOCK sensor should be mounted to the underside of the frame with the camera lens pointing directly down toward the ground.

<img src="https://github.com/AhmedSaleh627/Eagles_MegaProject/assets/88249795/3b1b518d-31c0-4138-b47c-dbe2d0b805f8" width="400" height="400" />   

### HEREFLOW Sensor
The HereFlow is a miniature UAV navigation board incorporating a time-of-flight LiDAR sensor, an optical flow camera and a six-degree-of-freedom IMU and it only weights 1 gram.  

<img src="https://github.com/AhmedSaleh627/Eagles_MegaProject/assets/88249795/0a9901eb-751e-4538-8878-d773e131edab" width="200" height="300" /> 















