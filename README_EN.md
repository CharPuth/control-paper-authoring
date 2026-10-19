# Control Paper Authoring

[简体中文](README.md) | **English**

A skill bundle for writing control and robotics papers in English and Chinese. The main entry point, `control-paper-authoring`, organizes drafting, revision, translation, shortening, and experimental narratives. It combines control-paper sentence patterns, the research authors' perspective, and natural expression while preserving methods, equations, data, and the conditions under which conclusions hold.

Navigation: [Quickstart](#quickstart) · [Capabilities](#capabilities) · [Skill roles](#how-the-six-skills-work-together) · [Reference routing](#when-reference-files-are-read) · [Optional capabilities](#optional-capabilities-and-dependencies) · [Installation](#installation) · [Examples](#usage-examples) · [FAQ](#frequently-asked-questions) · [Sources and license](#sources-and-license)

## Quickstart

1. Download this repository and install **all six skill directories** under `skills/` in an AI tool that supports local skills. See “Installation” for Codex instructions.
2. Provide the manuscript or research materials, target language, requested operation, and content that must remain unchanged.
3. Invoke the main skill. For example:

```text
Use $control-paper-authoring to polish the attached English control paper.
Revise language only. Preserve the methods, equations, data, citations,
and scope of the conclusions. Use the research authors' perspective and
common control-engineering terminology. Return the revised manuscript
text and put representative before/after comparisons outside it.
```

In an interface that selects skills with `@`, select the corresponding skill. Naming `control-paper-authoring` in natural language also makes the requested workflow explicit. Invocation syntax depends on the host tool.

## Capabilities

| Task | Input | Main focus |
| --- | --- | --- |
| Draft from research materials | Confirmed methods, equations, figures, results, and target venue | Connect the problem, method, and evidence across the abstract, introduction, methods, experiments, and conclusion |
| Revise English or Chinese prose | A paragraph or complete manuscript | Resolve vague references, stacked qualifiers, empty modifiers, conversational replies, and awkward technical wording |
| Translate between Chinese and English | Source text, terminology preferences, and target language | Preserve technical meaning and notation while using appropriate academic phrasing |
| Shorten or restructure | Manuscript, length target, and permitted scope | Remove repetition and improve argument order while retaining essential definitions, evidence, and conditions |
| Organize simulations and experiments | Existing purposes, settings, comparisons, curves, and statistics | Distinguish nominal comparisons, module contributions, operating-point tests, command changes, constraint mechanisms, and field demonstrations |
| Refine figure/table text and prepare delivery | Figures, tables, captions, references, and submission requirements | Clarify what belongs in figures, tables, and prose; preserve notation, units, statistical definitions, and necessary reading guidance |

The bundle pays particular attention to distinctions that matter in control papers: controller output versus applied actuator input; reference-model error versus command-tracking error; design intent versus a demonstrated property; bounded parameters versus convergent parameters; and one recorded trial versus repeated-trial statistics. Language editing should preserve these distinctions.

For definitions of symbols, parameters, or conditions immediately after an English equation, the main skill uses lowercase `where` and adjusts punctuation accordingly. This convention applies to post-equation explanations. It does not prohibit other uses of `here`, and it is not presented as a mandatory TASE rule.

## How the six skills work together

| Skill | Role | When the main skill reads it |
| --- | --- | --- |
| [`control-paper-authoring`](skills/control-paper-authoring/SKILL.md) | Sets scope, organizes the authors' narrative, preserves technical meaning, and selects companion rules and references | Drafting, revising, translating, or structuring control and robotics papers |
| [`ieee-control-writing`](skills/ieee-control-writing/SKILL.md) | Selects English sentence patterns for definitions, assumptions, derivation, design, implementation, comparison, and interpretation | English drafting or revision |
| [`anti-defensive-writing`](skills/anti-defensive-writing/SKILL.md) | Organizes Chinese prose around supported contributions and removes unnecessary self-undermining and process narration | Chinese drafting or revision |
| [`anti-defensive-writing-en`](skills/anti-defensive-writing-en/SKILL.md) | Provides the corresponding English narrative rules | English drafting or revision; also referenced by `ieee-control-writing` |
| [`humanizer`](skills/humanizer/SKILL.md) | Identifies formulaic English, empty modifiers, and chatbot residue while preserving facts and the writer's voice | English drafting or revision |
| [`humanizer-zh`](skills/humanizer-zh/SKILL.md) | Identifies formulaic Chinese, stacked modifiers, invented compact phrases, and unnatural wording | Chinese drafting or revision |

Start with the main skill for the complete workflow. It keeps language rules subordinate to research facts, technical meaning, and supported claim scope. Companion skills can also be used independently, but doing so does not automatically apply every control-paper constraint in the main skill.

### What “calling another skill” means

The skills primarily consist of Markdown instructions and reference materials. The main skill asks the AI to read the relevant files and apply their rules to the current task. Calling another skill means reading and following its instructions; the repository does not contain a program that automatically schedules every module.

A complete task normally follows this logic:

1. **Set the scope.** Distinguish language-only editing, translation, drafting, substantive restructuring, and figure/layout work. A request to polish an existing manuscript defaults to language-only revision.
2. **Establish the facts.** Extract methods, notation, settings, results, statistical definitions, and protected content from the materials and author confirmations. Resolve actual conflicts outside the manuscript.
3. **Select the language branch.** Chinese work reads the Chinese anti-defensive and humanizer skills. English work reads the English anti-defensive skill, IEEE control-writing skill, and English humanizer. Mixed-language tasks primarily follow the target language of the submission.
4. **Read the references needed for the task.** A sentence edit may need only language guidance; an experimental section may need structure, evidence, and experimental-narrative references.
5. **Draft or revise.** Describe methods, results, and implications as the research authors. Technical terms, equations, facts, and essential conditions take priority over general style preferences.
6. **Check and deliver.** Check the argument, terminology and phrasing, and preservation of technical meaning. Deliver text, file edits, or a change comparison as requested, and report the checks actually completed.

Files already read in full in the current context do not need to be read again. Automatic skill activation, file access, browsing, and compilation depend on the host tool and the user's authorization.

## When reference files are read

### Six references in the main skill

These files are under `skills/control-paper-authoring/references/`.

| File | Read when | Contents |
| --- | --- | --- |
| [`author-voice-and-language.md`](skills/control-paper-authoring/references/author-voice-and-language.md) | Revising author voice, English/Chinese language, or formulaic expression | Author perspective, explicit objects and actions, common terms, natural sentences, and language checks |
| [`paper-structure-and-patterns.md`](skills/control-paper-authoring/references/paper-structure-and-patterns.md) | Drafting sections from abstract to conclusion, or restructuring with authorization | Section functions and optional sentence frames; full experimental-section work also points to the TASE narrative reference |
| [`tase-experiment-narrative.md`](skills/control-paper-authoring/references/tase-experiment-narrative.md) | Organizing validation, selecting numbers for prose, or interpreting ablations and comparisons | Roles of experiments, local interpretation and section summaries, figure/table division, and traceable TASE examples |
| [`control-semantics-and-evidence.md`](skills/control-paper-authoring/references/control-semantics-and-evidence.md) | Working on models, implementation, experimental facts, or comparative claims | Input/error definitions, timing, statistics, mechanism attribution, and claim–evidence alignment |
| [`figures-tables-and-delivery.md`](skills/control-paper-authoring/references/figures-tables-and-delivery.md) | Working on figures, tables, numeric formatting, references, anonymity, or delivery | Captions, metric presentation, actual template requirements, and delivery checks |
| [`revision-lessons.md`](skills/control-paper-authoring/references/revision-lessons.md) | Deciding whether a past editing lesson generalizes, or maintaining the skill | Reusable writing principles versus preferences specific to one manuscript |

### Five IEEE English-writing references

These files are under `skills/ieee-control-writing/references/`. Select them by the function of the current passage; reading all of them is unnecessary for every task.

| File | Read when |
| --- | --- |
| [`model-and-control-patterns.md`](skills/ieee-control-writing/references/model-and-control-patterns.md) | Writing notation, dynamics, controller design, equations, or discrete implementation |
| [`experiments-and-results.md`](skills/ieee-control-writing/references/experiments-and-results.md) | Writing experimental setup, comparisons, metrics, results, or captions |
| [`manuscript-sections.md`](skills/ieee-control-writing/references/manuscript-sections.md) | Writing abstracts, introductions, related work, contributions, discussion, or conclusions |
| [`natural-style-and-editing.md`](skills/ieee-control-writing/references/natural-style-and-editing.md) | Revising vocabulary, sentence structure, or natural academic expression |
| [`source-basis.md`](skills/ieee-control-writing/references/source-basis.md) | Checking sentence-pattern provenance, understanding the corpus, or extending it |

For a full Chinese rewrite or review, `humanizer-zh` also reads [`chinese-ai-patterns.md`](skills/humanizer-zh/references/chinese-ai-patterns.md). A light sentence edit can use the core rules in its `SKILL.md`. The English `humanizer` keeps its principal rules in its own `SKILL.md`.

## Optional capabilities and dependencies

All six core skills are included. The following skills are used only when the task needs them and they are available in the host environment. They are not fixed installation dependencies of this repository.

| Task | Optional skills or capabilities named by the main skill | Purpose |
| --- | --- | --- |
| Literature search or reference revision | `research-lookup`, `citation-management`, `nature-ref-verifier` | Search, manage, or verify literature and bibliographic records |
| An explicit request for Nature-style prose | `nature-polishing`, `nature-writing` | Assist with the requested style and structure while retaining accurate control terminology |
| Figures, templates, and file delivery | `scientific-visualization`, `venue-templates`, `pdf:pdf`, and suitable host tools | Support the actual plotting, formatting, PDF, or other artifact task |

Ordinary language editing does not require installing a larger research toolkit. If an optional skill is unavailable, the main skill requires an accurate statement of available capabilities and continued work on the parts that can be completed.

The writing instructions need no Python, Node.js, or project-specific API key. The host AI still needs a model, and operations such as editing Word files, compiling LaTeX, redrawing plots, or searching literature need suitable host capabilities. This repository contains no manuscripts, experimental datasets, plotting runtime, or compiler.

## Repository structure

```text
control-paper-authoring/
├── README.md
├── README_EN.md
├── LICENSE
├── THIRD_PARTY_NOTICES.md
├── .gitattributes
├── .gitignore
└── skills/
    ├── control-paper-authoring/
    │   ├── SKILL.md
    │   ├── agents/openai.yaml
    │   └── references/                 # Six main-skill references
    ├── ieee-control-writing/
    │   ├── SKILL.md
    │   ├── agents/openai.yaml
    │   └── references/                 # Five English-writing references
    ├── anti-defensive-writing/
    │   ├── SKILL.md
    │   └── LICENSE
    ├── anti-defensive-writing-en/
    │   ├── SKILL.md
    │   └── LICENSE
    ├── humanizer/
    │   ├── SKILL.md
    │   ├── README.md
    │   ├── LICENSE
    │   ├── agents/openai.yaml
    │   ├── scripts/validate-package.py
    │   └── …                          # Preserved upstream maintenance/plugin files
    └── humanizer-zh/
        ├── SKILL.md
        ├── README.md
        ├── LICENSE
        ├── NOTICE
        ├── agents/openai.yaml
        ├── references/chinese-ai-patterns.md
        └── examples/                  # Chinese before/after examples
```

`SKILL.md` defines when a skill applies and how to perform the task. `references/` holds detailed guidance read on demand. `agents/openai.yaml` supplies display metadata and a default invocation prompt. Preserved third-party plugin files belong to their respective component; they do not establish plugin registration for the full bundle.

## Installation

### Codex: install the complete bundle manually

1. Select **Code → Download ZIP** on this GitHub repository and extract it, or clone the repository.
2. Copy all six directories from `skills/` into the user skills directory, `~/.agents/skills/`. On Windows this is typically `C:\Users\YOUR_USERNAME\.agents\skills\`.
3. Keep the directories as siblings. If skills with the same names already exist, compare or back up those versions before updating them.
4. Invoke `control-paper-authoring` in the skill selector or a new conversation. If it does not appear, check the directory layout and restart Codex.

The installed layout should be:

```text
~/.agents/skills/
├── control-paper-authoring/SKILL.md
├── ieee-control-writing/SKILL.md
├── anti-defensive-writing/SKILL.md
├── anti-defensive-writing-en/SKILL.md
├── humanizer/SKILL.md
└── humanizer-zh/SKILL.md
```

Copying the entire repository into the skills directory leaves an extra `skills/` level. The main skill reads companions through paths such as `../skill-name/SKILL.md`, so keep the six skill directories at the same level.

For use within one code repository, install them under that repository's `.agents/skills/`. See the [official OpenAI skill documentation](https://learn.chatgpt.com/docs/build-skills) for local discovery and invocation details.

### Codex: ask the installer

Provide the current GitHub repository URL to Codex and explicitly request all six skills:

```text
Use $skill-installer to install these six directories from skills/ in
the repository URL I provided: control-paper-authoring,
ieee-control-writing, anti-defensive-writing, anti-defensive-writing-en,
humanizer, and humanizer-zh. Keep them as sibling directories.
If a skill already exists, compare versions and preserve local changes.
```

### Other AI tools

Place the six directories in the tool's supported local skill location, preserve the directory relationships, and use that tool's invocation syntax. A general chat interface needs access to the full instructions and required references to follow this workflow. Whether uploading a ZIP installs a skill depends on the platform.

## Usage examples

### 1. Polish Chinese prose

```text
Use control-paper-authoring to revise the following Chinese control-paper
paragraph. Edit language only: reduce empty modifiers, stacked qualifiers,
and wording that reads like a reply to the author. Preserve facts,
equations, data, citations, and essential conditions. Return manuscript-ready
Chinese text and keep editing notes separate.
```

### 2. Translate into English

```text
Use control-paper-authoring to translate the following Chinese methods
section into English for a control-systems journal. Preserve notation,
controller structure, and the order of discrete implementation steps.
Use the fixed terms reference model and control allocation.
Introduce post-equation symbol definitions with where and check punctuation
between the equation and the explanatory clause.
```

### 3. Draft from research materials

```text
Use control-paper-authoring to draft an English abstract and introduction
from the attached methods, equations, and experimental results.
The attachment states the target venue and length requirements.
Establish the research problem, core method, and strongest experimental
evidence before organizing the text. Use only supplied or explicitly
confirmed research facts. List essential missing information outside
the manuscript.
```

### 4. Organize the experimental section

```text
Use control-paper-authoring to restructure the existing simulation and
experimental sections. Read the TASE experimental-narrative reference.
Identify the role of each experiment, select the key numbers for the prose,
and connect the curves to supported mechanism explanations.
Preserve experiment identifiers, results, statistical definitions, and
essential conditions. Do not describe unfinished experiments as completed.
```

### 5. Shorten a manuscript

```text
Use control-paper-authoring to shorten the attached introduction and
discussion by approximately 20%. You may merge repeated arguments and
reorder sentences. Retain the research problem, method distinctions,
key evidence, citation relationships, and conditions affecting the
conclusions. Return the shortened text, then explain the main cuts.
```

### 6. Edit and deliver a file

```text
Use control-paper-authoring to edit the specified LaTeX manuscript.
Revise only the abstract and conclusion. Preserve figures, tables,
equations, numbers, and experiment identifiers. Keep the existing file
structure. If compilation is available, compile the edited document and
check the log. Report the checks actually completed and the output location.
```

File editing, compilation, and layout inspection are performed by host tools. When those operations are needed, specify the deliverable and provide the required source files.

## Inputs and outputs

Provide the information that changes the writing decisions: target language, target venue, current text or research materials, permitted changes, protected content, and whether you want text returned or files edited. Information already established in the conversation should not require repeated confirmation.

Possible deliverables include:

- Manuscript-ready prose.
- Edits to specified files.
- A comparison organized by location, original wording, specific problem, and revision.
- A short list of essential missing facts or actual conflicts, kept outside the manuscript.

The main skill writes from the research authors' perspective. Internal tasks, revision history, and AI verification notes are separated from submission prose. Scientific assumptions, unfavorable results, and scope conditions that matter to the conclusions remain in the appropriate methods and results statements.

## Scope

This project supplies a writing workflow and editorial references. The IEEE sentence guides draw on representative papers and editorial synthesis; the TASE guide draws on selected examples. They are not official IEEE or TASE language standards.

Research facts and technical meaning take priority. Anti-defensive rules help communicate supported contributions and do not authorize hiding data, limitations, or counterexamples that affect a core conclusion. Humanizer rules must not replace accurate terminology, invent facts, or change conclusions.

Acceptance depends on research quality, evidence, and venue requirements. The project does not guarantee acceptance or promise results against AI detectors.

## Frequently asked questions

**Why install six directories?** The main skill selects companions by language and uses paths between sibling directories. Installing the complete set preserves the workflow; copying only the main skill omits companion rules.

**Does every task read every file?** No. The output language selects companion skills, and the task selects references. Files already read in full in the current context need not be reread.

**Do I need Nature, literature-search, or plotting skills?** Ordinary language revision does not need them. They are used only for tasks that require the corresponding capabilities.

**Can language-only revision change methods or data?** The main skill requires preserving scientific meaning and results. Actual conflicts should be raised outside the manuscript; editing cannot silently supply missing research facts.

**Should every Here after an equation be replaced?** The convention covers explanations of symbols, parameters, or conditions immediately after an equation and requires appropriate syntax and punctuation. It does not extend to other uses of `here` or `hereafter`.

**How do I update?** Download the new version, compare all six directories, preserve your changes, and update the bundle. Keep the main skill and its companion references on compatible versions.

## Sources and license

Original project content is released under the [MIT License](LICENSE). Third-party components retain their own licenses and copyright notices.

See [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) for component authors, provenance, and licenses. Original `LICENSE` and `NOTICE` files are preserved with their components. Research-paper attribution is recorded in the relevant references; licensing this repository does not change the rights in those papers.
