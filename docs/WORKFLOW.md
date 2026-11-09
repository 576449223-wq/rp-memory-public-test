# Archive Update Workflow

> This is a workflow specification for testing only. It does not authorize putting private archives in this public repository.

## A. Before an update
1. Identify the exact project by its Project ID and canonical repository path.
2. Read the current project index and relevant archive files.
3. Confirm the requested source event belongs to this project.
4. Check for contradictions, missing timestamps, and unsupported assumptions.
5. If a required fact is missing, preserve it as UNKNOWN rather than inventing it.

## B. Prepare the change
1. Add each new event as an immutable event record.
2. Update the continuity snapshot only with facts supported by recorded events.
3. Update character knowledge separately for each character.
4. Preserve prior values in the change log when correcting a field.
5. Never silently overwrite an earlier event or merge two projects.

## C. Validate before commit
- Project ID matches the target archive.
- No content from another project is included.
- User-controlled protagonist actions, dialogue, thoughts, feelings, or decisions have not been authored by the assistant.
- Timeline order is consistent.
- Character knowledge has a plausible source and acquisition time.
- Unknown facts remain explicitly UNKNOWN.
- All changed files are listed in the proposed summary.

## D. Commit and verify
1. Present a concise change summary.
2. Write only to the explicitly selected test path.
3. Commit with a descriptive message.
4. Read the committed files back from GitHub.
5. Compare the read-back content with the intended content.
6. Report success only after read-back verification.

## E. Corrections and rollback
- Corrections create a new change-log entry; they do not erase historical evidence.
- Record old value, corrected value, reason, and source.
- Prefer a new corrective commit over destructive history rewriting.
- If verification fails, stop and report the failure. Do not claim success.

## F. Privacy boundary
This repository is public. Never store real roleplay archives, personal information, private messages, credentials, API keys, or sensitive material here. Use a separate private repository for any future real project archive, after its access scope has been checked.
