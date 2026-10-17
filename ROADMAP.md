# Project Roadmap

This roadmap describes the next decisions and deliverables for Open Society Simulation. It is a planning document, not a promise of dates. The project is at the foundation stage; no playable game has been implemented. The proposed player experience is described in the [project vision](docs/VISION.md).

## 1. Define the first playable experience — in progress

- Specify one small daily-life loop that a player can experience in a virtual community.
- Decide which needs, activities, interactions, and shared resources belong in that first slice.
- Define the smallest neutral core and scenario interface needed to host different community-created ideas.
- Keep the world and its social rules understandable, inspectable, and open to alternatives.
- Use the initial resource-allocation experiment as a candidate subsystem, not as the whole game.

**Deliverable:** a reviewed playable-scope brief with player goals, world boundaries, assumptions, and evaluation questions.

## 2. Establish project practices

- Publish the GNU GPL-3.0-or-later license for software code and clarify terms for documentation, data, and visual assets as the project develops.
- Decide how contributors propose and review changes.
- Document project governance and how disagreements are handled.
- Identify a project contact for community and security reports.

**Deliverable:** a repository with clear software licensing and contribution expectations.

## 3. Design a minimal playable prototype

- Compare suitable implementation options against the game vision and contributor capacity.
- Build one small daily-life scenario that runs locally without an account or network connection.
- Provide a visual no-code workflow to change and export a few scenario settings or rules.
- Specify explicit compatibility metadata and an adapter path for combining or migrating between scenarios.
- Make the virtual society's rules and simulation state inspectable and reproducible.
- Keep world data under the user's control and document export and backup formats.
- Document how to install, inspect, and run the software from source.

**Deliverable:** a minimal local game slice with a small visual scenario editor that a person can play, customize, and understand without a project-operated service.

## 4. Support shared, user-controlled worlds

- Allow a user or community to host a persistent shared world on a server they control.
- Let people register with a specific community world without requiring a central project identity service.
- Do not build a project-operated service that runs simulations on behalf of users; prioritize local use and user-controlled deployment.
- Document server administration, player-data handling, backups, moderation, and world transfer or shutdown.
- Before adding network-facing server components, review whether AGPL-3.0-or-later is appropriate; network copyleft does not replace local execution and self-hosting.
- Make data flows explicit and keep telemetry off by default.

**Deliverable:** players can choose local play or join a community world whose operator controls its server and data.

## 5. Evaluate and iterate

- Compare results across alternative rules and starting conditions.
- Check whether measures are meaningful and whether important effects are omitted.
- Document uncertainty, limitations, and unexpected results.
- Revise the model based on review and evidence.

**Deliverable:** a documented experiment and an updated model specification.

## Principles for changing this roadmap

Priorities may change as the research scope becomes clearer. Changes should explain what changed and why. The roadmap does not imply that later stages are approved before the earlier questions are answered.
