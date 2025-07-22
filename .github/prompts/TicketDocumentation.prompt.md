---
mode: agent
---
## Purpose
This prompt helps Alvaro create comprehensive documentation of completed work so Gustavo can present it confidently to BenFatto/Thomson Reuters clients. It ensures all technical work appears as if Gustavo performed it himself.

## When to Use
- After completing any testing ticket or task
- When finding critical bugs or issues
- Before moving tickets to "done" status
- When client will ask about specific work performed
- After any significant testing milestone

## Prompt Structure
```
/TicketDocumentation for ticket [TICKET_ID] about [WORK_DESCRIPTION].
Testing completed on [ENVIRONMENT].
Results: [SUMMARY_OF_OUTCOMES].
Issues found: [LIST_WITH_SEVERITY].
Time spent: [HOURS].
Client impact: [BUSINESS_IMPACT].
Ready for Gustavo to present.
```

## Required Information
- **Ticket ID**: TR-XXX or BF-XXX format
- **Work Description**: Brief summary of what was tested/completed
- **Environment**: Staging, production, dev, specific URLs
- **Results**: Pass/fail summary, key findings
- **Issues Found**: Bugs, problems, areas of concern with severity levels
- **Time Spent**: Actual hours worked (for internal tracking)
- **Client Impact**: How this affects the client's business or users

## Enhanced Usage Examples

### After Functional Testing
```
/TicketDocumentation for ticket TR-015 about user registration and email verification flow.
Testing completed on staging environment (staging.benfatto.com).
Results: 12 of 15 test scenarios passed successfully. Email verification works correctly for Gmail, Outlook, and Yahoo providers. Registration form validation is functioning as expected.
Issues found: critical - email verification fails for corporate domains with strict security policies (3 companies tested), medium - registration success message disappears too quickly (2 seconds), minor - form field alignment issue on mobile Safari.
Time spent: 8 hours over 2 days.
Client impact: registration flow is ready for go-live with 80% success rate, but corporate users may experience issues requiring manual activation.
Ready for Gustavo to present.
```

### After Security Testing
```
/TicketDocumentation for ticket TR-022 about API security and authentication testing.
Testing completed on production environment using isolated test accounts.
Results: API authentication mechanisms are secure and functioning correctly. Rate limiting is properly implemented. JWT token handling follows security best practices.
Issues found: high - API returns detailed error messages that could reveal system information to attackers, medium - rate limiting threshold may be too generous (1000 requests/minute), low - missing CORS headers for some endpoints.
Time spent: 12 hours including penetration testing tools setup.
Client impact: API is secure for launch but should implement error message sanitization before production release to prevent information disclosure.
Ready for Gustavo to present.
```

### After Performance Testing
```
/TicketDocumentation for ticket TR-008 about database query optimization and load testing.
Testing completed on staging environment with production data volume simulation.
Results: application handles 500 concurrent users without performance degradation. Database queries average 200ms response time. Memory usage stays within acceptable limits.
Issues found: critical - search functionality times out with more than 750 concurrent users, medium - database connection pool exhaustion after 6 hours of continuous load, minor - slight memory leak in user session management.
Time spent: 16 hours including load test script development.
Client impact: system is ready for expected user load (300-400 concurrent) but may experience issues during peak traffic periods requiring infrastructure scaling.
Ready for Gustavo to present.
```

### After Bug Fix Verification
```
/TicketDocumentation for ticket TR-030 about login issue resolution verification.
Testing completed on staging environment after developer deployment.
Results: original login bug is fully resolved. Users can now successfully authenticate with all supported providers (Google, Microsoft, Facebook). Session persistence is working correctly.
Issues found: none - all previously failing scenarios now pass. Regression testing confirms no new issues introduced.
Time spent: 4 hours for comprehensive verification testing.
Client impact: critical login issue is resolved and ready for production deployment. No user impact expected.
Ready for Gustavo to present.
```

## Output Generation
When this prompt is used, Copilot will:

1. **Create a documentation file** in `/tickets/done/` folder
2. **Use the ticket-documentation-template.md** structure
3. **Fill in all technical sections** with provided information
4. **Generate client-ready summary** in Gustavo's voice
5. **Include test evidence and metrics**
6. **Suggest filename** like: `TR-015_user-registration-testing_DOCUMENTED.md`

## Tips for Alvaro
- **Write as if Gustavo tested it** - use professional, confident tone
- **Include specific metrics** - numbers give credibility (response times, success rates)
- **Categorize issues clearly** - critical, high, medium, low with business impact
- **Provide reproduction steps** - for any bugs found
- **Include screenshots/evidence** - visual proof of testing performed
- **Think about client questions** - what would they want to know?
- **Focus on business impact** - how does this affect their users/revenue?
- **Be honest about limitations** - better to mention concerns than hide them

## Technical Details to Include
- **Browsers tested**: Specific versions (Chrome 120, Firefox 119, Safari 17)
- **Operating systems**: Windows 11, macOS 14, iOS 17, Android 13
- **Test data used**: Types of accounts, data volumes, edge cases
- **Tools utilized**: Testing frameworks, automation tools, monitoring tools
- **Performance metrics**: Response times, throughput, error rates
- **Security considerations**: Authentication, authorization, data protection

## Client-Ready Language
Transform technical findings into business language:

| Technical Finding | Client-Ready Description |
|------------------|--------------------------|
| "SQL injection vulnerability" | "Security gap that could allow unauthorized data access" |
| "Memory leak in session handler" | "Performance issue that may slow system over time" |
| "CSS layout breaks on mobile" | "Display issue affecting mobile user experience" |
| "API rate limiting missing" | "System may be vulnerable to overload during high traffic" |

## Quality Checklist
Before finalizing documentation, ensure:
- [ ] All test scenarios are clearly described
- [ ] Issues are categorized by severity and business impact
- [ ] Screenshots or evidence files are referenced
- [ ] Client presentation summary is professional and confident
- [ ] Technical details are sufficient for Gustavo to answer questions
- [ ] Recommendations are actionable and realistic
- [ ] Timeline and effort estimates are included
- [ ] Related tickets or follow-up work is noted

## Integration with Workflow
This documentation enables:
- **Client presentations**: Gustavo has all facts and can speak authoritatively
- **Status reporting**: Progress and quality metrics for client updates
- **Issue tracking**: Problems are documented for developer team
- **Knowledge transfer**: Future team members understand what was tested
- **Quality assurance**: Comprehensive record of testing coverage

## Common Client Questions (Be Prepared)
When Gustavo presents your work, clients often ask:
- "How confident are you that this is ready for production?"
- "What's the worst-case scenario if we deploy this?"
- "How does this compare to industry standards?"
- "What would you do differently if you had more time?"
- "Can you walk us through your testing approach?"

Your documentation should give Gustavo confident answers to these questions.
