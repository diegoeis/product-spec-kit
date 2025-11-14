# STORY-001: {Action-Oriented Title}

**Related Epic**: {Epic Name from Plan}

## Context
{Background: why this story matters, how it fits into the epic, what the problem and how this solve it, related features}

**As a** {type of user}
**I want** {capability}  
**So that** {benefit/value delivered}

## Acceptance Criteria
{Remember the level difference of acceptance criteria of a PRD/Epic and Stories/Tasks cited in `SKILL.md`. Below follow the example.}

```
#### Authentication Flow
- When user clicks "Login" button on homepage, system displays login modal
- When user enters email in email field, system validates format in real-time
- When user enters invalid email format, system displays "Please enter a valid email" error below field
- When user enters password and clicks "Submit", system attempts authentication
- When authentication succeeds, system closes modal and redirects to dashboard
- When authentication fails, system displays "Invalid credentials" error above form
- When user clicks "Forgot Password" link, system displays password reset modal

#### Password Reset Flow
- When user enters email in reset form and clicks "Send Reset Link", system sends reset email
- When system sends email, system displays "Check your email for reset link" confirmation
- When user doesn't receive email within 1 minute, system shows "Resend Email" button
```

## Technical requirements

- **Implementation Guidance**: {Suggestions, not requirements}
- **Performance Requirements**: {If applicable}
- **Security Considerations**: {If applicable}
- **Data Requirements**: {If applicable}


## Edge Cases & Error Handling

1. **{Edge Case 1}**: {How system should handle}
2. **{Edge Case 2}**: {How system should handle}
3. **{Error Scenario}**: {User-friendly error message and recovery}

## Out of Scope

- {What this story explicitly does NOT include}
- {Features deferred to future stories}


### Design Assets

- {Link to mockups/wireframes}
- {Link to prototypes}
- {Link to design specs}
