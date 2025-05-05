MVMTEST PLAN

TESTER: EUPHEMIA NNAEMEKA

29th APRIL, 2025




Table of Contents
1.0 Introduction
1. Scope
2. Objectives
3. Test Items
4. Test Types
5. Test Environment
6. Test Strategy
7. Tools Used
8. Deliverables
9. Risks and Assumptions
10. Timeline


Introduction
This test plan outlines the QA strategy for exploratory, functional, API, and performance testing of the Breach Platform web application. The testing covers both the frontend (UI/UX) and backend (APIs, WebSocket) components, as well as load testing and cross-browser compatibility checks, as part of the MVM QA Engineer take-home assignment.

Scope
In Scope
    Exploratory testing of all frontend flows
    API validation using Swagger documentation and Postman
    WebSocket testing using Postman 
    Functional UI testing on different screen sizes and browsers
    Load/performance testing of key APIs
    Bug documentation and visual evidence collection (screenshots, videos)

Out of Scope
Mobile app testing
Deep security testing (e.g., penetration testing)
Automation testing (not required in this task)

Objectives
    Discover functional, UI, and API-level defects through exploratory testing
    Ensure all major frontend flows work as expected
    Verify backend endpoints respond correctly with proper status codes and payloads
    Check system behavior under load
    Test WebSocket events and message flow
    Identify and track all bugs with detailed documentation

Test Items
Area                Details
UI                  Homepage, Interests Page, Sign-Up, Post Editor
APIs                Auth, Interests, Posts (Swagger-based)
WebSocket           Real-time messaging & updates
Performance         Load testing APIs using JMeter
Design Validation   Compare UI with Figma reference
Multi-Device        Chrome DevTools simulation + real device checks


Test Types
Type                    Description
Functional Testing      Validate core user flows, navigation, form actions
Exploratory Testing     Identify unknown risks via unscripted exploration
UI/UX Testing           Match against Figma, check alignment, visual consistency
API Testing             Use Postman to test endpoints for GET, POST, PUT, DELETE
WebSocket Testing       Connect via WebSocket tool / Postman to verify event emissions
Load Testing            Simulate concurrent users 10 and 100 on selected endpoints and document system behavior
Cross-browser Testing   Validate layout and functionality across Chrome, Firefox, and Edge

Test Environment
Item            Configuration
Platform        Web
Browsers:       Chrome, Firefox,
Devices:        Laptop (Windows 10), Android device (mobile view)
API Docs
Swagger link    provided
WebSocket URL:  Provided by team
Tools:          Postman, jmeter, Chrome DevTools, Loom, Google Sheets

Test Strategy
Manual UI Testing
Compare all pages against Figma.

Check responsiveness using Chrome DevTools.
Validate footer links, header buttons, post cards, etc.
Attempt negative scenarios like submitting empty forms.


API Testing
Import Swagger into Postman.
Test each endpoint with correct and incorrect payloads.
Validate status codes, response time, schema, and headers.


WebSocket Testing
Connect via Postman or WebSocket client.
Trigger frontend actions and verify real-time updates.
Send messages and assert server responses.


Load Testing
Identify frequently used endpoints (e.g., /posts, /auth).

Simulate 10–100 virtual users using jmeter

Log response times, errors, and threshold breaches.


Bug Tracking
All bugs tracked in Google Sheets/docs (with ID, title, steps, severity).

Supporting evidence includes Loom recordings and screenshots.

Tools Used
Tool                        Purpose
Postman                     API and WebSocket Testing
Loom                        Screen Recording
Google Sheets               Bug Tracking
Chrome DevTools             Responsive Testing
Swagger                     API Documentation Reference
Jmeer                       Load Testing
GitHub                      Repository and README hosting

Deliverables
Test Plan (test-plan.md)
Test Documentation (test-documentation.md)
Bug Tracker (Google Sheets)
Bug Report (Screenshots, Loom Videos)
Load Test Results
Public GitHub Repository with:
    Test Plan
    Documentation
    README with all necessary links


Risks and Assumptions
Risks
    Incomplete documentation (no PRD or user stories)
    WebSocket behavior may be unclear due to limited spec

Assumptions
    Swagger represents live API structure
    WebSocket events are active and emit data during user interactions
    All UI elements are linked to functional features


Timeline
Task                        Timeframe   Date
Exploratory Testing         3  Day      April 29-2nd May, 2025
API + WebSocket Testing     2 Day       May 3-4, 2025
Load Testing                Half Day    May 5, 2025

Final Submission                        May 5, 2025


