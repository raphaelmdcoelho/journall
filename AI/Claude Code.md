
## Overview

It is a `agentic coding tool` that lives in the `terminal`.

To start use it is simple:

```bash
cd project-folder
claude
```

What it does:

* Build features from descriptions.
* Debug and fix issues.
* Navigate any codebase.
* Automate tasks.

Claude code is `Unix philosophy`:

```bash
tail f app.log | claude -p "Slack me if you see any anomalies appear in this log stream".
```

## Slash Commands

* **/init**
* **/memory** *there is a `Project memory` and `User Memory`*
	* `#` add the content to be added to the memory.
* **/mcp**
	```bash
	claude mcp -h
	claude mcp list
	claude mcp remove MCP_SERVER_NAME
	claude mcp add MCP_SERVER_NAME mcp_command
	```
	Obs.: .claude/settings.local.json
## Settings

`SHIFT` + `TAB` --> `auto-accept edits on` or `plan mode on`

## Structure

`CLAUDE.md` is like a memory to Claude Code.

There is a folder called `.claude` that stores configuration info.

* `settings.local.json` is a local file to store configuration like permissions allows and denies.
* `commands`: It's a folder that stores custom commands:
```markdown

# Task

Follow the instructions ... <instructions></instructions> ...

## Tasks to be performed: $ARGUMENTS

<instructions> ... </instructions>

```

## Hooks

The AI agent executes a commands that you choose.

```json
{
	"hooks": {
		"EventName": [
			{
				"matcher": "ToolPattern",
				"hooks": [
					{
						"type": "command",
						"command": "your-command-here"
					}
				]
			}
		]
	}
}
```

#ai #cli 