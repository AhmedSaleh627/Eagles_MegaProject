# Saint Louis University SUAS 2023 Video Summary - README

## Introduction

This README provides a concise summary of Saint Louis University's participation in the SUAS 2023 (Student Unmanned Aerial Systems) competition, as depicted in their video presentation. This summary aims to highlight the key aspects of their project. For detailed information or collaboration inquiries, please refer to the team's official channels.

## Team Credentials

- **Certified Pilot and Ground Operator:** The team had a certified pilot and a dedicated ground station operator for managing mission profiles via telemetry.

- **Camera Setup:** They utilized a GoPro camera capable of recording in 1080p at 60 frames per second, paired with a GPU Jetson Nano for processing.

- **Telemetry System:** Their telemetry system operated at 915 MHz, with an impressive range of up to 3000 feet.

- **Transmitter and Receiver:** The team used a Futaba 10J transmitter and a Futaba R3008 SB receiver, both operating at 2.4 GHz.

## Propulsion and Motor Testing

- **Electric-Based Propulsion:** Their UAS featured an electric-based propulsion system powered by a 10,000 milliamp-hour LiPo battery.

- **Motor and Propeller:** They employed an A60 motor with a 5x40 propeller, boasting an 18-inch propeller diameter. Motor performance was rigorously tested on a thrust stand, reaching a remarkable thrust of 30 pounds at 1780 PWM signal.

- **Load Cell:** For precise thrust measurements, they used a type S load cell.

## Control and Navigation

- **Control Hardware:** A Pixel 4 Mini served as their controller hardware, paired with a PX4 autopilot as the flight controller.

- **Flight Controller Firmware:** The flight controller ran on PX4 autopilot firmware, an open-source solution capable of waypoint navigation.

- **Flight Planning:** Flight plans were created on a Windows 10 laptop and uploaded to the Pixel 4 Mini.

- **Obstacle Avoidance:** Their UAS boasted an advanced obstacle avoidance algorithm, creating circular boundaries when detecting other Autonomous Unmanned Systems (AUS) and generating additional waypoints to navigate around these boundaries.

## Onboard Data Link Camera (ODLC)

- **ODLC Camera:** A Sony RX100 V2 camera was employed for Onboard Data Link Camera (ODLC) purposes.

- **Performance:** The ODLC system performed admirably, even when processing data from the camera at 360p resolution. The Jetson Nano's GPU proved capable of handling the task.

## Testing and Results

- **Flight Duration:** During testing, the UAS achieved an impressive flight duration of 19 minutes and 46 seconds, covering distances of up to 1600 feet while maintaining a connection every second.

- **Telemetry Performance:** Out of 1187 telemetry messages sent, only 37 were lost, highlighting robust communication capabilities.

- **Navigation Success:** The UAS successfully followed 64 out of 94 waypoints across four different flight plans, demonstrating its reliable navigation capabilities.

- **UAS Detection Algorithm:** Regrettably, the team was unable to test their UAS detection algorithm during this project.

## Funding

- The team expressed gratitude for receiving a grant from NASA through the Missouri Space Grant Consortium, which significantly contributed to the success of their UAS project.

This summary provides a glimpse into Saint Louis University's impressive SUAS 2023 project as showcased in their video presentation. For more details or to connect with the team, please refer to their official communication channels. Your interest and support for their project are greatly appreciated.

## Literature Cited

YouTube. (2023). YouTube. Retrieved September 28, 2023, from https://www.youtube.com/watch?v=9MQUOILc-XM&amp;list=PLelb3ZzP70dQa_RKuvNC5fHli9hd39_ku&amp;index=26&amp;ab_channel=SUASCompetition.
