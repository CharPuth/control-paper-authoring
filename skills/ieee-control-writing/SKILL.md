---
name: ieee-control-writing
description: "Draft, revise, translate, and polish English control-systems papers using clear terminology and scenario-specific sentence patterns drawn from IEEE control-paper examples. Use for requests about IEEE/TAC academic style, common control-paper sentence structures, plain academic English, natural manuscript language, or preserving technical content during language editing. Covers models, controllers, implementation, experiments, abstracts, introductions, and conclusions."
---

# IEEE Control Paper Writing

Write precise, readable control-engineering prose. Choose sentence structures by what the sentence must do: define, assume, derive, design, implement, compare, or interpret. A consistent style is desirable; mechanical repetition and forced variation are not.

This is an editorial skill, not an official IEEE style standard or a guarantee of journal quality. Its initial source corpus contains two IEEE Transactions on Automatic Control papers. See [source-basis.md](references/source-basis.md) for the sources, limits, and distinction between observed wording and original editorial patterns.

## First steps

1. Determine the requested operation: language-only revision, translation, new drafting from supplied facts, or substantive restructuring. Default to language-only revision when asked to polish existing text.
2. For English manuscript writing, read the companion `../anti-defensive-writing-en/SKILL.md` before drafting unless it has already been read in the current context. Resolve this path relative to the current skill directory. Respect host restrictions on repeated file reads. If unavailable, do not claim to have used it. This skill remains usable without silently installing dependencies.
3. Briefly identify the writing skills being used. Keep this process note outside the manuscript.
4. Establish a compact fact ledger from the supplied text and author confirmations: notation, coordinate frames, method architecture, assumptions, timing, parameter roles, evaluation windows, statistics, and claims. Preserve established answers rather than repeatedly asking for independent verification.
5. Read the relevant references below. Use their sentence frames as options, not a fill-in template that every paragraph must follow.

## Reference routing

| Writing task | Reference |
| --- | --- |
| Notation, dynamics, controller design, equations, implementation | [model-and-control-patterns.md](references/model-and-control-patterns.md) |
| Experimental setup, comparisons, metrics, results, captions | [experiments-and-results.md](references/experiments-and-results.md) |
| Abstract, introduction, related work, contributions, discussion, conclusion | [manuscript-sections.md](references/manuscript-sections.md) |
| Plain vocabulary, natural sentence structure, before/after examples, editing passes | [natural-style-and-editing.md](references/natural-style-and-editing.md) |
| Source attribution, dated quartile evidence, extending the corpus | [source-basis.md](references/source-basis.md) |

## Content-preservation contract

- Preserve scientific content during language-only editing: equations, variable meanings, inequalities, assumptions, algorithm order, sampling indices, experimental facts, numbers, units, citations, and claim scope.
- Do not change a controller output into an applied actuator force, a model-tracking error into a command-tracking error, or a parameter-update direction into a complete update law.
- Preserve qualifiers that carry meaning, including local, nominal, measured, estimated, previous, mean, per-condition, and under the stated assumptions.
- Accept author-confirmed research facts as writing inputs. Do not insert internal verification questions or statements of personal uncertainty into submission prose merely because the agent has not rerun the experiments.
- Do not invent results, guarantees, optimal tuning, matched bandwidths, statistical significance, experimental procedures, or contributions. Do not hide conditions or findings that materially change the interpretation of the main result.
- If a proposed improvement would change the science or requires an unresolved fact, leave the affected claim unchanged and ask one focused question outside the manuscript. Continue editing unrelated passages.
- Do not import the reference papers' assumptions, algorithms, stability results, or citations into the user's manuscript merely because their wording was consulted.

## Voice and sentence selection

Use the research authors' perspective. State the method, action, object, and result directly. Prefer common control-engineering terms over ornamental substitutes, but retain a long word when it is the established and precise term.

Choose the verb according to the logical operation:

| Operation | Typical wording |
| --- | --- |
| Definition | is defined as; denotes |
| System description | is described by; is given by |
| Assumption | is assumed to; we assume that |
| Design choice | is selected as; we choose |
| Derivation | substituting ... into ... gives; it follows from ... that |
| Implementation | is computed from; is updated using |
| Observation | Figure ... shows; the mean ... is lower than |
| Interpretation | indicates ... under the tested conditions |

Use active and passive constructions according to emphasis. Repeat a conventional equation lead-in when it fits. Do not rotate synonyms, alternate voices, insert conversational wording, or vary sentence length merely to look human. Pronouns are acceptable when their referents are immediate and unambiguous.

## Editing procedure

1. Read each necessary manuscript source once when the host requires a one-pass file workflow. Plan all changes from that source snapshot.
2. For a full-manuscript language revision, use three distinct passes over the available text: terminology and collocations; sentence structure and references; technical meaning and prose-to-equation/result consistency. For a short passage, apply these lenses proportionately without inventing a multi-pass ceremony.
3. Change only identified problems. Do not rewrite every sentence or make the paper uniformly short, uniformly passive, or uniformly ornate.
4. Before applying edits, compare each candidate with its source for preserved meaning. If the user authorized only language changes, separate any substantive suggestions from the edits.
5. Apply edits in the file workflow permitted by the host. Do not create extra reports, modify global instructions, change figures, recalculate statistics, compile documents, or run validators unless requested or otherwise authorized.
6. Report what was actually done. When a change list is requested, provide location, original sentence, specific problem, and revised sentence. Do not claim a number of completed passes, independent reviewers, or layout checks that did not occur.

## Delivery

Return polished manuscript text or update the requested files. Keep explanations, unresolved questions, and editorial notes outside submission prose. State the revision scope briefly. Never promise acceptance, a quartile-level standard, or text that is guaranteed to evade AI detection.
