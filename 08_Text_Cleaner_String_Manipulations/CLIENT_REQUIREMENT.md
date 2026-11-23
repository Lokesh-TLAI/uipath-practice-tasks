# Client Requirement Specification
## Project 08: Text Cleaner & String Manipulations
**Client**: Master Data Management Group  
**Requirement ID**: REQ-RPA-008  
**Target Environment**: UiPath Studio (Windows / VB.NET)  

### 1. Executive Summary
The Data Cleansing Operations team requires an automated string manipulation robot to sanitize raw unformatted text feeds by stripping leading/trailing whitespace, normalizing character casing, and computing length metrics.

### 2. Functional Requirements
- **FR-01**: Initialize raw text variable: `rawText = "   lokesh kumar - RPA DEVELOPER   "`.
- **FR-02**: Apply string methods:
  - `cleanText = rawText.Trim` (whitespace removal)
  - `upperText = cleanText.ToUpper` (case normalization)
  - `lowerText = cleanText.ToLower` (case normalization)
  - `charCount = cleanText.Length` (character count)
- **FR-03**: Output comparative report to Output console via `Write Line`.

### 3. Acceptance Criteria
- Verified elimination of extraneous leading and trailing spaces.
