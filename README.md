# n8n Automation Workflows

A curated repository of production-ready **n8n automation workflows**, integrating AI agents, webhooks, third-party APIs, and cloud services.

---

## 📁 Repository Structure

```
.
├── workflows/
│   ├── hr_recruitment_screening_pipeline.json
│   └── daily_voice_agent_newsletter.json
└── README.md
```

---

## 🚀 Workflows Overview

### 1. HR Recruitment Candidate Screening Pipeline
* **File:** [`workflows/hr_recruitment_screening_pipeline.json`](file:///workflows/hr_recruitment_screening_pipeline.json)
* **Trigger:** JazzHR Webhook (`CANDIDATE-EXPORT`)
* **Key Integrations:**
  * **JazzHR API / Webhooks:** Ingests candidate profiles and job descriptions.
  * **Google Drive:** Decodes and backs up candidate resume PDFs.
  * **PDF Text Extractor:** Parses binary resumes into raw text.
  * **OpenAI (GPT-4.1):** Evaluates candidate credentials against 10 dynamic criteria and threshold scores pulled from Google Sheets.
  * **Gmail & Calendly:** Automatically issues branded interview invitations with self-scheduling links for qualified candidates, or sends empathetic updates for non-selected applicants.
  * **Google Sheets:** Real-time logging of scores, AI explanations, and interview status.

---

### 2. Daily AI Voice Agent Research & HTML Newsletter
* **File:** [`workflows/daily_voice_agent_newsletter.json`](file:///workflows/daily_voice_agent_newsletter.json)
* **Trigger:** Daily Cron Schedule (7:00 AM)
* **Key Integrations:**
  * **LangChain AI Agent:** Deep research on Voice AI technologies (Vapi, ElevenLabs, Retell, OpenAI Realtime API).
  * **OpenRouter / Claude / GPT:** Synthesis of business and technical intelligence into branded HTML email digests.

---

## 🛠️ How to Import into n8n

1. Open your n8n canvas (`http://localhost:5678` or Cloud instance).
2. Click the top-right menu **(...)** and select **Import from File**.
3. Select any `.json` workflow file from the [`workflows/`](file:///workflows) folder.
4. Configure your API credentials (OpenAI, Google Sheets, Gmail, etc.) in the respective node settings.
5. Activate the workflow!
