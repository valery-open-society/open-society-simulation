# Initial Experiment: Resource Allocation in a Small Community

**Status:** candidate subsystem for the proposed life-simulation game; model details below are proposals for review, not implemented behavior.

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

The prototype should run locally without an account, network connection, or project-operated service. Experiment inputs, configuration, and results should remain under the user's control and be saved in documented formats that can be copied and rerun elsewhere. Remote execution is outside the first prototype.

## Provisional numeric scenario (for review)

The following small scenario makes the first comparison reproducible. Its values are invented for demonstration; they are not estimates of real consumption or a recommended standard of living. Treat this as a proposal until contributors review it.

Each row represents one synthetic person. Each resource is allocated independently in one step. Fractional units are allowed so the model can represent exact shares without introducing a rounding rule in the first version.

| Person | Water need | Food need | Energy need |
| --- | ---: | ---: | ---: |
| A | 2 | 2 | 1 |
| B | 2 | 3 | 2 |
| C | 3 | 2 | 1 |
| D | 3 | 3 | 2 |
| E | 4 | 3 | 2 |
| F | 4 | 4 | 3 |
| **Total** | **18** | **17** | **11** |

Compare two supply conditions, applying the same percentage to each resource category:

| Scenario | Supply rule | Water | Food | Energy |
| --- | --- | ---: | ---: | ---: |
| Baseline | 80% of total stated need | 14.4 | 13.6 | 8.8 |
| Supply shock | 50% of total stated need | 9 | 8.5 | 5.5 |

These percentages are convenient test settings, not claims about a realistic crisis. Later versions can vary them as experiment parameters.

## Provisional allocation rules (for review)

1. **Equal amount per person:** divide the available amount equally among all six people, cap each allocation at that person's stated need, then redistribute any remainder equally among people who still have unmet need. Repeat until supply is exhausted or all needs in that category are met.
2. **Equal proportion of stated need:** allocate the same percentage of each person's need in that resource category. With a single resource category and no other constraints, this is equivalent to proportional-to-need allocation; it should be represented as one rule, not counted as two competing rules.

The rules deliberately encode different ideas of equality: equal quantities per person versus equal shares of stated need. Neither should be labeled “fair” by the model. A later proposal may add an explicit priority rule, but it should specify whose needs receive priority and why before implementation.

## Provisional outputs

For every rule and supply scenario, report allocations and unmet needs per person and resource, plus:

- total need coverage per resource and overall (allocated need divided by stated need);
- the lowest individual coverage and the distribution of individual coverage rates;
- remaining unused supply, which should be zero whenever any need remains under these rules;
- the configuration and rule identifier needed to reproduce the run.

Show the measurements separately. Do not collapse them into a single fairness score or overall winner. The first version should use deterministic arithmetic; random behavior and seeds are unnecessary until a stochastic rule is proposed.

## Candidate allocation rules

The two provisional rules above are the proposed first comparison. They are comparison cases, not endorsements. A priority-based rule remains a possible extension, but it needs a documented priority rationale before it can be modeled. Other rules can be proposed and compared using the same inputs.

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

- Should the provisional six-person needs table and 80%/50% supply settings be adopted, revised, or replaced?
- Should the first comparison use only the two allocation rules above, or add a precisely specified priority rule?
- Should any minimum acceptable needs threshold be included, and what evidence or rationale should define it?
- Which measures should be mandatory in the first report?
- What terms should apply to experiment documentation and any datasets published with results?
