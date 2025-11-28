# n8n-ai-chatbot
# 🎓 Scholarship Eligibility Automation – n8n Workflow

This repository contains an automated **Scholarship Eligibility Workflow** built using **n8n**.  
It collects student details through a form, processes the data, checks scholarship eligibility based on percentage, and automatically sends an email response to the student using the Gmail API.

---

## 🚀 Features

### ✅ 1. Student Form Submission  
Students submit the following details:

- First Name  
- Last Name  
- Email ID  
- Phone Number  
- Percentage  

---

## 🛠️ 2. Data Transformation (Edit Fields)

After submission, the workflow automatically:

- Combines **First Name + Last Name → Full Name**
- Adds **+91** country code prefix to Phone Number  
- Cleans & prepares data for eligibility check  

---

## 🔍 3. Eligibility Logic (IF Condition)

The workflow checks scholarship eligibility based on percentage:

- **If Percentage ≥ 70% → Eligible for Scholarship**
- **If Percentage < 70% → Not Eligible**

Examples:
- 80% → Eligible  
- 65% → Not Eligible  

---

## ✉️ 4. Automated Email Notifications (Gmail API)

Based on the eligibility result:

### ✔️ Eligible Students Receive:
> "Congratulations! You are eligible for the scholarship."

### ❌ Not Eligible Students Receive:
> "Thank you for applying. Unfortunately, you are not eligible for the scholarship."

This is powered by the **Gmail API** integrated through **Google Cloud Console**.

---

## 🔧 Workflow Structure

Form Submission → Edit Fields → IF (Percentage Check) →
→ True → Send Email (Eligible)
→ False → Send Email (Not Eligible)


---

## 🖼️ Workflow Screenshot

*(Screenshot from n8n Cloud Editor)*

![Workflow Screenshot](Screenshot-2025-11-28-160724.png)

---

# 🔐 Google Cloud API Setup (Gmail API Integration)

This workflow uses the **Gmail API** to send automated eligibility emails.

### ✔️ Steps Completed in Google Cloud Console:

1. Opened **Google Cloud Console**  
   https://console.cloud.google.com

2. Created a new project for the Scholarship Bot.

3. Enabled the following API:
   - **Gmail API**

4. Opened:  
   **APIs & Services → Credentials → Create Credentials**

5. Created:
   - **OAuth Client ID**
   - Selected “Web Application”
   - Added **n8n redirect URI**

6. Downloaded the `client_secret.json` credentials file.

7. Added OAuth credentials in **n8n → Credentials → Gmail OAuth**:
   - Uploaded credentials  
   - Logged into Google account  
   - Authorized Gmail API access

### ✔️ Purpose of Gmail API  
The Gmail node in n8n cannot send emails without:
- Gmail API  
- OAuth consent  
- Client credentials  
- Authorization scopes  

This setup ensures secure, authenticated email automation.

---

# 📁 Files in This Repository

- `workflow.json` – Exported n8n workflow  
- `README.md` – Project documentation  
- `Screenshot-2025-11-28-160724.png` – Workflow screenshot  

---

# 📥 How to Import This Workflow in n8n

1. Open n8n  
2. Go to **Workflows → Import**
3. Upload `workflow.json`
4. Configure Gmail OAuth credentials  
5. Click **Activate Workflow**  
6. Test form submission  

---

# 🎯 Project Purpose

This project demonstrates:

- No-code/low-code automation using n8n  
- Data preprocessing and formatting  
- Conditional workflow logic  
- API integration (Gmail API)  
- Full automation pipeline from form submission → validation → email  

Perfect for:
- Portfolio projects  
- Automation engineer roles  
- Backend/Workflow engineering  
- AI/Automation internships  

---

# 👨‍💻 Author

**Your Name**  
Email: sibinakasrija@gmail.com



