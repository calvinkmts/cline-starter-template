# Context Window & Memory Management

## 📉 The 60% Threshold Rule

You must actively monitor the size of the current conversation context.

- **Threshold:** Once you estimate the context is 60% full, or the conversation history exceeds 20-30 turns, you MUST trigger a "Context Reset" protocol.
- **Action:** Before reaching the limit, notify the developer: "Context window is approaching threshold. I need to summarize and reset."

## 🧠 Summarization Protocol (The "Brain Dump")

Before a context reset or when a major milestone is reached:

1. **Sync Memory Banks:** Ensure `activeContext.md` and `systemPatterns.md` contain every critical discovery from the current session.
2. **Prune History:** Identify information that is now "redundant" (e.g., old error logs that have been fixed).
3. **Consolidate:** Move transient "Recon" data into permanent `docs/recon/` files so it can be removed from the active chat window.

## 🚫 No-Dump Policy

- Never re-read a file you have already analyzed in the current session unless it has been modified.
- Use `grep` or `sed` to extract specific lines rather than reading entire large files.
