# For Repository Admins

This folder contains repository-maintenance notes and copy-ready templates for creating new modules or tutorial pages.

## Current Folder Structure

```text
for-repo-admins/
├── README.md
├── exercise-template.md
├── tutorial-page-template.md
├── template-larger-module/
│   ├── README.md
│   ├── ai-module-prompt.md
│   ├── link_summaries.md
│   ├── references.md
│   ├── module-basics/
│   │   ├── README.md
│   │   ├── references.md
│   │   └── topic-page.md
│   └── module-pro/
│       ├── README.md
│       ├── advanced-topic-page.md
│       └── references.md
└── template-shorter-module/
    ├── README.md
    └── ai-short-module-prompt.md
```

## Module Structure

Modules are implemented as numbered Markdown folders so the learning path, URLs, and repository tree stay easy to scan. A typical module has:

- `README.md`: the module overview, learning path, page links, related pages, and external references
- Topic pages: focused `.md` files for individual lessons, tools, or workflows
- `references.md`: sources used only by that module or track
- Optional subfolders: nested learning tracks when a topic naturally splits into levels, audiences, or workflows
- Optional support pages: exercises, cheatsheets, link summaries, redirects, or curated tool lists

## Larger Modules

Use `02-vmd/` as the model for a larger module. Its parent `README.md` explains the overall VMD path and links to two nested tracks: `vmd-basics/` for an ordered beginner sequence and `vmd-pro/` for advanced, question-driven workflows. Each track keeps its own `README.md`, topic pages, and `references.md`, while shared VMD resources stay at the parent module level.

When adding a larger module, copy `template-larger-module/` to a new numbered folder such as `06-new-module/`, then rename `module-basics/`, `module-pro/`, `topic-page.md`, and `advanced-topic-page.md` to match the new topic.

Use the larger-module files this way:

- `README.md`: parent module overview and navigation
- `module-basics/`: beginner track with ordered topic pages
- `module-pro/`: advanced track with research-question pages
- `references.md`: module-level sources
- `link_summaries.md`: optional supporting links, videos, or notes
- `ai-module-prompt.md`: prompt for drafting a larger module with AI

## Shorter Modules

Use `04-batch-computing/` or `05-useful-tools-for-membrane-analysis/` as the model for a shorter module. A shorter module usually has one `README.md` that explains the purpose, learning focus, how to use the module, related course pages, and external references. This format works well for redirect modules, curated tool lists, or compact topics that do not need separate basics/pro tracks.

When adding a shorter module, copy `template-shorter-module/` to a new numbered folder such as `06-new-module/`, then replace the placeholder title, resource names, related pages, and references.

Use the shorter-module files this way:

- `README.md`: complete single-page module template
- `ai-short-module-prompt.md`: prompt for drafting a shorter module with AI

## Standalone Page Templates

Use `tutorial-page-template.md` when adding one new lesson page inside an existing module. Use `exercise-template.md` when adding a focused exercise page.

## Update Checklist

After adding any module, update:

- Root `README.md` roadmap
- Root `README.md` module contents
- Root `README.md` repository tree
- Root `references.md` if the sources are broadly useful
- Module-level links back to related course pages

Use the AI prompt inside the matching template folder when asking an AI assistant to draft the first version of a module.
