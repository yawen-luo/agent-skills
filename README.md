# Agent Skills

A version-controlled collection of reusable AI agent skills and workflows. Each skill has one entry-point `SKILL.md`, with focused references and optional assets loaded only when needed.

## Available skills

| Skill | Description | Version | Source |
| --- | --- | --- | --- |
| [Career Application](skills/career-application/SKILL.md) | Evidence-based resume/CV tailoring, cover letters, graduate and research applications, strict independent review, and LaTeX formatting. | 1.0.0 | [Full skill directory](skills/career-application/) |

## Install

Use the Agent Skills CLI to list the available skills:

```bash
npx skills add yawen-luo/agent-skills --list
```

Install only Career Application:

```bash
npx skills add yawen-luo/agent-skills --skill career-application
```

For an existing installation, use the CLI's update/check commands as supported by your environment:

```bash
npx skills check
npx skills update
```

GitHub is the canonical source for skill instructions. Publishing a repository does not guarantee immediate appearance in the skills.sh discovery directory.

## Repository structure

```text
agent-skills/
├── README.md
├── LICENSE
└── skills/
    └── career-application/
        ├── SKILL.md
        ├── README.md
        ├── references/
        │   ├── cover-letter.md
        │   ├── resume-cv.md
        │   ├── review-scoring.md
        │   ├── evidence-and-opportunity.md
        │   ├── format-and-templates.md
        │   └── test-cases.md
        └── assets/
            ├── cover-letter-minimal.tex
            └── resume-jake-style.tex
```

## Maintenance

1. Make behavior changes in the appropriate skill's `SKILL.md` or `references/`, and modify `assets/` only for formatting.
2. Keep the `name`, `description` and version metadata in each `SKILL.md` accurate.
3. Run scenarios in `references/test-cases.md`; verify the actual application requirement and factual source before using any output.
4. Review changes for private data before committing. Use Git history for rollback and tag releases when useful.
5. When adding a skill, create `skills/<skill-name>/SKILL.md` and add it to the Available skills table.

## Privacy and trust

**Do not commit personal Evidence Banks, transcripts, applications, credentials, private project files, letters of recommendation, or private Notion content.** Skills contain reusable instructions and sanitized examples; personal facts stay in authorized private sources. Generated application materials must not invent project metrics, employment, awards, publications or other claims.

## Scope

The [Lecture Notes plugin](https://github.com/yawen-luo/lecture-notes-plugin) remains a separate project; it is not bundled into this repository yet. Additional skills may be migrated here after they are authored and tested.

## License

MIT — see [LICENSE](LICENSE).
