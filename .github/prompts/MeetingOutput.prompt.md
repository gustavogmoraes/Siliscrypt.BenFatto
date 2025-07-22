---
mode: agent
---
## Purpose
This prompt helps Gustavo create comprehensive meeting outputs for Alvaro after client meetings with BenFatto/Thomson Reuters. It ensures Alvaro gets all the information needed to execute work without attending meetings.

## When to Use
- After any client meeting (video calls, phone calls, emails)
- When requirements change or new direction is given
- When client provides feedback on previous work
- Before major deliverables or milestones

## Prompt Structure
```
/MeetingOutput with client [CLIENT_NAME] on [DATE] about [MEETING_TOPIC].
Key action items for Alvaro: [SPECIFIC_TASKS].
New testing requirements: [DETAILED_REQUIREMENTS].
Client priorities: [PRIORITY_LIST].
Next deadline: [DATE].
Additional context: [ANY_IMPORTANT_CONTEXT].
```

## Required Information
- **Client Name**: BenFatto, Thomson Reuters, or specific contact person
- **Date**: Meeting date in YYYY-MM-DD format
- **Topic**: Brief description of meeting purpose
- **Action Items**: Specific, actionable tasks for Alvaro
- **Requirements**: Technical requirements, testing scope, new features
- **Priorities**: What client cares about most (security, performance, timeline)
- **Deadlines**: When deliverables are due

## Enhanced Usage Examples

### After Requirements Meeting
```
/MeetingOutput with client BenFatto on 2025-07-22 about new user authentication system.
Key action items for Alvaro: test SSO integration with SAML, verify multi-factor authentication flow, validate session timeout behavior.
New testing requirements: must support Azure AD, Google Workspace, and Okta providers. Test on mobile Safari and desktop Edge browsers specifically.
Client priorities: security compliance first, user experience second, performance third.
Next deadline: 2025-07-25 for initial results, 2025-07-30 for full testing report.
Additional context: client mentioned they had issues with previous vendor's SSO implementation, so they're particularly concerned about edge cases and error handling.
```

### After Status Update Meeting
```
/MeetingOutput with client Thomson Reuters on 2025-07-23 about weekly status review.
Key action items for Alvaro: retest the payment gateway issue found last week, expand API testing to include rate limiting scenarios, prepare demo environment for client walkthrough.
New testing requirements: client wants to see actual test execution during next meeting, need screen recordings of critical test scenarios.
Client priorities: payment system stability is critical for go-live, demo readiness for stakeholder presentation.
Next deadline: 2025-07-26 for payment gateway confirmation, 2025-07-28 for demo prep.
Additional context: client CEO will attend next meeting, so presentation quality is important. They're impressed with thoroughness so far.
```

### After Issue Escalation Meeting
```
/MeetingOutput with client BenFatto on 2025-07-24 about production incident review.
Key action items for Alvaro: perform root cause analysis on login failures, create comprehensive regression test suite, validate fix in staging environment before production deployment.
New testing requirements: must include load testing with 1000 concurrent users, validate database connection pooling under stress, test failover scenarios.
Client priorities: preventing similar incidents is top priority, need confidence in stability before next release.
Next deadline: 2025-07-25 for root cause analysis, 2025-07-27 for regression testing completion.
Additional context: incident caused 2-hour downtime affecting 5000 users. Client's reputation is at stake, so extra thorough testing is essential.
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
- **Be specific** about technical requirements - Alvaro needs details to test effectively
- **Include client concerns** - helps Alvaro understand what to focus on
- **Mention client personality/preferences** - helps tailor communication style
- **Note any political context** - important stakeholders, sensitive areas
- **Include exact quotes** when possible - especially for requirements or concerns
- **Specify environments** - staging, production, specific test servers
- **List any credentials or access** needed for testing

## Quality Checklist
Before finalizing the meeting output, ensure:
- [ ] All action items are specific and testable
- [ ] Deadlines are realistic and clearly stated
- [ ] Technical requirements include enough detail for execution
- [ ] Client priorities are clearly ranked
- [ ] Any blockers or dependencies are noted
- [ ] Next steps are defined for both Gustavo and Alvaro
- [ ] Contact information is included if Alvaro needs to escalate

## Integration with Workflow
This prompt connects to:
- **Ticket creation**: Action items often become tickets in `/tickets/todo/`
- **Documentation updates**: May require updates to testing procedures
- **Client communication**: Sets expectations for next deliverables
- **Quality assurance**: Ensures nothing from meetings gets lost
