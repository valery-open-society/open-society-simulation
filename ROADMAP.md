# Project Roadmap

This roadmap describes the next decisions and deliverables for Open Society Simulation. It is a planning document, not a promise of dates. The project is at the foundation stage; no simulation software has been implemented.

## 1. Establish the research scope — in progress

- Refine the agreed initial direction: compare resource-allocation rules in a small synthetic community with finite resources.
- Set the boundaries of the first model: what it represents and what it leaves out.
- Identify assumptions and possible sources of data.
- Define a small set of interpretable outcome measures.

**Deliverable:** a reviewed [initial experiment brief](docs/INITIAL_EXPERIMENT.md) with assumptions, limitations, and evaluation questions.

## 2. Establish project practices

- Publish the GNU GPL-3.0-or-later license for software code and clarify terms for documentation, data, and visual assets as the project develops.
- Decide how contributors propose and review changes.
- Document project governance and how disagreements are handled.
- Identify a project contact for community and security reports.

**Deliverable:** a repository with clear software licensing and contribution expectations.

## 3. Design a minimal prototype

- Compare suitable implementation options against the research requirements.
- Specify the model inputs, rules, outputs, and reproducibility requirements.
- Build one small, documented scenario that runs locally without an account or network connection.
- Keep experiment inputs and outputs under the user's control and in documented, exportable formats.
- Document how to install, inspect, and run the software from source.

**Deliverable:** a minimal local prototype whose behavior can be explained, inspected, and reproduced without a project-operated service.

## 4. Support user-controlled deployment

- Document deployment on a server controlled by a user or community.
- Do not build a project-operated service that runs simulations on behalf of users; prioritize local use and user-controlled deployment.
- Before adding network-facing server components, review whether AGPL-3.0-or-later is appropriate; network copyleft does not replace local execution and self-hosting.
- Make data flows explicit and keep telemetry off by default.

**Deliverable:** users can choose local execution or administer their own deployment with control over models, inputs, and results.

## 5. Evaluate and iterate

- Compare results across alternative rules and starting conditions.
- Check whether measures are meaningful and whether important effects are omitted.
- Document uncertainty, limitations, and unexpected results.
- Revise the model based on review and evidence.

**Deliverable:** a documented experiment and an updated model specification.

## Principles for changing this roadmap

Priorities may change as the research scope becomes clearer. Changes should explain what changed and why. The roadmap does not imply that later stages are approved before the earlier questions are answered.
