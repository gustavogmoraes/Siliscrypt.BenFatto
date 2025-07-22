---
mode: agent
---
## Purpose
This prompt helps Gustavo create comprehensive meeting outputs for Alvaro after Thomson Reuters meetings. It ensures Alvaro gets all the information needed to execute work without attending meetings. Thomson Reuters is our client through BenFatto (our employer).

## When to Use
- After any Thomson Reuters meeting (training sessions, KT sessions, status updates, requirements gathering)
- When new testing direction is given or requirements change
- When Thomson Reuters provides feedback on previous work
- Before major deliverables or milestone presentations

## Prompt Structure
```
/MeetingOutput with Thomson Reuters on [DATE] about [MEETING_TOPIC].
Key action items for Alvaro: [SPECIFIC_TASKS_WITH_CONTEXT].
Important context: [TECHNICAL_BACKGROUND_AND_SYSTEM_DETAILS].
Thomson Reuters priorities: [WHAT_THEY_CARE_ABOUT_MOST].
Next deadline: [DATE].
Additional context: [MEETING_BACKGROUND_AND_CONCERNS].
```

## Required Information
- **Date**: Meeting date in YYYY-MM-DD format
- **Topic**: Brief description of meeting purpose (KT, training, status, requirements, etc.)
- **Action Items**: Specific, actionable tasks for Alvaro with enough technical detail
- **Context**: System details, technical background, workflow information
- **Thomson Reuters Priorities**: What they care about most right now
- **Deadlines**: When deliverables are due

## Enhanced Usage Examples

### After KT/Training Session
```
/MeetingOutput with Thomson Reuters on 2025-07-22 about OGT configuration management training.
Key action items for Alvaro: learn to access OGT configs via Profile > Debug, practice modifying customer XML config files, validate changes using Integration Workbench inbound_message_path lookup, test system functionality after config modifications.
Important context: OGT is Thomson Reuters' main software, each customer has unique XML config file for customizations (landing pages, tariffs, etc.). Haritha showed step-by-step process for config changes and validation.
Thomson Reuters priorities: ensuring QA team can properly test customer-specific configurations, validating that config changes reflect correctly in system behavior.
Next deadline: 2025-07-25 for initial config testing practice and documentation.
Additional context: training included visual walkthrough with screenshots, several attendees needed clarification on automation triggers and partner config files.
```

### After Status Update Meeting
```
/MeetingOutput with Thomson Reuters on 2025-07-23 about weekly testing progress review.
Key action items for Alvaro: complete regression testing on payment gateway fixes, expand API testing to include rate limiting scenarios, prepare demo environment with test data for stakeholder walkthrough.
Important context: payment system is critical for go-live, Thomson Reuters CEO will attend next demo meeting, they want to see actual test execution with screen recordings.
Thomson Reuters priorities: payment system stability is critical for production release, demo quality matters for executive presentation.
Next deadline: 2025-07-26 for payment gateway validation, 2025-07-28 for demo environment ready.
Additional context: Thomson Reuters impressed with testing thoroughness so far, presentation quality important due to CEO attendance.
```

### After Requirements/Issue Meeting
```
/MeetingOutput with Thomson Reuters on 2025-07-24 about production incident analysis.
Key action items for Alvaro: perform root cause analysis on authentication failures, create comprehensive regression test suite covering edge cases, validate fixes in staging with load testing (1000 concurrent users), test database connection pooling under stress.
Important context: incident caused 2-hour downtime affecting 5000 users, Thomson Reuters reputation at stake, they need extra confidence before next production release.
Thomson Reuters priorities: preventing similar incidents is top priority, thorough testing more important than speed, need detailed documentation of test scenarios.
Next deadline: 2025-07-25 for root cause analysis, 2025-07-27 for complete regression testing.
Additional context: Thomson Reuters stakeholders are nervous about stability, they prefer over-testing to under-testing given recent incident impact.
```

## Output Generation
When this prompt is used, Copilot will:

1. **Create a meeting output file** in `/meetings/` folder
2. **Use the meeting-output-template.md** structure
3. **Fill in all sections** with provided information
4. **Add action items** in checklist format for Alvaro
5. **Include timeline and priority context**
6. **Suggest filename** like: `2025-07-22_client-benfatto-auth-requirements_output.md`

## Tips for Gustavo
- **Provide rich context** - Alvaro needs to understand the system, environment, and business context
- **Be specific about technical details** - include system names, URLs, specific steps, tools required
- **Include Thomson Reuters concerns** - helps Alvaro understand what to focus on and why
- **Mention key Thomson Reuters contacts** - who to escalate to, their roles and expertise areas
- **Include exact quotes** when possible - especially for requirements, concerns, or specific instructions
- **Specify environments and access** - staging, production, specific servers, credentials needed
- **Explain the "why"** - business context helps Alvaro make better testing decisions
- **Note meeting dynamics** - who was confused, what needed clarification, political context

## Quality Checklist
Before finalizing the meeting output, ensure:
- [ ] All action items are specific and testable with enough context
- [ ] Technical requirements include system details and environment info
- [ ] Thomson Reuters priorities and concerns are clearly explained
- [ ] Deadlines are realistic and clearly stated
- [ ] Any blockers or dependencies are noted
- [ ] Background context is sufficient for someone who wasn't in the meeting
- [ ] Next steps are defined for both Gustavo and Alvaro
- [ ] Escalation contacts are included with their expertise areas

## Integration with Workflow
This prompt connects to:
- **Ticket creation**: Action items often become tickets in `/tickets/todo/`
- **Documentation updates**: May require updates to testing procedures or system knowledge
- **Knowledge transfer**: Builds Alvaro's understanding of Thomson Reuters systems and priorities
- **Quality assurance**: Ensures nothing from meetings gets lost and context is preserved
