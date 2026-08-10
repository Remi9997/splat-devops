# Science Platform DevOps

## Goal

Provide standardized DevOps artifacts and tools for scaffolding Science Platform projects.

## Plan

All DevOps functionality is implemented in modules. The user specifies the capabilites and parameters as input.
Then, the sepcified capabilities are combined into a DevOps artifact with the parameters.

Modules contain the implementation. They are handled differently for each type of DevOps artifact. 

- Azure Pipelines
  - Template YAML files.
  - Pulled from git.

- Terraform
  - Terraform modules
  - Pulled from git.

- Dockerfile
  - Base images
  - Pulled from a Docker registry.

A CLI tool will be created to provide a simple interface for all users.
It will validate user input and generate DevOps artifact ouptuts.
The generated code should be very simple and mostly reference the modules. 

Responsabilities:
- Modules
  - DevOps implementations
  - Using the parameters (e.g. GCP project ID)

- CLI
  - Input validation
  - Selecting and combining modules
  - User experience (UX)