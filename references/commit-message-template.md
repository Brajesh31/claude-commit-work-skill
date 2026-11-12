# Commit Message Template

Use this format when the project follows Conventional Commits.

```text
<type>(<scope>): <imperative summary>

<what changed and why it changed>

<footer>
```

## Subject

- Use a recognized type such as `feat`, `fix`, `refactor`, `perf`, `test`, `docs`, `build`, `ci`, `chore`, or `revert`.
- Add a scope when it makes the affected area clearer.
- Use an imperative summary that describes the outcome.
- Keep the subject focused and avoid ending it with a period.
- Respect any stricter subject-length rule configured by the repository.

## Body

Explain the motivation and relevant context. Prefer:
- why the change was needed;
- the important behavior change;
- constraints or trade-offs;
- migration notes when applicable.

Do not write a line-by-line implementation diary.

## Footer

Use a footer for issue references, co-authorship, or breaking-change details only when required by the repository.

Example:

```text
feat(auth): support passkeys

Allow eligible users to sign in with a registered passkey.
Keep the password flow available as a fallback.

Closes #482
```

## Multiple commits

Split changes when they represent separate concerns, such as:
- feature work versus refactoring;
- backend logic versus UI changes;
- production code versus tests;
- formatting versus behavior;
- unrelated dependency updates.

A commit should be independently understandable and, where practical, independently verifiable.

## Final review

Before committing, inspect the staged diff. Confirm that it contains only intended files and does not include credentials, debug artifacts, generated output, or unrelated changes.
