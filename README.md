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
    %% Styles - Optimized for Visibility
    classDef legacy fill:#f9f9f9,stroke:#333,stroke-width:1px,color:#000;
    classDef automation fill:#e1f5fe,stroke:#0277bd,stroke-width:2px,color:#000;
    classDef ai fill:#e8f5e9,stroke:#2e7d32,stroke-width:2px,color:#000;
    classDef output fill:#fff3e0,stroke:#ef6c00,stroke-width:2px,color:#000;

    subgraph "Data Sources (Legacy)"
        direction TB
        A[("Jira / Project Mgmt")]:::legacy
        B[("Financial Dashboards")]:::legacy
        C[("Timesheets & KPIs")]:::legacy
    end

    subgraph "Automation Engine (Python)"
        direction TB
        D[("Selenium Scraper")]:::automation
        E[("Pandas Cleaning")]:::automation
        F[("JSON Payload")]:::automation
    end

    subgraph "Intelligence (LangChain)"
        direction TB
        G[("LangChain Agent")]:::ai
        H[("LLM Reasoning")]:::ai
        I[("Variance Analysis")]:::ai
    end

    subgraph "Business Output"
        direction TB
        J[("Status Report")]:::output
        K[("Exec Summary Slide")]:::output
        L[("98% Effort Savings")]:::output
    end

    %% Connections
    A --> D
    B --> D
    C --> D
    
    D --> E
    E --> F
    
    F --> G
    G <--> H
    G --> I
    
    I --> J
    I --> K
    J --> L
    K --> L
