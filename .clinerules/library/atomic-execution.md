# Atomic Execution Protocols

## 1. Chunked Generation (Large Spec/Docs)

*Use for OpenAPI YAML, Javadocs, or large logs.*

- **Scaffold First:** Create the file structure with headers/placeholders only.
- **The Append Loop:** Read ONE source file, generate its segment, and append/merge.
- **Verify:** Validate syntax after every append to prevent "Loop of Death" cutoffs.

## 2. Surgical Refactoring (Large File Logic Moves)

*Use for files >500 lines or moving logic to helpers.*

- **Plan:** State exact line ranges to be replaced before acting.
- **Delete-then-Import:** Delete the old logic *first*, then add the import/call.
- **The Usage Audit:** After refactoring, search for the old function name; if it still exists, the task is a failure.
