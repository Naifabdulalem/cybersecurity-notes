---

# Introduction to the Burp Proxy

The Proxy module is one of the most important features in Burp Suite. It acts as a middleman between my browser and the target web application.

Normally, when I visit a website, my browser sends requests directly to the server. With Burp Suite running as a proxy, every request passes through Burp first. This gives me the ability to inspect, modify, or even stop requests before they reach the server.

This feature is extremely useful during penetration testing because it allows me to understand how a web application communicates with its backend.

---

# Proxy Workflow

The basic workflow looks like this:

```text
Browser
    │
    ▼
Burp Proxy
    │
    ▼
Web Server
```

Every request and response travels through Burp Suite, allowing me to analyze the application's behavior.

---

# Proxy Intercept

The **Intercept** tab allows Burp to pause outgoing HTTP requests.

When **Intercept is ON**, Burp captures every request before it reaches the server.

From here I can:

- View the request
- Edit headers
- Modify parameters
- Change cookies
- Forward the request
- Drop the request completely

If **Intercept is OFF**, Burp simply forwards traffic without stopping it.

---

# HTTP History

The HTTP History tab records every request that passes through Burp.

This became one of the most useful features during the room because I could review every page I visited without needing to browse the website again.

Each request contains information such as:

- Request method
- URL
- Status code
- Response length
- MIME type

This makes it easy to analyze how the application works.

---

# Connecting Firefox with Burp (FoxyProxy)

Instead of changing Firefox proxy settings manually, I used the **FoxyProxy** extension.

FoxyProxy makes switching between normal browsing and Burp Suite much easier.

The available options were:

- Disable
- Burp
- Caido

To send my browser traffic through Burp, I simply selected **Burp**.

---

# Configuring Burp

The setup process was straightforward.

1. Open Burp Suite.
2. Start a Temporary Project.
3. Use the default configuration.
4. Launch Firefox.
5. Select **Burp** in FoxyProxy.
6. Browse the target website.

Once configured, Burp immediately started capturing my browser traffic.

---

# Target Module

The Target module helps visualize the structure of a web application.

The most useful feature is the **Site Map**.

As I browsed the website, Burp automatically recorded every page I visited.

This included:

- Pages
- Directories
- JavaScript files
- Images
- API endpoints

Instead of manually keeping track of URLs, Burp organized everything automatically.

---

# Site Map Challenge

During the room, I explored every page linked from the homepage.

After opening the Site Map, I noticed one endpoint that looked very unusual:

```text
/5yjR2GLcoGoiJ2ZK
```

Unlike the other URLs, this endpoint contained a random string instead of a meaningful page name.

Opening this endpoint revealed hidden content that wasn't obvious while browsing normally.

This exercise showed me how Burp's Site Map can help discover hidden functionality inside a web application.

---

# Issue Definitions

Although Burp Community Edition cannot automatically scan for vulnerabilities, it still includes a useful reference called **Issue Definitions**.

This section explains common web vulnerabilities such as:

- SQL Injection
- Cross-Site Scripting (XSS)
- Directory Traversal
- Cross-Site Request Forgery (CSRF)

Each entry contains:

- Description
- Risk level
- References
- Possible remediation

I found this section useful as a learning resource for understanding common web security issues.

---

# Burp Suite Browser

Burp also provides its own Chromium-based browser.

Using the built-in browser automatically routes all traffic through Burp without needing additional browser configuration.

Although I mainly used Firefox with FoxyProxy during this room, the Burp Browser is a convenient option because everything is already configured.

---

# What I Learned From This Section

- Burp Proxy intercepts communication between the browser and the server.
- HTTP History records every request made during browsing.
- FoxyProxy makes switching between normal browsing and Burp much easier.
- The Site Map automatically maps the application's structure.
- Hidden endpoints can often be discovered by simply browsing the application.
- Issue Definitions provide useful explanations of common web vulnerabilities.
