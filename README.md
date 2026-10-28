# Synthetix-Grid

**Autonomous Decoupled Multi-Agent Swarm for Block-Level Urban Climate Resilience**

Track: Agentic AI Engineer
Author: Madhumitha.D

Pitch deck: [Synthetix-Grid_Pitch_Deck.pdf](Synthetix-Grid_Pitch_Deck.pdf)

---

## Overview

Micro-level urban disasters such as flash floods, power grid failures and hyper-local heat islands escalate faster than central authorities can process incoming data. Most disaster management tools are dashboards that need a human operator to triage information manually, causing a decision delay of roughly 45-60 minutes.

Synthetix-Grid is an agentic AI swarm built on a Decoupled Supervisor-Worker multi-agent pattern. Agents independently monitor micro-data, run localized predictions, write relief-routing code and trigger automated actions through APIs.

Target impact: reduce emergency response time from 45 minutes to under 60 seconds.

## Agents

- Orchestrator / Router Agent: routes tasks and supervises the workers
- Data Ingestion Agent: polls sensor, weather and social APIs, normalizes data, flags anomalies
- Predictive Code Solver Agent: calculates inundation zones, writes path-finding code, self-corrects failed tool calls
- Action Dispatch Agent: sends SMS alerts, calls map routing APIs, reroutes emergency logistics

## Tech Stack

- Presentation: Next.js 14 + TailwindCSS (live agent trace dashboard)
- Orchestration: LangGraph / AutoGen (stateful execution graphs)
- Intelligence: Llama 3 70B via Groq + Claude (planning), ChromaDB vector store
- Data Ingestion: FastAPI + async Python workers

## User Journey

1. Trigger: the Ingestion Agent detects a rainfall sensor spike (above 80 mm/hr).
2. Reasoning: the Predictive Solver pulls elevation maps, writes a path-finding script and calculates flood zones.
3. Execution: the Dispatch Agent sends SMS alerts and reroutes emergency vehicles through map APIs.

## Feasibility and Safety

- Built on open-source frameworks (LangGraph, FastAPI, ChromaDB) and accessible LLM endpoints.
- Fallback routing to lightweight local models reduces API cost and avoids token exhaustion under load.
- Confidence thresholds with human override for high-impact actions; every decision is logged in the agent trace.
- Future scope: edge deployment on Raspberry Pi / Jetson modules for offline operation.

## Status

This repository currently contains the concept and pitch deck. Implementation is planned using the stack above.

## Author

Madhumitha.D, B.E. Computer Science and Engineering
