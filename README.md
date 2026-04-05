# Agentic Coding for Beginners

**You don't need to copy-paste from ChatGPT anymore.**

I know most of y'all are doing this right now:

1. Google the problem
2. Ask ChatGPT
3. Copy the code
4. Paste into VS Code
5. Pray it works
6. It doesn't. Back to step 2

I did the same thing freshman year. There are tools now that make this whole cycle obsolete and most CS students have no idea they exist. That's why I made this.

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

So you know how ChatGPT gives you code and you have to copy-paste it into your editor? These tools skip all of that. They run in your terminal, they can see every file in your project, and they edit your code directly.

Here's what they can do that ChatGPT can't:

- Read your entire project, not just whatever you pasted into a chat box
- Actually create and edit files on your machine
- Run your code, see the errors, and fix them without you doing anything
- Use the terminal -- install packages, run tests, commit to git, whatever
- Keep trying until something works instead of just giving you one answer

Easiest way to think about it:

| | ChatGPT | Agentic Coding Tool |
|---|---|---|
| Where it runs | Browser tab | Your terminal / VS Code |
| Knows your project? | Only what you paste | Reads all your files |
| Edits your code? | No, you copy-paste | Yes, directly |
| Runs your code? | No | Yes |
| Fixes its own mistakes? | Only if you paste the error | Sees the error and retries |

ChatGPT is like texting someone photos of your code and asking for help. These tools are like someone sitting next to you with access to your laptop.

---

## Why Should I Care?

Honestly? This changed how I build stuff. Here's what's different:

- **Things take way less time.** Not because the AI does your homework, but because you stop burning hours on syntax errors, environment issues, and dependency hell.
- **You actually learn more.** The AI is working in YOUR project, explaining YOUR code. Not some random example from the internet that doesn't match what you're building.
- **Debugging is completely different.** Instead of copying an error message into ChatGPT and hoping it understands your setup, the tool already sees everything. It reads the file, finds the bug, and explains what went wrong.
- **You pick up real dev tools by accident.** Git, terminal commands, testing, project structure -- you learn it just by watching the AI use it.

I'm not gonna pretend this is some magic thing that does everything for you. You still have to think. But the busy work goes away.

---

## The 3 Tools You Should Know About

There are three big ones right now. All of them are free to start with.

| Tool | Made By | Free Tier | Best For |
|---|---|---|---|
| **Claude Code** | Anthropic | Yes (with limits) | Best overall in my experience |
| **Codex CLI** | OpenAI | Yes (with limits) | If you already use ChatGPT/OpenAI |
| **Gemini CLI** | Google | Yes (with limits) | Generous free tier |

You don't need all three. Just pick one and try it. You can always switch later.

---

## Getting Started (Pick One)

### Claude Code

Anthropic's coding tool. This is the one I use the most.

**Install:**
```bash
npm install -g @anthropic-ai/claude-code
```

> If you don't have npm, you need Node.js first. Go to [nodejs.org](https://nodejs.org), grab the LTS version, install it, restart your terminal, then run the command above.

**Run it:**
```bash
cd your-project-folder
claude
```

First time it'll ask you to log in. After that you just type what you want.

You can also use it as a VS Code extension (search "Claude Code" in extensions), a desktop app, or at [claude.ai/code](https://claude.ai/code) in your browser.

---

### OpenAI Codex CLI

Same idea, made by OpenAI.

**Install:**
```bash
npm install -g @openai/codex
```

**Run it:**
```bash
cd your-project-folder
codex
```

You'll need an OpenAI account to log in.

---

### Gemini CLI

Google's version.

**Install:**
```bash
npm install -g @google/gemini-cli
```

> Double check [Google's repo](https://github.com/google-gemini/gemini-cli) for the latest install command, this might change.

**Run it:**
```bash
cd your-project-folder
gemini
```

Signs in with your Google account.

---

## Your First 15 Minutes

Alright you installed one. Here's what to do.

### 1. Open your terminal and go to a project folder

```bash
cd ~/my-project
```

If you don't have a project yet:

```bash
mkdir my-first-ai-project
cd my-first-ai-project
```

### 2. Start the tool

```bash
claude
```
(or `codex` or `gemini`, whichever one you installed)

### 3. Tell it to build something

Type something like:

```
Build me a simple to-do list app using HTML, CSS, and JavaScript. 
Make it look clean and modern. Save todos to localStorage so they 
persist when I refresh the page.
```

Now just watch. It's going to create the files, write all the code, and you'll have a working app. You can keep going from there -- "add a delete button", "make it dark mode", whatever.

### 4. Actually look at the code

Open the files it made. Read through them. This is where you learn. You'll start noticing patterns and structures you can reuse in your own stuff.

### 5. Ask it to break things down

```
Explain the JavaScript in this project. 
What does each function do? Keep it simple.
```

That's it. You just built something and you can explain how it works. Took maybe 10 minutes.

---

## How to Actually Talk to These Tools

How you ask for things matters a lot. Vague prompts get vague results.

### Be specific

```
Vague:   "make a website"
Better:  "Create a personal portfolio website with an about section, 
          a projects section with 3 cards, and a contact form. 
          Use HTML, CSS, and vanilla JavaScript."
```

### Tell it what's going on

```
Vague:   "fix my code"
Better:  "The login form in index.html isn't submitting. When I click 
          the submit button nothing happens. Can you check the event 
          listener in script.js?"
```

### Don't just ask it to fix things, ask it to explain

```
"Fix the bug and explain what was wrong so I don't make the same mistake"
```

### Tell it your level

```
"I'm learning React for the first time. I know HTML and basic 
 JavaScript but I've never used components before."
```

This actually changes how it explains things to you. Worth doing.

### Build on what's there

You don't have to start over every time something isn't right:

```
"That's close but make the navbar sticky and switch the colors to blue/white"
```

It remembers the whole conversation so use that.

---

## Real Student Examples

Some actual things you can try:

### Stuck on a data structures assignment

```
I need to implement a binary search tree in Java. 
I already have the TreeNode class. I need insert, 
search, and delete methods. Help me write them and 
walk me through the logic.
```

### No idea how to set up a project

```
I need to create a React app for my web dev class. 
Set up the project, create a basic file structure, 
and add a homepage component. I've never used React before.
```

### Can't find a bug

```
My Python script reads a CSV and calculates the average 
of the "grades" column but it keeps throwing a TypeError. 
Look at my code and tell me what's wrong.
```

It's going to read your actual files, find the problem, fix it, and tell you what happened. No more copying error messages back and forth.

### Never used git

```
I've never used git. Initialize a repo for this project, 
walk me through the basics, and help me make my first commit.
```

---

## Mistakes Every Beginner Makes

### 1. Not reading the code

The tool writes code fast. That doesn't mean you should just accept it and move on. If you can't explain what it wrote, you're going to get destroyed on exams and code reviews. Always read it. If something doesn't make sense, ask.

### 2. Blindly trusting the output

AI gets things wrong. It might use a library your professor doesn't allow, over-engineer a simple assignment, or write something that works but breaks your project's requirements. Check it against what you actually need to turn in.

### 3. Being in the wrong folder

This one gets people all the time. The tool can only see files in whatever directory your terminal is in. If you're sitting in your home folder wondering why it can't find your code:

```bash
cd ~/my-project
claude
```

Always cd into your project first.

### 4. Vague prompts

"Make a website" vs "Build a recipe website with a search bar, recipe cards with images, and a favorites feature" -- these are going to give you completely different results. Put in a little effort on the prompt and the output gets way better.

### 5. Using it as a ghostwriter instead of a tutor

Look, I get it. It's tempting to just generate everything and turn it in. But then you:
- Can't explain your code when the professor asks
- Bomb the exam because you never learned the material
- Fall behind in every class that builds on this one

Use it to learn faster, not to skip learning. There's a big difference.

---

## Which Tool Should I Use?

If you're still going back and forth:

```
Just want to start? ..... Claude Code
Already pay for ChatGPT? ..... Codex CLI
Want the most free usage? ..... Gemini CLI
On a Chromebook? ..... claude.ai/code (browser)
```

They all do basically the same thing. Seriously just pick one. You're not signing a contract.

---

## The One File That Changes Everything

Once you've been using this for a bit, here's something that makes it way better.

Each tool has a special file you can drop in your project folder. It's basically a note to the AI that says "here's what this project is, here's the rules, here's how to run it." The AI reads it automatically every time you start a session.

| Tool | File Name |
|---|---|
| Claude Code | `CLAUDE.md` |
| Codex CLI | `AGENTS.md` |
| Gemini CLI | `GEMINI.md` |

Here's an example. Say you're in a Java class -- create a file called `CLAUDE.md` in your project root:

```markdown
# CS 2340 Project

Java Spring Boot app for Objects & Design.

## Rules
- Java 17 only
- No external libraries beyond what's in build.gradle
- camelCase for methods, PascalCase for classes
- All methods need Javadoc comments
- JUnit 5 for tests

## Project Structure
- src/main/java/com/app/ -- source code
- src/test/java/com/app/ -- tests
- Entry point is Application.java

## How to Run
- ./gradlew bootRun
- Tests: ./gradlew test
```

Now you never have to explain any of that again. Every conversation starts with the AI already knowing your setup, your rules, and your constraints. It's a small thing that saves a ton of time.

Check the [example-claude-md](./example-claude-md/) folder for more examples.

---

## Going Further

Once you're comfortable:

**Keyboard shortcuts** -- `Escape` stops the AI mid-response, `Up Arrow` cycles through previous prompts, `/help` shows all commands.

**Plan before you build** -- for bigger projects, ask the AI to plan first before writing any code. Review the plan, give it feedback, then let it go. Way better results than just saying "build me X."

**Go deeper:**
- [Claude Code Best Practices](https://github.com/shanraisshan/claude-code-best-practice) -- a massive deep-dive into advanced usage. Great resource once you're past the basics.
- [Anthropic's official docs](https://docs.anthropic.com/en/docs/claude-code)

**Communities:**
- [r/ClaudeAI](https://www.reddit.com/r/ClaudeAI/)
- [r/ChatGPTCoding](https://www.reddit.com/r/ChatGPTCoding/)

---

## Contributing

If something in here confused you, open an issue. If you figured out something that would help other beginners, open a PR. That's how this gets better.

---

MIT License. Use it, share it, whatever.
