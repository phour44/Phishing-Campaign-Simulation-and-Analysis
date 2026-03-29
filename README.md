# Phishing Simulation and Email Analysis Project

## Overview

This project documents a controlled phishing simulation conducted inside a 22-person enterprise environment. The simulation tested user susceptibility to credential harvesting attacks, measured behavioral response rates before and after security awareness training, and used real-world phishing email samples to build detection skills.

Phase 1 was an active attack simulation using Zphisher, LocalXpose, and Ngrok to build and deliver credential-harvesting phishing pages cloned from WordPress, Adobe, and Yahoo. Phase 2 was a static email analysis exercise using Phishing Pot samples analyzed with Thunderbird, Mousepad, AbuseIPDB, URLScan.io, and VirusTotal.

---

## Objectives

- Simulate a realistic credential harvesting phishing attack in a controlled enterprise environment
- Measure user susceptibility before and after awareness training
- Demonstrate attacker toolchain setup from infrastructure to delivery to credential capture
- Analyze real-world phishing email samples to build detection skills
- Map attack techniques to MITRE ATT&CK and produce actionable recommendations

---

## Tools Used

| Tool         | Role                                                       |
|--------------|------------------------------------------------------------|
| Zphisher     | Phishing page cloning and credential capture               |
| LocalXpose   | Tunnel service to expose local phishing server publicly    |
| Ngrok        | Alternative tunnel for phishing infrastructure             |
| Phishing Pot | Repository of real-world phishing email samples            |
| Thunderbird  | Email client for rendering and inspecting phishing samples |
| Mousepad     | Text editor for raw email header inspection                |
| AbuseIPDB    | Threat intelligence lookup for sender IP addresses         |
| URLScan.io   | URL reputation and domain analysis                         |
| VirusTotal   | Multi-engine file and URL threat scanning                  |

---

## Environment

- **Organization size:** 22 employees
- **Attack type:** Credential harvesting via cloned login pages
- **Delivery method:** Email with embedded phishing URL
- **Pages cloned:** WordPress, Adobe, Yahoo
- **Infrastructure:** Local server exposed via LocalXpose and Ngrok tunnels
- **Compliance context:** ISO 27001:2022 Annex A.6.3

---

## KPI Results

| Metric | Pre-Training | Post-Training | Change |
|---|---|---|---|
| Link Click Rate | 80% | 30% | -50 percentage points |
| Credential Submission Rate | 60% | 20% | -40 percentage points |
| Incident Report Rate | 10% | 80% | +70 percentage points |

---

## Full Attack Simulation Walkthrough

### Phase 1: Zphisher Installation

#### Step 1: Download Zphisher from GitHub

Zphisher is cloned from its GitHub repository. The tool downloads to the local working directory.

![DOWNLOADING ZPHISHER TOOL FROM GITHUB](https://github.com/user-attachments/assets/e3f0b7e9-514f-45dd-9557-8cda6871968c)


---

#### Step 2: Install Zphisher — Part 1

The installation script runs. Package dependency checks and initial setup execute automatically.

![INSTALLING ZPHISHER_1](https://github.com/user-attachments/assets/d720dfa9-7be8-402f-95b4-ec21f1f10ce6)


---

#### Step 3: Install Zphisher — Part 2

Installation continues. Additional packages and environment configuration are applied.

![INSTALLING ZPHISHER_2](https://github.com/user-attachments/assets/bd79dbb7-8b6b-4d46-8743-e3b8e3ca994d)


---

#### Step 4: Zphisher Ready

The Zphisher main menu confirms successful installation.

![ZPHISHER INSTALLED](https://github.com/user-attachments/assets/c1d51480-a723-4bd7-870f-2b9e0ad421fc)


---

### Phase 2: WordPress Attack Scenario — LocalXpose Tunnel

#### Step 5: Clone WordPress Login Page

WordPress is selected from the Zphisher menu. A pixel-accurate clone is created locally.

![CLONING WORDPRESS PAGE FROM THE OPTIONS](https://github.com/user-attachments/assets/0aa447f0-7a78-41a9-b8e4-fa9df7ab3d5b)


---

#### Step 6: Select Hosting Method

LocalXpose is selected as the tunnel provider to generate a public HTTPS URL.

![OPTIONS TO HOST THE LINK](https://github.com/user-attachments/assets/0a98a5a7-9fc9-4905-8ac8-a8aaf717b98c)


---

#### Step 7: LocalXpose Homepage

The LocalXpose site is accessed to create an account and retrieve the API token.

![LOCALXPOSE HOMEPAGE](https://github.com/user-attachments/assets/a4f40a00-2de8-410f-b9c5-9486b6d6882f)


---

#### Step 8: Sign Up on LocalXpose

A new account is registered on LocalXpose to obtain tunnel access credentials.

![SIGNING UP ON LOCALXPOSE](https://github.com/user-attachments/assets/5521f340-9e48-4215-917b-62fd842b7bba)


---

#### Step 9: Navigate to Access Token Section

After login, the Access section of the LocalXpose dashboard is located.

![LOGGED INTO LOCALXPOSE_CLICKING ON ACCESS](https://github.com/user-attachments/assets/56f133ef-7845-423d-826e-4f88cdd38ba2)


---

#### Step 10: Copy the Access Token

The API token is copied from the LocalXpose dashboard to authenticate the tunnel client.

![COPYING ACCESS TOKEN ON LOCALXPOSE](https://github.com/user-attachments/assets/4a6af290-ed97-4f85-8f90-f99ff88938df)


---

#### Step 11: Save Token in Text Editor

The token is pasted into a text editor for reference during Zphisher configuration.

![ACCESS TOKEN PASTED AND SAVED IN TEXT EDITOR](https://github.com/user-attachments/assets/cd244971-fb49-4f65-a451-5d454eb9d676)


---

#### Step 12: Select Localhost Option in Zphisher

Localhost 1 is selected inside Zphisher, paired with LocalXpose for external tunnel access.

![CHOSING LOCAL HOST 1](https://github.com/user-attachments/assets/fb7d7ba1-4e46-4918-90e0-6928b72846c8)


---

#### Step 13: Tunnel Configuration — In Progress

The LocalXpose access token is entered. Zphisher initiates the tunnel.

![CONFIGURING LOCAL HOST SELETED TO HOST LINK](https://github.com/user-attachments/assets/77a6ecdb-cb58-415a-9e31-e60f828bdb0b)


---

#### Step 14: Tunnel Configuration Complete

The LocalXpose tunnel is established. The WordPress phishing page is publicly accessible.

![CONFIGURING LOCAL HOST SELETED TO HOST LINK_DONE](https://github.com/user-attachments/assets/0c6db75a-8df7-4d79-86eb-6cee4ff081af)


---

#### Step 15: Copy the Phishing URL

Zphisher displays the active phishing URL. The link is copied for use in the phishing email.

![COPY LINK CREATED ](https://github.com/user-attachments/assets/dd9325f2-4b30-40f3-8dfa-07830a989970)


---

### Phase 3: Email Delivery and Victim Interaction

#### Step 16: Craft and Send Phishing Email

A phishing email with the copied URL embedded is sent via Thunderbird.

![CRAFTING PHISHING EMAIL AND INSERTING COPIED LINK](https://github.com/user-attachments/assets/208428ba-6a7a-4a78-a736-a81423d8fe1b)

---

#### Step 17: Victim Receives and Opens Email

The target receives the phishing email and opens it.

![VICTIME RECEIVED EMAIL AND OPENING LINK](https://github.com/user-attachments/assets/455dd873-8164-4b2b-bcac-56d7b6a7c95e)


---

#### Step 18: Victim Opens the Phishing Link

The victim clicks the URL and is redirected to the cloned WordPress login page.

![VICTIM OPEN LINK](https://github.com/user-attachments/assets/c3f05a1d-d303-49ca-998d-9cf8e988d4cd)


---

#### Step 19: Victim Enters Login Credentials

The victim types username and password into the fake login form.

![VICTIME INSERT LOGIN DETAILS](https://github.com/user-attachments/assets/3c253efe-af6a-4741-af63-a2012f6ec34b)


---

### Phase 4: Credential and IP Capture

#### Step 20: Credentials Harvested

Zphisher captures the submitted credentials in real time.

![USERNAME AND PASSWORD CREDENTIALS HARVESTED FROM SUBMITTING BY VICTIME TO PHISHING WORDPRESS PAGE](https://github.com/user-attachments/assets/59c2a859-44e1-4406-83bc-9ae798f26186)

---

#### Step 21: Victim IP Address Captured

Zphisher logs the victim's IP address alongside the captured credentials.

![CHECKING IP CAPTURED BY ZPHISHER FROM VICTIM](https://github.com/user-attachments/assets/db64eb23-0cc2-4b23-9717-023256439e57)


---

#### Step 22: Save Captured Credentials

The harvested data is saved to a file for simulation documentation.

![CAPTURED VICTIM USERNAME AND PASSWORD SAVED](https://github.com/user-attachments/assets/c200c531-c1d5-4e20-bdc7-92f5d17f2fb2)


---

### Phase 5: Adobe Phishing Scenario

#### Step 23: Adobe + LocalXpose Setup

![USING ADOBE AND LOCALXPOSE ](https://github.com/user-attachments/assets/ac4b79ab-3f38-4fc1-aff1-947f9db76f62)

#### Step 24: LocalXpose for Adobe Page

![USING LOCALXPOSE FOR ADOBE LOGIN PAGE](https://github.com/user-attachments/assets/06403db9-5fa3-4b4b-aee0-214dcbe415ef)


#### Step 25: Paste Access Token

![USING LOCALXPOSE FOR ADOBE LOGIN PAGE AND PASTING THE ACCESS TOKEN FROM LOCALXPOSE PAGE](https://github.com/user-attachments/assets/41dbfda2-9a29-4231-9899-c5e16b05fdc3)



#### Step 26: Token Entry Complete
![USING LOCALXPOSE FOR ADOBE LOGIN PAGE AND PASTING THE ACCESS TOKEN FROM LOCALXPOSE PAGE_1](https://github.com/user-attachments/assets/f8a97130-10bb-45a7-9464-5103251822ae)


#### Step 27: Adobe Phishing URL Generated

![URL CREATED USING LOCALXPOSE](https://github.com/user-attachments/assets/8a703a5a-54ee-4638-b342-9d708899a9d6)

#### Step 28: Link Fails — IP Still Captured

The page did not fully load, but the victim's IP was logged at point of connection.

![LINK DOESN&#39;T WORK BUT VICTIM IP ADDRESS WAS CAPTURED](https://github.com/user-attachments/assets/3ed716fc-444b-43da-8139-cfd366884d5c)



---

### Phase 6: Yahoo Phishing Scenario

#### Step 29: Yahoo Landing Page

![YAHOO LANDING PAGE ](https://github.com/user-attachments/assets/aff124ad-e677-4146-bca2-2e0e08012f59)


#### Step 30: Yahoo Phishing Simulator Active

![USING YAHOO LOGIN PAGE FOR THE  PHISHING SIMULATOR](https://github.com/user-attachments/assets/2b9b4bc7-e8c5-4d5d-a0ba-bf56af1c35bb)

#### Step 31: Yahoo Credentials Harvested

![VICTIME CREDENTIALS HARVESTED](https://github.com/user-attachments/assets/5fe890db-8bff-4164-9d6a-76f346786344)


#### Step 32: Yahoo Template in Zphisher

![USING YAHOO ON ZPHISHER](https://github.com/user-attachments/assets/0f9f3711-d521-4fef-b870-a508003f84a0)


---

### Phase 7: Phishing Pot Email Analysis

#### Step 33–35: Launch Phishing Pot and Browse Samples

![USING PHISHING_POT_00](https://github.com/user-attachments/assets/5b41dfbf-4bc0-4b58-87a3-a36a43619709)


![INSTALLING PHISHING_POT ](https://github.com/user-attachments/assets/ba73c75e-3c15-492d-b2de-3406e95a0b0c)


![PHISHING_POT_EMAIL_EMAIL SAMPLES](https://github.com/user-attachments/assets/ff9fa3e7-fc85-4726-9ad0-87987cb61858)


#### Step 36: Sample 276 in Mousepad

![PHISHING_PIT_EDITING EMAIL SAMPLE_276 IN MOUSEPAD](https://github.com/user-attachments/assets/6f191898-29af-40d4-bb08-fb812549c736)


#### Steps 37–40: Thunderbird Renders

![THUNDERBIRD EMAIL SAMPLE 267](https://github.com/user-attachments/assets/3335d500-4da1-4410-89a2-b2d74f8df8b2)


![THUNDERBIRD OPEN EMAIL LIKE IT WILL OPEN IN NORMAL WEBMAIL](https://github.com/user-attachments/assets/39b16115-f27b-4d56-8b59-5186ed8aff8d)


![THUNDERBIRD EMAIL SAMPLE 2781](https://github.com/user-attachments/assets/8cb7452f-760e-42d5-81d2-59557bf30c05)


![THUNDERBIRD OPEN EMAIL 2781 LIKE A NORMAL WEBMAIL FORMAT](https://github.com/user-attachments/assets/1926331c-8808-452d-afe1-69f8eeced939)


#### Steps 41–46: Header and IP Analysis

![ANALYZING EMAIL SAMPLE 276 USING MOUSEPAD  TO CHECK HEADER SPF DMARC](https://github.com/user-attachments/assets/5f50925a-6e29-44ce-ac0f-da3cb6fe6678)


![ANALYZING EMAIL SAMPLE 276](https://github.com/user-attachments/assets/d8cf11a8-700d-4f06-98fb-e266db5ba91d)


![ANALYZING SENDER IP ADDR WITH ABUSEIPDB](https://github.com/user-attachments/assets/95d818ff-1e7d-44a1-98c2-2ab4efed9427)


![ANALYZING EMAIL SAMPLE 2781 USING MOUSEPAD](https://github.com/user-attachments/assets/46ac3271-a35a-463d-b0e4-f2affc7663cb)


![ANALYZING EMAIL SAMPLE 2781 ](https://github.com/user-attachments/assets/f4d41c32-b314-47d5-aab6-afb5a656d85b)

![ANALYZING EMAIL 2781 SENDER IP ADDR WITH ABUSEIPDB](https://github.com/user-attachments/assets/677a50a4-4895-4a18-9a54-7f688e63da08)

---

### Phase 8: Ngrok Tunnel Walkthrough (Steps 47–63)

![USING NGROK](https://github.com/user-attachments/assets/ba8dbcb5-2381-4864-8115-030d6a2c6c7b)

![USING NGROK_1](https://github.com/user-attachments/assets/57515304-871c-4b5f-91b6-2eaffc6a784a)

![USING NGROK_2](https://github.com/user-attachments/assets/cd86eea9-5343-4f61-93be-6b86893a5f2e)

![USING NGROK_3](https://github.com/user-attachments/assets/af45be08-9a1b-456d-950f-091dd844190e)

![USING NGROK_4](https://github.com/user-attachments/assets/4994a744-d1e8-43bd-a57e-f77278d93282)

![USING NGROK_5](https://github.com/user-attachments/assets/af61adbb-e3b6-46dd-af80-016c24f6060f)

![USING NGROK_6](https://github.com/user-attachments/assets/769af8ea-cb3a-42ac-b4ed-44accdff02dc)

![USING NGROK_7](https://github.com/user-attachments/assets/b8c41b4f-0f30-4623-8b76-244c83e3b0e2)

![USING NGROK_8](https://github.com/user-attachments/assets/1d65fa42-450d-487c-a192-5d9214e32675)

![USING NGROK_9](https://github.com/user-attachments/assets/65170d97-9910-4fbc-966b-2acc43c25dd5)

![USING NGROK_10](https://github.com/user-attachments/assets/76366433-6e88-441a-a253-feffb1df721b)

![USING NGROK_11](https://github.com/user-attachments/assets/e8368eef-e2a4-47fd-9f28-f95890ec71d1)

![USING NGROK_12](https://github.com/user-attachments/assets/6addef40-58db-41fa-821e-19aa94f588bd)

![USING NGROK_13](https://github.com/user-attachments/assets/24452a2b-1ec4-4999-ac1f-af46836d05b7)

![USING NGROK_14](https://github.com/user-attachments/assets/8ad2584f-99f6-4414-b7a6-cf855cc8d8cb)

![USING NGROK_15](https://github.com/user-attachments/assets/84cac707-0ac7-42d4-8a77-f73bb350b5a9)

![USING NGROK_16](https://github.com/user-attachments/assets/55a00281-70c7-45e0-8d02-bad071b25452)


---

### Phase 9: Extended Email Analysis — Email 4555 and Sample 217

![ANALYZING EMAIL_00](https://github.com/user-attachments/assets/d90d3d93-e855-45f6-9ed6-e6c3be1e8aec)

![ANALYZING EMAIL_00_EMAIL 4555](https://github.com/user-attachments/assets/e752d23c-56bf-4eef-9b81-f1430452b81f)

![ANALYZING EMAIL_00_EMAIL 4555_01](https://github.com/user-attachments/assets/20af1c88-4d32-49e4-9f21-87239614e1e9)

![ANALYZING EMAIL_00_EMAIL 4555_02](https://github.com/user-attachments/assets/b207497e-d4fe-4b7e-8eec-c501764ad821)

![ANALYZING EMAIL_00_EMAIL 4555_02_DOMAIN COULD NOT BE RESOLVED_RESULT FROM URLSCAN IO](https://github.com/user-attachments/assets/8b05bb66-9a2e-404c-8035-bc7575cb9076)

![ANALYZING EMAIL SAMPLE 217](https://github.com/user-attachments/assets/3a4229eb-8d15-444a-8501-5c52ad5d223a)

![ANALYZING EMAIL SAMPLE 217_00](https://github.com/user-attachments/assets/4ec1b440-7984-4893-a966-c3be8dbbfcf3)

![ANALYZING EMAIL SAMPLE 217_01_ANALYZING LINK](https://github.com/user-attachments/assets/90b30188-d176-4602-b55c-440b261af366)

![ANALYZING EMAIL SAMPLE 217_01_ANALYZING LINK_VIRUS TOTAL ANALYZIS](https://github.com/user-attachments/assets/2918cead-55c2-47b5-a856-d84b94fac486)

![ANALYZING EMAIL_00_EMAIL 4555_04_CHECKING SENDER IP ON ABUSEIPDB](https://github.com/user-attachments/assets/805e0508-3422-4814-a777-90355db1cb27)

![ANALYZING EMAIL SAMPLE 217_01_ANALYSIS OF_FROM_SPF_SENDER IP](https://github.com/user-attachments/assets/ed81bd71-3160-4f57-bd5b-7cfbc2f680de)

![ANALYZING EMAIL SAMPLE 217_01_SENDER IP ANALYSIS](https://github.com/user-attachments/assets/8543fd84-d5cd-4cb2-be9f-4cbdeb440201)

![ANALYZING EMAIL SAMPLE 217_01_ANALYSIS OF_RETURN PATH](https://github.com/user-attachments/assets/12de6a32-5812-4ab9-b5ad-6fcbdb7d1212)

![ANALYZING EMAIL_00_EMAIL 4555_03_ANALYSIS OF FROM_SPF_IP_HEADER](https://github.com/user-attachments/assets/1b298139-1fd1-4a4b-9654-0d3a19c1973a)


---

## MITRE ATT&CK Mapping

| Tactic | Technique ID | Technique Name | How It Was Applied |
|---|---|---|---|
| Reconnaissance | T1598.003 | Phishing for Information: Spearphishing Link | Phishing pages harvested credentials from employees who believed they were logging into real services |
| Resource Development | T1583.003 | Acquire Infrastructure: Virtual Private Server | LocalXpose and Ngrok tunnels provided public infrastructure without a dedicated server |
| Initial Access | T1566.001 | Phishing: Spearphishing Link | Crafted emails with embedded URLs led victims to cloned login pages |
| Execution | T1204.001 | User Execution: Malicious Link | 80% of employees clicked the phishing URL pre-training |
| Credential Access | T1056.003 | Input Capture: Web Portal Capture | Zphisher captured plaintext credentials submitted through fake login forms |
| Collection | T1078 | Valid Accounts | Captured credentials represent real accounts usable in post-simulation attack chains |

---

## Behavioral Analysis

**Why users clicked:** The email used authority (trusted platform branding), urgency (time pressure), and familiarity (routine login prompts). Without trained skepticism, employees had no baseline to verify sender legitimacy before clicking.

**Why credentials were submitted:** The cloned pages were visually identical to real services. The HTTPS padlock from LocalXpose/Ngrok tunnels gave a false impression of legitimacy. Users who clicked were already primed to complete the action the page requested.

**Why reporting increased:** Post-training, employees received specific indicators to look for and understood reporting as a protective act. The jump from 10% to 80% reporting is the most operationally significant outcome — a high-reporting workforce is a live threat detection layer.

---

## Lessons Learned

- 80% initial click rate confirms low baseline skepticism toward unsolicited email links
- 60% initial submission rate confirms visual cloning is sufficient to defeat user verification
- Post-training improvement to 30%/20% confirms that targeted awareness training has measurable impact
- The 80% reporting rate is the most valuable outcome — reporting enables early detection of real attacks
- Residual risk (20% submission, ongoing IP capture) requires technical controls: MFA and DNS filtering

---

## Ethical Considerations

This simulation was conducted with explicit authorization from organizational leadership inside a controlled environment. All captured credentials and IP addresses were used solely for documentation and training. No data was retained beyond the scope of the project. Participants were informed after the exercise concluded, and results were used to improve employee security posture, not to penalize individuals.

All techniques documented here are for authorized security testing and educational purposes only.

---

## Compliance

| Standard | Control | How This Project Addresses It |
|---|---|---|
| ISO 27001:2022 | Annex A.6.3 — Information Security Awareness, Education and Training | Pre- and post-training KPIs provide quantified evidence of an effective, measured awareness programme |

---

**Author:** Ibrahim Fayomi | Cybersecurity Student and Analyst
**Date:** March 2026
