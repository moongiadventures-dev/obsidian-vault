---
title: "Obsidian + Claude Code: The Second Brain Setup That Actually Works"
date: 2026-04-21T18:57:00.241Z
type: youtube-video
source: https://www.youtube.com/watch?v=Y2rpFa43jTo
tags:
  - #ingested
  - #processed
threads_post: "Here's a compelling post under 500 characters:

---

Your \"second brain\" is useless if it's just a graveyard of notes.

The real unlock: pair Obsidian with Claude Code + GitHub.

→ Free version control + cloud backup
→ Git plugin = auto-sync (no terminal needed)
→ Claude Code skills that actually *manage* your notes, not just store them

Counterintuitive truth: the best PKM system isn't the one with the prettiest notes—it's the one an AI can navigate faster than you can.

Full walkthrough 👇
..."
notion_id: "34978e4b-f5c9-81be-b84f-d08f686c8262"
---

## Source
[Watch on YouTube](https://www.youtube.com/watch?v=Y2rpFa43jTo)
**Channel:** Eric Tech
**Complete Guide:** [Notion](https://www.notion.so/34978e4bf5c9812b92bbe2d7f307868c)

## Summary
Learn how to build a powerful "second brain" by integrating Obsidian with Claude Code for personal knowledge management. The tutorial covers setting up GitHub for free version control, using the Git plugin for automatic syncing, and installing Obsidian CLI skills so Claude Code can manage your notes and projects.

## X Post (EN)
Here's a compelling post under 500 characters:

---

Your "second brain" is useless if it's just a graveyard of notes.

The real unlock: pair Obsidian with Claude Code + GitHub.

→ Free version control + cloud backup
→ Git plugin = auto-sync (no terminal needed)
→ Claude Code skills that actually *manage* your notes, not just store them

Counterintuitive truth: the best PKM system isn't the one with the prettiest notes—it's the one an AI can navigate faster than you can.

Full walkthrough 👇
...

## Threads Post (KR — Moongi 스타일)
Second brain, 드디어 제대로 돌아가더라.

Obsidian 혼자 쓸 때? 그냥 노트 무덤이었어.
근데 Claude Code 붙이니까 게임이 바뀜.

내 노트를 AI가 직접 읽고, 정리하고, 연결해.
Terminal 안 건드려도 GitHub에 자동 백업.
프로젝트 관리까지 Claude가 해줌.

핵심은 이거야.
노트는 쌓는 게 아니라 굴리는 거.
AI가 내 knowledge base를 실제로 "쓸 수 있는" 형태로 만들어줘야 second brain이지.

Setup 30분. 평생 바뀜.

지식은 저장이 아니라 실행이야.

## Complete Guide
# Building a Second Brain with Obsidian and Claude Code: The Complete Setup Guide

## Overview

The concept of a "second brain" — a reliable, searchable system for capturing thoughts, notes, and project information — has long been a goal for knowledge workers. While tools like Notion, Roam, and Evernote have each had their moment, the combination of **Obsidian** (a local-first markdown editor) and **Claude Code** (Anthropic's agentic coding assistant) creates something genuinely new: a knowledge base that you fully own, version-controlled for free, and intelligently managed by an AI agent that understands your workflow.

This guide walks through the full setup demonstrated in the video: configuring Obsidian as your personal knowledge management (PKM) hub, connecting it to GitHub for automatic cloud backup and version control, and installing custom Claude Code "skills" that let the AI read, write, and organize your notes on command. The end result is a system where you can ask Claude to draft project notes, summarize research, create structured documents, or reorganize your vault — all while your data stays on your local machine and syncs safely to a private repo.

Unlike paid sync services (Obsidian Sync is $4–8/month), this approach costs nothing beyond your existing tools and gives you far more control. It's also portable — the entire vault is just a folder of markdown files, which means it works with any editor and will outlive any specific app.

## Key Concepts

### Obsidian as a Local-First Knowledge Base
Obsidian stores notes as plain markdown files in a folder on your machine called a **vault**. There's no proprietary database, no lock-in, and no internet dependency. This makes it ideal as the foundation for a second brain because your data is already in a format (markdown) that AI tools can natively read and write.

### GitHub for Version Control and Backup
By turning your Obsidian vault into a Git repository and pushing it to GitHub, you get three things for free:
- **Cloud backup** — your notes are safely stored off-device
- **Version history** — every change is tracked, so you can recover any previous state
- **Multi-device sync** — pull the repo to any machine with Obsidian installed

### The Obsidian Git Plugin
Rather than manually using the terminal to commit and push changes, the community **Obsidian Git** plugin automates syncing. It can auto-commit on an interval, pull on startup, and push in the background — making version control invisible.

### Claude Code Skills
**Skills** are reusable instruction sets that extend Claude Code's capabilities for specific domains. The Obsidian skill (by Kepano, Obsidian's CEO) teaches Claude how to interact with an Obsidian vault — understanding its folder structure, formatting conventions, links, tags, and metadata. Once installed, Claude becomes a competent assistant for managing your notes.

### Agentic Note Management
The breakthrough here is that Claude Code doesn't just generate text — it can read your existing vault, understand context, create new notes in the right places, link them to related content, and even refactor your organization system. This turns PKM from a manual discipline into a collaborative workflow.

## Step-by-Step Breakdown

### 1. Create a GitHub Repository (1:28)
- Log into GitHub and create a **new private repository** (e.g., `obsidian-vault`)
- Do **not** initialize with a README — you'll be pushing an existing folder
- Copy the repo URL for later

### 2. Install and Set Up Obsidian (3:25)
- Download Obsidian from [obsidian.md](https://obsidian.md)
- Create a new vault in a location you'll remember (e.g., `~/Documents/vault`)
- Open the terminal, navigate to your vault folder, and initialize Git:
  ```
  git init
  git remote add origin <your-repo-url>
  git add .
  git commit -m "Initial commit"
  git push -u origin main
  ```

### 3. Configure Automatic Cloud Backups (4:21)
- In Obsidian, go to **Settings → Community plugins** and disable Restricted Mode
- Browse and install the **Obsidian Git** plugin
- Enable the plugin and configure:
  - **Auto-commit interval** (e.g., every 10 minutes)
  - **Auto-pull on startup** (so edits from other devices come in)
  - **Auto-push** (so changes are immediately backed up)
- Verify by editing a note and checking your GitHub repo for the commit

### 4. Install the Obsidian Skill for Claude Code (7:32)
- Clone or download the skill from [github.com/kepano/obsidian-skills](https://github.com/kepano/obsidian-skills)
- Place the skill file in your Claude Code skills directory (typically `~/.claude/skills/`)
- Point Claude Code to your Obsidian vault path so it knows where to operate

### 5. Run Claude Code from Your Vault (8:16)
- Open a terminal in your vault directory
- Launch Claude Code
- Start issuing instructions like:
  - "Create a new project note for Q4 planning with a weekly checklist"
  - "Summarize all notes tagged #research from this month"
  - "Refactor my daily notes into a monthly index"

## Practical Applications

**Project Management** — Ask Claude to scaffold a project folder with a brief, task list, meeting notes template, and linked resource page. It handles the structure while you focus on the content.

**Research Synthesis** — Dump raw notes or web clippings into an inbox folder, then have Claude process them: tagging, summarizing, and filing them into topic-based notes.

**Meeting Notes & Follow-ups** — After a call, paste a transcript and ask Claude to extract action items, create task notes, and link them to the relevant project.

**Daily and Weekly Reviews** — Have Claude generate a weekly review by reading your daily notes, summarizing progress, and flagging open loops.

**Knowledge Base Maintenance** — Periodically ask Claude to audit your vault: finding orphan notes, suggesting missing links, and reorganizing folder structures as your thinking evolves.

**Writing and Drafting** — Use your vault as context for long-form writing. Claude can draft articles by pulling from your existing notes, maintaining your voice and references.

## Key Takeaways

- **Obsidian's plain-markdown vault is the ideal substrate for AI-assisted PKM** — no lock-in, no proprietary formats
- **GitHub provides free, reliable sync and versioning** — eliminating the need for paid sync services
- **The Obsidian Git plugin automates backups** — set it up once and forget about the terminal
- **Claude Code skills turn the AI into a domain-specific assistant** — the Obsidian skill gives it native fluency with your vault
- **Agentic note management shifts PKM from discipline to delegation** — Claude handles organization so you can focus on thinking
- **The whole stack costs nothing beyond your Claude subscription** — and you keep full ownership of your data

## Related Resources

- **[Obsidian Skills by Kepano](https://github.com/kepano/obsidian-skills)** — The official skill repo referenced in the video
- **[NotebookLM + Claude Code](https://youtu.be/fV17ZkPBlAc)** — A complementary workflow for research-heavy projects
- **[Obsidian Git Plugin documentation](https://github.com/denolehov/obsidian-git)** — Full configuration options for automatic syncing
- **[Claude Code Skills documentation](https://docs.claude.com/en/docs/claude-code)** — Learn to build your own custom skills for other workflows
- **Building a Second Brain by Tiago Forte** — The foundational book on PKM methodology (CODE and PARA frameworks pair well with this setup)
- **[bookzero.ai](https://bookzero.ai)** — Example of a production app built with Claude Code, mentioned by the creator

With this setup in place, your notes become more than storage — they become a living, AI-augmented extension of your thinking, fully under your control and backed up by default.

## Source Content
### Transcript
This video details how to construct a powerful "second brain" by integrating Obsidian with Claude Code, showcasing its application for effective "personal knowledge management". We explore using Obsidian for "project management" and leveraging Claude Code as an "ai assistant" to manage notes, including creating specialized Obsidian "claude code skills" for enhanced note-taking workflows. Join our School community to access all resources and further discussions!

Key takeaways:

- Set up Obsidian with GitHub for free version control and cloud backup
- Install the Git plugin for automatic syncing without touching the terminal
- Use Obsidian CLI skills to let Claude Code manage your notes, projects, and knowledge base

🔗 Join our School community: skool.com/erictech

🔗 Check out bookzero.ai — AI-powered bookkeeping built entirely with Claude Code

📌 Mentioned videos:

- NotebookLM + Claude Code: https://youtu.be/fV17ZkPBlAc?si=fWYwV08LGUtiAzxj

- Obsidian Skill: https://github.com/kepano/obsidian-skills

Timestamps:
0:00 — Intro
1:28 — GitHub Repo Setup
3:25 — Obsidian Setup
4:21 — Cloud Backups
7:32 — Obsidian Skills
8:16 — Demo & Results
16:19 — Outro

#claudecode #obsidian #secondbrain

