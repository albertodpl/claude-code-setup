# Claude Code Setup

Configuration files and custom commands for integrating Claude Code with Obsidian vault and personal productivity workflows.

## Overview

This repository contains custom Claude Code configurations to enhance productivity by integrating with an Obsidian knowledge base using the PARA method and Zettelkasten system.

## Structure

```
claude-configuration/
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

## Requirements

- Claude Code
- Obsidian vault with PARA method folder structure
- Markdown-based note-taking system
