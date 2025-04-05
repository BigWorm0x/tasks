# Same-Origin Policy (SOP) vs Cross-Origin Resource Sharing (CORS)

## 🔒 Same-Origin Policy (SOP)

### Definition
Security mechanism that restricts how documents/scripts from one origin can interact with resources from another origin.

### Key Points
- **Origin** = Protocol + Domain + Port
- Default browser security policy
- Prevents malicious scripts from accessing sensitive data
- Applies to: AJAX requests, DOM access, cookies, etc.

### How it Works
```javascript
// Blocked by SOP:
fetch('https://api.other-site.com/data')
  .then(response => response.json())
  .catch(err => console.error('Failed:', err));
Exceptions
Loading some cross-origin resources allowed:

<img src="...">

<script src="...">

<link href="...">

But JavaScript can't read the content

🔄 Cross-Origin Resource Sharing (CORS)
Definition
Mechanism that allows restricted resources to be requested from another domain.

Key Points
Extension to SOP (not replacement)

Requires server cooperation via HTTP headers

Enables secure cross-origin requests

Commonly used for APIs

Implementation
Server must include headers:

http
Copy
Access-Control-Allow-Origin: https://your-site.com
Access-Control-Allow-Methods: GET, POST, OPTIONS
Access-Control-Allow-Headers: Content-Type
Flow
Browser sends "preflight" OPTIONS request

Server responds with allowed methods/origins

If approved, actual request proceeds

📊 Comparison Table
Feature	SOP	CORS
Type	Restriction	Relaxation
Initiated by	Browser	Server + Browser
Default State	Block cross-origin requests	Allow with permission
Required For	All web interactions	Cross-domain APIs
Security Model	Deny-by-default	Allow-by-permission
Preflight Request	No	Yes (for complex requests)
🛠️ When to Use Each
SOP Use Cases
General web security

Preventing CSRF attacks

Isolating untrusted content

CORS Use Cases
Public APIs

Microservices architecture

CDN-hosted resources

Cross-domain single sign-on

⚠️ Common Issues
SOP Problems
Can block legitimate use cases

Difficult to debug

CORS Problems
Misconfigured headers

Overly permissive settings (Access-Control-Allow-Origin: *)

Preflight request overhead


