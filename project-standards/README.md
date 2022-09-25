
# Project Standards

## Coding

### All code MUST use a linter and formatter:
- Rubocop for rails
- Prettier + ESLint for JavasScript / TypeScript
- Your IDE MUST run Linters on save (recommended to use Visual Studio Code)
- If you disable a linter rule (at the file level), you must comment why
- Pre-commit git hooks MUST block any commit with linter errors

### The linter/formatter settings must be the same across all projects
- Ruby projects MUST use the same Rubocop settings
- All TypeScript projects MUST use the same Prettier + ESLint settings
- All React  projects MUST use the same Prettier + ESLint settings

## Code Reviews

## Rails
- [Avoid/Remove n+1 queries](https://evilmartians.com/chronicles/how-to-graphql-with-ruby-rails-active-record-and-no-n-plus-one)
- API list operations built in [Relay Style](https://graphql-ruby.org/pagination/using_connections) - [More](https://graphql-ruby.org/pagination/stable_relation_connections)

## JavaScript:
- Convert to TypeScript

### TypeScript:
- No use of “any”
- Use arrow functions 
- - Bad: `function printWords(word) { console.log(word); }` 
- - Good: `const printWords = (word, word2) => console.log(word, word2);` 
- - Good: `const printWord = word => console.log(word);`
- Eliminate code duplication - extract to `utils` folder
- No “let” - use “const”
- Immutable - No array.push (use reduce)
- Immutable - No “forEach” (use map or reduce or filter)

### React
- Always use useCallback
- Split components into View and Container. 
- - View = pure functional component. No function definitions. No `return` statement.
- Follow Standard Code organization
- - https://capture.dropbox.com/BFWjvVkZ6UkeIgej
- - https://capture.dropbox.com/CIJYWFH2nbMjjiNE
- No Redux (use Context API, local state, Apollo)
- Use TypeScript instead of JavaScript
- Leverage design framework. Use theme file intensively and limit custom styles as much as possible.
- Define functions that don't need access to state OUTSIDE of render function
- Avoid/Eliminate class-based comonents (use functional components with hooks)
- Use useRef or (less preferably) useMemo on objects and arrays to prevent re-rendering
- [Profile code to find unnecessary re-renders](https://brycedooley.com/debug-react-rerenders/)

### Apollo
- Use typed-generated hooks (https://www.the-guild.dev/graphql/codegen/docs/guides/react#typed-hooks-for-apollo-and-urql)
- No use of “refetch”
- Only uses default fetch method (cache-first) https://www.apollographql.com/docs/react/data/queries/#setting-a-fetch-policy
- Avoid using .length on records when you mean “count”

### All APIs should:
- Be GraphQL-based. NOT REST!!!!
- Use TypeScript if written in Node/JavaScript

### All Tests should:
- Reference the ticket number they are addressing: I.e “#54 - As a user, I can comment on another user’s card”

### Dependencies
- Pull requests should be automatically created whenever there is an update for a project dependency (i.e. dependabot)
- Unless expressly determined, all dependencies should be kept current
- No dependency should be added to a project without lead approval

## Process

### All Deploys should:
- Run linters and block on error
- Automatically Update version number(s)
- Run tests and block on error
- Notify Appropriate Slack channels (success/failure)
- Be automatically evaluated for performance implications (i.e. Scout APM)
- Be triggered by git pushes to cooresponding git branch (i.e. push to dev deploys dev environment, push to staging deploy staging environment, etc)

### All production errors should:
- Be automatically created and a cooresponding ticket should be opened (i.e. Honeybadger, Sentry, etc)
- Be able to be ignored and thus not create repeated or duplicated tickets

### All Git commits should:
- Be atomic. One commit for each ticket
- Reference the ticket number they are addressing: i.e. “Closes #45” (this will automatically update the ticket)

### All Infrastructure should:
- Reside in an isolated AWS account (I.e. dev = AWS Account #1, staging = AWS Account #2)
- Automated and repeatable using a build tool such as CDK CDK - Never, ever, ever make a change via console or use a manual process to make changes!!!!!
- Have the least privileged access to individuals

### All Tickets should:
- Be created in GitHub (so project metrics are automated)
- Include effort points from developer

### All Documentation
- Must reside in Git/GitHub for easy reference to repositories
- Project specific documentation must be in the project repository
- Globalal documentation must be in the docs repository

### Meetings
- 15 minutes or less
- All meetings must have an agenda (No “Let’s meet to just talk about….”)

### Avoid Tools in Search of a Problem
- Tools (Slack, GitHub, Figma) can make a project run smoothly or de-rail one just as easily. 
- Tools should avoid duplication of work and solve a specific problem that can't be solved with the existing toolset.
- If a tool is added to a project, it must be thoroughly documented
