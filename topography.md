## CNC Topographic Terrain Map

### Project Overview
This project is a CNC-machined wooden topographic map that represents terrain using elevation data rather than a specific real-world location. The purpose of the project was to practice converting digital terrain models into a physical object using CNC machining while focusing on accuracy, clean cuts, and overall craftsmanship.

The finished piece was carved from wood and displays elevation changes through raised and lowered surfaces, creating a clear visual representation of terrain.

---

### Photos / Videos
IMG_2418  

https://github.com/user-attachments/assets/053faa4e-982c-4b83-8be0-fb1a95b9b857

---

### CNC Topography Workflow

#### 1. Creating the Terrain Model
- Opened https://jthatch.com/Terrain2STL/
- Generated a terrain model using elevation data
- Defined the model area using the selection box
- Adjusted terrain settings:
  - Z scale to control height exaggeration
  - Water drop to separate low areas
  - Base height to add support under the terrain
- Downloaded the terrain model as an STL file

---

#### 2. CNC Job Setup in Aspire
- Created a new project in Vectric Aspire
- Set the job type to single-sided machining
- Entered stock dimensions to match the wood material
- Set zero locations:
  - Z zero at the top of the material
  - XY origin at the bottom left corner
- Imported the STL file and oriented it correctly
- Scaled the model to fit within the material thickness
- Centered the model in the workspace

---

#### 3. Model Layout Adjustments
- Increased vertical scale to improve terrain visibility
- Adjusted base thickness for strength
- Centered the model within the stock
- Created a rectangular boundary to define machining limits

---

#### 4. CNC Toolpath Creation

**Roughing Pass**
- Tool used: 1/8 inch flat end mill
- Strategy: raster or Z-level
- Boundary set to the model area
- Left material for finishing

**Finishing Pass**
- Tool used: 1/8 inch ball nose end mill
- Strategy: raster or offset
- Used to smooth surfaces and add detail

---

#### 5. Profile Cut
- Selected the boundary outline
- Tool used: 1/8 inch flat end mill
- Cut depth set to release the part from the stock
- Climb cutting enabled
- Tabs were not required

---

#### 6. Simulation and Export
- Simulated toolpaths to verify accuracy
- Checked for collisions or missed areas
- Reviewed machining time estimates
- Saved the Aspire project file
- Exported toolpaths using the Carvera ATC post processor
- Combined toolpaths into a single CNC file

---

### PCB Toolpath and Milling Workflow

#### Key Notes
- 0.8 mm flat end mill used for removing bulk material
- 0.2 mm engraving bit used for cutting traces
- Tabs were required due to clamp-based workholding

---

#### PCB Toolpath Setup in MakeraCAM
- Opened MakeraCAM and selected 3-axis machining
- Set stock dimensions:
  - Material: PCB
  - X: 127 mm
  - Y: 101 mm
  - Z: 1.7 mm
- Imported PCB design files
- Repositioned layers to the bottom left with an offset
- Created pocket toolpaths for copper traces
- Generated drilling toolpaths when needed
- Created contour toolpaths for board edges
- Added tabs to secure the board
- Previewed and exported G-code

---

### PCB Milling Process
- Connected to the milling machine
- Homed the machine
- Verified probe readings
- Loaded and previewed G-code
- Enabled automatic features
- Began milling

---

### Issue Encountered: Origin Mismatch

#### Problem
During early test runs, the machining did not start in the expected location on the material. This happened because the origin point set in the software did not match the machine zero, causing the toolpaths to shift.

---

#### Solution
- Verified the origin settings in the CAM software
- Reset the origin to match the machine setup
- Re-exported the toolpaths
- Re-zeroed the CNC machine
- Confirmed correct alignment before rerunning the job

---

### Files Included
- Aspire design file
- CNC toolpath file

---

### Lessons Learned
- Software origin and machine zero must match exactly
- Setup settings should always be checked before machining
- Small setup errors can lead to major problems

---

### Summary
This project emphasized the importance of proper setup and planning when using CNC machines. Creating a physical terrain map from digital data required careful preparation, testing, and verification. The lessons learned from this project will be applied to future CNC and fabrication work.
