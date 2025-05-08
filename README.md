# Project-Oddity

**Introduction:**

The Oddity project proposal aims to advance space exploration by developing a cutting-edge Mars rover. Inspired by the achievements of ISRO, NASA, and university competitions like ERC and URC, our team is driven to pioneer new frontiers in robotic exploration.
Mars exploration offers unique insights into the planet's geological history and the potential for extraterrestrial life. This project seeks to design, build, and deploy a sophisticated Mars rover equipped with state-of-the-art technologies.


**Motivation:**

Our project is driven by the following motivations:

Scientific Exploration: A well-equipped rover can provide valuable data on Martian geology, climate, and the possibility of past or present life, offering clues about the origins of our solar system.
Technological Innovation: Developing a Mars rover pushes the boundaries of current robotic technologies, incorporating innovations in autonomy, communication, and power systems.
Inspiring Future Generations: Our project aims to inspire the next generation of space explorers through engagement with students, collaboration, and outreach activities.
International Collaboration: By securing funding, we aim to establish partnerships with research institutions, space agencies, and industry leaders, fostering international cooperation in the pursuit of scientific knowledge.


**Broad Objectives:**

The broad objective of the Oddity rover proposal is that our rover ‘ODDITY’ will have the following subsystems:

1. Control and Processing Subsystem (C.P.S.): The Processing Subsystem is the brain of Oddity, ensuring seamless integration and execution of complex activities. It consolidates data from rover sensors, cameras, and other input devices using an NVIDIA Jetson Xavier-NX, providing high processing capacity for sophisticated control algorithms in real-time.

Sensor Integration: This subsystem integrates data from various sensors, including FPV and stereo cameras, IMU sensors, and 2-D LIDAR, utilizing advanced sensor fusion techniques like Kalman and Extended Kalman Filtering for a comprehensive understanding of the rover's surroundings.
Control Algorithms: It executes intricate control algorithms, such as PID and PI, governing the rover's movements and responses to external stimuli, ensuring effective decision-making processes.
Real-time Processing: The subsystem ensures low-latency processing for real-time decision-making, essential for navigating and responding to challenges in dynamic and uneven terrains.
Communication Interface: It facilitates seamless communication with other subsystems via Controller Area Network (CAN) for efficient coordination and data exchange. It also interfaces with the Communication Subsystem to relay information to the base station and receive remote commands.
2. Autonomous Navigation Subsystem(A.N.S.): The Autonomous Navigation Subsystem handles Oddity's autonomous navigation over rough terrains using the following tools:

Decision-Making Algorithms: Utilizing Simultaneous Localization and Mapping (SLAM) and sensor fusion between 2-D LIDAR and an Intel Realsense D457 stereo camera with Extended Kalman Filtering, this subsystem enhances obstacle avoidance and autonomous roving capabilities.
Adaptive Control: Adaptive control algorithms adjust the rover's speed, direction, and behavior in real time based on terrain, lighting, and other environmental conditions, ensuring optimal performance in varying and unforeseen situations.
Integration with Processing Subsystem: Seamless connection with the Processing Subsystem allows for real-time data processing, enabling quick decision-making and course corrections.
Image Processing for ARUCO Tag Localization: Incorporates image processing algorithms to detect and localize ARUCO tags. The navigation module uses this information to determine the rover's relative position and orientation, enabling precise navigation towards the tags.

3. Drive Subsystem(D.S.): Our team will develop this subsystem, encompassing meticulously designed mechanical components that define the rover's movement, stability, and adaptability.[1]
Chassis Design: A rough CAD model for Oddity’s chassis has been developed and will be further analyzed for structural integrity using ANSYS.
Wheel and Suspension System: Oddity features a six-wheel rocker-bogie suspension system, providing greater maneuverability and precise roving over harsh terrains.

4. Communication Subsystem(C.S.): Oddity will use 5 GHz, 2.4 GHz and 900 MHz bandwidths for communication with various subsystems. The 5 GHz band, known for its low latency, will transmit FPV camera feed and sensor data will be sent to the base station via 2.4 GHz channel. The 900 MHz band, with its longer range and reduced interference, will transmit commands from the base station to the rover. During latency in the 900 MHz channel, the base station commands will be transmitted via 2.4 GHz channel after multiplexing the two input frequency channels at the base station. Commands will be sent using a TBS Crossfire Nano Tx, with a  TBS Crossfire Nano Rx unit present on the rover. A 2x2 Dual-Polarity MIMO Ubiquiti AMO-5G10 Omnidirectional antenna, paired with a Rocket-M5 at both the rover and base station ends, will handle video and sensor data transmission.

5. Manipulator and Sample Collection and Identification (M.S.C.I.) Subsystem: The MSCI subsystem features a 6 D.O.F. serial manipulator responsible for sample collection task.
Robotic Arm Design: The arm links are made of lightweight aluminum to meet Oddity's design requirements and can handle a payload of about 500 grams. It uses a two-fingered end effector for  sample collection.
Actuation and Control: Servo-actuated joints provide 6 degrees of freedom for smooth manipulation. PID control , using feedback data from the arm’s servo, ensures precise control.

6. Electrical and Power Subsystem (E.P.S.): The Power Subsystem provides electrical power to all components, balancing energy efficiency, weight, and the rover's diverse functionalities.
Power Distribution System:Five 22.2V, 5200 mAh, 35C , 6S Lithium-Polymer batteries will power the rover. These batteries are chosen for their higher charging capacity and rechargeability. Efficient power management circuits, including battery management systems, over and under-voltage protection, DC-DC buck converters, and power amplifiers, will ensure at least 1 hour of continuous operation, meeting competition requirements. A kill switch will be present for emergency shutdowns. The rover’s internal circuitry will be designed for minimal power consumption and effective distribution.[6]
Thermal Management:The rover’s electronics box will have constant thermal monitoring, maintaining an optimal temperature using exhaust fans.

7. Science Subsystem(S.S.): The Science Subsystem tests soil and rock samples on the interplanetary surface, analyzing compositions and environmental conditions.
Instrument Operation: A Raspberry Pi 5 processes data from various scientific instruments, including gas, alcohol, formaldehyde, UV, and RGB color sensors.
Sample Collection: Equipped with a custom-made drill bit, extraction tools, and a rotating collection drum with chambers, the subsystem collects soil and rock samples, ensuring no cross-contamination.
Sample Analysis: Tools like a USB microscope and chemical reagents analyze soil and rock samples, providing valuable information about the terrain’s composition.
Remote Sensing: Using cameras and spectrometers, the subsystem performs remote sensing to study the terrain’s topography and atmospheric conditions.[7]
Data Processing and Storage: The Raspberry Pi processes and stores collected data, converting raw sensor inputs into usable scientific information. Machine learning models classify rocks based on grain patterns, and onboard tests with chemical reagents detect extinct or extant life.

