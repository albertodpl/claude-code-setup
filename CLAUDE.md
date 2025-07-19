# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repository contains custom Claude Code configurations for integrating with an Obsidian knowledge base that follows the PARA method (Projects, Areas, Resources, Archive) and Zettelkasten system. The main purpose is to enable productivity workflows through custom slash commands that interact with Obsidian vault files.

## Architecture

The project is organized as a configuration repository with custom Claude Code commands:

### Core Structure
```
claude-configuration/obsidian-vault/_claude/commands/
├── add-thought.md    # Quick thought capture to Obsidian INBOX
└── todo.md          # Task management for Obsidian
```

### Custom Commands System

The repository implements two main slash commands that interact with an Obsidian vault:

#### /add-thought Command
- **Purpose**: Captures quick thoughts to daily capture files
- **Target**: `0 INBOX` folder with format `YYYY-MM-DD Capture.md`
- **Behavior**: Appends timestamped entries with format `**HH:MM:**`
- **Usage**: `/add-thought Your thought description here`

#### /todo Command
- **Purpose**: Comprehensive task management system for Obsidian
- **Target Locations**: 
  - Default: `0 INBOX` folder in daily capture files
  - Specified: Project/Area main notes in `1 PROJECTS` or `2 AREAS` folders
- **Task Format**: 
  - Pending: `- [ ] #task <description> [#when/this_week] [priority] [recurrence] creation_date [due_date]`
  - Completed: `- [x] #task <description> [#when/this_week] [priority] [recurrence] creation_date [due_date] completed_date`
- **Priority System**: ⏬ (low) or 🔺 (high)
- **Date Format**: ➕ YYYY-MM-DD (creation), 📅 YYYY-MM-DD (due), ✅ YYYY-MM-DD (completion)

### Integration Requirements

When working with this system:

1. **Obsidian Vault Structure**: The commands expect a PARA method folder structure:
   - `0 INBOX 📥` - Capture inbox for new ideas
   - `1 PROJECTS 🚀` - Active projects with deadlines
   - `2 AREAS ♻️` - Areas of ongoing responsibility
   - `3 RESOURCES 📚` - Reference materials
   - `4 ARCHIVE 🗄` - Completed or inactive items

2. **File Naming Conventions**:
   - Daily capture files: `YYYY-MM-DD Capture.md`
   - Zettelkasten notes: `YYYYMMDDHHMM ID.md` format

3. **Task Management Workflow**:
   - Tasks search across `0 INBOX`, `1 PROJECTS`, and `2 AREAS` folders
   - Task completion searches for matching descriptions and updates in-place
   - Time-sensitive tasks use `#when/this_week` tags for filtering

## Development Notes

This is primarily a configuration repository with no build process, tests, or traditional development commands. The "code" consists of markdown files that define custom Claude Code slash commands for Obsidian integration.

When modifying commands:
- Maintain the existing markdown-based command format
- Preserve the Obsidian vault structure expectations
- Keep task format compatibility with the existing system
- Follow the timestamp and emoji conventions established in the system