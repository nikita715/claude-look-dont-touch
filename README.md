# look-dont-touch

A Claude Code plugin that makes Claude act only when you explicitly ask it to. A question gets an answer, not changes.

## What it does

A **SessionStart hook** adds an instruction to every session: change files or run modifying commands only on a direct instruction. Questions get answers, and statements like "we should do X" get discussion, not changes.

It is a behavioral instruction, not a technical restriction: it works in any permission mode, including auto mode, and adds no permission prompts. Reading files and searching the codebase stays unrestricted.

## Install

```
/plugin marketplace add nikita715/claude-look-dont-touch
/plugin install look-dont-touch@claude-look-dont-touch
```

Restart Claude Code after installing. Run `/hooks` to check that the SessionStart hook is registered.

## Customize

Edit `plugin/instructions.md` to change the instruction.