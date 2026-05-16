🤖 ProspectPilot AI — Autonomous Multi-Agent Sales Pipeline

An advanced AI-powered B2B sales automation system built with n8n
 that researches prospects, scores leads using real company data, retrieves knowledge from a Pinecone RAG system, writes hyper-personalized outreach emails, verifies deliverability, and automatically manages CRM workflows — all in under 30 seconds.

Built using a true Multi-Agent AI Architecture with:

🔍 Research Agent
🧠 AI Lead Scoring Agent
📚 RAG Retrieval Agent
✍️ AI Email Writer Agent
🚀 Features

✅ Autonomous AI Lead Qualification
✅ Real-Time Company Research via Google Search
✅ Multi-Agent AI Workflow Architecture
✅ RAG (Retrieval Augmented Generation) Integration
✅ Hyper-Personalized AI Email Writing
✅ Email Deliverability Validation (ZeroBounce)
✅ Gmail Auto-Sending for HOT Leads
✅ Slack Real-Time Notifications
✅ Notion CRM Auto-Creation
✅ Google Sheets Lead Logging
✅ Pinecone Vector Database Integration
✅ Context-Aware AI Reasoning
✅ Fully Automated End-to-End Pipeline

⚡ End-to-End Workflow
Lead Submission (Webhook)
        ↓
🔍 Research Agent (Serper API)
        ↓
🧠 AI Scoring Agent (Gemini)
        ↓
📚 RAG Retrieval Agent (Pinecone)
        ↓
✍️ AI Email Writer Agent
        ↓
✅ ZeroBounce Email Validation
        ↓
Switch Routing
        ↓
🔥 HOT  → Gmail + Slack + Notion + Sheets
🟡 WARM → Slack + Notion + Sheets
❄️ COLD → Google Sheets Log Only
🧠 Multi-Agent AI Architecture

Unlike traditional workflows using a single AI node, ProspectPilot uses multiple specialized AI agents working together as a coordinated AI sales team.

┌──────────────────────────────────────────────┐
│         PROSPECTPILOT AI SYSTEM             │
├──────────────────────────────────────────────┤
│                                              │
│  🔍 Research Agent                           │
│      ↓                                       │
│  🧠 Lead Scoring Agent                       │
│      ↓                                       │
│  📚 Pinecone RAG Retrieval Agent            │
│      ↓                                       │
│  ✍️ AI Email Writer Agent                    │
│                                              │
└──────────────────────────────────────────────┘
📚 RAG (Retrieval Augmented Generation)

ProspectPilot uses a real RAG pipeline powered by:

Pinecone
Google Gemini Embeddings
Semantic Vector Search

The system stores:

sales playbooks
tone guidelines
email frameworks
case studies
pricing strategy
follow-up rules

inside Pinecone vector storage.

Before writing outreach emails, the AI retrieves the most relevant playbook sections and injects them into prompts for highly personalized generation.

🛠️ Tech Stack
Core Automation
n8n
 — Workflow Automation Engine
AI & Intelligence
Google Gemini AI
 — Multi-Agent Reasoning
Pinecone
 — Vector Database
Serper API
 — Google Search Research
Gemini Embeddings — Semantic Vector Generation
Integrations
Slack API
 — Team Notifications
Notion API
 — CRM Management
Google Sheets API
 — Lead Logging
Gmail API
 — Automated Outreach
ZeroBounce
 — Email Verification
🔍 Agent 1 — Research Agent

Uses Serper API to search Google for:

company overview
recent news
B2B signals
market positioning
business context

Example Query:

Microsoft company overview B2B

This gives downstream AI agents real company intelligence before scoring leads.

🧠 Agent 2 — AI Lead Scoring Agent

The scoring agent analyzes:

email domain
lead source
company research
business signals

Returns structured JSON:

{
  "score": "HOT",
  "reason": "Corporate email with strong B2B signals",
  "email_draft": "Personalized outreach email",
  "next_action": "Send email immediately"
}
📚 Agent 3 — Pinecone RAG Retrieval Agent

The RAG agent:

converts sales playbook into embeddings
stores vectors in Pinecone
retrieves relevant chunks during email generation
Pinecone Configuration
Setting	Value
Index Name	smartlead-rag
Dimensions	3072
Metric	cosine
Cloud	AWS
Region	us-east-1
✍️ Agent 4 — AI Email Writer Agent

Combines:

company research
scoring context
sales playbook knowledge

to generate hyper-personalized B2B outreach emails.

Generated emails:

reference company news
follow playbook tone
remain consultative
avoid generic AI language
✅ Email Verification Layer

Before auto-sending emails, ProspectPilot validates deliverability using ZeroBounce
.

Validation prevents:

bounce damage
spam reputation issues
invalid outreach
📋 Automated CRM Management

Every HOT and WARM lead is automatically:

added to Notion CRM
logged into Google Sheets
pushed to Slack notifications

CRM includes:

lead info
AI reasoning
research summary
next action
email status

📸 Screenshots
🔄 Workflow Canvas
screenshots/workflow-canvas.png
📚 RAG Ingestion Workflow
screenshots/rag-ingestion.png
🔥 Slack HOT Lead Notifications
screenshots/slack-alerts.png
📋 Notion CRM Database
screenshots/notion-crm.png
📊 Google Sheets Lead Log
screenshots/google-sheets-log.png
🧠 Pinecone Vector Database
screenshots/pinecone-dashboard.png
✅ ZeroBounce Email Validation
screenshots/zerobounce-output.png
🔄 Workflow Architecture
Webhook Trigger
      ↓
Research Agent (Serper API)
      ↓
Research Processing
      ↓
Gemini AI Lead Scoring
      ↓
AI JSON Parsing
      ↓
Pinecone RAG Retrieval
      ↓
AI Email Writer
      ↓
Email Validation
      ↓
HOT / WARM / COLD Routing
      ↓
CRM + Notifications + Logging
📡 API Example
Request
{
  "name": "Sara Khan",
  "email": "sara@microsoft.com",
  "company": "Microsoft",
  "source": "LinkedIn"
}
Response
{
  "score": "HOT",
  "reason": "Corporate email with strong B2B signals",
  "email_draft": "Personalized outreach email",
  "next_action": "Send immediately"
}
🔧 Setup Instructions
1️⃣ Import Workflows

Import:

ProspectPilot AI.json
ProspectPilot AI RAG Ingestion.json

into your n8n workspace.

2️⃣ Configure Credentials

Required credentials:

Google Gemini API
Pinecone API
Serper API
Gmail OAuth2
Slack OAuth2
Notion OAuth2
Google Sheets OAuth2
ZeroBounce API
3️⃣ Configure Pinecone

Create index:

Index Name: smartlead-rag
Dimensions: 3072
Metric: cosine
Cloud: AWS
Region: us-east-1
4️⃣ Run RAG Ingestion Workflow

Execute:

ProspectPilot AI RAG Ingestion

This uploads your sales playbook into Pinecone vector storage.

5️⃣ Activate Main Workflow

Activate:

ProspectPilot AI

Your autonomous AI sales pipeline is now live.

🎯 Use Cases

✅ AI Sales Automation
✅ AI SDR Systems
✅ Lead Qualification
✅ Personalized Outreach
✅ CRM Automation
✅ AI-Powered Agencies
✅ Startup Sales Pipelines
✅ Enterprise Lead Routing

📈 Why This Project Matters

This project demonstrates:

AI workflow engineering
Multi-agent orchestration
RAG implementation
vector databases
prompt engineering
automation architecture
API integrations
production-grade AI systems
