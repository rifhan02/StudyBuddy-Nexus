# Project Title: StudyBuddy Nexus 🎓

## Mission Overview
StudyBuddy Nexus is a Strategic Research Swarm designed to gather and synthesize unstructured academic data. It helps students navigate complex research by summarizing dense literature and indexing key findings.

## System Architecture (A2A Flow)
The system uses an Agent-to-Agent (A2A) flow:
1. **The Scout Agent**: Scans unstructured data (PDFs/Web) for relevant research.
2. **The Analyst Agent**: Reasons over the gathered data to find insights and contradictions.
3. **The Architect Agent**: Monitors the swarm's performance and handles failures if an agent fails to provide a reasoning trace.

## Profiles
* The Scout (Data Ingestion): Responsible for gathering unstructured data, such as indexing PDFs or scraping research text
* The Analyst (Reasoning Engine): Synthesizes the gathered information to find insights and reason over complex data
* The Architect (System Robustness): A specialized agent that monitors logs and triggers automated recovery paths if the reasoning chain is interrupted.
  
## Setup Instructions
1. Clone this repository.
2. Install dependencies: `pip install -r requirements.txt --user`.
3. Set your API Key: `export GEMINI_API_KEY='your_actual_key_here'`.
4. Run the swarm logic:  `python3 agents/logic.py`.

## Demo Video
https://youtu.be/FzKkKq_8tLc

## Flow
User Input -> Scout Agent -> Raw Data -> Analyst Agent -> Architect Monitoring -> Final Mission Report

graph TD
    User([User Input: Research Topic]) --> Scout[Scout Agent]
    
    subgraph Swarm Logic
        Scout -->|Unstructured Data| Analyst[Analyst Agent]
        Analyst -->|Reasoning Trace| Architect{Architect Agent}
        Architect -->|Check Robustness| Analyst
        Architect -->|Success| Final[Mission Report]
    end
    
    Final --> User
    
    style Architect fill:#f96,stroke:#333,stroke-width:2px
    style Swarm Logic fill:#f5f5f5,stroke:#d3d3d3,stroke-dasharray: 5 5
