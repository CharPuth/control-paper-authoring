# Control Paper Authoring

[简体中文](README.md) | English

A bundle for drafting, revising, translating, shortening, and organizing control and robotics papers in English and Chinese. Seven installable skills work through nine writing modules. A field profile selects the providers. The supplied profile covers control and robotics; future fields can bind different skills without replacing the control configuration.

[Entry point](skills/control-paper-authoring/SKILL.md) · [Profiles](skills/control-paper-authoring/profiles/index.md) · [Changelog](skills/control-paper-authoring/CHANGELOG.md) · [Extension contract](skills/control-paper-authoring/references/maintenance.md) · [Refactoring audit](AUDIT_20261029.md)

## Quickstart

Install all seven sibling directories under `skills/`. Supply the manuscript or research materials, target language, permitted scope, and content to preserve.

```text
Use $control-paper-authoring to polish the attached English control paper.
Use the control profile, focusing on M03 natural language and M05 vocabulary.
Preserve the methods, equations, data, and citations. Correct a clearly
excessive claim to the scope established by the evidence and report the edit.
Ask before resolving scientific uncertainty or adverse findings that affect
a core conclusion or key comparison.
```

Modules can be requested by name or ID. Existing author confirmations need not be repeated. Invocation syntax, file access, and compilation depend on the host.

## The nine modules

IDs identify stable responsibilities. The [active field profile](skills/control-paper-authoring/profiles/control.md) selects their actual files.

| Module | Responsibility and input | Provider in the control profile |
| --- | --- | --- |
| M01 Structure | Arrange sections from the problem, method, and evidence; shorten or restructure | [structure.md](skills/control-paper-authoring/modules/structure.md) |
| M02 Author narrative | Organize supported strengths and select the narrative focus | [author-voice.md](skills/control-paper-authoring/modules/author-voice.md), using the appropriate anti-defensive skill |
| M03 Natural language | Address defensive prose, loss of the author perspective, obscure word choices, coined phrases, ambiguity, repetition, and chat residue | [natural-language.md](skills/control-paper-authoring/modules/natural-language.md), using the appropriate humanizer |
| M04 Style and sentence patterns | 17 general rules, seven functional groups of sentence frames, and manuscript teaching examples | [control-paper-writing-style](skills/control-paper-writing-style/SKILL.md) |
| M05 Vocabulary | 51 groups of contextual vocabulary, general and manuscript examples, and terminology distinctions | [control-paper-vocabulary](skills/control-paper-vocabulary/SKILL.md) |
| M06 Meaning and evidence | Preserve models, signals, timing, windows, statistical units, and claim scope | [evidence.md](skills/control-paper-authoring/modules/evidence.md) |
| M07 Experiments | Assign roles to completed evaluations and organize comparisons, ablations, figures, and numbers | [experiments.md](skills/control-paper-authoring/modules/experiments.md) |
| M08 Delivery | Captions, notes, numerical display, references, template selection, anonymity, and file checks | [delivery.md](skills/control-paper-authoring/modules/delivery.md) |
| M09 Layout | Definition order, float proximity and ordering, spacing, whitespace, column alignment, and rendered-page checks | [layout.md](skills/control-paper-authoring/modules/layout.md) |

Vocabulary guidance is editorial synthesis, not a field-wide frequency ranking. The new teaching material records 20 abstracts (3,193 English lexical tokens) and six sampled full-text readings across six venues, with a focus on MPC, learning control, navigation, and formations. The two TAC sources and editorial guidance retained from the old provider are documented in [M04 sources](skills/control-paper-writing-style/references/sources.md); the newer corpus is listed in [M05 sources](skills/control-paper-vocabulary/references/sources.md). This migration did not add a large-scale literature study.

At the author’s request, manuscript examples retain their method names, values, and scenarios to explain language choices. Details added in recommended revisions depend on that manuscript’s context. A new paper reuses the linguistic lesson, not those research settings. Both providers distinguish grammatical or collocation problems, terminology or reference problems, and optional improvements; correct originals may be retained.

## What gets read

The entry point establishes scope and chooses a field before loading modules. Requests between modules resolve through that active profile, rather than jumping back to a fixed control implementation.

- Every manuscript-writing task reads the target-language anti-defensive skill through M02 before drafting.
- Drafting and structural revision use M01. Language editing uses M03, which invokes Humanizer in embedded mode and returns final prose unless analysis is requested.
- M04 uses `writing-rules.md` for relevant language rules, `sentence-patterns.md` for drafting or finding a functional frame, and `style-examples.md` for teaching. It does not supply section templates. M05 selects `vocabulary.md`, `contrastive-examples.md`, or `manuscript-examples.md` as needed; ordinary editing does not load every example.
- M06 handles technical, statistical, and claim issues; M07 organizes experiments; M08 handles actual figure, reference, or file-delivery work; M09 handles float placement, spacing, and page layout.
- [TASE source notes](skills/control-paper-authoring/references/tase-source-notes.md), [sentence-pattern sources](skills/control-paper-writing-style/references/sources.md), maintenance instructions, and history are read only for provenance or maintenance tasks.

A version already read in full need not be read again. A new file does not become active merely by appearing in a directory. Calling a skill means reading and applying instructions; the bundle does not include a program that automatically runs every module.

## Resolved writing conventions

Introductions progress from practical tasks and significance to prior achievements, remaining issues and the research question, then the proposed method and validation. Paragraph count follows the material.

Explanations immediately after an English equation must use lowercase `where` in the same sentence, with corresponding punctuation. This is a bundle convention, not an IEEE mandate. Explanatory prose generally avoids dashes; numerical ranges, mathematical notation, and established terms retain meaningful connectors.

Organize a paper around supported strengths. Unrelated weaknesses may be omitted without adding a catalogue of shortcomings. Ask the author before handling adverse findings that affect a core conclusion or key comparison, then establish the positioning and claim scope. Do not hide material facts to manufacture support. Clearly excessive scope may be narrowed and reported; uncertainty requires an author question first.

Third-party skills remain intact. M02 and M03 define their academic adaptations. Facts, terminology, necessary conditions, and the actual venue template take priority over general style advice. New conflicts are not resolved by whichever file happens to be loaded last.

M03 checks four recurring problems: unnecessary defensiveness and self-disparagement, a response or debate voice in manuscript prose, unnecessarily obscure words, and coined or compressed phrases that hide meaning. It restores direct author statements and favors familiar, precise words and explicit relationships. Narrative decisions remain with M02 and vocabulary guidance with M05. Necessary scientific qualifications, meaningful technical contrasts, and accurate terms are preserved; these editing cues do not identify who wrote a text.

Layout priorities are: define concepts before use; keep floats close to their first substantive text reference; group consecutive same-side tables with tables and figures with figures; follow first-reference order; prefer page tops over bottoms; use consistent journal-prescribed internal spacing; eliminate conspicuous whitespace; and align the bottoms of float regions across columns when possible. A float and its first reference may be on adjacent pages, but never have a full page between them. Added text must be supported and relevant. See [M09](skills/control-paper-authoring/modules/layout.md) for the full rules and conflict handling.

## Seven installable directories

| Directory | Role |
| --- | --- |
| `control-paper-authoring` | Entry point, modules, field profiles, maintenance contract, and changelog |
| `control-paper-writing-style` | General rules, functional sentence frames, manuscript examples, and sources |
| `control-paper-vocabulary` | 51 contextual vocabulary groups, general and manuscript examples, and corpus sources |
| `anti-defensive-writing` | Chinese author narrative provider |
| `anti-defensive-writing-en` | English author narrative provider |
| `humanizer` | English natural language, with upstream metadata and maintenance files |
| `humanizer-zh` | Chinese natural language, references, and examples |

Using a companion alone does not load the full orchestration. Start with `control-paper-authoring` for the complete workflow.

```text
skills/control-paper-authoring/
├── SKILL.md
├── CHANGELOG.md
├── profiles/        # Index and field-specific module bindings
├── modules/         # Built-in rules and third-party adaptations
├── references/      # Maintenance and provenance
└── agents/          # UI metadata

skills/control-paper-writing-style/
├── SKILL.md
├── references/      # General rules, functional frames, manuscript examples, sources
└── agents/

skills/control-paper-vocabulary/
├── SKILL.md
├── references/      # Vocabulary, general contrasts, manuscript examples, sources
└── agents/
```

## Change a module or add a field

For an existing rule, name the module and intended change:

```text
Update only M01's introduction guidance in the control profile.
Check conflicts with companion skills and ask me about unresolved choices.
Update the changelog and both READMEs.
```

Layout can be requested separately:

```text
Use M09 in the control profile to adjust the manuscript layout in priority order.
Use the venue template, compile, and inspect all rendered pages.
Any added prose must use the supplied research materials.
```

For a new provider, reference its actual skill rather than copying its full prompt:

```text
Read the vocabulary skill I supplied and integrate it as control's M05
provider. Preserve still-applicable unique rules, ask about conflicts,
and record the change.
```

To add a field, create a separate profile with explicit bindings for all nine modules. It may reuse M02 and M03 while selecting other section, sentence, vocabulary, evidence, experiment, or delivery providers. Keep `control` independent. Vocabulary replacement alone does not establish support for a new field; evidence and evaluation standards may also differ.

Each module has one primary provider. Conditional extensions declare their path, trigger, language, input/output, and supplement-or-replace relationship. Check internal dependencies and resolve conflicts before registration. The [maintenance contract](skills/control-paper-authoring/references/maintenance.md) supplies the fields and procedure. Record actual changes in the [changelog](skills/control-paper-authoring/CHANGELOG.md). Only control is supplied today.

## Optional capabilities

M08 selects available host tools for literature search, citation verification, figures, templates, and Word/PDF/LaTeX delivery. Skills such as `research-lookup`, `citation-management`, `nature-ref-verifier`, `scientific-visualization`, and `venue-templates` are not bundled. An explicit request for Nature style may be adapted with `nature-writing` or `nature-polishing` after checking its relationship with the active modules.

The writing instructions themselves need no Python, Node.js, or project-specific API key. Running an AI, editing files, compiling, and browsing require host capabilities. Report missing optional capabilities and continue independent work; do not install them automatically or claim unperformed checks.

## Installation


### Codex: install the complete bundle manually

1. Select **Code → Download ZIP** on this GitHub repository and extract it, or clone the repository.
2. Copy all seven directories from `skills/` into the user skills directory, `~/.agents/skills/`. On Windows this is typically `C:\Users\YOUR_USERNAME\.agents\skills\`.
3. Keep the directories as siblings. If skills with the same names already exist, compare or back up those versions before updating them.
4. Invoke `control-paper-authoring` in the skill selector or a new conversation. If it does not appear, check the directory layout and restart Codex.

The installed layout should be:

```text
~/.agents/skills/
├── control-paper-authoring/SKILL.md
├── control-paper-writing-style/SKILL.md
├── control-paper-vocabulary/SKILL.md
├── anti-defensive-writing/SKILL.md
├── anti-defensive-writing-en/SKILL.md
├── humanizer/SKILL.md
└── humanizer-zh/SKILL.md
```

Copying the entire repository into the skills directory leaves an extra `skills/` level. The main skill reads companions through paths such as `../skill-name/SKILL.md`, so keep the seven skill directories at the same level.

For use within one code repository, install them under that repository's `.agents/skills/`. See the [official OpenAI skill documentation](https://learn.chatgpt.com/docs/build-skills) for local discovery and invocation details.

### Upgrading an older bundle

Replacing the M04 and M05 providers changes the complete bundle from six directories to seven. Back up or compare custom changes, then install the seven directories above. After verifying the new configuration, move the old `ieee-control-writing` out of the host’s skill-discovery directory to avoid stale invocations. Do not simply overlay the new files on the old bundle.

Reusable sentence frames and missing collocations have migrated to the new providers, and the author’s manuscript examples remain. The from/to/by examples now distinguish an endpoint from an amount of change. Both new providers require lowercase `where` for post-equation explanations, whether used independently or through the entry point.

### Codex: ask the installer

Provide the current GitHub repository URL to Codex and explicitly request all seven skills:

```text
Use $skill-installer to install these seven directories from skills/ in
the repository URL I provided: control-paper-authoring,
control-paper-writing-style, control-paper-vocabulary,
anti-defensive-writing, anti-defensive-writing-en,
humanizer, and humanizer-zh. Keep them as sibling directories.
If a skill already exists, compare versions and preserve local changes.
```

### Other AI tools

Place the seven directories in the tool's supported local skill location, preserve the directory relationships, and use that tool's invocation syntax. A general chat interface needs access to the full instructions and required references to follow this workflow. Whether uploading a ZIP installs a skill depends on the platform.


## Delivery, sources, and license

Return usable manuscript text or changes in the designated files. When requested, provide location, original, specific issue, and revision. Keep internal questions and editing history outside submission prose. Report actual checks; prose editing does not itself trigger new research experiments.

The guides are editorial syntheses, not official IEEE/TASE standards, and do not guarantee acceptance or AI-detector outcomes. Original material uses [MIT](LICENSE). Third-party copyright and license notices remain intact; see [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).
