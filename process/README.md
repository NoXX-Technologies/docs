# NoXX Process Guide


This guide should serve as the go-to resource for all operations on the Becket Collect project. Please review carefully and adhere to the best practices outlined here. If you encounter a situation that is not covered in this guide, please alert Krish or Cody who will answer your question and update this document accordingly.

With each change, the version number should be bumped above, so you’ll always know if there have been changes since your last review.

### Under Construction ###

This document is in the process of being separated and updated to address specific roles within the Beckett family.

Additionally, some items in this document refer to working with our legacy Heroku/Netlify stack which is being phased out with our ongoing migration to AWS.


## “Good software development is not a reactive, chaotic endeavor. Too often, teams mistake ‘busy’ for ‘productive’. Instead productivity in software development comes from a proactive, consistent and methodical approach.” -DHH 


## Goals



1. Give developers an environment to work unencumbered by distractions in which they can develop rapidly without fear of breaking the end-user’s experience
2. Allow developers to work at their own pace while providing them the tools, process and trainings to accomplish more in the same amount of time
3. Understand how changes affect the underlying system and be able to repair or rollback negative changes quickly
4. Focus on important tasks while minimizing urgent tasks
5. Rigorously track effort and velocity so we can provide accurate estimations 




# Iterations


## GitHub Integration

All Milestones should be named after the start date of the iteration in the following format YYYY-mm-dd, i.e. 2022-06-07.

Each repo (React, Rails, etc) should have a milestone created.

This responsibility falls on the project manager.


## Schedule

Please note - while every day in the iteration (including weekends) has a schedule, we do not expect everyone to work seven days a week. Nor do we enforce any set schedule for when to work (i.e. 9-5). We just expect that, if you are working on a given day, you follow the schedule for that day.

Additionally, all team members will be invited to calendar items to provide additional reminders


### **Day 1: First Wednesday**


#### All



* Groom Backlog
* IPM


#### Project Manager



* Create new Iteration Milestones in GitHub
* Close Iteration Milestones (and move any open tickets to the next Milestone)


#### Lead Developer



* Deploy Rails to production (if QA approved)
* Deploy React to production (if QA approved)
* Answer any developer questions on slack


#### Developers



* [Work on assigned tickets for the iteration](https://github.com/orgs/NoXX-Technologies/projects/2/views/1)
* Start of development phase of the iteration


### **Day 2: First Thursday**


#### Lead Developer



* Answer any developer questions on slack


#### Developers



* [Work on assigned tickets for the iteration](https://github.com/orgs/NoXX-Technologies/projects/2/views/1)


### **Day 3: First Friday**


#### Lead Developer



* Answer any developer questions on slack


#### Developers



* [Work on assigned tickets for the iteration](https://github.com/orgs/NoXX-Technologies/projects/2/views/1)


### **Day 4: First Saturday**


#### Lead Developer



* Answer any developer questions on slack


#### Developers



* [Work on assigned tickets for the iteration](https://github.com/orgs/NoXX-Technologies/projects/2/views/1)


### **Day 5: First Sunday**


#### Lead Developer



* Answer any developer questions on slack


#### Developers



* [Work on assigned tickets for the iteration](https://github.com/orgs/NoXX-Technologies/projects/2/views/1)


### **Day 6: First Monday**


#### Lead Developer



* Answer any developer questions on slack


#### Developers



* [Work on assigned tickets for the iteration](https://github.com/orgs/NoXX-Technologies/projects/2/views/1)
* **Submit branches for review by 11:59 pm EST. If your branch is not submitted by then, it will not be included in the iteration deploy. PENCILS DOWN!**


### **Day 7: First Tuesday**


#### Lead Developer



* Answer any developer questions on slack
* Conduct Code Reviews
* Conduct Dependency analysis (Security Audit)
* Merge developer (and dependabot) branches into main branch
* Deploy Rails to Staging
* DeployReact to Staging


#### Developers



* [Work on assigned tickets for the iteration](https://github.com/orgs/NoXX-Technologies/projects/2/views/1)


### **Day 8: Second Wednesday**


#### QA



* Acceptance Testing
* Regression Testing


#### Lead Developer



* Answer any developer questions on slack


#### Developers



* [Fix any regression bugs from QA](https://github.com/orgs/NoXX-Technologies/projects/2/views/7)
* [Fix any rejected tickets from QA](https://github.com/orgs/NoXX-Technologies/projects/2/views/7)
* If lack of regression/rejection, start on next iteration tickets
* Start of fixes phase of the iteration


### **Day 9: Second Thursday**


#### QA



* Acceptance Testing
* Regression Testing


#### Lead Developer



* Answer any developer questions on slack


#### Developers



* [Fix any regression bugs from QA](https://github.com/orgs/NoXX-Technologies/projects/2/views/7)
* [Fix any rejected tickets from QA](https://github.com/orgs/NoXX-Technologies/projects/2/views/7)
* If lack of regression/rejection, start on next iteration tickets


### **Day 10: Second Friday**


#### QA



* Acceptance Testing
* Regression Testing


#### Lead Developer



* Answer any developer questions on slack
* Analyze performance reports from latest staging deploy


#### Developers



* [Fix any regression bugs from QA](https://github.com/orgs/NoXX-Technologies/projects/2/views/7)
* [Fix any rejected tickets from QA](https://github.com/orgs/NoXX-Technologies/projects/2/views/7)
* If lack of regression/rejection, start on next iteration tickets


### **Day 11: Second Saturday**


#### QA



* Acceptance Testing
* Regression Testing


#### Lead Developer



* Answer any developer questions on slack
* Use performance analysis to optimize any problem areas


#### Developers



* [Fix any regression bugs from QA](https://github.com/orgs/NoXX-Technologies/projects/2/views/7)
* [Fix any rejected tickets from QA](https://github.com/orgs/NoXX-Technologies/projects/2/views/7)
* If lack of regression/rejection, start on next iteration tickets


### **Day 12: Second Sunday**


#### QA



* Acceptance Testing
* Regression Testing


#### Lead Developer



* Answer any developer questions on slack
* Use performance analysis to optimize any problem areas


#### Developers



* [Fix any regression bugs from QA](https://github.com/orgs/NoXX-Technologies/projects/2/views/7)
* [Fix any rejected tickets from QA](https://github.com/orgs/NoXX-Technologies/projects/2/views/7)
* If lack of regression/rejection, start on next iteration tickets


### **Day 13: Second Monday**


#### QA



* Acceptance Testing
* Regression Testing


#### Lead Developer



* Answer any developer questions on slack
* Use performance analysis to optimize any problem areas


#### Developers



* [Fix any regression bugs from QA](https://github.com/orgs/NoXX-Technologies/projects/2/views/7)
* [Fix any rejected tickets from QA](https://github.com/orgs/NoXX-Technologies/projects/2/views/7)
* If lack of regression/rejection, start on next iteration tickets


### **Day 14: Second Tuesday**


#### QA



* Acceptance Testing
* Regression Testing


#### Lead Developer



* Answer any developer questions on slack
* Use performance analysis to optimize any problem areas


#### Developers



* [Fix any regression bugs from QA](https://github.com/orgs/NoXX-Technologies/projects/2/views/7)
* [Fix any rejected tickets from QA](https://github.com/orgs/NoXX-Technologies/projects/2/views/7)
* If lack of regression/rejection, start on next iteration tickets




# Coding Guide

The following contains a few best practices for coding on the project


## Rails



1. [Avoid/Remove n+1 queries](https://evilmartians.com/chronicles/how-to-graphql-with-ruby-rails-active-record-and-no-n-plus-one)
2. Use cursor based pagination connections from graphql gem when building unbounded arrays


## React



1. Standardize component hierarchy

    - Card


    -- Detail


    --- CardDetailView.tsx


    --- CardDetailContainer.tsx 


    --- CardDetailStyles.ts


    -- List


    --- CardListView.tsx


    --- CardListContainer.tsx 


    --- CardListStyles.ts


    --- Item


    ---- CardListItemView.tsx


    ---- CardListItemContainer.tsx 


    ---- CardListItemStyles.ts

2. Split all components into View/Container/Styles
    1. View: Pure Functional component. No variable assignments, no return statements. In an MVC, think of the View as the View.
    2. Container: Gathers data and defines UI handlers. In MVC, think of this as the Controller
    3. Styles: The JSS for the View
3. If you’re working on a Javascript (.js) file, convert it to a TypeScript (.tsx) file.
4. Don’t use “let” for variable assignment (use const)
5. Use arrow functions
    4. Bad: `function printWords(word) { console.log(word); }`
    5. Good: `const printWords = (word, word2) => console.log(word, word2);`
    6. Good: `const printWord = word => console.log(word);`
6. If a component is rendered in a loop, the name of the file should end in “Item.tsx”, i.e “CardListItemContainer.tsx and CardListItemView.tsx”
7. `useQuery` should not appear in any Item.tsx file (meaning, no queries should be made in a loop. This avoids n+1 requests)
8. Fix all warnings - especially unused import/var
9. Remove all queries.js, fragments.js and mutations.js and replace with __generated__ technique. See below:
    7. [https://www.apollographql.com/blog/graphql/fragments/using-graphql-fragments-for-safer-cleaner-and-faster-code/](https://www.apollographql.com/blog/graphql/fragments/using-graphql-fragments-for-safer-cleaner-and-faster-code/)
    8. [https://www.apollographql.com/blog/tooling/apollo-codegen/typescript-graphql-code-generator-generate-graphql-types/](https://www.apollographql.com/blog/tooling/apollo-codegen/typescript-graphql-code-generator-generate-graphql-types/)
10. Put all reused functions into their own file in utils directory and import them
11. Put all reused constant variables into const directory and import them
12. Define functions outside of the component body if it doesn’t depend on state
13. Use useCallback for all functions defined within a component body
14. Use useRef or (less preferably) useMemo on objects and arrays to prevent re-rendering
15. [Profile code to find unnecessary re-renders](https://brycedooley.com/debug-react-rerenders/)




# Ticket Management Guide

The following are guidelines for the QA team and outline best practices for creating tickets. It also spells out how the developers should respond.

Some general rules:



1. If developers can’t reproduce it in staging, they probably can’t fix it, so please provide replicable steps in your tickets.
2. Please note the version number in your tickets


## Hotfix

Something critical to the function of the app (blocking users) is broken on production and we need to fix it asap.

Open a defect issue for the current iteration and label it “hotfix”.

Additionally, notify the development team in Slack.

Developers should follow the process outline in the Hotfixes section to fix and, when closing the ticket, note the version number in which it is fixed


## Regression

A regression is a type of bug that appears on staging and not production. 

In order to prevent the bug from making it to production, open a defect ticket in the current iteration and label it “regression”.

Since regressions are fixed directly on staging branch and deployed without review, developers must note the version number in which the fix occurred as a comment when closing the ticket.


## Bug

A bug is something that doesn’t work in staging or in production and would not be considered a hotfix.

For these, open a new defect ticket and don’t assign a milestone (i.e., leave it in the backlog).


## Feature

A feature is a request for anything new. This could be a new product feature (As a user, I want to login with my phone number, so I don’t need to monitor my email) or a new chore (Change color of header to red).


# Git Branch Management

This section is for developers only



1. At the beginning of each iteration, create a new branch off of “main” using the following format:  \
`&lt;developer_name>/&lt;iteration start date in YYYY-mm-dd>`
2. For each issue, commit changes using the following format:  \
`$ git commit -am "closes #issue-number"`
3. By Monday at 11:59 PM (**Pencils Down)**, submit a pull request with this branch to “main” branch
4. **Lead Developer Only**: Review pull requests and either accept and merge or assign back to developer for changes.
5. Make any changes requested during code review to your iteration branch and resubmit a pull request to main
6. After approved, delete iteration branch from your local git repository.
7. **Lead Developer Only**: Once all pull requests are approved and merged into main, check out staging branch and merge main into staging. 
8. **Lead Developer Only**: Staging Deploy
    1. Rails: `$ scripts/deploy `
    2. React: `$ yarn deploy`
    3. When prompted, select “minor” for update type, which will create a new Git tag and create a GitHub release
9. Pull changes from staging branch into your local staging branch
10. During Acceptance Testing, Regression Testing, Code Fixes, make your changes directly on staging branch, commit them, pull for any changes and deploy directly (no code review) 
    4. Rails: `$ scripts/deploy `
    5. React: `$ yarn deploy`
    6. When prompted, select “patch” for update type, which will create a new Git tag and create a GitHub release
11. **Lead Developer Only**: Following IPM, if we get thumbs up for production deploy, checkout production branch, pull for any changes, merge staging into production and deploy.
    7. Rails: `$ scripts/deploy `
    8. React: `$ yarn deploy`
    9. When prompted, select “none” for update type
12. **Lead Developer Only**: Following deploy, checkout main branch and merge production into main and push changes to main

**PLEASE NOTE: Only the lead developer should EVER merge code into the main branch.**


## Hotfixes

If something is caught during regression that is ALSO broken currently on production and is a blocker, it needs to be hotfixed to prod immediately.

Example: During staging regression you find out someone can't upload a card photo. You're like "oh shit. Let me see if this works on prod" and it doesn't. 

Of course, that doesn't need to wait to be fixed on prod. That needs to be fixed immediately.

To do that, check out the production branch and make the fix directly on production. Then deploy with the following:



1. Rails: `$ scripts/deploy `
2. React: `$ yarn deploy`
3. When prompted, select “patch” for update type, which will create a new Git tag and create a GitHub release
4. Checkout staging branch, merge production into staging. Push staging to remote
5. Checkout main branch, merge production into main. Push main to remote

This is the only case in which the code should be written directly on the production branch and deployed with a patch version update.


## Deploying

The deploy process is described sporadically throughout the document, but is consolidated here.

Staging deploys occur on the first Tuesday of the iteration, following code review and branch mergers from the lead developer.

This deploy gets a minor (major.minor.patch) version update. There is only one minor version (for each Rails and React) update per iteration.

**Rails**


```
$ scripts/deploy # select "minor"
```


**React**


```
$ yarn deploy # select "minor"
```


This marks the end of the development phase of the iteration and the start of the fixes phase of the iteration.

During the fixes phase of the iteration, developers work directly on the staging branch and deploy a patch (major.minor.patch) version update with each fix.

Prior to deploying, the developer should pull from staging to make sure there isn’t a conflict.

**Rails**


```
$ git checkout staging; git pull; scripts/deploy # select "patch"
```


**React**


```
$ git checkout staging; git pull; yarn deploy # select "patch"
```


As opposed to the minor update, there will be multiple patch updates (one for each fix).

During the IPM on Wednesday, the team decides whether the code is ready for a production deploy.

If so, the lead developer merges staging into production and deploys WITHOUT a version update. 

**Rails**


```
$ git checkout production; git pull; git merge staging; scripts/deploy # select "none"
```


**React**


```
$ git checkout production; git pull; git merge staging; yarn deploy # select "none"
```


**Note: the backend and frontend version numbers are displayed in the footer of the web app**




# Third Party Tools

Below is a list of third party tools and integrations we use to assist us with our process.

If you need access to any of these tools, please let Cody or Krish know.


## Scout APM

Scout APM records performance metrics for the Rails API and Postgres database.

We use these metrics after QA finishes their testing each iteration to compare performance from one iteration to the next.


## HotJar

HotJar records user sessions and we use it, in conjunction with Google Analytics, to analyze usability problems with the app.

For example, if we are noticing a high drop off at a certain point in a GA Funnel, we can use HotJar to see why users aren’t completing a particular step in the GA Funnel.


## Honeybadger

Honeybadger captures and tracks backend errors in the Rails API and creates GitHub tickets for us so we can triage them.


## Loadster

Loadster allows the QA team to records interactions and user stories and then play them back in the browser repeatedly while collecting render and load metrics.

We use this to determine if there have been positive or negative gains in performance from iteration to iteration.


## Cypress.io

Cypress.io provides a dashboard for stakeholders to see metrics on our end-to-end tests, including speed metrics and code coverage as well as what tests are not passing.

This is updated every time code is committed to the GitHub repo.


## Log Rocket

Log Rocket captures and tracks front-end errors in production and creates GitHub tickets for them so the developers can triage them.


## Google Analytics

Stakeholders use Google Analytics to analyze standard metrics and use them to guide product decisions and UI/UX optimizations.


## Slack

Slack is our main form of communication among the team with several automated integrations, including GitHub, Cypress and more.




# Roles


## Project Manager

Dan Stern

Adrian Colon


## QA

Dan Stern

Adrian Colon


## Lead Developer / Code Owner

Cody Swann


## Technical Director

Krish Dasgupta


## Developer

Cody Swann

David Etkin

Dary Merckens

Tim Brand

Tony Ye


# 


# Terms and Definitions


## Pencils Down

This is a term we use to describe branch submission deadline, which is 11:59 PM EST on the first Tuesday of the iteration. Any branch that is not submitted for review by then will be excluded from the deploy.


## IPM

IPM is an Iteration Planning Meeting and they are held at the start of each iteration.

The agenda for each IPM is as follows:



* Are we good to deploy to production?
* Any clarification needed on tickets?
* How many Effort Points did the team close last iteration?
* What is the team’s velocity now?
* Have developers reached their allotment of tickets?
* Do all assigned tickets have effort points?
* Any news or announcements?


## Effort Points

Effort Points is a relative number used to denote how difficult a ticket is to complete for a specific developer (each developer sets their own effort points).

It’s kind of a combination of estimated time and difficulty on the following scale: 1, 2, 4, 8, 16, 32

If a ticket is estimated at more than 32 effort points, it should be broken down into multiple smaller tickets.


## Velocity

The team as a whole, as well as each developer has what’s called a Velocity Score, which is the total number of effort points that can be accomplished in a single iteration.

At the end of each iteration, sum up all the effort points for the team and for each developer and you get the velocity score for that particular iteration.

However, the single iteration velocity score is not very useful, instead, the overall velocity score for the team and developers is important.

This is simply adding up the iteration velocity scores and dividing by the number of iterations.

This tells you, on average, how many effort points the team and each developer can be expected to complete each iteration.

**Very important: **The goal is not to see how many effort points you can close in a single iteration. It’s to get a true, working score which can be used for estimation purposes. It’s ok if you get sick or take a vacation or something comes up. There is no need to cram. In fact, it hurts to do so!


## Regression Testing

Regression testing is the process of using the site as an end user to see if anything that previously was working no does not work.

This is part of QA’s responsibility with the aid of Cypress which we use for end-to-end integration testing.

The following are some guidelines for regression testing:



1. Only include one item in each ticket. For example, if you view the home page and notice two new bugs, open two separate tickets - one for each bug.
2. if it’s broke on staging, does it work on prod? And vice versa, If you’re reporting something on production, please try to provide a reproducible example on staging so the developers can replicate it.
3. If a regression is found that works on production but not staging, it needs to be assigned to a developer and fixed during the Acceptance Testing, Regression Testing, Code Fixes portion of the schedule. OTHERWISE, it should be assigned to the backlog or the next iteration depending on severity.
4. Please include the version number and environment in the ticket. **Note: the backend and frontend version numbers are displayed in the footer of the web app**
5. When submitting a regression bug, assume the developer will know nothing about the specific area. I.e., instead of submitting: “I get an error when I try to upload a card”, file something like this:
    1. Go to beta.noxx.com
    2. Sign in if you’re not signed in already
    3. Click “Add Cards”
    4. Fill in form
    5. Hit submit
    6. Expected: I see the details of the card I just added
    7. Actual: Nothing happens
    8. **TODO: Update our ticket templates on Github**


## Acceptance Testing

Acceptance Testing is the process of making sure new features work as they were intended to.

This is one of QA’s responsibilities.

The following are guidelines for acceptance testing:



1. Does the request work as it is spelled out in the ticket but it needs changes? 
    1. If so, the ticket should be accepted and a change request should be opened in the form of a new ticket for the next iteration.
    2. Example: Change title font size to 48px. If the font size is 48px, but upon seeing it, you also think the font color should be changed from black to blue, this is NOT a rejection. Accept the ticket and open a new ticket to change the color to blue
2. Does the request NOT work as it is spelled out in the ticket?
    3. The ticket should be rejected and the developer should fix it during the Acceptance Testing, Regression Testing, Code Fixes portion of the schedule
    4. Example: Change title font size to 48px. If the font size is 40px, reject the ticket and explain why you rejected it.
3. When rejecting a ticket, please be as specific as possible and include all steps the developer needs to reproduce in order to replicate the error/rejection


## Backlog Grooming

For more information, see [Backlog Grooming](https://www.productplan.com/glossary/backlog-grooming/)


### QA

Review tickets to make sure they are still valid. Check priorities and adjust if necessary.


### Developers

Review tickets to see which ones are appropriate for you and assign them to you if they are. If you assign a ticket to yourself, add effort points.


# FAQs


## How do I know what the latest version should be?

First, check the app on the environment in question. The version number will be in the footer of the app and look like this: version 0.10.2 / 0.12.0 where the backend version is first, followed by the frontend version.

Check these against the version numbers in the package.json files in the respective Rails and React repo (keeping in mind to check the right branch, i.e. staging/production). If they are different, then a deploy failed.

For the backend, check the “Actions” tab on the Rails repo.

For the frontend, check the Netlify logs 