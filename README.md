# IDS-Integration-with-SIEM-for-Intrusion-Detection-and-Monitoring
## Project Overview

This project focuses on integrating an Intrusion Detection System (IDS) with a Security Information and Event Management (SIEM) solution to detect and monitor security threats in a simulated network environment. By setting up a virtualized environment that mimics real-world attack and defense scenarios, this project provides hands-on experience in intrusion detection, security event monitoring, and log analysis. The goal is to understand how IDS and SIEM tools work together to identify and mitigate security threats effectively.


## Environment Setup

The virtual network environment consists of:

- **Kali Linux (Attacker)** - Configured with NAT networking for controlled attack simulations.

- **Ubuntu Server (Hosting Splunk)** - Also set to NAT networking for secure communication.

- **Ubuntu PC (Running Snort and forwarding logs to Splunk)** - Runs in a bridged network with INetSim to provide network services simulation.

- **Metasploitable2 (Vulnerable machine for attack simulations)** - Connected via a bridged adapter for realistic network interactions.

## Implementation Details

1. **Network Configuration:** Set up the virtual network to simulate real-world attack scenarios using a mix of NAT and bridged networking.

2. **Snort Installation & Configuration:**

    - Installed Snort on Ubuntu.

    - Created and implemented custom intrusion detection rules.

    - Configured Snort to generate alert logs for security events.

3. **Splunk Deployment:**

    - Installed and configured Splunk on Ubuntu Server.

    - Integrated Snort logs with Splunk for centralized monitoring.

4. **Attack Simulations:**

    - Used Kali Linux to execute penetration tests against Metasploitable2.

    - Captured intrusion attempts via Snort and analyzed alerts in Splunk.

5. **Security Event Analysis:**

    - Configured a Splunk dashboard to visualize Snort alerts.

    - Monitored and identified potential security threats.

## Tools & Technologies Used

- Snort (Network Intrusion Detection System)
- Splunk (SIEM for log analysis and monitoring)
- Kali Linux (Penetration testing)
- Metasploitable2 (Vulnerable machine for attack simulations)
- Ubuntu Server & PC (Hosting IDS and SIEM components)
- INetSim (Network service simulation for better attack analysis)

## How to Use

### 1. **Set Up the Virtual Machines**

  - Install and configure Kali Linux, Ubuntu Server, Ubuntu PC, and Metasploitable2.

  - Configure networking:
      - Kali Linux and Ubuntu Server should use NAT.

      - Ubuntu PC (Snort) and Metasploitable2 should use Bridged Adapter with INetSim.

### 2. **Install Snort & Create Rules**

  - Install Snort on Ubuntu PC.

  - Create custom Snort rules to detect potential threats.

  - Configure Snort to log alerts for Splunk ingestion.

### 3. **Deploy Splunk & Integrate Logs**

  - Install Splunk on Ubuntu Server.

  - Configure Splunk to receive logs from Snort.

  - Set up a Splunk dashboard to visualize alerts.

### 4. **Simulate Attacks**

  - Use Kali Linux to perform penetration tests:

    - Scan the network with Nmap.

    - Exploit vulnerabilities using Metasploit.

    - Generate suspicious traffic to test Snort detection.

  - Monitor Snort logs in real-time to observe triggered alerts.

### 5. **Monitor & Analyze Logs**

  - Access Splunk’s Snort dashboard.

  - Analyze security event logs.

  - Identify attack patterns and potential threats.

## Expected Outcomes

- Real-time intrusion detection and alerting.
- Effective monitoring and analysis of security events.
- Hands-on experience with IDS and SIEM integration.

## Future Enhancements

- Automating attack simulations for continuous testing.
- Enhancing Snort rules for better accuracy.
- Integrating additional log sources into Splunk.
- Implementing threat intelligence feeds for better detection.
  
## References

- [Snort Documentation](https://www.snort.org/documents)
- [Splunk Documentation](https://docs.splunk.com/Documentation/Splunk)
- [Kali Linux Tools](https://www.kali.org/tools/)

