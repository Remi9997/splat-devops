# Science Platform DevOps

## Goal

Provide standardized DevOps artifacts and tools for scaffolding Science Platform projects.

## Plan

Use composition to provide DevOps functionality in modules. Use templates to put those modules together.

## Composition
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

## Templates

Templates generate code from a set of parameters.
They combine modules together to form a cohesive DevOps artifact (e.g. pipeline, infrastructure spec, Dockerfile).


