# OCR A Level Computer Science NEA (H446)  
## Python-friendly project ideas — student guide

You’re choosing an NEA project that must generate evidence for **Analysis, Design, Development/Testing, and Evaluation**. The easiest way to do that is to build a **real tool for a real user** (stakeholder) with **data + rules + edge cases**.

---

## 1) What makes a “good” NEA project

Pick a project that has:

### A real stakeholder
- A teacher, technician, librarian, club leader, family member, small business, etc.
- You can interview them twice: **start (requirements)** and **end (evaluation)**.

### Measurable success criteria
Examples:
- “Reduces time to do X from 20 minutes to 5.”
- “Prevents double-booking.”
- “Produces a weekly report automatically.”

### Enough technical depth
Aim for **2–3** of these:
- A proper **data model** (multiple related entities)
- A meaningful **algorithm** (matching, scheduling, searching, ranking, simulation)
- A **workflow/state** (submitted → approved → completed)
- **Parsing/importing** data (CSV/log files)
- **Permissions/roles** (admin vs normal user)
- **Analytics/reporting** (charts optional; summary tables are fine)

### Buildable in time
A finished MVP with excellent testing beats an unfinished “mega app”.

---

## 2) Python project types that score well (pick one)

Each idea below is “NEA-shaped”: it naturally produces content for every write-up section.

### A) School operations tools (high success rate)

1. **Intervention / revision session scheduler**
   - Core: schedule students into sessions with constraints (capacity, clashes, priorities)
   - Depth: constraint checking + prioritisation rules + reporting

2. **Room/equipment booking system**
   - Core: create bookings and prevent clashes
   - Depth: overlap detection + roles (staff/admin) + audit log

3. **Club sign-up with waitlist + priority**
   - Core: signup, capacity, waitlist
   - Depth: fairness rules + auto-promotion + reports

4. **Library loans + reservations**
   - Core: checkout/return/reserve
   - Depth: state transitions + overdue rules + usage reports

### B) Revision and learning tools (good if adaptive/analytic)

5. **Revision planner (spaced practice)**
   - Core: generates a weekly plan from topics + deadlines
   - Depth: scheduling algorithm + progress tracking + analytics

6. **Adaptive quiz engine + weakness analysis**
   - Core: question bank with tags and quiz creation
   - Depth: adaptive selection rules + performance tracking + reports

7. **Exam question tracker + recommender**
   - Core: log completed questions and scores
   - Depth: recommend “next best” questions based on gaps

### C) Data-heavy tools (great for testing evidence)

8. **CSV markbook analyser**
   - Core: import CSV, summarise performance, identify priority students/topics
   - Depth: parsing + data cleaning + ranking/grouping + report generation

9. **Log analyser (e.g., network/firewall logs)**
   - Core: parse logs and flag suspicious patterns
   - Depth: rule engine + pattern matching + summary reports

10. **Inventory/asset tracker**
   - Core: track items, check-in/out, condition
   - Depth: audit trail + reconciliation rules + reports

### D) Scheduling/optimisation style (strong algorithm write-up)

11. **Student group generator with constraints**
   - Core: auto-generate groups
   - Depth: balancing algorithm (ability/behaviour/EAL etc.) + constraints

12. **Work experience placement matcher**
   - Core: match students to placements based on preferences/constraints
   - Depth: scoring/matching algorithm + fairness constraints + reporting

### E) Simulation/modelling (excellent design + evaluation)

13. **Epidemic spread simulation**
   - Core: simulate spread with adjustable parameters
   - Depth: simulation loop + experiments + graphs/tables for outcomes

14. **Queue/throughput simulation (canteen/library)**
   - Core: simulate queues under different staffing levels
   - Depth: scenario comparisons + results + recommendations

### F) Game projects (only choose if you include real CS depth)

15. **Maze/stealth game with pathfinding enemies**
   - Required depth: A* pathfinding + finite state machine AI + level data model

16. **Puzzle game with level editor + solver/hints**
   - Required depth: editor tools + search/backtracking solver + testable level cases

---

## 3) What you must produce for the write-up (choose a project that supports it)

Whatever you pick, you must be able to show:

### Analysis
- Interview notes + current process (“how they do it now”)
- **8–12 functional requirements** + **4–6 non-functional**
- **Success criteria** (measurable)

### Design
- Data model (tables/classes)
- Key algorithms in pseudocode/flow
- UI sketches + navigation
- Architecture (modules/files)

### Development + Testing
- Iterations (build → test → fix)
- Evidence of technique (validation, data structures, algorithms)
- Test plan + results + fixes

### Evaluation
- Stakeholder feedback vs success criteria
- What worked, what didn’t, what you’d improve next

---

## 4) A simple Python tech stack that works

Choose one (keep it manageable):

### Option 1: Desktop app
- Python + `tkinter` (or `ttkbootstrap`)
- SQLite for data

### Option 2: Web app
- Python + Flask
- SQLite
- HTML templates (Jinja)

### Option 3: Command-line tool (allowed if well designed)
- Python CLI + SQLite/CSV
- Strong reporting output + solid test suite

**Tip:** pick the stack you already know best. The NEA rewards evidence and correctness, not trendy frameworks.

---

## 5) Avoid these common traps

Projects that often underperform:
- “Just CRUD” (add/edit/delete only) with no rules/logic
- Static websites with minimal backend logic
- API-dependent ideas that break when the API changes
- Hardware projects with unreliable kit (unless you have a software-only fallback)

---

## 6) Quick project approval checklist (use this before committing)

You should be able to answer **yes** to all of these:

- I have a stakeholder I can interview twice.
- I can write **8–12 functional requirements**.
- I can define **measurable success criteria**.
- My project includes **2–3 complexity drivers** (data + algorithm + workflow is ideal).
- I can build an MVP in **6–8 weeks**, then improve it.
- I can create at least **12–20 test cases** (normal, boundary, invalid, edge).

