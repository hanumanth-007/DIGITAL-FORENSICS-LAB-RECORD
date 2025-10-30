# MHA Analyzer (Message Header Analyzer)

# Aim: 

To parse and interpret raw email headers—making them human-readable and helping investigators trace the email’s route, source IP, delays, and authentication status.

# Tools / Features:

• A Flask-based web tool developed by lnxg33k that accepts pasted email headers and translates them into a clearer, visual format. It identifies hop delays, source IPs, and even the country of each hop.

• Available both as: 

o A web-based standalone version hosted at mha.azurewebsites.net

o An Outlook add-in that integrates directly into Outlook/OWA to display header analysis inline

# Process:

1. Via Web:
   
a. Navigate to the MHA web app (e.g., mha.azurewebsites.net)
.
b. Paste the raw email header text into the input field.

c. The tool instantly parses and visualizes the routing path, delays, and metadata.

4. Via Outlook Add-in:
 
a. Install the Message Header Analyzer add-in via Exchange Admin Center or Office Store

b. Once enabled, open an email in Outlook or OWA and click the MHA icon to view the parsed header details inline.

# OUTPUT:

<img width="1920" height="1080" alt="Screenshot (116)" src="https://github.com/user-attachments/assets/1a1b4ccf-1aea-4d9b-a761-f9e44448d57a" />

---

<img width="1920" height="1080" alt="Screenshot (117)" src="https://github.com/user-attachments/assets/95ef1b3f-6c76-47a3-9959-b54e5413cf09" />

---

<img width="1920" height="1080" alt="Screenshot (118)" src="https://github.com/user-attachments/assets/edf13a64-63a7-45ed-8d10-09f4b6ceb486" />

---

<img width="1920" height="1080" alt="Screenshot (119)" src="https://github.com/user-attachments/assets/3d9d489c-20b7-428d-87db-0ff3e1ddccb3" />

---

<img width="1920" height="1080" alt="Screenshot (120)" src="https://github.com/user-attachments/assets/ba84041f-915a-4353-bda1-169f9cb66c19" />

---

# Rubrics

| Criteria | Mark Allotted | Mark Awarded |
|---|---:|---:|
| 1. GitHub Activity & Submission Regularity | 3 | |
| 2. Application of Forensic Tools & Practical Execution | 3 | |
| 3. Documentation & Reporting | 2 | |
| 4. Engagement, Problem-Solving & Team Collaboration | 2 | |
| *Total* | *10* | |

---

# Result:
• The raw email headers are transformed into a structured, user-friendly format.

• You can easily see the hop-by-hop journey of the email, including timestamps, delays, source IPs, and countries—helpful for tracking and forensic analysis.

• In Outlook, this analysis is accessible directly within the email interface through the add-in.
