# AI-Driven Program Management Agent
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Selenium](https://img.shields.io/badge/-selenium-%2343B02A?style=for-the-badge&logo=selenium&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-Agents-green?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Production-success?style=for-the-badge)

## 📋 Executive Summary
**Problem:** Managing a **Multi **Million USD Healthcare IT Engagement** involves collating data from disparate sources (Jira, Financial Dashboards, Excel trackers) for Weekly Status Reports (WSR). This manual "toil" consumed ~4-5 hours per week per Project Manager.

**Solution:** I architected and deployed a **Python + LangChain** automation agent that scrapes, aggregates, and analyzes project metrics.

**Outcome:** * **98% reduction** in manual reporting effort (reduced to <5 mins/week).
* Eliminated copy-paste errors in executive presentations.
* Allowed leadership to focus on strategy rather than data entry.

---

## 🏗️ System Architecture
The solution treats "Project Reporting" as an ETL (Extract, Transform, Load) problem, with an LLM as the transformation engine.

```mermaid
graph TD
    %% Styles
    classDef legacy fill:#f9f9f9,stroke:#333,stroke-dasharray: 5 5;
    classDef automation fill:#e1f5fe,stroke:#01579b,stroke-width:2px;
    classDef ai fill:#e8
