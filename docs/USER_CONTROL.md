# User Control and Deployment Requirements

**Status:** project requirement for future design; no simulation software is implemented yet.

Open Society Simulation is intended to give people a tool they can run and control. It must not require a project-operated remote service to perform the simulation. This requirement follows Richard Stallman's criticism of *Service as a Software Substitute* (SaaSS), where users send their computing work to a server they do not control instead of running software they can inspect and change.

## Requirements

1. **Local execution:** the simulation's core functions must run on the user's computer without an internet connection, account, or remote execution service.
2. **Self-hosting:** users and communities must be able to install and operate the software on hardware they control. Setup and administration instructions are part of the project.
3. **No project-operated simulation service:** the project will not run models on a central server on users' behalf. Users run models locally or on a server whose software they control. Publishing project information or exchanging files is a separate activity and must not become a substitute for users' own computation.
4. **User-controlled data:** models, inputs, and results remain on the user's device or chosen server by default. Do not transmit experiment data or telemetry without a clear, voluntary choice.
5. **Portability and reproducibility:** document data formats and provide a way to export a run's configuration and results so users can inspect, copy, and rerun them elsewhere.
6. **Inspectable software:** publish source and build/run instructions so users can study, modify, and run their own version under the project's free software license.

## Review checklist for new features

Before accepting a feature, contributors should be able to answer:

- Does the core feature still work locally and offline?
- Can users operate the feature on a server they control?
- Does the feature create an account requirement, central dependency, telemetry, or data transfer? If so, is it optional, clearly explained, and off by default where applicable?
- Can users export their inputs and outputs in documented formats?
- Does the feature make a service operated by someone else a substitute for software users can run themselves? If it computes users' models remotely, redesign it for local or user-controlled operation.

If a feature cannot meet these requirements, it needs a public design discussion before implementation.

## Network services and licensing

GPL-3.0-or-later remains the license for software code at this stage. If network-facing server components are proposed, review AGPL-3.0-or-later before implementation because it can require source availability to users interacting with a modified program over a network. AGPL does not by itself prevent SaaSS or guarantee user control; local execution and self-hosting remain separate requirements.

These requirements are informed by [Richard Stallman's explanation of SaaSS](https://www.gnu.org/philosophy/who-does-that-server-really-serve.html), his [computing practices](https://stallman.org/stallman-computing.html), and the [GNU license recommendations for server software](https://www.gnu.org/licenses/license-recommendations.en.html).
