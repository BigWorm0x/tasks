# Same-Origin Policy (SOP) vs Cross-Origin Resource Sharing (CORS)

## 1. Same-Origin Policy (SOP)

### What is it?
- A **browser-enforced security policy** that prevents JavaScript on a webpage from accessing data from another webpage **unless they share the same origin** (same protocol, domain, and port).
- **Purpose**: Prevent attacks like data theft (e.g., stealing cookies or sensitive information).

### How does it work?
- **Blocks**:
  - `fetch()` or `XMLHttpRequest` to different domains
  - Reading content from an `iframe` of another origin
- **Allows**:
  - Loading resources like images (`<img>`), scripts (`<script>`), or CSS (`<link>`) from other domains (but JS cannot read their content)

### Example:
```javascript
// A page on https://example.com tries to fetch data from https://api.another.com
fetch("https://api.another.com/data")
  .then(response => response.json()) // ❌ Fails due to SOP
  .catch(err => console.log("Blocked by SOP!"));

2. Cross-Origin Resource Sharing (CORS)
What is it?
A mechanism that safely relaxes SOP by using special HTTP headers

Purpose: Enable secure cross-origin communication (e.g., accessing APIs)

How does it work?
The server must include headers like:

http
Copy
Access-Control-Allow-Origin: https://example.com
Access-Control-Allow-Methods: GET, POST, PUT
The browser checks these headers before allowing access

Example:
If api.another.com supports CORS:

http
Copy
HTTP/1.1 200 OK
Access-Control-Allow-Origin: https://example.com
Key Differences
Feature	SOP	CORS
Purpose	Blocks cross-origin access	Allows cross-origin access with conditions
Enforced by	Browser only	Browser + server cooperation
Default	Always active	Opt-in via server headers
Practical Comparison
Without CORS:

SOP blocks example.com from reading api.another.com data

With CORS:

Server can explicitly allow example.com access
