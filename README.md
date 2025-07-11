
FundSight AI — Project Plan

---

Project Overview

Build an AI-powered Business Investment Evaluator that analyzes startup business models, investment terms (e.g., $X for Y% equity), and market potential to determine profitability, return on investment (ROI), and risk factors.

Target Users:
- Angel investors
- Startup accelerators
- Early-stage VCs
- Founders validating pitches
- Business students learning investment analysis

---

1. MVP Goal

Given a business idea and investment terms, provide a clear verdict on investment viability, estimated ROI, risk factors, and an AI-generated investment memo.

---

2. MVP Features

- Input Form
  - Business description
  - Market / Industry
  - Revenue model (e.g., subscription, B2B)
  - Investment terms ($ amount for % equity)
  - Time horizon for exit / ROI

- AI Analysis Engine
  - Extract key info from input using GPT
  - Estimate market size (TAM/SAM/SOM)
  - Benchmark revenue growth and exit potential
  - Calculate break-even points and ROI (IRR) scenarios
  - Flag risks (market size, competition, moat, etc.)

- Output Report
  - Verdict: Investable / Risky / Avoid
  - Financial forecast (revenue, equity returns)
  - AI-generated memo summarizing investment rationale and risks
  - (Optional) Export as PDF report

- User Interface
  - Clean, investor-focused web UI
  - Responsive form + results page

---

3. System Architecture

Layer          | Technology Stack
---------------|-------------------
Frontend       | Next.js, Tailwind CSS, shadcn/ui
Backend        | FastAPI or Django REST framework
AI Layer       | OpenAI GPT-4 API via LangChain / LangGraph
Database       | PostgreSQL (or SQLite for MVP)
Integrations   | Crunchbase API (optional for market data)
Hosting        | Vercel (frontend), Railway/Render (backend)

---

4. High-Level Workflow

User Input: Business & Investment Terms
  ↓
GPT Extracts Key Data
  ↓
Market Size & Growth Estimation
  ↓
Revenue & Exit Scenario Modeling
  ↓
Equity Dilution & ROI Calculation
  ↓
Risk Assessment & Memo Generation
  ↓
Output Verdict & Report

---

5. Technical Components

Input Processing
- Structured form inputs
- GPT-powered natural language parsing for unstructured descriptions
- (Optional) Pitch deck upload and automated parsing

Market Analysis Module
- GPT estimates TAM/SAM/SOM from description and external data
- Scraping/integration with Crunchbase or similar for comparable company data

Financial Modeling
- Valuation and equity percentage calculations
- Revenue growth projections based on business model type
- IRR and ROI calculations over specified time horizon

AI Reasoning & Risk Flagging
- GPT identifies market, competition, and business model risks
- Generates investment memo explaining rationale

Reporting
- Web UI report display
- Exportable PDF summary (optional)

---

6. Milestones & Timeline

Week | Goals & Deliverables
-----|----------------------
1    | Setup project repo, user input UI, backend scaffold, OpenAI API integration
2    | Implement GPT pipeline for data extraction & market estimation
3    | Develop financial model: ROI, IRR, dilution, exit simulation
4    | Build output report UI + generate investment memo
5    | Testing, bug fixes, deploy MVP (Vercel + Railway/Render)
6+   | User feedback, polish UI, add PDF export, integrate Crunchbase API

---

7. Future Enhancements

- Cap Table Simulator: Model multiple rounds, SAFE to equity conversions
- Real-time Market Comps: Integrate PitchBook, CB Insights, or public datasets
- Memory & Portfolio Tracking: Store multiple deals and track ongoing returns
- Email Parsing: Automate deal update ingestion from investor emails
- Mobile App: For on-the-go deal evaluation
- Multi-user Accounts: For syndicates or fund management

---

8. User Acquisition & Feedback Strategy

- Target angel investor communities on LinkedIn and AngelList
- Share in startup and VC forums (Reddit: r/startups, r/venturecapital)
- Offer free deal evaluation during beta phase
- Collect user feedback & iterate rapidly

---

9. Sample User Input & Output

Input:
- Business: "AI bookkeeping SaaS for freelancers"
- Market: Small-to-medium businesses
- Revenue model: $19/month subscription
- Investment: $100,000 for 10% equity
- Exit goal: $3 million in 5 years

Output:
- Market size estimated at $400M TAM
- Competitive landscape: High (QuickBooks, Xero)
- Break-even projected at 3 years with $50K MRR
- Risks: Low pricing power, narrow moat
- Verdict: Moderate viability, requires niche or GTM advantage

---

10. Useful Resources & APIs

- OpenAI GPT-4 API: https://platform.openai.com/docs/models/gpt-4
- Crunchbase API: https://data.crunchbase.com/docs
- LangChain Documentation: https://docs.langchain.com
- PitchBook: https://pitchbook.com (for inspiration)
- CB Insights: https://www.cbinsights.com

---

11. Next Steps

- Setup repo & project skeleton
- Draft detailed GPT prompts for data extraction & viability evaluation
- Design wireframes for user input and report pages
- Start implementation and share progress for feedback

---

Feel free to ask if you want help with:
- Project repo & folder structure
- Sample GPT prompt templates
- Database schema design
- UI wireframes/mockups
- MVP code snippets

Let’s build this impactful AI-powered investment tool! 🚀
