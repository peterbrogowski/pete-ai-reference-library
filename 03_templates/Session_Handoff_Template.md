# Session Handoff: SFD_CHECK System & Project Export Workflow

**Date:** March 20, 2025  
**Duration:** Long session  
**Status:** Complete for this phase  
**Next session ready for:** Organ Machine Perfusion export or organic use of `<<SFD_CHECK>>`

---

## ✅ What We Built

### 1. **`<<SFD_CHECK>>` Collaborative Sense-Making Tool**
**Status:** Ready to use immediately

**What it is:**
- A tag-based system (`<<SFD_CHECK>>`) for working through fuzzy ideas
- 5-step workflow: Listen → Clarify → Reflect → Truth-Tell → Decide
- Uses interactive widgets (`ask_user_input`) instead of prose questions
- Designed for ADHD brain and honest collaboration

**Files created:**
- `SFD_CHECK_System_Prompt.md` (detailed system documentation)
- Already integrated into your Claude custom instructions

**How to use:**
```
<<SFD_CHECK>>

Here's my rough idea: [shitty first draft]
```

Then I automatically run the 5-step workflow.

---

### 2. **Fresh Custom Instructions (v2.0)**
**Status:** Added to Claude settings

**What changed:**
- ✅ Removed competing systems (logs, snapshots, continuity files)
- ✅ Replaced confirmation codes with interactive widgets
- ✅ Kept only 3 core modes: Autonomy, `<<SFD_CHECK>>`, Handoff
- ✅ Much leaner and actually usable
- ✅ ADHD-friendly formatting

**Three operating modes:**
1. **Autonomy Mode** – I act independently (default)
2. **`<<SFD_CHECK>>` Mode** – Collaborative sense-making
3. **Handoff Mode** – Long session continuity (manual request)

**File:** `Claude_Custom_Instructions_v2.md`

---

### 3. **Project Export Prompt Template**
**Status:** Tested and working

**What it is:**
A reusable prompt you can give to any AI to export a project.

**How it works:**
- Works with ChatGPT, Claude, or any AI
- AI reads your chat context and understands "the current project"
- Generates a bash script automatically
- Script creates complete folder structure + context files on Desktop
- Folder is GitHub-ready

**Key features:**
- 10 numbered folders (00_START_HERE through 10_IMPORTS_RAW)
- Auto-generated Markdown context files
- JSON state files for machine readability
- AI startup prompt for next continuity transfer
- Safe (won't overwrite existing folders)

**Tested on:** CTP Curriculum Project (successfully exported to GitHub)

---

### 4. **Working GitHub Repository**
**Status:** Live and accessible

**Project:** CTP Curriculum Project  
**URL:** https://github.com/peterbrogowski/ctp-curriculum-project  
**Structure:** Complete with all 10 folders

**Current state:**
- ✅ Structure is solid
- ⚠️ Many Markdown files are stubs (need manual enrichment)
- ✅ Raw imports folder has real content (PDF + knowledge base)
- 📌 Ready to be fleshed out over time

---

## 🧠 Key Insights From This Session

1. **SFD_CHECK > Bash Confirmation Codes**
   - Interactive widgets are more flexible and ADHD-friendly
   - Sequential dialogue beats parallel multi-step systems
   - You'll actually use this

2. **Lean > Bloated**
   - Your old custom instructions had too many competing systems
   - Three core modes (Autonomy, Collaboration, Handoff) is enough
   - Everything else was friction

3. **ChatGPT Already Built This**
   - The export script template is solid
   - You don't need to reinvent it
   - Just reuse the same prompt for all 20 projects

4. **Export Structure Works**
   - The folder/file layout is logical
   - GitHub-ready out of the box
   - Can be enriched over time (doesn't need to be perfect)

---

## ⏭️ What's Ready to Do Next

### Immediate (Whenever you have energy)
- [ ] Test `<<SFD_CHECK>>` on a real shitty first draft
- [ ] Use the export prompt for "Organ Machine Perfusion"
- [ ] Push OMP export to GitHub

### Medium-term (This week/month)
- [ ] Enrich CTP Curriculum repo with real content
- [ ] Fill in MASTER_STATUS and NEXT_ACTIONS for each project
- [ ] Add actual project files to 10_IMPORTS_RAW folders

### Long-term (Ongoing)
- [ ] Export remaining 17 projects using same prompt
- [ ] Build GitHub org structure for all 20 projects
- [ ] Keep context files updated as projects evolve

---

## 📂 Files You Have

**Downloadable (in `/mnt/user-data/outputs/`):**
1. `SFD_CHECK_System_Prompt.md` – System documentation
2. `Claude_Custom_Instructions_v2.md` – Custom instructions (already in settings)

**On your Mac:**
- `~/Desktop/CTP_Curriculum_Project_Export/` (if you ran the script locally)

**On GitHub:**
- https://github.com/peterbrogowski/ctp-curriculum-project

---

## 🗣️ Resume Prompt (For Next Session)

If you return to this work, start here:

```
I have a system for exporting projects to GitHub for AI continuity.

I've already set up:
1. <<SFD_CHECK>> mode for collaborative sense-making
2. Fresh custom instructions (v2.0)
3. A working export template
4. CTP Curriculum project exported to GitHub

Next, I want to export "Organ Machine Perfusion" using the same process.

[Continue from here]
```

---

## 🎯 One Thing to Remember

**You're not trying to be perfect.**

The export is a *skeleton*. It's meant to:
- ✅ Capture structure
- ✅ Provide a starting point
- ✅ Enable AI continuity

You fill in the meat over time. That's fine.

---

## 💬 Questions for Next Session?

If anything is unclear or needs refinement:
- Tag me with `<<SFD_CHECK>>` when you're ready
- I'll help you troubleshoot or improve
- No need to re-explain—I have context

---

## 📊 Session Summary

| What | Status | Effort | Next |
|------|--------|--------|------|
| `<<SFD_CHECK>>` system | ✅ Ready | Done | Use it |
| Custom instructions v2 | ✅ Ready | Done | Already active |
| Export prompt template | ✅ Ready | Done | Use for OMP |
| CTP Curriculum export | ✅ Live | Done | Enrich over time |
| OMP export | ⏳ Ready to run | <5 min | Run when ready |

---

*Handoff created March 20, 2025 by Claude (Haiku 4.5)*  
*For Pete Brogowski*
