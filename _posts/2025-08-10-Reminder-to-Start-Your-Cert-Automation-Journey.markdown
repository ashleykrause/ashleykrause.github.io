---
title:  "Reminder to Start Your Cert Automation Journey"
description: "With the latest operating systems mandating HSTS, and cert lifespans shrinking, it's time to automate your certificate management strategy"
date: 2025-08-10 15:52:00 -0400
categories: [pki]
tags: [certificates,pki,tls,automation]
image:
  path: https://imagedelivery.net/gOCYw6gNw41o7u2FuVh4ZA/9595c6be-4ee3-4e6b-a6f6-e54b0d09b200/public
  alt: TLS Certificate Lifetimes Illustration
---

With latest operating systems like Windows 11 mandating HSTS, and cert life cycles shrinking to 47 days in 2029[^footnote-1], manual cert rotation is going to become less and less realistic in large environments.

The real challenge is going to be with internal web interfaces (network switches, server idracs, virtualization environments...etc.) all of which likely have self signed certs at the moment by a large number of organizations. Unless if you want to install those self signed certs as trusted CAs on all endpoints, you'll need to get them certs enrolled by trusted certificate authorities.

I anticipate web browsers following the `CA/B Forum's` [^footnote-2] Guidance and enforcing the cert lifespans and only recognizing certs with lifespans less than the current industry's lifespan, and HSTS will make it impossible to override it.

Company's may need to begin looking into solutions like Let's Encrypt, Cyber Ark's Venafi, and Digicert One for handling certificate automation.

## References
[^footnote-1]: [TLS Certificate Lifetimes Will Officially Reduce to 47 Days](https://www.digicert.com/blog/tls-certificate-lifetimes-will-officially-reduce-to-47-days)

[^footnote-2]: [What is the CA/B Forum?](https://www.digicert.com/faq/compliance/what-is-the-certification-authority-browser-forum)
