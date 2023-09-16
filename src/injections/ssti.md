# Server Side Template Injection

Frameworks like Flask and Django (Python), Liquid (Ruby), Handlebars (NodeJS), etc. are ways of extending traditional programming languages into interactive web applications. 

Vulnerabilities can occur when user input is not sanitized. These are especially dangerous because they allow remote code execution (RCE). 

---
Example:

Flask (a Python web framework) uses double curly braces ```{{}}``` to mix Python code into an HTML page. A malicious user could post ```{{ 7*7 }}``` to see if the answer 49 appears anywhere in the resulting webpage, illustrating that RCE is possible.  

---



```${{<%[%'"}}%\.```