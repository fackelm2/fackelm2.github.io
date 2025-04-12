---
layout: post
title: Multi-Factor Authentification
date: 2024-12-15 07:00:10
last_updated: 2024-12-15 07:00:10
description: safer authentication (multi-factor authentciation - MFA)
tags: security authentication
categories: security
featured: false
---

draft

## One-factor Authentification

do not do this in 2024

## Two-factor Authentification

SMS, one-time passcodes and mobile authentication

"If we've learned anything in the last few years it's that "something you know" isn't a great authentication factor.
We could already use hardware keys to log in over SSH (e.g. yubikey or TPM chips), and/or use one-time passwords."
(see https://github.com/ThomasHabets/sim)

## Multi-factor authentication with Yubico

"Phishing-resistant MFA that stops modern cyberthreats. Trusted by the world’s largest brands."

Not all MFA is created equal

"Stop phishing attacks and account takeovers before they start with modern,
phishing-resistant multi-factor authentication (MFA).
Stay ahead of evolving cyber threats and regulatory requirements with a proven solution which cannot be bypassed by
malicious actors, unlike basic forms of MFA such as SMS, one-time passcodes and mobile authentication.
Accelerate your zero trust strategy and gain a bridge to passwordless for enterprises, SMBs, individuals and developers."

[https://www.yubico.com/de/product/security-key-nfc-by-yubico-black/]: https://www.yubico.com/de/product/security-key-nfc-by-yubico-black/ "Yubico"

[https://www.yubico.com/de/product/security-key-nfc-by-yubico-black/]

### See Hints

[https://github.com/ThomasHabets/cmdg]: https://github.com/ThomasHabets/cmdg "U2F Yubikey"

[https://github.com/ThomasHabets/cmdg]

"GMail web UI uses username and password to log in, which means they can be stolen. You should be using U2F Yubikeys, so that losing the password isn't as big of a deal. The user has to re-type the password every now and then, which is an opportunity for the attacker to steal the password."

### FIDO authentication standard

"Yubico co-created the FIDO authentication standards and made them open to drive an ecosystem of strong security
across all platforms and services"

## SIM Aprover

https://play.google.com/store/apps/details?id=com.thomashabets.simapprover

"Mit dieser App können Sie vom Sim-Tool erstellte Administratorbefehle genehmigen. Weitere Informationen zum
Einrichten finden Sie unter: https://github.com/ThomasHabets/sim"

"But you have peer review for code, don't you? Why not peer review for adding users, removing files, and installing software?"
