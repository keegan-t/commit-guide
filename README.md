# Conventional Commits

A quick reference for writing consistent git commit messages. Based on the [Conventional Commits](https://www.conventionalcommits.org/) spec.

## Format

```
<type>(<scope>): <description>
```

- **description** should read like an instruction: `add`, `update`, `remove` - not `added`, `updated`, `removed`. A good test: the message should complete *"If applied, this commit will..."*
- **scope** is optional - it's a label for the specific part of the codebase affected
- No period at the end
- Keep it 72 characters or less
- **type** should be selected from one of the options below

## Types

| Type | Use for |
|------|---------|
| `feat` | New functionality |
| `fix` | Bug fixes |
| `refactor` | Restructuring code, no behaviour change |
| `perf` | Performance improvements, no behaviour change |
| `style` | Formatting / whitespace, no logic change |
| `chore` | Maintenance tasks that don't change the code |
| `docs` | Documentation only |
| `test` | Adding or updating tests |

## Examples

```
feat(auth): add login page
fix: prevent app from crashing on startup
refactor: move css to separate file
perf(images): use lazy loading
style: reformat code to project style guide
chore: update dependencies
docs(readme): add setup instructions
test: add unit tests for form validation
```

## Breaking Changes

A breaking change is any change that would cause external dependents to stop working - for example, removing an endpoint or changing a return type.

Add `!` after the type and describe the break in the footer:

```
feat(api)!: remove deprecated v1 endpoints

BREAKING CHANGE: /v1/users removed. Migrate to /v2.
```
