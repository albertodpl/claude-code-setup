# Claude Code Setup

Configuration files and custom commands for integrating Claude Code with my Obsidian vault that implements the PARA method (Projects, Areas, Resources, Archive) combined with Zettelkasten and GTD principles, plus additional productivity workflows.

## Overview

This repository contains custom Claude Code configurations to enhance productivity by integrating with an Obsidian knowledge base that follows:

- **PARA Method**: Organizational structure with Projects, Areas, Resources, and Archive folders
- **Zettelkasten**: Atomic notes with timestamp IDs and bi-directional linking
- **GTD (Getting Things Done)**: Task management with contexts, priorities, and time-based filtering

The commands for the Obsidian vaults are very specific to my personal setup, but it may serve as inspiration or starting point for others implementing similar systems.

## Structure

```
claude-configuration/
├── global/
│   └── _claude/
│       └── commands/
│           ├── commit.md         # Git commit automation
│           └── push.md          # Git push automation
└── obsidian-vault/
    └── _claude/
        └── commands/
            ├── add-thought.md    # Quick thought capture to Obsidian INBOX
            └── todo.md          # Task management for Obsidian
```

## Custom Commands

### /add-thought
Captures quick thoughts and ideas directly to your Obsidian INBOX with timestamp formatting.

**Usage:**
```
/add-thought Your thought description here
```

### /todo
Comprehensive task management system for Obsidian with support for:
- Creating tasks with priorities and due dates
- Marking tasks as complete
- Listing tasks by project or area

**Usage:**
```
/todo add Task description
/todo add -p "Project Name" -m "Task description" -d 2024-01-15 -P high
/todo complete Task description
```

## Features

- **Obsidian Integration**: Seamlessly work with your existing Obsidian vault
- **PARA Method Support**: Organized around Projects, Areas, Resources, and Archive
- **Zettelkasten Compatible**: Supports timestamp-based note IDs and atomic notes
- **Time-stamped Entries**: Automatic timestamp formatting for capture files
- **Priority Management**: High/low priority task support with emoji indicators

## Setup

1. Place this configuration in your Claude Code configuration directory
2. Ensure your Obsidian vault follows the PARA method structure
3. Use the custom commands via Claude Code's slash command interface

## Obsidian Vault Structure

The commands expect a specific PARA method folder structure:

- `0 INBOX 📥` - Capture inbox for new ideas and information
- `1 PROJECTS 🚀` - Active projects with deadlines
- `2 AREAS ♻️` - Areas of ongoing responsibility 
- `3 RESOURCES 📚` - Reference materials including Zettelkasten notes
- `4 ARCHIVE 🗄` - Completed or inactive items
- `5 TOOLS 🧰` - Templates and configuration files

## Requirements

- Claude Code
- Obsidian vault with PARA method folder structure
- Markdown-based note-taking system with Obsidian-flavored markdown

## Note

This configuration is continuously evolving as I implement new workflows and automation. The Obsidian-specific commands are tailored to my personal productivity system but may provide useful patterns for others building similar integrations.

I'm aware of the existing Obsidian MCP integration and will most likely move in that direction in the future. However, I wanted to first get a feel for how much can be accomplished with barebone commands before adopting more sophisticated tooling.
