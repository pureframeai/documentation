> For Mintlify product knowledge (components, configuration, writing standards),
> install the Mintlify skill: `npx skills add https://mintlify.com/docs`

# Documentation project instructions

## About this project

- This is a documentation site built on [Mintlify](https://mintlify.com)
- Pages are MDX files with YAML frontmatter
- Configuration lives in `docs.json`
- Use the Mintlify MCP server, `https://mcp.mintlify.com`, to edit content and settings via MCP
- Use the Mintlify docs MCP server, `https://www.mintlify.com/docs/mcp`, to query information about using Mintlify via MCP

## Terminology

- Use **Pureframe AI** for the product name.
- Use **account** for the customer security and billing boundary. Do not use
  **organization** or **user** as synonyms unless they are exact API field names.
- A **collection** is a named group of videos. Every video belongs to one collection.
- A **video** is the uploaded source file. A **segment** is a timestamped search
  result within a video. Use **moment** only as plain-language shorthand for a
  segment. Use **clip** only when an API or tool field uses that term.
- Use **processing** for the asynchronous work after an upload and **searchable**
  for a video whose status is `done`.
- Describe the search signals as **visual**, **transcript**, **scene**, and
  **on-screen text**. Preserve exact API values such as `frame` and `ocr` in code
  and field references.

## Style preferences

- Use active voice and second person ("you")
- Keep sentences concise: one idea per sentence
- Use sentence case for headings
- Bold for UI elements: Click **Settings**
- Code formatting for file names, commands, paths, and code references
- Lead with what the reader can accomplish, then show how.
- Prefer bounded, observable claims. Avoid "any," "every," "always," "never,"
  and performance superlatives unless they are part of a verified guarantee.
- Keep code examples minimal, realistic, and copy-pasteable.
- Link to one canonical explanation instead of repeating it across pages.

## Content boundaries

- Treat `openapi.json` as the source of truth for public endpoints, parameters,
  response fields, and error shapes.
- Document public contracts and observable behavior: authentication, permissions,
  request and response formats, status values, limits, supported inputs, errors,
  recovery steps, and verified customer-facing guarantees.
- Explain search behavior at the level developers need to choose a mode and handle
  results. Do not disclose model or vendor names, model sizes, vector dimensions,
  database products, query functions, ranking algorithms or constants, sampling
  intervals, cache sizes, internal retries, worker topology, pipeline ordering,
  or re-indexing architecture.
- A cryptographic detail may appear when it is part of a public integration
  contract, such as webhook signature verification. Do not disclose credential
  storage implementation merely to sound reassuring.
- Security, privacy, data retention, residency, deletion, pricing, and performance
  statements must describe a verified commitment. Add a TODO comment when the
  current behavior or owner approval is uncertain.
- Do not include internal source-file names, implementation comments, private
  service names, or operational procedures in public pages or agent instructions.
- Do not document internal administration features.
