# Skiller Instinct

Structured prompts for producing business deliverables with AI assistants. Each one gathers the required input, presents proposals for approval, and only then builds.

| Prompt | Produces | Output | Used by |
|---|---|---|---|
| [`brand-design`](brand-design/prompt.md) | Brand manual | PPTX + MD + logos, isotypes, favicons | `bootstrap-landing-page`, `business-plan`, `corporative-presentation` |
| [`bootstrap-landing-page`](bootstrap-landing-page/prompt.md) | Landing page, no build step | HTML/CSS/JS (Bootstrap) | — |
| [`business-plan`](business-plan/prompt.md) | Business plan | PPTX + MD | — |
| [`corporative-presentation`](corporative-presentation/prompt.md) | Capabilities presentation | PPTX + MD | — |
| [`itil-service-catalog`](itil-service-catalog/prompt.md) | ITIL service catalog | XLSX | `iso27001-process` |
| [`iso27001-process`](iso27001-process/prompt.md) | ISO 27001 procedures | DOCX + BPMN + org chart | — |
| [`nist-maturity-assessment`](nist-maturity-assessment/prompt.md) | NIST CSF 2.0 maturity assessment | XLSX + Chart.js dashboard | — |

## Usage

1. Load `prompt.md` into the assistant (system prompt, skill, or first message).
2. Attach the example files from the same folder.
3. Answer the questions and approve each stage.

Requires an assistant that can run code and generate files.

## Prompt structure

```
<prompt>/
├── prompt.md
│   ├── ---
│   │   name:          short identifier
│   │   description:   what it produces
│   │   version:       semver
│   │   ---
│   ├── # Action       what is built and in which format
│   ├── # Subject      scope, required input and workflow
│   ├── # Purpose      expert roles the model takes on
│   ├── # Examples     reference material
│   ├── # Context      goal and end-user profile
│   ├── # Constraints  mandatory rules and output structure
│   └── # Template     visual or format guide
└── example-*          reference files
```

Folders use `kebab-case`.

---
Pablo Albarrán Arriagada
