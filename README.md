# AI-Multichannel-Lead-Operations-Engine
AI-powered multichannel lead classification, routing, assignment and lifecycle tracking engine built with n8n and Groq.

## Overview

This project implements an AI-powered multichannel lead classification, routing, assignment, and lifecycle tracking system built using n8n and Groq LLM.

The engine consolidates leads from multiple sources (Website, WhatsApp, Gmail, App forms) into a centralized Google Sheets database and applies AI-based classification logic to determine intent, urgency, recommended action, and operational routing.

This system acts as an intelligent backend operations layer for sales and service organizations.

---

## Problem Statement

Businesses receive leads from multiple channels:

- Website forms
- WhatsApp inquiries
- Email
- Social media
- Offline entry

These leads are often:
- Unstructured
- Not categorized properly
- Not routed to the correct team
- Not tracked through lifecycle stages

Manual processing creates:
- Delayed response
- Missed follow-ups
- Poor visibility
- Revenue leakage

This engine centralizes and automates lead operations using AI-driven logic.

---

## Architecture

### Lead Collection Layer (External – Future Integration)

- Website Forms
- WhatsApp API
- Gmail API
- App Integrations

All leads are consolidated into a single Google Sheet.

---

### AI Processing Layer

1. Google Sheets Trigger / Manual Trigger
2. Lead Data Extraction
3. AI Agent (Groq LLM)
4. Lead Classification:
   - Intent (Inquiry / Purchase / Service / Replacement)
   - Product Type
   - Capacity / Requirement
   - Usage Type
   - Urgency
   - Budget Sensitivity
   - Lead Score
   - Recommended Action

5. Sheet Update (Structured Fields)

---

### Operations Routing Layer

- Telegram Bot Notification (Currently)
- WhatsApp Business API (Planned)

Operations team receives:

- Lead details
- AI classification
- Recommended action
- Lead ID

Team replies:

RECEIVED <LeadID> → Marks as Assigned  
CLOSED <LeadID> <Remark> → Marks as Closed with remark

---

### Lifecycle Tracking

Each lead moves through:

- New
- Assigned
- In Progress
- Closed

All updates are reflected in the centralized sheet.

---

## Technologies Used

- n8n (Workflow Automation)
- Groq LLM (llama-3.1-8b-instant)
- Google Sheets API
- Telegram Bot API
- Prompt Engineering
- Structured JSON Output Control

---

## Key Features

- AI-based intent classification
- Automated lead scoring
- Multichannel aggregation design
- Centralized operations control
- Lifecycle status tracking
- Telegram-based command handling
- Structured system prompt enforcement
- Human-in-the-loop confirmation

---

## Design Philosophy

This system is built as an operations backend engine.

It does not replace sales teams.
It augments operational clarity.

Goals:
- Reduce manual sorting
- Reduce missed leads
- Increase accountability
- Enable scalable routing
- Maintain full audit trail

---

## Current Limitations

- Poll-based execution (manual trigger in development)
- No persistent database (Google Sheets used as temporary store)
- No RAG-based product database yet
- No analytics dashboard
- Telegram used instead of WhatsApp Business API
- No SLA monitoring layer yet

---

## Enterprise Upgrade Roadmap

1. Replace Google Sheets with PostgreSQL
2. Add RAG for structured product database retrieval
3. Add SLA timers and escalation alerts
4. Add performance dashboard
5. Add agent-based routing (Sales / Service / Installation)
6. Integrate WhatsApp Business API
7. Add CRM synchronization layer

---

## Production Risks

- LLM misclassification if prompt constraints weakened
- API dependency risk
- Poll-based delay in trigger
- Manual override required for edge cases

---

## Future Vision

This engine can evolve into a non-geographic AI-driven operations layer for distributed service businesses.

Scalable model:
- Central AI classification
- Distributed execution teams
- Unified visibility
- Multichannel acquisition
- Structured lifecycle management

---

## Author

**Mohanarengan Krishnaraja**  
AI Automation Developer  
