---
title: "CLAUDE CODE FULL COURSE 4 HOURS: Build & Sell (2026)"
date: 2026-04-21T18:53:24.319Z
type: youtube-video
source: https://www.youtube.com/watch?v=QoQBzR1NIqI
tags:
  - #ingested
  - #processed
threads_post: "Here are a few options for your post:

**Option 1 (Counterintuitive insight):**

Most people use Claude Code like a fancy autocomplete.

That's why they fail.

The real unlock? Git worktrees + sub-agents running in parallel.

One prompt = 5 Claude instances working simultaneously. Hours of work done in minutes.

Just dropped a 4hr masterclass showing exactly how 👇

**Option 2 (Hook-driven):**

Nobody talks about this, but your CLAUDE.md file is the difference between AI that ships and AI tha..."
notion_id: "34978e4b-f5c9-81c4-bb43-e8badfd85826"
---

## Source
[Watch on YouTube](https://www.youtube.com/watch?v=QoQBzR1NIqI)
**Channel:** Nick Saraev
**Complete Guide:** [Notion](https://www.notion.so/34978e4bf5c9818ab4a3fdb625a5c774)

## Summary
A 4-hour beginner-to-advanced Claude Code masterclass covering setup, IDE configuration, CLAUDE.md, hooks, sub-agents, Git worktrees, MCP tools, and cloud deployment—teaching you to build and automate real software projects efficiently.

## X Post (EN)
Here are a few options for your post:

**Option 1 (Counterintuitive insight):**

Most people use Claude Code like a fancy autocomplete.

That's why they fail.

The real unlock? Git worktrees + sub-agents running in parallel.

One prompt = 5 Claude instances working simultaneously. Hours of work done in minutes.

Just dropped a 4hr masterclass showing exactly how 👇

**Option 2 (Hook-driven):**

Nobody talks about this, but your CLAUDE.md file is the difference between AI that ships and AI tha...

## Threads Post (KR — Moongi 스타일)
Claude Code 4시간 강의 하나 봤어.

충격적인 건 이거야.

Sub-agent 여러 개 동시에 돌리고, Git worktree로 병렬 작업. 혼자서 팀 하나를 운영하는 수준이더라.

예전엔 개발자 5명 붙여서 몇 주 걸릴 일.
지금은 Claude Code 인스턴스 5개 띄우면 끝이야.

"나는 개발 못 해서 못 만들어요"
이 말, 2026년엔 변명도 안 돼.

툴은 이미 나왔어. Ship 할 사람만 없을 뿐이지.

Days, not months.
Solo, not team.

지금이 크리에이터한테 가장 미친 시기야.

## Complete Guide
# The Complete Guide to Claude Code: Building and Shipping Real Software in 2026

## Overview

Claude Code represents a fundamental shift in how developers—and non-developers—interact with software creation. Rather than writing every line of code manually, Claude Code allows you to direct an AI agent through natural language, enabling you to build production-ready applications, automate workflows, and deploy services to the cloud in a fraction of the time traditional development requires. This guide distills Nick Saraev's four-hour masterclass into a structured reference you can return to as you build.

The course covers everything from initial installation through advanced agentic workflows, including parallel execution with sub-agents, Git worktrees for simultaneous development streams, context and token management strategies, and cloud deployment via Modal. Whether you're a complete beginner trying to ship your first web app or an experienced developer looking to 10x your output, this guide will help you build a mental model of how Claude Code fits into a modern development stack.

By the end of this guide, you'll understand not just the commands and configurations, but the strategic thinking behind using Claude Code effectively: when to delegate to sub-agents, how to conserve tokens, how to verify AI output, and how to structure projects so the AI can reason about them intelligently.

## Key Concepts

### The Terminal and the IDE
Claude Code runs primarily in a terminal—a text-based interface for issuing commands to your computer. While this may feel intimidating at first, the terminal is dramatically more powerful than graphical interfaces because it can execute, chain, and automate commands. An **IDE (Integrated Development Environment)** like Visual Studio Code or Antigravity wraps the terminal with useful features: file browsers, syntax highlighting, and built-in AI panels. The course recommends **Antigravity** (Google's IDE) as a beginner-friendly option that integrates well with Claude Code.

### CLAUDE.md: The Project Brain
Every Claude Code project should contain a `CLAUDE.md` file at its root. This file is automatically loaded into context every time Claude Code runs, making it your project's "system prompt." It should contain:
- Project purpose and scope
- Coding conventions and style rules
- Architecture decisions
- Known constraints and gotchas
- Commands for testing and deployment

A well-written CLAUDE.md dramatically reduces the amount of re-explaining you need to do and improves Claude's output consistency.

### The .claude Directory
This hidden directory stores project-specific Claude Code configurations, including:
- **Slash commands** (reusable prompts invoked with `/commandname`)
- **Hooks** (scripts that fire on events like file edits)
- **Skills** (packaged capabilities Claude can invoke)
- **Sub-agents** (specialized mini-agents for specific tasks)

### Context Management
Large language models have finite context windows. Every file, conversation turn, and tool result eats into this budget. Efficient Claude Code use requires actively managing context through techniques like `/clear`, `/compact`, loading only relevant files, and offloading specialized work to sub-agents that maintain their own context windows.

### MCP (Model Context Protocol)
MCP is an open standard that lets Claude Code connect to external tools and services (Gmail, GitHub, databases, etc.). MCP servers expose tools Claude can call. Be aware: MCP tool definitions consume tokens even when unused, so enable only what you need.

### Skills vs. Sub-Agents vs. Plugins
- **Skills** are lightweight, reusable instructions Claude can invoke on demand—think of them as bundled expertise.
- **Sub-agents** are fully separate Claude instances with their own context windows, spawned to handle specific parallel tasks.
- **Plugins** are packaged extensions that add functionality to Claude Code itself.

### Git Worktrees
A Git worktree allows multiple branches of the same repository to exist simultaneously in different folders. Combined with Claude Code, this lets you run **multiple Claude instances in parallel**, each working on a different feature, then merging the results. This is where productivity compounds dramatically.

## Step-by-Step Breakdown

### Phase 1: Setup (0–25 minutes)
1. **Install Node.js** — required for Claude Code to run.
2. **Install Claude Code** via npm: `npm install -g @anthropic-ai/claude-code`
3. **Authenticate** by running `claude` in your terminal and following the login flow.
4. **Install Antigravity** (or VS Code) as your IDE.
5. **Open a new project folder**, launch the terminal inside it, and run `claude`.

### Phase 2: Your First Web App (25–45 minutes)
1. Create a project folder and `cd` into it.
2. Run `claude` to start the agent.
3. Create a `CLAUDE.md` file describing the project (e.g., "a simple landing page for a freelance proposal service").
4. Prompt Claude to scaffold the app: *"Build a responsive landing page with a hero, features, pricing, and contact form."*
5. Ask Claude to run a local dev server and iterate on design feedback.
6. **Verify the output** — open the rendered page, test links, and spot-check the code. Never trust AI claims of completion blindly.

### Phase 3: Leveling Up (45 minutes – 2 hours)
1. Explore the `.claude/` directory and create your first **slash command** (e.g., `/review` that asks Claude to audit code).
2. Add a **hook** that automatically runs your linter after any file edit.
3. Initialize Git and push to GitHub so Claude can reason about commits.
4. Integrate payment functionality (e.g., Stripe) and test end-to-end.

### Phase 4: Context and Token Management (2–2.5 hours)
1. Use `/clear` between unrelated tasks to reset context.
2. Use `/compact` to summarize long conversations.
3. Audit which MCP servers are enabled — disable anything unused.
4. Build **skills** for repetitive tasks (e.g., "write a commit message in our house style").

### Phase 5: Sub-Agents and Scaling (2.5–3.5 hours)
1. Convert a skill into a **sub-agent** when the task requires extended reasoning.
2. Create specialized sub-agents: a code reviewer, a test writer, a documentation generator.
3. Spin up an **agent team** where multiple sub-agents coordinate on a larger objective (e.g., email classification at scale).

### Phase 6: Parallelism and Deployment (3.5–4 hours)
1. Set up a **Git worktree** for each parallel task: `git worktree add ../feature-x feature-x-branch`.
2. Launch a Claude Code instance in each worktree. They work simultaneously without stepping on each other.
3. Deploy a backend API to the cloud using **Modal** — a serverless Python platform that integrates cleanly with Claude-generated code.
4. Merge worktrees back into main when features are verified.

## Practical Applications

- **Freelance client work**: Spin up client websites, proposals, and dashboards in hours instead of weeks.
- **Internal business automation**: Build custom tools (email classifiers, invoice processors, CRM integrations) without hiring a developer.
- **SaaS MVPs**: Go from idea to deployed product in a weekend using Claude Code + Modal.
- **Content and marketing ops**: Use sub-agents to parallelize research, writing, and editing tasks.
- **Agency scaling**: Use worktrees and agent teams to deliver multiple client projects simultaneously with the same headcount.

## Key Takeaways

- **Claude Code is a force multiplier, not a replacement for thinking.** Your judgment on architecture, verification, and product decisions is still what makes the output valuable.
- **The CLAUDE.md file is the single highest-leverage artifact** in any Claude Code project. Invest time writing it well.
- **Always verify.** AI confidently claims completion on tasks it hasn't actually finished. Test, click, and read the code.
- **Context is a scarce resource.** Manage it actively with `/clear`, `/compact`, and careful MCP hygiene.
- **Sub-agents unlock parallelism within a single session**; Git worktrees unlock parallelism across sessions. Use both.
- **Skills encode repeated expertise** — build them once, reuse forever.
- **Deployment matters.** Tools like Modal make it trivial to push Claude-generated APIs to production.
- **Start simple.** Build one small web app end-to-end before diving into sub-agents and worktrees.

## Related Resources

- **Vibe Coding with Antigravity (6-hour course)** — deeper dive into Antigravity-specific workflows.
- **Agentic Workflows (6-hour course)** — broader patterns for orchestrating AI agents beyond Claude Code.
- **n8n Full Course** — complement Claude Code with visual workflow automation for non-coding tasks.
- **Anthropic's official Claude Code documentation** — authoritative reference for flags, config options, and updates.
- **Modal documentation** — for serverless Python deployment.
- **MCP specification (modelcontextprotocol.io)** — to build or evaluate custom MCP servers.
- **Git worktree documentation** (`git help worktree`) — the underlying mechanic behind parallel Claude sessions.

With this foundation, you're equipped to not just use Claude Code, but to build real, monetizable software with it. The edge goes to builders who combine AI speed with rigorous verification and thoughtful system design — that's the positioning this course, and this guide, equip you for.

## Source Content
### Transcript
🔥 Join Maker School & get customer #1 guaranteed: https://skool.com/makerschool/about
💎 All course files: https://drive.google.com/drive/folders/1m182p16V_mZBAOTO-0iq4T4-cj6O-hev
📚 NEXT COURSE (ADVANCED): https://www.youtube.com/watch?v=UPtmKh1vMN8

💼 Work with my team to automate your business: https://dub.sh/work-with-me-epk
🎙️ Listen to my silly podcast: www.youtube.com/@stackedpod

📚 More free courses
→ Vibe Coding w/ Antigravity (6hr full course): https://www.youtube.com/watch?v=gcuR_-rzlDw
→ Agentic Workflows (6hr full course): https://www.youtube.com/watch?v=MxyRjL7NG18
→ N8N (6hr full course, 900K+ views): https://www.youtube.com/watch?v=2GZ2SNXWK-c

Summary ⤵️
The end-to-end, definitive course on Claude Code for beginners! I'll take you through a full four-hour masterclass where I start by teaching you how to set up and install Claude Code, how to configure your IDE or integrated development environment (we'll use Antigravity), how to utilize your CLAUDE.md file as your project brain, how to build your first project in Antigravity using Claude Code in under 15 minutes, advanced Claude Code functionality including hooks, slash commands, and more. 

I also teach you how to spin up multiple Claude Code instances and have them work on your behalf; how to parallelize work using sub-agents; how to use Git work trees to accomplish many hours of work in just a few minutes; how to conserve tokens and use context management to crush your coding and software projects; how to deploy things to the cloud using Modal and related services, and in general... how to be awesome at Claude Code!

My software, tools, & deals (some give me kickbacks—thank you!)
🚀 Instantly: https://link.nicksaraev.com/instantly-short
📧 Anymailfinder: https://link.nicksaraev.com/amf-short
🤖 Apify: https://apify.com?fpr=nick (30% off for 2 months with code 30NS) 
🧑🏽‍💻 n8n: https://n8n.partnerlinks.io/h372ujv8cw80
📈 Rize: https://link.nicksaraev.com/rize-short (25% off with promo code NICK)

Follow me on other platforms 😈
📸 Instagram: https://www.instagram.com/nick_saraev
🕊️ Twitter/X: https://twitter.com/nicksaraev
🤙 Blog: https://nicksaraev.com

Why watch?
If this is your first view—hi, I’m Nick! TLDR: I spent six years building automated businesses with Make.com (most notably 1SecondCopy, a content company that hit 7 figures). Today a lot of people talk about automation, but I’ve noticed that very few have practical, real world success making money with it. So this channel is me chiming in and showing you what *real* systems that make *real* revenue look like.

Hopefully I can help you improve your business, and in doing so, the rest of your life 🙏

Like, subscribe, and leave me a comment if you have a specific request! Thanks.

Chapters
00:00:00 Introduction to Claude Code
00:01:07 Learning the Basics of Claude Code
00:03:44 Setting Up Claude Code
00:08:05 Terminal vs. Graphical User Interface
00:12:23 Understanding IDEs
00:13:53 Exploring Visual Studio Code
00:19:11 Getting Started with Antigravity
00:24:01 Building Your First Web App with Claude Code
00:30:29 Utilizing the CLAUDE.md File (Project Brain)
00:34:40 Approaches to Website Design in CC +Antigravity 
00:41:47 Importance of Verification in AI
00:54:42 Advanced Claude Code Functionality
00:55:13 Understanding the .claude Directory
02:01:24 Adjusting the Proposal Design
02:01:55 Testing Payment Functionality
02:05:20 Leveraging GitHub for Project Management
02:06:12 Setting Up the Project
02:07:50 The Power of Automation
02:13:53 Context Management Explained
02:19:56 Understanding MCP Tools
02:27:23 Strategies for Token Management
02:35:29 Creating Skills for Efficiency
02:41:15 The Structure of Skills
02:44:39 Building a New Skill
02:50:58 Introduction to Model Context Protocol
02:58:15 Evaluating Token Usage in MCPs
03:07:57 Gmail Label Insights
03:09:07 Exploring Claude Code Plugins
03:11:08 Introduction to Sub-Agents
03:12:15 Transforming Skills into Sub-Agents
03:14:14 Scaling Email Classification
03:18:54 Creating Useful Sub-Agents
03:26:27 Understanding Agent Teams
03:32:59 Enabling and Using Agent Teams
04:02:34 Utilizing Git Worktrees
04:03:08 Deploying APIs with Modal

