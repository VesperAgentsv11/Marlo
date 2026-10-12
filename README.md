<p align="center">
  <img src="assets/banner.webp" alt="Marlo: A Leading OpenHarness" width="100%">
</p>

<h3 align="center">The desktop AI coding agent that plans, edits, tests and ships code in your real projects.</h3>
<p align="center">Built on the <b>Vesper Engine</b> · Zero data retention · Bring any model · You approve every risky step</p>

<p align="center">
  <a href="https://github.com/VesperAgentsv11/Marlo/releases/latest"><img alt="Latest release" src="https://img.shields.io/github/v/release/VesperAgentsv11/Marlo?label=release&color=e11d2e&style=for-the-badge"></a>
  <a href="https://github.com/VesperAgentsv11/Marlo/releases"><img alt="Downloads" src="https://img.shields.io/github/downloads/VesperAgentsv11/Marlo/total?color=111111&style=for-the-badge"></a>
  <img alt="Windows 10 and 11" src="https://img.shields.io/badge/Windows-10%20%7C%2011-111111?style=for-the-badge&logo=windows&logoColor=white">
  <img alt="Zero data retention" src="https://img.shields.io/badge/data%20retention-zero-e11d2e?style=for-the-badge">
</p>

<p align="center">
  <a href="https://github.com/VesperAgentsv11/Marlo/releases/latest"><b>⬇ Download Marlo for Windows</b></a>
</p>

---

## Contents

[What is Marlo](#what-is-marlo) · [Zero data retention](#-zero-data-retention) · [The Vesper Engine](#%EF%B8%8F-the-vesper-engine) · [Built-in skills](#-built-in-skills) · [Self-improvement](#-self-improvement) · [Behaviour](#-how-marlo-behaves) · [Decision models](#%EF%B8%8F-decision-models) · [Permissions](#%EF%B8%8F-permissions) · [Models](#-bring-any-model) · [Get started](#-get-started) · [FAQ](#-faq)

---

## What is Marlo?

Marlo is an AI software engineer that lives on your desktop. Point it at a project folder, describe what you want in plain words, and it gets to work:

1. **Understands** your request, restating it in one line so a misunderstanding is caught before any work starts.
2. **Reads** your code to learn how the project builds, tests and is structured.
3. **Plans** larger tasks as a short checklist you can follow live.
4. **Edits** files, **runs** your tests, linters and builds, and **fixes** what it broke.
5. **Reports back** with what changed, how it was checked, and anything still open.

You watch every step, can steer it mid-task, and nothing risky runs without your OK.

---

## 🔒 Zero data retention

Marlo has **no servers and keeps no copy of your work**. Everything stays on your computer.

| | |
|---|---|
| **No Marlo cloud** | There is no Marlo backend. Your code, chats, plans and settings never pass through us. |
| **No telemetry** | Usage analytics are off, and Marlo sends nothing about how you use it. |
| **Local storage only** | Sessions, checkpoints, feedback and memory live in a local database in `%APPDATA%\Marlo`, on your machine. |
| **Encrypted keys** | API keys and tokens are encrypted with Windows' own protection (DPAPI). They are never stored in plain text, never shown to the model and never written to logs. |
| **Direct to your provider** | When the agent needs a model, it talks straight to the provider *you* chose, with *your* key. Nothing in between. |
| **Fully offline option** | Run local models through Ollama or LM Studio and no prompt ever leaves your computer. |
| **You own the data** | Export everything or delete sessions, usage history and caches at any time from Settings → Data & Privacy. |

> Your model provider's own data policy applies to the requests you send them. For zero retention end to end, use a local model or a provider plan with zero data retention.

---

## ⚙️ The Vesper Engine

Marlo is the app; the **Vesper Engine** is the agent runtime underneath it:

- **Agent loop:** planning, tool calls, retries with backoff, automatic fallback to backup models during outages, and context compaction for long sessions.
- **Tools:** read, search and edit files, a real terminal with background processes, web search and fetch, MCP servers, sub-agents for parallel research, and rich result cards.
- **Permission engine:** classifies every command and file change before it runs (see [Permissions](#%EF%B8%8F-permissions)).
- **Skills:** 40+ built-in expert skills, loaded only when a task needs them (see below).
- **Self-improving harness:** learns from finished tasks and your feedback, with every change verified and reversible.
- **Decision models:** optional fast "second opinion" models for triage and safety checks.
- **Provider adapters:** OpenAI, Anthropic and every other supported provider, with streaming, reasoning effort and vision.

---

## 🧩 Built-in skills

Skills are expert playbooks the agent loads **only when a task matches**, so they cost nothing until they're needed. The Vesper Engine ships with **42 built-in skills**, all switched on by default:

| Area | Skills |
|---|---|
| **Core engineering** | engineering core habits, surgical coding, verify before done, receiving review, refactoring, codebase onboarding |
| **Planning & thinking** | brainstorming, writing plans, architecture, test-driven development |
| **Quality** | debugging, testing, code review, web-app testing, accessibility, performance, concurrency |
| **Languages & stacks** | TypeScript, React, Python, databases, shell scripting, Electron, mobile apps, CLI tools |
| **Building with AI** | LLM apps, MCP server builder, skill creator, web research, data analysis |
| **Shipping & operations** | git workflow, DevOps, release, incident response, observability, dependency upgrades, API integration, security |
| **Craft** | frontend design, docs, internationalization, memory consolidation ("dream") |

On top of these:

- **Featured design skills** (taste, canvas design, frontend design, design lab) for interfaces that look hand-crafted, not generated.
- **Skill marketplace:** 32 more expert playbooks in one click (premium UI polish, design systems, landing pages, clean architecture, API design, performance profiling, test-suite architecture, code review, product specs, MVP builder, RAG pipelines, AI agents, security audits, CI/CD, Docker, auth, and more).
- **Your own skills:** write them, import them from a folder or `.zip`, or simply ask Marlo to create one for a procedure you repeat.

---

## 🔁 Self-improvement

Marlo gets better at **your** projects the more you use it, and you stay in charge of every change.

- **Learns after each task:** a short review of the finished session proposes improvements to the agent's own notes, skills, sub-agents and memory.
- **You approve what changes:** low-risk updates can apply automatically if you allow it; medium- and high-risk ones always wait for you.
- **Verification gate:** a proposed improvement is kept only if your project's tests, lint, type check and build still pass. Otherwise it is rolled back automatically.
- **Learns from your feedback:** rate any reply with 👍 or 👎 and add a note ("too slow", "use tabs"). Marlo turns your ratings into guidance for later sessions. Feedback stays on your computer, and you can switch learning off at any time.
- **Fully versioned:** every change to the agent's setup has a version you can inspect and revert, with results tracked over time.
- **Project memory:** a "dream" pass consolidates what it learned into a small, organised memory the agent reads at the start of each session.

---

## 🧭 How Marlo behaves

Marlo is tuned to work like a careful senior engineer, not a code generator:

- **Gets the request exactly right.** It reads for intent (short, informal or misspelled messages are fine), treats screenshots and pasted errors as the most precise part of the request, does every part of a multi-part message, and applies your corrections everywhere they apply.
- **Does what you asked, and only that.** No surprise features, renames or redesigns; worthwhile extras are suggested in one line at the end.
- **Matches effort to the task.** A question or one-file fix is handled directly; bigger work gets a live task list you can follow.
- **Understands before it changes.** It reads the relevant code and conventions first, and matches your project's style, naming and comment density.
- **Verifies its own work.** It runs your tests, linter, type checker and build, fixes what it broke, and never weakens or deletes tests to make them pass.
- **Talks to you while it works.** Short, plain updates on what it's doing and why; setbacks are reported, never hidden.
- **Takes steering.** Type while it's working; your message lands after the current step and the plan adjusts without a restart.
- **Respects limits.** Configurable budgets for turns, tokens and time; long sessions are compacted automatically; backup models take over if your main one fails.

---

## ⚖️ Decision models

Marlo can work alongside a **decision model**: a small, fast model that doesn't write text but answers typed questions (yes/no, a choice, a score) with calibrated probabilities in milliseconds. Connect **Jev (TypeSafe)**, run **Laya on your own computer**, or use any compatible endpoint. A model running locally is **detected automatically**.

Marlo uses it as a second opinion next to your main model:

- **Request triage:** before a run, it reads your request (type, whether to plan first, ambiguity and risk) and gives the agent a hint.
- **Prompt-injection checks:** web pages, files and tool output are checked for hidden instructions aimed at the AI, on top of Marlo's own detection.
- **`decide` tool:** the agent can ask quick, structured questions while it works.

Every use can be switched on or off. **Approvals and safety rules never depend on it:** you still decide.

---

## 🛡️ Permissions

Every command and file change is checked by the Vesper Engine's permission engine **before** it runs. Choose a mode per session:

| Mode | What runs on its own | What asks you first |
|---|---|---|
| **Ask** | Nothing | Every command and file write |
| **Auto** (recommended) | Read-only commands, `git status / diff / log`, test, lint and build scripts, lockfile installs, and edits inside the project | Deleting files, `git push` / `reset --hard`, global installs, `sudo`, network uploads, writes outside the project, secret files and system config |
| **Full Access** | Everything | Only the always-confirm list below |

**Always confirms, even in Full Access:**

- recursively deleting a drive root, filesystem root, home directory or system directory;
- formatting or partitioning disks;
- writing raw data to disk devices;
- fork bombs and recursive permission changes on the filesystem root;
- shutting down or rebooting the machine;
- writing to operating-system directories (`C:\Windows`, `/etc`, `/usr`, …).

**More control:**

- **Allow and deny rules** per project or globally, with wildcards. Deny rules win over everything, including Full Access. "Always allow in this project" adds a rule in one click.
- **Approval cards:** approve, edit the command before it runs, deny with a reason (the agent is told not to retry it unchanged), or always allow.
- **Plan mode:** read-only research and a proposed plan; nothing changes until you approve it.
- **Checkpoints:** every edit is a checkpoint. Review changes hunk by hunk, accept or reject them, and rewind at any time.
- **Prompt-injection guard:** content from files, web pages and tools is treated as data, never as instructions.
- **Stays in your project:** file tools and `@`-mentions can't reach outside the project folder.

---

## 🧠 Bring any model

Use the models you already pay for, or run them locally:

**OpenAI** (API key or ChatGPT subscription) · **Anthropic** (API key or Claude subscription) · **OpenRouter** · **Qwen Cloud** · **Alibaba Token Plan** · **Kimi (Moonshot)** · **Z.ai** · **Cline / ClinePass** · **NaraRouter** · **OpenCode Zen / Go** · **Ollama / LM Studio** (local) · **any OpenAI-compatible endpoint**

Pick a model per session, set the reasoning effort from *low* to *max*, and add backup models that take over automatically during outages. Marlo knows each model's context size, vision and reasoning support.

---

## 🚀 Get started

1. **Download** `Marlo-Setup-x.y.z-x64.exe` from the [latest release](https://github.com/VesperAgentsv11/Marlo/releases/latest) and run it.
   > Marlo isn't code-signed yet, so Windows may show *"Windows protected your PC"*. Click **More info → Run anyway**.
2. **Connect a model:** Settings → Providers → add an API key, or sign in with your ChatGPT or Claude subscription.
3. **Pick a project folder** and describe your task, for example *"Add a dark mode toggle to Settings and keep the tests green."*

**Updates are automatic.** Marlo checks for new versions at startup and every 6 hours, shows **New update available**, and installs when you say so.

**System requirements:** Windows 10 or 11 (64-bit), about 450 MB of disk space, a model (API key, subscription or local), and Git (recommended, for checkpoints and branches).

---

## ❓ FAQ

**Is my code sent anywhere?** Only to the model provider you choose, directly, when the agent needs it for your task. Marlo has no servers and keeps no copy. With a local model, nothing leaves your computer.

**Does it cost anything?** Marlo itself is free. Model usage is billed by your provider, or covered by your subscription.

**Can it break my project?** Every edit is a checkpoint you can rewind, risky actions ask first, and destructive system-level commands always ask, even in Full Access.

**Which model should I use?** Any strong coding model works. Marlo adapts to each model's context size, vision and reasoning settings.

**How do I report a bug?** Open an [issue](https://github.com/VesperAgentsv11/Marlo/issues) with what you did and what happened. Logs are in `%APPDATA%\Marlo\logs`.

---

<p align="center">
  <b>Marlo</b> · built on the Vesper Engine<br>
  <a href="https://github.com/VesperAgentsv11/Marlo/releases/latest">Download</a> ·
  <a href="https://github.com/VesperAgentsv11/Marlo/releases">All releases</a> ·
  <a href="https://github.com/VesperAgentsv11/Marlo/issues">Report an issue</a>
</p>
