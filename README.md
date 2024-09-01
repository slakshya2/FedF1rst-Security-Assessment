# FedF1rst Security Assessment: Securing the Perimeter

## Project Overview
The "FedF1rst Security Assessment" project aims to design and implement a secure network architecture that protects sensitive data and resources from potential threats. This project focuses on identifying security vulnerabilities, implementing a secure network design, and utilizing continuous monitoring techniques to ensure ongoing security compliance.

## Table of Contents
- [Section One: Designing a Secure Network Architecture](#section-one-designing-a-secure-network-architecture)
- [Section Two: Building a Secure Network Architecture in Azure](#section-two-building-a-secure-network-architecture-in-azure)
- [Section Three: Continuous Monitoring with a SIEM](#section-three-continuous-monitoring-with-a-siem)
- [Section Four: Zero Trust](#section-four-zero-trust)
- [Conclusion](#conclusion)

## Section One: Designing a Secure Network Architecture

### Security Problems Identified
1. **Problem 1: Lack of Network Segmentation**
   - **Risk:** Without proper segmentation, an attacker gaining access to one part of the network could easily move laterally to other parts, increasing the risk of data breaches.

2. **Problem 2: Inadequate Firewall Placement**
   - **Risk:** Firewalls not placed strategically can leave critical assets exposed to external threats, making it easier for unauthorized access to occur.

3. **Problem 3: Unsecured File Storage Server**
   - **Risk:** If the file storage server lacks secure connection methods (e.g., VPN), sensitive data could be intercepted during transmission, leading to data leaks.

### Network Diagram
*The diagram illustrates the segmented network zones, strategic firewall placements, and secure connection methods for the file storage server.*

### Security Principles
- **Principle 1:** [Description of the first security principle and its benefits.]
- **Principle 2:** [Description of the second security principle and its benefits.]
- **Principle 3:** [Description of the third security principle and its benefits.]

## Section Two: Building a Secure Network Architecture in Azure

### Azure VNets and Subnets
- **Screenshots:** 
  - ![DMZ VNet](path/to/your/dmz_vnet_screenshot.png)
  - ![Internal VNet](path/to/your/internal_vnet_screenshot.png)

*The screenshots demonstrate the creation of two Azure VNets: DMZ (containing Public-DMZ and Private-DMZ subnets) and Internal (containing Internal-Subnet).*

### Security Rules Setup
- **Public-DMZ Subnet:** Ports 80 (HTTP) and 443 (HTTPS) are opened for inbound connections.
- **Private-DMZ Subnet:** Only MySQL (3306) connections from the Public-DMZ are allowed, with all other connections denied.

## Section Three: Continuous Monitoring with a SIEM

### Benefits of SIEM
1. **Benefit 1: Real-time Threat Detection**
   - SIEM systems provide real-time monitoring and alerts for suspicious activities, enabling quick response to potential threats.

2. **Benefit 2: Centralized Log Management**
   - By aggregating logs from various sources, SIEM systems facilitate easier analysis and compliance reporting.

3. **Benefit 3: Enhanced Incident Response**
   - SIEM tools streamline incident response processes, allowing security teams to investigate and remediate threats more effectively.

### VM Deployment
- **Screenshots:** 
  - ![Elk-Server Deployment](path/to/your/elk_server_screenshot.png)
  - ![Filebeat-VM Deployment](path/to/your/filebeat_vm_screenshot.png)

*The screenshots verify the deployment of the Elk-Server and Filebeat-VM within their designated subnets.*

### Updated Security Rules
- **Private-DMZ Security Rules:** 
  - Public access to ports 22 (SSH) and 5601 (Kibana).
  - Access to ports 9200 (Elasticsearch) and 5044 (Filebeat) only from the Public-DMZ subnet.
- **Screenshot:** 
  - ![Updated Private-DMZ Rules](path/to/your/updated_private_dmz_rules.png)

*This screenshot shows the updated network security rules allowing the specified access for the SIEM components.*

### Service Verification
- **Screenshots:** 
  - ![Filebeat Service Running](path/to/your/filebeat_running_screenshot.png)
  - ![Kibana Logs](path/to/your/kibana_logs_screenshot.png)

*These screenshots demonstrate that the Filebeat service is running on the web server and that Kibana is receiving logs from it.*

## Section Four: Zero Trust

### Comparison with Traditional Models
- **Zero Trust Principle 1:** [Comparison and benefits]
- **Zero Trust Principle 2:** [Comparison and benefits]
- **Zero Trust Principle 3:** [Comparison and benefits]

### Justification for Zero Trust Model
- **Selected Model:** [Name of the chosen Zero Trust model]
- **Justification:** This model addresses XYZ’s specific security challenges by [explain how it addresses challenges] and aligns with XYZ’s security objectives by [explain alignment with objectives].

## Conclusion
The "FedF1rst Security Assessment" project successfully identifies critical security vulnerabilities and implements a robust network architecture designed to protect sensitive information. Continuous monitoring and the adoption of Zero Trust principles further enhance the security posture, ensuring ongoing protection against evolving threats.
