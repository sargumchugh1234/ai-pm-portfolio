# AI PM Portfolio – Sargam Chugh

Working prototypes of AI agents I have designed as a Product Manager. Each project has a live demo, the product thinking behind it, and the guardrails that keep it safe.

I am an Associate Product Manager leading the AI transformation of Kaiznn, an order and deckle management platform for the paper and packaging industry. I also run Mysstical Tarot, a tarot, numerology and crystal business, which I use as a playground for AI products.

## Projects

| Project | What it does | Live demo |
| --- | --- | --- |
| [Ask the Mill](./ask-the-mill) | Conversational search agent that answers paper mill questions from planning and production data, with intent and data confidence shown for every answer | [Open demo](https://sargumchugh1234.github.io/ai-pm-portfolio/ask-the-mill/) |
| [Ask Tara](./ask-tara) | Booking assistant for Mysstical Tarot that helps visitors pick a reading, answers FAQs and keeps clear boundaries | [Open demo](https://sargumchugh1234.github.io/ai-pm-portfolio/ask-tara/) |
| [Numerology Guide](./numerology-guide) | Vedic numerology agent: Mulank, Bhagyank, Chaldean name number, Vedic grid, compatibility and quick questions | [Open demo](https://sargumchugh1234.github.io/ai-pm-portfolio/numerology-guide/) |

## How I build AI agents

- **Start with the user's real questions.** Map them into intents before writing any logic.
- **Write the guardrails before the happy path.** Every agent here has a list of things it will never do.
- **Ask instead of guessing.** When confidence is low, the agent asks a clarifying question.
- **Show the source.** Answers say where they came from.
- **Keep knowledge separate from logic.** Domain experts can update the knowledge without touching the code.

## About the demos

Each demo is a single HTML file with no build step and no data sent anywhere. They use rule-based matching so the behaviour, especially the guardrails, is predictable and easy to review. Production versions would add an LLM for open questions, with the same guardrails applied first.

All mill, customer and client data in these demos is invented sample data.

## Contact

- Portfolio: [SARGAM is your PM Buddy](https://app.notion.com/p/c66a21a8cb9342428904381eeeb4735a)
- LinkedIn: [Sargam Chugh](https://www.linkedin.com/in/sargam-chugh-aa0023183/)
- Email: sargamchugh1234@gmail.com
