QA Test Documentation Breach Web Application

General Overview
This QA documentation covers the homepage, sign-up (Join Breach), login, dashboard, interest selection, and responsiveness of the Breach platform, tested through exploratory methods in the absence of a PRD. 

This includes:
    Exploratory UI testing across different flows and screen sizes
    API and WebSocket checks via Postman
    Load/performance testing
    Screen recordings of sessions

Homepage: Features Verified
    Logo –                             clickable, redirects to homepage ✅
    "Join Breach" & "Login":           clickable, navigate to sign-up/login ✅
    Robot animation and headline:       visible ✅
    Filters: "Featured", "Popular", "Recent":  clickable but no contents do not reflect actual dates❌
    Categories (Humour, Art, Crypto, Tech, Sport etc ):  visible but not clickable ❌
    "Back to Top" :  functional ✅

Footer items:
    Links: Support email, About, Terms, Privacy – not navigating ❌

Logout button appears on homepage after successful login/signup ✅

UI Discrepancies
    Filters (Featured, Popular, Recent):  Inconsistency between Figma and UI  ❌
    Stream dates/content differ from Figma ❌
    "General" category shows more content in Figma than in UI ❌


Join Breach (Sign-Up): Flow
    Triggered from "Join Breach" ✅
    Logo and back arrow navigable ✅
    Fields: Email, Password – functional ✅
    Continue button ✅
    Links: Terms & Privacy – not navigating ❌
    "Already have an account?" – clickable ✅
    Success screen → "Let's Begin" → navigates to Interests ✅
    Interest Selection Flow
    Heading: "What are your interests?" ✅
    UI: 26 interests
    Figma: 24 interests ❌
    Buttons: "Next" and "Skip for later" ✅
Behavior
    If interests selected → homepage filters populate ✅
    If skipped → homepage filters show no content ❌


Login Flow
    Fields: Email, Password ✅
    Continue button ✅
    "Don't have an account?" – navigates to sign-up ✅
    Logo and back arrow navigable ✅


Dashboard Features
    Logo, Streams section, Hero image ✅
    Side menu: Start Writing, Home, Dashboard, Publications visible ✅
    Editor; Start Writing : not clickable ❌
    Stream dates/topics mismatch Figma ❌


Responsive Design Testing
Tested across Mobile (375x667), Tablet (768x1024), Laptop (1366x768), and Desktop (1920x1080) using Chrome and Firefox DevTools.
Screen Size                         Page                                Result
1920x1080                           All pages                           All layouts render correctly ✅
1366x768                            Dashboard                           Side nav and content aligned ✅
768x1024                            Interest Page                       Interest grid responsive ✅
375x667                             Login/Signup                        Forms accessible, no overflow ✅
375x667                             Homepage                            Filters visible & usable ✅

API & WebSocket Testing
    API endpoints tested using Postman ✅
    Endpoints: Almost all don't return expected result and status code ❌

Websocket
    WebSocket connection using Postman WebSocket and Browser Websocket API failed ❌
    WebSocket URL: `wss://breach-api-ws.qa.mvm-tech.xyz`
- Test Goal: Verify real-time communication functionality.
- Current Status: Not reachable; server returned `ENOTFOUND`.
- Next Step: Awaiting confirmation on server status or internal access requirement


Load Testing
    Performed basic load test using browser Jmeter:
    All 100 requests failed with the following error:❌
    Users Simulated: 10 users, 100 users
    Non HTTP response code: java.net.UnknownHostException
    Non HTTP response message: breach-api.qa.mvm-tech.xyz


Video Evidence
    Recorded screen sessions covering:
    Signup, Login, Interest, Homepage flows
    Responsiveness checks (Mobile, Tablet, Laptop)
    API and WebSocket tests in Postman
    Category and filter content exploration
    Available via shared drive link on Readme ✅

Summary of Key Issues
    Filters and category content do not align with Figma ❌
    Terms, Privacy, Footer links not working ❌
    Stream section not showing expected topics ❌
    UI interest count differs from Figma ❌
    Date metadata static or incorrect ❌

Recommendations
1. Fix Terms/Privacy/Footer navigation
2. Sync homepage filters and categories with design
3. Match content population logic with Figma expectations
4. Fix interest count mismatch
5. Improve dynamic timestamping logic
6. If the endpoint becomes reachable again, I can rerun the test and capture proper response times and throughput.
7. Confirm if the WebSocket server is live and publicly accessible, or if VPN or internal environment access is required.
8. Status: Testing completed and documented as per instruction.








