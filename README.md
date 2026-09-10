# llm-council

A [Claude Skill](https://claude.com/) that replicates the structure of
[Andrej Karpathy's llm-council](https://github.com/karpathy/llm-council) — but instead of querying
multiple external LLM APIs through OpenRouter, Claude plays every role itself in a single conversation.

For hard, ambiguous, or high-stakes questions, a single first-pass answer can anchor on one framing.
This skill forces a more rigorous process instead:

1. **Independent opinions** — Claude drafts 3–4 genuinely distinct answers from different reasoning
   stances (e.g. pragmatist vs. rigor-first, optimist vs. skeptic, different domain lenses) — not the
   same answer reworded.
2. **Anonymous peer review** — each answer is anonymized and critiqued/ranked by every stance, including
   its own author, using a structured review + ranking format.
3. **Chairman synthesis** — an impartial "chairman" pass combines the strongest insights and rankings into
   one final, standalone answer, explicitly calling out where the council agreed vs. disagreed.

No external API calls, no servers, no API keys — it runs entirely within a single Claude conversation.

## Install

Drop `llm-council.skill` into your Claude skills, or point Claude at this repo's `SKILL.md`.

## When it triggers

Ask for a "council," "multiple perspectives," "second opinions," a "debate," or to "stress-test" or
"check" an answer — or just ask a consequential, judgment-call-heavy question and Claude will offer to
run it through the council process.
