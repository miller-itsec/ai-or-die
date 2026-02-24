# Engineering: AI-Assisted Development — Quiz Questions

> Engineering AI knowledge check — quiz questions for the engineering module.
> 6 modules, 31 questions total.

---

## Module 1: Why AI-Assisted Coding? (5 questions)

**Q1: What percentage of developers use AI coding tools at work (2025)?**
- A) 50%
- B) 75%
- C) 92% ✓
- D) 99%

**Q2: Which is NOT a level at which AI coding tools operate?**
- A) Tab Completion
- B) Agent Mode
- C) Automatic Deployment ✓
- D) Code Review

**Q3: A new engineer says "AI tools are just fancy autocomplete." Based on this module, what's the best counter-example?**
- A) AI can write documentation
- B) Agent mode autonomously edits multiple files to complete complex tasks ✓
- C) AI tools have nice syntax highlighting
- D) AI can run faster than human typing

**Q4: What is the recommended target for AI tool adoption across engineering?**
- A) 50%
- B) 75%
- C) 95% ✓
- D) 100%

**Q5: Your team lead asks why AI adoption matters at a security company. Which answer best reflects the module's argument?**
- A) AI tools are trendy and look good in job postings
- B) AI helps ship faster, catch security issues earlier, and maintain consistency ✓
- C) Engineers without AI tools will be fired
- D) AI tools eliminate the need for code review

---

## Module 2: Cursor vs Copilot — Tools Overview (5 questions)

**Q1: What is Cursor's flagship feature that sets it apart?**
- A) Ghost text suggestions
- B) Agent mode (multi-file editing) ✓
- C) JetBrains plugin
- D) GitHub integration

**Q2: Which tool has better JetBrains IDE support?**
- A) Cursor
- B) Copilot ✓
- C) Both are equal
- D) Neither supports JetBrains

**Q3: Can engineers use both Cursor and Copilot?**
- A) No, you must pick one
- B) Yes, both are approved ✓
- C) Only with manager approval
- D) Only for personal projects

**Q4: A teammate uses JetBrains IntelliJ exclusively and refuses to switch IDEs. Which tool should you recommend?**
- A) Cursor — it has better AI features overall
- B) Copilot — it has a native JetBrains plugin ✓
- C) Neither — JetBrains has built-in AI
- D) ChatGPT in the browser

**Q5: Where does Cursor get its deep codebase context from?**
- A) It reads your clipboard
- B) It indexes your full repository ✓
- C) It only uses the current open file
- D) It downloads context from GitHub

---

## Module 3: Cursor Deep Dive (5 questions)

**Q1: What keyboard shortcut opens Cursor's inline edit?**
- A) Cmd+L
- B) Cmd+K ✓
- C) Cmd+Shift+P
- D) Tab

**Q2: What is Agent Mode best used for?**
- A) Single-line fixes
- B) Complex multi-file tasks ✓
- C) Code formatting
- D) Git commits

**Q3: What context operator searches your entire project in Cursor chat?**
- A) @files
- B) @folders
- C) @codebase ✓
- D) @project

**Q4: A teammate's Agent Mode edit accidentally deleted test files. What is the most likely cause?**
- A) Agent Mode has a bug
- B) The prompt didn't specify to preserve existing tests ✓
- C) Cursor doesn't support test files
- D) The project was too small for Agent Mode

**Q5: You want to refactor a single function in-place without affecting other files. Which Cursor feature is most appropriate?**
- A) Agent Mode
- B) Cmd+K inline editing ✓
- C) @codebase chat
- D) Create a .cursorrules file

---

## Module 4: Copilot Deep Dive (5 questions)

**Q1: How do you accept a full Copilot ghost text suggestion?**
- A) Enter
- B) Tab ✓
- C) Ctrl+Enter
- D) Space

**Q2: What slash command generates tests in Copilot Chat?**
- A) /generate
- B) /tests ✓
- C) /test-gen
- D) /unittest

**Q3: What prefix gives Copilot full workspace context in chat?**
- A) @files
- B) @project
- C) @workspace ✓
- D) @codebase

**Q4: You write a comment "# Parse CSV rows into UserRecord objects" and Copilot suggests garbage. What's the most likely fix?**
- A) Switch to Cursor instead
- B) Make the comment more specific with types, edge cases, and expected behavior ✓
- C) Delete the comment and type the code manually
- D) Restart your IDE

**Q5: Which Copilot integration can auto-generate PR descriptions on GitHub?**
- A) Copilot in CLI
- B) Copilot in Pull Requests ✓
- C) Copilot in Docs
- D) Copilot Tab Completion

---

## Module 5: Advanced AI Patterns (6 questions)

**Q1: What is the highest-ROI use of AI mentioned in this module?**
- A) Code generation
- B) Documentation generation ✓
- C) Test generation
- D) Code review

**Q2: Where does Copilot's project instruction file go?**
- A) .cursorrules
- B) .copilot/config.yml
- C) .github/copilot-instructions.md ✓
- D) copilot.json

**Q3: You ask AI to generate tests and it produces tests that all pass trivially (e.g., assert True). What should you do?**
- A) Ship them — at least you have test coverage
- B) Review and rewrite tests that don't meaningfully test behavior ✓
- C) Stop using AI for test generation entirely
- D) Add more trivial tests to increase coverage numbers

**Q4: Given this .cursorrules snippet: "Never log sensitive data (API keys, passwords, PII)". Which prompt would violate this instruction?**
- A) "Log the request method and endpoint path"
- B) "Add logging for the user's auth token value for debugging" ✓
- C) "Add error logging with the exception type and message"
- D) "Log the response status code and timing"

**Q5: What advantage do custom instruction files (.cursorrules, copilot-instructions.md) have over verbal prompts?**
- A) They make AI faster
- B) They are version-controlled and apply to every AI interaction automatically ✓
- C) They bypass the AI's safety filters
- D) They only work for Python projects

---

## Module 6: Responsible AI Use (5 questions)

**Q1: Which of these is safe to paste into an AI coding tool?**
- A) API keys
- B) Customer emails
- C) Stack traces (scrubbed of secrets) ✓
- D) Partner proprietary algorithms

**Q2: What should you do if AI generates concerning output?**
- A) Ignore it
- B) Delete the file
- C) Flag it to your lead ✓
- D) Post it on Slack

**Q3: AI generates a login function that stores passwords in plain text. What's the right response?**
- A) Accept it — AI knows best practices
- B) Reject it and implement proper password hashing (bcrypt/argon2) ✓
- C) Add a comment saying "TODO: fix later"
- D) Use it in development but change it before production

**Q4: You need to debug a payment processing function. How should you share code with AI?**
- A) Paste the full function including real credit card numbers from logs
- B) Replace real data with masked/dummy values before sharing ✓
- C) Don't use AI for anything involving payments
- D) Only share the function name, nothing else

**Q5: Who is responsible for bugs in AI-generated code that makes it to production?**
- A) The AI tool vendor
- B) The engineer who accepted and committed the code ✓
- C) Nobody — it's an AI limitation
- D) The team lead who approved AI tool usage
