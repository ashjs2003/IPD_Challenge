# Takt Engine

Room-boundary based takt planner for the finish sequence:

`Interior Walls -> MEP -> Ceiling -> Doors -> Interior Finishes`

Run Level 1 with one room per takt zone:

```powershell
python -m src.Takt_engine.takt_planner --level "L 1" --rooms-per-zone 1
```

Run Level 1 with neighboring room grouping:

```powershell
python -m src.Takt_engine.takt_planner --level "L 1" --rooms-per-zone 2
```

Inputs:

- `outputs/room_boundaries/room_takt_zones.csv`
- latest `revit_schedules/*_Room_Boundaries.csv`, when available, for room polygons
- `outputs/takt_zones/central_bim_model.csv`
- `src/Planning_engine/ALICE_BIM_mapper/outputs/Crew.csv`
- `src/Planning_engine/ALICE_BIM_mapper/outputs/Equipment.csv`

Outputs are written to `src/Takt_engine/outputs/`, including:

- `Takt_Planner.html`
- `Takt_Report.md`
- `Takt_Schedule.csv`
- `Takt_Crew_Idle_Report.csv`
- `Takt_Element_Allocations.csv`
- `Takt_Element_Splits.csv`
