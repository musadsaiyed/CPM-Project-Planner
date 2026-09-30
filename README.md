# 📊 CPM Project Planner Pro

**CPM Project Planner Pro** is a free, browser-based project scheduling and Critical Path Method (CPM) analysis tool.

It allows users to create or import a project schedule and automatically calculate CPM results, identify the critical path, generate a PDM / Activity-on-Node network diagram, create a Gantt chart, and analyze project costs.

The application runs entirely in the browser and does not require installation.

---

## 🌐 Live Demo

👉 **[Open CPM Project Planner Pro](https://musadsaiyed.github.io/CPM-Project-Planner/)**

---

## ✨ Features

### 📋 Project Scheduling

Create and edit project activities directly in the browser.

Each activity can include:

- Task Name
- Duration
- Predecessors
- Relationships
- Lag
- Cost

Activities can be added or deleted at any time.

---

### 🧮 Automatic CPM Calculations

The application automatically performs the forward and backward pass and calculates:

- Early Start (ES)
- Early Finish (EF)
- Late Start (LS)
- Late Finish (LF)
- Total Float (TF)
- Project Duration
- Critical Activities
- Critical Path

Critical activities are automatically highlighted in the network diagram.

---

## 🔗 Logical Relationships

The scheduler supports the four standard activity relationships:

| Relationship | Meaning |
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

If a relationship is left blank, the application automatically assumes:

```text
Finish-to-Start (FS) with 0 lag
```

This keeps basic CPM data entry clean and simple.

---

## 📂 Smart CSV Import

Projects can be created manually or imported from a CSV file.

The importer can process scheduling information such as:

```text
Activity
Duration
Predecessor
Relationship
Lag
Cost
```

### Repeated Activities

If an activity appears multiple times in the CSV because it has multiple predecessors, CPM Project Planner Pro automatically merges those rows.

For example:

```text
Activity   Predecessor   Relationship   Lag

F          C             SS             2
F          D
```

is interpreted as one activity:

```text
Activity: F
Predecessors: C, D

C → F = SS+2
D → F = FS+0
```

Blank relationships automatically use the default **FS with 0 lag**.

---

## 🕸️ PDM / Activity-on-Node Network Diagram

The application automatically generates a **Precedence Diagramming Method (PDM)** network.

Activity nodes display scheduling information including:

```text
ES        Activity        EF
LS        Duration        LF
```

Total Float is also displayed for each activity.

Critical activities and critical relationships are visually highlighted.

---

## 🧠 Automatic Network Untangling

The network layout automatically rearranges activity boxes to improve readability.

The layout engine attempts to:

- Reduce crossing relationship lines
- Keep related activities close together
- Reduce unnecessarily long arrows
- Prevent arrows from passing through unrelated activities
- Keep incoming relationships separate
- Keep outgoing relationships separate
- Improve the overall logical flow of the network

Only the **visual position** of activities is changed.

The actual project logic, predecessors, relationships, durations, and CPM calculations remain unchanged.

---

## ▶️ START and END Nodes

START and END nodes are added only when necessary.

### Single Starting Activity

If the project has only one starting activity:

```text
A → B → C
```

no additional START node is displayed.

### Multiple Starting Activities

If several activities can begin independently, a common START node is automatically created.

### Single Ending Activity

If there is only one terminal activity, no additional END node is displayed.

### Multiple Ending Activities

If several activities finish independently, a common END node is automatically created.

---

## 📅 Gantt Chart

The application automatically generates a Gantt chart based on the calculated schedule.

The chart helps visualize:

- Activity timing
- Activity duration
- Critical activities
- Available float
- Overall project duration

---

## 💰 Project Cost Analysis

Optional activity costs can be entered for the project.

The application can calculate and visualize:

- Total Project Cost
- Cumulative Project Cost
- Cost progression throughout the project

If cost analysis is not required, activity costs can simply remain:

```text
0
```

---

## 🎲 CPM Practice Mode

The application includes an **A–G practice project**.

Activities:

```text
A
B
C
D
E
F
G
```

The practice project uses random durations with simple predecessor logic.

A new practice example can be generated using:

**Random A–G**

This can be useful for learning and practicing CPM network calculations.

---

## 📤 Export Options

CPM Project Planner Pro supports several output options:

- Import CSV
- Export CSV
- Save Network Diagram as SVG
- Save Gantt Chart as SVG
- Save Cost Chart as SVG
- Print Project Report
- Save Report as PDF

---

## 🚀 How to Use

1. Open CPM Project Planner Pro.
2. Enter activities manually or import a CSV file.
3. Enter the activity durations.
4. Enter predecessors.
5. Enter relationships only when they differ from the default FS relationship.
6. Add lag where required.
7. Enter activity costs if cost analysis is needed.
8. Review the automatically calculated CPM schedule.
9. Inspect the PDM network diagram and critical path.
10. Review the Gantt chart and project cost information.
11. Export or print the results if required.

---

## 📁 Project Structure

The application is intentionally lightweight.

```text
CPM-Project-Planner-Pro/
│
├── index.html
├── README.md
└── CHANGELOG.md
```

The main application is contained in `index.html`.

No installation or server-side application is required.

---

## 💻 Running Locally

Download or clone the repository.

Then open:

```text
index.html
```

in a modern web browser.

No installation is required.

---

## 🌐 GitHub Pages

The project can be hosted for free using **GitHub Pages**.

Typical configuration:

```text
Branch: main
Folder: / (root)
```

Once GitHub Pages is enabled, the application can be accessed directly through the generated GitHub Pages URL.

---

## 🛠️ Technologies

CPM Project Planner Pro is built as a lightweight browser application using:

- HTML
- CSS
- JavaScript
- SVG-based visualization
- Client-side CPM calculations

No backend server is required.

---

## 🎯 Project Goal

The goal of CPM Project Planner Pro is to make project scheduling and network analysis easier to understand and visualize.

It is particularly useful for:

- Project Management students
- Construction Management students
- Civil Engineering students
- Scheduling practice
- CPM exercises
- PDM network visualization
- Small project schedule analysis

---

## ⚠️ Disclaimer

CPM Project Planner Pro is intended primarily as an **educational and planning tool**.

Users should independently verify schedule calculations before relying on the application for professional, contractual, financial, or construction-management decisions.

---

## 📝 Changelog

See [`CHANGELOG.md`](CHANGELOG.md) for project updates, improvements, and bug fixes.

---

## 🤝 Contributions

Suggestions, bug reports, and improvements are welcome.
If you find an issue, feel free to open a GitHub Issue describing:

- What happened
- What you expected
- The project data or CSV that caused the issue
- A screenshot, if applicable

---

## ⭐ Support the Project

If you find **CPM Project Planner Pro** useful, consider giving the repository a ⭐ on GitHub.

It helps others discover the project.

---

## 👨‍💻 Author

**Musad Saiyed**


### CPM Project Planner Pro

**Plan. Calculate. Visualize. Understand.**
