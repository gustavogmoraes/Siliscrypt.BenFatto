# Integration Guide - How to Use This System

## 🚀 Getting Started

### For Gustavo (After Client Meetings):
1. Use prompt: `/MeetingOutput with client [name] on [date] about [topic]...`
2. Copilot will create a meeting output file in `meetings/`
3. Alvaro reads it and knows exactly what to do

### For Alvaro (After Completing Work):
1. Use prompt: `/TicketDocumentation for ticket [ID] about [work]...`
2. Copilot creates documentation in `tickets/done/`
3. Gustavo reviews and can confidently present to client

### For Questions/Blockers:
1. Use prompt: `/QuickQuestion about [topic]...`
2. Copilot creates question file in `notes/`
3. Gustavo responds in the same file

## 🔄 Daily Workflow Examples

### Gustavo's Morning (After Client Meeting):
```
> /MeetingOutput with client BenFatto on 2025-07-22 about security testing. 
  Key action items for Alvaro: penetration testing, vulnerability scan, 
  security audit report. Client priorities: data encryption, access controls. 
  Next deadline: 2025-07-25.
```

### Alvaro's Evening (After Completing Testing):
```
> /TicketDocumentation for ticket TR-003 about security audit. 
  Testing completed on production environment. 
  Results: found 2 critical vulnerabilities, 5 medium issues. 
  Time spent: 8 hours. Ready for Gustavo to present.
```

### When Alvaro Gets Stuck:
```
> /QuickQuestion about production access. I'm working on TR-003 security testing. 
  Stuck on: need admin credentials for vulnerability scan. 
  Tried: current test account doesn't have sufficient permissions. 
  Need answer by: tomorrow morning.
```

## 📋 File Organization

### Meeting Outputs:
- `meetings/2025-07-22_client-security-review_output.md`
- Gustavo creates these after meetings
- Alvaro reads for direction

### Ticket Documentation:
- `tickets/done/TR-003_security-audit_DOCUMENTED.md`
- Alvaro creates these after completing work
- Gustavo reviews before client presentation

### Questions/Communication:
- `notes/2025-07-22_question-prod-access.md`
- For async coordination
- Both can create/respond

## 🎯 Success Indicators

✅ **Working Well When:**
- Gustavo can confidently discuss any work Alvaro completed
- Alvaro has clear direction without attending meetings
- Client sees consistent, professional service
- Minimal back-and-forth needed between Gustavo and Alvaro

❌ **Needs Improvement When:**
- Gustavo is surprised by questions about Alvaro's work
- Alvaro is working without clear requirements
- Client notices inconsistencies
- Too much synchronous coordination needed

## 💡 Pro Tips

1. **Use the prompts consistently** - they're designed for your workflow
2. **Document everything** - better to over-document than miss something
3. **Be specific with ticket IDs and dates** - helps with tracking
4. **Focus on client impact** - what matters to BenFatto/Thomson Reuters
5. **Keep templates simple** - you can always add detail later

## 🔧 Customization

The system is designed to evolve. You can:
- Modify templates based on what works
- Add new prompt shortcuts as needed
- Adjust folder structure if requirements change
- Create specialized templates for specific types of work

Remember: **Keep it simple and practical** - the goal is efficient async coordination, not perfect documentation.
