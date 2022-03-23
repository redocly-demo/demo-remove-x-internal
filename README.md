# Demo the `remove-x-internal` decorator

Redocly has a CLI tool with a [built-in `remove-x-internal` decorator](https://redocly.com/docs/cli/resources/built-in-decorators/) which transforms an OAS definition to remove nodes tagged with `x-internal: true`.

The Redocly configuration and OpenAPI file demonstrate how to:
- Remove the internal nodes (an operation, and a schema property)
- Apply different theme and features to internal versus external
- Override the info description for a different internal description

This repo has:

- a minimal OAS definition  (`openapi.yaml`)
- a Redocly configuration file (`redocly.yaml`)

To produce the external version, run `openapi bundle internal`. To produce the internal version, run `openapi bundle external`. On the other hand, as you add APIs to the registry, pick the appropriate one you wish to add (or add them both).

## Registry results

### Internal API

- [OAS bundle](https://api.redocly.com/registry/bundle/testing_acme/internal/latest/openapi.yaml?branch=main)
- [Docs](https://internal-example.redoc.ly/)

### External API

- [OAS bundle](https://api.redocly.com/registry/bundle/testing_acme/external/latest/openapi.yaml?branch=main)
- [Docs](https://external-example.redoc.ly/)
