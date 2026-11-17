# Numerology Guide

A Vedic numerology agent for Mysstical Tarot. It calculates core numbers from a name and date of birth, draws the Vedic grid, checks compatibility, and answers quick questions, with clear guardrails.

**[Open the live demo](https://sargumchugh1234.github.io/ai-pm-portfolio/numerology-guide/)**

## Problem

- Numerology questions repeat: what is my number, what does it mean, are we compatible
- Each answer needs the same calculations done by hand
- Free calculators online use different methods, so people arrive with conflicting results

## Features

1. **My numbers:** Mulank, Bhagyank and Chaldean name number, with traits, favourable day, and the Vedic grid showing strong, missing and combination numbers
2. **Compatibility:** compares two dates of birth across four pairings and gives an overall pattern. Your details carry over from My numbers
3. **Ask:** quick answers about any number, your own numbers, the grid, missing numbers and compatibility

## How it calculates

- **Mulank:** birth day reduced to one digit (23 → 2 + 3 = 5)
- **Bhagyank:** all digits of the full date of birth, reduced to one digit
- **Name number:** Chaldean chart (A I J Q Y = 1, B K R = 2, C G L S = 3, D M T = 4, E H N X = 5, U V W = 6, O Z = 7, F P = 8), shown as compound and single digit
- **Vedic grid:** 3 1 9 / 6 7 5 / 2 8 4. Birth date digits without zeros, plus Bhagyank, plus Mulank when the birth day is 11 to 31 and not 10, 20 or 30
- **Compatibility:** friendly, neutral and challenging numbers based on traditional planetary friendships (1 Sun, 2 Moon, 3 Jupiter, 4 Rahu, 5 Mercury, 6 Venus, 7 Ketu, 8 Saturn, 9 Mars)

Published sources disagree on some details, such as using the full birth year or only its last two digits. I chose one method, documented it here, and kept every rule in one knowledge base object (`KB` in the code) so it can be replaced with my own teaching without touching the logic.

## Guardrails

- No health, pregnancy, death, accident or lifespan predictions
- No legal or financial advice, and no lucky numbers for trading, lottery or betting
- Never calls a number cursed or bad. Missing numbers are qualities to build
- Never tells anyone to marry, leave or reject someone. Compatibility is a pattern, not a verdict
- No name-change spellings. Those need a full consultation
- No guarantees
- Dates of birth are calculated in the browser and never stored or sent

## Checked against published examples

- 23-08-1990 → Mulank 5, Bhagyank 5
- SARAH → Chaldean 12 → 3

## Sources

- [The Lo Shu Grid – AstroMedha](https://astromedha.in/insights/lo-shu/grid)
- [Vedic Numerology – PanchangBodh](https://panchangbodh.com/vedic-numerology)
- [Psychic and Destiny Number Compatibility – AstroSight](https://astrosight.ai/kundli/psychic-and-destiny-number-compatibility)
- [Chaldean Numerology – Numerologist.com](https://numerologist.com/numerology/4-things-you-need-to-know-about-chaldean-numerology)
- [Vedic Grid Numerology Guide – Astrology Experts](https://astrologyexperts.in/blog/vedic-grid-numerology-guide-decode-predictions-using-your-date-of-birth/)
- [Vedic Numerology Grid Calculator – AstroLeaf](https://astroleaf.in/vedic-numerology-grid-calculator/)
