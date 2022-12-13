# Onboarding

Onboarding documenation will guide a new hire from noob to contributing hero as quickly as possible.

We have broken this section down by role and cover everything from access, equipment and education.

The relevant roles are [reflected as teams in the GitHub organization](https://github.com/orgs/NoXX-Technologies/teams) and explained below.

Please do not complain about not understanding the tech stack if you have not read and understand the education material listed below.

To be clear, we are not requiring frontend developers to educate themselves on backend material and vice versa. In fact, if you're not a backend developer, you should not be concerned with how the backend works (and vice versa).

## Frontend Developers
Frontend Developers work primarily in React to build customer-facing clients that connect to backend technologies
## Backend Developers
Backend Developers create microservices that power, create, format and serve data to numerous front-end clients.

## Platform Developers
Platform Developers are NoOps engineers who automate Operations into PaaS and FaaS that host the services and clients built by the backend and frontend developers. This role also creates CI/CD pipelines as well as local development setups. Essentially, the Platform Developers' job is to make sure the Frontend Developers and Backend Developers only need to worry about creating application business logic.

### Onboarding Checklist

Below is a list of items you'll need/need access to. Further down, you'll find the owner for each item - contact them for the item.

#### Platform Developers
- [ ] Corporate Laptop
- [ ] Signed Offer Letter
- [ ] Signed Employee Docs
- [ ] Benefits Selection
- [ ] AWS (AdministratorAccess Access)
- [ ] GitHub Organization (Admin Role for each Repo)
- [ ] Miro
- [ ] Slack
- [ ] Office 365
- [ ] Google Workspace
- [ ] Serverless Framework
- [ ] Scout APM
- [ ] Honeybadger
- [ ] Loadster
- [ ] Cypress.io
- [ ] Figma

#### Backend Developers
- [ ] Corporate Laptop
- [ ] Signed Offer Letter
- [ ] Signed Employee Docs
- [ ] Benefits Selection
- [ ] GitHub Organization (Write Role for each Repo)
- [ ] Miro
- [ ] Slack
- [ ] Office 365
- [ ] Google Workspace
- [ ] Serverless Framework
- [ ] Scout APM
- [ ] Honeybadger
- [ ] Figma

#### Frontend Developers
- [ ] Corporate Laptop
- [ ] Signed Offer Letter
- [ ] Signed Employee Docs
- [ ] Benefits Selection
- [ ] GitHub Organization (Write Role for each Repo)
- [ ] Miro
- [ ] Slack
- [ ] Office 365
- [ ] Google Workspace
- [ ] Cypress.io
- [ ] LogRocket
- [ ] Figma

#### Project Managers
- [ ] Corporate Laptop
- [ ] Signed Offer Letter
- [ ] Signed Employee Docs
- [ ] Benefits Selection
- [ ] GitHub Organization (Read Role for each Repo)
- [ ] Miro
- [ ] Slack
- [ ] Office 365
- [ ] Google Workspace
- [ ] Figma
- [ ] Google Analytics
- [ ] Notion

#### Quality Assurance Specialists
- [ ] Corporate Laptop
- [ ] Signed Offer Letter
- [ ] Signed Employee Docs
- [ ] Benefits Selection
- [ ] GitHub Organization (Read Role for each Repo)
- [ ] Miro
- [ ] Slack
- [ ] Office 365
- [ ] Google Workspace

## Project Managers
Project Managers are responsible for running iterations and IPMs. Additionally, project managers are responsible for estimation and timeline creation using a team's velocity.

## Product Managers
Product Managers create functional requirements with acceptance criteria which Project Managers used to prioritize and fill sprints.

## Quality Assurance Specialists
Quality Assurance Specialists ensure that the acceptance criteria created by the Product Managers are met. Additionally, this role is responsible for finding any regressions prior to production deployments.
## Access

This is a list of services and tools you'll need access to, along with what it's used for and whom to contact to get access.

### Noxx GitHub Organization
Used for:
- Code Management
- Project Management
- CI/CD

Owner: Krish Dasgupta

Used by: Everyone


### Slack
Used for:
- Team Communication
- Various Notifications (deployments, etc)

Owner: Krish Dasgupta

Used by: Everyone

### Miro
Used for: Data Prototyping

Owner: Krish Dasgupta

Used by: Everyone

### Figma
Used for: Design Mockups

Owner: Krish Dasgupta

Used by: Everyone

### Office 365
Used for: 
- Document Management
- Email
- Video Conferencing

Owner: ???

Used by: Everyone

### Google Workspace 
Used for: 
- Document Management
- Email
- Video Conferencing

Owner: Krish Dasgupta

Used by: Everyone

### Google Analytics 
Used for: 
- A/B Testing
- Product Useage Data

Owner: ???

Used by: Project Manager

### Notion
Used for: 
- Product documentation

Owner: ???

Used by: Project Manager


### Serverless Framework 
Used for: Deploying and Monitoring Micro Services

Owner: Krish Dasgupta

Used by: 
- Frontend Developers
- Backend Developers
- Platform Developers


### HotJar

HotJar records user sessions and we use it, in conjunction with Google Analytics, to analyze usability problems with the app.

For example, if we are noticing a high drop off at a certain point in a GA Funnel, we can use HotJar to see why users aren’t completing a particular step in the GA Funnel.

Owner: ???

Used By:
- Frontend Developers
- Product Managers

### [Scout APM](https://scoutapm.com/)
Used for: Performance Monitoring

Owner: Krish Dasgupta

Used By:
- Backend Developers
- Platform Developers


### [Honeybadger](https://www.honeybadger.io/)
Honeybadger captures and tracks backend errors in the Rails API and creates GitHub tickets for us so we can triage them.

Used for: Error Monitoring

Owner: Krish Dasgupta

Used By:
- Backend Developers
- Platform Developers
- Project Managers

### [LogRocket](https://logrocket.com/)

Log Rocket captures and tracks front-end errors in production and creates GitHub tickets for them so the developers can triage them.

Used for: Error Monitoring

Owner: Krish Dasgupta

Used By:
- Frontend Developers
- Platform Developers
- Project Managers



### AWS 
Used for: Building, Managing and Hosting Platform Infrastructure

Owner: ???

Used By:
- Platform Developers

### [Loadster](https://loadster.app/)

Loadster allows the QA team to records interactions and user stories and then play them back in the browser repeatedly while collecting render and load metrics.

We use this to determine if there have been positive or negative gains in performance from iteration to iteration.

Owner: Krish Dasgupta

Used By:
- Platform Developers
- Backend Developers
- Quality Assurance Specialists

### [Cypress.io](https://www.cypress.io/)

Cypress.io provides a dashboard to see metrics on our end-to-end tests, including speed metrics and code coverage as well as what tests are not passing.

This is updated every time code is committed to the GitHub repo.

Used By:
- Frontend Developers
- Project Managers

## Education

This section descriptions a list of tools, technologies and processes that various roles should be familiar with.

Additionally, each role will have a required level of knowledge of each ranging from novice to advanced.

### [Project Management and Deveopment](../process/README.md)

Used By:
- Everyone - Advanced

### GraphQL

Used By:
- Frontend Developers - Advanced
- Backend Developers - Advanced
- Platform Developers - Intermediate

Training Material:
- [Getting Started](https://graphql.org/graphql-js/)

### React

Used By:
- Frontend Developers - Advanced

Training Material:
- [Getting Started](https://reactjs.org/docs/getting-started.html)

### Cypress

Used By:
- Frontend Developers - Advanced
- Platform Developers - Novice (just need to know how to configure it for CI/CD)

Training Material:
- [Getting Started](https://docs.cypress.io/guides/end-to-end-testing/writing-your-first-end-to-end-test)

### Material UI

Used By:
- Frontend Developers - Advanced

Training Material:
- [Getting Started](https://mui.com/material-ui/getting-started/installation/)

### React Router

Used By:
- Frontend Developers - Advanced

Training Material:
- [Getting Started](https://v5.reactrouter.com/web/guides/quick-start)

### Apollo Client
Used By:
- Frontend Developers - Advanced

Training Material:
- [Getting Started](https://www.apollographql.com/docs/react/get-started/)

### TypeScript
Used By:
- Frontend Developers - Intermediate
- Platform Developers - Intermediate

Training Material:
- [Getting Started](https://www.typescriptlang.org/docs/)

### Figma

Used By:
- Frontend Developers - Intermediate
- Designers - Advanced
- Product Managers - Novice
- Project Managers - Novice

Training Material:

### Rails
Used By:
- Backend Developers - Intermediate

Training Material:
- [Getting Started](https://guides.rubyonrails.org/)

### Rails Admin Gem
Used By:
- Backend Developers - Intermediate

Training Material:
- [Getting Started](https://github.com/railsadminteam/rails_admin/wiki)

### GraphQL Gem (with Pro)
Used By:
- Backend Developers - Intermediate

Training Material:
- [Getting Started](https://graphql-ruby.org/getting_started)
- [Pro](https://graphql.pro/)

### Searchkick Gem
Used By:
- Backend Developers - Intermediate

Training Material:
- [Getting Started](https://github.com/ankane/searchkick#getting-started)

### Rspec
Used By:
- Backend Developers - Intermediate
- Platform Developers - Novice (know how to run it during CI/CD)

Training Material:
- [Getting Started](https://semaphoreci.com/community/tutorials/getting-started-with-rspec)


### Rails Lamby

Lamby is Rails built with SAM on an the AWS Elastic Container Service to run serverlessly on Lambda.

Used By:
- Backend Developers - Intermediate
- Platform Developers - Advanced

Training Material:
- [Getting Started](https://lamby.custominktech.com/docs/quick_start)

### Node
Used By:
- Backend Developers - Novice

Training Material:

### Python
Used By:
- Backend Developers - Novice

Training Material:

### Java
Used By:
- Backend Developers - Novice

Training Material:

### AWS CloudFormation Development Kit
Used By:
- Platform Developers - Advanced

Training Material:

### AWS CloudFormation
Used By:
- Platform Developers - Advanced

Training Material:

### AWS Serverless Application Model
Used By:
- Platform Developers - Advanced

Training Material:

### Aurora (Postgres)
Used By:
- Platform Developers - Intermediate

Training Material:

### RDS Proxy
Used By:
- Platform Developers - Intermediate

Training Material:

### Elasticache (Redis)
Used By:
- Platform Developers - Intermediate

Training Material:

### OpenSearch
Used By:
- Platform Developers - Intermediate

Training Material:

### AWS SQS
Used By:
- Platform Developers - Intermediate

Training Material:

### AWS VPCs
Used By:
- Platform Developers - Intermediate

Training Material:

### Docker
Used By:
- Backend Developers - Novice
- Platform Developers - Intermediate

Training Material:

### Lambda
Used By:
- Platform Developers - Advanced
- Backend Developers - Intermediate

Training Material:

### Serverless Framework
Used By:
- Platform Developers - Advanced
- Backend Developers - Novice

Training Material:
- [Getting Started](https://www.serverless.com/framework/docs/getting-started)
