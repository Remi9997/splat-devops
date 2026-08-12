# Science Platform DevOps

## Goal

Provide standardized DevOps artifacts and tools for scaffolding Science Platform projects.

## Plan

All DevOps functionality is implemented in modules. The user specifies the capabilites and parameters as input.
Then, the sepcified capabilities are combined into a DevOps artifact alonside some parameters.

Capabilites are specific functions in a DevOps artifact. Some example capabilities with Azure Pipelines:
- Python testing
- Building and pushing an image
- Deploying to Google Cloud Run

Modules contain the implementation. They are handled differently for each type of DevOps artifact. 
- Azure Pipelines
  - Template YAML files.
  - Pulled from git
- Terraform
  - Terraform modules
  - Pulled from git
- Dockerfile
  - Base images
  - Pulled from a Docker registry

A CLI tool will be created to provide a simple interface for all users.
It will validate user input and generate DevOps artifacts.
The generated code should be very simple and mostly reference the modules.
The complexity should remain in the modules.

**Responsabilities:**
- Modules
  - DevOps implementations
  - Using the parameters (e.g. GCP project ID)

- CLI
  - Input validation
  - Selecting and combining modules
  - User experience (UX)
