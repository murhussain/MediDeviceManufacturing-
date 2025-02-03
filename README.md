# Medical Device Manufacturing App - Screen Specifications

## Overview
This document outlines the first six screens of our medical device manufacturing application for blood tubing sets. The app is designed to guide operators through the complete manufacturing process while ensuring GMP compliance and quality control.

## 1. Production Order Selection Screen
### Purpose
- Initial screen where operators select a production order (PO) to begin the manufacturing process
- Only displays POs with status "In Production" or "Waiting"

### Key Features
- Filterable list of production orders
- Display fields:
  - PO Number
  - Status (color-coded)
  - Product type
  - Quantity
  - Start date
- Status indicators:
  - Waiting (yellow)
  - In Production (blue)
- Search functionality by PO number
- Status filter dropdown

### Business Rules
- Only POs with status "In Production" or "Waiting" should be selectable
- If PO status is "In Production", operator should be returned to where they left off
- Each PO must display its current status clearly with color coding

## 2. Equipment Selection Screen
### Purpose
- Allow operators to select and verify required equipment for the assembly process
- Ensure all equipment is properly sterilized and available

### Key Features
Three main equipment categories:
1. Clothing
   - Clean room suits
   - Status tracking
   - Sterilization options
2. Gloves
   - Sterile gloves selection
   - Status verification
3. Testing Equipment
   - Pressure leak tester selection
   - Calibration status

### Equipment Status Types
- Allocated
- Deallocated
- Sterilized
- Not sterilized

### Business Rules
- Only sterilized and deallocated equipment can be selected
- Equipment status must be clearly indicated with color coding
- Option to sterilize equipment if needed
- Option to deallocate equipment if currently allocated
- Equipment selection must match requirements for blood tubing set assembly

## 3. Workstation Selection Screen
### Purpose
- Enable operators to select an appropriate assembly workstation
- Manage workstation cleanliness and allocation status

### Key Features
- Visual layout of available workstations
- Status indicators for each workstation:
  - Available (green)
  - In Use (yellow)
  - Needs Sterilization (red)
- Workstation details:
  - Station ID
  - Current status
  - Last cleaning time
  - Current operator (if allocated)

### Business Rules
- Only display workstations designated for assembly
- Workstation status types:
  - Allocated
  - Deallocated
  - Sterilized
  - Not sterilized
- Option to clean and deallocate workstations
- Cannot select stations that are:
  - Currently allocated
  - Not sterilized
  - In need of cleaning

## 4. Equipment and Workstation Overview Screen
### Purpose
- Provide a final verification step before beginning manufacturing
- Collect digital signature for process initiation

### Key Features
- Summary of selected equipment:
  - Clean room suit details
  - Gloves information
  - Testing equipment status
- Workstation details:
  - Station number
  - Cleanliness status
  - Tool verification
- Pre-start checklist:
  - Equipment sterilization verification
  - Workstation preparation confirmation
  - Safety procedure review
- Digital signature field

### Business Rules
- All equipment must be verified as sterilized
- Workstation must be confirmed as properly prepared
- Digital signature required to proceed
- All checklist items must be completed
- Cannot proceed without valid signature

## 5. Material Preparation Screen
### Purpose
- Guide operators through material gathering and verification
- Track material usage and batch numbers

### Key Features
- Material requirements list:
  - Tubing materials
  - Roller clamps
  - Required quantities
- Batch number verification
- Quantity tracking
- Barcode scanning capability
- Material verification checklist

### Business Rules
- All materials must be scanned or manually entered
- Batch numbers must be recorded
- Quantities must match production order requirements
- Option to report deviations:
  - Minor deviations
  - Major deviations
  - Critical deviations
- Must log manufacturing start date

## 6. Sub-Assembly Process Screen
### Purpose
- Guide operators through the sub-assembly of tubing and roller clamp
- Ensure quality checks during assembly

### Key Features
- Step-by-step assembly instructions
- Visual guides and diagrams
- Process controls:
  - Start/pause functionality
  - Time tracking
  - Units completed counter
- Quality verification checklist
- Digital signature requirement

### Business Rules
- Cannot proceed without completing each step
- Digital signature required for process verification
- Must follow precise assembly sequence
- Quality checks required at specified steps
- Option to report deviations during process
- Time tracking for each unit produced

## General Requirements
- All screens must maintain GMP compliance
- Consistent color coding for status indicators
- Clear navigation between screens
- Option to report deviations at any point
- Digital signatures required for critical steps
- All actions must be logged for traceability

## Implementation Notes
- Build using Tulip's no-code platform
- Utilize built-in GxP requirements
- Implement proper data collection at each step
- Ensure proper error handling
- Maintain consistent UI/UX across all screens
