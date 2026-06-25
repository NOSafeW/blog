+++
title = "SafeW's “Security Reports” Are Lying to You: One Says Signal, the Other Says Telegram"
description = "Put SafeW's two self-published “security” write-ups side by side and you don't get proof of safety — you get proof that its own claims can't agree with each other, and can't be trusted."
date = 2026-06-23T00:28:08+08:00
draft = false
tags = ["SafeW", "SafeX", "SparkCat", "crypto theft", "secure messaging", "scam"]
categories = ["Debunked"]
author = "SafeW Risk Dossier"
images = ["/images/posts/safew-fake-security-reports/og-en.png"]
+++

When you search “is SafeW safe,” the “security reviews” and “security reports” near the top often aren't neutral third parties — they're SafeW itself. It has registered a cluster of look-alike domains — `safews.cn`, `safew.org`, `safew-app.org`, `safew-im.com`, and more — that keep publishing the same self-serving “security analysis,” flooding the first page of results so the first thing you see is SafeW vouching for SafeW.

Let's be clear up front: **a developer that plants information-stealing malware in its own app has zero credibility when it writes its own “security report.”** When it claims to use Signal, claims to be end-to-end encrypted, claims to hold some international certification, you have no reason to believe any of it — none of it can be verified on a closed-source, packed binary, and all of it comes from an outfit already caught stealing user data. The only reason we go through it point by point below isn't that its material counts as evidence; it's that its own several stories can't even keep each other straight.

> One write-up says SafeW uses the Signal protocol; the other says Telegram. These are two incompatible designs, and the same app is described both ways — its “reports” say whatever they please, and not one of them can be relied on.

<!--more-->

## 1. The protocols contradict each other: one says Signal, one says Telegram

The “security review” on `safews.cn` states it plainly:

> “SafeW uses the Signal open-source encryption protocol, the most trusted end-to-end encryption scheme recognized by cryptographers worldwide.”

{{< figure src="/images/posts/safew-fake-security-reports/signal.png" alt="safews.cn claims SafeW uses the Signal protocol" caption="The `safews.cn` write-up: 'SafeW uses the Signal open-source encryption protocol.'" >}}

The PDF “security report” on `safew.org` tells a different story:

> “SafeW's core communication encryption is based on Telegram's MTProto 2.0 protocol.”

{{< figure src="/images/posts/safew-fake-security-reports/telegram.png" alt="the safew.org PDF claims SafeW is based on Telegram MTProto" caption="The `safew.org` PDF: its core encryption is 'based on Telegram MTProto 2.0.' The same app, two different stories." >}}

The Signal protocol and Telegram's MTProto 2.0 are two completely different, incompatible designs. No single app can both “use the Signal protocol” and “be based on MTProto 2.0.” Two documents, both wearing the “official” label, flatly disagree. With two stories that fight each other, what that really tells you isn't which one is right; it's that **its “reports” say whatever they please, and not one of them can be relied on.**

Still, at least one claim can be disproven outright. To show “the libraries it uses are legitimate,” that same “security report” lists the app's core libraries in its own screenshot:

- `libtmessages.48.so`, which it itself labels “Telegram core communication API”
- a local database named `cache4.db`, with a message table called `messages_v2`

{{< figure src="/images/posts/safew-fake-security-reports/libtmessages.png" alt="the report's library list includes libtmessages.48.so" caption="The PDF's own list of core libraries: `libtmessages.48.so`, labeled 'Telegram core communication API.'" >}}

These all come from Telegram — fingerprints you can't scrub off. **SafeW is just a reskinned fork of Telegram.** So the `safews.cn` write-up's confident “uses the Signal protocol” **is a flat lie you can catch on the spot.** As for the other document that calls itself “Telegram-based,” that doesn't deserve to be taken at face value either — a packed, closed-source app already caught planting malware can claim anything it likes about what it uses and how it encrypts, and none of it can be verified.

| | The `safews.cn` write-up | The `safew.org` PDF |
|---|---|---|
| Encryption protocol | “uses the Signal protocol” | “based on Telegram MTProto 2.0” |
| Scope of E2E | “all communications are end-to-end encrypted” | E2E only for “secret chats” |
| Server storage | “zero storage, no message content kept” | normal chats relayed through MTProto servers |

The same app, three key questions, three answers that don't line up.

## 2. “Signal's audits apply to SafeW” — a bait-and-switch

The review has another line built to impress:

> “The Signal protocol has undergone multiple independent audits by Cure53 and others… since SafeW uses the Signal protocol directly, those audit results apply equally to SafeW.”

This doesn't hold, for two reasons. First, as shown above, SafeW doesn't use Signal at all — the premise is already false. Second, even if it did use some protocol, **auditing a protocol and auditing your specific app are two entirely different things.** Cure53 audited Signal's public source code; SafeW is closed-source, no one can see its implementation, and there's no reason whatsoever to transfer an audit of Signal onto it.

Software that genuinely welcomes scrutiny opens its source so anyone can check. SafeW goes the opposite way — which the next section makes even clearer.

## 3. That “Ijiami” shell protects the people who planted the malware, not you

The “security report” hammers one thing as a selling point: that it uses “Ijiami Enterprise” hardening, DEX VMP virtualization, and code obfuscation to “resist static reverse engineering.”

{{< figure src="/images/posts/safew-fake-security-reports/ijiami-shell.png" alt="the report shows its Ijiami Enterprise hardening" caption="The report shows off its 'Ijiami Enterprise' hardening as a selling point — packing an app is exactly what blocks an analyst's view." >}}

This needs to be said plainly. Packing and obfuscating an app exist to stop other people from prying it open and seeing what it actually does. For a clean app, that's anti-piracy at most; but for an app Kaspersky has confirmed carries information-stealing malware, it's obvious who that shell protects — it blocks security researchers and antivirus engines, making the planted malware harder to find and harder to prove. Here, packing has nothing to do with “protecting users”; **it protects the side doing the poisoning.**

And they have the nerve to write this “so-you-can't-find-the-problem” shell into a report as a “security feature” and market it to users. That alone shows they know perfectly well they have something to hide.

## 4. “Everything is end-to-end encrypted” — even by its own account, this falls apart

Again: **its saying it's end-to-end encrypted doesn't make it end-to-end encrypted.** This is a closed-source, packed app already caught planting malware; any encryption promise it makes can't be verified and isn't worth trusting.

Even one step back, reading strictly from its own material, the promise still breaks. The review says “all of SafeW's communications are end-to-end encrypted”; yet the “security report” itself writes that E2E only covers “secret chats,” and that “secret-chat history is kept only on the current device; switching devices or reinstalling requires starting a new session.” That is exactly how Telegram's “secret chats” behave: off by default, opt-in, not synced across devices. In other words, your everyday normal chats run client-to-server through its servers — the packet capture in the report hitting `45.204.21.75:5222` is its server address.

So “all communications are end-to-end encrypted” isn't even supported by its own other document. Meanwhile the review also claims “zero server storage, no message content kept,” which again contradicts the fact that ordinary chats must pass through the server.

## 5. ISO 27001, “all green on VirusTotal,” “passed Tencent's scan” — no proof, and another bait-and-switch

Both documents wave these around, and none of them survives a second question.

ISO 27001 and ISO 27034 certification: from start to finish, there's no certificate number, no issuing body, no record anyone can verify. A real ISO 27001 certificate carries a registration number you can look up on the certifying body's site. It can't produce any of that. A “certification” with no verifiable basis that nonetheless gets written into its marketing over and over isn't self-promotion — **it's deception aimed straight at users.**

“65 antivirus engines all green on VirusTotal,” “passed Tencent's scan”: scanning one submitted package once and getting “no detection at the time” does not prove the app is clean. A few reasons. First, SparkCat-class stealers are packed and obfuscated to begin with (that very shell), and signature-based antivirus misses them easily. Second, you can perfectly well run a clean build to produce a “scan report,” then distribute the actually-malicious package from your own website — bypassing app-store review, which is exactly what its “private deployment” is really for. Third, the fine print on that Tencent screenshot says plainly it's only a free online malware-scan service, not an endorsement of any kind.

The conclusion that actually carries weight is the opposite one: Kaspersky in February 2025, and The Hacker News in 2026, **publicly named SafeW / SafeX for carrying the SparkCat information-stealing trojan.** One independent security vendor's hands-on finding is worth more than any number of “all green” reports it prints for itself.

## 6. That READ_MEDIA screenshot: answering a question nobody asked

The “security report” makes a point of including a JADX code-search screenshot showing the app requesting `READ_MEDIA` (read photos/media) permission, with a batch of classes under `org.safew.messenger` checking `READ_MEDIA_IMAGES`, `READ_MEDIA_AUDIO`, and the like. It wants this to show that it only requests photo access when there's a genuine need, so its “permission design is reasonable.”

{{< figure src="/images/posts/safew-fake-security-reports/read-media.png" alt="the READ_MEDIA permission code screenshot from the report" caption="The READ_MEDIA permission-code screenshot from the report. The question isn't when it asks — it's what it does once it has your photos." >}}

This dodges the real question. The crux was never “when it requests permission,” but “what it does with your photos once it has them.” SparkCat's method is precisely this: once it has photo-library access, it uses OCR to scan your screenshots for crypto wallet recovery phrases, then drains your wallet. What Kaspersky confirmed is that after-the-fact theft — which has nothing to do with how restrained it looks while requesting the permission.

More to the point, the very behavior it offers as proof of innocence matches Kaspersky's description of SparkCat exactly. Kaspersky's researchers note that SparkCat works by disguising the theft as a normal permission request — using a plausible-looking reason to obtain authorization, then quietly scanning the photo library in the background. Which means “I only request it when genuinely needed, and the design is reasonable” doesn't clear it at all; **it's precisely the disguise this kind of trojan relies on.** The harder it tries to use this screenshot to prove its “permission request is reasonable,” the more snugly it fits the modus operandi Kaspersky described.

Besides, “only requests it when needed” is just its own narration paired with a screenshot. This is a closed-source, packed app; what it shows you is only the few snippets of code it chooses to show. Inside the shell, beyond that screenshot, where your photo data goes after it's read is something you have no way to check. Using a “see how restrained my request is” screenshot to answer an independent body's accusation of theft is changing the subject.

## 7. It was never a security team — it's a content farm

Sites like `safews.cn` are, at heart, content farms churning out SEO articles: “How to Set Up SafeW Privacy,” “The Complete SafeW Desktop Guide,” “SafeW Voice and Video Call Hands-on Test”… a new one every few days, stuffed with keywords, with a single purpose — to occupy every search result connected to “SafeW.” It's no surprise that a “security review” cobbled together by a content farm reaches for “Signal protocol” and “ISO 27001” off the cuff: no one's checking, and no one has to answer for it.

The “official download site” label, meanwhile, hangs on `safews.cn`, `safew.org`, and several other different domains at once. How can there be that many “official” sites? That's exactly the playbook of a domain matrix: one set of talking points, copied across dozens of look-alike domains that cite each other and fill the whole results page.

## Conclusion

Put these two “self-certifications” side by side, and what you can confirm isn't “how safe SafeW is” — it's that its account neither holds together nor can be believed:

- the encryption protocols contradict each other, one saying Signal, the other Telegram;
- it borrows Signal's audits to pass itself off as secure and mislead users, while staying closed-source and packed so no one can verify anything;
- it markets a “so-you-can't-find-the-problem” packing shell as a security feature;
- “everything is end-to-end encrypted” isn't even supported by its own other document;
- the ISO certification can't produce a single number, and “all green on VirusTotal” can't hold off an independent vendor's hands-on finding.

Whether software is safe is judged by the testing of independent bodies like Kaspersky — not by reports the developer prints for itself, and certainly not by a cluster of sites it registered to vouch for one another. And this developer has been confirmed to plant a trojan that steals crypto wallets inside its own product — so every “we're safe” it utters **should be read in reverse.**

**Don't install SafeW or SafeX — either of them. If you already have, revoke its photo and other permissions, uninstall it, and move your crypto to a brand-new wallet right away.** For the full evidence and timeline, see [nosafew.com](https://nosafew.com/).
