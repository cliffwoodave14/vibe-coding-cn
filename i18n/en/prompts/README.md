# 💡 AI Prompt Library (Prompts)

`i18n/zh/prompts/` stores the prompt assets of this repository: **System Prompts** are used to constrain AI's boundaries and taste, and **Task Prompts** drive the development pipeline of "demand clarification → planning → execution → review".

## Recommended Usage Path (From 0 to Controllable)

1.  **First Define Boundaries**: Select a system prompt version (recommended `v8` or `v10`).
2.  **Then Run Process**: Select `coding_prompts/` by stage in specific tasks (clarification / planning / execution / review).
3.  **Finally Productize**: When you repeatedly do similar work in a certain field, upgrade "Prompt + Data" to a Skill in `skills/` (more reusable, more stable).

## Directory Structure (Subject to actual repository directory)

```
i18n/en/prompts/
├── README.md
├── coding_prompts/                 # Programming/R&D Prompts (currently 41 .md files)
│   ├── index.md                    # Auto-generated index and version matrix (do not modify manually)
│   ├── Standardized Process.md
│   ├── Project Context Document Generation.md
│   ├── Intelligent Requirement Understanding and R&D Navigation Engine.md
│   └── ...
├── system_prompts/                 # System Prompts (Multiple versions of CLAUDE + other collections)
│   ├── CLAUDE.md/                  # Version 1~10 directory (v9 currently placeholder only)
│   │   ├── 1/CLAUDE.md
│   │   ├── 2/CLAUDE.md
│   │   ├── ...
│   │   ├── 9/AGENTS.md             # v9 currently no CLAUDE.md
│   │   └── 10/CLAUDE.md
│   └── ...
└── user_prompts/                   # User's own/one-time prompts
    ├── ASCII Art Generation.md
    ├── Data Pipeline.md
    └── Project Variables and Tools Unified Maintenance.md
```

## `system_prompts/`: System-Level Prompts (First Make AI "Controllable")

System prompts are used to define **working mode, code taste, output format, and security boundaries**. The directory adopts a versioned structure:

-   Path convention: `i18n/en/prompts/system_prompts/CLAUDE.md/<version_number>/CLAUDE.md`
-   Recommended versions:
    -   `v8`: Comprehensive version, suitable for general Vibe Coding
    -   `v10`: More focused on Augment/context engine standardization constraints
-   Note: `v9` directory is currently a placeholder only (no `CLAUDE.md`)

## `coding_prompts/`: Task-Level Prompts (Make the Process Run Through)

`coding_prompts/` are geared towards "one task": from requirement clarification, planning decomposition to delivery and review. It is recommended to treat it as a workflow script library:

-   **Entry-level** (must-use for new sessions/projects)
    -   `Project Context Document Generation.md`: Solidify context, reduce cross-session drift
    -   `Intelligent Requirement Understanding and R&D Navigation Engine.md`: Break down vague requirements into executable tasks
-   **Delivery-level** (ensure auditable output)
    -   `Standardized Process.md`: Hardcode "what to do first, what to do next", reduce loss of control
    -   `System Architecture Visualization Generation Mermaid.md`: Output architecture as visualizations (a picture is worth a thousand words)

### About `index.md` (Important)

[`coding_prompts/index.md`](./coding_prompts/index.md) is an automatically generated index (including version matrix and jump links), **do not edit manually**. If you batch add/delete/adjust versions, it is recommended to generate the index through the toolchain and then synchronize.

## `user_prompts/`: Personal Workbench (Not for Systematization)

Place some personal habits, temporary scaffolding prompts here. The principle is: **usable, not messy, not polluting the main library**.

## Quick Use (Copy and Use)

```bash
# View a task prompt
sed -n '1,160p' i18n/zh/prompts/coding_prompts/Standardized Process.md

# Select system prompt version (it is recommended to back up your current CLAUDE.md first)
cp i18n/zh/prompts/system_prompts/CLAUDE.md/10/CLAUDE.md ./CLAUDE.md
```

## Maintenance and Batch Management (Optional)

If you need batch maintenance capabilities for Excel ↔ Markdown, the repository has a built-in third-party tool: `libs/external/prompts-library/`. It is recommended to treat it as a "prompt asset production tool", and `i18n/zh/prompts/` as a "curated collection for daily development".

## Related Resources

- [`../skills/`](../skills/): Consolidate high-frequency domain capabilities into Skills (stronger reuse)
- [`../documents/`](../documents/): Methodologies and best practices (prompt design and workflow principles)
- [`../libs/external/prompts-library/`](../libs/external/prompts-library/): Prompt Excel ↔ Markdown management tool