# Client Requirement Specification
## Project 01: Simple Calculator (Addition vs String Concatenation)
**Client**: Financial Core Services Ltd.  
**Requirement ID**: REQ-RPA-001  
**Target Environment**: UiPath Studio (Windows / VB.NET)  

### 1. Executive Summary
The client requires an automated module that clearly illustrates the distinction between arithmetic operations on Integer datatypes and textual concatenation on String datatypes.

### 2. Functional Requirements
- **FR-01**: Initialize two internal integer variables `IntA = 10` and `IntB = 5` (`Int32`).
- **FR-02**: Compute mathematical summation `(IntA + IntB)` yielding `15`.
- **FR-03**: Compute string concatenation `IntA.ToString + IntB.ToString` yielding `105`.
- **FR-04**: Compute multiplication `(IntA * IntB)` yielding `50`.
- **FR-05**: Format combined audit statement: `"Sum is: " + (IntA + IntB).ToString`.
- **FR-06**: Write results to the Output panel using `Write Line` and alert operator via `Message Box`.

### 3. Acceptance Criteria
- No type casting exceptions during execution.
- Mathematical sum and string concatenation must match expected values.
