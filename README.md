# Elastic Security Information & Event Manager (SIEM) Home Lab

## Objective

The Elastic SIEM Home Lab provides a controlled environment for simulating and detecting security events on host machines. The primary focus is to collect and analyze logs within a SIEM deployment created through the Elastic Stack. This hands-on experience was designed to provide a space to practice utilization of a SIEM and deepen understanding of network security, attack patterns, and defensive strategies.

### Skills Learned

- Basic understanding of SIEM concepts and practical application.
- Experience with analyzing and interpreting network logs.
- Ability to generate and recognize attack signatures and patterns.
- Enhanced knowledge of network protocols and security vulnerabilities.
- Development of critical thinking and problem-solving skills in cybersecurity.

### Tools Used

- Elastic Stack SIEM for log ingestion and analysis.
  - Kibana for viewing the data
  - Integrations for telemtry generation
- VirtualBox to deploy a Kali Linux virtual machine (VM)
- Nmap via Linux terminal to generate security events

## Process

1.) Gathered tools needed for the lab: Created an account and started a free trial on Elastic's web portal. Then downloaded the pre-configured Kali Linux VirtualBox VM and imported the file into VirtualBox for use on my host machine. (Kali Linux was chosen to use as the endpoint for generating telemetry for this lab because it has Nmap pre-installed)


2.) Established the SIEM instance by creating a deployment in the Elastic web portal. 


3.) Started up the Kali box to install and set up the agent for log collection.


4.) Logged into Elastic on the Kali machine. Navigated to Kibana to install and setup the integration on the VM. "Elastic Defend" was the integration used for this lab because it collects security data from host machines and provides visibility of security events. 


5.) Once the specific agent is chosen, Elastic provides instructions on what commands to run in order to install and setup the agent properly. The commands were copied and ran in the Kali box terminal.
    - Ran a command to do a quick check to make sure the agent was installed correctly and running


6.) Once it was established that the agent was up and running,several Nmap scans were run on the Kali machine to start generating telemtry to the SIEM.


7.) Checked the logs in the Elastic deployment to determine whether the agent was collecting data.


8.) Observed detailed view of several logs to determine some queries to use to filter the logs


9.) Tested a few queries


10.) Created a dashboard to visualize the data that was being collected


11.) Created an alert to detect specific security events. 

