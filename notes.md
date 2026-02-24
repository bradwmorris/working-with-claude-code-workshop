# Presentation Notes & Additional Information

## Slide-by-Slide Notes

### Slide 1: Title
- Title slide for "Working with Coding Agents"
- Event: The Remix — Byron Bay

### Slide 2: Before we start
- **Type:** Question/Discussion slide
- **Purpose:** Icebreaker to get audience engaged
- **Format:** Open discussion / hands up / icebreaker
- **Question:** What does your current dev workflow look like? IDE vs terminal? Which models? How are you using them?

### Slide 3: The Agentic Timeline
- **Note:** IMAGE: GENERATE — s1-agentic-timeline.png
- This slide needs a generated diagram showing the agentic timeline

### Slide 4: The METR Benchmark
- Image: `images/metr.jpg`
- Key point: Time horizon of software tasks LLMs can complete — from minutes to hours. The curve is going vertical.

### Slide 5: Steve Yegge — The AI Vampire
- Image: `images/yegge-vampire.jpg`
- Quote: "AI is starting to kill us all, Colin Robinson style"
- Source: Steve Yegge — *The AI Vampire* (Feb 2026)
- Key point: People are overworking because of AI. Not replacing us — supercharging the pace.

### Slide 6: $1 Trillion Wiped from Software Stocks
- Image: `images/10years saas.jpg`
- Source: Nicolas Bustamante — 10 years building vertical SaaS.
- Key point: 5 moats destroyed. 5 holding. The ones that broke were the ones that kept competitors out.

### Slide 7: Karpathy: Software 1.0 vs 2.0
- Image: `images/karpathy software.jpg`
- Quote: "Software 1.0 easily automates what you can **specify**. Software 2.0 easily automates what you can **verify**."
- Note: Karpathy is the highest signal-to-noise voice in AI. First principles, no hype.

### Slide 8: What's changing in your world?
- **Type:** Question/Discussion slide
- **Purpose:** Open discussion
- **Questions:** What shifts are you seeing — in your workspace, your team, your industry? Personal examples? Meta-level observations?

### Slide 9: What is a Coding Agent?
- **Note:** IMAGE: GENERATE — s2-coding-agent-anatomy.png
- This slide needs a generated diagram showing coding agent anatomy

### Slide 10: The 5 Layers
- Breakdown of coding agent layers:
  1. Pre-training — base model, "expensive autocomplete"
  2. Post-training — SFT + RLHF, "the assistant"
  3. Reasoning — inference-time compute, let it think
  4. Tool use + agentic loop — give it hands, let it act
  5. The harness — the tools, the loop, the guardrails
- Key point: Most of the secret sauce lives in layer 5.

### Slide 11: Two Different Approaches
- OpenAI: Built a **dedicated coding model** — codex-1 is o3 with additional RL on real coding tasks.
- Anthropic: Claude Code uses the **same general-purpose models** you'd use for anything else.
- Key point: The coding agent behaviour comes from the harness: the tools, the loop, the system prompt.
- Tagline: **Same brain, different workshop.**

### Slide 12: The Harness is the Product
- Image: `images/drew.jpg`
- Key point: System prompt composition across 6 coding agents. Tool descriptions, workflow guidance, personality — all defined in the prompt, not the weights.

### Slide 13: "At their core is an AI model..."
- Image: `images/drew2.jpg`
- Quote: "At their core is an AI model, but wrapped around it is a mix of code, tools, and prompts: the harness."
- Source: Drew Breunig & Srihari Sriraman — *How System Prompts Define Agent Behavior* (Feb 2026)

### Slide 14: The Secret Sauce Lives in the Harness
- Key points:
  - The model provides intelligence.
  - The harness provides **everything else**.
  - Quote: "Model quality sets a ceiling; the harness, policy, and eval loop determine whether that ceiling is reached."
  - The same model that writes poetry also writes your code. What makes it a *coding agent* is the wrapper.

### Slide 15: Which of these have you used?
- **Type:** Question/Discussion slide
- **Purpose:** Show of hands / quick poll
- **Tools mentioned:** Cursor? Claude Code? Codex? Copilot? Windsurf? Open Code?
- **Question:** What's your experience been?

### Slide 16: What is a Harness?
- **Note:** IMAGE: GENERATE — s3-harness.png
- This slide needs a generated diagram showing what a harness is

### Slide 17: Five Things
- The five components of a harness:
  1. The loop — keep going until the job is done
  2. The tools — read, write, search, execute
  3. The instructions — system prompt + CLAUDE.md
  4. The memory — manage what fits in context
  5. The guardrails — permissions, safety, human-in-the-loop
- Summary: A harness is the wrapper around the model that gives it tools, keeps it on track, and stops it from breaking things.

### Slide 18: Cursor
- Image: `images/cursor.png`
- Description: IDE-based: editor + chat panel. Model-agnostic, multiple providers.

### Slide 19: Claude Code
- Image: `images/claudecode.webp`
- Description: Terminal-native. General-purpose Claude models + harness.

### Slide 20: Codex
- Image: `images/codex.jpg`
- Description: Cloud sandbox. Dedicated codex-1 model (o3 + RL).

### Slide 21: Open Code
- **Note:** opencode.mp4 is a video — switch to live demo or screenshot
- **Action item:** Brad: show this live or grab a screenshot to embed
- Description: Open-source terminal agent. Model-agnostic. Community-driven.

### Slide 22: Why Claude Code Works: Bash is All You Need
- Image: `images/bash all you need.jpg`
- Quote: "There's a growing conviction that filesystems and bash are the optimal abstraction for AI agents."
- Key point: LLMs already understand terminals, files, and git. Give your agent a shell and let it work.

### Slide 23: Questions?
- **Type:** Question/Discussion slide
- **Purpose:** Open discussion
- **Questions:** What surprised you about how these tools work under the hood? Anything you'd do differently knowing this?

### Slide 24: Build Something
- **Note:** IMAGE: GENERATE — s4-build-in-public.png
- This slide needs a generated diagram/image

### Slide 25: What's Next: April Workshops
- **Action item:** Brad: flesh out with dates, format, specifics
- Key points:
  - We're planning hands-on build sessions.
  - Bring something you've already started — or start fresh.
  - The goal: go from zero to working prototype with a coding agent in one session.

### Slide 26: That's What I Did
- **Note:** short_reddit_look.mp4 is a video — switch to screen share
- **Action item:** Brad: show this live — quick walkthrough of what you built
- Key point: Built RA-H from scratch using coding agents. Not a developer by training — but the tools close the gap.

### Slide 27: Bring Something to Build
- **Type:** Question/Discussion slide
- **Questions:**
  - Something you've already started?
  - Something you've been putting off?
  - Or start from scratch — we'll scaffold the context graph together.
- Key point: The best way to learn a coding agent is to **use** one on a real problem.

### Slide 28: Setup a Coding Agent
- **Note:** Live demo section

### Slide 29: Open Your Terminal
- Two options provided:
  - Option A: Open Code (free, open-source) — `npx open-code@latest`
  - Option B: Claude Code (requires Anthropic account) — `npm install -g @anthropic-ai/claude-code` then `claude`
- Note: We'll walk through it step by step.

### Slide 30: Live Demo
- **Action item:** Brad: live demo here
- Steps:
  1. Open terminal
  2. Install Open Code or Claude Code
  3. Point it at a project
  4. Give it a task
  5. Watch it work

### Slide 31: Thanks
- Closing slide
- Tagline: Let's build something.
- Twitter: @bradwmorris

## Images Needed

1. **s1-agentic-timeline.png** — Diagram showing the agentic timeline (to be generated)
2. **s2-coding-agent-anatomy.png** — Diagram showing coding agent anatomy (to be generated)
3. **s3-harness.png** — Diagram showing what a harness is (to be generated)
4. **s4-build-in-public.png** — Image for "Build Something" section (to be generated)

## Videos/Media

1. **opencode.mp4** — Video of Open Code in action (needs to be converted to screenshot or shown live)
2. **short_reddit_look.mp4** — Video walkthrough of RA-H (needs to be shown live or converted to screenshot)

## Action Items for Brad

1. Flesh out April Workshops slide with dates, format, specifics
2. Show Open Code live or grab a screenshot to embed
3. Show RA-H walkthrough live — quick walkthrough of what you built
4. Live demo section — demonstrate coding agent setup and usage
