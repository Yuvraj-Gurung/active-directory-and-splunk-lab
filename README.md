# **Active Directory and Splunk Cybersecurity Lab**

## **Project Overview**  
The purpose of this project is to integrate **Active Directory (AD)** with **Splunk** for efficient security monitoring and threat detection. The setup involves **Windows Server 2022, Windows 10, Ubuntu Server**, and key security tools such as **Sysmon, Atomic Red Team, and Splunk** to simulate real-world attack scenarios and analyze security events.


## **Architecture Diagram**  
### Components Involved:
1. **Windows Server 2022** – AD Domain Controller (DC)
2. **Windows 10** – Client machine (part of AD domain)
3. **Ubuntu Server** – Splunk Enterprise / Server
4. **Splunk** – Security Information and Event Management (SIEM)
5. **Sysmon** – System Monitoring to log critical events
6. **Atomic Red Team** – Simulates adversarial techniques for testing defenses


## **Installation & Configuration Guide**  
### **1. Setting Up Active Directory (AD) on Windows Server 2022**  
1. Install Active Directory Domain Services (AD DS).
2. Configure the domain (e.g., 'testlab.local').
3. Add a Windows 10 machine to the AD domain.
4. Set up **Group Policies (GPOs)** for security enhancements.

### **2. Installing and Configuring Splunk**  
1. Download and install **Splunk Enterprise** on Ubuntu Server.
2. Configure Splunk **forwarders** on Windows Server 2022 and Windows 10 to collect logs.
3. Create Splunk **data inputs** for Active Directory event logs.

### **3. Deploying Sysmon for Enhanced Logging**  
1. Install **Sysmon** on both Windows Server and Windows 10 clients.
2. Configure a robust **Sysmon configuration file** (such as [SwiftOnSecurity's config](https://github.com/SwiftOnSecurity/sysmon-config)).
3. Verify that Sysmon logs critical security events (process creation, file access, registry modifications).

### **4. Using Atomic Red Team for Adversary Simulation**  
1. Install **Atomic Red Team** (`Invoke-Atomic` PowerShell module).
2. Run specific attack simulations (e.g., **Privilege Escalation, Credential Dumping**).
3. Validate logs in **Splunk** to check for detections.

### **5. Analyzing Logs & Building Dashboards in Splunk**  
1. Query logs for **failed login attempts, privilege escalation, persistence mechanisms**.
2. Develop **Splunk dashboards** for real-time monitoring.
3. Create **correlation searches** to detect suspicious activities.


## **Testing & Validation**  
- Perform **login brute-force attacks** and check logs.
- Simulate **malicious PowerShell executions** and ensure they are logged.
- Validate that Splunk **alerts** trigger on **suspicious activities**.


## **Conclusion**  
This project demonstrates how to integrate **Active Directory with Splunk** for effective cybersecurity monitoring. By utilizing **Sysmon and Atomic Red Team**, SOC analysts can **simulate attacks, analyze threats, and improve defenses** in a Windows environment.


## *Walkthrough | Screenshots*

**Installing Windows Server 2022**

<img src="project/image1.png"> <img src="project/image2.png"> <img src="project/image3.png"> <img src="project/image4.png"> <img src="project/image5.png"> <img src="project/image6.png"> <img src="project/image7.png"> <img src="project/image8.png"> <img src="project/image9.png"> <img src="project/image10.png"> <img src="project/image11.png"> <img src="project/image12.png"> <img src="project/image13.png"> <img src="project/image14.png">

**Installing Windows 10**

<img src="project/image15.png"> <img src="project/image16.png"> <img src="project/image17.png"> <img src="project/image18.png"> <img src="project/image19.png"> <img src="project/image20.png"> <img src="project/image21.png"> <img src="project/image22.png"> <img src="project/image23.png"> <img src="project/image24.png"> <img src="project/image25.png"> <img src="project/image26.png"> <img src="project/image27.png"> <img src="project/image28.png">


**Ubuntu Server 24.04.1 Installation**

<img src="project/image29.png"> <img src="project/image30.png"> <img src="project/image31.png"> <img src="project/image32.png"> <img src="project/image33.png"> <img src="project/image34.png"> <img src="project/image35.png"> <img src="project/image36.png"> <img src="project/image37.png"> <img src="project/image38.png"> <img src="project/image39.png"> <img src="project/image40.png"> <img src="project/image41.png"> <img src="project/image42.png"> <img src="project/image43.png">


**Splunk Installation**

<img src="project/image44.png"> <img src="project/image45.png"> <img src="project/image46.png"> <img src="project/image47.png"> <img src="project/image48.png"> <img src="project/image49.png"> <img src="project/image50.png"> <img src="project/image51.png"> <img src="project/image52.png">


**Splunk Universal Forwarder/Sysmon Installation**

<img src="project/image53.png"> <img src="project/image54.png"> <img src="project/image55.png"> <img src="project/image56.png"> <img src="project/image57.png"> <img src="project/image58.png"> <img src="project/image59.png"> <img src="project/image60.png"> <img src="project/image61.png"> <img src="project/image62.png"> <img src="project/image63.png"> <img src="project/image64.png"> <img src="project/image65.png">


**Splunk Configuration**

<img src="project/image66.png"> <img src="project/image67.png"> <img src="project/image68.png"> <img src="project/image69.png"> <img src="project/image70.png"> <img src="project/image71.png"> <img src="project/image72.png"> <img src="project/image73.png"> <img src="project/image74.png"> <img src="project/image75.png"> <img src="project/image76.png"> <img src="project/image77.png"> <img src="project/image78.png">


**Active Directory Configuration/Installing Active Directory Domain Services/Joining Windows 10 to a Domain**

<img src="project/image79.png"> <img src="project/image80.png"> <img src="project/image81.png"> <img src="project/image82.png"> <img src="project/image83.png"> <img src="project/image84.png"> <img src="project/image85.png"> <img src="project/image86.png"> <img src="project/image87.png"> <img src="project/image88.png"> <img src="project/image89.png"> <img src="project/image90.png"> <img src="project/image91.png"> <img src="project/image92.png"> <img src="project/image93.png"> <img src="project/image94.png"> <img src="project/image95.png"> <img src="project/image96.png"> <img src="project/image97.png"> <img src="project/image98.png"> <img src="project/image99.png"> <img src="project/image100.png"> <img src="project/image101.png"> <img src="project/image102.png"> <img src="project/image103.png"> <img src="project/image104.png"> <img src="project/image105.png"> <img src="project/image106.png"> <img src="project/image107.png"> <img src="project/image108.png"> <img src="project/image109.png"> <img src="project/image110.png"> <img src="project/image111.png"> <img src="project/image112.png"> <img src="project/image113.png"> <img src="project/image114.png"> <img src="project/image115.png"> <img src="project/image116.png"> <img src="project/image117.png"> <img src="project/image118.png"> <img src="project/image119.png"> <img src="project/image120.png"> <img src="project/image121.png"> <img src="project/image122.png"> <img src="project/image123.png"> <img src="project/image124.png">


**Atomic Red Team Installation**

<img src="project/image125.png"> <img src="project/image126.png"> <img src="project/image127.png"> <img src="project/image128.png">


**MITRE ATT&CK FRAMEWORK**

<img src="project/image129.png"> <img src="project/image130.png">

**Running Atomic Red Team Tests/Viewing Logs_Alerts in Splunk**

<img src="project/image131.png"> <img src="project/image132.png"> <img src="project/image133.png"> <img src="project/image134.png"> <img src="project/image135.png">











