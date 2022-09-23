# Docs

Welcome to NOXX's collection of documentation!

Who ever thought documentation could be this fun, right?

Anyway, the main page here acts as an index into specific levels of documentation.

************ STOP *****************

Is something missing or off?

Does something not work like the documentation says it should?

Don't keep going! Fix/add it! Or contact Cody and he'll fix/add it!

[Please check back often for updates and changes!](https://github.com/NoXX-Technologies/docs/commits/main)

## Everybody
- [Project Management Process](process/README.md)
## Developers
- [Severless Services](developers/services/README.md)
- [Global Infrastructure](https://github.com/NoXX-Technologies/infrastructure)
- [React](https://github.com/NoXX-Technologies/react-frontend)
- [Rails](https://github.com/NoXX-Technologies/rails)
- Workstation Setup (TODO)
- [Common Access Requirements](onboarding/README.md)

## Designers

- [Common Access Requirements](onboarding/README.md)

## QA

- [Common Access Requirements](onboarding/README.md)

## Project Managers

- [Common Access Requirements](process/README.md)

## Standards

### Coding

#### All code MUST use a linter and formatter:
- Rubocop for rails
- Prettier + ESLint for JavasScript / TypeScript
- Your IDE MUST run Linters on save (recommended to use Visual Studio Code)
- If you disable a linter rule (at the file level), you must comment why
- Pre-commit git hooks MUST block any commit with linter errors

#### The linter/formatter settings must be the same across all projects
- Ruby projects MUST use the same Rubocop settings
- All TypeScript projects MUST use the same Prettier + ESLint settings
- All React  projects MUST use the same Prettier + ESLint settings

### Code Reviews

#### TypeScript:
- No use of “any”

#### JavaScript/TypeScript:
- No “let” - use “const”
- Immutable - No array.push (use reduce)
- Immutable - No “forEach” (use map or reduce or filter)

#### React
- Always use useCallback
- View/Container split. View = pure functional component
- No Redux (use Context API, local state, Apollo)

#### Apollo
- Use typed-generated hooks (https://www.the-guild.dev/graphql/codegen/docs/guides/react#typed-hooks-for-apollo-and-urql)
- No use of “refetch”
- Only uses default fetch method (cache-first) https://www.apollographql.com/docs/react/data/queries/#setting-a-fetch-policy
- Avoid using .length on records when you mean “count”

#### APIs
- No REST. Create GraphQL APIs

#### All Tests should:
- Reference the ticket number they are addressing: I.e “#54 - As a user, I can comment on another user’s card”

### Process

#### All Deploys should:
- Run linters and block on error
- Automatically Update version number(s)
- Run tests and block on error
- Notify Appropriate Slack channels (success/failure)


#### All Git commits should:
- Be atomic. One commit for each ticket
- Reference the ticket number they are addressing: i.e. “Closes #45” (this will automatically update the ticket)

#### All Infrastructure should:
- Reside in an isolated AWS account (I.e. dev = AWS Account #1, staging = AWS Account #2)
- Automated and repeatable using a build tool such as CDK CDK - Never, ever, ever make a change via console or use a manual process to make changes!!!!!
- Have the least privileged access to individuals

#### All Tickets should:
- Be created in GitHub (so project metrics are automated)
- Include effort points from developer

#### All Documentation
- Must reside in Git/GitHub for easy reference to repositories
- Project specific documentation must be in the project repository
- Globalal documentation must be in the docs repository

#### Meetings
- 15 minutes or less
- All meetings must have an agenda (No “Let’s meet to just talk about….”)


