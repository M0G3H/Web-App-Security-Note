# ⚡ Web Application Entry Points — Simplified Examples + Related Vulnerabilities

A **quick reference guide** showing where and how users or systems can interact with your web app — from frontend interfaces like forms or APIs to backend mechanisms like webhooks or message queues.
Each item includes a **real-world example** and **related vulnerabilities**.

---

## 📚 Table of Contents

* [🖥️ Frontend Entry Points](#%EF%B8%8F-frontend-entry-points)
* [🧩 Additional Frontend Entry Points](#-additional-frontend-entry-points)
* [🛠️ Backend Entry Points](#-backend-entry-points)
* [⚙️ Additional Backend Entry Points](#-additional-backend-entry-points)

---

## 🖥️ Frontend Entry Points

### 1. 📝 Forms

**Example:** A login form where the user enters an email and password.
**Related Vulnerabilities:** SQL Injection, Cross-Site Scripting (XSS), CSRF, Broken Authentication

### 2. 🔗 URL Parameters

**Example:** `/products?id=123` loads product #123.
**Related Vulnerabilities:** IDOR, Parameter Tampering, Open Redirects

### 3. 🛡️ HTTP Headers

**Example:** Sending `Authorization: Bearer <token>` in API requests.
**Related Vulnerabilities:** Header Injection, Token Leakage, Missing/Weak Authentication

### 4. 🍪 Cookies

**Example:** Storing a session cookie like `session_id=abc123`.
**Related Vulnerabilities:** Session Hijacking, Cookie Theft via XSS, Insecure Cookie Flags (`HttpOnly`, `Secure`)

### 5. 💾 Local / Session Storage

**Example:** `localStorage.setItem('theme', 'dark')`.
**Related Vulnerabilities:** Sensitive Data Exposure, XSS Data Theft

### 6. 📤 File Uploads

**Example:** Uploading a profile picture in an image upload form.
**Related Vulnerabilities:** Remote Code Execution (RCE), Malware Upload, Path Traversal

### 7. 👆 User Interactions

**Example:** Clicking a “Like” button or selecting from a dropdown.
**Related Vulnerabilities:** DOM-Based XSS, Clickjacking

### 8. 🌐 WebSockets

**Example:** Real-time chat updates in a messaging app.
**Related Vulnerabilities:** Insecure WebSocket Handshakes, Data Injection, Authentication Bypass

### 9. 🔗 Third-Party Integrations

**Example:** Logging in with Google or paying with Stripe.
**Related Vulnerabilities:** OAuth Misconfiguration, Supply Chain Attacks

### 10. ⚡ AJAX / Fetch Requests

**Example:** Fetching user data without reloading the page.
**Related Vulnerabilities:** CORS Misconfigurations, Insecure API Calls

---

## 🧩 Additional Frontend Entry Points

### 1. 📱 Progressive Web App (PWA) Features

**Example:** A PWA that works offline using service workers.
**Related Vulnerabilities:** Service Worker Manipulation, Cache Poisoning

### 2. 🧩 Browser Extensions

**Example:** A password manager autofilling login fields.
**Related Vulnerabilities:** Extension Privilege Escalation, Data Leakage

### 3. 📋 Clipboard Access

**Example:** Copying a coupon code with a “Copy” button.
**Related Vulnerabilities:** Clipboard Hijacking

### 4. 🌍 Geolocation API

**Example:** Getting the user’s location for nearby restaurant results.
**Related Vulnerabilities:** Privacy Leaks, Unauthorized Location Access

### 5. 📷 Device Sensors

**Example:** Using the camera for AR features.
**Related Vulnerabilities:** Camera/Sensor Exploitation, Privacy Violations

### 6. 🔔 Push Notifications

**Example:** Receiving a new message alert in your browser.
**Related Vulnerabilities:** Notification Spoofing, Unauthorized Subscriptions

### 7. 💳 Payment Request API

**Example:** Paying with Apple Pay directly in the browser.
**Related Vulnerabilities:** Payment Spoofing, Man-in-the-Browser Attacks

### 8. 🗄️ IndexedDB

**Example:** Caching product data locally for offline browsing.
**Related Vulnerabilities:** Sensitive Data Exposure, Local Data Tampering

### 9. 🔄 Cross-Origin Resource Sharing (CORS)

**Example:** Fetching data from an external API domain.
**Related Vulnerabilities:** CORS Misconfiguration, Data Exfiltration

### 10. 📺 Iframe Embedding

**Example:** Embedding a YouTube video in a blog post.
**Related Vulnerabilities:** Clickjacking, Content Injection

### 11. 🕰️ Browser History API

**Example:** Navigating between pages in a single-page app.
**Related Vulnerabilities:** History Manipulation, Information Disclosure

### 12. 📂 Drag-and-Drop API

**Example:** Dragging a file into a drop zone to upload.
**Related Vulnerabilities:** File Injection, Path Traversal

### 13. 🎤 Speech Recognition / Synthesis

**Example:** Using voice commands to search.
**Related Vulnerabilities:** Audio Injection, Privacy Leakage

### 14. 🖼️ WebAssembly (Wasm)

**Example:** Running a fast image editor inside the browser.
**Related Vulnerabilities:** Memory Corruption, Sandbox Escape

### 15. 🔗 Third-Party Scripts

**Example:** Loading Google Analytics or ads on a website.
**Related Vulnerabilities:** Supply Chain Attacks, XSS

### 16. 🔒 Content Security Policy (CSP)

**Example:** Restricting scripts to trusted domains only.
**Related Vulnerabilities:** Misconfigured CSP, Script Injection

### 17. 🔄 Browser Storage Events

**Example:** Syncing tabs when localStorage changes.
**Related Vulnerabilities:** Sensitive Data Leakage, XSS

### 18. ⚙️ Web Workers

**Example:** Processing data in the background without freezing the UI.
**Related Vulnerabilities:** Data Leakage, Race Conditions

### 19. 📹 WebRTC

**Example:** Peer-to-peer video calling in a web app.
**Related Vulnerabilities:** Eavesdropping, Insecure Media Streams

### 20. ✉️ Custom Protocols

**Example:** Clicking `mailto:` opens your email client.
**Related Vulnerabilities:** Protocol Abuse, Phishing

---

## 🛠️ Backend Entry Points

### 1. 🌐 API Endpoints

**Example:** `/api/users` returns a list of users.
**Related Vulnerabilities:** Broken Access Control, Injections, Information Disclosure

### 2. 🔔 Webhooks

**Example:** Stripe sends a payment confirmation to `/webhook/payment`.
**Related Vulnerabilities:** Replay Attacks, Unvalidated Payloads

### 3. 📝 Server-Side Forms

**Example:** Submitting a contact form processed by the backend.
**Related Vulnerabilities:** SQL Injection, XSS, CSRF

### 4. 🗄️ Database Queries

**Example:** Running `SELECT * FROM users` on login.
**Related Vulnerabilities:** SQL Injection, Data Leakage

### 5. 💻 Command-Line Interfaces (CLI)

**Example:** Running `python manage.py migrate` to update the database.
**Related Vulnerabilities:** Unauthorized Access, Privilege Escalation

### 6. 📥 Message Queues

**Example:** Sending tasks to a background worker using RabbitMQ.
**Related Vulnerabilities:** Message Injection, Unauthorized Access

### 7. 🖥️ Server-Side Rendering (SSR)

**Example:** Next.js renders a dynamic HTML page on the server.
**Related Vulnerabilities:** Template Injection, XSS

### 8. 🔐 Authentication Mechanisms

**Example:** Validating tokens at `/auth/login`.
**Related Vulnerabilities:** Broken Authentication, Token Replay

### 9. 📂 File System Access

**Example:** Serving images from a `/uploads` directory.
**Related Vulnerabilities:** Path Traversal, Unauthorized File Access

### 10. 🔗 Third-Party API Calls

**Example:** Fetching weather data from an external API.
**Related Vulnerabilities:** Supply Chain Attacks, Data Leakage

### 11. 🌐 WebSocket Connections

**Example:** Real-time notifications sent from the server.
**Related Vulnerabilities:** Insecure Authentication, Data Injection

### 12. ⚙️ Middleware

**Example:** Logging every incoming request in Express.js.
**Related Vulnerabilities:** Information Disclosure, Misconfiguration

### 13. 🔒 Server Configuration

**Example:** Reading secrets from `.env` files.
**Related Vulnerabilities:** Secret Leakage, Misconfiguration

---

## ⚙️ Additional Backend Entry Points

### 1. 📊 GraphQL Subscriptions

**Example:** Real-time stock updates using GraphQL over WebSockets.
**Related Vulnerabilities:** Injection, Broken Access Control

### 2. ☁️ Serverless Functions

**Example:** AWS Lambda function triggered on file upload.
**Related Vulnerabilities:** Insecure Triggers, Privilege Escalation

### 3. 🌍 Edge Computing

**Example:** Cloudflare Worker caching assets closer to users.
**Related Vulnerabilities:** Cache Poisoning, Misconfigured Logic

### 4. 🗄️ Database Triggers

**Example:** Automatically updating `updated_at` when a record changes.
**Related Vulnerabilities:** Privilege Escalation, Logic Abuse

### 5. 📨 Event-Driven Architecture

**Example:** Publishing an event when a new user registers.
**Related Vulnerabilities:** Event Injection, Unauthorized Event Trigger

### 6. 🕰️ Batch Processing

**Example:** Running nightly data cleanup jobs.
**Related Vulnerabilities:** Data Leakage, Job Manipulation

### 7. 🛠️ Admin Panels

**Example:** Django Admin dashboard for managing users.
**Related Vulnerabilities:** Broken Access Control, Default Credentials

### 8. 💓 Health Checks

**Example:** `/health` endpoint returns “OK” if the server is running.
**Related Vulnerabilities:** Information Disclosure

### 9. ⏱️ Rate Limiting Endpoints

**Example:** `/rate-limit` checks how many API calls remain.
**Related Vulnerabilities:** Bypass Rate Limits, DoS

### 10. 📤 Data Import / Export

**Example:** Uploading a CSV file to bulk-create users.
**Related Vulnerabilities:** CSV Injection, Unauthorized Access

### 11. 🌐 WebSocket Gateways

**Example:** Managing multiple WebSocket clients.
**Related Vulnerabilities:** Insecure Authentication, Data Injection

### 12. ⚡ Server-Side Caching

**Example:** Using Redis to store frequently accessed data.
**Related Vulnerabilities:** Cache Poisoning, Data Leakage

### 13. 🔄 Reverse Proxies

**Example:** Nginx forwarding requests to backend servers.
**Related Vulnerabilities:** Misconfiguration, Header Injection

### 14. ⚖️ Load Balancers

**Example:** Distributing requests across multiple instances.
**Related Vulnerabilities:** Misrouting, Session Affinity Issues

### 15. 🔗 Internal APIs

**Example:** Microservices communicating via private APIs.
**Related Vulnerabilities:** Broken Access Control, Data Leakage

### 16. 📡 Data Streaming

**Example:** Sending live logs through a streaming endpoint.
**Related Vulnerabilities:** Data Leakage, Insecure Channels

### 17. 🛡️ Custom Middleware

**Example:** Middleware adding security headers to responses.
**Related Vulnerabilities:** Misconfiguration, Bypass

### 18. 📝 Job Queues

**Example:** Tracking background jobs with Celery.
**Related Vulnerabilities:** Unauthorized Access, Task Injection

### 19. 🚩 Feature Flags

**Example:** Toggling new features using LaunchDarkly.
**Related Vulnerabilities:** Feature Abuse, Logic Manipulation

### 20. 📜 Audit Logs

**Example:** Logging every admin action for compliance.
**Related Vulnerabilities:** Tampering, Insufficient Logging

### 21. ✅ Data Validation Endpoints

**Example:** `/validate/email` checks if an email is valid.
**Related Vulnerabilities:** Validation Bypass, Injection

### 22. 🔑 OAuth2 Token Endpoints

**Example:** `/oauth/token` issues access tokens for apps.
**Related Vulnerabilities:** Token Leakage, Replay

### 23. 🛡️ Web Application Firewalls (WAF)

**Example:** Blocking malicious requests before reaching the app.
**Related Vulnerabilities:** Bypass, Misconfiguration

### 24. 🗄️ Database Migrations

**Example:** Applying schema updates with migration scripts.
**Related Vulnerabilities:** Unauthorized Access, Data Loss

### 25. 🖥️ Server-Side Rendering (SSR) Endpoints

**Example:** Generating dynamic product pages on demand.
**Related Vulnerabilities:** Template Injection, XSS

### 26. 🌐 Content Delivery Networks (CDN)

**Example:** Serving static images from a global CDN.
**Related Vulnerabilities:** Cache Poisoning, Data Leakage

### 27. 🔗 API Gateways

**Example:** AWS API Gateway managing multiple backend APIs.
**Related Vulnerabilities:** Misconfigured Routes, Broken Access Control

### 28. 🔒 Data Encryption Endpoints

**Example:** `/encrypt` API to secure sensitive data.
**Related Vulnerabilities:** Weak Cryptography, Key Leakage

### 29. 🐞 Error Reporting Endpoints

**Example:** Frontend sends errors to Sentry via `/error-report`.
**Related Vulnerabilities:** Information Disclosure, Injection

### 30. 🌐 Custom DNS Resolvers

**Example:** Resolving internal service domains automatically.
**Related Vulnerabilities:** DNS Spoofing, Privilege Escalation

