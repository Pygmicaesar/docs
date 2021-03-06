---
layout: page
title: "Server-side PDF printing"
category: configuration
date: 2019-02-11 15:11:00
order: 5
---

> **Please contribute!** This document is a stub. If you have recently implemented a PDF generator that works well with modern WordPress in Seravo's environment, please contribute to this page via the Github link in top right corner.

Traditionally developers have generated PDF files on the server side using one of the tools below. Unfortunately, none of them meet modern standards anymore.

* [PHP-DOMPDF](http://dompdf.github.io/): Works only with PHP 5. Is not maintained anymore.
* PHP-FPDF: Works only with PHP 5 and is not maintained anymore. Anyway needed Apache and suexec to run, so was never a good option.
* wkhtmltopdf: Uses webkit for rendering and thus does not render correctly all modern websites. Needs X virtual framebuffer which is inconvenient server-side.

For modern WordPress sites there are three recommended options:
1. Render PDF files client-side using JavaScript and/or print CSS
2. Render PDF files server-side using the headless Chrome available in Seravo's environments
3. Use an custom WordPress plugins for the purpose (e.g. [Waterwoo](https://www.waterwoo.me/) for watermarks) or external service via API requests

Also note, that since Seravo's server have NodeJS available, any of the NodeJS server-side JavaScript tools out there are also potential options.
