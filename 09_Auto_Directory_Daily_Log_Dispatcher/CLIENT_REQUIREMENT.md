# Client Requirement Specification
## Project 09: Auto Directory & Daily Log File Creator
**Client**: Enterprise Security & Audit Compliance  
**Requirement ID**: REQ-RPA-009  
**Target Environment**: UiPath Studio (Windows / VB.NET)  

### 1. Executive Summary
The Audit & Compliance department requires an automated routine to ensure operational audit folders exist on the local workstation, provisioning them dynamically if missing, and logging timestamped process telemetry to a daily formatted text file.

### 2. Functional Requirements
- **FR-01**: Define base directory variable: `folderPath = "C:\Users\hp5cg\Desktop\RPA_Daily_Logs"`.
- **FR-02**: Compute dynamic daily log file path: `fileName = folderPath + "\Log_" + Now.ToString("dd-MM-yyyy") + ".txt"`.
- **FR-03**: Check directory existence via `Folder Exists` activity into `isFolderExist` (`Boolean`).
- **FR-04**: If folder is missing (`isFolderExist = False`), invoke `Create Folder` to provision directory.
- **FR-05**: Invoke `Write Text File` with header, timestamp, and status report.
- **FR-06**: Notify completion via `Message Box` and console log.

### 3. Acceptance Criteria
- Folder and log file created idempotently without file access collisions.
