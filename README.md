# Swift API Design Guidelines Skill

Expert guidance for any AI coding tool that supports the [Agent Skills open format](https://agentskills.io/home) — naming, clarity at the point of use, and conventions from Apple's Swift API Design Guidelines.

This skill distills the [official Swift API Design Guidelines](https://www.swift.org/documentation/api-design-guidelines/) into actionable checklists and references so agents can write or review Swift APIs consistently with the Swift ecosystem.

## Who this is for

- Teams writing Swift libraries or public APIs who want consistent naming and documentation
- Developers reviewing Swift code for clarity, argument labels, and style
- Anyone designing types, methods, and parameters who wants to follow Apple's guidelines

## How to Use This Skill

### Option A: Using skills.sh

Install this skill with a single command:

```bash
npx skills add https://github.com/gu7araujo/Swift-API-Design-Guidelines-Skill --skill swift-api-design-guidelines
```

Then use the skill in your AI agent, for example:

> Use the Swift API Design Guidelines skill and review this Swift file

### Option B: Manual install

1. **Clone** this repository.
2. **Install or symlink** the skill folder (root of this repo) following your tool's official skills installation docs (see links below).
3. **Use your AI tool** as usual and ask it to use the "swift-api-design-guidelines" skill when writing or reviewing Swift APIs.

#### Where to Save Skills

Follow your tool's official documentation; here are a few popular ones:

- **Cursor:** [Enabling Skills](https://cursor.com/docs/context/skills#enabling-skills)
- **Codex:** [Where to save skills](https://developers.openai.com/codex/skills/#where-to-save-skills)
- **Claude:** [Using Skills](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview#using-skills)

**How to verify:** Your agent should reference the checklists in `SKILL.md` and use `reference.md` for full wording and examples when applying the guidelines.

## What This Skill Offers

This skill gives your AI coding tool practical Swift API design guidance. It can:

### Apply the guidelines when writing Swift

- Name types, methods, properties, and parameters for **clarity at the point of use**
- Choose argument labels (omit vs. include, prepositional phrases, value-preserving conversions)
- Form fluent call sites (e.g. mutating/nonmutating pairs, factory `make` prefix, boolean assertions)
- Use terminology and casing consistently (UpperCamelCase vs. lowerCamelCase, acronyms)

### Review existing Swift code

- Check naming against the fundamentals (clarity over brevity, role-based names, no redundant type words)
- Validate parameters (defaults at end, doc-friendly names, `#fileID` vs. `#filePath`)
- Suggest doc comments (summary, symbol markup, complexity for non-O(1) computed properties)

### Avoid common mistakes

- Overloading on return type; ambiguous labels with weak types (`Any`, `NSObject`)
- Unlabeled tuple members and closure parameters; overload ambiguity with unconstrained generics

## What Makes This Skill Different

**Official alignment:** Based directly on Apple's [Swift API Design Guidelines](https://www.swift.org/documentation/api-design-guidelines/), with no extra opinion on architecture or project structure.

**Checklist-driven:** `SKILL.md` provides when-to-apply rules and checklists (naming, conventions, doc comments) so agents can work through decisions quickly.

**Concise + detailed:** Summaries and checklists in the skill file; full wording and rationale in `reference.md` for deeper lookups.

## Skill Structure

```text
Swift-API-Design-Guidelines-Skill/
  README.md
  SKILL.md          # When to apply, fundamentals, checklists, doc-comment rules
  reference.md      # Full reference text and examples from the official guidelines
  LICENSE
```

## Contributing

Contributions are welcome. This repository follows the [Agent Skills open format](https://agentskills.io/home). When contributing:

- Keep `SKILL.md` as the entry point (when to use, checklists, links to reference).
- Put extended explanations and examples in `reference.md`.
- Preserve alignment with the [official Swift API Design Guidelines](https://www.swift.org/documentation/api-design-guidelines/).

## License

This project is open-source. See [LICENSE](LICENSE) for details.
