# Changelog

All notable changes to **CPM Project Planner Pro** will be documented here.

---

## v1.0.0

### 🎯 CPM Project Planner Pro

A browser-based CPM project scheduling and network analysis tool designed for easy project planning, CPM calculations, and PDM visualization.

### ✨ Features

- Interactive project task table
- Add and delete activities
- Reset project data
- Import project data from CSV
- Export project data to CSV
- Automatic CPM calculations
- Automatic Critical Path detection
- Forward and backward pass calculations
- Calculates:
  - Early Start (ES)
  - Early Finish (EF)
  - Late Start (LS)
  - Late Finish (LF)
  - Total Float (TF)
- Automatic project duration calculation
- Project cost calculation
- PDM / Activity-on-Node network diagram
- Gantt chart
- Cumulative cost chart
- SVG export
- Print / Save as PDF report

### 🔗 Relationship Support

Supports the four major activity relationships:

- Finish-to-Start (FS)
- Start-to-Start (SS)
- Finish-to-Finish (FF)
- Start-to-Finish (SF)

Positive and negative lag values are also supported.

Examples:

`FS+2`

`SS+1`

`FF-2`

`SF+3`

If the Relationship field is blank, the application automatically assumes:

`FS with 0 lag`

### 📂 Smart CSV Import

The CSV importer automatically recognizes project scheduling data.

Supported information includes:

- Activity
- Duration
- Predecessor
- Relationship
- Lag
- Cost

Repeated activities in a CSV are automatically merged.

For example:

Activity F with predecessor C

Activity F with predecessor D

will automatically become:

Predecessors: `C, D`

If both relationships are blank, both are automatically interpreted as FS with 0 lag.

### 🧹 Cleaner Relationship Input

Predecessors and Relationships are displayed in separate columns.

Example:

Predecessors:

`C, D`

Relationships:

`SS+2, FS`

means:

- C → Activity = SS+2
- D → Activity = FS

Default FS with zero lag does not need to be entered manually.

### 📊 Improved PDM Network Diagram

The PDM network diagram includes:

- Activity name
- Duration
- ES
- EF
- LS
- LF
- Total Float

Critical activities and critical relationships are automatically highlighted.

### 🧠 Automatic Network Untangling

The network layout automatically rearranges activity boxes to improve readability.

The application attempts to:

- Reduce crossing arrows
- Reduce unnecessarily long relationship lines
- Keep related activities near each other
- Prevent arrows from passing through unrelated activity boxes
- Keep incoming relationships visually separate
- Keep outgoing relationships visually separate

Activity logic is never changed when rearranging the diagram.

Only the visual position of activities is adjusted.

### ➡️ Improved Arrow Routing

Relationship arrows now:

- Use cleaner 90-degree routing
- Connect directly to activity boxes
- Have visible arrowheads
- Keep separate predecessor relationships visually independent
- Keep separate successor relationships visually independent
- Route around intermediate activity boxes where possible

This helps prevent the diagram from visually suggesting relationships that do not exist.

### 🟢 START and END Logic

START and END boxes are created only when necessary.

- One starting activity → No START box
- Multiple starting activities → START box is shown
- One terminal activity → No END box
- Multiple terminal activities → END box is shown

This keeps simple networks cleaner.

### 🎲 Default Practice Project

The application starts with activities:

`A, B, C, D, E, F, G`

Durations are randomly generated.

The default network uses simple predecessor logic:

A → Start

B → A

C → A

D → B

E → C

F → D

G → E, F

All default relationships are:

`FS with 0 lag`

All default costs are:

`$0`

### 🎲 Random A–G Generator

The **Random A–G** button generates a new practice project with random durations.

This makes the application useful for practicing CPM calculations and network scheduling.

### 🔧 Fixes

- Fixed CSV import failing after network routing changes
- Fixed duplicate-looking relationship arrows
- Fixed missing arrowheads
- Fixed arrows passing through unrelated activities
- Fixed overlapping incoming relationships
- Fixed overlapping outgoing relationships
- Fixed misleading terminal activity arrows
- Fixed Add Task changing blank relationships to visible FS
- Fixed stray commas appearing in blank Relationship fields
- Fixed default FS relationships after table refresh
- Improved PDM activity positioning
- Improved START and END handling
- Improved readability of larger networks

---

## Default Relationship Rule

Throughout CPM Project Planner Pro:

> **Blank Relationship = Finish-to-Start (FS) with 0 lag**

This keeps project data entry simple while maintaining correct scheduling logic.
