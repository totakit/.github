# Governance

## Project Structure

totakit is currently maintained by a single developer ([@nkr-ops](https://github.com/nkr-ops)). As the project grows, this governance model will evolve.

## Roles

| Role | Responsibilities | Current |
|------|-----------------|---------|
| Maintainer | Final say on all decisions, merges, releases | @nkr-ops |
| Contributor | Submit PRs, report issues, suggest features | Open to all |
| Paid Subscriber | Priority support, feature requests | [totakit.com/pricing](https://totakit.com/pricing) |

## Decision Making

### For code changes

- Bug fixes: Maintainer merges directly
- New features: Issue discussion → PR → review → merge
- Breaking changes: RFC in [rfcs repo](https://github.com/totakit/rfcs) → community feedback → decision

### For new tools

1. Community suggests via [New Tool Request](https://github.com/totakit/.github/blob/main/.github/ISSUE_TEMPLATE/new_tool_request.yml)
2. Maintainer evaluates feasibility, demand, and alignment
3. Accepted tools are added to the roadmap
4. Paid subscribers' requests are prioritized

### For architecture decisions

- Documented in the relevant repo's README or ARCHITECTURE.md
- Major decisions require an RFC with a 7-day comment period
- Maintainer has final authority

## Non-Negotiable Principles

These are not up for debate:

1. Files never leave the user's device
2. Developer tools (SDK, CLI) are MIT licensed
3. MCP server is proprietary (Developer/Fleet tiers)
3. No tracking of file content
4. No server-side processing of user files
5. Accessibility is a requirement, not a feature

## Conflict Resolution

1. Discussion in the relevant issue or PR
2. If unresolved, maintainer makes the final call
3. Decisions are documented with reasoning

## Future Governance

When totakit has 5+ regular contributors, we will:
- Establish a core team with commit access
- Create a formal RFC process
- Consider a steering committee for major decisions
- Publish a roadmap with community input

## Contact

- General: [hello@totakit.com](mailto:hello@totakit.com)
- Security: [security@totakit.com](mailto:security@totakit.com)
- Conduct: [conduct@totakit.com](mailto:conduct@totakit.com)
