# creating-a-backdoor-with-SET
creating a backdoor with SET - Ethical Hacking Techniques course

# AIM:
To Create a backdoor with Social Engineering Toolkit (SET)

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode


### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

### Architecture Diagram

```
+----------------+        +------------------------+        +----------------------+
| Attacker's PC  | -----> | SET (Credential        | -----> | Fake Login Page      |
| (Kali Linux)   |        | Harvester via Apache)  |        | (Hosted by SET)      |
+----------------+        +------------------------+        +----------------------+
       |                                                             |
       |                                                             v
       |   1. Configure SET with phishing site (e.g., Gmail clone)   |
       |                                                             |
       |                                                             v
       |                                                 +----------------------+
       |                                                 | Victim's Browser     |
       | <------------------------------------------------| Clicks Phishing Link|
       |                                                 +----------------------+
       |                                                             |
       |                                                             v
       |     2. Victim Enters Credentials → Sent to SET/Attacker    |
       |                                                             |
       |                                                             v
       |                                                 +----------------------+
       |                                                 | Credentials Captured |
       |                                                 | in Apache log/SET DB |
       |                                                 +----------------------+

```

## EXECUTION STEPS AND ITS OUTPUT:
Social Engineering attacks are the various cons used by the hackers to trick people into providing sensitive data to the attackers.

**Steps to Use SET for Phishing (Credential Harvester Attack Method)**

**1. Open terminal:**
```bash
sudo setoolkit
```
<img width="645" height="108" alt="image" src="https://github.com/user-attachments/assets/c237161a-1601-49d2-ba5e-0f0c726e7f78" />


**2. Navigate:**
```bash
1) Social-Engineering Attacks  
2) Website Attack Vectors  
3) Credential Harvester Attack Method  
```
<img width="917" height="781" alt="image" src="https://github.com/user-attachments/assets/b3406edf-a7c9-40d6-9961-4e9b462d45d0" />
<img width="948" height="431" alt="image" src="https://github.com/user-attachments/assets/3ac819f2-3e1d-4bd1-946b-e681a94bb2a6" />


**3. Enter your IP address as the attacker server.**
<img width="742" height="368" alt="image" src="https://github.com/user-attachments/assets/73fa4795-5b58-4852-982d-1b9ef7f807e8" />

**4. Choose:**
```bash
2) Site Cloner
```
**5. Enter the URL of the legitimate site ```(e.g., https://accounts.google.com)```**
![Uploading image.png…]()


**6. Send the generated link to the victim.**
<img width="814" height="476" alt="image" src="https://github.com/user-attachments/assets/9463e04b-7ffd-47bb-a131-e924d8ce3f84" />


**7. Once the victim logs in → their credentials are stored in:**
```bash
/var/www/html/
```
<img width="628" height="195" alt="image" src="https://github.com/user-attachments/assets/7569286a-fb8b-40ff-a095-eeaff36ac7cd" />




## RESULT:
The Social Engineering Toolkit (SET) is used to create backdoor is  examined successfully
