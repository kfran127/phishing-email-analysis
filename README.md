<p align="center">
  <img src="https://github.com/user-attachments/assets/4928343a-31cf-4033-a166-3a77eafc74e1" alt="SOC140 - Phishing Mail Detected">
</p>

<h1>SOC140 - Phishing Mail Detected - Suspicious Task Schedule</h1>

<p>This project documents my investigation of a phishing alert using the LetsDefend platform. The SOC140 alert, titled "Phishing Mail Detected - Suspicious Task Schedule," involved analyzing and handling a potentially malicious email. This case allowed me to follow a structured playbook, analyze a suspicious attachment, and ultimately confirm it as a phishing attempt.</p>

---

<h2>Part 1: Alert Triage and Initial Investigation</h2>

<p><strong>Step 1: Access the SIEM Dashboard</strong></p>
<ul>
  <li>Located the "Phishing Mail Detected - Suspicious Task Schedule" alert in the LetsDefend SIEM dashboard and took ownership of the case.</li>
</ul>
<p align="center">
<img width="1420" alt="Screenshot 2024-11-08 at 12 15 51 AM" src="https://github.com/user-attachments/assets/c099f68e-19cc-42c1-9365-fe38b6a86beb">


<p><strong>Step 2: Parse Email Details</strong></p>
<ul>
  <li>Identified key email information:
    <ul>
      <li><strong>Event Time:</strong> Mar 21, 2021, 12:26 PM</li>
      <li><strong>SMTP Address:</strong> 189.162.189.159</li>
      <li><strong>Sender:</strong> aaronluo@cmail.carleton.ca</li>
      <li><strong>Recipient:</strong> mark@letsdefend.io</li>
      <li><strong>Subject:</strong> COVID19 Vaccine</li>
      <li><strong>Attachment:</strong> Suspicious zip file</li>
    </ul>
  </li>
</ul>
<p align="center">
<img width="1440" alt="Screenshot 2024-11-08 at 1 20 12 AM" src="https://github.com/user-attachments/assets/80ec96ba-4ad4-4c17-84e7-21818bf75fa7">


<h2>Part 2: Attachment Analysis and Threat Confirmation</h2>

<p><strong>Step 3: Check for Attachments and URLs</strong></p>
<ul>
  <li>Confirmed that the email contained a zip file attachment, which required further analysis.</li>
</ul>
<p align="center">
<img width="1440" alt="Screenshot 2024-11-08 at 1 21 52 AM" src="https://github.com/user-attachments/assets/039b4f61-c9ff-448b-8cb9-b3b997d679bf">


<p><strong>Step 4: Analyze Attachment in Sandbox</strong></p>
<ul>
  <li>Attempted to download the file, and Chrome flagged it as malicious. This raised an immediate red flag.</li>
  <li>Bypassed Chrome's block and uploaded the file to VirusTotal, which confirmed it as malicious.</li>
</ul>
<p align="center">
<img width="1440" alt="Screenshot 2024-11-08 at 12 31 20 AM" src="https://github.com/user-attachments/assets/34da5a9d-43eb-4413-a262-9e87f0dc91e3">
<img width="1007" alt="Screenshot 2024-11-08 at 12 31 52 AM" src="https://github.com/user-attachments/assets/92732033-f7be-4702-86ea-85ac9b0453b9">
<img width="1440" alt="Screenshot 2024-11-08 at 12 35 17 AM" src="https://github.com/user-attachments/assets/b87950ff-9ce5-4717-a7f2-38d6857c4061">
<img width="1440" alt="Screenshot 2024-11-08 at 12 35 39 AM" src="https://github.com/user-attachments/assets/05bae3d4-2129-4e8c-878a-1a3e96d65b24">






<h2>Part 3: Mitigation and Documentation</h2>

<p><strong>Step 5: Check Mail Delivery Status</strong></p>
<ul>
  <li>Verified in the alert details that the email was <strong>blocked</strong> and not delivered to the recipient.</li>
</ul>
<p align="center">
<img width="1440" alt="Screenshot 2024-11-08 at 1 30 16 AM" src="https://github.com/user-attachments/assets/4c0e8e87-b1e3-44a8-b2cb-dba483e28401">





<p><strong>Step 6: Add Artifacts</strong></p>
<ul>
  <li>Added relevant artifacts to the case:
    <ul>
      <li><strong>Phishing Sender:</strong> aaronluo@cmail.carleton.ca</li>
      <li><strong>MD5 Hash of Malicious File:</strong> 72c812cf21909a48eb9cceb9e04b865d</li>
    </ul>
  </li>
</ul>
<p align="center">
<img width="1208" alt="Screenshot 2024-11-08 at 1 30 47 AM" src="https://github.com/user-attachments/assets/89d06a05-e066-47f1-aeb1-ae68a4a7369a">




<p><strong>Step 7: Document Findings and Close Alert</strong></p>
<ul>
  <li>Recorded comments summarizing the investigation process and marked the alert as closed.</li>
</ul>
<p align="center">
  <img src="https://github.com/yourusername/yourrepository/assets/document-and-close.png" alt="Document and Close Alert" width="80%">
</p>

<h2>Conclusion</h2>

<p>Through this investigation, I practiced using a SOC playbook to analyze phishing emails, identified suspicious files using sandbox environments, and documented the process effectively. This case reinforced key skills in threat detection, email analysis, and proper handling of malicious attachments.</p>
