## Literature Survey

Building an **energy-efficient hybrid Intrusion Detection System (IDS)** for new-age vehicles, especially for **Electric Vehicles (EVs)** or **Autonomous Vehicles (AVs)**, requires focusing on multiple dimensions. This combination of cybersecurity, vehicular networks, and energy efficiency can be a complex but promising area. Here’s an outline to guide you through feasibility, scope, applications, difficulties, and shortcomings.

### Key Focus Areas:

1. **Hybrid IDS Design**:
    - **Signature-based Detection**: Focuses on known threats, allowing for quick detection of established attack patterns.
    - **Anomaly-based Detection**: Identifies abnormal behavior, offering protection against new or unknown threats.
    - **Energy-Efficient Algorithms**: Design detection algorithms that reduce computational overhead, ideally with real-time capabilities while preserving energy.
2. **Vehicle Communication Networks**:
    - Focus on **CAN Bus** (Controller Area Network), **Ethernet**, **V2X Communication** (Vehicle-to-Everything), and **OBD-II** systems.
    - Incorporating IDS in **ECUs** (Electronic Control Units) to monitor internal communications while ensuring minimal energy consumption.
3. **Resource Constraints**:
    - Vehicles have limited resources (CPU, memory, and power), so you need to balance detection effectiveness with low power consumption.
    - Use **lightweight cryptography** or **compressed data structures** like Bloom filters for detection.
4. **Machine Learning Integration**:
    - Use energy-efficient machine learning models (like **decision trees** or **lightweight neural networks**) for anomaly detection.
    - Consider federated learning to keep model updates efficient without constant cloud communication.
5. **Energy Efficiency**:
    - Use techniques like **sleep-mode**, where parts of the system are powered off when not in use, and wake up during abnormal traffic.
    - Optimize sensor data collection and processing to minimize the energy required to operate the IDS.
6. **Attack Surfaces in EV/AV**:
    - Consider attacks targeting sensors (e.g., LIDAR, RADAR), communication channels (Wi-Fi, Bluetooth), or the charging system.
    - Ensure coverage for both internal and external threats, including physical tampering and remote attacks.

### Feasibility:

- **Technology Availability**: The increasing use of **5G, V2X**, and **advanced vehicular networks** makes it feasible to implement real-time IDS solutions.
- **Hardware Support**: Most EVs and AVs are now built with high-performance **ECUs** and communication interfaces that can support lightweight IDS without overburdening the system.
- **Power Constraints**: Developing an energy-efficient system is feasible but challenging, especially as IDS might add computational overhead. However, hardware advancements like **TPUs (Tensor Processing Units)** for inference can alleviate this.

### Applications:

1. **Electric Vehicles (EVs)**:
    - Protecting the communication between **Battery Management Systems (BMS)**, **charging systems**, and **cloud services**.
    - Securing **OTA (Over-the-Air)** updates, navigation systems, and infotainment systems.
2. **Autonomous Vehicles (AVs)**:
    - Defending against cyberattacks on sensors like **LIDAR**, **RADAR**, or **camera feeds**, which are critical for decision-making.
    - Monitoring V2X communication to prevent attacks like **man-in-the-middle**, **replay attacks**, and **spoofing**.
3. **Fleet Management**:
    - IDS can be implemented to protect **commercial fleets** that are interconnected with backend systems for real-time monitoring, dispatching, or maintenance scheduling.

### Difficulties:

1. **Power Consumption**:
    - A hybrid IDS requires a balance between detection accuracy and power consumption. While vehicles are increasingly efficient, IDS may still contribute to non-trivial energy drain, impacting the range of EVs or AVs.
2. **False Positives and Negatives**:
    - With anomaly-based detection, you need to carefully tune the system to avoid high rates of false positives (which can disrupt normal operation) or false negatives (where threats are missed).
3. **Real-Time Processing**:
    - Vehicles operate in real-time environments where decisions (like braking) are made in milliseconds. An IDS needs to process data in near real-time, adding pressure on the processing system.
4. **Scalability**:
    - Scaling the IDS across many vehicles or fleets, while maintaining low power and processing requirements, presents a major challenge. Federated learning could reduce the burden but introduces new complexities in implementation.
5. **System Integration**:
    - Integrating IDS within the vehicle’s complex system without disrupting existing vehicle functions is tricky. You will need to ensure that IDS functions smoothly across all components, from the **ECU** to the **sensors** and communication modules.

### Shortcomings:

1. **Latency**:
    
    Hybrid IDS solutions may introduce latency, especially in resource-constrained environments like vehicles, where real-time response is essential. Latency in detection could result in security risks, especially for AVs.
    
2. **Complexity in Detection**:
    - Balancing signature-based detection for known threats with anomaly-based detection for unknown threats can be complicated, especially with a hybrid approach. Fine-tuning for performance without sacrificing accuracy is difficult.
3. **Limited Dataset Availability**:
    - Training an anomaly-based IDS requires large datasets of both normal and abnormal vehicle behavior, but data on vehicle cybersecurity incidents is scarce, making it difficult to model real-world threats.
4. **Evolving Threat Landscape**:
    - The landscape of vehicular threats is constantly evolving, especially with new connectivity technologies like **5G**, which increases the attack surface. Hybrid IDS solutions may need frequent updates to stay relevant.

### Conclusion:

Building an **energy-efficient hybrid IDS for new-age vehicles** is feasible but presents numerous challenges. The key to success will be optimizing detection algorithms to minimize energy use, leveraging machine learning intelligently, and carefully balancing security with real-time operational needs. While potential difficulties like resource constraints, system integration, and false positives exist, advancements in vehicular hardware, connectivity, and energy-efficient algorithms make this a promising and impactful project in the long term.