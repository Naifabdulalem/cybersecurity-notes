

# Scoping and Targeting

During a penetration test, it's important to define exactly what should be tested. Burp Suite allows me to create a **scope**, which tells Burp which websites or domains are considered part of the assessment.

Using a scope helps reduce unnecessary traffic and keeps my testing focused on the target application.

For example, if I am testing:



I can add this domain to the scope so Burp ignores requests sent to other websites.

This is especially useful when a website loads resources from external domains such as Google Fonts, CDNs, or analytics services.



# Proxying HTTPS

Most modern websites use HTTPS to encrypt communication between the browser and the server.

Since Burp Suite acts as a proxy, it needs to decrypt HTTPS traffic before it can inspect it.

To do this, Burp generates its own Certificate Authority (CA) certificate.

After installing Burp's CA certificate into the browser, Burp can decrypt HTTPS requests and responses, allowing me to inspect encrypted traffic without browser warnings.

Without installing this certificate, the browser will display SSL or certificate errors.


# Example Attack

The room demonstrated a simple example of how Burp Suite can intercept and modify HTTP requests.

The general workflow is:

1. Enable **Intercept**.
2. Visit the target website.
3. Burp captures the outgoing request.
4. Inspect or modify request parameters.
5. Forward the modified request to the server.
6. Analyze the server's response.

This process is the foundation of many manual web application security tests.



# Typical Burp Workflow

The workflow I learned throughout this room can be summarized as:


Open Burp Suite
        │
        ▼
Create Temporary Project
        │
        ▼
Configure FoxyProxy
        │
        ▼
Browse the target website
        │
        ▼
Inspect requests using Proxy
        │
        ▼
Review HTTP History
        │
        ▼
Explore the Site Map
        │
        ▼
Send interesting requests to Repeater
        │
        ▼
Modify requests for further testing


Although this room only introduced the basics, this workflow will be used repeatedly in future web penetration testing labs.



# Practical Exercise

During the room, I completed several hands-on tasks, including:

- Installing and launching Burp Suite Community Edition
- Learning the layout of the Burp interface
- Configuring Firefox with FoxyProxy
- Browsing a web application through Burp
- Exploring the Target Site Map
- Discovering a hidden endpoint using the Site Map
- Understanding the purpose of Burp's main modules

These exercises helped me become more comfortable using Burp Suite in a real testing environment.



# Key Takeaways

After completing this room, I learned that:

- Burp Suite is one of the most important tools for web application penetration testing.
- The Proxy module allows me to inspect and modify HTTP requests.
- HTTP History records every request sent through Burp.
- The Target Site Map automatically maps the structure of a web application.
- FoxyProxy makes switching between normal browsing and Burp very simple.
- HTTPS traffic can be inspected after installing Burp's CA certificate.
- Defining a scope helps focus testing on the intended target.
- Even the free Community Edition is powerful enough for learning manual web application testing.



# Personal Notes

A few things I want to remember when using Burp Suite:

- Keep **Intercept OFF** unless I need to modify a request. Otherwise, browsing becomes slow because every request is paused.
- Always verify that FoxyProxy is using the **Burp** profile before starting a lab.
- Check the **HTTP History** if I need to find a request that I missed.
- The **Site Map** is useful for discovering hidden pages and understanding the application's structure.
- Use **Repeater** to safely test modifications without refreshing the browser every time.


# Conclusion

This room gave me a solid introduction to Burp Suite and its role in web application security testing. I learned how Burp acts as an intercepting proxy, how to configure my browser to use it, and how to inspect HTTP and HTTPS traffic.

The hands-on exercises also helped me understand how to map a website, discover hidden endpoints, and become familiar with Burp's interface. These skills provide a strong foundation for future rooms that focus on identifying and exploiting web vulnerabilities.

c
# References

- TryHackMe – Burp Suite: The Basics
- https://portswigger.net/burp
- https://portswigger.net/web-security
