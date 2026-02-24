# Engineering: AI-Assisted Development

> **Module 0** | Estimated reading time: 30 minutes | Last updated: February 2026

---

## Section 1: Why AI-Assisted Coding?

### The State of AI Coding in 2026

AI coding tools have moved from novelty to necessity. Here's what the data shows:

- **92% of developers** now use AI coding tools at work (GitHub survey, 2025)
- Engineers using AI tools report **55% faster task completion**
- Code quality metrics (bugs per KLOC) have **improved by 30%** with AI assistance
- Companies without AI adoption are losing talent to those that have it

**Across the industry**, the impact is already clear. Engineers using AI tools are generating thousands of lines of production code with AI assistance every month.

### What AI Coding Tools Actually Do

AI coding tools operate at multiple levels:

1. **Tab Completion** — Real-time line/block suggestions as you type
2. **Chat / Inline Edit** — Ask questions, request changes in natural language
3. **Agent Mode** — AI autonomously edits multiple files to complete a task
4. **Code Review** — AI reviews your code for bugs, security issues, and style

These aren't just autocomplete on steroids. Modern AI tools understand your full codebase context, your project's conventions, and can reason about complex multi-file changes.

### Why Your Team Should Care

Modern engineering teams build complex, security-critical software. AI tools help you:

- **Ship faster** without sacrificing quality
- **Catch security issues** before they reach production
- **Maintain consistency** across large codebases
- **Onboard new engineers** faster with AI-assisted code exploration

The goal: **95% AI tool adoption** across your engineering teams.

### What AI Cannot Do

AI is a powerful tool, but it has clear limitations that engineers must understand:

- **Understand your business domain** — AI doesn't know why you made certain architectural decisions, or the regulatory constraints you operate under
- **Replace code review** — AI catches mechanical issues, but human reviewers understand context, maintainability, and team conventions at a deeper level
- **Guarantee correctness** — AI generates plausible code that may have subtle logic errors, security holes, or use deprecated APIs
- **Handle novel problems** — If the problem has no analogues in training data, AI struggles. Cutting-edge algorithms, proprietary protocols, and bespoke architectures require human engineering
- **Own accountability** — You are responsible for every line of code you commit, whether you wrote it or AI generated it

> **Key principle:** AI produces drafts, not production code. Every AI output is a starting point for your review, not a replacement for your judgment.

---

## Section 2: Cursor vs Copilot — Tools Overview

### At a Glance

Both **Cursor** and **GitHub Copilot** are production-ready AI coding tools, but they have different strengths:

| | **Cursor** | **Copilot** |
|---|---|---|
| **Type** | Full IDE (VS Code fork) | Extension for existing IDEs |
| **Best at** | Multi-file edits, agent mode | Inline suggestions, ecosystem integration |
| **IDE support** | Cursor only | VS Code, JetBrains, Vim, Visual Studio |
| **Context** | Deep — indexes full repo | Good — workspace-aware |
| **Learning curve** | Moderate | Easy |
| **Enterprise** | SOC 2 compliant | GitHub Enterprise integration |

### When to Use Cursor

Cursor shines when you need:

- **Agent Mode** — The flagship feature. AI autonomously creates, edits, and deletes files across your entire project. Perfect for new features, large refactors, migrations.
- **Deep codebase context** — Cursor indexes your full repository and uses it for every suggestion. Ask "how does auth work in this project?" and it knows.
- **Cmd+K inline editing** — Select code, describe the change, done. Surgical refactoring.
- **.cursorrules** — Version-controlled project instructions that every AI interaction follows.

**Ideal for**: Large codebases, multi-file features, complex refactoring, C/C++/Rust projects.

### When to Use Copilot

Copilot shines when you need:

- **IDE flexibility** — Works natively in VS Code, JetBrains, Vim, Visual Studio. You don't have to switch editors.
- **Flow state coding** — Ghost text suggestions appear as you type with minimal disruption. Accept with Tab, ignore by typing. Zero friction.
- **GitHub ecosystem** — Copilot in pull requests, Copilot in CLI, Copilot in docs. Deep integration with your existing GitHub workflow.
- **Enterprise compliance** — GitHub Enterprise manages licensing, data policies, and code suggestions at organizational level.

**Ideal for**: JetBrains users, teams on GitHub Enterprise, beginners, inline-completion-heavy workflows.

### Feature Comparison

| Feature | Cursor | Copilot |
|---------|--------|---------|
| **Tab completion** | Fast, context-aware | Industry standard |
| **Agent mode** | Excellent — flagship feature | Workspace agent (newer) |
| **Inline edit** | Cmd+K for targeted edits | Comment-driven + ghost text |
| **Chat** | Cmd+L with @files/@codebase | Ctrl+Shift+I with @workspace |
| **Custom instructions** | `.cursorrules` in project root | `.github/copilot-instructions.md` |
| **Multi-file editing** | Native — Agent creates/edits/deletes | Growing capability |
| **JetBrains support** | Limited | Excellent — native plugin |
| **VS Code support** | Native (it IS VS Code) | Excellent — native extension |
| **Code review** | Via chat | Copilot in PRs |
| **CLI integration** | Terminal in IDE | `gh copilot` CLI tool |

### Frequently Asked Questions

**Q: Can I use both?**
Yes! Many engineers use Cursor for complex tasks and Copilot in JetBrains for daily coding. They don't conflict — use the best tool for each situation.

**Q: Which is better for my language?**
Both support all major languages. Cursor has an edge for systems languages (C/C++, Rust) due to deeper codebase indexing. Copilot has broader training data for web languages.

**Q: Is my code safe?**
Both Cursor and Copilot Enterprise don't use your code for training. Check with your lead if using the free/personal tier.

**Q: I'm a JetBrains user. Do I need Cursor?**
You can be very productive with just Copilot in JetBrains. However, Cursor's agent mode is currently unmatched. Consider Cursor for complex tasks and JetBrains for daily work.

**Q: What about Claude Code, Windsurf, Codeium, etc.?**
The recommended tools are Cursor and GitHub Copilot. Other tools may be evaluated later. Browser-based AI (ChatGPT, Claude) is fine for general questions but avoid pasting proprietary code.

---

## Section 3: Cursor Deep Dive

### Tab Completion Mastery

Cursor's tab completion is its bread and butter:

- **How it works**: As you type, Cursor predicts the next line(s) and shows them in gray
- **Accept**: Press `Tab` to accept the suggestion
- **Partial accept**: Press `Ctrl+Right` to accept word by word
- **Reject**: Keep typing or press `Escape`

**Pro tip**: Write a comment describing what you want, then let Tab do the work. The more context Cursor has (open files, recent edits), the better the suggestions.

### Cmd+K — Inline Editing

Select code and press `Cmd+K` (or `Ctrl+K`) to edit it with natural language:

- "Refactor this to use async/await"
- "Add error handling for the API call"
- "Convert this class to a dataclass"

Cmd+K is surgical — it modifies exactly what you selected. Perfect for targeted refactors.

**Before/After — Cmd+K: "Convert this class to a dataclass"**

*Before:*
```python
class UserConfig:
    def __init__(self, name, email, role="user", active=True):
        self.name = name
        self.email = email
        self.role = role
        self.active = active

    def __repr__(self):
        return f"UserConfig({self.name}, {self.email})"
```

*After (Cursor generates):*
```python
from dataclasses import dataclass

@dataclass
class UserConfig:
    name: str
    email: str
    role: str = "user"
    active: bool = True
```

**Pro tip**: Select MORE context than you need. Include surrounding code so Cursor understands the broader context, even if you only want to change a few lines.

### Chat Panel (Cmd+L)

The chat panel (`Cmd+L`) gives you a conversational AI assistant:

- Ask questions about your codebase
- Generate new code from descriptions
- Debug errors by pasting stack traces
- Plan implementation approaches

**Context operators** — the key to great chat responses:
- `@files` — Reference specific files
- `@folders` — Reference entire directories
- `@codebase` — Search your entire project
- `@docs` — Reference documentation
- `@web` — Search the internet

### Agent Mode — The Power Feature

Agent mode is Cursor's most powerful feature:

- The AI autonomously edits **multiple files** to complete a task
- It can create new files, modify existing ones, and run terminal commands
- Think of it as a junior developer that follows your instructions

**When to use Agent**: Complex tasks that span multiple files — new features, refactors, test generation, migrations.

**When NOT to use Agent**: Simple single-line fixes (Tab or Cmd+K is faster).

**Tips for Agent mode**:
1. Be specific about what you want (vague = bad results)
2. Mention files that should be modified
3. Reference existing patterns: "Follow the pattern in auth.py"
4. Set constraints: "Don't modify the database schema"

**Before/After — Agent Mode Refactor**

*Prompt:* "Refactor this monolithic api.py into separate modules. Split route handlers into routes/, database queries into db/repository.py, and utility functions into utils/. Update all imports. Don't break existing tests."

*Before (single file):*
```
api.py          (500 lines — routes, DB queries, helpers all mixed)
tests/test_api.py
```

*After (Agent creates):*
```
routes/
  __init__.py
  users.py      (user route handlers)
  auth.py       (auth route handlers)
db/
  repository.py (all database queries)
utils/
  helpers.py    (utility functions)
app.py          (FastAPI app setup, imports routes)
tests/test_api.py  (imports updated automatically)
```

### .cursorrules — Your Team's AI Config

Create a `.cursorrules` file in your project root to give Cursor persistent instructions:

```
You are working on a security-critical backend service.
- Always use type hints in Python
- Follow our error handling pattern: wrap external calls in try/except
- Use pytest for testing, not unittest
- Never log sensitive data (API keys, passwords, PII)
- Database queries go through the repository pattern in db/
- All API responses use our standard Response model
```

This file is version-controlled — the whole team benefits from one engineer's setup. Review and update it regularly as your project evolves.

**Before/After — .cursorrules Effect**

*Without .cursorrules* — prompt: "Add a user creation endpoint"
```python
def create_user(data):
    user = db.execute("INSERT INTO users VALUES (?)", data["name"])
    print(f"Created user: {data}")  # Logs PII!
    return {"status": "ok"}
```

*With .cursorrules* — same prompt, Cursor follows project rules:
```python
def create_user(data: CreateUserRequest) -> Response[User]:
    try:
        user = user_repository.create(data)
        logger.info("User created", extra={"user_id": user.id})
        return Response(data=user, status="ok")
    except DatabaseError as e:
        logger.error("User creation failed", extra={"error": str(e)})
        raise HTTPException(status_code=500, detail="Creation failed")
```

---

## Section 4: Copilot Deep Dive

### Ghost Text Mastery

Copilot's signature feature — inline ghost text that appears as you code:

- **Accept full suggestion**: Press `Tab`
- **Accept word**: Press `Ctrl+Right Arrow`
- **Dismiss**: Press `Escape` or keep typing
- **Cycle alternatives**: Press `Alt+]` for next, `Alt+[` for previous

**Pro tip**: Copilot learns from your file's context. Open related files in tabs so Copilot can reference them for better suggestions.

**Advanced**: If you don't like the suggestion, don't dismiss — keep typing a few characters to steer Copilot. It adapts in real-time.

### Copilot Chat — Beyond Ghost Text

Open Copilot Chat for conversational AI assistance:

- **VS Code**: Click the chat icon or `Ctrl+Shift+I`
- **JetBrains**: Tool window or `Alt+C`

**Slash commands for speed**:
- `/fix` — Fix the selected code
- `/explain` — Explain what the code does
- `/tests` — Generate tests for the selection
- `/doc` — Add documentation

**Context operators**:
- `@workspace` — Full project context
- `@terminal` — Include terminal output
- `#file` — Reference a specific file

### Comment-Driven Development

Write descriptive comments and let Copilot generate the implementation:

```python
# Function that validates an email address using regex
# Returns True if valid, False otherwise
# Handles edge cases: empty string, missing @, multiple dots
def validate_email(email: str) -> bool:
    # Copilot generates the implementation here
```

This works especially well for:
- Utility functions with clear inputs/outputs
- Data transformations
- API endpoint handlers
- Test cases

**Before/After — Comment Specificity**

*Vague comment (poor output):*
```python
# Process data
def process(data):
    # Copilot: returns data  (useless)
```

*Specific comment (great output):*
```python
# Parse CSV rows into UserRecord objects
# Skip rows with missing email or invalid date format (YYYY-MM-DD)
# Return list of valid UserRecords and count of skipped rows
def parse_user_csv(rows: list[dict]) -> tuple[list[UserRecord], int]:
    # Copilot generates a complete, correct implementation
```

**Pro tip**: The more specific your comments, the better the output. "Process data" gives garbage. "Parse CSV rows into UserRecord objects, skip malformed rows" gives gold.

### Copilot in Your Workflow

Beyond the editor, Copilot integrates with your full workflow:

**Copilot in Pull Requests** (GitHub):
- Auto-generates PR descriptions
- Reviews code changes
- Suggests improvements in PR comments

**Copilot in CLI**:
```bash
gh copilot suggest "find all Python files modified in the last week"
gh copilot explain "git log --oneline --graph --all"
```

**Copilot in Docs**:
- Generates documentation from code
- Translates between languages
- Creates API reference docs

**Before/After — /tests Command**

*Select a function and type `/tests` in Copilot Chat:*

*Before (your code):*
```python
def calculate_discount(price: float, tier: str) -> float:
    rates = {"gold": 0.20, "silver": 0.10, "bronze": 0.05}
    return price * rates.get(tier, 0)
```

*After (Copilot generates):*
```python
def test_gold_discount():
    assert calculate_discount(100.0, "gold") == 20.0

def test_silver_discount():
    assert calculate_discount(100.0, "silver") == 10.0

def test_unknown_tier_no_discount():
    assert calculate_discount(100.0, "unknown") == 0.0

def test_zero_price():
    assert calculate_discount(0.0, "gold") == 0.0
```

Use these integrations to multiply your productivity beyond just code writing.

---

## Section 5: Advanced AI Patterns

### AI-Assisted Code Review

Use AI to review code before submitting PRs:

1. **Paste your diff** into chat: "Review this change for bugs and security issues"
2. **Ask for edge cases**: "What edge cases might this function miss?"
3. **Security scan**: "Are there any security vulnerabilities in this code?"

**Example prompt for a thorough review:**
```
Review this PR diff for:
1. Security vulnerabilities (injection, auth bypass, data exposure)
2. Logic errors and edge cases
3. Performance concerns

For each finding, provide:
- Severity: CRITICAL / HIGH / MEDIUM / LOW
- Location: file and line number
- Issue: what's wrong
- Suggestion: how to fix it
```

**Sample AI review output:**
```
Finding 1 — HIGH — auth/login.py:42
  Issue: Password comparison uses == instead of constant-time compare.
  Suggestion: Use hmac.compare_digest() to prevent timing attacks.

Finding 2 — MEDIUM — api/users.py:87
  Issue: User input interpolated directly into SQL query.
  Suggestion: Use parameterized queries: cursor.execute("SELECT * FROM users WHERE id = ?", (user_id,))

Finding 3 — LOW — utils/cache.py:15
  Issue: Cache TTL hardcoded to 3600s. No invalidation on data change.
  Suggestion: Add cache invalidation in the update/delete handlers.
```

AI won't replace human review, but it catches mechanical issues so reviewers can focus on architecture and design.

### Test Generation

AI excels at generating test scaffolding:

- **Unit tests**: "Write pytest tests for this function covering happy path and edge cases"
- **Integration tests**: "Generate API test for this endpoint using requests"
- **Property-based**: "Write hypothesis tests for this data validation function"

**Full example — source function to prompt to tests:**

*Source:*
```python
def parse_duration(text: str) -> int:
    """Parse '3h', '45m', '2d' into total seconds. Raises ValueError on bad input."""
    units = {"s": 1, "m": 60, "h": 3600, "d": 86400}
    if not text or text[-1] not in units:
        raise ValueError(f"Invalid duration: {text}")
    return int(text[:-1]) * units[text[-1]]
```

*Prompt:* "Write pytest tests for parse_duration. Cover happy path for each unit, edge cases (empty string, no number, unknown unit, zero, negative), and parametrize where possible."

*AI generates:*
```python
import pytest
from utils import parse_duration

@pytest.mark.parametrize("text,expected", [
    ("30s", 30), ("5m", 300), ("2h", 7200), ("1d", 86400),
])
def test_valid_durations(text, expected):
    assert parse_duration(text) == expected

@pytest.mark.parametrize("bad_input", ["", "abc", "3x", "h", None])
def test_invalid_input_raises(bad_input):
    with pytest.raises((ValueError, TypeError)):
        parse_duration(bad_input)

def test_zero_duration():
    assert parse_duration("0s") == 0
```

**Important**: Always review generated tests. AI may miss important edge cases or write tests that pass trivially.

### Documentation Generation

Let AI help with documentation:

- **Docstrings**: Select a function, ask "Add a comprehensive docstring"
- **README sections**: "Generate API documentation for these endpoints"
- **Architecture docs**: "Explain the data flow in this module"

**Full example — undocumented function to rich docstring:**

*Before:*
```python
def retry(fn, max_attempts=3, delay=1.0, backoff=2.0, exceptions=(Exception,)):
    for attempt in range(max_attempts):
        try:
            return fn()
        except exceptions as e:
            if attempt == max_attempts - 1:
                raise
            time.sleep(delay * (backoff ** attempt))
```

*Prompt:* "Add a comprehensive docstring with Args, Returns, Raises, and a usage example."

*After:*
```python
def retry(fn, max_attempts=3, delay=1.0, backoff=2.0, exceptions=(Exception,)):
    """Execute a function with exponential backoff retry logic.

    Args:
        fn: Callable to execute. Must take no arguments.
        max_attempts: Maximum number of attempts before giving up.
        delay: Initial delay in seconds between retries.
        backoff: Multiplier applied to delay after each retry.
        exceptions: Tuple of exception types that trigger a retry.

    Returns:
        The return value of fn() on success.

    Raises:
        The last exception raised by fn() if all attempts fail.

    Example:
        >>> result = retry(lambda: requests.get(url), max_attempts=5, delay=0.5)
    """
```

This is one of the highest-ROI uses of AI — engineers hate writing docs, and AI does it well.

### Custom Instructions Files

Both tools support project-level instruction files:

**Cursor**: `.cursorrules` in project root — a complete example:
```
You are working on a cloud security scanning service.
Tech stack: Python 3.12, FastAPI, PostgreSQL, Redis, pytest.

Code standards:
- Always use type hints for function signatures
- Follow Google Python Style Guide for docstrings
- All API endpoints return our standard ApiResponse[T] model
- Database access goes through repository classes in db/repos/
- Use dependency injection via FastAPI Depends()
- Never log PII, secrets, or raw request bodies
- Error handling: wrap external calls in try/except, use custom exceptions
- All new endpoints need corresponding tests in tests/api/
- Use UTC timestamps everywhere (datetime.now(timezone.utc))
- Prefer list comprehensions over map/filter for readability

Testing:
- Use pytest with fixtures, not unittest
- Mock external services with pytest-mock
- Integration tests use the test database (see conftest.py)
```

**Copilot**: `.github/copilot-instructions.md` — matching example:
```markdown
## Cloud Security Service — Copilot Instructions

### Tech Stack
- Python 3.12, FastAPI, PostgreSQL, Redis

### Code Standards
- Type hints required on all function signatures
- Google-style docstrings for public functions
- API responses use `ApiResponse[T]` model
- Database queries through repository pattern (`db/repos/`)
- Never log PII, secrets, or raw request bodies

### Testing
- pytest with fixtures (see conftest.py for examples)
- All new endpoints need tests in tests/api/
```

These files are version-controlled, so the whole team benefits.

### Real Workflow: Feature Implementation End-to-End

Here's how an experienced AI-assisted engineer implements a complete feature — from ticket to PR.

**The ticket**: *"Add rate limiting to the /api/scan endpoint. Limit to 100 requests per minute per API key. Return 429 when exceeded."*

**Step 1: Plan with AI**
```
Prompt (Chat): "I need to add rate limiting to a FastAPI endpoint.
The limit is 100 req/min per API key. What's the best approach?
Consider: Redis vs in-memory, middleware vs decorator, 429 response format.
We use FastAPI + Redis already (see @requirements.txt)."
```
AI suggests: Redis sliding window, decorator pattern, standard RFC 429 response with `Retry-After` header.

**Step 2: Implement with Agent/Chat**
```
Prompt (Agent Mode): "Implement rate limiting as planned:
1. Create rate_limiter.py with a Redis sliding window implementation
2. Add a @rate_limit(max_requests=100, window=60) decorator
3. Apply it to the scan endpoint in routes/scan.py
4. Return 429 with Retry-After header when exceeded
5. Add rate limit headers (X-RateLimit-Remaining) to all responses
Follow the patterns in our existing middleware/ directory."
```
Agent creates 2 new files, modifies 1 existing file.

**Step 3: Review + test generation**
```
Prompt: "Review the rate limiter implementation for:
1. Race conditions in the Redis sliding window
2. What happens when Redis is unavailable
3. Edge cases around window boundaries

Then generate pytest tests covering:
- Normal requests under limit
- Requests at and over limit
- Window expiry and reset
- Redis connection failure fallback"
```

**Step 4: Generate PR description**
```
Prompt: "Generate a PR description for these changes.
Include: summary, what changed, how to test, rollback plan."
```

**Key takeaway**: AI handles the mechanical work (boilerplate, tests, docs), while you focus on the decisions (architecture, edge cases, security implications).

---

## Section 6: Responsible AI Use

### What NOT to Feed AI

**Never paste into AI tools:**
- API keys, passwords, tokens, or secrets
- Customer PII (names, emails, financial data)
- Proprietary algorithms or trade secrets from partners
- Internal security vulnerability details

**Safe to use:**
- Your own production code (both Cursor and Copilot have enterprise data policies)
- Open-source code references
- General architecture questions
- Error messages and stack traces (scrub sensitive data first)

### Always Review AI Output

AI generates plausible-looking code that may be:

- **Subtly wrong**: Logic errors that pass basic tests
- **Insecure**: SQL injection, XSS, improper auth checks
- **Outdated**: Using deprecated APIs or patterns
- **Hallucinated**: Referencing functions/libraries that don't exist

**The rule**: You own every line AI generates. Review it with the same rigor as if a junior engineer wrote it.

### AI Policy Best Practices

Key guidelines:

1. **Use approved tools** — Cursor and GitHub Copilot are approved for all projects
2. **No secrets in prompts** — Use environment variables, never hardcode
3. **Review before commit** — AI-generated code must pass the same review process
4. **Report issues** — If AI generates concerning output, flag it to your lead
5. **Stay updated** — AI tools evolve rapidly; keep your extensions current

The goal is maximum productivity with responsible guardrails.

---

## Section 7: Prompt Lab Challenges

### Challenge 1: Onboard a Teammate

**Scenario:** A new engineer joins your team tomorrow. They've never seen your codebase. Write a prompt for an AI assistant that will generate a useful codebase overview for them.

**Scoring criteria:**
- **Specificity** (2 pts) — Mention specific technologies, frameworks, or project areas
- **Context** (2 pts) — Explain who the output is for and what they need to understand
- **Output Format** (2 pts) — Request a specific format (list, diagram, sections)
- **Depth** (2 pts) — Write a detailed prompt (20+ words)

### Challenge 2: Universal Prompt

**Scenario:** Write a single prompt that would work well in BOTH Cursor and Copilot to generate a complete utility function. The function should validate and sanitize user input for a web form.

**Scoring criteria:**
- **Function spec** (2 pts) — Clearly specify function name, parameters, and return type
- **Input/Output** (2 pts) — Define what the function accepts and returns
- **Edge cases** (2 pts) — Mention validation rules or error handling
- **Cross-tool compatibility** (2 pts) — Write in a way that works for both tools

### Challenge 3: Agent Mode Refactor

**Scenario:** You have a legacy Python module (`analytics.py`, ~400 lines) that mixes data fetching, transformation, and visualization. Write an Agent Mode prompt to refactor it into clean, separated modules.

**Scoring criteria:**
- **Task clarity** (2 pts) — Clearly describe the refactoring goal
- **Code preservation** (2 pts) — Mention preserving tests, existing behavior, or imports
- **Structure** (2 pts) — Specify the target file/module structure
- **Constraints** (2 pts) — Set boundaries on what should and shouldn't change

### Challenge 4: Comment-Driven Development

**Scenario:** Write detailed Python comments that would guide Copilot to generate a complete class for managing user sessions — including creation, validation, and expiration.

**Scoring criteria:**
- **Class definition** (2 pts) — Define the class and its purpose
- **Parameters** (2 pts) — Specify attributes with types
- **Methods** (2 pts) — Describe at least 3 methods with behavior
- **Edge cases** (2 pts) — Mention expiration, validation, or error handling

### Challenge 5: Security Code Review

**Scenario:** Write a prompt asking AI to perform a security-focused code review of a payment processing module. The prompt should guide the AI to catch real vulnerabilities.

**Scoring criteria:**
- **Security focus** (2 pts) — Mention specific vulnerability types to check
- **Review scope** (2 pts) — Define what files/functions to review
- **Severity levels** (2 pts) — Ask for categorized findings
- **Edge cases** (2 pts) — Mention data handling, auth, or injection vectors

### Challenge 6: Safe Data Handling

**Scenario:** You need to debug a function that processes sensitive customer data. Write a prompt that gets useful AI debugging help WITHOUT exposing real customer information.

**Scoring criteria:**
- **PII/data safety** (2 pts) — Demonstrate masking or replacing real data
- **Bug description** (2 pts) — Clearly describe the problem
- **Code context** (2 pts) — Provide enough code for the AI to help
- **Responsible use** (2 pts) — Show awareness of data sensitivity

---

## Quiz: Engineering Module (31 Questions)

See [00-engineering-quiz.md](00-engineering-quiz.md) for the complete quiz with answer key.
