# ⏱️ OMPS ADP Timecard Tracking — Slack List + Workflow

**Owner:** Pete Brogowski, Manager OMP (NEDS)
**Built:** 2026-09-27  |  **First live cycle:** Mon 2026-09-28  |  **First automated run:** Mon 2026-10-12
**Status:** ✅ Live

---

## 🗺️ Big Picture

Every 2 weeks (pay Monday), OMPS timecards are due in ADP by **10:00**, and manager approval is due by **13:00**.
Slack handles the **reminders and tracking**. **ADP is the source of truth.**

```
07:00 ──────► 09:30 ──────► 10:00 ──────► by 13:00
Tasks + DMs   Optional      🔴 check +    Approve in ADP
auto-sent     nudge         DM stragglers + check 👍
```

---

## 🧩 Components

| Piece | Name | What it does |
|---|---|---|
| 📋 Slack List | **OMPS Time Cards** | One task per person per pay period |
| 🔁 Workflow | **⏱️ Timecard tasks – Monday** | Every 2 weeks, Mon 07:00: creates 7 tasks + sends 7 DMs |
| 🔔 Notification | (built into List) | Pings Pete when a task is marked complete |
| 👁️ Saved view | **🔴 Not submitted** | Filter: task complete ⭕ = unchecked |

- **List link:** https://newenglanddon-hg24425.slack.com/lists/TG6GE61QE/F0C4T78HN6S
- **ADP:** https://workforcenow.adp.com/public/index.htm

---

## 📋 List Structure — OMPS Time Cards

| Column | Type | Filled by |
|---|---|---|
| ⭕ (built-in task circle) | Task complete | **Employee**, after submitting in ADP |
| Name | Text (locked primary column) | Workflow → `Timecard – due Monday 10:00 AM` |
| Assignee | People (single) | Workflow |
| Due Date | Date (no time option) | Workflow → *Date the workflow ran* |
| 👍 Approved | Checkbox | **Pete**, after approving in ADP |
| Notes | Text | Anyone (PTO, on a case, etc.) |

- **Sharing:** 6 OMPS + Pete, **Can edit** (not shared to a channel)

---

## 🔁 Workflow — ⏱️ Timecard tasks – Monday

**Trigger:** On a schedule, starts **Mon 10/12/2026 07:00 ET**, repeats **every 2 weeks on Monday**

| Steps | Action |
|---|---|
| 1–7 | **Add an item to a list** → OMPS Time Cards, one per person, Due Date = *Date the workflow ran* |
| 8–14 | **Send a message** → DM to each person (including Pete) |

**Team roster in workflow:** Rachel Bates, William Like, Noah Murray, Olivia Bourgeois, Brian Tiu, Idio Dos Reis, Pete Brogowski

**DM text:**
```
⏰ Timecard Monday: due by 10:00 AM today

Please complete and submit your timecard in ADP by 10:00 AM:
👉 https://workforcenow.adp.com/public/index.htm

Then mark your task complete ⭕ ✅ in OMPS Time Cards:
📋 [List link]

I'll review and approve by 1300. Thanks, team! 🙌
```
> ⚠️ Workflow Builder does **not** convert `*asterisks*` to bold — use ⌘B in the editor.

---

## ✅ Pay-Monday Checklist (Pete)

- [ ] **07:00** — Confirm tasks + DMs went out
- [ ] **09:30** *(optional)* — Open 🔴 view, friendly nudge
- [ ] **10:00** — Open 🔴 view → DM anyone still listed
- [ ] **10:00–13:00** — Approve each timecard in **ADP**, then check 👍 on their row
- [ ] Confirm every ⭕ matches a timecard actually in the ADP approval queue

---

## 🛠️ Maintenance

| When | Do |
|---|---|
| **New hire** | Add 1 "Add an item" step + 1 DM step to the workflow; share List with them |
| **Departure** | Delete their 2 steps; remove from List sharing |
| **Holiday shifts pay Monday** | Workflow won't know — send a manual reminder + add rows by hand |
| **Workflow didn't run** | Check Workflows → run history; duplicate a prior row set manually |
| **Safe test** | Duplicate workflow → keep only Pete's 2 steps → schedule 5 min out → delete after |

---

## 🧠 Lessons Learned (build notes)

- Slack's **first List column is locked as text** — rename only.
- **Date columns have no time option** → put "due 10:00 AM" in the task name.
- The **built-in task circle** beats a separate checkbox (shows in *Assigned to you*).
- Date variable = **date the workflow ran** only → schedule moved from Sunday night to **Monday 07:00** so Due Date is correct and the task doubles as the reminder.
- Scheduled triggers must be a **future** date/time.
- Don't test-run the live workflow — it pings all 7 people.
