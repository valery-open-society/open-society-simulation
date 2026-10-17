# Core, Scenarios, and Modding

**Status:** proposed architecture direction; no engine or modding tools have been implemented.

The project should have one shared, inspectable world core that runs the simulation. It represents the common conditions every scenario uses: people and their needs, resources, land, flora and fauna, and ecological processes and limits such as carrying capacity. Communities add their own social systems around this foundation through scenarios and modifications, without replacing the shared core. The core provides common world conditions, not a prescribed social or economic model.

## What belongs in the core

The first core should stay deliberately small. Candidate responsibilities:

- advance world time and process player or system actions;
- represent characters, places, resources, services, and world state;
- represent ecological conditions and limits, including land use, population pressures, and resource regeneration where the model supports them;
- apply rules and events supplied by a scenario;
- save, load, inspect, and export world state;
- record enough configuration and events to explain and reproduce a run;
- create checkpoints and branches so players can recover, compare alternatives, and change course;
- expose a documented interface for compatible scenario packages.

The core should not hard-code one allocation policy, political structure, cultural model, or definition of a successful society. Shared data types should support extension, and scenario authors should be able to state their assumptions and add new concepts. Separate scenarios may use the same core and comparable starting conditions while keeping their rule sets distinct and versioned.

## Scenarios and modifications

A scenario package may provide:

- a starting world, characters, locations, resources, and services;
- rules for activities, resource use, cooperation, and collective decisions;
- events, goals, dialogue, text, art, sound, and localization;
- optional interface layouts or gameplay variations.

Each package should include a human-readable description and a machine-readable manifest with its identifier, version, compatible core versions, dependencies, declared data types, and license/attribution. The package should be inspectable before installation and portable as a file. Users should be able to create, export, back up, and share packages without a project-operated account or service.

## Choosing and joining social experiments

Players should be able to browse scenarios, understand what each one proposes, and choose which community's social system to experience on the shared world core. A scenario may be authored by an individual, a community, a research group, or an existing project. For example, The Venus Project could create a playable visualization of its own social vision. The project should provide shared foundations and a public catalogue, not certify every scenario's claims.

Before joining, players should be able to review:

- the scenario's goals, assumptions, rules, and intended experience;
- its creator, version, sources, and known limitations;
- which data is stored by a local or community-hosted world;
- whether participation, data collection, or public sharing is optional.

Players choose whether to join and should be able to leave. A scenario should preserve its stated rules and version for reproducibility while allowing a community to propose changes through transparent world governance.

## Public results and comparison

Communities should be able to publish scenario packages and result reports in an open catalogue so others can inspect, reproduce, and compare them. Reports should include the scenario and core versions, starting conditions, rules and parameters, evaluation criteria, outcome data, known omissions, and a record of revisions. Unsuccessful runs and negative results should remain publishable alongside successful ones.

Do not collapse the result into a single universal success score. Communities should declare criteria before interpreting a run and may examine multiple dimensions such as meeting human needs, distribution and fairness, ecological health, resilience, and participant experience. Show trade-offs and uncertainty, and identify who chose the criteria. A result can be called successful only relative to the stated goals and this model's limits; it is not a final ranking of real social systems.

## Interpreting results beyond the game

The core must label outcomes as results of a model, not proof or prediction about real societies. It should let scenario authors disclose assumptions and sources, preserve versions, compare alternative runs, and show uncertainty and sensitivity to changed assumptions as these tools become available.

Moving an idea from a virtual world into a real community requires evidence beyond gameplay. Any such proposal should receive independent review, involve affected people in deciding whether and how to proceed, define safeguards and measures in advance, protect participants' privacy, and begin cautiously with a reversible approach. The game can help surface hypotheses, trade-offs, and failure modes; it cannot by itself certify a social system as safe or successful in real life.

## Creation without programming

The project should aim to provide a visual scenario editor so people can create and change worlds without writing code. Possible tools include forms and visual editors for characters, needs, places, resources, services, rules, events, and localization; reusable rule blocks; validation that explains errors in plain language; and a preview/playtest mode.

Creation can progress from simple settings to visual rule composition and, optionally, code extensions. A first version should prefer safe, constrained building blocks over requiring arbitrary scripts. Programmers should still be able to build deeper extensions through documented interfaces.

## Scenario interoperability

Interoperability is a core project goal, but packages should not be assumed compatible just because they are both scenarios. Use versioned shared concepts and publish explicit compatibility information. Support three clear outcomes:

1. **Compatible:** packages can be combined in one world using shared definitions.
2. **Adaptable:** a documented adapter or mapping is needed to translate concepts, units, or rules.
3. **Incompatible:** the packages rely on assumptions that cannot currently be reconciled; keep them as separate worlds.

Where feasible, users should be able to combine compatible modules when creating a world, or export a world and import it into another scenario through an explicit migration/adapter. Preserve the source scenario, rule versions, and transformation details so results remain understandable. Never silently merge conflicting rules or treat one community's terms as universal.

## Failure recovery and changing course

The game should help players notice when a world is moving away from its stated goals and safely explore corrections. The core should provide:

- **Visible indicators and alerts:** players or a community choose which conditions to track and set warning thresholds. An alert is a signal to investigate, not an automatic judgment that a society has failed.
- **Checkpoints:** save a complete, portable snapshot of world state, scenario and mod versions, rules, and relevant event history.
- **What-if branches:** create a separate branch from a checkpoint, change rules or decisions, and compare what follows without overwriting the original path.
- **Forward correction:** edit rules or policy from the current point onward, record what changed and why, and preserve the earlier history.
- **Restore or rollback:** return a world to a checkpoint when needed. Restoration should create a new, clearly labeled branch and keep the previous history available; it should not silently erase the path that players experienced.
- **Comparison and review:** show the assumptions, interventions, and outcomes for the original and alternative branches side by side.

In a shared world, rollback affects everyone. The server's community should decide who can propose, approve, and perform a restore. The world should record who initiated it, when it happened, the checkpoint used, and what was restored. Owners should communicate major restores to players. The default design should favor branching and transparent history over an untraceable rewind.

This supports both recovery inside the game and learning from a failed experiment: players can preserve the original outcome, test a different course, and decide whether to continue from the new branch.

## Initial vertical slice

Before building a large editor or multiplayer platform, validate a small local workflow:

1. start a sample world from a scenario package;
2. change a few world settings with a visual, no-code editor;
3. preview the effect in play;
4. save and export the modified scenario as a portable package;
5. load it again and reproduce the same starting world;
6. save a checkpoint, branch the world, change a rule, and compare both paths without losing the original.

The exact visual style, editor framework, and first rule blocks remain open design decisions.

## Open questions

- Which world concepts are truly shared enough to define in the first core?
- What is the simplest visual rule editor that remains understandable to non-programmers?
- Which scenarios should be directly composable, and what does a useful adapter look like?
- How should conflicting packages, dependencies, versions, and licenses be shown to creators?
- How can the core validate packages and protect users from unsafe extensions?
- Which early-warning indicators should a scenario author be able to define?
- What restore and approval rules should shared-world communities be able to configure?

