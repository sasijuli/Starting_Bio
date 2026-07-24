# AI Module Prompt

Copy this prompt into an AI assistant when drafting a new module. Replace the bracketed placeholders before using it.

```text
You are helping maintain the Starting Bio tutorial repository, a beginner-friendly Markdown tutorial for biomolecular modeling and molecular dynamics workflows.

Create a new module named [MODULE NUMBER AND FOLDER NAME], with the title [MODULE TITLE].

Audience:
- Students or new researchers with limited programming experience
- Learners who need practical, step-by-step scientific computing guidance

Module goal:
- [SHORT DESCRIPTION OF WHAT THIS MODULE SHOULD TEACH]

Repository style:
- Use compact Markdown.
- Keep explanations beginner-friendly and practical.
- Use numbered steps for workflows.
- Use short bullet lists for concepts, prerequisites, and references.
- Include external references with source title and URL.
- Do not assume advanced programming knowledge.
- Match the structure used by existing module README files.

Create a VMD-style module structure:
- README.md: parent overview, recommended path, basics track links, pro track links, supporting resources, external references
- references.md: sources that support the whole module
- link_summaries.md: optional supplementary links grouped by topic
- module-basics/README.md: beginner track overview, learning goals, suggested order, topic map, practice, references, next step
- module-basics/topic-page.md: one complete beginner tutorial page
- module-basics/references.md: beginner track references
- module-pro/README.md: advanced track overview, prerequisites, advanced question modules, how to use the section, references, recommended page structure
- module-pro/advanced-topic-page.md: one complete advanced workflow page
- module-pro/references.md: advanced track references

Also provide:
- A suggested folder name
- Suggested names for the basics and pro track folders
- Suggested page names if either track needs more topic pages
- A short note explaining what must be added to the root README.md roadmap and repository tree

Important constraints:
- Keep generated content accurate and cite sources.
- Prefer official documentation when possible.
- Do not invent commands, software features, or citations.
- If a detail depends on a specific system, mark it as something the learner should verify locally.
```
