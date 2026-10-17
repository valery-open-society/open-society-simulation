# Project Vision: A Shared Virtual Society

**Status:** direction proposed by the project founder; gameplay and technical details remain open for community discussion.

Open Society Simulation aims to become an open-source life simulation in which people can create or inhabit virtual characters and experience everyday life inside a changing society. It should feel like living in a virtual world, not only entering numbers into a resource-allocation model.

Players should be able to explore how a society works through ordinary activities, relationships, shared decisions, and the consequences of how resources and infrastructure are organized. Models of social organization are part of the world and its rules; they are not presented as proven predictions about real societies.

The game should be built around one shared, neutral world core. It represents people, resources, land, flora and fauna, and ecological limits such as the carrying capacity of the land. Communities can build their own social systems around this common foundation by defining institutions, rules, technologies, and ways of life. The core supplies common world conditions; it does not prescribe one social order. People should be able to create scenarios and modifications with visual tools, even if they do not program. See the proposed [core and modding architecture](CORE_AND_MODDING.md).

People should be able to explore a catalogue of clearly described social experiments and choose which community scenario they want to experience. A community, research group, or project such as The Venus Project could create a scenario that presents its own vision, assumptions, and rules in a playable form on the shared core. Communities should be able to publish their scenario definitions and result reports for public inspection, including failures and revisions. Results should be compared using disclosed criteria, assumptions, and model limits; inclusion or a favorable in-game result does not mean the project endorses a scenario or guarantees it would work in real life.

## Intended experience

A future playable version may let players:

- create a character and take part in everyday life in a virtual community;
- meet and cooperate with other characters, including characters controlled by other players in a shared world;
- use homes, services, public spaces, and infrastructure supported by the world;
- experience how different rules for resources, work, services, and collective decisions affect daily life;
- take part in changing those rules and observe consequences over time;
- set warning indicators, preserve checkpoints, explore a different direction in a separate branch, and recover a world without erasing its earlier path;
- create or adapt scenarios with no-code tools, then share them as portable packages;
- choose a scenario, understand its assumptions and participation rules, and voluntarily join or leave its experiment.
- inspect public reports from other communities, including the setup, criteria, limitations, and unsuccessful runs.

This is a direction, not a finished feature list. The first prototype should validate one small, understandable slice of this experience before the project commits to a large world or detailed social systems. The initial resource-allocation experiment remains useful as a small model of one system within that world, but it is not the whole product.

## Worlds, accounts, and user control

- **Local world:** a person can start and play a world on their own computer without an account or internet connection.
- **Community world:** people can join a shared world hosted by its owner or community. Players register with that particular world; there is no required project-wide identity service.
- **Self-hosting:** communities can run their own server, set its rules, and control the world data they host.
- **Portability:** document world and character data formats and provide export and backup paths as the software develops.
- **No project-operated game service:** the project will not require a central service to run the simulation or keep a world alive. The detailed user-control requirements are in [USER_CONTROL.md](USER_CONTROL.md).

## Design questions to resolve

- What is the smallest playable daily-life loop that makes the world feel inhabited?
- Is the first prototype single-player, local co-op, or a small community server?
- Which needs, relationships, activities, and shared services matter in that first slice?
- How do players propose and change community rules?
- How can players identify when a world is moving away from its stated goals and test a correction safely?
- How should world owners handle moderation, backups, privacy, and shutdown or transfer of a world?
- Which platform and visual style can contributors realistically build and maintain?
- Which common scenario concepts should the core standardize, and which should remain community-defined?
- How can players tell whether two scenarios can be combined or need an adapter?

## Relationship to existing ideas

The [Venus Project](https://www.thevenusproject.com/) discusses a resource-based economy and a systems approach to areas such as city design, food, water, energy, transportation, and education. These ideas can inspire a community-authored scenario built on the shared core and explored alongside alternatives. The game remains independent and must not present any one proposal as established fact or as the project's required ideology.

## From virtual experience to real-world ideas

The project hopes that people can use virtual worlds to explore ideas carefully and identify questions worth investigating. A scenario's results show what happened inside that model under its assumptions. They do not verify that the same system would work in a real society. Any proposal for real-world use needs evidence beyond the game, independent scrutiny, informed participation of affected communities, clear safeguards, and a cautious, reversible approach.

