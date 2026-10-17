# Open Society Simulation

<img src="assets/open-society-simulation-avatar.png" alt="Open Society Simulation mark" width="220">

**An open-source life simulation for exploring how people live together in different kinds of societies.**

Open Society Simulation aims to become a playable virtual world where people can inhabit characters, take part in everyday life, and explore how a society's rules shape shared experience. Resource-allocation models and transparent experiments are tools within that world, not the whole experience. The project supports inquiry and discussion; it does not present one society as the correct answer.

> **Status:** project foundations. There is no playable game yet. The life-simulation direction is proposed; the first playable scope and technical design remain open.

## Why this project

Ideas about how societies might organize resources, work, decision-making, and infrastructure are often discussed without a shared way to examine their assumptions and possible consequences. This project aims to make those assumptions explicit and help people explore, reproduce, and compare different approaches.

The intended audience includes researchers, developers, students, and other interested participants. Simulation results should be treated as outputs of a model—not as predictions or policy recommendations for real societies.

## What we aim to build

The proposed game has five connected parts:

1. **Virtual worlds and characters** where players can choose and inhabit different community-created social experiments.
2. **Social and resource systems** covering needs, homes, services, work, production, and infrastructure.
3. **A small, extensible core** that advances the world while leaving social rules and values open to scenarios.
4. **Scenario and mod tools** that let people create and adapt worlds with visual tools, without requiring programming.
5. **Scenario interoperability** with explicit compatibility and adapters so compatible ideas can be combined without silently flattening differences.

These are working concepts, not a finalized specification. Read the [project vision](docs/VISION.md) and the proposed [core and modding architecture](docs/CORE_AND_MODDING.md). Players should be able to explore a scenario without treating an in-game outcome as proof that the same idea will work in real life. The [initial experiment brief](docs/INITIAL_EXPERIMENT.md) defines a small resource-allocation model that may support one part of a future game. Model boundaries and implementation choices remain open.

## User control and deployment

The game is intended to run locally and to support shared worlds on servers controlled by users or communities. Local play should work offline without an account. Players may register with a particular community server, but using the project must not require a central project account or remote execution service. Users and server operators should control their worlds and data. See the [user control and deployment requirements](docs/USER_CONTROL.md).

The project will not operate a hosted service that runs simulations on users' behalf. That would substitute for software they can run and control themselves (*Service as a Software Substitute*, or SaaSS).

## Principles

- **Pluralism:** support exploration of different models and assumptions without privileging one ideology as the project's answer.
- **Transparency:** document assumptions, rules, parameters, limitations, and changes.
- **Reproducibility:** make it possible to rerun documented experiments and inspect how results were produced.
- **User control:** support offline local play and self-hosted worlds; do not require a project-controlled service or central account.
- **Scientific integrity:** distinguish model outputs from evidence about the real world, and report uncertainty and limitations.
- **Open collaboration:** welcome contributors across disciplines and backgrounds; develop project materials and decisions in the open.
- **Free software:** software code in this repository is licensed under the GNU General Public License, version 3 or (at your option) any later version. See [LICENSE](LICENSE).

## License

The GNU GPL-3.0-or-later applies to software code in this repository. Documentation, datasets, and visual assets are not covered by that license unless a file states otherwise. Each contribution must respect the license and copyright terms stated for the files it changes.

## Relationship to existing ideas

The project may examine ideas from a range of social and economic approaches. The [Venus Project](https://www.thevenusproject.com/) is one relevant source of ideas about resource management, systems design, and ecological sustainability. Its proposals may be modeled and examined alongside alternatives; they are not assumed conclusions of this project. Open Society Simulation is independent and is not affiliated with or endorsed by The Venus Project.
