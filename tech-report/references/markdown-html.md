# Markdown and HTML Production

Read this reference when producing or checking a technical report in Markdown or
HTML. Apply only the requested format guidance. Preserve an existing format when
the request leaves it unspecified; otherwise use Markdown. Do not create an HTML
companion automatically for a Markdown request.

## Markdown

- Identify the intended renderer from the destination or existing project when
  possible. Check support before relying on raw HTML anchors, Mermaid, math, or
  other extensions. These are not universally portable. If renderer support is
  unknown, use readable standard Markdown or state the dependency and limit.
- Use a coherent heading hierarchy, fenced code with an appropriate language,
  and descriptive link labels. Keep tables readable; move long explanations out
  of crowded cells. Use overview tables and glossaries only when they help.
- Use the renderer's verified heading-anchor behavior or supported explicit
  anchors for cross-references. Do not call raw HTML anchors renderer-independent.
  For a renderer that preserves HTML IDs, this is a possible pattern:

  ```markdown
  <a id="comparison-conditions"></a>
  ## Comparison conditions

  See [comparison conditions](#comparison-conditions).
  ```

- Render diagrams with a supported extension or use a portable image with a
  text explanation. If a diagram cannot render, supply a readable fallback that
  preserves its essential relationships. A raw Mermaid block alone does not
  establish that the reader can see a diagram.
- Keep referenced assets reachable from the delivered document. Prefer relative
  paths for bundled local assets and avoid machine-specific absolute paths when
  the artifact is meant to move.

## HTML

Produce a semantic, readable document rather than initiating a website workflow.
Use a complete document with the appropriate `lang`, UTF-8 charset, and viewport
metadata. Keep essential content available without interaction or script.

- Use ordered heading levels and native document elements for paragraphs,
  lists, figures, and tables. Give tables real header cells and captions where
  needed to explain their purpose. Preserve header-to-cell relationships in
  complex tables.
- Use descriptive links and appropriate alternative text for informative
  images. Provide a nearby text explanation for diagrams when needed to convey
  their relationships. Keep key findings and material limitations visible
  without hover states, collapsed controls, or script-only content. Supporting
  details may use progressive disclosure if the main explanation remains complete.
- Use readable typography, contrast, spacing, and line lengths. Check both wide
  and narrow layouts. Let wide tables scroll within their container if needed
  without making the whole document overflow or dropping data.
- Bundle assets or use stable references appropriate to delivery. Avoid local
  absolute paths and undocumented external font, image, or script dependencies.
  Verify that the artifact works under the intended access method, including
  local-file viewing when that is how it will be delivered.
- Ensure diagrams actually render. Prefer embedded SVG or bundled images when
  suitable; if script-based rendering is used, preserve a readable fallback.
  Do not make successful script loading necessary to understand the report.

## Verify the delivered artifact

Use available tools proportionately to the artifact and requested task. A local
wording edit may need only checks of the affected content and its references;
layout or format changes need rendered inspection.

1. **Content:** Check values, units, labels, qualifiers, code, and equations
   against the reviewed material. Confirm body, tables, diagrams, and any
   glossary agree after edits or renames.
2. **Links and assets:** Mechanically check internal targets, duplicate IDs,
   local reference paths, and required assets. Include renderer-generated
   heading IDs in anchor checks when they are used. Check external destinations
   when accessible and relevant; report access failures without equating them
   with proof that the destination is wrong.
3. **Semantic navigation:** Follow consequential cross-references, especially
   after merges or renames. Confirm each link reaches the section the sentence
   intends, not merely an existing target. Check useful descriptive labels.
4. **Rendered output:** Use the available browser or renderer for the actual
   target format. Inspect heading hierarchy, table legibility, diagrams, code,
   and asset loading. For HTML, check wide and narrow views and essential content
   without dependence on interaction or script. For Markdown, use the intended
   renderer where available rather than assuming another renderer is equivalent.

Use `rg` or an available parser for a bounded mechanical sweep, but state its
coverage. A regex for explicit HTML IDs misses generated Markdown anchors and
other link forms; empty output establishes only what that check actually covers.
Mechanical existence checks do not replace semantic navigation or visual checks.

If both Markdown and HTML are requested, verify that they contain the same
claims, data, conditions, uncertainty, limitations, and intended section targets.
Their presentation can differ. Do not treat a successful conversion command as
evidence of content or layout equivalence.

Report evidence review, comprehension checks, and rendered inspection separately.
If rendering was not checked, say so and identify any material renderer or asset
uncertainty. Deliver clearly labeled gaps rather than implying unperformed
verification. Stop after the requested checks establish completion or a material
constraint remains; do not add hosting, publishing, or unrelated experiments.
