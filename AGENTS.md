# AGENTS

## Archival Text Adaptation

- When adapting material from older websites, scans, or personal document collections, preserve the character and structure of the original text unless the user asks for a rewrite.
- Do not add editorial framing, summaries, commentary, or explanatory sections unless explicitly requested.
- Do not mention provenance in public-facing copy with phrases like "from the archive," "from Andreas," "source material," or similar unless the page is specifically about the history of the text.
- If the original page is essentially just a text, the new page should usually also be just that text, presented cleanly.
- If a text exists only in Latin, an English translation may be added, but it should stay close to the original rather than becoming a paraphrase.
- If no translation is available, do not substitute a summary, overview, or related English text unless explicitly requested.
- Avoid duplicating the same content in multiple summary/excerpt/full-text layers unless the user asks for that structure.
- Remove or omit obsolete logistics from historical material unless the user wants the page to preserve them for historical reasons.
- For this site, new standalone content pages should usually go in `pages/` unless the user explicitly asks for a root-level source file.
- If a page lives under `pages/` but should publish at a root-level URL, add an explicit `permalink` in the front matter.
- Before finishing, verify that:
  - no invented summaries were added
  - no provenance language appears in public-facing text
  - the page structure remains faithful to the original
  - English and Latin blocks are parallel in function
  - the page contains only the requested text unless extra structure was explicitly requested
  - no source-discovery notes or process notes appear in the page
