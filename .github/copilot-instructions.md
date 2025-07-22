# Copilot Instructions for Siliscrypt.BenFatto Project

## 🎯 Main Objective
This repository manages QA subcontracting work for **BenFatto** → **Thomson Reuters**. The key dynamic is:
- **Gustavo**: Primary contractor (client-facing), handles meetings and complex issues
- **Alvaro**: Technical executor (backend), does 80%+ of actual testing work
- **Client must never know** about this division - everything appears as Gustavo's work

## 🔒 Critical Rules
1. **All client communication goes through Gustavo only**
2. **Alvaro's work must be documented so Gustavo can present it as his own**
3. **Keep internal workflow simple and flexible**
4. **Focus on asynchronous coordination between Gustavo and Alvaro**
5. **Maintain professional appearance for BenFatto/Thomson Reuters**

## 📁 Repository Structure
```
├── tickets/              # Simple kanban: todo/doing/done
├── notes/               # Quick documentation
├── meetings/            # Meeting outputs from Gustavo
├── templates/           # Coordination templates
├── .github/
│   ├── copilot-instructions.md  # These instructions
│   └── prompts/         # Detailed prompt definitions
├── INTERNAL-WORKFLOW.md # Private working agreement
└── README.md           # Simple project overview
```

## 🔄 Workflow Understanding
### Gustavo's Role:
- Attends all client meetings
- Handles complex technical escalations
- Presents all work as his own
- Provides direction to Alvaro via meeting outputs

### Alvaro's Role:
- Executes most tickets and testing work
- Documents everything for Gustavo's presentation
- Escalates when stuck
- Works asynchronously based on meeting outputs

## 🎯 Template System
### `/MeetingOutput` - Gustavo → Alvaro
After client meetings, Gustavo documents what Alvaro needs to know and do

### `/TicketDocumentation` - Alvaro → Gustavo  
When Alvaro completes work, documents it so Gustavo can present confidently

### `/QuickQuestion` - Alvaro → Gustavo
When Alvaro needs guidance or clarification

## 💡 When Helping Users:
- **Keep solutions simple** - they prefer to evolve organically
- **Focus on practical templates** that enable async coordination
- **Always maintain the client-facing facade** - everything appears as Gustavo's work
- **Prioritize documentation** that helps knowledge transfer
- **Suggest lightweight processes** that can be expanded as needed

## 🚫 Avoid:
- Over-engineering the workflow
- Complex folder structures
- Processes that require constant synchronization
- Anything that exposes the internal work division to clients
- Heavy templates that slow down actual work

## 🎯 Success Metrics:
- Gustavo can confidently present any work Alvaro does
- Alvaro has clear direction from meetings he doesn't attend
- Client sees consistent, professional service
- Minimal coordination overhead between Gustavo and Alvaro
- Clear escalation path when Alvaro hits complex issues
