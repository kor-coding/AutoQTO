How to use
==========
1. Capture the UI matching "Capture this" for the slot you want.
2. Save the image into public/screenshots/ with the EXACT filename listed below.
3. Run npm run dev or npm run build. If auto-wire works, the image appears with no guides.ts edit.
   Otherwise set src: '/screenshots/<filename>' on that slot in src/data/guides.ts (or on
   ScreenshotPlaceholder in src/pages/index.astro for landing).

Drop the file with the exact name → rebuild → it appears. No need to edit guides.ts unless you want custom paths.

Slots: 64 (61 guide + 3 landing).
Filenames use the stable file field on each screenshot slot — do NOT renumber remaining
files when slots are removed (e.g. guide-pan-and-zoom-3.png stays -3 even if -1/-2 are gone).

Naming
======
- Guides: guide-<slug>-<n>.png  (n from stable file field, not array index; gaps OK)
- Landing: hero-main-window.png, landing-detection-overlay.png, landing-quantity-dock.png

Alt text must describe what is shown (for screen readers), not the filename.
Caption is the short visible label under the figure.

Landing / hero
--------------

  hero-main-window.png
    Page:        /
    Caption:     Main window: PDF viewer + quantity dock
    Capture this: Main application window showing the PDF drawing viewer beside the Quantity Take-Off dock.

  landing-detection-overlay.png
    Page:        /
    Caption:     Detection overlay on plan
    Capture this: Floor plan with room detection overlays and wall centerlines on the drawing canvas.

  landing-quantity-dock.png
    Page:        /
    Caption:     Quantity dock with formulas
    Capture this: Quantity Take-Off dock listing rooms and centerlines with formula columns.

Guides
------

### Workflow (workflow)

  Guide: How a takeoff usually runs
  URL:   /guides/typical-takeoff-flow

    guide-typical-takeoff-flow-1.png
      Caption:      Typical toolbar after Open PDF
      Capture this: Application toolbar after opening a PDF, showing Save PDF, page controls, and Switch to CAD.

    guide-typical-takeoff-flow-2.png
      Caption:      Rooms and centerlines on a floor plan
      Capture this: Floor plan with translucent room polygons and orange and blue wall centerlines overlaid.

    guide-typical-takeoff-flow-3.png
      Caption:      Quantity Take-Off dock with schedule rows
      Capture this: Quantity Take-Off dock listing schedule rows for detected rooms and centerlines.

### Document & view (document-view)

  Guide: Open PDF
  URL:   /guides/open-pdf

    guide-open-pdf-1.png
      Caption:      Open PDF dialogue
      Capture this: Open PDF file dialogue for choosing a vector PDF drawing.

    guide-open-pdf-2.png
      Caption:      Page 1 loaded in PDF view
      Capture this: Page 1 of a drawing shown in the fast PDF view for pan and zoom preview.

    guide-open-pdf-3.png
      Caption:      Toolbar with Save PDF and Switch to CAD enabled
      Capture this: Toolbar with Save PDF, page buttons, and Switch to CAD enabled after opening a PDF.

  Guide: Prev / Next Page
  URL:   /guides/prev-next-page

    guide-prev-next-page-1.png
      Caption:      Page controls on the toolbar
      Capture this: Toolbar page controls for Prev Page and Next Page.

    guide-prev-next-page-2.png
      Caption:      New sheet after Next Page
      Capture this: New drawing sheet displayed after using Next Page.

    guide-prev-next-page-3.png
      Caption:      Empty overlays ready for re-identify
      Capture this: Canvas with empty overlays after a page change, ready for re-identify.

  Guide: PDF view vs Switch to CAD
  URL:   /guides/pdf-view-vs-cad

    guide-pdf-view-vs-cad-1.png
      Caption:      Same sheet in PDF view
      Capture this: Drawing sheet shown in PDF view before switching to CAD.

    guide-pdf-view-vs-cad-2.png
      Caption:      After Switch to CAD with tiled underlay
      Capture this: Same sheet after Switch to CAD, showing a tiled underlay ready for analysis.

    guide-pdf-view-vs-cad-3.png
      Caption:      Waiting panel during CAD switch
      Capture this: Waiting panel displayed while Switch to CAD extracts vectors.

  Guide: Pan and zoom
  URL:   /guides/pan-and-zoom

    guide-pan-and-zoom-3.png
      Caption:      View framed after clicking a dock row
      Capture this: View zoomed to frame a room after clicking its row in the Quantity dock.

  Guide: Ruler
  URL:   /guides/ruler

    guide-ruler-1.png
      Caption:      Ruler tool active
      Capture this: Ruler tool active on the toolbar ready for a two-point measure.

    guide-ruler-3.png
      Caption:      Distance readout in current unit
      Capture this: Ruler distance readout shown in the current calibrated unit.

  Guide: Calibrate Scale
  URL:   /guides/calibrate-scale

    guide-calibrate-scale-1.png
      Caption:      Calibrate Scale two-point pick
      Capture this: Calibrate Scale mode with two points picked on a known length.

    guide-calibrate-scale-2.png
      Caption:      Enter distance and unit
      Capture this: Dialogue to enter the real distance and unit for Calibrate Scale.

  Guide: Find Grid Extents + confirm scale
  URL:   /guides/find-grid-extents

    guide-find-grid-extents-1.png
      Caption:      Green dashed grid extent boxes
      Capture this: Green dashed boxes highlighting grid extent clusters on the plan.

    guide-find-grid-extents-2.png
      Caption:      Confirm Grid Dimension Scale panel
      Capture this: Confirm Grid Dimension Scale panel with candidate dimensions to accept or skip.

    guide-find-grid-extents-3.png
      Caption:      Blue box and gold ticks on a dimension
      Capture this: Blue selection box with gold ticks marking a grid dimension candidate.

  Guide: Reopen previously measured PDF
  URL:   /guides/reopen-measured-pdf

    guide-reopen-measured-pdf-1.png
      Caption:      Open PDF choosing a previously saved file
      Capture this: Open PDF dialogue selecting a previously measured PDF with session data.

    guide-reopen-measured-pdf-2.png
      Caption:      Restored rooms after Switch to CAD
      Capture this: Restored room overlays after Switch to CAD on a previously saved PDF.

    guide-reopen-measured-pdf-3.png
      Caption:      Edit Areas continuing on restored polygons
      Capture this: Edit Areas mode continuing edits on restored room polygons.

### Takeoff geometry (takeoff-geometry)

  Guide: Hide Drawings
  URL:   /guides/hide-drawings

    guide-hide-drawings-1.png
      Caption:      Hide Drawings floating panel
      Capture this: Floating Hide Drawings panel with colour and random hide modes.

    guide-hide-drawings-2.png
      Caption:      Colour-hide removing dimension ticks
      Capture this: Plan after colour-hide removed dimension tick strokes.

    guide-hide-drawings-3.png
      Caption:      Shift+drag box-select hide
      Capture this: Shift+drag box selection hiding multiple strokes at once.

  Guide: Identify Rooms
  URL:   /guides/identify-rooms

    guide-identify-rooms-1.png
      Caption:      Identify Rooms running with red door bypasses
      Capture this: Identify Rooms in progress with red dashed door-opening bypasses.

    guide-identify-rooms-2.png
      Caption:      Translucent room polygons and labels
      Capture this: Translucent room polygons with labels after Identify Rooms completes.

    guide-identify-rooms-3.png
      Caption:      Detected Rooms group in the Quantity dock
      Capture this: Detected Rooms group listing room areas in the Quantity Take-Off dock.

  Guide: Generate Centerlines
  URL:   /guides/generate-centerlines

    guide-generate-centerlines-1.png
      Caption:      Generate Centerlines gap dialog
      Capture this: Generate Centerlines dialogue for setting smallest and largest wall gap in millimetres.

    guide-generate-centerlines-2.png
      Caption:      Orange internal and blue external centerlines
      Capture this: Floor plan showing orange dashed internal and blue external wall centerlines.

    guide-generate-centerlines-3.png
      Caption:      Centerlines group in the Quantity dock
      Capture this: Centerlines group with length rows in the Quantity Take-Off dock.

  Guide: Rooms Offset
  URL:   /guides/rooms-offset

    guide-rooms-offset-1.png
      Caption:      Rooms Offset live three-room demo
      Capture this: Rooms Offset live three-room demo illustrating the selected area mode.

    guide-rooms-offset-2.png
      Caption:      GFA mode on a floor plate
      Capture this: GFA offset mode applied to a floor plate with shared walls to centerline.

    guide-rooms-offset-3.png
      Caption:      Status: internal vs external edges matched
      Capture this: Rooms Offset status reporting how many internal versus external edges matched.

  Guide: Edit Areas
  URL:   /guides/edit-areas

    guide-edit-areas-1.png
      Caption:      Edit Areas second toolbar
      Capture this: Edit Areas second toolbar with select, draw, split, merge, and offset tools.

    guide-edit-areas-2.png
      Caption:      Dragging a vertex with snaps
      Capture this: Dragging a polygon vertex with snap points visible in Edit Areas.

    guide-edit-areas-3.png
      Caption:      Split and merge on adjacent rooms
      Capture this: Split and merge operations applied to adjacent room polygons.

  Guide: Clear Overlay
  URL:   /guides/clear-overlay

    guide-clear-overlay-1.png
      Caption:      Overlays visible on plan
      Capture this: Coloured room and centerline overlays visible on the plan canvas.

    guide-clear-overlay-2.png
      Caption:      Canvas after Clear Overlay
      Capture this: Plan canvas after Clear Overlay removed coloured overlays.

### Quantities & export (quantities-export)

  Guide: Quantity Take-Off dock
  URL:   /guides/quantity-takeoff-dock

    guide-quantity-takeoff-dock-1.png
      Caption:      Quantity Take-Off dock on the right
      Capture this: Quantity Take-Off dock docked on the right with room and centerline rows.

    guide-quantity-takeoff-dock-2.png
      Caption:      Gold highlight after clicking a room row
      Capture this: Room polygon highlighted in gold after clicking its dock row.

  Guide: User columns and formulas
  URL:   /guides/user-columns-and-formulas

    guide-user-columns-and-formulas-1.png
      Caption:      Add Column dialogue
      Capture this: Add Column dialogue for creating a user-defined Quantity dock column.

    guide-user-columns-and-formulas-2.png
      Caption:      Formula cell with =@[Area]
      Capture this: Quantity dock cell showing a formula using =@[Area] syntax.

    guide-user-columns-and-formulas-3.png
      Caption:      Fill Down across a group
      Capture this: Fill Down applying a formula across rows in the same dock group.

  Guide: Export to Excel
  URL:   /guides/export-to-excel

    guide-export-to-excel-1.png
      Caption:      Export to Excel command
      Capture this: Export to Excel command highlighted in the application UI.

    guide-export-to-excel-2.png
      Caption:      Waiting panel during export
      Capture this: Waiting panel shown while Export to Excel builds the workbook.

    guide-export-to-excel-3.png
      Caption:      Resulting .xlsx in a spreadsheet app
      Capture this: Exported .xlsx workbook open in a spreadsheet application.

  Guide: Save PDF
  URL:   /guides/save-pdf

    guide-save-pdf-1.png
      Caption:      Save PDF in progress
      Capture this: Save PDF operation in progress with waiting panel.

    guide-save-pdf-2.png
      Caption:      Rooms as Area measurements in PDF XChange
      Capture this: Saved PDF open in PDF XChange showing rooms as Area measurements.

    guide-save-pdf-3.png
      Caption:      Orange/blue dashed centerline lengths on the saved page
      Capture this: Saved PDF page with orange and blue dashed centerline length annotations.

### Paid features (paid-features)

  Guide: Auto Bot
  URL:   /guides/auto-bot

    guide-auto-bot-2.png
      Caption:      Human-in-the-loop prompt during an Auto Bot run
      Capture this: Dialogue prompt appearing mid-run for human-in-the-loop input during Auto Bot.

    guide-auto-bot-3.png
      Caption:      Pause / Resume / Stop during a mid-run edit
      Capture this: Pause, Resume, and Stop controls available while editing mid Auto Bot run.

  Guide: 3D View
  URL:   /guides/3d-view

    guide-3d-view-1.png
      Caption:      Floor height prompt for 3D View
      Capture this: Prompt asking for expected floor height before opening 3D View.

    guide-3d-view-2.png
      Caption:      3D visualisation with zoom / pan / rotate
      Capture this: 3D visualisation of measurements with zoom, pan, and rotate controls.

    guide-3d-view-3.png
      Caption:      Quantity dock showing vertical area columns
      Capture this: Quantity Take-Off dock showing vertical area quantity columns from 3D View.

### Enterprise (enterprise)

  Guide: Save and load template
  URL:   /guides/save-load-template

    guide-save-load-template-1.png
      Caption:      Template button on the Quantity dock top row
      Capture this: Template button on the top row of the Quantity Take-Off dock.

    guide-save-load-template-2.png
      Caption:      Save template for user-defined headers
      Capture this: Save template option exporting user-defined column headers.

    guide-save-load-template-3.png
      Caption:      Load template on a new project
      Capture this: Load template option restoring saved column headers on a new project.

### Account (account)

  Guide: Waiting panel
  URL:   /guides/waiting-panel

    guide-waiting-panel-1.png
      Caption:      Waiting panel during Identify Rooms
      Capture this: Waiting panel displayed during Identify Rooms analysis.

    guide-waiting-panel-2.png
      Caption:      Free-user promo with Continue
      Capture this: Waiting panel free-user promo with a Continue button.

