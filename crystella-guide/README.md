# Crystella Guide

A crystal guide agent for Crystella, my crystal line under Mysstical Tarot. People describe what they're going through in their own words, the agent suggests crystals that fit, and once they choose one it gives a complete guide to using it.

**[Open the live demo](https://sargumchugh1234.github.io/ai-pm-portfolio/crystella-guide/)**

## Problem

- Customers rarely know which crystal they need. They know their problem: stress, sleep, money, a breakup
- After buying, the same questions come back: which hand do I wear it on, how do I charge it, can I wash it
- Care advice online is inconsistent, and some of it damages stones (water on selenite, sun on amethyst)

## How it works

1. **Describe the problem** in free text or tap a common concern
2. **Get 2–3 suggestions**, each with a one-line reason
3. **Choose one** and get the full guide:
   - What it supports and why it fits
   - Chakra, best wrist and stones it pairs with
   - How to use it as a bracelet, tumble, palm stone, tower or raw piece, and pendant
   - Cleansing and charging methods that are safe for that specific stone (water, sun and salt flags)
   - How often to cleanse
   - A 4-step intention ritual and a daily affirmation
   - Care and storage

Free text is matched to 14 concerns (stress, sleep, love, heartbreak, confidence, money, focus, protection, overthinking, anger, communication, motivation, new beginnings, intuition) across 19 crystals.

## Guardrails

- **Crisis first:** if someone mentions suicide or self-harm, the agent stops recommending crystals and shares Tele-MANAS (14416 / 1-800-891-4416) and the emergency number 112
- **Not medicine:** never claims a crystal cures or treats illness, and never suggests stopping medication
- **Health questions** are pointed to a doctor, with crystals offered only as comfort alongside care
- **No crystal water:** warns against drinking gem water, since some stones release harmful substances
- **No guarantees:** crystals support intention and action, they don't guarantee outcomes
- **Child and pet safety:** small stones are a choking hazard

Replies that hit a guardrail are marked in the demo so the rule is visible.

## Design choices

- **Problem first, crystal second.** Users start from what they feel, not from crystal names
- **Safety is per stone.** Care instructions come from water, sun and salt flags on each crystal, so the guide never recommends a method that damages that stone
- **Knowledge is separate from logic.** Crystals and concerns live in two data objects (`C` and `CONCERNS`) that can be edited without touching the conversation code

## How I'll measure it

- Share of conversations that end with a crystal chosen
- Clicks from the guide to buying from Crystella
- Fewer repeat care questions after purchase

## Sources

- [How to Cleanse and Charge Crystals – Crystals.com](https://www.crystals.com/blogs/news/how-to-cleanse-and-charge-crystals)
- [Which Hand Should You Wear Your Crystal Bracelet? – Solacely](https://solacely.co/blogs/crystals/which-hand-should-you-wear-your-crystal-bracelet)
- [25 Essential Crystals and Their Meanings – Crystals.com](https://www.crystals.com/blogs/news/25-essentialcrystals-and-their-meanign-breif-guide)
- [Tele-MANAS – Ministry of Health and Family Welfare](https://pib.gov.in/PressReleasePage.aspx?PRID=2022057)
