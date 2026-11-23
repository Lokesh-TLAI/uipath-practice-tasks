# Client Requirement Specification
## Project 05: Notepad Desktop Automation
**Client**: Enterprise IT Administration  
**Requirement ID**: REQ-RPA-005  
**Target Environment**: UiPath Studio (Windows / VB.NET)  

### 1. Executive Summary
The IT Admin team requires an automated desktop robot to launch Windows Notepad, type dynamic system verification text, and demonstrate attended desktop automation capabilities.

### 2. Functional Requirements
- **FR-01**: Initialize attended desktop context targeting `notepad.exe`.
- **FR-02**: Use `Use Application/Browser` (or `Open Application`) to bring Notepad to foreground.
- **FR-03**: Execute `Type Into` activity targeting the main text editing area with content:
  `"Mera pehla UiPath automation successful raha! Timestamp: " + Now.ToString("dd-MM-yyyy HH:mm:ss")`.
- **FR-04**: Write success audit message to Output panel.

### 3. Acceptance Criteria
- Notepad opens reliably and types text with simulated or hardware keys.
