# Client Requirement Specification
## Project 11: REST API Users Directory to SQL Server Ingestion
**Client**: Enterprise IT Systems Integration Group  
**Requirement ID**: REQ-RPA-011  
**Target Environment**: UiPath Studio (Windows / VB.NET / SQL Server)  

### 1. Executive Summary
The IT Directory Synchronization team requires an enterprise-grade automated pipeline to ingest user identity records from an external REST API (`https://jsonplaceholder.typicode.com/users`), deserialize complex JSON arrays, and perform duplicate-checked parameterized SQL insertions into Microsoft SQL Server.

### 2. Functional Requirements
- **FR-01**: Execute HTTP GET request to `https://jsonplaceholder.typicode.com/users` with timeout 15000ms.
- **FR-02**: Validate response status code equals 200 OK; throw runtime exception if failed.
- **FR-03**: Deserialize raw response body into `JArray` using `Deserialize JSON Array` activity.
- **FR-04**: Establish secure SQL Server connection using `Connect to Database` with connection string:
  `"Server=localhost\SQLEXPRESS;Database=Enterprise_Users_DB;Integrated Security=True;TrustServerCertificate=True"`.
- **FR-05**: Iterate each user token (`JToken`) in `JArray`:
  - Extract primitive fields: `id`, `name`, `username`, `email`, `phone`, `website`.
  - Extract nested tokens: `user("address")("city")`, `user("address")("zipcode")`, `user("company")("name")`.
  - Execute parameterized SQL command with duplicate check (`IF NOT EXISTS ... INSERT INTO [dbo].[ApiUsers]`).
- **FR-06**: Write audit log to Output console and disconnect cleanly.

### 3. Acceptance Criteria
- Zero SQL Injection risk via parameterized inputs (`@Id`, `@Name`, etc.).
- Idempotent execution (duplicate primary keys safely skipped).
