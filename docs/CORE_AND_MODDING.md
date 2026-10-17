# Core, Scenarios, and Modding

**Status:** proposed architecture direction; no engine or modding tools have been implemented.

The project should have a small, inspectable core that runs a virtual world. Communities should be able to add their own ideas through scenarios and modifications without changing that core. The core should provide shared technical foundations, not prescribe one social or economic model.

## What belongs in the core

The first core should stay deliberately small. Candidate responsibilities:

- advance world time and process player or system actions;
- represent characters, places, resources, services, and world state;
- apply rules and events supplied by a scenario;
- save, load, inspect, and export world state;
- record enough configuration and events to explain and reproduce a run;
- create checkpoints and branches so players can recover, compare alternatives, and change course;
- expose a documented interface for compatible scenario packages.

The core should not hard-code one allocation policy, political structure, cultural model, or definition of a successful society. Shared data types should support extension, and scenario authors should be able to state their assumptions and add new concepts.

## Scenarios and modifications

A scenario package may provide:

- a starting world, characters, locations, resources, and services;
- rules for activities, resource use, cooperation, and collective decisions;
- events, goals, dialogue, text, art, sound, and localization;
- optional interface layouts or gameplay variations.

Each package should include a human-readable description and a machine-readable manifest with its identifier, version, compatible core versions, dependencies, declared data types, and license/attribution. The package should be inspectable before installation and portable as a file. Users should be able to create, export, back up, and share packages without a project-operated account or service.

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

