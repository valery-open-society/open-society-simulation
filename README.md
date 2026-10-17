# Open Society Simulation

![Open Society Simulation mark](assets/open-society-simulation-avatar.png)

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
- **Free software:** the project intends to use a free/libre and open-source software license. No license has been selected yet, so the repository currently has no license grant.

## Relationship to existing ideas

The project may examine ideas from a range of social and economic approaches. The [Venus Project](https://www.thevenusproject.com/) is one relevant source of ideas about resource management, systems design, and ecological sustainability. Its proposals may be modeled and examined alongside alternatives; they are not assumed conclusions of this project. Open Society Simulation is independent and is not affiliated with or endorsed by The Venus Project.

## Scope and limitations

A simulation is a simplified model, not a complete representation of society. Its results depend on assumptions, data, selected measures, and implementation. They must not be presented as proof that a social system will work in practice.

The project has not selected a first scenario or committed to a particular economic, political, or social model. Those choices should be documented and open to review before implementation.

## Next steps

See the [project roadmap](ROADMAP.md) for the current sequence of work. The immediate priorities are to refine the initial experiment, define a small example model, and select a software license before accepting code contributions.

## Participate

The project is at an early stage. Feedback on its mission, scope, first research question, and modeling principles is welcome. Open an [issue](https://github.com/valery-open-society/open-society-simulation/issues) with a focused question or proposal. Before contributing, please read [CONTRIBUTING.md](CONTRIBUTING.md).

Please explain the problem you want to explore, the assumptions involved, and how a proposal could be evaluated. Project governance will be documented as the contributor community develops.
