# SNT-ddos Simulated Network Traffic (SNT) DDoS Detection Dataset Using Mininet and Ryu


Dataset Overview
This dataset was created to aid the development of machine learning models for detecting Distributed Denial of Service (DDoS) attacks in a Software-Defined Networking (SDN) environment. It includes both normal and malicious network traffic, generated in a controlled, simulated network environment using Mininet (for network simulation) and the Ryu SDN controller (for managing traffic flow).

The dataset contains 1,034,669 records of network traffic flows:

527,576 benign flows (normal traffic).
507,093 malicious flows (DDoS attacks).
It provides a detailed feature set of 22 features, capturing flow-level statistics that are crucial for understanding network behavior and training machine learning models.

Dataset Highlights
Source: Simulated network traffic in Mininet with Ryu SDN controllers.
Purpose: To facilitate research on DDoS detection and mitigation using machine learning techniques.
File Format: CSV, labeled for ML tasks.
Traffic Types:
Normal Traffic: Generated using randomized client-server interactions.
Malicious Traffic: Includes various types of DDoS attacks such as ICMP flood, UDP flood, TCP SYN flood, and LAND attacks.
Traffic Generation Process
1. Normal Traffic Generation
A Python script was used to simulate realistic, randomized client-server network behavior:

Network Configuration:
Multiple hosts and switches connected in a topology, simulating a typical data center network.
Realistic Traffic Patterns:
Traffic was enriched with data center-like traffic patterns and randomized intervals to mimic unpredictable real-world behavior.
Data sizes were distributed as follows:
18%: < 0.1 KB
38%: 0.1–10 KB
90%: < 1 MB
Remainder: < 10 MB
Traffic Labeling:
All captured data labeled as normal traffic (1).
Data Export:
The traffic flows were saved as CSV for further use.
2. Malicious Traffic Generation
To simulate malicious traffic, various DDoS attacks were launched:

Network Topology:
A network of hosts and switches was configured using Mininet, with Ryu managing traffic.
Attack Simulation:
Tools such as hping3 were used to launch attacks, including:
ICMP flood
UDP flood
TCP SYN flood
LAND attack
Randomized Behavior:
Attack intervals, target IPs, and attack types were varied to create diverse, realistic traffic patterns.
Traffic Labeling:
All malicious traffic labeled as DDoS traffic (0) and optionally categorized by attack type.
Data Export:
The dataset was saved as a CSV file.
Dataset Features
The dataset provides 22 flow-level features, enabling comprehensive analysis of network traffic patterns. These features include:

Source/Destination IP
Protocol Type
Packet Counts
Byte Counts
Traffic Duration
Potential Use Cases
DDoS Detection and Mitigation:
Train machine learning models to accurately identify and classify DDoS attacks.
Feature Analysis:
Evaluate feature importance for DDoS detection using techniques like Gini Index or Information Gain.
SDN Security Research:
Explore the impact of DDoS attacks on SDN controller performance.
Dataset Details
Total Records: 1,034,669
Benign Flows: 527,576
Malicious Flows: 507,093
File Format: CSV
Use Cases: Supervised ML tasks (classification).
Why Use This Dataset?
This dataset provides a rich set of labeled network flows that simulate realistic network and attack scenarios. Its balanced distribution of normal and malicious traffic and comprehensive feature set make it an excellent resource for researchers working on network security and machine learning for DDoS detection.

We used the cache size of the files mentioned in reference (1) as normal files.

1. Roy, Arjun, et al. "Inside the social network's (datacenter) network." Proceedings of the 2015 ACM Conference on Special Interest Group on Data Communication. 2015.

