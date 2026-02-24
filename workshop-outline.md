# Working with Coding Agents — Workshop Outline

## Opening

Quick icebreaker before diving in.

**Question:** What does your current dev workflow look like? IDE vs terminal? Which models? How are you using them?

---

## 1. The Agentic Timeline

What's happening right now and why this is bigger than code completion. Four signals:

- The METR benchmark — task complexity LLMs can handle is going vertical
- The AI Vampire (Yegge) — AI is supercharging pace, not replacing people
- $1 trillion wiped from software stocks — vertical SaaS moats are breaking
- Karpathy's Software 2.0 — "easily automates what you can verify"

**Question:** What's changing in your world? What shifts are you seeing in your workspace, your team, your industry?

---

## 2. What is a Coding Agent?

The anatomy — how you get from a base model to a coding agent in 5 layers:

1. Pre-training — "expensive autocomplete"
2. Post-training — "the assistant"
3. Reasoning — inference-time compute, let it think
4. Tool use + agentic loop — give it hands, let it act
5. The harness — where most of the secret sauce lives

Two approaches compared: OpenAI's dedicated coding model (codex-1) vs Anthropic's general model + harness (Claude Code). The harness is the product — system prompts define agent behaviour more than weights do.

**Question:** Which of these have you used? Cursor? Claude Code? Codex? Copilot? Windsurf? Open Code?

---

## 3. What is a Harness?

The wrapper that turns a model into a coding agent. Five components:

1. The loop — keep going until the job is done
2. The tools — read, write, search, execute
3. The instructions — system prompt + CLAUDE.md
4. The memory — manage what fits in context
5. The guardrails — permissions, safety, human-in-the-loop

Walk through real examples: Cursor (IDE), Claude Code (terminal), Codex (cloud), Open Code (open-source). Why "bash is all you need" — LLMs already understand terminals, files, and git.

**Question:** What surprised you about how these tools work under the hood? Anything you'd do differently knowing this?

---

## 4. Build Something

The best way to learn is to build. And build in public.

- Preview of April hands-on workshops
- Example: what I built with coding agents (RA-H)

**Question:** Bring something to build? Something you've already started? Something you've been putting off? Or start from scratch — we'll scaffold it together.

---

## 5. Setup a Coding Agent

Live demo. Open your terminal, install a coding agent, give it a task, watch it work.

- Option A: Open Code (free, open-source)
- Option B: Claude Code (requires Anthropic account)

Step by step, together.

---

## Open Questions

1. **Format check:** Is it okay to use slides at all? They're light and interactive — but want to confirm this works for the group vs pure demo/discussion. Hard to anchor the session without them.

2. **Content review:** Walk through the slides briefly — anything missing, anything to cut, anything that doesn't land?

3. **April workshops:** Need to clarify the idea for hands-on build sessions. Current thinking: attendees bring a project (or start fresh) and we scaffold a context graph together using a coding agent. What does this actually look like? Format, duration, prerequisites, what people walk away with.
