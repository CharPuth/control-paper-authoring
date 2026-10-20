# Sentence Patterns by Manuscript Section

Use these as a menu of rhetorical functions. A paragraph does not need every function, and a section need not repeat a fixed sequence. The frames are original examples, not quotations from the source papers.

## Abstract

Identify the specific control difficulty, the method's action, the evidence, and the supported result. Avoid a broad opening about rapid technological development when the actual problem can be stated directly.

- Problem: "During [operation], changes in [physical quantities] affect [controlled behavior]."
- Method: "We develop [controller] that adjusts [commands or parameters] to compensate for [specified effects]."
- Architecture: "The controller operates at the [interface] and retains [existing components]."
- Evaluation: "The method is evaluated in [simulation study] and [experimental study]."
- Result: "Across [tested conditions], [method] reduces [specified metric] by [reported amount]."

Use only the moves needed for the paper. Do not force every abstract into four identical sentences. Avoid "a novel, robust, efficient framework" unless each property has a concrete, supported meaning. In language-only revision, do not invent a numerical result to make the abstract appear stronger.

## Introduction: practical significance, prior work, research problem, and approach

Organize the introduction in this order: actual tasks and practical significance; related research and established achievements; remaining issues and the present research question; the proposed method and validation plan. Each part may occupy one or more paragraphs, depending on the material and venue requirements.

### 1. Actual tasks and practical significance

Start with the applications, why the tasks matter, and the relevant capabilities of the platform or system. Establish the practical context before narrowing to a specific technical problem.

- "[Application task] requires [documented capability] under [conditions]."
- "[Platform class] supports [application] through [documented capability]."
- "The ability to [capability] is relevant to [specific practical need]."

For an aerial-aquatic vehicle paper, this can mean explaining documented application needs and how cross-medium capabilities serve them before reviewing platforms and control methods. Use only supported applications and capabilities. A statement that a topic has attracted growing interest needs literature support and should lead to concrete practical relevance. Other platforms follow the same progression with their own tasks and capabilities.

### 2. Related research and established achievements

Explain what prior studies developed or demonstrated and how those achievements relate to the task. Group references by relevant research direction or technical approach. Where appropriate, progress from platforms and systems to the control methods directly relevant to the paper.

- "[Authors] developed [platform or method] for [task]."
- "The system in [citation] achieves [documented capability] using [approach]."
- "For [related control task], [authors] proposed [method] to address [effect]."
- "These studies establish [supported capability] under [reported conditions]."

Connect each citation to a specific method, capability, result, or assumption. Distinguish retained platform, sensing, or control components from the present contribution. Select architecture and actuator details for their relevance to the application or the research question that follows.

### 3. Remaining issues and the present research question

Build on the established achievements to identify an unresolved issue under the target task or operating conditions. Explain when it occurs, what it affects, and why existing work does not sufficiently address that particular requirement. Use physical causes and control consequences to make the research question precise.

- "Under [target condition], [supported unresolved issue] remains."
- "Changes in [physical quantity] affect [controlled behavior] during [operation]."
- "The resulting problem is to [control objective] while [design requirement]."

Keep the mechanism consistent with the model and the evidence. Attribute limitations to sources that support them. If the literature review does not establish a field-wide gap, state the paper's design problem. Avoid assigning a weakness to every cited study or claiming "no existing method" or "for the first time" without verification.

### 4. The proposed method and validation plan

Introduce the method in direct response to the research question, explain its main idea, and summarize supported contributions and the validation performed. State what the simulations, physical experiments, or other completed evaluations examine. Leave detailed implementation and experimental procedures to their respective sections. An outline of the remaining paper is optional.

- "To address [research problem], we develop [method] that [key action]."
- "The method accounts for [specified effects] through [supported mechanism]."
- "We evaluate [property] in [simulation study] and examine [capability] in [experimental study]."

Select the contribution count and validation types from the actual research. These frames do not authorize adding experiments, mechanisms, or claims absent from the supplied materials.

## Contributions

- "We formulate [control problem] at the [interface], which allows [supported architectural consequence]."
- "We develop [method] to compensate for [specified effects] as [operating conditions] change."
- "We evaluate [method] over [conditions] without retuning [specified design parameters]."

A contribution should name an action and explain its relevance. A list of a reference model, a regressor, and a projection operator does not by itself explain the method's contribution. Do not claim every retained component as new. Use the number of contributions the evidence supports, not a mandatory three-item list.

## Section openings and transitions

- "This section introduces [model or problem]."
- "Using the channel models in [section], we design [controller]."
- "The resulting [command] is passed to [next component]."
- "We next evaluate [specific property] under [conditions]."

Use a transition when it explains dependency or sequence. Omit repetitive announcements if the heading already provides the necessary context. Avoid "Building upon the aforementioned comprehensive framework" when "Using the model in Section II" identifies the actual connection.

## Discussion: interpretation tied to evidence

- "The reduction in [metric] is consistent with [mechanism already established in the paper]."
- "The results indicate [supported behavior] over [tested range]."
- "The improvement is largest in [condition or channel], where [reported observation]."

Distinguish a measured effect from its interpretation. Use causal language only when the analysis or experiment establishes the causal link. Do not turn a plausible explanation into a verified mechanism. Avoid stacking "suggests," "appears," and "may" around a directly measured result.

## Scope and necessary conditions

- "The model assumes [necessary condition]."
- "The evaluation covers [actual range]."
- "[Reported result] holds under [stated conditions]."

State necessary conditions at their relevant location rather than appending generic self-doubt to every result. Do not add an inventory of untested scenarios unless requested or essential to interpreting the contribution. Conversely, do not delete a condition that the main claim needs in order to be true.

## Conclusion

- "We developed [method] for [specific control task]."
- "The controller adjusts [commands] to account for [supported effects]."
- "The experiments showed [specific result] across [tested conditions]."
- "Future work will address [author-approved next task]."

Summarize the contribution and the strongest supported evidence without repeating the abstract word for word. Do not introduce new experiments or claims. A future-work sentence is optional; do not invent commitments or weaken a complete conclusion with an unrelated list of possible extensions.
