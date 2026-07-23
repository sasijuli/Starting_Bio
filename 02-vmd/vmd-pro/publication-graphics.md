# How Can I Make High-Resolution Images And Movies?

## Scientific Question

How can I make a molecular figure or animation that is clear, high resolution, and reproducible from documented VMD settings?

## When To Use This Module

Use this workflow for report figures, paper figures, presentation images, graphical abstracts, and short movies that need more control than a quick screenshot.

## Required Background

- You can load a structure or trajectory.
- You can create multiple representations.
- You can choose selections, drawing methods, colors, and materials.
- You can save commands or a VMD state file so the scene can be recreated.

## Figure Questions

### What is the message of the image?

Start with one scientific message: binding site, conformational change, membrane insertion, hydrogen-bond network, or trajectory motion. Choose representations only for that message.

### How can I increase visual resolution?

Increase representation-specific resolution settings such as sphere, cylinder, or cartoon resolution until extra detail no longer changes the visible result. Keep interactive work lighter, then raise resolution for the final render.

### How should I choose colors and materials?

Use consistent colors for recurring molecular parts. Use opaque materials for the main subject, transparent materials for context, and neutral backgrounds when the image must be placed in a document.

### How can I get high resolution for the images?

Use VMD rendering rather than relying only on the OpenGL screenshot. The built-in Render window and `render` command can export the scene through renderers such as Tachyon. For final figures, set the scene, remove axes if they are not needed, adjust clipping, choose output resolution, and render to an image format suitable for editing or publication.

### How do I make the figure reproducible?

Save the commands used to load files, define representations, set colors/materials, orient the view, and call the renderer. A scripted figure is easier to revise when reviewers or collaborators request changes.

For teaching or figure revision, also save a VMD state file for the scene. Keep in mind that state files depend on the referenced structure and trajectory paths, so store them with the input files or document the expected directory layout.

## Movie Questions

### When should I make a movie?

Use a movie when motion is the scientific result. For a static structural comparison, a still image with multiple frames or aligned structures may be clearer.

### How do I make trajectory motion readable?

Use trajectory smoothing, draw selected frame ranges, and update selections for coordinate-dependent features. Avoid showing too many atoms if the movie becomes visually dense.

## Suggested Output

- One final high-resolution image.
- One saved VMD state or Tcl script that recreates the scene.
- A short note listing representation choices, rendering method, image size, and any post-processing.

## Validation Checks

- Confirm that all labels, axes, and periodic artifacts are intentional.
- Check text, colors, and transparent surfaces against the final background.
- Render a low-resolution draft before committing to a high-resolution render.
- Keep a copy of the source script or state file with the final image.

## Supplementary Resource

The local [`mkvmd_render` redirect module](mkvmd-render.md) points to a GitHub tutorial with practical examples for Tachyon rendering, ambient occlusion, materials, lights, transparency, and high-resolution settings.

Read the local [publication graphics link summary](../link_summaries.md#publication-graphics) before using it as a follow-up exercise.

## External References

- Official Using VMD tutorial, figure rendering sections: https://www.ks.uiuc.edu/Training/Tutorials/vmd/tutorial-html/node2.html
- VMD Images and Movies tutorial: https://www.ks.uiuc.edu/Training/Tutorials/vmd-imgmv/imgmv/tutorial-html/node3.html
- VMD save state command: https://www.ks.uiuc.edu/Research/vmd/current/ug/node23.html
- Current VMD User's Guide, rendering documentation: https://www.ks.uiuc.edu/Research/vmd/current/ug.pdf
- `mkvmd_render`: https://github.com/skblnw/mkvmd_render
- [VMD Pro references](references.md)
