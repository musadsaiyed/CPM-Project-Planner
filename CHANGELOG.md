# Changelog

All notable changes to **CPM Project Planner Pro** will be documented in this file.

---

## [1.0.0] - Initial Public Release

### Added

- Interactive CPM project scheduling table
- Activity ID and task-name support
- Activity duration input
- Multiple predecessor support
- Finish-to-Start (FS) relationships
- Start-to-Start (SS) relationships
- Finish-to-Finish (FF) relationships
- Start-to-Finish (SF) relationships
- Positive and negative lag support
- Default FS with zero lag when relationship is blank
- Automatic forward-pass calculations
- Automatic backward-pass calculations
- Early Start (ES)
- Early Finish (EF)
- Late Start (LS)
- Late Finish (LF)
- Total Float (TF)
- Automatic project-duration calculation
- Critical activity identification
- Critical-path visualization
- PDM / Activity-on-Node network diagram
- Orthogonal relationship arrows
- Independent incoming and outgoing relationship routing
- Smart network untangling
- Conditional START milestone
- Conditional END milestone
- Gantt chart
- Project cost tracking
- Cumulative cost chart
- CSV import
- CSV export
- Smart merging of repeated activities during CSV import
- SVG diagram export
- Printable project report
- Browser PDF support
- A–G CPM practice project
- Random practice durations
- Reset functionality

### Improved

- PDM relationship routing
- Multiple predecessor visualization
- Multiple successor visualization
- Long relationship routing
- Critical-path highlighting
- Network readability
- Activity positioning
- CSV column recognition
- Relationship and lag handling
- Default FS+0 relationship behavior

### Fixed

- Unnecessary commas appearing in the Relationship column
- Blank relationships now correctly represent FS with zero lag
- Duplicate relationship arrows
- Missing network arrowheads
- Relationship lines passing through unrelated activities
- Terminal relationship routing
- Multiple-predecessor CSV import issues
- Relationship display after adding new activities
