# Labs

## Overview
*Labs* is a open-source project that provides a platform for learning Application Security in a practical way. It offers a variety of hands-on **ephemeral labs** and **exercises** that cover different aspects of application security. 

### Features
- **Hands-on Labs**: Interactive labs that allow you to practice your skills in a safe environment.
- **Ephemeral Environments**: Each lab runs in its own isolated environment, ensuring that your work does not affect others and can be reset easily.
- **Evaluators**: Automated tools that assess your work and provide feedback, helping you learn and improve.
- **Manual Review**: In addition to automated evaluations, some labs may require manual review by instructors or peers for more complex tasks.

### Stack
The *Labs* project is built using a stack that includes:
- **Frontend**: Angular (with PrimeNG).
- **Backend**: Golang (with Echo).
- **API**: Golang (with Echo).
- **Orchestrator**: Kubernetes for managing lab environments.
- **Database**: PostgreSQL, Redis and MongoDB.

--- 
## Architecture
The *Labs* project is designed to be modular and extensible, allowing for easy addition of new labs and exercises. The architecture includes:
![Architecture Diagram](/img/labs/architecture.png)
1. **Frontend**: A user-friendly interface, providing access to labs and exercises.
2. **Backend**: A server that plays the role of BFF (Backend for Frontend): handling requests from the frontend, performing business logic, managing user labs sessions, and communicating with the API (Cluster-API) and database.
3. **REDIS**: A redis instance used as a caching layer to store session data (lab session attempts) and improve performance.
4. **Postgres**: A database that stores user progress, lab configurations and evaluation results.

