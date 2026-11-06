# EYEAR Application

Owner: **Yewon Joung** | Part of [EYEAR](https://github.com/HY-LG-EYEAR)

> Status: repository scaffold and implementation plan. This upload kit does not contain runnable services, approved new contracts, trained models, or measured results. Preserve existing implementation files when adding this scaffold.

## Responsibility

Build the ThinQ-style application using a Next.js frontend and Spring Boot backend. The course prototype is an independent interface, not a production ThinQ application modification.

Frontend: resident preference forms, observed-state views, agent proposals, selected/deferred/rejected actions, dialogue, and operator start/pause/reset/override controls. Show live/replay/authored input and GPT/fallback mode explicitly.

Backend: preference persistence, application APIs, authorized operator request routing, UI-facing queries and trace delivery. Delegate automated decisions and approved device commands to the Python Orchestrator. Hyochang owns simulation logic; agree whether its renderer is embedded or linked.

Dependency versions, Java version, build tool, database, authentication and deployment settings are not chosen by this scaffold.

## Inputs and outputs

Next.js communicates with Spring Boot application APIs. Spring Boot forwards decisions/control requests to the Orchestrator and exposes observed results to the UI. Publish OpenAPI after endpoints are implemented; do not claim proposed endpoint names already exist.

The authoritative shared contract release is maintained in [LG-EYEAR/contracts](https://github.com/HY-LG-EYEAR/LG-EYEAR/tree/main/contracts). Coordinate changes with producers and consumers; do not create an incompatible local contract under the same version.

## Structure

| Path | Intended content |
| --- | --- |
| `frontend/` | Next.js source belongs here. Add actual package manifest, lockfile, verified Node version and development/build commands. |
| `backend/` | Spring Boot source belongs here. Add the actual Maven/Gradle project, Java/Spring versions, config examples and verified commands. |
| `docs/` | API boundaries, screens, preference fields, error responses and integration configuration. |
| `tests/` | Frontend/backend contract and integration tests, including unavailable services and rejected controls. |

## Setup and execution status

This scaffold introduces no runtime dependencies or working launch commands. Preserve existing code. The owner must add the actual prerequisites, pinned dependency installation, configuration example, start/stop commands, and one verified smoke-test procedure before marking this repository runnable. Separate existing prototype instructions from the planned integrated system.

## Verification checklist

- [ ] Shared contract version and valid/invalid examples are identified.
- [ ] Dependencies and OS/hardware versions are recorded.
- [ ] A mock-input smoke test is reproducible.
- [ ] Missing, stale, unknown and invalid input behavior is tested.
- [ ] Integration with the next component is verified and exact commits are recorded.
- [ ] Current limitations and measured results are documented without invented metrics.

## Documentation

- [Integration and scenarios](https://github.com/HY-LG-EYEAR/LG-EYEAR)
- [CSE406 engineering document](https://github.com/HY-LG-EYEAR/LG-EYEAR-docs)
- [ITE351 research blog](https://github.com/HY-LG-EYEAR/LG-EYEAR-blog)

> Independent academic prototype. EYEAR is not an official LG Electronics product. The course prototype does not modify ThinQ ON firmware, integrate with the production ThinQ application, or control physical LG appliances.
