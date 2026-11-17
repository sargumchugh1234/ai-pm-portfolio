# Ask the Mill

A conversational search agent for paper mill teams. Planners, production heads and sales teams ask questions in plain language and get answers from planning and production data, with the numbers and the source behind them.

**[Open the live demo](https://sargumchugh1234.github.io/ai-pm-portfolio/ask-the-mill/)**

This demo is based on the Search and Knowledge agent I led for Kaiznn, which is live with customers. The demo runs on invented sample data for a fictional mill.

## Problem

- Answers were spread across order books, deckle plans and production logs
- A simple question meant opening several screens or asking the planning team
- Managers needed answers in seconds, but reports were built for analysts

## What the demo answers

- Trim waste and why it changed
- Order status and pending quantity, by customer or GSM
- Production against plan, by machine
- Reels and tons produced, and downtime

## How it works

Every question passes through the same 8 steps:

1. Understand the question and normalise mill shorthand (GSM, BF, PM1, PM2)
2. Classify the intent
3. Extract entities: GSM, machine, customer, dates
4. Score intent confidence
5. Retrieve the right data
6. Score data confidence
7. Answer, or ask a clarifying question when confidence is low
8. Cite the data source

The "Answer details" panel shows both confidence scores, the detected entities and the steps for every answer.

**Dual-confidence scoring** is the key design decision. The agent checks "Did I understand the question?" and "Do I have the right data?" separately. If either is low, it asks instead of guessing. In manufacturing, a confident wrong answer costs more than a follow-up question.

## Guardrails

- Answers only from mill data
- Asks when unsure instead of guessing
- Always shows the data source
- Read-only: never changes orders, plans or settings
- Users only see data they already have access to
- Declines questions unrelated to the mill

## Try

- "Why did trim waste go up this week?"
- "What's pending for BlueLine?"
- "How did PM1 do against plan?"
- "How are things?" (a vague question, to see it ask for clarification)

## Notes

The demo uses rule-based intent matching so it runs anywhere with no API keys. The production agent uses an LLM with retrieval.
