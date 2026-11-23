# Client Requirement Specification
## Project 04: Even / Odd Number Conditional Classifier
**Client**: Logistics Parcel Sorting Services  
**Requirement ID**: REQ-RPA-004  
**Target Environment**: UiPath Studio (Windows / VB.NET)  

### 1. Executive Summary
The sorting facility requires an algorithmic routing bot to classify transaction numbers and parcel IDs into Odd and Even batches using conditional branching.

### 2. Functional Requirements
- **FR-01**: Capture numeric input from operator via `Input Dialog` (`intNum` as `Int32`).
- **FR-02**: Evaluate modulo parity condition: `intNum Mod 2 = 0`.
- **FR-03**: If True, branch to Then sequence: Output `"Even Number hai!"`.
- **FR-04**: If False, branch to Else sequence: Output `"Odd Number hai!"`.
- **FR-05**: Log decision to Output panel and notify via Message Box.

### 3. Acceptance Criteria
- Numbers divisible by 2 route to Even branch.
- Numbers not divisible by 2 route to Odd branch.
