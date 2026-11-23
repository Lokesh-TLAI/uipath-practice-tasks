# Client Requirement Specification
## Project 03: Dynamic Age Calculator
**Client**: Insurance Demographics Services  
**Requirement ID**: REQ-RPA-003  
**Target Environment**: UiPath Studio (Windows / VB.NET)  

### 1. Executive Summary
The policy underwriting department requires an automated routine to calculate customer age on-the-fly from birth year input using system calendar functions.

### 2. Functional Requirements
- **FR-01**: Prompt user via `Input Dialog` requesting Birth Year: `"Enter Birth Year (e.g. 2000)"`.
- **FR-02**: Store input in `strBirthYear` (`String`).
- **FR-03**: Parse input and evaluate age using expression: `Now.Year - CInt(strBirthYear)`.
- **FR-04**: Assign result to `intAge` (`Int32`).
- **FR-05**: Present calculated age in `Message Box` and write diagnostic log to Output panel.

### 3. Acceptance Criteria
- Accurate mathematical difference relative to `Now.Year`.
- Clean string conversion handling.
