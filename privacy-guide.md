---
title: Proof of Concept - Privacy Guide
description: 
published: true
date: 2021-12-07T18:04:57.878Z
tags: 
editor: markdown
dateCreated: 2021-12-07T18:04:57.878Z
---

**THIS IS A PROOF OF CONCEPT, THE CONTENT OF THIS PAGE WILL SURELY END UP IN A DEDICATED WEB PAGE OUTSIDE OF THE WIKI**

# Privacy Guide


## Why?


This guide has been created because privacyguides org and privacytools io made awful decisions and recommend awful things **that even their own team members disagree with** (https://mikaela.info/blog/english/2021/11/23/leaving-privacyguides.html)

Some examples of bad decisions I contested:

- Removal of LineageOS: https://github.com/privacyguides/privacyguides.org/pull/294#issuecomment-988092870
- Removal of Posteo: https://github.com/privacyguides/privacyguides.org/pull/369#issuecomment-988094653
- Removal of CanvasBlocker: https://github.com/privacyguides/privacyguides.org/pull/259#issuecomment-988097091
- Removal of Ubuntu Touch: https://github.com/privacyguides/privacyguides.org/pull/253#issuecomment-988099275
- Removal of 7zip: https://github.com/privacyguides/privacyguides.org/pull/258#issuecomment-988104029

The "Do not use" category include things recommended by privacyguides org, that, as the name suggest, you shouldn't use.


## Requirements


- All software must be open source, no exception.

- All providers musn't be based in the [Five Eyes](https://en.wikipedia.org/wiki/Five_Eyes) - USA/Canada/Australia/United Kingdom/New Zealand.

- All providers *shouldn't* ideally be based in Switzerland.

- All providers must have open source clients (or use an open standard, like e-mail).

- All providers *should* ideally have open source servers.

- All providers mustn't be invite only (sorry RiseUp and cTemplar)

# List

## Providers


### Cloud Storage

Use:

- Your own self-hosted Nextcloud

- Any provider supported by [Rclone](https://rclone.org/docs/)

Do not use:

- Any provider not supported by [Rclone](https://rclone.org/docs/)


### DNS Resolver

Use (if you use a VPN):

- The one provider by your VPN provider

USe (if you don't use a VPN):

- [Adguard](https://adguard.com/en/adguard-dns/overview.html) (Note: Log some things: https://adguard.com/en/privacy/dns.html )

- [Quad9](https://quad9.net/) (Note: Based in Switzerland)

Do not use:

- Cloudflare: it's [Cloudflare](https://git.disroot.org/dCF/deCloudflare)

- NextDNS: USA-based

- UncensoredDNs: DNS requests are to sensitive to give to an hobby project.


### Email provider

Resource: https://digdeeper.neocities.org/ghost/email.html

Use:

- [Posteo](https://posteo.de/en) (Note: No custom domains allowed, but 100% open source)

- [Mailbox](https://mailbox.org/en/) (Note: 100% closed source)

- [Tutanota](https://tutanota.com/) (Note: No IMAP/POP3, using their *open source* client is required, server code is closed source)

- [Disroot](https://disroot.org/en/services/email) (Note: Hobby project, but **should** [last](https://forum.disroot.org/t/will-disroot-last/101/2). I still wouldn't recommended it as a main provider.)

Do not use:

- Protonmail: Sketchy (potentially a honeypot), alledgedly weird fundings sources tied to Israel inteligence agencies.

- StartMail: Made Startpage, and sold it to an advertising company.


### Search Engines

Use:

[SearX](https://searx.me/)

Do not use:

- Anything else (including Whoogle, that is just SearX but worse)


### Social Networks

Social networks are fundamentaly not private by design, but if you have to use one, follow this list:

Use:

- Any Fediverse-compatible project (Mastodon, diaspora*, Friendica, GNU social, Pleroma, Pixelfed...)

- [Lemmy](https://join-lemmy.org/) (Note: Projects owners/creators are heavily politically biased)

Do not use:

- Anything else


### Social News Aggregator

Use: 

- RSS

Do not use:

- Anything else


### VPN

Note: A good rules is to avoid any VPN that has referals and/or advertise (basically 90% of them).

Use:

- [Mullvad](https://mullvad.net/)

- [IVPN](https://www.ivpn.net/)

Do not use:

- ProtonVPN: Like Protonmail: Sketchy (potentially a honeypot), alledgedly weird fundings sources tied to Israel inteligence agencies.


# Software

TODO