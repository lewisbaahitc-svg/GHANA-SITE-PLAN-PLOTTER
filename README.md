# Ghana Site Plan Plotter — V15 Update

This build keeps the approved Ghana Site Plan Plotter interface and adds:

- Contour generation from user-entered point elevations (metres).
- Contours can be shown on the drawing and/or satellite map.
- Contour interval options: 0.5, 1, 2, 5, 10 m.
- Ghana Metre Grid / Leigon — EPSG:25000.
- Improved Ghana War Office and Ghana Metre Grid to WGS84 conversion for map/KML positioning using documented 3-parameter transformations.
- Existing CSV, DXF, KML, report, grid, satellite and Google Maps functions retained.

Contour lines are interpolated from the supplied spot heights. They are intended for visualization/planning and should not be treated as a survey-grade terrain model unless the elevation data and control are survey-grade.

Ghana Metre Grid reference: EPSG:25000. Ghana War Office reference: EPSG:2136. Verify the transformation/control used by the responsible survey authority before official cadastral work.


## Coordinate Converter
The public version includes a separate Feet ↔ Metres coordinate converter supporting up to 100 X/Y coordinate rows. It uses the official Gold Coast foot factor (0.304799710181509 m per foot) and does not alter the main plot until the user enters the converted values there.
