# Burp Suite: The Basics

## Introduction

In this room, I learned the fundamentals of Burp Suite, one of the most popular tools used for web application security testing.

Burp Suite works as an intercepting proxy between my browser and a web server. Instead of communicating directly with the website, my requests first pass through Burp Suite. This allows me to inspect, intercept, modify, and replay HTTP requests and responses before they reach the server.

Throughout this room, I learned how to configure Burp Suite, connect my browser using FoxyProxy, navigate the interface, and use some of the most important modules that will be useful during future penetration testing labs.

---

# What is Burp Suite?

Burp Suite is a web application security testing tool developed by PortSwigger. It is widely used by penetration testers and bug bounty hunters to analyze web traffic and identify vulnerabilities.

Instead of simply viewing a website in the browser, Burp allows me to see exactly what is being sent between my browser and the server. I can also modify requests before they are forwarded, making it an essential tool for manual web application testing.

---

# Burp Suite Editions

Burp Suite comes in two editions.

## Community Edition

The Community Edition is free and mainly focuses on manual testing. Although it has fewer features than the Professional Edition, it still provides all the tools needed to learn web application testing.

Some of the available tools include:

- Proxy
- Repeater
- Decoder
- Comparer
- Limited Intruder

## Professional Edition

The Professional Edition is the paid version of Burp Suite.

It includes additional features such as:

- Automated vulnerability scanning
- Website crawling
- Project saving
- Report generation
- Advanced Intruder features

The Professional Edition is designed for penetration testers who regularly assess web applications.

---

# Installing Burp Suite

In the TryHackMe AttackBox, Burp Suite Community Edition is already installed, so there is no need to download it manually.

When launching Burp Suite, I learned the following startup process:

1. Start Burp Suite.
2. Create a Temporary Project.
3. Use the default configuration.
4. Click **Start Burp**.

After loading, Burp opens the Dashboard, which acts as the main overview of the current project.

---

# The Dashboard

The Dashboard is the first page displayed after Burp Suite starts.

It provides useful information about Burp's current activity.

The Dashboard contains four main sections.

## Tasks

Displays background tasks that Burp is performing.

In the Community Edition, the default task is **Live Passive Crawl**, which records the pages visited while browsing.

---

## Event Log

Shows information about everything Burp is doing.

Examples include:

- Starting the proxy
- Browser connections
- Network events
- Internal Burp messages

This section is useful when troubleshooting connection problems.

---

## Issue Activity

This feature mainly belongs to Burp Professional.

It lists vulnerabilities discovered by Burp's automated scanner.

Since I used the Community Edition, this section remained mostly empty.

---

## Advisory

The Advisory section provides information about detected vulnerabilities.

It explains:

- What the vulnerability is
- Why it is dangerous
- Possible remediation steps

Like Issue Activity, this feature is mainly useful in the Professional Edition.

---

# Navigating Burp Suite

Burp Suite contains multiple modules located at the top of the interface.

Each module has its own purpose during web application testing.

The modules I learned about include:

- Dashboard
- Target
- Proxy
- Intruder
- Repeater
- Decoder
- Comparer

Some modules also contain additional sub-tabs.

For example:

Proxy

- Intercept
- HTTP History
- WebSockets

These sub-tabs organize features related to the selected module.

---

# Useful Keyboard Shortcuts

To navigate more quickly, Burp provides several keyboard shortcuts.

| Shortcut | Function |
|-----------|----------|
| Ctrl + Shift + D | Dashboard |
| Ctrl + Shift + T | Target |
| Ctrl + Shift + P | Proxy |
| Ctrl + Shift + R | Repeater |
| Ctrl + Shift + I | Intruder |

Using shortcuts makes switching between modules much faster during testing.

---

# Burp Suite Settings

Burp Suite has two different types of settings.

## User Settings

User settings affect Burp Suite every time the application starts.

Examples include:

- Appearance
- Hotkeys
- Updates

These settings remain saved even after closing Burp.

---

## Project Settings

Project settings only affect the current project.

Examples include:

- Scope
- Proxy configuration
- Sessions
- Connections

Since I was using Burp Suite Community Edition, these settings were not saved after closing the application.

---

# Helpful Settings

During the room, I also learned where to find some useful settings.

### Cookie Jar

Location:

Settings → Sessions

Used to manage cookies collected during browsing.

---

### Updates

Location:

Settings → Suite → Updates

Controls Burp Suite update behaviour.

---

### Hotkeys

Location:

Settings → User Interface → Hotkeys

Allows keyboard shortcuts to be customized.

---

# What I Learned From This Section

- Burp Suite is an intercepting proxy used for web application testing.
- The Community Edition is suitable for learning manual penetration testing.
- The Dashboard provides an overview of Burp's activity.
- Burp contains multiple modules, each designed for a different task.
- User settings and Project settings serve different purposes.
