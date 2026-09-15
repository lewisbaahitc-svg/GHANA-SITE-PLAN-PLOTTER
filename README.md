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


## Phone GPS field capture
The coordinate entry panel includes phone GPS capture. GET MY LOCATION reads WGS84 latitude/longitude and phone accuracy; ADD AS GHANA METRE GRID POINT converts it to Ghana Metre Grid (EPSG:25000) and saves it as the next point. Users can walk to successive locations and collect up to 100 points. Phone GPS is for preliminary positioning, not survey-grade GNSS/control.


## V20 layout and KML update
- The interface is now arranged as two focused pages: **Coordinates & Field** and **Results & Tools**, reducing visual clutter while keeping the existing features.
- Coordinate entry, CSV import/export, Plot & Compute, Load Demo, and phone GPS capture are kept together on Page 1.
- Drawing, satellite, contours, feet/metres conversion, Excel/print conversion, KML, DXF and report tools are organized on Page 2.
- KML/WGS84 conversion was corrected by using proper geocentric datum transformation calculations and correct ellipsoid eccentricity formulas for the Ghana Metre Grid and War Office workflows.
- KML contains the boundary and survey points in WGS84 with ground-clamped altitude for Google Earth.
- The tool remains a preliminary mapping/engineering aid; official cadastral work should use approved survey control and transformations.
