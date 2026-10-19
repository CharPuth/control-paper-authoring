# Plain Academic English Without Mechanical Writing

Naturalness comes from matching wording to meaning, not from trying to defeat an AI detector. A control paper may legitimately use a consistent style throughout. Standard equation lead-ins can repeat without becoming a problem.

## Vocabulary: familiarity and precision, not word length

Retain established terms such as regressor, reference model, input effectiveness, projection operator, parameter estimation, Lyapunov function, controllability, and asymptotic stability when they name the intended concept. A shorter substitute is worse if it loses that concept.

The following are contextual alternatives, not a forbidden-word list:

| Wording to examine | Often clearer alternative | Preserve this distinction |
| --- | --- | --- |
| utilize | use | Retain a technical fixed expression when appropriate. |
| facilitate improved tracking | improve tracking; enable a named action | State what the method actually does. |
| ameliorate the error | reduce the error | Identify the error or statistic. |
| leverage measured information | use the measured states | Do not rename the available measurements. |
| comprehensive validation | specify the tests performed | Do not imply completeness. |
| superior performance | lower mean RMSE in a named condition | Do not silently replace a broader claim in a language-only edit. |
| seamless integration | connects to the existing interface | Avoid adding an unsupported ease-of-use claim. |
| operational regimes | operating conditions | Retain regime if it denotes a distinct physical mode. |
| adaptive compensation mechanism | adaptive term or controller | Choose the actual mathematical or implemented object. |
| hardware | pool experiments, bench tests, or physical components | Resolve the intended referent; do not ban legitimate hardware terminology. |
| acts on | adjusts, computes, updates, or supplies | Match the verb to the operation. |
| driving speed and depth | used as the control inputs of the speed and depth models | Preserve the input-output relationship. |
| maximum error | maximum per-condition RMSE, if that is the metric | Do not change the underlying statistic. |

Do not replace every occurrence of a repeated word. Technical consistency often matters more than lexical variety. Do not replace "controller" with "scheme," "framework," and "mechanism" in rotation if all refer to the same object.

## Sentence structure: choose by information function

- Use a direct subject-verb-object sentence for a controller action.
- Use a passive construction when the defined or computed quantity is the topic.
- Use a short subordinate clause when it carries a necessary condition.
- Split a sentence when it combines several different operations or obscures the main relation.
- Keep a compound sentence when its parts describe a real contrast or dependency.
- Use a pronoun when its referent is clear; repeat the technical noun when several plausible referents intervene.

There is no target sentence length, passive-voice percentage, synonym quota, or required mix of openings. Uniform style is allowed. Flexibility means selecting a suitable structure, not alternating structures according to a schedule.

## Before-and-after examples

These are generalized editing examples, not claims about a particular experiment. A candidate replacement is valid only if the supplied manuscript has the stated meaning.

### A. Ambiguous object before an equation

Original: "Together with the moment commands, they form [equation]."

Problem: The reader must recover both the antecedent of "they" and the name of the resulting object.

Revision: "The force and moment command vector is defined as [equation]."

"They form" is grammatical and is not prohibited in IEEE papers. Replace it here because the definition is clearer with an explicit object, not because the phrase is inherently nonacademic.

### B. Vague action

Original: "Adaptation acts on the force commands before allocation."

Revision: "The adaptive controller adjusts the force commands before allocation."

The revised subject and verb identify the component and its action without adding a new mechanism.

### C. Compressed input-output description

Original: "We use local models with the longitudinal force driving speed and the vertical force driving depth."

Revision: "The local speed and depth models use the longitudinal and vertical force commands, respectively, as control inputs."

Use "commands" only if the source quantities are command signals. If they are measured or applied forces, retain that meaning instead.

### D. Two distinct model roles

Original: "The simulator retains all six degrees of freedom; the outer loop controls speed and depth."

Revision: "The simulation uses the full six-degree-of-freedom model. The outer loop controls speed and depth."

The revision names the model directly. The semicolon was not incorrect; the two short sentences make the different roles easier to follow.

### E. Experiment versus physical components

Original: "Simulation and hardware use separate parameter sets."

Revision: "Simulation and pool experiments use separate parameter sets."

Use "pool experiments" only for experiments actually conducted in a pool. For another platform, choose its accurate experimental setting. Retain "hardware" when discussing processors, sensors, electronics, or hardware-in-the-loop evaluation.

### F. Explicit statistical comparison

Original: "Method A gives lower mean depth RMSE than Method B in each case."

Revision: "The mean depth RMSE of Method A is lower than that of Method B in each case."

The revised subject is the measured statistic. The original is not universally wrong; use the revision when it improves local consistency and clarity.

### G. Unclear parameter category

Original: "The parameters stay unchanged across the tests."

Revision, if confirmed: "The controller design parameters remain fixed across the tests."

Specifying design parameters prevents confusion with adaptive estimates. If the source does not establish which parameters are fixed, ask instead of choosing a meaning.

### H. Overloaded implementation sentence

Original: "At each sampling instant, the controller constructs the regressor from the measurements and previous output, evaluates the parameter update, and integrates and projects the estimate before computing the new command."

Revision: "At each sampling instant, the controller constructs the regressor from the current measurements and the previous output. It then evaluates the parameter update, integrates and projects the estimate, and computes the new command."

This example illustrates sentence division only. Preserve the actual algorithm order; do not adopt this order for another implementation. "Current" is appropriate only if the original measurements belong to the current sample.

### I. Wordy transition

Original: "Building upon the aforementioned model formulation, the controller design is subsequently presented."

Revision: "Using the model in Section II, we design the controller as follows."

Use the correct section reference. If the heading already establishes the transition, deletion may be clearer than replacement, provided no content is lost.

### J. Nominalization hiding an action

Original: "The computation of the derivative estimate is performed using a moving window."

Revision: "The derivative estimate is computed using a moving window."

Retain the actual estimator description and its supplied window size. Do not replace the method with a different numerical derivative or filter.

### K. Repetition that should remain

Text: "The state error is defined as [equation]. The parameter error is defined as [equation]."

Action: Keep the repeated structure when these are parallel definitions. Do not replace one lead-in with an unusual phrase merely to create variety.

### L. Strong-sounding but incomplete result

Original: "The proposed framework delivers superior performance across diverse scenarios."

Candidate, only when supported: "The proposed controller has a lower mean depth RMSE than the baseline in all tested switching cases."

This is not automatically a language-only replacement: the candidate specifies a metric and scope that the original leaves unstated. Use supplied evidence and author intent to resolve that scope. If it cannot be resolved, flag the sentence outside the manuscript instead of inventing the missing comparison.

## Three-pass full-manuscript procedure

### Pass 1: terminology and collocations

Identify unfamiliar ornament, imprecise shorthand, inconsistent names, and phrases that do not identify an action or object. Retain standard control terms and valid repeated wording. Map each proposed change to a concrete issue rather than a vague AI-likelihood judgment.

### Pass 2: sentence structure and local flow

Check the subject, verb, object, pronoun reference, condition, and logical connection. Separate definitions from consequences and observations from interpretations. Divide overloaded sentences only where that improves comprehension. Do not apply a uniform sentence template to the whole paper.

### Pass 3: meaning preservation and technical fit

Compare source and candidate wording against the available equations, method description, and reported results. Pay particular attention to frames, timing, initialization, reset rules, control interfaces, error definitions, evaluation windows, statistics, and the scope of comparative claims. This is a text-based editing pass, not a new experiment or an independent technical validation.

Use the existing source snapshot when file rereads are restricted. Follow the host's permissions for actual validation, compilation, or visual inspection. A writing request alone does not authorize rerunning experiments or changing their results.

## Change-list format

When requested, use one row per substantive sentence edit:

| Location | Original sentence | Specific issue | Revised sentence |
| --- | --- | --- | --- |
| [section or line] | [source] | [ambiguity, collocation, or structure issue] | [revision] |

Do not label all changes simply "AI-like." Explain the identifiable language problem. Distinguish a necessary correction from an optional stylistic preference. Report actual pass counts and leave unresolved scientific questions outside the submission text.
