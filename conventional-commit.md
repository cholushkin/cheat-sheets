# Conventional commit cheat sheet
```
<type>[optional scope]: <description>

[optional body]

[optional footer, "key: value" format]
```
Example:
```
fix(shopping cart)!: button handler 
add(cart): additional checks and error handling #cart

The error occurred because of <reasons>. Multiline comment. #reason

BREAKING CHANGES: ticket enpoints no longer supports list all entites.
JIRA: 1337
tags: #cart #error-handling
```
## Type
### List of possible types
`doc`/`docs`/`documentation`, `add`, `remove`, `change`, `feature`/`feat`, `fix`, `refactor`, `opt`/`optimization`/`perf`/`performance`, `ver`/`version`, `build`, `ops`, `style`, `test`/`tests`, `oops`, `chore`

### Types description
- `feat` Commits, that adds or remove a new feature
- `fix` Commits, that fixes a bug
- `refactor` Commits, that rewrite/restructure your code
- `perf` Commits are special `refactor` commits, that improve performance
- `style` Commits, that do not affect the meaning (white-space, formatting, missing semi-colons, etc.)
- `test` Commits, that add missing tests or correcting existing tests
- `docs` Commits, that affect documentation only
- `build` Commits, that affect build components like build tool, ci pipeline, dependencies, project version
- `ops` Commits, that affect operational components like infrastructure, deployment, backup, recovery
- `chore` Miscellaneous commits e.g. modifying `.gitignore`, `submodules` 
- `oops` Addition to the previous commit when you forgot to commit something

### Scope examples
- fix(api:shoping cart): correctly handle empty message in request body
- build(release): bump version to 1.0.0 
- feat(core): add character controller
- feat(art:asset:character): add character idle animation

## Notes
- The `scope` optionally provides extra context to the type. 
- The `description` is a short description of the code changes
	-  Don't capitalize the first letter
	- No dot (`.`) at the end
	-  Use the imperative, present tense: "change" not "changed" nor "changes"
	    - Think of `This commit will...` or `This commit should...`

# Change log resulting categories
`Added`, `Changed`, `Deprecated`, `Removed`, `Fixed`, `Security`

# Examples
Most generic commit when you don't want to think at all:
```
change: some description
```

Commit contains multiple fixes or features:
```
feat!: adds v4 UUID to crypto
fix(utils): unicode no longer throws exception
feat(art)!: update unicode texture atlas

This adds support for v4 UUIDs to the library.

PiperOrigin-RevId: 345559154
BREAKING-CHANGE: encode method no longer throws.
Source-Link: googleapis/googleapis@5e0dcb2
PiperOrigin-RevId: 345559182
Source-Link: googleapis/googleapis@e5eef86
```

```
feat(api)!: send an email to the customer when a product is shipped
```

```
feature: add Inventory module

Inventory added. Now the player can put items in the inventory and manipulate them inside the inventory #inventory
```
