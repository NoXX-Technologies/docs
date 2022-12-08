# Docs

Welcome to NOXX's collection of documentation!

Who ever thought documentation could be this fun, right?

Anyway, the main page here acts as an index into specific levels of documentation.

************ STOP *****************

Is something missing or off?

Does something not work like the documentation says it should?

Does something not make sense?

Don't keep going! Fix/add it! Or contact Cody and he'll fix/add it!

[Please check back often for updates and changes!](https://github.com/NoXX-Technologies/docs/commits/main)

Also, the #docs slack channel will automatically be notified when this repo is updated.

## Everybody
- [Onboarding](onboarding/README.md)
- [Org Chart](org-chart/README.md)
- [Project Standards](project-standards/README.md)
- [Project Management Process](process/README.md)

## Developers
### Tech Stack Overview

The Collect Tech Stack is a collection of microservices running on AWS products.
#### [Severless Services](developers/services/README.md)
These services are built using the [Serverless Framework](https://serverless.com/) and include the following:
- [Card Recognition Service (Python)](https://github.com/NoXX-Technologies/card-recognition-service). Written in Python, this service is for Natural Language Processing and Image recognition of card images
- [Data Service (Java)](https://github.com/NoXX-Technologies/collect-java). Written in Java, this service is for data and asset integration with Palantir Foundry
- [Congito Single Sign On Service (TypeScript)](https://github.com/NoXX-Technologies/cognito-service). Written in TypeScript, this service provides the authentication and authorization layer for Collect and, soon, the rest of Beckett
#### Other Services
- [Global Infrastructure](https://github.com/NoXX-Technologies/infrastructure). Built using TypeScript CDK, this is an Infrastructure as Code service that builds the Infrastructure required to run the other services.
- [Collect Frontend (React)](https://github.com/NoXX-Technologies/react-frontend). Built using TypeScript React, this service provides the presentation layer for the Collect frontend.
- [Collect API and Admin (Rails)](https://github.com/NoXX-Technologies/rails-api). Built using Ruby on Rails running on an Elastic Container Service-backed Lambda, this service provides the GraphQL API used by the Frontend as well as the Admin and Moderation services allowing authorized team members to modify and approve data. 


