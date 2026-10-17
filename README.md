# Open Society Simulation

<img src="assets/open-society-simulation-avatar.png" alt="Open Society Simulation mark" width="220">

**An open platform for exploring and comparing models of social organization.**

Open Society Simulation is an early-stage project to develop tools for describing social models, running transparent experiments, and comparing outcomes under stated assumptions. Its purpose is to support inquiry and discussion—not to encode one society as the correct answer.

> **Status:** project foundations. There is no runnable simulation yet. The first research direction is agreed, while the detailed model and technical design remain open.

## Why this project

Ideas about how societies might organize resources, work, decision-making, and infrastructure are often discussed without a shared way to examine their assumptions and possible consequences. This project aims to make those assumptions explicit and help people explore, reproduce, and compare different approaches.

The intended audience includes researchers, developers, students, and other interested participants. Simulation results should be treated as outputs of a model—not as predictions or policy recommendations for real societies.

## What we aim to build

The current concept has five parts:

1. **Society models** describing people or populations, needs, resources, production, and infrastructure.
2. **Configurable rules** for resource allocation, work, collective decision-making, and interaction.
3. **A simulation engine** that advances a model over time and records its state.
4. **Reproducible experiments** that specify initial conditions, rules, parameters, and random seeds where applicable.
5. **Analysis tools** for examining and comparing outcomes using documented measures, such as needs met, resource use, environmental effects, and resilience.

These are working concepts, not a finalized specification. The first proposed research track is a small synthetic community with finite resources; see the [initial experiment brief](docs/INITIAL_EXPERIMENT.md). Model boundaries, data needs, indicators, and implementation choices remain open.

## Principles

- **Pluralism:** support exploration of different models and assumptions without privileging one ideology as the project's answer.
- **Transparency:** document assumptions, rules, parameters, limitations, and changes.
- **Reproducibility:** make it possible to rerun documented experiments and inspect how results were produced.
- **Scientific integrity:** distinguish model outputs from evidence about the real world, and report uncertainty and limitations.
- **Open collaboration:** welcome contributors across disciplines and backgrounds; develop project materials and decisions in the open.
- **Free software:** software code in this repository is licensed under the GNU General Public License, version 3 or (at your option) any later version. See [LICENSE](LICENSE).

## License

The GNU GPL-3.0-or-later applies to software code in this repository. Documentation, datasets, and visual assets are not covered by that license unless a file states otherwise. Each contribution must respect the license and copyright terms stated for the files it changes.

## Relationship to existing ideas

The project may examine ideas from a range of social and economic approaches. The [Venus Project](https://www.thevenusproject.com/) is one relevant source of ideas about resource management, systems design, and ecological sustainability. Its proposals may be modeled and examined alongside alternatives; they are not assumed conclusions of this project. Open Society Simulation is independent and is not affiliated with or endorsed by The Venus Project.
