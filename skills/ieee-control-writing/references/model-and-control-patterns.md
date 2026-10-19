# Models, Control Design, and Implementation

These are original editorial frames, not quotations or mandatory IEEE formulas. Square-bracketed fields identify facts to supply from the manuscript; never leave them in submission text or fill them with invented details. Retain the manuscript's notation and numbering.

## 1. Introduce the plant and its variables

**Function:** Identify the system before presenting equations.

- "Consider the nonlinear system [equation]."
- "The dynamics of [system] are described by [equation]."
- "Here, [symbol] denotes the state vector, and [symbol] denotes the control input."

Use "consider" to introduce a mathematical problem; use a direct system description for an already introduced vehicle or apparatus. Explain dimensions and known or unknown quantities where they matter. Do not substitute a compact model for a detailed one unless their equivalence is established in the supplied content.

## 2. Separate kinematics from dynamics

**Function:** Explain what each equation block describes.

- "The position and attitude kinematics are given by [equations]."
- "The translational and rotational dynamics are written as [equations]."
- "The simulation uses the full [model description], whereas the controller uses [reduced model description]."

Name the relationship between the full model and the control model. Do not call kinematic relations force-balance equations or confuse the number of states with the number of degrees of freedom. A change from a full model to a local model is a technical distinction, not a stylistic detail.

## 3. Define vectors and scalar quantities

**Function:** Introduce a mathematical object with a clear name.

- "The actuator input vector is defined as [equation]."
- "Let [symbol] denote [quantity]."
- "The components of [vector] are [component meanings], respectively."

Use "defined as" for a definition, not for an empirical observation or a relation that requires derivation. Ensure that "respectively" has an unambiguous one-to-one correspondence. Repeat a short technical noun when a pronoun would leave the object unclear.

## 4. Specify coordinate frames and transformations

**Function:** Identify the frame before and after a rotation.

- "The force command [symbol] is expressed in [frame]."
- "The rotation matrix [symbol] maps vectors from [source frame] to [destination frame]."
- "The corresponding [destination-frame] force command is obtained as [equation]."

A command vector can contain signals expressed in different frames. Do not label the entire vector as body-frame merely because its moment components are body-frame quantities. Preserve axis directions, rotation order, and the distinction between a vector and its coordinate representation.

## 5. Define measurement references and offsets

**Function:** Distinguish the sensor value, a baseline, and a relative displacement.

- "The measured coordinate [symbol] is positive in the [direction] direction."
- "The baseline [symbol] is recorded while [confirmed reference condition]."
- "The displacement relative to this baseline is [expression]."

Use the actual sensing definition. A motion-capture coordinate is not automatically an immersion depth, and a measured coordinate is not automatically baseline-subtracted. Mention a physical reference point only if it is defined by the measurement setup. Preserve the relation between the plotted quantity and its command offset.

## 6. State assumptions and local approximations

**Function:** State the conditions under which a model is used.

- "For [operating regime], [quantity] is assumed to be [property]."
- "Neglecting [specified terms], [equation] reduces to [equation]."
- "Near [operating point], the [channel] dynamics are approximated by [equation]."

Keep approximation language when it carries technical meaning. Do not replace "approximated by" with "equals" to make a claim sound stronger. Avoid routine disclaimers after every assumption; give its relevant domain and proceed with the design.

## 7. Introduce local channels and control inputs

**Function:** Identify the input-output relation without vague action verbs.

- "The local [output] model uses [symbol] as the control input."
- "The [first] and [second] channel models use [input one] and [input two], respectively, as control inputs."
- "The term [symbol] represents [specific load, uncertainty, or coupling effect]."

Prefer a named model and input over "the force drives the state" when the latter obscures the channel definition. Distinguish additive loads from input effectiveness: an input coefficient and an additive disturbance do not have interchangeable meanings.

## 8. State the control objective

**Function:** Connect the problem to the variables the controller regulates.

- "The objective is to track [reference] while maintaining [specified condition]."
- "We design [controller] to reduce [defined errors] over [stated operating range]."
- "The controller adjusts [commands] to compensate for [modeled effects]."

Do not turn a design objective into a proved result. "The objective is to achieve convergence" and "the error converges" make different claims. Name the regulated quantities rather than using "enhanced performance" without an object.

## 9. Introduce a reference model and tracking errors

**Function:** Define the desired dynamics and the relevant error.

- "The desired response is specified by [reference model]."
- "The reference-model state is denoted by [symbol]."
- "The model-tracking error is defined as [expression]."
- "The command-tracking error is defined as [expression]."

Keep reference-model states distinct from user commands. Do not combine the last two frames unless the paper actually defines the same error. Explain initialization in the implementation section if it is part of the supplied protocol.

## 10. Describe the controller architecture

**Function:** Name the interfaces and the contribution of each block.

- "The outer-loop controller computes [force commands] from [measurements and references]."
- "The attitude controller generates [moment commands]."
- "The allocator maps [command vector] to [actuator inputs]."
- "The adaptive term compensates for [specified effects] at the [named interface]."

Explain why the architecture addresses the stated control problem, rather than listing its blocks as contributions. Use "existing" or "retained" when the attitude controller or allocator is not a newly proposed component. Do not change the signal path to obtain a simpler sentence.

## 11. Present a control law or a design choice

**Function:** Distinguish the proposed rule from quantities chosen within it.

- "We choose the control input as [equation]."
- "The proposed control law is given by [equation]."
- "The gain [symbol] is selected to satisfy [condition]."
- "The nominal term [symbol] compensates for [known effect], while [symbol] accounts for [specified uncertainty]."

Use a precise role for each term. "Accounts for" or "compensates for" should identify an actual modeled effect, not serve as a generic claim of robustness. A selected gain is not necessarily an optimally tuned gain.

## 12. Introduce regressors and delayed signals

**Function:** Explain the construction and time index of the regression vector.

- "The regressor is constructed from [named signals]."
- "At sampling instant [index], the regressor uses the current [measurements] and the previous [controller outputs]."
- "The stored value [symbol] is updated after [specified operation]."

Keep previous controller outputs distinct from predicted forces, measured forces, actuator commands, and applied forces. Do not introduce saturation handling, filters, or prediction stages that are absent from the algorithm. The word "previous" is part of the method when it defines a sample delay.

## 13. Describe adaptive estimation and projection

**Function:** Identify what changes online and how constraints are imposed.

- "The parameter estimates are updated according to [equation]."
- "The update direction is given by [equation]."
- "The estimates are projected onto [defined set]."
- "The learning rate associated with [component] is set to zero."

Do not conflate an update direction with the complete continuous-time law or discrete update. Preserve inactive components. A lower bound that prevents division by zero does not by itself establish stability, parameter convergence, or disturbance rejection.

## 14. Present an algebraic derivation

**Function:** State the operation that leads to the next expression.

- "Substituting [expression] into [equation] gives [result]."
- "Using [identity] and [equation], we obtain [result]."
- "Collecting the terms associated with [quantity] yields [equation]."
- "It follows from [stated relation] that [conclusion]."

Use "it follows" only when the referenced relation supports the conclusion. Do not describe a definition as a derivation or replace an approximation with an exact identity. "Gives," "yields," and "obtain" are ordinary technical verbs; no synonym rotation is required.

## 15. Describe initialization and resets

**Function:** Make trial boundaries and switching behavior reproducible.

- "At the start of each trial, [state or estimate] is initialized to [confirmed value or rule]."
- "The reference-model states are initialized using the current measured values."
- "The reference-model states are not reset when [command] changes."
- "The same parameter-estimate initial conditions are used in [specified trial groups]."

Use only confirmed rules. Separate controller states, reference-model states, parameter estimates, and fixed design parameters. Initialization at the beginning of a trial does not imply reinitialization at every command switch.

## 16. Explain the sampled implementation

**Function:** State the implemented sequence without compressing away operations.

- "At each sampling instant, [controller] first computes [quantity]."
- "The derivative estimate is computed from [measurements] using [specified method]."
- "The update is integrated using [specified numerical rule] and then [specified next operation]."

Preserve the actual operation order. A moving-window derivative is not automatically a particular filter or fitted estimator. Give a window length or sample period only when supplied. Do not use "hardware sampling" when the intended quantity is the controller update interval or a sensor sampling interval.

## 17. State theoretical results only when present

**Function:** Separate theorem conditions, results, and proof steps.

- "Under Assumptions [identifiers], [precisely stated result] holds."
- "Consider the Lyapunov function [equation]."
- "Differentiating [function] along the system trajectories gives [equation]."

Use these frames only for theory actually supplied and retained in the manuscript. Do not add theorem-like claims to a paper that reports a controller and experiments without such a proof. Boundedness, asymptotic convergence, exponential convergence, and practical stability are different results.
