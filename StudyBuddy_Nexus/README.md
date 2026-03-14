# Project Title: StudyBuddy Nexus 🎓

## Mission Overview
[cite_start]StudyBuddy Nexus is a Strategic Research Swarm designed to gather and synthesize unstructured academic data[cite: 18, 19]. [cite_start]It helps students navigate complex research by summarizing dense literature and indexing key findings.

## System Architecture (A2A Flow)

[cite_start]The system uses an Agent-to-Agent (A2A) flow[cite: 45]:
1. [cite_start]**The Scout Agent**: Scans unstructured data (PDFs/Web) for relevant research[cite: 19].
2. [cite_start]**The Analyst Agent**: Reasons over the gathered data to find insights and contradictions[cite: 19].
3. **The Editor Agent**: Compiles the final report for the user.

## Setup Instructions
1. Clone this repository.
2. Install dependencies: `pip install -r requirements.txt`.
3. [cite_start]Add your API Key to a `.env` file (DO NOT SHARE PUBLICLY [cite: 41]).
4. Run `python main.py`.

## Demo
https://youtu.be/FzKkKq_8tLc

## Flow
1. User input -> Scout Agent
2. Scout Agent -> Analyst Agent
3. Analyst Agent -> Final Mission Report

## Profiles
* The Scout (Data Ingestion): Responsible for gathering unstructured data, such as indexing PDFs or scraping research text
* The Analyst (Reasoning Engine): Synthesizes the gathered information to find insights and reason over complex data
* The Architect (Recovery specialist): Monitors the swarm's performance and handles failures if an agent fails to provide a reasoning trace.

## System Architecture
User Input -> [Scout Agent] -> Raw Data -> [Analyst Agent] -> Reasoned Synthesis
