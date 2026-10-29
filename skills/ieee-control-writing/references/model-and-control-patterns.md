# Models, control design, and implementation

M04 sentence frames. These are original editorial examples; their signals, conditions, and operations must match the current research. For technical distinctions use the active profile's M06. Source provenance is in [source-basis.md](source-basis.md).

## Objects, equations, and symbols

- "Consider the nonlinear system [equation]."
- "The dynamics of [system] are described by [equation]."
- "The actuator input vector is defined as [equation]."
- "Let [symbol] denote [quantity]."
- "The components of [vector] are [meanings], respectively."

For explanations of symbols, parameters, or conditions immediately after an English equation, continue the same sentence with lowercase `where`:

```text
The dynamics are given by
[equation],
where [symbol] denotes [quantity] and [symbol] is [quantity].
```

Adjust the equation's ending punctuation to the sentence, normally a comma; do not leave a period before this continuation or add a comma mechanically after `where`. Do not use `Here` for this post-equation role. This is the bundle's convention, not an IEEE mandate, and does not ban other uses of `here` or `hereafter`.

## Model roles, coordinates, and measurements

- "The position and attitude kinematics are given by [equations]."
- "The translational and rotational dynamics are written as [equations]."
- "The simulation uses [full model], whereas the controller uses [local model]."
- "The rotation matrix [symbol] maps vectors from [source frame] to [destination frame]."
- "The force command [symbol] is expressed in [frame]."
- "The measured coordinate [symbol] is positive in the [direction] direction."
- "The baseline [symbol] is recorded while [reference condition]."
- "The displacement relative to this baseline is [expression]."

## Assumptions, approximations, and channels

- "For [operating regime], [quantity] is assumed to be [property]."
- "Neglecting [specified terms], [equation] reduces to [equation]."
- "Near [operating point], the dynamics are approximated by [equation]."
- "The local [output] model uses [symbol] as the control input."
- "The term [symbol] represents [specified load, uncertainty, or coupling]."

## Objectives, architecture, and errors

- "The objective is to track [reference] while maintaining [condition]."
- "The desired response is specified by [reference model]."
- "The model-tracking error is defined as [expression]."
- "The command-tracking error is defined as [expression]."
- "The outer-loop controller computes [commands] from [measurements and references]."
- "The attitude controller generates [moment commands]."
- "The allocator maps [command vector] to [actuator inputs]."

Use each frame for its actual signal and role. The two error definitions are alternatives only when the manuscript defines them as such.

## Design, estimation, and derivation

- "We choose the control input as [equation]."
- "The gain [symbol] is selected to satisfy [condition]."
- "The nominal term [symbol] compensates for [known effect], while [symbol] accounts for [specified uncertainty]."
- "The regressor is constructed from [named signals]."
- "The parameter estimates are updated according to [equation]."
- "The update direction is given by [equation]."
- "The estimates are projected onto [defined set]."
- "The learning rate associated with [component] is set to zero."
- "Substituting [expression] into [equation] gives [result]."
- "Collecting the terms associated with [quantity] yields [equation]."
- "It follows from [stated relation] that [conclusion]."

Definitions, design choices, calculations, and derived consequences have different meanings; select the corresponding verb rather than a stylistic synonym.

## Initialization and sampled implementation

- "At the start of each trial, [state or estimate] is initialized to [confirmed value]."
- "The reference-model states are not reset when [command] changes."
- "At sampling instant [index], the regressor uses the current [measurements] and the previous [controller outputs]."
- "The derivative estimate is computed from [measurements] using [specified method]."
- "The update is integrated using [rule] and then [actual next operation]."
- "The stored value [symbol] is updated after [specified operation]."

These frames do not prescribe a reset policy, sample delay, derivative estimator, or algorithm order. Keep the implemented sequence.

## Theory, when supplied

- "Under Assumptions [identifiers], [precisely stated result] holds."
- "Consider the Lyapunov function [equation]."
- "Differentiating [function] along the system trajectories gives [equation]."

Use only retained theory with its conditions. Stability and convergence distinctions belong to the active profile's M06, not to sentence polishing.
