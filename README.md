# 🌍 Automated HTML Travel Page Generator

An end-to-end automation project that creates, publishes, and manages dynamic
travel HTML pages using **n8n**, **Airtable**, and **AI services**.

The system generates a complete travel website for a selected city or country,
deploys it automatically to GitHub Pages, and allows the user to approve or
reject the result directly from an email.

---

## 📌 Project Overview

This project demonstrates a fully automated workflow, from user input to a live
published website.

### Workflow Summary:
1. User enters a **city or country** and **email address** in Airtable
2. n8n workflow is triggered automatically
3. AI generates travel content and attraction recommendations
4. Images are fetched dynamically from the Unsplash API
5. A styled HTML page is generated dynamically
6. A Google Maps embed is added with points of interest
7. The website is deployed to **GitHub Pages**
8. The user receives an email with:
   - A link to the generated website
   - Approve and Reject buttons
9. User decision handling:
   - ✅ **Approve** → Confirmation page is displayed and status is updated
   - ❌ **Reject** → Feedback form opens to collect notes for regeneration

---

## 🔁 n8n Workflow Overview

The image below shows the full automation workflow implemented in n8n,
including all nodes and integrations used to generate and manage the HTML
travel pages.

<img width="1396" height="703" alt="Screenshot 2025-12-25 at 15 44 26" src="https://github.com/user-attachments/assets/fdc2c401-2342-41c4-a358-462ef164b173" />


---

## 🧠 Technologies & Tools

- **n8n** – Workflow automation platform  
- **Airtable** – User input, request tracking, and data storage  
- **Groq API** – AI-generated text content  
- **Unsplash Developers API** – Destination images  
- **Google Maps (Embed)** – Interactive map integration  
- **HTML & CSS** – Dynamic page generation  
- **GitHub Pages** – Hosting and publishing generated websites  
- **Gmail Integration** – User approval workflow  

---

## 🔄 Workflow Logic

Each request is managed using a status-based flow:

- `New`
- `Waiting Approve`
- `Approved`
- `Regenerate`

Approval and rejection actions are handled through webhooks directly from the
email, without requiring user authentication.

---

## 📂 Repository Structure

```text
presentation/      -> Project presentation (PDF)
workflow/          -> n8n workflow export + public workflow link
docs/              -> Workflow documentation (Scribe)
```
---

## 🔗 Useful Links

Airtable Base
https://airtable.com/appM8JpRNkpjZB2rT

Public n8n Workflow (Read-only)
See: workflow/workflow_public_link.txt

Workflow Documentation (Scribe)
https://scribehow.com/viewer/Workflow_Overview_Automating_HTML_Page_Creation_with_n8n_and_Airtable__C3kuWMlmTBWUWOFvuUaemA

---

## ⚠️ Important Notes

API keys, tokens, and credentials were removed before publishing this
repository

Users must configure their own credentials in n8n before running the workflow

Webhook URLs are placeholders and should be updated per deployment

---

## 👤 Authors

**Itamar Hadad**  
B.Sc. Computer Science Student – Afeka College  
📧 hzitamar4@gmail.com  
[LinkedIn](https://www.linkedin.com/in/itamar-hadad)
