# GitHub Copilot Prompts for Siliscrypt.BenFatto

This directory contains detailed prompt definitions for the BenFatto/Thomson Reuters QA project.

## Available Prompts

### Core Coordination Prompts

#### `/MeetingOutput`
**File**: `MeetingOutput.prompt.md`  
**User**: Gustavo (after client meetings)  
**Purpose**: Document meeting outcomes and provide direction to Alvaro

#### `/TicketDocumentation`
**File**: `TicketDocumentation.prompt.md`  
**User**: Alvaro (after completing work)  
**Purpose**: Document completed work so Gustavo can present to clients

#### `/QuickQuestion`
**File**: `QuickQuestion.prompt.md`  
**User**: Alvaro (when blocked or needing guidance)  
**Purpose**: Efficiently escalate questions to Gustavo

## How to Use

1. **Type the prompt** (e.g., `/MeetingOutput`) in Copilot chat
2. **Follow the structure** defined in the corresponding file
3. **Copilot will generate** the appropriate document using the templates
4. **Files are created** in the correct project folders automatically

## Project Context

This prompt system supports asynchronous coordination between:
- **Gustavo**: Primary contractor (client-facing)
- **Alvaro**: Technical executor (80%+ of actual work)
- **Client**: BenFatto → Thomson Reuters (unaware of internal division)

## Key Benefits

- **Seamless handoffs** between client meetings and technical execution
- **Professional documentation** that maintains client-facing facade
- **Efficient communication** without constant synchronous meetings
- **Complete knowledge transfer** for confident client presentations

## Integration

These prompts work with:
- Project templates in `/templates/`
- Ticket workflow in `/tickets/`
- Meeting documentation in `/meetings/`
- Quick notes in `/notes/`

For quick reference, see `/quick-prompts.md` in the project root.

## Prompt Files

- **`MeetingOutput.prompt.md`** - Complete `/MeetingOutput` guide and implementation
- **`TicketDocumentation.prompt.md`** - Complete `/TicketDocumentation` guide and implementation
- **`QuickQuestion.prompt.md`** - Complete `/QuickQuestion` guide and implementation
