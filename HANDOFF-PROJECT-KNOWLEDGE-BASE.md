# Project Handoff: Project Knowledge Base (PKB)

## 📋 Overview
**Date:** 2026-09-21
**From:** Secretary Kim (with @engi, @aunt-next-door)
**To:** Next session / team member

---

## 🎯 Project Summary
Ampas Industries Project Knowledge Base — a self-contained HTML portal that showcases 18 PE (Process Engineering) projects with an interactive animated background featuring a4-way industrial estate intersection.

## 📁 File Structure

```
handoff-project-knowledge-base/
├── SKILL.md                          # Handoff skill documentation
├── README.md                         # Repo documentation
├── pkb-homepage.html                 # 🏠 Portal homepage (main entry)
├── project-knowledge-base.html       # 📋 18 project detail pages
└── hermes-teams-architecture.html    # 🏗️ PE Bot architecture (iframe)
```

## 🔗 Navigation Flow

```
pkb-homepage.html (Portal)
    │
    └── "📋 View All Projects" button
            │
            └── project-knowledge-base.html
                    │
                    └── Click project card → detail page
                            │
                            └── PE Bot (#6) → Architecture tab
                                    │
                                    └── hermes-teams-architecture.html (iframe)
```

## 🏠 pkb-homepage.html — Portal

### Features
- **Header:** "🏠 Ampas Industries Portal"
- **Stats:** 18 Projects, 15 Worked, 1 Failed, 2 Pitfall
- **Portal Link:** "📋 View All Projects" → project-knowledge-base.html
- **3D Wrench:** CSS 2.5D illustration with tilt animation (±12°)
- **Background:** Animated 2D industrial estate4-way intersection
- **Cars:** JS random spawner, 4 directions, bright colors
- **Factories:** 4 large buildings (only 1/4 visible at intersection corners)
- **Trees:** 8 decorative trees along road edges

### Technical Details
- **Self-contained:** Single HTML file, no external dependencies (except Google Fonts)
- **3D Wrench:** Uses `clip-path: polygon()` for wrench shape, `transform-style: preserve-3d` for 2.5D tilt
- **Cars:** JavaScript spawner with random timing (1.2-3.5s intervals), random speeds (6-12s)
- **Background:** `position: fixed` — doesn't scroll with page

### CSS 3D Wrench Approach
- **NOT a rotating cube** — uses 2.5D tilt (±12°) to avoid exposing side faces
- Front/back faces: wrench shape via `clip-path: polygon()`
- Side faces: rectangular strips (only visible at small angles)
- Animation: subtle tilt, not full 360° rotation

### Car Spawning
- 4 car types: right, left, down, up
- 6+ colors: red, yellow, white, blue, green, orange, purple, teal
- Random speed per car (6-12 seconds to cross screen)
- Random spawn interval (1.2-3.5 seconds)
- Cars are removed after crossing screen

## 📋 project-knowledge-base.html — Projects

### Features
- 18 projects with detailed information
- Search and filter functionality
- Pipeline flow charts
- Branch history timelines
- Architecture tabs (for projects with architecture_url)

### Projects Included
1. WI Generator
2. PFMEA Tool
3. Process Control Plan
4. Run@Rate Generator
5. Excel WI Translation
6. PE Self-Audit Bot (has Architecture tab)
7. MiMo Calculator
8. 3-Bot 'Best New Team'
9. Excel High-Fidelity Automation
10. Executive Presentation
11. Excel Data Verification
12. PDF-to-Excel Conversion
13. Storyboard Generator
14. Excel MCP Server
15. PE Audit Presentations
16. PE Audit Bot PWA
17. PFMEA Universal Prompt
18. Excel Capture Tool

## 🏗️ hermes-teams-architecture.html

- Embedded via iframe in PE Bot (#6) Architecture tab
- Shows Hermes Agent architecture for Teams bot
- Self-contained HTML file

## 🔧 Known Issues & Limitations

1. **Wrench 2.5D only** — Cannot do full 360° rotation because CSS clip-path wrench shape doesn't extrude properly to side faces
2. **Cars are 2D** — Bird's eye view only, no perspective
3. **Factories are static** — Only smoke animates, buildings don't move
4. **No edit/delete UI** — Read-only portal

## 📝 Design Decisions

### Why 2.5D Wrench (not full 3D)?
- CSS `clip-path: polygon()` creates a 2D shape
- When rotated 90°, side faces show as plain rectangles (not wrench profile)
- Solution: tilt only ±12° for subtle 3D effect without exposing broken sides

### Why JS Car Spawner (not CSS animation)?
- CSS `animation-delay` is fixed — all cars appear at same time
- JS allows random spawn timing and speed
- Cars are created/destroyed dynamically

### Why Fixed Background?
- Background should stay in place while scrolling portal content
- `position: fixed` ensures intersection is always centered

## 🚀 How to Run

1. Open `pkb-homepage.html` in browser
2. Or use: `file:///D:/AI_Hermes/pkb-homepage.html`
3. Click "📋 View All Projects" to see all 18 projects

## 📂 GitHub Repository

**https://github.com/Waefinder/handoff-project-knowledge-base**

## 👥 Team

| Role | Agent |
|------|-------|
| Planner/Coordinator | Secretary Kim |
| Main Worker | @engi |
| Reviewer | @aunt-next-door |

## 📞 Contacts

- **GitHub:** Waefinder
- **Hermes Profile:** secretary-kim-2

---

*Last updated: 2026-09-21*
