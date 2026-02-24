---
marp: true
theme: rah-terminal
paginate: true
size: 16:9
---

<!-- _class: lead -->

# Working with Coding Agents
## Foundations and Guardrails

*The Remix — Byron Bay*

---

![bg contain](images/terminal.png)

---

![bg contain](images/chat.jpg)

---

## Today

**1. The Timeline** — where things are heading
**2. What is a Coding Agent?** — how they actually work
**3. What are the options?** — the tools available right now
**4. Setup a Coding Agent** — install one, live
**5. Build Something (April)** — what's next

---

<!-- _class: question -->

What are the most 'high taste', human elements of your work?

---

<!-- _class: question -->

What are the parts of your work that are most 'easily verifiable'?

---

<!-- _class: question -->

Anyone want to share?

---

## Why 'code-completion' is a big deal

- Code follows strict rules — easier for AI to predict than prose
- You can run it and instantly know if it works
- So the AI can try, fail, fix, and retry — in seconds
- That loop is the unlock

---

<span class="highlight">Give a sufficiently intelligent model basic access to your computer — the ability to run commands and read/write files — and it can do most of what humans do on a computer.</span>

---

![bg contain](images/fck.jpg)

---

<!-- _class: lead -->

# 1. The Timeline

Where things are heading — and why you need to be paying attention

![bg opacity:0.3](images/agentic%20timeline.jpg)

---

These tools are reshaping work and the entire economy right now. <span class="highlight">Learning how to use them is huge leverage.</span>

---

## The METR Benchmark

Time horizon of software tasks LLMs can complete — from minutes to hours. The curve is going vertical.

![contain](images/metr.jpg)

---

## $1 Trillion Wiped from Software Stocks

Nicolas Bustamante — 10 years building vertical SaaS.

![contain](images/10years%20saas.jpg)

---

## Karpathy: Software 1.0 vs 2.0

*"Software 1.0 easily automates what you can **specify**. Software 2.0 easily automates what you can **verify**."*

![contain](images/karpathy%20software.jpg)

---

![bg contain](images/steinberger.jpg)

---

## "AI is starting to kill us all, Colin Robinson style"

People are overworking because of AI. Not replacing us — supercharging the pace.

![contain](images/yegge-vampire.jpg)

---

![bg contain](images/rick-rubin-meme.jpg)

---

<!-- _class: question -->

What shifts are you seeing in your workspace, your team, your industry?

---

<!-- _class: lead -->

# 2. What is a Coding Agent?

The anatomy and the landscape

![bg opacity:0.3](images/anatomy%20of%20coding%20agent.jpg)

---

<!-- _class: question -->

Anyone want to have a guess at what 'harness' means?

---

## Creating a 'coding agent'

**1.** Pre-training — base model, "expensive autocomplete"
**2.** Post-training — SFT + RLHF, "the assistant"
**3.** Reasoning — inference-time compute, let it think
**4.** Tool use + agentic loop — give it hands, let it act

<span class="highlight">**5. The harness — the tools, the loop, the guardrails**</span>

*\*This is crude oversimplification*

---

## Different Approaches

🅾️ **OpenAI** — built a dedicated coding model. Specialised brain.

🔵 **Anthropic** — same general model, smarter harness. Same brain, different workshop.

🟢 **Kimi Code (Moonshot AI)** — open-source harness, open-weight model. Same idea as Anthropic, but everything is open.

---

## The harness is the product — and the secret sauce is 'largely' in the system message

> *"At their core is an AI model, but wrapped around it is a mix of code, tools, and prompts: the harness."*

Drew Breunig & Srihari Sriraman — *How System Prompts Define Agent Behavior* (Feb 2026)

![contain](images/drew.jpg)

---

![bg contain](images/harness_image.png)

---

A harness is the wrapper around the model that gives it tools, keeps it on track, and stops it from breaking things.

---

<!-- _class: question -->

Who has used/is using these coding tools? Would anyone like to share their current setup?

---

<!-- _class: question -->

Anyone else like to share their AI workflow or other agentic tools they're using?

---

<!-- _class: lead -->

# 3. What are the options?

The wrapper that turns a model into a coding agent

![bg opacity:0.3](images/what%20is%20harness.png)

---

## At a Glance

| | **Claude Code** | **Cursor** | **Codex** | **Open Code** |
|---|---|---|---|---|
| **Where** | Terminal | IDE (VS Code) | Cloud | Terminal |
| **Model** | Claude | Any | OpenAI (codex-1) | Any |
| **Cost** | Pay per use | $20/mo subscription | Pay per use | Free (BYO key) |
| **Best for** | Full autonomy | Visual editing | Background tasks | Experimenting |
| **Skill floor** | Comfortable with terminal | Familiar with VS Code | Minimal | Comfortable with terminal |

---

## Claude Code

Terminal-native. General-purpose Claude models + harness.

![contain](images/claudecode.webp)

---

## Cursor

IDE-based: editor + chat panel. Model-agnostic, multiple providers.

![contain](images/cursor.png)

---

## Codex

Cloud sandbox. Dedicated codex-1 model (o3 + RL).

![contain](images/codex.jpg)

---

## Open Code

Open-source terminal agent. Model-agnostic. Community-driven.

![contain](images/opencode.jpg)

---

## But it's fuzzy...

There are many different products and services built by and integrated with coding agents.

![contain](images/download-1.png) ![contain](images/download.jpg) ![contain](images/download.png)

---

<!-- _class: question -->

Any questions?

---

<!-- _class: lead -->

# 4. Setup a Coding Agent

Let's do it live

---

## ⚠️ Before We Install Anything

**The obvious risk:** you're giving a coding agent access to your computer. It can read, write, and delete your files. All of them. It can delete all of your shit.

**The less obvious risk:** prompt injection. If you install extensions or MCP servers you haven't vetted, a malicious instruction can hijack what the agent does — without you realising.

If you plan to keep using this stuff — just spend a couple of hours understanding the risks involved and how to mitigate.

---

## Step 1: Install

Go to [opencode.ai](https://opencode.ai/) — copy the install command. Open your terminal and paste it:

```bash
curl -fsSL https://opencode.ai/install | bash
```

Then close your terminal and reopen it.

---

## Step 2: Pick a Model

Inside Open Code:

- Type `/models` — pick a model (there are free ones)

---

## Step 3: Create a Project

```bash
mkdir ~/Desktop/my-first-project
cd ~/Desktop/my-first-project
opencode
```

**Or** — just ask the agent to create it for you.

- `mkdir` = **m**a**k**e **dir**ectory — creates a folder
- `cd` = **c**hange **d**irectory — moves into it

---

## Step 4: Build Something

Paste this prompt and watch it work:

> *"Create a single index.html file with a simple, clean todo list app. I can type a task and press enter to add it. Each task has a checkbox to mark it done and a delete button. Done tasks get a strikethrough. Dark theme, modern looking. All CSS and JS inline."*

---

## Step 5: Open It

Find the `index.html` file in your project folder and double-click it.

It opens in your browser. You just built that.

---

## Step 6: Vibe Away

Now make it yours. Ask the agent to:

- Add confetti when you complete a task 🎉
- Pull in a random motivational quote from the internet
- Make it play a sound when you delete something
- Surprise you

Let it cook. Tell it to search the web for ideas. See what happens.

---

<!-- _class: lead -->

# 5. Build Something (April)

And build it in public

![bg opacity:0.3](images/buildsomething.jpg)

---

## What's Next: April Workshops

Learn to do this in a more refined way:

- **MCP (Model Context Protocol)** — give your agent access to databases, APIs, and tools beyond just files
- **Better prompting** — how to guide an agent on longer, more complex tasks
- **Project setup** — rules files, context, guardrails

Bring something you've already started — or start fresh.

---

<!-- _class: lead -->

# Thanks

Let's build something.

*@bradwmorris*
