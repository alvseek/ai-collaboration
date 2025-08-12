# Git Commit Message Standards

This document outlines the standards for writing clear and effective Git commit messages.

## Commit Message Structure

```
<type>(<scope>): <subject>

<body>

<footer>
```

### Type
Must be one of the following:
- `feat`: A new feature
- `fix`: A bug fix
- `docs`: Documentation only changes
- `style`: Changes that do not affect the meaning of the code (formatting, etc.)
- `refactor`: Code changes that neither fix a bug nor add a feature
- `perf`: Code changes that improve performance
- `test`: Adding missing tests or correcting existing tests
- `chore`: Changes to build process or auxiliary tools

### Scope
- Optional, in parentheses
- Specifies the part of the codebase affected (e.g., component name, file name)

### Subject
- Imperative mood ("change" not "changed" or "changes")
- No capitalization of first letter
- No period (.) at the end
- Limited to 50 characters
- Concise description of the change

### Body
- Optional
- Wrapped at 72 characters
- Explains what and why vs. how
- Separated from subject by blank line
- Use bullet points if needed

### Footer
- Optional
- Reference issue tracker IDs
- Breaking changes should start with "BREAKING CHANGE:"

## Examples

Good commit messages:
```
feat(auth): add JWT authentication

Implement JSON Web Token authentication for API endpoints
- Add token generation
- Add token validation middleware
- Update user routes to use auth

Closes #123
```

```
fix(database): resolve connection timeout issue

- Increase connection timeout to 30s
- Add connection retry logic
- Add error logging

Fixes #456
```

## Best Practices

1. Keep commits atomic and focused
2. Write clear, meaningful messages
3. Use the imperative mood
4. Separate subject from body with blank line
5. Reference issues and pull requests
6. Consider future readers
7. Don't end subject line with period
8. Capitalize the subject line

## Anti-Patterns to Avoid

❌ "fixed stuff"
❌ "WIP"
❌ "Updated files"
❌ "."
❌ Multiple unrelated changes in one commit

Remember: A well-written commit message shows respect for those who will maintain your code in the future, including yourself.
