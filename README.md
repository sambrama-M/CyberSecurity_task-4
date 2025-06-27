# Task-4: Setup and Use a Firewall on Windows

## Objective
The goal of this task was to configure and test firewall rules on a Windows system using Windows Defender Firewall. This helps in understanding how network traffic is managed and secured using custom rules.

## Tools Used
- Windows Defender Firewall with Advanced Security (accessed via `wf.msc`)
- Windows 10/11 operating system
- A mobile device for testing (via Bluetooth)

## Summary of Steps

1. Opened Windows Firewall settings through Control Panel under "System and Security" > "Windows Defender Firewall" > "Advanced Settings".

2. Explored the three main types of firewall rules:
   - Inbound Rules: These manage incoming traffic to the system.
   - Outbound Rules: These manage outgoing traffic from the system.
   - Connection Security Rules: These use IPsec to authenticate and encrypt network traffic, ensuring secure connections rather than allowing or blocking traffic directly.

3. Created a custom inbound rule to block traffic on port 445, which is commonly associated with SMB file sharing and potential vulnerabilities. 
   - Chose to create a new rule based on a port.
   - Selected TCP as the protocol and entered 445 as the port number.
   - Chose to block the connection.
   - Applied the rule to all network profiles: Domain, Private, and Public.
   - Gave the rule a clear name for identification.

4. Tested the rule by attempting to connect to the system from a mobile device via Bluetooth. The connection was successfully blocked, confirming that the rule was applied correctly.

5. Removed the rule after testing by right-clicking it in the Inbound Rules section and selecting "Delete". This restored the system to its previous state without the block.

## How Firewall Filters Traffic

Windows Firewall acts like a security checkpoint between your computer and the network. It checks each incoming and outgoing packet of data against a set of rules. If the data matches an allow rule, it is permitted; if it matches a block rule, it is denied. Rules can be based on direction (inbound or outbound), port numbers, network protocols (such as TCP or UDP), specific applications, and IP addresses. In some cases, connection security rules can also enforce encrypted and authenticated connections.

## Outcome

The task was successfully completed. A custom inbound rule was created, tested, and removed. The test confirmed that Windows Firewall effectively blocked unwanted traffic based on the specified rule, demonstrating a basic understanding of traffic control and system protection.

## Deliverables

- Screenshot of the applied firewall rule (to be attached)
- This README summarizing the task
