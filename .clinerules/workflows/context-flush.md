# Workflow: Context Reset & Handover

## 📋 Objective

Clear the AI's active memory while preserving all critical project state in the Memory Banks.

## 🤖 AI Execution Steps

1. **Final Sync:** Update `progress.md` with the exact line of code or task currently being worked on.
2. **Knowledge Check:** Verify that all new "Infrastructure" or "DAO" findings are in `systemPatterns.md`.
3. **The Handover Note:** Write a "Handover Note" at the bottom of `activeContext.md` titled `## Handover for Next Session`.
   - State exactly where the cursor should go next.
   - State the last successful command run.
4. **The Reset:** Instruct the human to "Start a new Chat" and point the new session to the `activeContext.md`.
