---
mode: agent
---
## Purpose
This prompt helps Alvaro efficiently communicate with Gustavo when blocked, confused, or needing guidance. It ensures questions are clear, actionable, and include necessary context for quick resolution.

## When to Use
- When stuck on technical implementation or testing approach
- When client requirements are unclear or contradictory
- When you need access to systems, credentials, or environments
- When discovering issues that might affect client relationships
- When unsure about testing scope or priorities
- Before escalating issues that might require client communication

## Prompt Structure
```
/QuickQuestion about [SPECIFIC_TOPIC].
I'm working on [TICKET_OR_TASK].
Stuck on: [SPECIFIC_PROBLEM].
Tried: [WHAT_YOU_ATTEMPTED].
Need answer by: [TIMELINE].
Impact: [HOW_THIS_AFFECTS_WORK].
```

## Required Information
- **Specific Topic**: Clear, focused question topic
- **Current Work**: What ticket or task you're working on
- **Specific Problem**: Exact issue or blocker you're facing
- **Attempts Made**: What you've already tried to solve it
- **Timeline**: When you need an answer to continue working
- **Impact**: How this affects deliverables or client work

## Enhanced Usage Examples

### Environment Access Issues
```
/QuickQuestion about staging environment access for API testing.
I'm working on TR-025 API security testing.
Stuck on: getting 403 forbidden errors when trying to access staging API endpoints at api-staging.benfatto.com.
Tried: VPN connection, cleared browser cache, tried different test accounts (testuser1, testuser2), checked API documentation for authentication requirements.
Need answer by: tomorrow morning (2025-07-23 9:00 AM).
Impact: cannot complete API security testing without access, client expects results by 2025-07-25.
```

### Requirements Clarification
```
/QuickQuestion about browser compatibility requirements for mobile testing.
I'm working on TR-018 mobile responsiveness validation.
Stuck on: client said "test on mobile browsers" but didn't specify which versions. Should I test on all iOS/Android versions or just latest?
Tried: checking meeting notes and project documentation, but no specific versions mentioned.
Need answer by: this afternoon (2025-07-22 3:00 PM).
Impact: affects testing scope and timeline - could be 2 hours vs 8 hours of work depending on requirements.
```

### Technical Implementation Questions
```
/QuickQuestion about load testing parameters for performance validation.
I'm working on TR-030 performance testing before go-live.
Stuck on: what constitutes acceptable response times and concurrent user targets? Client mentioned "fast performance" but no specific metrics.
Tried: industry standard research (found 2-3 seconds is typical), checked similar projects in our notes, reviewed application architecture.
Need answer by: tomorrow end of day (2025-07-23 5:00 PM).
Impact: affects test design and pass/fail criteria - need client-approved benchmarks before starting performance testing.
```

### Critical Issue Discovery
```
/QuickQuestion about critical security vulnerability found during testing.
I'm working on TR-012 user authentication testing.
Stuck on: discovered users can access other users' data by manipulating URL parameters. This is a serious security flaw.
Tried: confirmed issue exists across multiple test accounts, documented reproduction steps, verified it's not test environment configuration issue.
Need answer by: immediately - this is critical.
Impact: this could be a data breach risk if deployed to production. Client needs to know ASAP but not sure how to communicate without alarming them.
```

### Client Communication Strategy
```
/QuickQuestion about how to handle negative test results with high-profile client.
I'm working on TR-033 final pre-launch testing for Thomson Reuters.
Stuck on: found 15 issues including 3 critical bugs that will delay launch. Client has already announced launch date publicly.
Tried: double-checked all findings, created detailed reproduction steps, categorized by severity, prepared technical summary.
Need answer by: before tomorrow's client meeting (2025-07-24 10:00 AM).
Impact: client relationship is at stake - need guidance on how to present bad news professionally and constructively.
```

### Tool and Process Questions
```
/QuickQuestion about automated testing tool selection for regression testing.
I'm working on TR-040 automated test suite development.
Stuck on: client wants automated testing but didn't specify tools. Should I use Selenium, Playwright, or Cypress? Budget and maintenance implications differ significantly.
Tried: researched pros/cons of each tool, considered client's tech stack (React/Node.js), evaluated learning curve and maintenance requirements.
Need answer by: end of week (2025-07-26).
Impact: affects project timeline, budget, and long-term maintenance strategy. Wrong choice could mean rebuilding test suite later.
```

## Output Generation
When this prompt is used, Copilot will:

1. **Create a question file** in `/notes/` folder
2. **Use the quick-question-template.md** structure
3. **Include all context and attempts made**
4. **Provide space for Gustavo's response**
5. **Suggest filename** like: `2025-07-22_question-staging-api-access.md`

## Tips for Alvaro
- **Be specific**: "Can't access API" vs "Getting 403 errors on /api/v1/users endpoint"
- **Show your work**: List everything you tried - demonstrates you're not just asking without effort
- **Include error messages**: Copy exact error text, screenshots if helpful
- **Consider client impact**: How does this affect deliverables or relationships?
- **Suggest solutions**: If you have ideas, mention them - shows initiative
- **Be realistic about timelines**: Give Gustavo enough time to respond thoughtfully
- **Escalate appropriately**: Mark urgent things as urgent, but don't cry wolf

## Response Time Expectations
- **Critical issues**: Gustavo responds within 2 hours during business hours
- **Blocking issues**: Response within 4-6 hours
- **Clarification questions**: Response within 24 hours
- **Strategic/planning questions**: Response within 48 hours

## Question Categories

### Technical Questions
- Environment access and configuration
- Tool selection and implementation
- Performance benchmarks and criteria
- Security requirements and testing approaches

### Client Relationship Questions
- How to communicate bad news or delays
- Requirements clarification strategies
- Presentation and reporting approaches
- Escalation procedures for critical issues

### Process Questions
- Testing scope and priorities
- Documentation standards
- Quality gates and acceptance criteria
- Timeline management and adjustments

## Integration with Workflow
Questions often lead to:
- **Updated meeting outputs**: Gustavo may need to clarify with client
- **Modified tickets**: Requirements or scope changes
- **Process improvements**: Better procedures for future work
- **Documentation updates**: Lessons learned for team knowledge

## Follow-up Actions
After Gustavo responds:
- [ ] Update ticket with clarified requirements
- [ ] Document solution in notes for future reference
- [ ] Adjust timeline estimates if needed
- [ ] Communicate status to stakeholders if required
- [ ] Close the question file or mark as resolved

## Emergency Escalation
For critical issues requiring immediate attention:
- Use "URGENT" in the question title
- Include potential client impact
- Suggest immediate next steps
- Provide your contact info for real-time discussion
- Consider whether client needs to be contacted immediately
