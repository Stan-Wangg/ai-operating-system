# AI Operating System

An AI operating system is a folder of Markdown files that gives a coding agent, such as Claude Code or Codex, up-to-date context on your projects every time it starts.

This is the knowledge base and context layer over all my projects.

It holds what I'm working on, the status of each project, and the next steps.

It remembers the work I did before, so I can keep building.

The key thing: the coding agent always has the most up-to-date and relevant context.

By [Stanley Wang](https://github.com/Stan-Wangg), senior data analyst.

## Where this comes from

I was inspired by Andrej Karpathy's LLM wiki.

I turned it into a research wiki that is ever-growing.

I took the same principles and made them a knowledge context layer for businesses. It acts as a second brain, so people can work collaboratively with coding agents.

## It's just a folder

A coding harness connects to it. I run it on Claude Code. Codex connects to it and works the exact same way.

When one model gets better than the other, I switch. Nothing gets rebuilt.

## Why not use the tool's built-in memory

The memory layer inside these tools is not enough for a business. Here the memory is files you own.

## What's inside

```
AGENTS.md        the one rulebook the agent reads first
CURRENT.md       what is true right now
SESSION_LOG.md   what happened in each session
wiki/
  index.md       catalogue of every page
  log.md         record of every change
  projects/      one page per project
  decisions/     one dated page per decision
  feedback/      standing rules you have given the agent
```

| File | Answers |
|---|---|
| `AGENTS.md` | How should the agent work here? |
| `CURRENT.md` | What is true today, and what is next? |
| `wiki/` | What do we know, and why did we decide it? |
| `SESSION_LOG.md` | What happened last time? |

## Design decision: one rulebook

There is only AGENTS.md. No CLAUDE.md.

AGENTS.md is becoming the standard. Claude Code reads it too, so there is one file to maintain, not two.

Claude Code reads `AGENTS.md` when the folder has no `CLAUDE.md` (version 2.1.277 or newer).

## Example: a team

First and foremost, this is a knowledge layer for employees to go to AI first to retrieve information.

A lot of teams just use Claude and rely on the memory layer under the hood. Unfortunately that memory doesn't have the updated information or the current statuses, so after a long period of time it's not good enough to be useful.

Let's say an employee has a question for the business owner or a head of department. "Hey, where can I find this information to onboard a client?" That takes a couple of minutes out of that person's day, and there's a chance they're not online to reply.

It might sound like a small action. However, when you're onboarding a client it's time-sensitive, and you could lose a sale from it.

The operating system solves this by having updated context, so the employee asks the agent first.

## Make it your own

1. Fork this repo, or click **Use this template**.
2. Open the folder in Claude Code or Codex.
3. Say: "Read AGENTS.md, then ask me what I'm working on."
4. Replace the example project with your first real one.
5. At the end of each session, say: "Close the session." The agent updates `CURRENT.md` and `SESSION_LOG.md`.

It is very lean on purpose. Add a folder only when you need it.
