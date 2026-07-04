# AGENTS.md

`AGENTS.md` is the file that turns Codex from a one-off assistant into a more consistent working partner.

Without it, every new Codex session starts with limited knowledge of how you want work done. You have to repeat your preferences, your quality bar, your communication style, your review expectations, and your security concerns over and over. That creates inconsistent results.

`AGENTS.md` solves that problem by giving Codex durable instructions it can apply whenever it works in the repository.

## The Problem It Solves

The core problem is repeated context.

Most bad or mediocre AI-assisted work does not happen because the model cannot write text or code. It happens because the assistant is missing stable expectations:

- What role should it play?
- How direct should it be?
- What does a good answer look like?
- What risks should it consider?
- What should it avoid?
- What does "done" mean?
- How should it communicate with engineers versus leaders?
- When should it ask questions, and when should it make reasonable assumptions?

If those expectations only live in your head, Codex has to infer them from every prompt. That leads to uneven output.

An `AGENTS.md` file makes those expectations explicit.

## Why This Matters

For simple questions, a prompt may be enough.

For serious work, especially security architecture, code review, engineering design, risk analysis, and executive communication, the assistant needs a stable operating model.

`AGENTS.md` helps with that by defining:

- The assistant's role
- The type of work it should optimize for
- The expected quality bar
- The preferred communication style
- The user's professional context
- The level of rigor required for security topics
- The behavior expected during coding tasks
- The way assumptions, risks, and recommendations should be handled

This reduces the gap between what you meant and what the assistant produces.

## What Good AGENTS.md Guidance Prevents

A strong `AGENTS.md` helps prevent common failure modes:

- Generic answers that do not fit the audience
- Security advice that sounds correct but lacks practical mitigation
- Unsupported severity claims
- Overly soft or vague communication
- Excessive clarification questions
- Code changes that ignore local patterns
- Reviews that miss correctness, security, or test coverage concerns
- Executive summaries that bury the decision or business impact

The file does not guarantee perfect output, but it gives Codex a better default posture.

## What This Repository's AGENTS.md Is Designed To Do

The [AGENTS.md](../AGENTS.md) file in this repository is written for a user who uses Codex as both:

- A coding assistant
- A regular AI assistant for security architecture, writing, analysis, planning, and communication

It is optimized for someone who communicates with:

- Engineers
- Managers
- Directors
- VPs

The file pushes Codex to produce work that is:

- Direct
- Practical
- Audience-aware
- Security-conscious
- Technically defensible
- Clear enough for workplace use
- Strong enough to compare against other advanced AI models

## What The File Tells Codex

The root [AGENTS.md](../AGENTS.md) tells Codex to:

- Adopt the right role for the task
- Match the answer to the likely audience
- Be direct, clear, and defensible
- Improve weak framing instead of blindly answering
- Handle security topics with rigor
- Distinguish facts, assumptions, risks, mitigations, and residual risk
- Treat coding tasks like a senior engineer
- Preserve user changes
- Keep changes scoped
- Verify work when practical
- Produce polished communication for engineers and leaders

That guidance matters because it changes the default behavior before the task even starts.

## When AGENTS.md Is Most Useful

`AGENTS.md` is most useful when you repeatedly ask Codex to do similar kinds of work.

Examples:

- Reviewing designs
- Drafting security recommendations
- Writing executive updates
- Reviewing code
- Debugging issues
- Explaining architecture decisions
- Preparing risk summaries
- Creating reusable prompts or playbooks

Instead of restating your expectations each time, you encode the durable parts once.

## How To Think About Maintaining It

Treat `AGENTS.md` as a living operating guide.

When Codex gives a weak answer, ask what expectation was missing. Then add that guidance to the file.

Good reasons to update it:

- Codex is too verbose.
- Codex is too generic.
- Codex misses security tradeoffs.
- Codex asks unnecessary questions.
- Codex does not distinguish risk from impact.
- Codex gives advice that would not survive engineering review.
- Codex writes for the wrong audience.

Do not add every preference immediately. Add guidance when the same issue repeats.

## Practical Rule

Use `AGENTS.md` for durable expectations.

Use the chat prompt for task-specific instructions.

That separation keeps the file useful:

- `AGENTS.md` defines how Codex should generally work.
- The current prompt defines what Codex should do right now.

The best `AGENTS.md` files are specific enough to shape behavior, but not so long that they become noise.
