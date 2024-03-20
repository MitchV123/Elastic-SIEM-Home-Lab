# Elastic Security Information & Event Manager (SIEM) Home Lab

## Objective

The Elastic SIEM Home Lab provides a controlled environment for simulating and detecting security events on host machines. The primary focus is to collect and analyze logs within a SIEM deployment created through the Elastic Stack. This hands-on experience was designed to provide a space to practice utilization of a SIEM and deepen understanding of network security, attack patterns, and defensive strategies.

### Skills Learned

- Basic understanding of SIEM concepts and practical application.
- Experience with analyzing and interpreting network logs.
- Ability to generate and recognize basic attack signatures and patterns.
- Development of critical thinking and problem-solving skills in cybersecurity.

### Tools Used

- Elastic Stack SIEM for log ingestion and analysis.
  - Kibana for viewing the data
  - Integrations for telemtry generation
- VirtualBox to deploy a Kali Linux virtual machine (VM)
- Nmap via Linux terminal to generate security events

## Process
(NOTE: reference screenshots have been added where applicable with reference numbers above each image. Specific areas have been outlined in red to draw attention to the particular action taken.)
</br>
</br>

#### Step 1:
Gathered tools needed for the lab: Created an account and started a free trial on Elastic's web portal. Then downloaded the pre-configured Kali Linux VirtualBox VM and imported the file into VirtualBox for use on my host machine. (Kali Linux was chosen to use as the endpoint for generating telemetry for this lab because it has Nmap pre-installed)
</br>
</br>
</br>

#### Step 2:
Established the SIEM instance by creating a deployment in the Elastic web portal (Ref 2.1). 
#### (Ref 2.1)
![SIEM_Step2](https://github.com/MitchV123/Elastic-SIEM-Home-Lab/assets/163186778/14134b80-08a8-43de-8f2b-2b9a52203b4e)
</br>
</br>
</br>

#### Step 3:
Started up the Kali box to install and set up the agent for log collection.
</br>
</br>
</br>

#### Step 4:
Logged into Elastic on the Kali machine. Navigated to Kibana to install and setup the integration on the VM (Ref 4.1). "Elastic Defend" was the integration used for this lab because it collects security data from host machines and provides visibility of security events(Ref 4.2 & 4.3). 
#### (Ref 4.1)
![SIEM_Step4-1](https://github.com/MitchV123/Elastic-SIEM-Home-Lab/assets/163186778/cd8e99fb-ef73-4a41-8735-b033f9e2f395)
#### (Ref 4.2)
![SIEM_Step4-2](https://github.com/MitchV123/Elastic-SIEM-Home-Lab/assets/163186778/94b11989-9cc0-493d-a5c1-6d10b588fac4)
#### (Ref 4.3)
![SIEM_Step4-3](https://github.com/MitchV123/Elastic-SIEM-Home-Lab/assets/163186778/87aa315d-0441-4e30-b9ee-5dbd98f805a0)
</br>
</br>
</br>

#### Step 5
Once the specific agent is chosen, Elastic provides instructions on what commands to run in order to install and setup the agent properly (Ref 5.1 & 5.2). The commands were copied and ran in the Kali box terminal (Ref 5.3).
#### (Ref 5.1)
![SIEM_Step5-1](https://github.com/MitchV123/Elastic-SIEM-Home-Lab/assets/163186778/a1d3663d-bd01-4134-ae63-26bfe02943c6)
#### (Ref 5.2)
![SIEM_Step5-2](https://github.com/MitchV123/Elastic-SIEM-Home-Lab/assets/163186778/599ce189-2662-46a8-a341-5bb3269a436b)
#### (Ref 5.3)
![SIEM_Step5-3](https://github.com/MitchV123/Elastic-SIEM-Home-Lab/assets/163186778/647276c5-a316-4fe9-8e6e-91b8cc3edb9b)
</br>
   - Ran a command to do a quick check to make sure the agent was installed correctly and running (Ref 5.4)
#### (Ref 5.4)
![SIEM_Step5-4](https://github.com/MitchV123/Elastic-SIEM-Home-Lab/assets/163186778/5a2a8922-5aff-43dc-a818-eb78913c6223)
</br>
</br>
</br>

6.) Once it was established that the agent was up and running, several Nmap scans were run on the Kali machine to start generating telemtry to the SIEM.
#### (Ref 6.1)
![SIEM_Step6](https://github.com/MitchV123/Elastic-SIEM-Home-Lab/assets/163186778/ec715093-9a89-48b5-ac2c-6051c99b0117)
</br>
</br>
</br>

#### Step 7
Checked the logs in the Elastic deployment to determine whether the agent was collecting data (Ref 7.1).
#### (Ref 7.1)
![SIEM_Step7](https://github.com/MitchV123/Elastic-SIEM-Home-Lab/assets/163186778/0e1a8ae2-82dd-4e58-a768-3789addb0bd5)
</br>
</br>
</br>

#### Step 8
Observed detailed view of several logs (by clicking on 3 dots on right side of log entry and selecting "View Details") to determine some queries to use to filter the logs (Ref 8.1).
#### (Ref 8.1)
![SIEM_Step8](https://github.com/MitchV123/Elastic-SIEM-Home-Lab/assets/163186778/33cb6e0e-36a7-4af0-bff8-0e14f2443d5c)
</br>
</br>
</br>

#### Step 9
Tested a few queries (Ref 9.1)
#### (Ref 9.1)
![SIEM_Step9](https://github.com/MitchV123/Elastic-SIEM-Home-Lab/assets/163186778/9e0fb061-cf73-40ed-bdf7-87a51dcac5c9)
</br>
</br>
</br>

#### Step 10
Created a dashboard to visualize the data that was being collected (Process shown in Ref 10.1 - 10.5)
#### Ref 10.1
![SIEM_Step10 1](https://github.com/MitchV123/Elastic-SIEM-Home-Lab/assets/163186778/523a1aec-b612-4201-8928-6324e255b90e)
#### Ref 10.2
![SIEM_Step10 2](https://github.com/MitchV123/Elastic-SIEM-Home-Lab/assets/163186778/a1526428-5463-4c10-b71b-3aa0713df26a)
#### Ref 10.3
![SIEM_Step10 3](https://github.com/MitchV123/Elastic-SIEM-Home-Lab/assets/163186778/ce70369c-92fb-4722-ac1c-b16a78675c8a)
#### Ref 10.4
![SIEM_Step10 4](https://github.com/MitchV123/Elastic-SIEM-Home-Lab/assets/163186778/4e2e2f5f-5d11-4595-ba85-2ffed0fd649f)
#### Ref 10.5
![SIEM_Step10 5](https://github.com/MitchV123/Elastic-SIEM-Home-Lab/assets/163186778/776778d8-fee9-47a1-9b43-d250f055acf4)
</br>
</br>
</br>

#### Step 11
Created an alert to detect specific security events. (Process shown in Ref 11.1 - 11.5)
#### Ref 11.1
![SIEM_Step11 1](https://github.com/MitchV123/Elastic-SIEM-Home-Lab/assets/163186778/6118e0eb-8e4a-4a41-b5ed-ade0fc7fee44)
#### Ref 11.2
![SIEM_Step11 2](https://github.com/MitchV123/Elastic-SIEM-Home-Lab/assets/163186778/1ad2e56e-6639-451c-a67b-07e21e939cba)
#### Ref 11.3
![SIEM_Step11 3](https://github.com/MitchV123/Elastic-SIEM-Home-Lab/assets/163186778/85c0d5b2-68bc-45d5-ad74-6578a846a761)
#### Ref 11.4
![SIEM_Step11 4](https://github.com/MitchV123/Elastic-SIEM-Home-Lab/assets/163186778/2165419a-a02b-4609-9238-37a04c91bd5d)
#### Ref 11.5
![SIEM_Step11 5](https://github.com/MitchV123/Elastic-SIEM-Home-Lab/assets/163186778/59769611-48a1-431f-9a99-b79498b1d08f)
