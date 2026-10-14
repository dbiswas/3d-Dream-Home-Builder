# Home 3D Modeler & Architect

An AI instruction prompt for reconstructing homes from photos, with an interactive cabin example.

```text
  +--------------+     +-----------------+     +----------------+
  | House photos | --> | Model + compare | --> | 3D home + plans |
  +--------------+     +-----------------+     +----------------+
                              ^     |
                              +-----+ refine
```

## Overview

This project pairs a reusable AI modeling prompt with a worked example: a square cabin with a roof ridge running diagonally from corner to corner. The prompt guides an assistant through studying photos, building a model, and comparing the result against the original views. The example lets homeowners, designers, and people exploring AI-assisted modeling inspect the geometry, floor plans, and documented assumptions.

## Key features

- A structured prompt covering photo analysis, reconstruction, rendering, and self-review.
- Clear labels for observed details, inferred details, and unknown areas.
- A weighted review rubric with a 90% target and a maximum of 10 review rounds.
- An interactive cabin viewer with exterior, interior, aerial, and plan-cut views.
- Four lighting modes, floor cuts, and a tree visibility toggle.
- A cabin report with two floor plans, four elevations, photo comparisons, presentation renders, dimensions, and an iteration log.

## How it works

1. Give an AI assistant the modeling prompt and upload photos of a home.
2. The prompt asks it to identify visible features, estimate scale, and flag missing views.
3. It guides modeling from the overall shape through floor layouts, roof geometry, and details, using the tools available to that assistant.
4. It asks the assistant to render matching views, score discrepancies, and refine the model. Results below the target must be reported honestly, with remaining gaps made explicit.

The HTML file is an existing example with its own JavaScript geometry and embedded report images. It displays the cabin; creating a model from new photos happens in your chosen AI assistant.

## Getting started

### Explore the cabin example

1. Download this repository and extract it if needed.
2. Open [Diagonal-ridge cabin_ 3D reconstruction.html](Diagonal-ridge%20cabin_%203D%20reconstruction.html) in a modern browser with JavaScript and WebGL enabled. Download the file first if you are viewing it on GitHub.
3. Drag to rotate the model, and scroll or pinch to zoom. Select **Aerial** to check that the camera controls work, then scroll down to read the report.

There is no build step, package installation, backend, or API key required to view the example. Internet access is needed to load Three.js 0.147.0 and OrbitControls from jsDelivr; the page also requests an IBM Plex Sans font from Google Fonts. Report images and floor plans are embedded in the HTML.

If the 3D library fails to load or WebGL is unavailable, the viewer is designed to show a still render with a status message. Check your connection and browser WebGL settings if you cannot interact with the model.

### Use the prompt with your own photos

1. Open [Home 3D Modeler AI System Prompt.md](Home%203D%20Modeler%20AI%20System%20Prompt.md).
2. Copy the instructions below its introductory divider into your AI assistant's system prompt or custom instructions.
3. Upload your house photos to that assistant. Reference images for this project are kept in [input-images/](input-images/).
4. Ask it to begin with the photo inventory and reconstruction plan. Supply missing views or agree to proceed with clearly labeled assumptions.

Use an assistant that accepts images. Building models and rendering views also depend on the tools available in that environment; the prompt does not install or provide those tools. The expected first response is an image analysis report and a reconstruction plan, including any requests for missing views.

## Example usage

**Inspect the supplied cabin:** Select **Plan cut** to look down into the main floor. Try **Upper floor** under Cut to inspect the upper level, and switch between **Day** and **Night** to compare lighting. Choose **Glass corner** to return to the opening camera view.

### Sample prompts

Configure the system prompt and attach your house photos first. Use a starting prompt below, then follow up as the model develops.

**Simple starting request:** This is the request used to generate the example's rendered design:

```text
Can you generate the 3D model plan for building this house?
```

The result is a concept model; construction still requires professional review.

**Start with photo analysis:** Use this to review the available evidence before modeling.

```text
Reconstruct this home from the attached photos. Start with the image
inventory, observed features, scale estimates, and missing views.
Label assumptions clearly before building the model.
```

**Request floor plans:** Use this after the initial photo analysis to explore the layout.

```text
Create a dimensioned floor plan for each level of this house based on
the attached photos. Label estimated dimensions and inferred room
layouts, and list any missing views needed to improve the plans.
```

**Request rendered views:** Use this once a model is available to compare it with the photos.

```text
Render the model from angles matching the attached exterior photos,
then create one presentation view. Match the visible materials and
colors, and flag any details that the photos do not confirm.
```

**Review and refine:** Use this to request another comparison round.

```text
Compare the current model with the source photos using the scoring
rubric. Fix the largest visible discrepancies, show the updated views,
and record the new scores and remaining gaps in the iteration log.
```

The full prompt defines the requested delivery package: an iteration log, floor plans, elevations, matched-angle comparisons, a presentation render, and an assumptions and accuracy report. Actual output depends on the assistant's capabilities and the evidence in the photos.

## Project structure

```text
.
|-- README.md
|-- Home 3D Modeler AI System Prompt.md         # Reusable AI instructions
|-- Diagonal-ridge cabin_ 3D reconstruction.html # Viewer and example report
`-- input-images/                              # Reference photos
```

## Customization

- **Modeling workflow:** Edit the prompt to adjust the review rubric, target score, iteration cap, or requested deliverables.
- **Cabin geometry:** The HTML's `DEFAULTS` object controls dimensions such as `L` (footprint side length), `zA` and `zC` (ridge heights), `zEave` (eave height), and `upperZ` (upper floor height). Measurements use metres.
- **Appearance and views:** The HTML defines material colors in `COLORS`, lighting in `MODES`, and camera presets in `V`.

Geometry changes require editing JavaScript. The embedded report images, floor plans, dimensions, and scores are static and will not update automatically when you change the live model.

## Limitations

- The cabin report records **85.9% after three review rounds**, below the prompt's 90% target. This is the report's own assessment, not an independently verified accuracy measurement; the example remains unfinished under its stated protocol.
- Missing north and east exterior views, bathroom photos, and landing views leave parts of the reconstruction uncertain. Read the HTML report's **Assumptions and unknowns** section before relying on those details.
- Photo-based dimensions are estimates. The plan's north label is a drawing convention; true north was not surveyed.
- Outputs are for concepts and visualization. Construction requires review by a licensed architect or engineer for structural design, code compliance, loads, foundations, and permits.
