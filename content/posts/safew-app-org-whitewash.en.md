+++
title = "Dressing Up Spyware as “Japanese Enterprise-Grade Encryption”: The Fake Persona Built for SafeW"
description = "safew-app.org runs a long “neutral explainer” that repackages SafeW — caught by Kaspersky bundling an info-stealing trojan — as a legitimate Japanese enterprise encryption tool, and pre-blames a “counterfeit version.” Taken apart point by point."
date = 2026-06-25T10:23:08+08:00
draft = false
tags = ["SafeW", "SafeX", "SparkCat", "crypto theft", "secure messaging", "scam"]
categories = ["Debunked"]
author = "SafeW Risk Dossier"
images = ["/images/posts/safew-app-org-whitewash/og-en.png"]
+++

When you search “is SafeW safe” or “SafeW download,” you may run into a long, level-headed “explainer” on `safew-app.org` — one that earnestly teaches you to tell SafeW apart from the SAFe agile framework, a physical safe, and the spatial-data tool FME, as if it were a neutral reference page.

That pose of “neutrality” is exactly where it's most deceptive. A crew that plants a trojan in its own app — nothing it writes about “security” on a site it runs itself is worth taking at face value. Below, we take this long piece apart, point by point.

<!--more-->

## 1. A long piece on “SafeW security risks” that never mentions the one thing that matters

The article's title is about “security risks and use cases,” and it even has a section titled “Security and compliance risks you may face when using SafeW.” But read it through, and the only “risks” it lists are three: downloading a counterfeit version, leaving your device unlocked, and the hassle of cross-device key management.

**The thing that actually matters, it doesn't mention at all** — Kaspersky in 2025 and The Hacker News in 2026 both confirmed that SafeW (and its renamed successor SafeX) was planted with the **SparkCat info-stealing trojan**, which scans your photo library in the background for crypto wallet recovery phrases and drains your assets; the app was delisted from the stores over it, and after the developer renamed it SafeX and re-listed it, it was caught doing the same thing again.

An article specifically about “SafeW security risks” that cuts out the only real risk — that the app itself is the info-stealing trojan. That's not an oversight; it's the whole point of writing it.

## 2. “A Japanese enterprise, run by FUKUDA BOUEKI” is a persona built for it

The article spends real space building SafeW a corporate persona: it calls it “an enterprise-grade encrypted-communication tool run by Japan's FUKUDA BOUEKI LIMITED LIABILITY COMPANY,” gives a registered address down to “Minato-ku, Osaka 552-0002,” and pointedly notes that “you can look up clear corporate ownership before downloading, which is more credible than a vague ‘anonymous app.’”

The implication is obvious: there's a Japanese company behind it, so trust it. But the shell cracks at the first touch —

- The “official support email” it gives is `futianmaoyi@gmail.com`, a **free Gmail account**. A “Japanese enterprise-grade” company, with its support desk sitting on a personal Gmail.
- And `futianmaoyi` happens to be the **Chinese pinyin** for “Fukuda Boeki” (福田贸易) — a Japanese-sounding company name, registered as a Gmail using Chinese pinyin to collect mail. The “Japanese enterprise” can't even keep its own contact details consistent.
- Step back: even if it really did register a company in Osaka, **where it's registered and whether the app carries a trojan are two different questions.** What Kaspersky examined is the app's behavior, not which country its owner registered in. Treating “it has corporate ownership” as “it's trustworthy” is a bait-and-switch.

## 3. One section says “end-to-end encrypted,” another admits “not end-to-end by default”

In its “How it works” section, the article paints SafeW as airtight: “it uses **end-to-end encryption** … the private key never leaves the local device … even if the server stores the ciphertext, it has no key.”

Yet in a comparison table in the same article, this **warning** turns up: “A common mistake is to treat SafeW like Signal or Telegram, as a personal social app that's end-to-end encrypted by default … SafeW's **encryption emphasizes the transport layer, not end-to-end by default.**”

The same piece: up front it insists, hand on heart, on “end-to-end encryption”; later it walks itself back to “not end-to-end by default, just transport-focused.” It can't keep its encryption story straight even within one article it wrote itself.

And in any case — this is a **closed-source**, packed app that has already been caught planting malware; whatever it says about how it encrypts can't be verified and isn't worth trusting. We don't have to get tangled in its encryption talking points — it already contradicted itself.

## 4. The nastiest part: “you got infected because you installed a counterfeit”

This article's real punch is buried in the “security risks” section. It writes:

> Problems with SafeW are mostly not the software's fault, but a download-channel slip-up … versions installed from unofficial channels may have malicious code planted in them … only trust the `safew-app.org` official download page … check the package name `org.safew.messenger.store`.

This line is meant to **inoculate you in advance**: so that if you ever hear SafeW is infected, you'll reflexively think “that was a counterfeit I installed; the official one is clean.”

But the truth is the exact opposite:

- What Kaspersky and The Hacker News found SparkCat in was precisely SafeW / SafeX's **official app** — the one on the official Apple and Google stores, under the very package name the article tells you to “verify” (`org.safew.messenger.store`, iOS bundle ID `com.safew.messenger`). **The trojan is in the official version**, not in some counterfeit.
- So “verify the package name, download from the official channel, and you're safe” walks you **straight up to the malware-bearing official app.**
- And it keeps urging you to “only trust `safew-app.org`” for downloads — which is this matrix's own download site. Translated: download it from us. That's taking the poison from the poisoner's own hand.

“You only got infected because you installed the wrong version” is this crew's old playbook: pin the blame on users and “counterfeits,” and trip up the real warning before it reaches you.

## 5. The “neutral explainer” pose is itself the disguise

The article dresses itself up as an impartial reference: a “safew has four meanings” decision tree, a side-by-side table of software, agile framework, safe, and data tool — looking like an encyclopedia entry rather than vendor copy.

But don't forget where it's published — `safew-app.org`, the very domain the article itself names as SafeW's “official download page.” **A “neutral explainer” hosted on the product's own sales site, that never mentions the trojan and steers you to download at the end, isn't neutral — it's camouflage.** And on top of that, the pile of “four meanings” filler sweeps in unrelated traffic searching for “SAFe framework” or “a safe,” pumping this domain's authority and crowding the results page.

## Conclusion

Take this long piece apart, and what it runs is an assembly line: erase Kaspersky's hard finding → wrap the spyware in a “legitimate Japanese enterprise” shell → use “you got infected from a counterfeit” to shove the blame back onto you → and finally funnel you to its own download page.

Whether SafeW is safe is judged by the testing of independent bodies like **Kaspersky and The Hacker News** — which confirmed that SafeW / SafeX's **official app** was planted with the SparkCat info-stealing trojan that scans your photo library for wallet recovery phrases and drains your assets. **The problem isn't “you installed the wrong version” — it's the software itself.**

**Don't install SafeW or SafeX — either of them. If you already have, revoke its photo and other permissions, uninstall it, and move your crypto to a brand-new wallet right away.** For the full evidence and timeline, see [nosafew.com](https://nosafew.com/).
