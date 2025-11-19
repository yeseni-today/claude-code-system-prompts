# Claude Code System Prompts

This repository contains an up-to-date list of all Claude Code's various system prompts and their associated token counts as of **[Claude Code v2.0.43](https://www.npmjs.com/package/@anthropic-ai/claude-code/v/2.0.43) (November 17th, 2025).**

Why multiple "system prompts?"

**Claude Code doesn't just have one single string for its system prompt.**

Instead, there are:
- Large portions conditionally added depending on the environment and various configs.
- Descriptions for builtin tools like `Write`, `Bash`, and `TodoWrite`, and some are fairly large.
- Separate system prompts for builtin agents like Explore and Plan.
- Numerous AI-powered utility functions, such as conversation compaction, `CLAUDE.md` generation, session title generation, etc. featuring their own systems prompts.

The result&mdash;40+ strings that are constantly changing and moving within a very large minified JS file.

> [!NOTE]
> Want to **modify a particular piece of the system prompt** in your own Claude Code installation?  **Use [tweakcc](https://github.com/Piebald-AI/tweakcc).**  It&mdash;
> - lets you customize the the individual pieces of the system prompt as markdown files, and then
> - patches your npm-based or native (binary) Claude Code installation with them, and also
> - provides diffing and conflict management for when both you and Anthropic have conflicting modifications to the same prompt file.

## Prompts

Note that some prompts contain interpolated bits such as builtin tool name references, lists of available sub agents, and various other context-specific variables, so the actual counts in a particular Claude Code session will differ slightly&mdash;likely not beyond ±20 tokens, however.
