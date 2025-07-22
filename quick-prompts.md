# Quick Copilot Prompts

These shortcuts help you quickly create coordination documents using the templates.

## 📝 Template Prompts

### `/MeetingOutput`
**Use this after client meetings (Gustavo)**
```
/MeetingOutput with client BenFatto on [date] about [topic]. 
Key action items for Alvaro: [list]. 
New testing requirements: [details].
Client priorities: [list].
Next deadline: [date].
```

### `/TicketDocumentation` 
**Use this after completing work (Alvaro)**
```
/TicketDocumentation for ticket [TR-XXX] about [feature/bug].
Testing completed on [environment].
Results: [passed/failed scenarios].
Issues found: [list with severity].
Time spent: [hours].
Ready for Gustavo to present.
```

### `/QuickQuestion`
**Use this when you need help (Alvaro)**
```
/QuickQuestion about [topic].
I'm working on [ticket/task].
Stuck on: [specific issue].
Tried: [what you attempted].
Need answer by: [timeline].
```

---

## 📚 Detailed Documentation

For comprehensive usage instructions, examples, and best practices, see:
- **`/.github/prompts/MeetingOutput.prompt.md`** - Complete `/MeetingOutput` guide
- **`/.github/prompts/TicketDocumentation.prompt.md`** - Complete `/TicketDocumentation` guide  
- **`/.github/prompts/QuickQuestion.prompt.md`** - Complete `/QuickQuestion` guide

## 💡 Usage Examples

**Gustavo after a client meeting:**
> /MeetingOutput with client BenFatto on 2025-07-22 about login testing requirements. Key action items for Alvaro: test new SSO integration, verify password reset flow, check mobile responsiveness. New testing requirements: must test on Safari and Edge browsers. Client priorities: security first, then performance. Next deadline: 2025-07-25.

**Alvaro after completing testing:**
> /TicketDocumentation for ticket TR-001 about login functionality testing. Testing completed on staging environment. Results: 8/10 scenarios passed, SSO integration failed on Safari. Issues found: critical SSO bug, minor UI alignment issue. Time spent: 6 hours. Ready for Gustavo to present.

**Alvaro when stuck:**
> /QuickQuestion about test environment access. I'm working on TR-002 API testing. Stuck on: can't access staging API, getting 403 errors. Tried: VPN connection, different credentials. Need answer by: tomorrow morning.

## 🎯 Pro Tips

- **Be specific** in your prompts - include ticket IDs, dates, environments
- **Use consistent naming** - helps with searchability later
- **Include timelines** - especially for questions and deadlines
- **Focus on client impact** - what matters to BenFatto/Thomson Reuters
- **Document everything** - better to over-document than under-document
