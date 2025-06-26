# Task 3: Basic Vulnerability Scan on Windows PC

## Objective
The goal of this task was to perform a basic vulnerability scan on my personal computer using a free vulnerability assessment tool. This helped me understand common system risks, identify vulnerabilities, and learn how to interpret scan results.

---

## Tools Used
- **Nessus Essentials** – A free edition of Tenable's powerful vulnerability scanner.
- **Operating System** – Windows 10 (or your version)
- **Browser** – Used to access the Nessus Web UI via `https://localhost:8834`

---

## Steps Performed

### 1. Installation & Setup
- Registered on [Tenable's official site](https://www.tenable.com/products/nessus/nessus-essentials) to receive a free activation key.
- Downloaded and installed Nessus Essentials for Windows.
![Screenshot 2025-06-26 124254](https://github.com/user-attachments/assets/920ba9ac-7051-4757-9e29-b9ea345cd43b)
- Accessed Nessus via browser (`https://localhost:8834`) and completed setup.
![Screenshot 2025-06-26 124339](https://github.com/user-attachments/assets/ed0e586d-3588-46d1-829a-85fe7ace903c)

### 2. Scan Configuration
- Created a new scan: **Basic Network Scan**
![Screenshot 2025-06-26 143936](https://github.com/user-attachments/assets/08ecc04e-9ebe-4f58-b492-79a395eb10bf)
![Screenshot 2025-06-26 144000](https://github.com/user-attachments/assets/58ebfdfa-a4d4-4004-942b-fc8b52493cdd)
- Set the target as `127.0.0.1` (localhost) to scan my own system.
- Saved and launched the scan.
![Screenshot 2025-06-26 144125](https://github.com/user-attachments/assets/ae68636e-78de-40e4-8739-e2e27934d97f)

### 3. Vulnerability Scan
- The scan ran for approximately 20-25 minutes.
- Discovered multiple vulnerabilities, categorized by severity:
  - Medium
  - Low
- Collected scan report and screenshots of key results.
![Screenshot 2025-06-26 145104](https://github.com/user-attachments/assets/652dc25f-62ec-4ae3-b3ff-5b47d48a1233)

---

## Identified Vulnerabilities

| Severity | Example Vulnerability Name       | Plugin ID | CVE ID        |
|----------|----------------------------------|-----------|---------------|
| Medium   | SMB Signing not required         | 57608     | N/A           |
| Medium   | SSL Certificate Cannot Be Trusted| 51192     | N/A           |

![Screenshot 2025-06-26 145114](https://github.com/user-attachments/assets/7d1952d2-c316-4d81-9efb-4e8db13940d1)
![Screenshot 2025-06-26 145126](https://github.com/user-attachments/assets/c4f268fa-ea0d-4c80-b313-9f651563cbad)
![Screenshot 2025-06-26 145436](https://github.com/user-attachments/assets/467ef753-352d-4ca1-811e-24702acea4c2)
![Screenshot 2025-06-26 145658](https://github.com/user-attachments/assets/0accaccc-c89b-4294-951a-459e4e8d65f0)

---

## Remediation / Fix Suggestions

- **SMB Signing not required** : Enforce message signing in the host's configuration. On Windows, this is found in the policy setting 'Microsoft network server: Digitally sign communications (always)'. On Samba, the setting is called 'server signing'. See the 'see also' links for further details.
- **SSL Certificate Cannot Be Trusted** : Purchase or generate a proper SSL certificate for this service.

---

## Key Learnings

- Understood how vulnerability scanners work and what CVEs are.
- Learned how to interpret the **Common Vulnerability Scoring System (CVSS)**.
- Recognized the importance of routine vulnerability scanning for personal or organizational security.
- Improved skills in analyzing and prioritizing vulnerabilities based on severity and impact.

---

## Folder Structure
```
├── README.md
└── Nessus_Report.pdf (optional export)
```

---

## Conclusion

This task offered hands-on experience with vulnerability scanning and taught me how to detect, analyze, and begin remediating common PC security flaws using industry tools.


