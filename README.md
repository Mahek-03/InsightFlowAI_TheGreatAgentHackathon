# InsightFlow AI

> An AI employee that autonomously handles everyday business operations across support, sales, and finance.

##  Overview

InsightFlow AI is an agentic business intelligence platform that helps businesses investigate problems, understand their root causes, and generate actionable recommendations.

Instead of manually searching through dashboards, reports, and different business systems, users can simply ask a business question in natural language.

InsightFlow AI then:

**Understands → Investigates → Delegates → Analyzes → Finds Root Cause → Recommends Actions**

For example:

> **"Why did our revenue decline by 18% last month?"**

InsightFlow AI can break this question into multiple investigations, delegate them to specialized agents such as Sales, Finance, and Support agents, analyze the findings, identify contributing factors, and provide recommendations.

---

# Demo

[https://velvety-longma-63c045.netlify.app/](https://velvety-longma-63c045.netlify.app/)

### Demo Video

[https://www.loom.com/share/64cb1e2745574986b0aea22ceb581686](https://www.loom.com/share/64cb1e2745574986b0aea22ceb581686)

---

##  Problem

Businesses generate large amounts of data across different departments such as:

- Sales
- Finance
- Customer Support
- Operations
- CRM
- Customer Analytics

However, having data does not automatically provide useful insights.

When a business metric changes, managers often have to:

1. Open multiple dashboards
2. Compare different metrics
3. Search for anomalies
4. Investigate possible causes
5. Combine findings manually
6. Decide what action to take

This process is time-consuming and requires significant manual effort.

### The Problem

> Businesses don't just need to know **what happened**. They need to understand **why it happened and what they should do next**.

---

##  Our Solution

InsightFlow AI transforms business questions into autonomous investigations.

Instead of simply returning an AI-generated answer, the system creates an investigation workflow and coordinates specialized AI agents.

```text
                Business Question
                       │
                       ▼
                InsightFlow AI
                       │
                       ▼
              Investigation Plan
                       │
          ┌────────────┼────────────┐
          ▼            ▼            ▼
      Sales Agent  Finance Agent  Support Agent
          │            │            │
          └────────────┼────────────┘
                       ▼
                 Data Analysis
                       │
                       ▼
                Root Cause Analysis
                       │
                       ▼
                 Recommendations
````

---

#  Key Features

###  Natural Language Business Queries

Users can ask complex business questions using natural language.

Example:

```text
Why did revenue decline last month?
```

No complex SQL queries or manual dashboard exploration is required.

---

###  AI Investigation

InsightFlow AI creates a structured investigation plan instead of immediately generating an answer.

```text
Business Question
        ↓
Understand Question
        ↓
Create Investigation Plan
        ↓
Identify Relevant Data
        ↓
Assign Specialist Agents
        ↓
Analyze Findings
        ↓
Identify Root Cause
        ↓
Generate Recommendations
```

---

###  Multi-Agent System

Different AI agents specialize in different business domains.

```text
                    Supervisor Agent
                           │
          ┌────────────────┼────────────────┐
          │                │                │
          ▼                ▼                ▼
     Sales Agent      Finance Agent     Support Agent
          │                │                │
          ▼                ▼                ▼
      Sales Data       Finance Data     Support Data
          │                │                │
          └────────────────┼────────────────┘
                           ▼
                    Analysis Engine
```

The architecture allows additional specialist agents to be added as the platform grows.

---

###  Root Cause Analysis

InsightFlow AI focuses on identifying **why** a business problem occurred.

For example:

```text
Revenue Decline
      │
      ├── Lower Sales
      │
      ├── Customer Churn
      │
      ├── Lower Repeat Purchases
      │
      └── Support Issues
```

The system combines findings from different agents to identify the most significant contributing factors.

---

###  Actionable Recommendations

InsightFlow AI does not stop after finding a problem.

It converts insights into recommendations.

Example:

```text
Root Cause:
Increased customer churn in the premium segment.

Recommendation:
Launch a targeted retention campaign for premium
customers and investigate the recent increase in
cancellation requests.
```

---

###  Transparent Agent Workflow

Users can see what the AI system is doing.

Instead of hiding the process behind a chatbot response, InsightFlow provides visibility into:

* Investigation progress
* Agents involved
* Agent status
* Root causes
* Recommendations

Example:

```text
Investigation

✓ Understanding business question
✓ Creating investigation plan
✓ Running sales analysis
✓ Running finance analysis
✓ Running support analysis
✓ Consolidating findings
✓ Generating recommendations
```

---

#  How It Works

## 1. Ask

The user enters a business question.

```text
"Why did revenue decline by 18% last month?"
```

## 2. Investigate

InsightFlow creates an investigation plan based on the question.

## 3. Agent Network

The system determines which specialist agents are required.

```text
                Supervisor
                    │
        ┌───────────┼───────────┐
        ▼           ▼           ▼
      Sales      Finance     Support
```

## 4. Analyze

Each specialist agent investigates its respective business area.

## 5. Root Cause

The findings are combined to determine the major contributing factors.

## 6. Recommend

The system generates actionable recommendations for the business user.

---

#  Architecture

```text
┌───────────────────────────────────────────────┐
│                 User Interface                │
│                                               │
│   Ask → Investigate → Agent Network →         │
│   Root Cause → Recommendations                │
└───────────────────────┬───────────────────────┘
                        │
                        ▼
┌───────────────────────────────────────────────┐
│              AI Orchestration Layer           │
│                                               │
│            Supervisor Agent                   │
│        Investigation & Delegation              │
└───────────────────────┬───────────────────────┘
                        │
              ┌─────────┼─────────┐
              ▼         ▼         ▼
           Sales      Finance    Support
           Agent       Agent      Agent
              │         │         │
              └─────────┼─────────┘
                        ▼
              Business Data Sources
                        │
                        ▼
                Analysis & Reasoning
                        │
             ┌──────────┴──────────┐
             ▼                     ▼
        Root Cause           Recommendations
```



# 🛠️ Technology Stack

## Frontend

* React
* Vite
* Tailwind CSS
* JavaScript
* Recharts / Data Visualization

## AI & Agent Layer

* Generative AI / LLMs
* Multi-Agent Architecture
* AI Agent Orchestration
* Tool-based AI workflows
* Structured investigation workflows

## Backend

* Python
* FastAPI
* REST APIs

## Data & Analytics

* Python
* Pandas
* NumPy
* Business analytics pipelines

## Development

* Git
* GitHub
* VS Code
* Netlify
---

#  Project Structure

```text
InsightFlow-AI/
│
├── src/
│   ├── components/
│   ├── pages/
│   ├── agents/
│   ├── services/
│   └── ...
│
├── .env.example
├── package.json
├── README.md
└── ...
```

---

#  Example Use Cases

##  Sales

**Question:**

> Why are sales declining this quarter?

The Sales Agent investigates sales trends, products, regions, and customer segments.

---

##  Finance

**Question:**

> Why has profitability decreased?

The Finance Agent investigates revenue, costs, expenses, and other financial metrics.

---

##  Customer Support

**Question:**

> Why have customer complaints increased?

The Support Agent analyzes complaint patterns, categories, and customer behavior.

---

##  Customer Retention

**Question:**

> Why are our premium customers leaving?

The system can combine Sales, Support, and Customer Analytics investigations.

---

#  Traditional Analytics vs InsightFlow AI

| Traditional Analytics      | InsightFlow AI                  |
| -------------------------- | ------------------------------- |
| User searches dashboards   | User asks a question            |
| Manual investigation       | AI-driven investigation         |
| One dashboard at a time    | Multiple specialist agents      |
| User finds possible causes | AI performs root-cause analysis |
| Manual interpretation      | AI-generated insights           |
| Manual next steps          | Actionable recommendations      |

---

#  What Makes InsightFlow AI Different?

Traditional AI business assistants often follow:

```text
Question → Answer
```

InsightFlow AI is designed around:

```text
Question
   ↓
Investigation
   ↓
Agent Delegation
   ↓
Analysis
   ↓
Root Cause
   ↓
Recommendation
```

The goal is not to build another chatbot.

The goal is to build an **AI employee capable of investigating business problems and helping teams make faster decisions.**

---

#  Human-in-the-Loop

For high-impact business actions, InsightFlow AI can incorporate human approval.

```text
AI Recommendation
       ↓
Risk Assessment
       ↓
Human Approval
       ↓
Action
```

This provides an additional layer of control before potentially sensitive business actions are executed.

---

#  Future Roadmap

### Phase 1 — Prototype

* [x] Natural-language business questions
* [x] Investigation workflow
* [x] Multi-agent workflow
* [x] Agent status visualization
* [x] Root-cause analysis interface
* [x] Recommendation interface

### Phase 2 — Real Business Data

* [ ] CRM integration
* [ ] Customer support integration
* [ ] Financial data integration
* [ ] Real-time business data
* [ ] Live dashboards

### Phase 3 — Autonomous Actions

* [ ] Create support tickets
* [ ] Update CRM records
* [ ] Send customer communications
* [ ] Generate reports
* [ ] Schedule follow-up tasks

### Phase 4 — Advanced Agents

* [ ] Agent memory
* [ ] Dynamic agent selection
* [ ] Long-running investigations
* [ ] Automatic anomaly detection
* [ ] Cross-system reasoning
* [ ] Agent performance monitoring

### Phase 5 — Enterprise

* [ ] Role-based access control
* [ ] Audit logs
* [ ] Multi-tenant architecture
* [ ] Enterprise integrations
* [ ] Advanced security
* [ ] Human approval workflows

---

# 📊 Expected Impact

InsightFlow AI aims to reduce the manual effort required to investigate business problems.

### Traditional Workflow

```text
Collect Data
     ↓
Open Dashboards
     ↓
Compare Metrics
     ↓
Find Anomalies
     ↓
Investigate Causes
     ↓
Prepare Report
     ↓
Decide Action
```

### InsightFlow Workflow

```text
Ask Question
     ↓
AI Investigates
     ↓
Specialist Agents Analyze
     ↓
Root Cause Identified
     ↓
Recommendations Generated
```
---


# ⚙️ Getting Started

## Prerequisites

Make sure you have:

* Node.js
* npm
* Git
* Python 3.10+
* Required API keys

## Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/InsightFlow-AI.git

cd InsightFlow-AI
```

## Install Dependencies

```bash
npm install
```

## Configure Environment Variables

Create a `.env` file and add the required API keys and configuration.

```env
API_KEY=your_api_key
```

**Never commit your `.env` file or secret API keys to GitHub.**

## Run the Application

```bash
npm run dev
```

Open the local URL provided by Vite in your browser.

---

# 🧪 Example

### User

```text
Why did revenue decline by 18% last month?
```

### InsightFlow AI

```text
Investigation Plan

✓ Understanding business question
✓ Creating investigation plan
✓ Analyzing sales
✓ Analyzing finance
✓ Analyzing customer support
✓ Comparing findings
✓ Identifying root cause
✓ Generating recommendations
```

### Result

```text
Root Cause:
Increased customer churn combined with
lower repeat purchases.

Recommendation:
Launch a targeted retention campaign and
investigate the increase in customer complaints.
```

---

# 🧠 Design Principles

### 1. Ask, Don't Search

Users should be able to ask questions naturally instead of manually navigating complex dashboards.

### 2. Investigate, Don't Guess

The system should follow a structured investigation process rather than immediately generating an unsupported answer.

### 3. Specialize Agents

Different agents can focus on different business domains.

### 4. Explain the Why

The system should help users understand the causes behind business changes.

### 5. Recommend Action

Insights should lead to practical next steps.

---

#  Hackathon

InsightFlow AI was developed for **The Great Agent Hackathon 2026**.

The project explores how agentic AI and multi-agent orchestration can transform traditional business analytics into an autonomous investigation workflow.

---

# 👥 Team

### Team Members

* **Mahek Chaurasia** — Backend Development
* **Sneha Chaurasia** — Frontend and Ideology

---

# 📄 License

This project is made for hackathon purpose.

---

## 💭 Vision

> **Businesses shouldn't have to search through dashboards to understand what's happening. They should be able to ask, investigate, understand, and act.**

### **InsightFlow AI — Ask. Investigate. Understand. Act.**

```
```
