## CSRF (Cross Site Resource Forgery)
* A CSRF attack tricks a logged-in user’s browser into making an unwanted request to a trusted site, using the user’s credentials (like cookies).
* Prevention
    * Using CSRF tokens:
        * Websites can generate unique tokens for each user session and include them in forms. The server verifies that the submitted token matches the one generated for the session, preventing unauthorized requests. 
        * Implementing strict SameSite cookie attributes: This helps ensure that cookies are only sent to the same site and not cross-origin. 
        * Verifying the Referer header: While not foolproof, verifying the Referer header can help identify if a request is coming from the expected origin. 

    
## Clickjacking
* Clickjacking tricks a user into clicking on something invisible or disguised, by overlaying or hiding sensitive UI elements (like buttons or links) inside an iframe or behind fake visuals.
* Prevention
    * X-Frame-Options: DENY or SAMEORIGIN (HTTP header). X-Frame-Options is an HTTP response header that controls whether a browser is allowed to render a page within a frame (like an <iframe>).
    * Content-Security-Policy: frame-ancestors 'none'. Content Security Policy (CSP) is a security standard that helps protect websites from various attacks, primarily cross-site scripting (XSS). It works by allowing web developers to control which resources (like scripts, stylesheets, images, and more) a browser can load and execute for a given page. By specifying legitimate sources, CSP helps prevent malicious code from being injected and executed, bolstering the security of web applications. 
    * UI challenges (e.g., double-click, confirm prompts)


## Pem
* A PEM file is a text-based file format commonly used to store cryptographic keys, certificates, and other related data. It's a de facto standard for storing and transmitting these items, often used in the context of SSL/TLS certificates and related security protocols. The format is defined by RFCs (Request for Comments) and is designed to be human-readable, typically containing Base64-encoded data surrounded by header and footer markers. 