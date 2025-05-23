```
change-type(optional scope): change-short-description

optional-body-full-description

optional-footer-key-value-1
...
optional-footer-key-value-N
```
## Type (of change)
- **add** – Introduces a new dependency, file, or component.
- **remove** – Deletes unused code, dependencies, or files.
- **change** – Modifies existing functionality without being a fix or feature.
- **fix (bugfix)** – Fixes a bug or incorrect behavior.
- **update (upd)** – General updates that don’t fit other categories.
- **feat (feature)** – Adds or removes a feature.
- **refactor (refactoring)** – Restructures existing code without changing functionality.
- **perf (performance, optimization, opt)** – Improves code performance or efficiency.
- **build** – Modifies the build system, dependencies, or CI/CD pipelines.
- **ops** – Changes related to infrastructure, deployment, or maintenance.
- **chore** – Miscellaneous updates like modifying config files.
- **style** – Formatting or stylistic changes without functional impact.
- **test (tests)** – Adds or improves tests.
- **followup** – A quick addition or correction to a previous commit.
- **deprecate** – Marks a feature or component as obsolete.
- **docs (documentation)** – Changes that affect documentation only.
- **security** – Addresses security vulnerabilities or enhances protection.
## Notes
- The `scope` optionally provides extra context to the type. 
- You can add tags to the end of each line.
- The `description` is a short description of the code changes
	- Don't capitalize the first letter
	- No dot (`.`) at the end
	- Use the imperative, present tense: "change" not "changed" nor "changes"
	    - Think of `This commit will...` or `This commit should...`

## Change log resulting categories
`Added`, `Changed`, `Deprecated`, `Removed`, `Fixed`, `Security`
## Examples
Most generic commit message when you don't want to think at all:
```
change: show caption for popup
```

Some one line commit messages:
```
fix(api:shoping cart): correctly handle empty message in request body #cart
```

```
build(release): bump version to 1.0.0
```

```
!feat(core): add character controller, breaking change
```

```
feat(art:asset:character): remove character idle animation
```

```
feature: add Inventory module

Inventory added. Now the player can put items in the inventory and manipulate them inside the inventory #inventory
```

One commit contains multiple fixes/features and footer section:
```
!feat: adds v4 UUID to crypto
fix(utils): unicode no longer throws exception #font
feat(art): update unicode texture atlas #font

This adds support for v4 UUIDs to the library.

PiperOrigin-RevId: 345559154
BREAKING-CHANGE: encode method no longer throws.
Source-Link: googleapis/googleapis@5e0dcb2
PiperOrigin-RevId: 345559182
Source-Link: googleapis/googleapis@e5eef86
tags: #cart #error-handling
```
## References
- Semantic Versioning (SemVer): https://semver.org/
- Conventional Commits specification: https://www.conventionalcommits.org/en/v1.0.0/
- keep a changelog: https://keepachangelog.com/en/1.0.0/
- Version history module for Unity: https://github.com/cholushkin/VersionHistory

ver.1.0
#prj-cheat-sheets #conventional-commit 