```markdown
# Ocxly Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns, conventions, and workflows used in the Ocxly TypeScript codebase. It covers file organization, import/export styles, commit message habits, and testing patterns. By following these guidelines, contributors can maintain consistency and quality across the project.

## Coding Conventions

### File Naming
- Use **camelCase** for all file names.
  - Example: `userProfile.ts`, `dataFetcher.ts`

### Imports
- Use **relative imports** for referencing modules.
  - Example:
    ```typescript
    import { fetchData } from './dataFetcher';
    ```

### Exports
- Use **named exports** for all modules.
  - Example:
    ```typescript
    // In userProfile.ts
    export function getUserProfile(id: string) { ... }
    ```

### Commit Messages
- Freeform style, no enforced prefixes.
- Average message length: ~48 characters.
  - Example:  
    ```
    Add initial user profile fetch logic
    ```

## Workflows

### Adding a New Module
**Trigger:** When creating a new feature or utility.
**Command:** `/add-module`

1. Create a new file using camelCase naming (e.g., `featureName.ts`).
2. Implement your logic and use named exports.
3. Use relative imports for any dependencies.
4. Write a corresponding test file (e.g., `featureName.test.ts`).
5. Commit your changes with a clear, concise message.

### Updating an Existing Module
**Trigger:** When modifying or refactoring existing code.
**Command:** `/update-module`

1. Locate the relevant file using camelCase naming.
2. Make your changes, ensuring you maintain named exports.
3. Update or add tests as needed.
4. Commit with a descriptive message.

### Writing Tests
**Trigger:** When adding or updating functionality.
**Command:** `/write-test`

1. Create or update a test file with the pattern `*.test.ts`.
2. Write tests for all new or changed logic.
3. Use the project's test runner to verify correctness.

## Testing Patterns

- Test files are named with the `*.test.*` pattern (e.g., `userProfile.test.ts`).
- The specific testing framework is not specified; follow the existing patterns in the repository.
- Place test files alongside the modules they test or in a dedicated test directory as appropriate.

## Commands
| Command         | Purpose                                    |
|-----------------|--------------------------------------------|
| /add-module     | Start the process of adding a new module   |
| /update-module  | Guide for updating an existing module      |
| /write-test     | Instructions for writing or updating tests |
```