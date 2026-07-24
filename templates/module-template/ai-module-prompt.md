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

Create these files:
- README.md: overview, learning goals, recommended path, module pages, related course pages, external references
- topic-page.md: one complete starter tutorial page with learning goals, background, step-by-step tutorial, practice, common errors, external references
- exercises.md: module-level exercises with objective, instructions, questions, expected result, external references
- references.md: official documentation, tutorials and guides, related course references

Also provide:
- A suggested folder name
- Suggested page names if the module needs more than one topic page
- A short note explaining what must be added to the root README.md roadmap and repository tree

Important constraints:
- Keep generated content accurate and cite sources.
- Prefer official documentation when possible.
- Do not invent commands, software features, or citations.
- If a detail depends on a specific system, mark it as something the learner should verify locally.
```
