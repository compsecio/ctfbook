# Server Side Template Injection

Frameworks like Flask and Django (Python), Liquid (Ruby), Handlebars (NodeJS), etc. are ways of extending traditional programming languages into interactive web applications. 

Vulnerabilities can occur when user input is not sanitized. These are especially dangerous because they allow remote code execution (RCE). 

---
Example:

Flask (a Python web framework) uses double curly braces ```{{}}``` to mix Python code into an HTML page. A malicious user could post ```{{ 7*7 }}``` to see if the answer 49 appears anywhere in the resulting webpage, illustrating that RCE is possible.  

---
1. Initial Recon:

    Determine which framework (Handlebars, Flask, etc.) is being used. One possibility is to send all the most common framework escape characters to see if any trigger a response. An example of this would be:

    ```${{<%[%'"}}%\.```

2. After elucidating which web framework, consult a CTF cheat sheet or use an automated tool like [this plugin](https://github.com/epinna/tplmap/blob/master/burp_extension/README.md) for Burp Suite. 


