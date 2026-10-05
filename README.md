# 📊 CPM Project Planner Pro

A free, browser-based **Critical Path Method (CPM) project scheduling and visualization tool**.

CPM Project Planner Pro allows users to create project schedules, calculate critical paths, analyze float, visualize PDM networks and Gantt charts, track project costs, and import/export project data — directly in the browser.

No installation or backend server is required.

## 🌐 Live Application

### 👉 [Launch CPM Project Planner Pro](https://musadsaiyed.github.io/CPM-Project-Planner/)

---

## ✨ Features

### 📋 Interactive Project Schedule

Create and edit project activities directly in the browser.

Each activity can contain:

- Activity ID
- Task Name
- Duration
- Predecessors
- Logical Relationships
- Lag
- Cost

Activities can be added or removed at any time.

---

## 🧮 CPM Calculations

The application automatically performs CPM forward and backward pass calculations.

Calculated values include:

- Early Start (ES)
- Early Finish (EF)
- Late Start (LS)
- Late Finish (LF)
- Total Float (TF)
- Project Duration
- Critical Activities
- Critical Path

Critical activities are automatically identified and highlighted.

---

## 🔗 PDM Logical Relationships

CPM Project Planner Pro supports all four standard Precedence Diagramming Method relationships:

| Relationship | Description |
|---|---|
| **FS** | Finish-to-Start |
| **SS** | Start-to-Start |
| **FF** | Finish-to-Finish |
| **SF** | Start-to-Finish |

Positive and negative lag values are supported.

Examples:

```text
FS+2
SS+3
FF+1
SF-2
```

### Default Relationship

If no relationship is entered, the application automatically assumes:

```text
FS with 0 lag
```

Therefore, basic Finish-to-Start schedules can be entered without repeatedly specifying `FS`.

---

## 🕸️ PDM / Activity-on-Node Network Diagram

The application automatically generates a **Precedence Diagramming Method (PDM) / Activity-on-Node (AON)** network.

Activity nodes display scheduling information such as:

```text
ES       Activity       EF
LS       Duration       LF
```

Total Float is also displayed.

Critical activities and relationships are visually distinguished from non-critical activities.

---

## 🧠 Smart Network Layout

The PDM diagram includes automatic layout logic designed to improve network readability.

The layout attempts to:

- Reduce crossing arrows
- Keep related activities together
- Separate multiple incoming relationships
- Separate multiple outgoing relationships
- Prevent arrows from unnecessarily passing through activity boxes
- Reduce confusing relationship paths
- Improve the overall left-to-right project flow

Activity positions may be rearranged visually to improve readability without changing the actual scheduling logic.

---

## ▶️ Intelligent START and END Nodes

START and END milestones are displayed only when needed.

If there is only **one starting activity**, an additional START node is not required.

If multiple activities can start independently, the application creates a common **START** node.

Similarly, if there is only one terminal activity, an additional END node is not required.

If multiple activities terminate independently, a common **END** node is created.

---

## 📅 Gantt Chart

The project schedule is automatically visualized as a Gantt chart.

The chart helps users understand:

- Activity start times
- Activity finish times
- Activity durations
- Critical activities
- Available float
- Overall project duration

---

## 💰 Project Cost Analysis

Optional activity costs can be entered into the schedule.

The application can display:

- Activity costs
- Total project cost
- Cumulative project cost
- Cost progression throughout the project

If cost analysis is not required, costs can simply remain at `$0`.

---

## 📂 Smart CSV Import

Project schedules can be imported from CSV files.

The importer supports common scheduling fields including:

```text
Activity
Task Name
Duration
Predecessor
Relationship
Lag
Cost
```

Column-name variations are also supported.

### Multiple Predecessors

If the same activity appears on multiple CSV rows because it has multiple predecessors, the importer can combine those relationships into a single activity.

Example:

```text
Activity,Duration,Predecessor,Relationship,Lag
F,5,C,SS,2
F,5,D,FS,0
```

is interpreted as:

```text
Activity F
Predecessors: C, D

C → F = SS+2
D → F = FS+0
```

Default `FS+0` relationships can remain visually blank to keep the schedule table clean.

---

## 📤 Import and Export

The application supports:

- CSV Import
- CSV Export
- PDM Network SVG Export
- Gantt Chart SVG Export
- Cost Chart SVG Export
- Printable project reports
- PDF output through the browser's print functionality

---

## 🎲 Practice Project

The application includes a simple **A–G CPM practice network**.

The practice network can generate random activity durations while maintaining straightforward predecessor logic.

This makes it useful for practicing:

- Forward pass
- Backward pass
- Critical path identification
- Float calculations
- Network scheduling

---

## 🚀 How to Use

1. Open CPM Project Planner Pro.
2. Add activities manually or import a CSV schedule.
3. Enter activity durations.
4. Enter predecessors.
5. Specify SS, FF, SF, or lag relationships where required.
6. Leave the relationship blank for standard `FS+0`.
7. Enter activity costs if cost analysis is required.
8. Review the CPM calculations.
9. Inspect the PDM network.
10. Review the Gantt chart.
11. Export or print the required results.

---

## 💻 Running Locally

No installation is required.

Download:

```text
index.html
```

and open it using a modern web browser.

---

## 📁 Repository Structure

```text
CPM-Project-Planner/
│
├── index.html
├── README.md
├── CHANGELOG.md
└── LICENSE
```

`index.html` contains the main browser application.

---

## 🛠️ Built With

- HTML
- CSS
- JavaScript
- SVG
- Client-side CPM scheduling logic

The application runs entirely in the browser.

---

## 🎓 Intended Use

CPM Project Planner Pro is particularly useful for:

- Project Management students
- Civil Engineering students
- Construction Management students
- Construction scheduling practice
- CPM exercises
- PDM/AON network visualization
- Small project schedule analysis

---

## ⚠️ Disclaimer

CPM Project Planner Pro is primarily an **educational and planning tool**.

Although the application performs automated scheduling calculations, users should independently verify results before using them for professional, contractual, construction, financial, or other critical project decisions.

---

## 🐛 Bug Reports & Suggestions

Found a problem or have an improvement idea?

Please open a GitHub Issue and, when possible, include:

- A description of the problem
- Expected behavior
- CSV/project data that caused the issue
- Screenshot of the issue

Contributions and suggestions are welcome.

---

## 👨‍💻 Author

**Musad Saiyed**

Master of Engineering – Civil Engineering  
Project Management  
University of Calgary

---

## ⭐ Support

If you find CPM Project Planner Pro useful, consider giving the repository a **⭐ Star**.

It helps others discover the project.

---

### CPM Project Planner Pro

**Plan. Calculate. Visualize. Understand.**
