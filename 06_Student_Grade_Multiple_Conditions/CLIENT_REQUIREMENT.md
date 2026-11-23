# Client Requirement Specification
## Project 06: Student Grade & Performance Evaluator (Multiple Conditions)
**Client**: Academic Evaluation & Certification Board  
**Requirement ID**: REQ-RPA-006  
**Target Environment**: UiPath Studio (Windows / VB.NET)  

### 1. Executive Summary
The Examination Board requires a multi-tiered conditional grading robot to evaluate numeric scores and categorize students into letter grades using clean `If - Else If` routing.

### 2. Functional Requirements
- **FR-01**: Prompt user for percentage/marks via `Input Dialog` (0-100).
- **FR-02**: Parse input to `int_Marks` (`Int32`).
- **FR-03**: Evaluate grading logic:
  - If `int_Marks >= 90` -> `str_Grade = "Grade A (Outstanding!)"`
  - Else If `int_Marks >= 75` -> `str_Grade = "Grade B (Very Good)"`
  - Else If `int_Marks >= 50` -> `str_Grade = "Grade C (Pass)"`
  - Else -> `str_Grade = "Needs Improvement (Fail)"`
- **FR-04**: Present final report via `Message Box` and log trace.

### 3. Acceptance Criteria
- Boundary conditions (90, 75, 50) assign correct respective grades.
