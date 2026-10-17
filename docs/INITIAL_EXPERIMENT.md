# Initial Experiment: Resource Allocation in a Small Community

**Status:** agreed research direction; model details below are proposals for review, not implemented behavior.

**Initial need categories:** water, food, and energy (selected for the first example). Units and numeric values will be synthetic and documented.

## Research question

How do different resource-allocation rules affect the coverage and distribution of basic needs in a small synthetic community under limited supply and a one-step supply shock?

This experiment is intended to compare explicit model rules under controlled assumptions. It cannot establish which rule is fairest in general or predict how a real society would behave.

## Proposed scope

The first model may include:

- a small synthetic population with differing, explicitly specified needs for water, food, and energy;
- limited quantities of water, food, and energy available for allocation;
- one-step allocation from a reproducible starting state;
- alternative allocation rules applied to the same population and resource conditions;
- a baseline-supply scenario and a reduced-supply stress scenario.

The first prototype should use synthetic data. It will compare allocation outcomes in one step; resource storage, multi-step dynamics, and recovery after a disruption are deferred to a later stage. Real-world data, money, markets, political institutions, complex behavior, and claims about particular populations are outside this initial experiment unless a later proposal justifies adding them.

## Candidate allocation rules

Candidate rules should be defined precisely before implementation. Initial examples for discussion:

1. **Equal share:** distribute the available amount equally among community members.
2. **Needs-prioritized:** allocate toward the most urgent unmet needs first, using a documented priority order.
3. **Proportional-to-need:** distribute the available amount in proportion to each member's stated need.

These are comparison cases, not endorsements. The model must document how ties, insufficient supply, and any remaining resources are handled. Other rules can be proposed and compared using the same inputs.

## Candidate measures

“Fairness” is not a single self-evident quantity. The experiment should report separate, interpretable measures and state what each does and does not capture. Candidate measures include:

- **Basic-needs coverage:** share of stated needs met, overall and by need category.
- **Unmet-need distribution:** how shortfalls are distributed across members, including the number of members below a documented minimum threshold.
- **Resource efficiency:** resources used, left unused, or lost under the modeled rules.
- **Shock impact:** change in needs coverage between baseline supply and the reduced-supply scenario. Recovery time is out of scope for the one-step model.

The thresholds, aggregation methods, and disruption scenario must be specified before results are interpreted. No single measure should be presented as a complete ranking of social systems.

## Experimental controls and reproducibility

When comparing rules, hold the population, needs, available supply, and shock scenario constant. Record all model parameters and, if stochastic behavior is later introduced, record the random seed. Publish the scenario definition with results so another person can reproduce the run.

## Assumptions and limitations to document

- How needs are defined, measured, prioritized, and allowed to change.
- Whether resources are interchangeable, storable, renewable, or perishable.
- Whether the model represents individuals, households, or aggregate groups.
- Which real social processes are deliberately omitted.
- How sensitive outcomes are to parameter choices and chosen measures.

The model is a simplified thought experiment. Its outputs describe only the model under its assumptions; they are not forecasts, policy recommendations, or evidence that a rule would succeed in practice.

## Relation to existing approaches

The [Venus Project](https://www.thevenusproject.com/) is one source of ideas about systems approaches to resource management and ecological sustainability. The experiment may represent relevant proposals as explicit rules if they can be operationalized, and compare them with alternatives. This does not imply endorsement, affiliation, or a claim that one proposal is validated by the simulation.

## Decisions still needed

- How should per-person demand and resource availability vary in the synthetic scenario?
- How should a minimum acceptable needs threshold be defined for the experiment?
- Which candidate allocation rules should be included in the first comparison?
- What magnitude of supply reduction should the stress scenario use?
- Which measures should be mandatory in the first report?
- Which software license should apply before code contributions begin?
