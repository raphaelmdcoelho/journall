# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is an Obsidian vault used for personal knowledge management, journaling, and note-taking. The repository contains markdown files organized into topic-based directories with links between notes following the Obsidian/Zettelkasten methodology.

## Structure

The vault is organized into the following main areas:

- **Journal/**: Daily journal entries organized by month (e.g., DECEMBER.md)
- **Technology/**: Technical notes organized by topic
  - Python/: Python programming notes with visual map (PYTHON.md is an Excalidraw drawing linking to sub-topics)
  - Terminal/: Terminal and Git Bash command references
  - Shell/: Shell scripting notes
  - Linux/: Linux system notes
- **AI/**: AI-related notes (e.g., Semantic Kernel SDK documentation)
- **Languages/**: Language learning materials
  - Chinese/: Chinese language learning with Excalidraw drawings
- **Anatomy/**: Anatomy study notes with reference images in Images/Anatomy/
- **Images/**: Image assets referenced by notes

## Obsidian Configuration

This vault uses:
- **Excalidraw plugin**: For visual mind maps and drawings embedded in markdown files
  - Python topic map: [Technology/Python/PYTHON.md](Technology/Python/PYTHON.md)
  - Chinese learning diagrams: [Languages/Chinese/](Languages/Chinese/)
- Obsidian internal links: `obsidian://open?vault=journall&file=...`

## Working with Notes

### Note Format
- Notes use Obsidian-flavored markdown with YAML frontmatter
- Excalidraw files contain compressed JSON data - treat as binary, do not edit the compressed data directly
- Tags are used for categorization (e.g., `#tech`, `#ai`)

### Creating New Notes
- Place technical notes in appropriate Technology/ subdirectories
- Use descriptive filenames with title case (e.g., "Python - Functions.md")
- Add relevant tags in frontmatter or at the bottom of the file

### Editing Excalidraw Files
- Files with Excalidraw data contain a warning: "Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu"
- The "Text Elements" section contains readable labels
- The "Element Links" section shows Obsidian links between elements
- Do not modify the compressed JSON data - edit only text elements or links sections if needed

## Git Workflow

This repository tracks:
- Main branch: `main`
- Standard git operations for version control of notes
- Git ignores are not configured, so be mindful of sensitive information in notes

### Common Commands
```bash
# View status
git status

# Commit notes
git add .
git commit -m "descriptive message"

# Push changes
git push origin main
```

## Important Patterns

1. **Visual Knowledge Maps**: PYTHON.md and other Excalidraw files serve as visual indexes linking to detailed topic pages
2. **Hierarchical Organization**: Main topic files (e.g., PYTHON.md) link to subtopic files (e.g., "Python - Types.md", "Python - Functions.md")
3. **Cross-linking**: Notes reference each other using Obsidian's internal link format
4. **Mixed Languages**: Content includes English and Portuguese notes

## When Working in This Vault

- Respect the existing organizational structure
- Maintain consistency with existing file naming conventions
- Preserve Excalidraw embedded drawings intact
- Keep the visual map files (like PYTHON.md) as navigation aids
- Use tags consistently with existing patterns
- please, use emojis when possible