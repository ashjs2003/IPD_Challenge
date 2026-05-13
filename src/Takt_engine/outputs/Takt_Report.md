# Takt Planner Report

- Level: L 1
- Rooms per grouped zone: 2
- Task dependency: Interior Walls -> MEP -> Ceiling -> Doors -> Interior Finishes
- Final duration: 192.36 working hours
- Split planning records: 0 source elements

## Crew Idle Time

| Crew | Idle Hours | Work Hours | Utilization |
|---|---:|---:|---:|
| ceiling_crew | 89.00 | 35.00 | 28.2% |
| doors_crew | 93.00 | 42.00 | 31.1% |
| interior_finishes_crew | 13.00 | 179.36 | 93.2% |
| interior_walls_crew | 0.00 | 114.00 | 100.0% |
| mep_rough_in_crew | 43.00 | 76.00 | 63.9% |

## Productivity Rates

| Task | Planning Crew | Rate | Unit |
|---|---|---:|---|
| Interior Walls | interior_walls_crew | 1.00 | EA/crew-hour |
| MEP | mep_rough_in_crew | 1.00 | EA/crew-hour |
| Ceiling | ceiling_crew | 1.00 | EA/crew-hour |
| Doors | doors_crew | 1.00 | EA/crew-hour |
| Interior Finishes | interior_finishes_crew | 50.00 | SF/crew-hour |

## Equipment Inputs

| Equipment | Count | Cost |
|---|---:|---:|
| compactor_roller | 1 | 0 |
| concrete_pump | 1 | 0 |
| excavator | 2 | 0 |
| mobile_crane | 1 | 0 |

## Notes

- Neighboring room grouping uses shared/touching room bounding boxes when possible, then nearest centroid as a fallback.
- Elements are assigned to one takt zone using room parameters first, centroid-in-room second, and nearest room centroid as the final fallback.
- MEP quantities are counted as one assembly per assigned room and dominant direction when the MEP task uses an EA productivity unit.
- Split threshold logic is disabled; no planning cuts are created by the takt planner.