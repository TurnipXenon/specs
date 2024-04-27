## Introduction

### Overview

Summary of the problem (from the perspective of the user), the context, suggested solution, and who are affected.

### Context

- Reasons why the problem is worth solving
- Origin of the problem
- How the problem affects our goals
- Past efforts made to solve the solution and why they were not effective
- How the product relates to our goals
- How the solution fits into the overall goals and strategies

### Requirements

- Product requirements in the form of user stories
- Technical requirements

### Out of scope

- Product and technical requirements that will be disregarded

### Future goals

Product and technical requirements slated for a future time

### Assumptions

Conditions and resources that need to be present and accessible for the solution to work as described.

### Current solution

- Current solution description
- Pros and cons of the current solution

### How does this subscribe to the Turnip Manifesto?

- See [Turnip's Game Dev Manifesto](./turnip-game-dev-manifesto.md)

## Proposed solution

### Solution overview

- External components that the solution will interact with and that it will alter
- Dependencies of the current solution
- Pros and cons of the proposed solution
- Diagram

### Dependencies

### Data Model / Schema Changes

- Schema definitions
- New data models
- Modified data models
- Data validation methods

### Business Logic

- API changes
- Pseudocode
- Flowcharts
- Error states
- Failure scenarios
- Conditions that lead to errors and failures
- Limitations

### Presentation Layer

- User requirements
- UX changes
- UI changes
- Wireframes with descriptions
- Links to UI/UX designer’s work
- Mobile concerns
- Web concerns
- UI states
- Error handling

### Other questions to answer

- How will the solution scale?
- What are the limitations of the solution?
- How will it recover in the event of a failure?
- How will it cope with future requirements?

## Plan

### Testing

- Explanations of how the tests will make sure user requirements are met
- Unit tests
- Integrations tests
- QA

#### Local testing

#### Dev stack testing

### Monitoring and Alerting Plan

- Logging plan and tools
- Monitoring plan and tools
- Metrics to be used to measure health
- How to ensure observability
- Alerting plan and tools

### Release / Roll-out and Deployment Plan

- Deployment architecture
- Deployment environments
- Phased roll-out plan e.g. using feature flags
- Plan outlining how to communicate changes to the users, for example, with release notes

### Workflow

- Testing locally
- Testing dev stack
- Pushing to staging
- Promoting staging to production
- Runbooks
- Onboarding guide

### Rollback Plan

- Detailed and specific liabilities
- Plan to reduce liabilities
- Plan describing how to prevent other components, services, and systems from being affected

## Alternate Solutions / Designs

- Short summary statement for each alternative solution
- Pros and cons for each alternative
- Reasons why each solution couldn’t work
- Ways in which alternatives were inferior to the proposed solution
- Migration plan to next best alternative in case the proposed solution falls through

## Further Considerations

### Impact on other people

- How will this increase the work of other people?
- How will this increase my work on other projects?

### Third-party services and platforms considerations

- Is it really worth it compared to building the service in-house or using someone else's?
- What are some of the security and privacy concerns associated with the services/platforms?
- How much will it cost?
- How will it scale?
- What possible future issues are anticipated?

### Cost analysis

- What is the cost to run the solution per day?
- What does it cost to roll it out?

### Security considerations

- What are the potential threats?
- How will they be mitigated?
- How will the solution affect the security of other components, services, and systems?

### Privacy considerations

- Does the solution follow local laws and legal policies on data privacy?
- How does the solution protect users’ data privacy?
- What are some of the tradeoffs between personalization and privacy in the solution?

### Regional considerations

- What is the impact of internationalization and localization on the solution?
- What are the latency issues?
- What are the legal concerns?
- What is the state of service availability?
- How will data transfer across regions be achieved and what are the concerns here?

### Accessibility considerations

- How accessible is the solution?
- What tools will you use to evaluate its accessibility?

### Operational considerations

- Does this solution cause adverse aftereffects?
- How will data be recovered in case of failure?
- How will the solution recover in case of a failure?
- How will operational costs be kept low while delivering increased value to the users?

### Risks

- What risks are being undertaken with this solution?
- Are there risks that once taken can’t be walked back?
- What is the cost-benefit analysis of taking these risks?

### Support considerations

- How will the support team get across information to users about common issues they may face while interacting with the changes?
- How will we ensure that the users are satisfied with the solution and can interact with it with minimal support?
- Who is responsible for the maintenance of the solution?
- How will knowledge transfer be accomplished if the project owner is unavailable?

## Success Evaluation

### Impact

- Security impact
- Performance impact
- Cost impact
- Impact on other components and services

### Metrics

- List of metrics to capture
- Tools to capture and measure metrics

## Work

### Work estimates and timelines

- List of specific, measurable, and time-bound tasks
- Resources needed to finish each task
- Time estimates for how long each task needs to be completed

### Prioritization

- Categorization of tasks by urgency and impact

### Milestones

- Dated checkpoints when significant chunks of work will have been completed
- Metrics to indicate the passing of the milestone

### Future work

- List of tasks that will be completed in the future

## Deliberation

### Discussion

- Elements of the solution that members of the team do not agree on and need to be debated further to reach a consensus.

### Open Questions

- Questions about things you do not know the answers to or are unsure that you pose to the team and stakeholders for their input. These may include aspects of the problem you don’t know how to resolve yet.

## Appendix

### Glossary

- Definition for specific terms

### Major Revisions

After a 1.0 release, maybe add revision notes here

### References

- Template from: [A practical guide to writing technical specs - Stack Overflow Blog](https://stackoverflow.blog/2020/04/06/a-practical-guide-to-writing-technical-specs/)
- [Top three considerations when documenting a microservice | Official Pythian®® Blog](https://blog.pythian.com/top-three-considerations-documenting-microservice/)

## Document Changelogs

- 2024-04-26: Created tech-spec-template.md
