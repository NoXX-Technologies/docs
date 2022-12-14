
# Project Standards

## Coding

We strongly recommend the use of Visual Studio Code, however, we understand that choice of IDE can be a very personal choice.

So while we have the strongest knowledge and support for VSC, as long as your IDE supports the following, feel free to use it.

### All code MUST use a linter and formatter:
- Rubocop for rails
- Prettier + ESLint for JavasScript / TypeScript
- Your IDE MUST run Linters on save
- If you disable a linter rule (at the file level), you must comment why
- Pre-commit git hooks MUST block any commit with linter errors

### The linter/formatter settings must be the same across all projects
This should take the form of an ide settings file such as a `.vscode` directory in the project.
- Ruby projects MUST use the same Rubocop settings
- All TypeScript projects MUST use the same Prettier + ESLint settings
- All React  projects MUST use the same Prettier + ESLint settings

### Linter Setup for TypeScript React Projects
- "format" includes removing unused imports
- "format" includes sorting/organizating imports
- Code format on save (using prettier)
- Code format on paste (using prettier)
- Code format on commit (using husky + prettier)
- Code check format on commit (using husky + prettier + eslint)
- Block commit if format errors (using husky + prettier + eslint)
- Deploy fails if format errors (eslint + prettier + github actions) <=== Platform team handles this
- unused vars = error
- unused import = error
- incorrect dependencies in useEffect, useCallback, useMemo = error

#### Relevant Files and Folders

- .husky
- .vscode
- .eslintignore
- .eslintrc.json
- .prettierignore.json
- .prettierrc.json
- package.json
- tsconfig.json

#### [Sample Project](https://github.com/NoXX-Technologies/docs/files/10230323/sample.zip)

### DO NOT DISABLE LINTER RULES INLINE OR GLOBALLY. PERIOD. FIX YOUR SHIT. DON'T COVER IT WITH LEAVES

## Code Reviews

## Rails
- [Avoid/Remove n+1 queries](https://evilmartians.com/chronicles/how-to-graphql-with-ruby-rails-active-record-and-no-n-plus-one)
- API list operations built in [Relay Style](https://graphql-ruby.org/pagination/using_connections) - [More](https://graphql-ruby.org/pagination/stable_relation_connections)

## JavaScript
- Convert to TypeScript (rename .js to .ts/.tsx and fix errors)

### TypeScript
- No use of `any`
- Use arrow functions 
  - Bad: `function printWords(word) { console.log(word); }` 
  - Good: `const printWords = (word, word2) => console.log(word, word2);` 
  - Good: `const printWord = word => console.log(word);`
- Eliminate code duplication - extract to `utils` folder
- No `let` - use `const` only
- Immutable - No `array.push` (use `reduce`)
- Immutable - No `forEach` (use `map` or `reduce` or `filter`)
- Immutable - Prefer `Promise.all` and `Promise.then` to `async`/`await`
- Use descriptive function names with short, composed function bodies

### React
- Always use `useCallback`
- Split components into View and Container. 
  - View = pure functional component. No function definitions. No `return` statement.
- Follow Standard Code organization
  - https://capture.dropbox.com/BFWjvVkZ6UkeIgej
  - https://capture.dropbox.com/CIJYWFH2nbMjjiNE
- No Redux (use Context API, local state, Apollo)
- Use TypeScript instead of JavaScript
- Define functions that don't need access to state OUTSIDE of render function
- Avoid/Eliminate class-based comonents (use functional components with hooks)
- Use `useRef` or (less preferably) `useMemo` on objects and arrays to prevent re-rendering
- [Profile code to find unnecessary re-renders](https://brycedooley.com/debug-react-rerenders/)
- Do not use plain HTML. i.e. replace `<div>` with `<Box>`, replace `<img>` with `<Box component="img">`
- Limit the use of custom CSS/JSS. [Leverage Design Framework](https://www.figma.com/file/dwJuFGoZK3Ey2P3xg5mnuG/MUI---Beckett?node-id=4662%3A14)
  - Bad: {color: "#FF0000";}
  - Good: {color: theme.palette.error}
  - Bad: {margin: "4px";}
  - Good: {margin: 1}
  - Never use a color, font name, etc that is not defined in the theme. If it's in Figma, but not the theme file, add it. If it's not in figma, design must add it first

### Apollo
- [Use typed-generated hooks](https://www.the-guild.dev/graphql/codegen/docs/guides/react#typed-hooks-for-apollo-and-urql)
- No use of “refetch”
- [Only uses default fetch method (cache-first)](https://www.apollographql.com/docs/react/data/queries/#setting-a-fetch-policy)
- Avoid using .length on records when you mean “count”

### All APIs should:
- Be GraphQL-based. NOT REST!!!!
- Use TypeScript if written in Node/JavaScript

### All Tests should:
- Reference the ticket number they are addressing: I.e “#54 - As a user, I can comment on another user’s card”

### Dependencies (i.e. gems/npm)
- Pull requests should be automatically created whenever there is an update for a project dependency (i.e. dependabot)
- Unless expressly determined, all dependencies should be kept current
- No dependency should be added to a project without lead approval
- Use Bundler to manage Ruby dependencies
- Use Yarn to manage TypeScript dependencies

## Testing
- Minimum acceptable test coverage is 90%
- All tests should reference the GitHub issue number they address
- All tests should be run on deploy
- All tests should be run with push/pull request

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
- Have verifiable acceptance criteria 

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

### Version numbers must be visible to the end user
- This will greatly help in QA and bug reporting. Typically, the version, which may be comprised of both a frontend number and backend number, will reside in the footer of the frontend's UI.
