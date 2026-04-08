# CERA Project Memory — Setup Guide (v1.01)

## What's New in v1.01

CERA v1.01 introduces a **two-tier architecture** that separates
session-level reasoning (session maps) from cross-session synthesis
(CERA Index). This replaces the single PROJECT_MEMORY.md file from
earlier versions.

**Key changes from v0.x:**
- Each conversation produces its own **session map** — a standalone
  reasoning record
- A dedicated **integrator conversation** synthesizes across sessions
  and produces the **CERA Index**
- The CERA Index is a lean cross-session index with connective tissue,
  not a monolithic memory file
- Bidirectional provenance tracking links every conclusion to its origin
- Native memory signposts provide lightweight orientation

---

## What You Need

1. The **SKILL.md** file (the CERA skill framework, v1.01)
2. A **Claude project** to install it in
3. Project context files (documents, transcripts, etc.) — optional
   but recommended

---

## Step 1: Install the Skill

1. In Claude, go to **Settings** (or the skills menu)
2. Find **cera-project-memory** in your skills list
3. Toggle it **ON**

The skill is now available globally. It activates when invoked inside
projects — everywhere else it stays dormant.

If the skill doesn't appear in your list, you may need to upload the
SKILL.md file as a custom skill. (Check Claude's current skill
installation process — this may vary as the feature evolves.)

---

## Step 2: Create or Open Your Project

1. In Claude, create a new **Project** (or open an existing one)
2. Add any relevant context files to the project's knowledge base:
   - Case documents, transcripts, prior work product
   - Existing notes or strategic documents
   - These give Claude raw material for the first session

---

## Step 3: First Working Session

1. Start a **new conversation** inside the project
2. Invoke CERA with a hash call (e.g., `/cera-project-memory`)
3. Claude detects no existing CERA artifacts and proceeds normally
4. Work on whatever you need — Claude operates with Layer 0
   collaborative reasoning protocol active
5. When ready, call for a **checkpoint**
6. Claude creates **SESSION_MAP_S01_V01.md** — the first session map
7. **Download** the session map file

---

## Step 4: Upload the Session Map

1. Go to your project's **knowledge base** (the files/documents section)
2. **Upload** the SESSION_MAP_S01_V01.md file
3. That's it — your first session is captured

---

## Step 5: Continue Working (Optional — Before Integration)

You can have multiple working sessions before creating the integrator:

1. Start a **new conversation**, invoke CERA
2. Claude sees the session map from your prior session and orients
   from it
3. Work, then checkpoint — Claude creates **SESSION_MAP_S02_V01.md**
4. Download and upload to the project knowledge base

Note: If Claude sees two or more session maps without a CERA Index,
it will remind you to create the integrator conversation. This is a
gentle nudge, not a blocker — you can continue working.

---

## Step 6: Create the Integrator Conversation

This is the dedicated management conversation that builds and maintains
the CERA Index.

1. Start a **new conversation** inside the project
2. Declare it as the integrator: **"This is the CERA integrator
   conversation"**
3. Claude acknowledges and enters integrator mode
4. Call for the first integration: **"Run integration"**
5. Claude reads all session maps from the project, synthesizes across
   them, and creates **CERA_INDEX_V01.md**
6. **Download** the CERA Index file
7. **Upload** it to the project knowledge base

---

## Ongoing Use

### Every working conversation:
- Invoke CERA at conversation start
- Claude reads the CERA Index for orientation (project overview,
  trajectory, strategic posture, session index)
- Claude loads the project-level primer and activation questions
- You work with full accumulated context
- Checkpoint when significant reasoning occurs → new session map
- Upload the session map to the project knowledge base

### Periodic integration (every 2-5 sessions, or as needed):
- Go to the integrator conversation
- Call for integration
- Claude reads new session maps, synthesizes, and updates the
  CERA Index
- Download the updated CERA Index
- Upload to the project knowledge base

### Within a single session (multiple checkpoints):
- If a session has multiple significant developments, call for
  additional checkpoints
- Claude versions the session map (S01_V01 → S01_V02 → S01_V03)
- Upload the latest version to the project (you can remove or keep
  prior versions — Claude always uses the highest version number)

### Periodic maintenance (every 10-15 sessions):
- In the integrator conversation, request a maintenance integration
- Claude performs deep analysis: dependency mapping, convergence/
  divergence, pruning, consolidation, trajectory update
- Produces a refreshed CERA Index

---

## Quick Reference

| Action | Who Does It | When |
|--------|------------|------|
| Toggle skill ON | You (once) | Setup |
| Create project | You (once) | Setup |
| Invoke CERA in conversation | You | Start of each session |
| Create session map | Claude (at checkpoint) | Working sessions |
| Upload session map to project | You (~30 sec) | After checkpoints |
| Declare integrator conversation | You (once) | After 1-2 sessions |
| Run integration | Claude (when called) | Every 2-5 sessions |
| Upload CERA Index to project | You (~30 sec) | After integration |
| Update native memory signposts | Claude (automatic) | At integration |
| Suggest maintenance | Claude | Every 10-15 sessions |

---

## File Naming Reference

| File | Naming Pattern | Created By |
|------|---------------|-----------|
| Session maps | SESSION_MAP_S01_V01.md | Working sessions |
| CERA Index | CERA_INDEX_V01.md | Integrator only |
| Legacy memory | PROJECT_MEMORY.md | Prior CERA versions |

- Session maps: S = session number, V = version within session
- CERA Index: V = version across integrations
- Claude always uses the highest version number for each file type
- Legacy PROJECT_MEMORY.md is treated as V00 seed material

---

## Migrating from v0.x

If your project has an existing PROJECT_MEMORY.md from CERA v0.x:

1. **Leave it in the project knowledge base** — don't remove it
2. Install the updated SKILL.md (v1.01)
3. Start a new working session and invoke CERA
4. Claude recognizes the legacy file and orients from it
5. Work normally, checkpoint → Claude creates SESSION_MAP_S01_V01.md
   in the new format
6. When you create the integrator conversation, Claude uses the
   legacy PROJECT_MEMORY.md as V00 seed material for the first
   CERA Index
7. After the first CERA Index is created, the legacy file is no
   longer needed (but keeping it doesn't cause problems — Claude
   prioritizes the versioned CERA Index)

---

## Troubleshooting

**Claude doesn't seem to remember anything from prior sessions:**
- Check that session maps and/or CERA Index are in the project's
  knowledge base
- Check that the CERA skill is toggled ON
- Invoke CERA explicitly at conversation start

**Claude warns about multiple session maps without a CERA Index:**
- This is expected if you haven't created the integrator yet
- Create the integrator conversation and run the first integration
- Or continue working — it's a reminder, not a blocker

**The integrator conversation is getting long:**
- Start a new integrator conversation
- The CERA Index carries the integration history (promotion log,
  revision notes), so a new integrator conversation can pick up
  where the old one left off
- The old integrator transcript provides additional context if needed

**Claude is applying CERA outside of projects:**
- This shouldn't happen — the skill activates only when invoked
- If it does happen, let Claude know: "We're not in a CERA project"

**Session map or CERA Index seems too large:**
- Request a maintenance integration in the integrator conversation
- Claude will prune, consolidate, and compress

**You accidentally left multiple versions of a file in the project:**
- No problem — Claude always uses the highest version number
- Clean up when convenient, but it won't cause errors

**You want to start CERA in a second project:**
- Each project gets its own independent set of session maps, CERA
  Index, and integrator conversation
- Reasoning patterns can be promoted across projects with your
  approval (cross-pollination protocol)

---

*Setup guide for CERA Project Memory Skill v1.01*
*Last updated: April 3, 2026*
