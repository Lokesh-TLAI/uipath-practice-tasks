# Client Requirement Specification
## Project 02: User Intake & Welcome Greeting
**Client**: Global Human Resources Inc.  
**Requirement ID**: REQ-RPA-002  
**Target Environment**: UiPath Studio (Windows / VB.NET)  

### 1. Executive Summary
The HR onboarding department requires an interactive bot to capture dynamic employee names during unattended or attended initiation and present an authenticated greeting.

### 2. Functional Requirements
- **FR-01**: Prompt user via `Input Dialog` with Title `"Enter Name"` and Label `"Aapka naam kya hai?"`.
- **FR-02**: Store user input into variable `strName` (`String`).
- **FR-03**: Validate non-empty entry and construct greeting string: `"Hello " + strName + ", UiPath me aapka swagat hai!"`.
- **FR-04**: Display personalized welcome card in `Message Box` and log trace in `Write Line`.

### 3. Acceptance Criteria
- User input correctly passes into variable.
- Message Box displays the full customized greeting without truncation.
