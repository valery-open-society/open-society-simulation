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

## Initial vertical slice

Before building a large editor or multiplayer platform, validate a small local workflow:

1. start a sample world from a scenario package;
2. change a few world settings with a visual, no-code editor;
3. preview the effect in play;
4. save and export the modified scenario as a portable package;
5. load it again and reproduce the same starting world.

The exact visual style, editor framework, and first rule blocks remain open design decisions.

## Open questions

- Which world concepts are truly shared enough to define in the first core?
- What is the simplest visual rule editor that remains understandable to non-programmers?
- Which scenarios should be directly composable, and what does a useful adapter look like?
- How should conflicting packages, dependencies, versions, and licenses be shown to creators?
- How can the core validate packages and protect users from unsafe extensions?

