# Kimi Code Skill

This repository contains the Kimi Code skill for Claude Code. This skill teaches Claude how to delegate tasks to Kimi Code CLI as a subagent for file operations, code summarization, and analysis.

## About the Skill

The Kimi Code skill enables Claude to delegate appropriate tasks to Kimi Code CLI (Moonshot AI's command-line programming assistant) for efficient task distribution.

### Key Features
- Transparent execution with ThinkPart/ToolCall visibility
- Safe --print mode (non-interactive, doesn't auto-approve destructive actions)
- Working directory isolation with -w flag
- Built-in caching with token usage statistics
- Multi-step reasoning capabilities

## Installation

### As a Skill
1. Clone this repository
2. Copy the `skills/kimi-code` directory to your Claude Code skills directory
3. Or use as a plugin (see below)

### As a Plugin (Claude Code)
You can register this repository as a Claude Code Plugin marketplace by running:
```
/plugin marketplace add Dominic789654/kimi-code-skills
```

Then install the skill via:
```
/plugin install kimi-code@Dominic789654-kimi-code-skills
```

## Usage

Once installed, Claude will automatically use this skill when appropriate tasks are detected. The skill guides Claude to:
- Delegate simple to moderate complexity tasks to Kimi Code
- Construct proper kimi commands with --print flag
- Parse Kimi's output (TextPart, ThinkPart, ToolCall sections)
- Handle errors and provide fallbacks

## Skill Structure

- `skills/kimi-code/SKILL.md` - Skill instructions and metadata
- `skills/kimi-code/LICENSE.txt` - Apache 2.0 license

## License

Apache 2.0 - See LICENSE.txt for complete terms.
