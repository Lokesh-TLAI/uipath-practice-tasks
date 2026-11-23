# Client Requirement Specification
## Project 07: Secret Number Guessing Game (Do While Loop)
**Client**: EdTech Interactive Gaming Systems  
**Requirement ID**: REQ-RPA-007  
**Target Environment**: UiPath Studio (Windows / VB.NET)  

### 1. Executive Summary
The client requires an interactive gamified loop module demonstrating `Do While` iterative execution, boolean state management, and retry handling.

### 2. Functional Requirements
- **FR-01**: Initialize `secretNumber = 7` (`Int32`) and flag `isCorrect = False` (`Boolean`).
- **FR-02**: Enclose interaction in a `Do While` activity evaluating condition `isCorrect = False`.
- **FR-03**: Prompt user via `Input Dialog` for guess between 1 and 10.
- **FR-04**: If guess equals 7, set `isCorrect = True` and notify success. Else, alert incorrect and repeat.

### 3. Acceptance Criteria
- Loop persists until the correct answer is entered.
- Process exits immediately on match without infinite looping.
