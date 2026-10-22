# Project Roadmap

This roadmap describes the next decisions and deliverables for Open Society Simulation. It is a planning document, not a promise of dates. The project is at the foundation stage; no playable game has been implemented. The proposed player experience is described in the [project vision](docs/VISION.md).

## 1. Define the first research question and playable direction — in progress

Develop the project from small to large: settle a bounded research question and a reproducible model first, review what it can and cannot show, then expand toward a playable daily-life loop and broader world systems. Each stage should have a concrete deliverable and a review point; later stages remain proposals until the earlier work informs them.

- Specify one small daily-life loop that a player can experience in a virtual community.
- Review the proposed starting question: how do different resource-allocation rules affect basic-needs coverage and distribution in a small synthetic community under limited or disrupted supply?
- Decide which needs, activities, interactions, and shared resources belong in that first slice.
- Define the smallest neutral core and scenario interface needed to host different community-created ideas.
- Specify shared core concepts for people, resources, land, flora and fauna, ecological processes, and carrying capacity.
- Design a scenario catalogue that explains each world's creator, assumptions, rules, sources, and limitations so players can choose where to participate.
- Make joining and leaving a world voluntary, and preserve scenario versions so players can understand which rules shaped a run.
- Define an open result-report format that includes success criteria, uncertainty, failures, and revisions, without reducing comparison to one universal score.
- Keep the world and its social rules understandable, inspectable, and open to alternatives.
- Use the initial resource-allocation experiment as a candidate subsystem, not as the whole game.

**Deliverable:** a reviewed playable-scope brief with player goals, world boundaries, assumptions, and evaluation questions.

## 2. Establish project practices

- Publish the GNU GPL-3.0-or-later license for software code and clarify terms for documentation, data, and visual assets as the project develops.
- Decide how contributors propose and review changes.
- Document project governance and how disagreements are handled.
- Identify a project contact for community and security reports.

**Deliverable:** a repository with clear software licensing and contribution expectations.

## 3. Build the initial research prototype

- Implement the bounded, one-step resource-allocation experiment in `docs/INITIAL_EXPERIMENT.md` using synthetic data.
- Compare the proposed allocation rules under the same baseline and reduced-supply conditions.
- Report allocations, unmet needs, coverage, and distribution as separate measures; do not rank scenarios with one universal score.
- Make the run local, deterministic, inspectable, and reproducible from a documented configuration.
- Record assumptions, limitations, and unsuccessful or unexpected outcomes for review.

**Deliverable:** a small research prototype and reproducible report that can be reviewed before the project expands the model or commits to a larger playable scope.

## 4. Design a minimal playable prototype

- Compare suitable implementation options against the game vision and contributor capacity.
- Build one small daily-life scenario that runs locally without an account or network connection.
- Provide a visual no-code workflow to change and export a few scenario settings or rules.
- Specify explicit compatibility metadata and an adapter path for combining or migrating between scenarios.
- Make the virtual society's rules and simulation state inspectable and reproducible.
- Add checkpoints and what-if branches to the local prototype so players can test a correction without losing the original path.
- Keep world data under the user's control and document export and backup formats.
- Document how to install, inspect, and run the software from source.
- Keep the first simulation engine focused on the smallest loop needed by the agreed experiment; add systems only when they serve a stated research or gameplay question.

**Deliverable:** a minimal local game slice with a small visual scenario editor that a person can play, customize, and understand without a project-operated service.

## 5. Support shared, user-controlled worlds

- Allow a user or community to host a persistent shared world on a server they control.
- Let people register with a specific community world without requiring a central project identity service.
- Do not build a project-operated service that runs simulations on behalf of users; prioritize local use and user-controlled deployment.
- Document server administration, player-data handling, backups, moderation, and world transfer or shutdown.
- Define transparent community procedures and permissions for restoring or branching a shared world.
- Before adding network-facing server components, review whether AGPL-3.0-or-later is appropriate; network copyleft does not replace local execution and self-hosting.
- Make data flows explicit and keep telemetry off by default.

**Deliverable:** players can choose local play or join a community world whose operator controls its server and data.

## 6. Evaluate and iterate

- Compare results across alternative rules and starting conditions.
- Check whether measures are meaningful and whether important effects are omitted.
- Document uncertainty, limitations, and unexpected results.
- Treat game outcomes as model results and hypotheses, not proof of real-world success; require independent evidence and cautious, reversible review before considering real-world application.
- Revise the model based on review and evidence.

**Deliverable:** a documented experiment and an updated model specification.

## Principles for changing this roadmap

Priorities may change as the research scope becomes clearer. Changes should explain what changed and why. The roadmap does not imply that later stages are approved before the earlier questions are answered.
