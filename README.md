# Agentic Coding for Beginners

**Stop copy-pasting from ChatGPT. Start building with AI in your terminal.**

If your current workflow looks like this:

1. Google the problem
2. Ask ChatGPT
3. Copy the code
4. Paste into VS Code
5. Pray it works
6. When it doesn't, go back to step 2

...then this guide is for you. There's a better way, and it takes 5 minutes to set up.

---

## Table of Contents

- [What Even Is Agentic Coding?](#what-even-is-agentic-coding)
- [Why Should I Care?](#why-should-i-care)
- [The 3 Tools You Should Know About](#the-3-tools-you-should-know-about)
- [Getting Started (Pick One)](#getting-started-pick-one)
  - [Claude Code](#claude-code)
  - [OpenAI Codex CLI](#openai-codex-cli)
  - [Gemini CLI](#gemini-cli)
- [Your First 15 Minutes](#your-first-15-minutes)
- [How to Actually Talk to These Tools](#how-to-actually-talk-to-these-tools)
- [Real Student Examples](#real-student-examples)
- [Mistakes Every Beginner Makes](#mistakes-every-beginner-makes)
- [Which Tool Should I Use?](#which-tool-should-i-use)
- [The One File That Changes Everything](#the-one-file-that-changes-everything)
- [Going Further](#going-further)

---

## What Even Is Agentic Coding?

You know how ChatGPT gives you code and you copy-paste it? **Agentic coding tools live inside your terminal and edit your code directly.** They can:

- Read your entire project (not just the one file you pasted in)
- Create and edit files for you
- Run your code and fix errors automatically
- Use the terminal (install packages, run tests, use git)
- Go back and forth until something actually works

Think of it like this:

| | ChatGPT | Agentic Coding Tool |
|---|---|---|
| Where it runs | Browser tab | Your terminal / VS Code |
| Knows your project? | Only what you paste | Reads all your files |
| Edits your code? | No, you copy-paste | Yes, directly |
| Runs your code? | No | Yes |
| Fixes its own mistakes? | Only if you paste the error | Sees the error and retries |

**It's the difference between texting a tutor photos of your homework vs. having the tutor sit next to you at your laptop.**

---

## Why Should I Care?

Real talk -- here's what changes:

- **Homework that took 3 hours takes 30 minutes.** Not because AI does it for you, but because you stop getting stuck on syntax errors and environment issues.
- **You actually understand the code.** Because the AI explains what it's writing, in your project, not some generic example.
- **You debug faster.** The AI sees the error, reads your code, and suggests fixes with context you'd have to manually explain in ChatGPT.
- **You learn tools real developers use.** Git, terminal, testing, project structure -- the AI uses them, and you learn by watching.

> This is not about cheating. This is about learning with a tool that meets you where your code actually is.

---

## The 3 Tools You Should Know About

There are three major agentic coding tools right now. All free to start. All work in your terminal.

| Tool | Made By | Free Tier | Best For |
|---|---|---|---|
| **Claude Code** | Anthropic | Yes (with limits) | Best overall, great at explaining |
| **Codex CLI** | OpenAI | Yes (with limits) | If you already use ChatGPT/OpenAI |
| **Gemini CLI** | Google | Yes (with limits) | Generous free tier, good for trying out |

You don't need all three. **Pick one and start.** You can always try the others later.

---

## Getting Started (Pick One)

### Claude Code

**What it is:** Anthropic's terminal-based AI coding tool. Reads your files, edits code, runs commands.

**Install:**
```bash
npm install -g @anthropic-ai/claude-code
```

> Don't have npm? You need Node.js first. Download it at [nodejs.org](https://nodejs.org) -- grab the LTS version, install it, restart your terminal.

**First run:**
```bash
cd your-project-folder
claude
```

It will ask you to log in the first time. After that, you just talk to it.

**Also available as:**
- A VS Code extension (search "Claude Code" in extensions)
- A desktop app (Mac and Windows)
- A web app at [claude.ai/code](https://claude.ai/code)

---

### OpenAI Codex CLI

**What it is:** OpenAI's terminal-based AI coding tool. Similar concept to Claude Code.

**Install:**
```bash
npm install -g @openai/codex
```

**First run:**
```bash
cd your-project-folder
codex
```

You'll need an OpenAI API key or to log in with your ChatGPT account.

---

### Gemini CLI

**What it is:** Google's terminal-based AI coding tool.

**Install:**
```bash
npm install -g @anthropic-ai/gemini-cli
```

> Note: Check [Google's docs](https://github.com/google-gemini/gemini-cli) for the latest install command as this may change.

**First run:**
```bash
cd your-project-folder
gemini
```

You'll sign in with your Google account.

---

## Your First 15 Minutes

Okay, you installed one. Now what? Here's a dead-simple first session.

### Step 1: Open your terminal and navigate to any project folder

```bash
cd ~/my-project
```

Don't have a project? Make one:

```bash
mkdir my-first-ai-project
cd my-first-ai-project
```

### Step 2: Launch the tool

```bash
claude
```
(or `codex` or `gemini`, whichever you installed)

### Step 3: Ask it to build something

Try typing this:

```
Build me a simple to-do list app using HTML, CSS, and JavaScript. 
Make it look clean and modern. Save todos to localStorage so they 
persist when I refresh the page.
```

**Watch what happens.** It will:
1. Create the files
2. Write the code
3. You can ask follow-up questions like "add a delete button" or "make it dark mode"

### Step 4: Look at what it made

Open the files in VS Code or your editor. **Read the code.** This is the learning part. You'll see patterns, structure, and techniques you can reuse.

### Step 5: Ask it to explain

```
Explain the JavaScript in this project like I'm a beginner. 
What does each function do?
```

**That's it.** You just built a project, and you can actually explain how it works.

---

## How to Actually Talk to These Tools

The way you prompt matters. Here's the difference between beginner prompts and prompts that actually get good results.

### Be specific about what you want

```
Bad:  "make a website"
Good: "Create a personal portfolio website with an about section, 
       a projects section with 3 cards, and a contact form. 
       Use HTML, CSS, and vanilla JavaScript."
```

### Tell it what you're working with

```
Bad:  "fix my code"
Good: "The login form in index.html isn't submitting. When I click 
       the submit button nothing happens. Can you check the event 
       listener in script.js?"
```

### Ask it to explain, not just fix

```
Bad:  "make it work"
Good: "Fix the bug and explain what was wrong so I understand it"
```

### Give it context about YOU

```
"I'm a CS student learning React for the first time. 
 I understand HTML and basic JavaScript but I've never 
 used components before. Explain things at that level."
```

### Iterate, don't start over

Instead of re-explaining everything when something's not right:

```
"That's close, but make the navbar sticky at the top 
 and change the color scheme to blue/white"
```

The tool remembers the whole conversation. Use that.

---

## Real Student Examples

Here are things you can actually do right now:

### "I have a Java assignment and I'm stuck"

```
I need to implement a binary search tree in Java. 
I have the TreeNode class already. I need insert, 
search, and delete methods. Can you help me write 
them and explain the logic?
```

### "I need to set up a project and I don't know how"

```
I need to create a React app for my web dev class. 
Set up the project, create a basic file structure, 
and add a homepage component. I've never used React before.
```

### "My code has a bug and I can't figure it out"

```
My Python script is supposed to read a CSV file and 
calculate the average of the "grades" column, but it 
keeps giving me a TypeError. Can you look at my code 
and figure out what's wrong?
```

The tool will read your actual files, find the bug, fix it, and explain what happened.

### "I need to learn git"

```
I've never used git before. Initialize a git repo for 
this project, show me the basic commands, and help me 
make my first commit. Explain each step.
```

---

## Mistakes Every Beginner Makes

### 1. Not reading the code it writes

The tool writes code for you. **Read it.** If you can't explain what it does, ask the tool to explain it. Accepting code you don't understand is the fastest way to fail an exam or break your project.

### 2. Accepting everything without thinking

AI makes mistakes. It might:
- Use a library you weren't supposed to use for class
- Over-engineer a simple assignment
- Write code that works but violates your assignment requirements

**Always review against your requirements.**

### 3. Not being in the right folder

The tool reads files from wherever your terminal is currently at. If you're in your home folder instead of your project folder, it can't see your code.

```bash
# Always cd into your project first
cd ~/my-project
claude
```

### 4. Giving vague prompts then getting frustrated

"Make a website" and "Build a recipe website with a search bar, recipe cards with images, and a favorites feature using React" will give you wildly different results. **The more specific you are, the better the output.**

### 5. Using it to cheat instead of learn

If you use it to generate code you turn in without understanding, you will:
- Fail when asked to explain your code
- Have no idea what to do on exams
- Fall behind in harder classes that build on this material

**Use it as a tutor, not a ghostwriter.**

---

## Which Tool Should I Use?

Still not sure which to pick? Here's a simple decision tree:

```
Do you just want to get started fast?
  --> Claude Code (easiest to set up, best explanations)

Do you already pay for ChatGPT Plus?
  --> Codex CLI (uses your existing OpenAI account)

Do you want the most free usage?
  --> Gemini CLI (generous free tier with Google account)

Are you on a Chromebook or limited machine?
  --> Try Claude Code web app at claude.ai/code (runs in browser)
```

Honestly, they all do the same core thing. **Just pick one.** You're overthinking it.

---

## The One File That Changes Everything

Once you're comfortable with the basics, here's a power-up: **the instructions file.**

Each tool has a special file you can put in your project root that tells the AI about your project. Think of it as a cheat sheet you write once, and the AI reads it every time.

| Tool | File Name |
|---|---|
| Claude Code | `CLAUDE.md` |
| Codex CLI | `AGENTS.md` |
| Gemini CLI | `GEMINI.md` |

### Example CLAUDE.md (or equivalent)

Create a file called `CLAUDE.md` in the root of your project:

```markdown
# My CS 2340 Project

This is a Java Spring Boot application for our Objects & Design class.

## Rules
- We must use Java 17
- No external libraries beyond what's in build.gradle
- Follow the professor's naming conventions: camelCase for methods, PascalCase for classes
- All methods need Javadoc comments
- We use JUnit 5 for tests

## Project Structure
- src/main/java/com/app/ -- main source code
- src/test/java/com/app/ -- test files
- The entry point is Application.java

## How to Run
- ./gradlew bootRun
- Tests: ./gradlew test
```

Now every time you start the tool in this folder, it **already knows** all of this. You don't have to re-explain your project every conversation.

---

## Going Further

Once you're comfortable with the basics, here are your next steps:

### Learn the keyboard shortcuts
- `Escape` -- cancel what the AI is doing
- `Up Arrow` -- cycle through your past prompts
- `/help` -- see all available commands (in Claude Code)

### Try plan mode
Before building something complex, ask the AI to plan first:
```
Plan how you would build a full-stack task manager with 
React frontend and Node.js backend. Don't write code yet, 
just outline the approach.
```

Review the plan, give feedback, then let it build.

### Read other people's setups
- [Claude Code Best Practices](https://github.com/shanraisshan/claude-code-best-practice) -- the comprehensive deep-dive (advanced, but great once you're comfortable)
- [Anthropic's official docs](https://docs.anthropic.com/en/docs/claude-code) -- the source of truth

### Join the community
- [r/ClaudeAI](https://www.reddit.com/r/ClaudeAI/) -- Reddit community
- [r/ChatGPTCoding](https://www.reddit.com/r/ChatGPTCoding/) -- General AI coding discussion

---

## Contributing

If you're a student and something in this guide confused you, **open an issue.** That's how we make this better. If you figured something out that would help other beginners, **open a PR.**

---

## License

MIT -- use it, share it, remix it.

---

*Built for CS students, by someone who's been there. Stop copy-pasting. Start building.*
