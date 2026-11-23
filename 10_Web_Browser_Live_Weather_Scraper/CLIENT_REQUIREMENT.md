# Client Requirement Specification
## Project 10: First Web Browser Bot (Google Live Temperature Scraper)
**Client**: Supply Chain & Logistics Telemetry  
**Requirement ID**: REQ-RPA-010  
**Target Environment**: UiPath Studio (Windows / Modern UI Automation)  

### 1. Executive Summary
The Fleet Routing unit requires an automated web bot to launch a web browser, execute live meteorological queries on Google Search, extract live regional temperature metrics, and display parsed telemetry.

### 2. Functional Requirements
- **FR-01**: Initialize search term variable: `cityName = "Mumbai"` (or via dynamic input dialog).
- **FR-02**: Target web browser container navigation to `https://www.google.com`.
- **FR-03**: Inject query: `"temperature in " + cityName` using `Type Into` followed by Enter key.
- **FR-04**: Extract temperature reading from Google weather result snippet using `Get Text` into `extractedTemp` (`String`).
- **FR-05**: Display result via `Message Box`: `"Live Weather Report for " + cityName + ": " + extractedTemp`.

### 3. Acceptance Criteria
- Web browser attaches correctly, executes search, and retrieves text without element timeout.
