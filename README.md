# A minimal coding with Agent set-up

## Context management:
> As we know that LLM has limited context window size, that cannot remember large data, to solve that we can use,
obsidian which as a persistent knowledge for LLM which use md files as principle which very suitable for LLM.

Please refer `obsidian/` which as a minimal template as you can go.

## Agent selection as the experience:
1. we can use the simple task for gemini 3.1 pro/flash model
2. If we need more complex works, we can use gpt-5.2-codex(fast, high, high-fast, xhigh, xhigh-fast), or claude 4.6, those are best agent engineers right now.
3. In cursor, avoid using MAX mode -> which burn your tokens/requests alot before you can finish your tasks, using cheap models + right workflows > expensive models.

## Planning vs vibe:
1. I prefer using plan mode in cursor, each time I need to implement complex tasks which much better just prompting and execute with agent mode.
2. combine plan mode with [Superpower plugin](https://github.com/obra/superpowers).
3. consider provide context for agents more than write simple prompt to force agent do its research, that help agents alot and reduce the tokens cost.