---
title: Proxies
description: Learn all about proxies, how they work, and how they can be leveraged in a scraper to avoid blocking and other anti-scraping tactics.
menuWeight: 4.1
category: courses
paths:
- anti-scraping/proxies
---

# [](#proxies) Proxies

A proxy server provides a gateway between users and the internet, to be more specific in our case - between the crawler and the target website.

Many websites have [rate-limiting]({{@link glossary/rate_limiting.md}}) set up, which is when a website **limits** the **rate** at which requests can be sent from a single IP address. In cases when a higher number of requests is expected for the crawler - using a proxy is essential to let the crawler run as smoothly as possible and avoid being blocked.

Fixing rate-limiting issues is only the tip of the iceberg of what proxies can do for your scrapers, though. By implementing proxies properly, you can successfuly avoid the majority of anti-scraping measures listed in the [previous lesson]({{@link anti_scraping.md}}).

## [](#understanding-proxy-links) A bit about proxy links

When using proxies in your crawlers, you'll most likely be using them in a format that looks like this:

```text
http://proxy.example.com:8080
```

This link is separated into two main components: the **host**, and the **port**. In our case, our hostname is `http://proxy.example.com`, and our port is `8080`. Sometimes, a proxy might use an IP address as the host, such as `103.130.104.33`.

If authentication (a username and a password) is required, the format will look a bit different:

```text
http://USERNAME:PASSWORD@proxy.example.com:8080
```

## [](#proxy-rotation) Proxy Rotation

Web-scrapers can implement a method called "proxy rotation" to **rotate** the IP addresses they use to access websites. Each request can be assigned a different IP address, which makes it appear as if they are all coming from different users in different location. This greatly enhances performance, and is a major factor when it comes to making a web-scraper appear more human.

## [](#next) Next up

This module's first lesson will be teaching you how to configure your crawler in the Apify SDK to use and automatically rotate proxies. [Let's get right into it!]({{@link anti_scraping/proxies/using_proxies.md}})