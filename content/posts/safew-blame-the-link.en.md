+++
title = "It Wasn't the Link That Stole Your USDT — It Was the App You Installed: Debunking the “iOS Vulnerability” Shill Posts"
description = "The moment someone gets their USDT drained, group chats flood with posts claiming “every iOS version is hacked, never click any link.” The panic gets aimed at links and websites, while the actual thief on your phone — SafeW and SafeX — never comes under suspicion. Here is that playbook, taken apart in plain language."
date = 2026-08-08T16:45:40+08:00
draft = false
tags = ["SafeW", "SafeX", "SparkCat", "crypto theft", "Xinbi Guarantee", "shill posts", "scam"]
categories = ["Debunked"]
author = "SafeW Risk Dossier"
images = ["/images/posts/safew-blame-the-link/og-en.png"]
+++

Over the past couple of days, the same post has been making the rounds in Chinese-language crypto and underground-payment group chats: on August 7, 2026, someone had 1.5 million USDT (worth over ten million RMB, by the post's own account) swept out of two wallets within ten seconds of each other. The post then offers its “deep analysis”: an Apple system vulnerability — iOS 13 through 26 have all been cracked, merely browsing a website can silently steal your wallet keys, therefore “do not click on any website” and “be careful with any URL.”

If this post has crossed your feed, keep the conclusion of this article in mind: **it wasn't a link you clicked that stole your USDT — it was an app you installed with your own hands.** And posts like this one, which blame everything on links and on Apple, are the smokescreen laid down for the real culprit. Below, in plain language, is who the thieves are and how the deflection script works.

<!--more-->

## 1. First, meet the thieves: this family of apps is in the USDT-stealing business

{{< figure src="/images/posts/safew-blame-the-link/tweet-xinbi.png" alt="Tweet: SafeW / SafeX pushed by Xinbi Guarantee, and related delivery apps, carry SparkCat" caption="The tweet: SafeW / SafeX, heavily pushed by Xinbi Guarantee, along with the closely connected delivery apps “Kuaizi Life” and “Wukong Waimai,” all carry SparkCat — malware built to steal wallet seed phrases." >}}

Xinbi Guarantee, a gray-market escrow bazaar on Telegram, runs a USDT-stealing business of its own. The two “insider” messengers it pushes hard — **SafeW** and **SafeX** — plus several Southeast Asian food-delivery apps tied to it in a thousand ways — “Kuaizi Life” (筷子生活) in the Philippines, “Wukong Waimai” (悟空外卖) in Thailand, “Baituo Baituo” (拜托拜托) in Dubai — have all been found carrying the same malicious code: **SparkCat, built specifically to steal crypto wallet seed phrases.**

This is not some group-chat rumor. Kaspersky, one of the world's best-known security firms, has confirmed it two years running:

- **February 2025**: Kaspersky published its SparkCat report — a batch of apps in the official App Store and Google Play had this stealer code embedded, and SafeW's package names were on the affected list. Per coverage at the time, the list included 43 apps from the App Store and 10 from Google Play; besides Wukong Waimai, it also featured ATV Asia TV, VPN accelerators, and several blockchain-related apps.
- **April 2026**: a new SparkCat variant surfaced — with “SafeW - Cloud Office Assistant” on iOS and SafeX on Android back on the list. New name, same theft.

{{< figure src="/images/posts/safew-blame-the-link/phhua-wukong.png" alt="Phhua forum post, February 2025: apps made by gray-industry operators" caption="A February 2025 post on Phhua, a Chinese-language forum in the Philippines: Kaspersky named Wukong Waimai among apps carrying SparkCat, which scans users' photo albums and can steal crypto and banking credentials." >}}

Plenty of Wukong Waimai users in Thailand said they had suffered unexplained thefts before, and only understood where the problem was after reading the coverage. The app even launched a WeChat mini-program.

The tweet puts it bluntly: **this is crooks preying on crooks.** People in these circles hold the most USDT, are the least likely to go to the police when robbed, and are the most eager to install whatever app “the circle” recommends — which makes them the fattest prey. Kaspersky has called it out two years in a row, people keep installing, and that is exactly the meal these thieves live off.

## 2. How SparkCat steals — no link-clicking required at any point

One piece of background first: **your seed phrase is the master key to your wallet** — the dozen-or-two English words you were told to write down when you created it. Whoever holds it can empty your wallet completely, without touching your phone, without your password, without any confirmation from you. Many people, for convenience, keep a screenshot of their seed phrase in their photo album. That screenshot is exactly what the thief is hunting for.

SparkCat's method, in plain language, is five steps:

1. You install an app that looks perfectly harmless — food delivery, chat, escrow deals.
2. It asks for **photo album access** with a legitimate-sounding excuse: sending pictures, uploading screenshots, submitting receipts. You tap “Allow” without a second thought.
3. In the background it runs OCR (the technology that “reads text out of images”) over your album, picture by picture, looking specifically for seed phrases, private keys, and bank card details.
4. Whatever it recognizes gets quietly uploaded to its server. At this point your wallet already belongs to someone else — you just don't know it yet.
5. The thief is in no hurry. One day they “harvest” in bulk, and a whole batch of wallets gets drained within seconds of each other.

Note: from start to finish, **you never clicked a single link**. You clicked nothing, and the money is gone anyway — because you installed the thief onto your phone yourself, and handed it your photo album with your own hands.

## 3. Now the “iOS vulnerability” post itself: a textbook deflection template

{{< figure src="/images/posts/safew-blame-the-link/shill-post-ios.png" alt="The “iOS vulnerability incident” post circulating in group chats" caption="The “iOS vulnerability” post flooding group chats: it warns you off every website and every URL — and never names a single app." >}}

Back to the post from the opening. It tells a story: two phones (one on iOS 18, one on 26.4), holding two different wallets, drained simultaneously within ten seconds; its “deep analysis” then concludes that phone A had its keys silently stolen while browsing a website — therefore, everyone, “do not click on any website.”

Not one part of it survives scrutiny:

**1. “Browsing a webpage can silently steal your keys”?** A vulnerability of that class is a top-tier weapon on the black market, worth tens of millions of dollars. Anyone actually holding it would go after exchanges and institutions, not spend their days picking off retail players in payment circles. And if it were real, Apple would ship an emergency patch overnight, security firms worldwide would be sounding alarms, and it would be all over the news. Yet this post can produce no CVE number and no report from any security vendor — its entire body of “evidence” is the very screenshot being forwarded from group to group.

**2. “Versions 13–17 were cracked, and now 18–26 are cracked too”?** Translated: every iOS version ever made is compromised and nobody can defend themselves. That isn't analysis, it's intimidation — scare you into feeling it's hopeless, and you'll stop investigating. It even trips over itself: it says version 26 is cracked, then tells you to “upgrade to the latest system without a moment's delay.” If everything is cracked, what exactly are you upgrading to escape?

**3. The post's own story contradicts its “link” theory.** If phone A was infected by clicking a link, how did phone B — a different phone, a different wallet — get drained in the same ten seconds? The only thing the two phones share is their owner: the same batch of “insider apps” installed, the same habit of keeping seed-phrase screenshots in the album. Two wallets emptied ten seconds apart means **the keys to both were already in the thief's hands** — that day was simply cash-out day. This is not the scene of a fresh link infection; it is the scene of a batch harvest. And that is precisely SparkCat's rhythm: scan albums, collect keys, accumulate a batch, then pick a day and strike all at once.

There's even a line in the post that gives the game away without meaning to: “different wallets doesn't mean you're safe.” Correct — but not because some Apple vulnerability has magical reach. It's because **both wallets' seed phrases sat in the same phone's photo album and were scanned out together by the same app.**

**4. Six pieces of “security advice,” five of them pointing outward.** Links, URLs, system versions, Apple IDs, IDs bought online — all of it aims your vigilance at the world outside your phone. The one item that comes close — “some small apps run their business at a loss, but they steal your USDT” — points in the right direction, yet refuses to name a single name. Why not? **Because naming names would mean naming themselves.**

**5. Why is “blame the link” the perfect scapegoat?** Because you open dozens, sometimes hundreds of webpages a day. “Did I click something I shouldn't have?” is a question you can never finish checking and never rule out. So the panic gets somewhere to go: you spend your days paranoid about links and websites, while the actual thief on your phone never spends a single day under suspicion. An explanation that can never be verified explains nothing — but it muddies the water perfectly.

So our call is direct: **posts like this are shill posts.** Every time someone gets drained, the group chats instantly fill with “it was the links” and “it was Apple.” Once or twice is coincidence; every single time is a script. Even if some individual forwarding it means well, the net effect of this talking-point is exactly one thing: you end up suspecting the entire world — except SafeW and SafeX.

To be complete: unfamiliar links do carry real risk — phishing sites that trick you into typing in your seed phrase are an everyday thing, and you should stay careful. But in this string of thefts that Kaspersky actually documented, the channel of attack was the apps themselves. Lock down links all you want; with these apps on your phone, you get robbed anyway.

## 4. Next time one of these posts crosses your feed, run it through three questions

1. **Does it name any specific app?** If it rails against “links,” “vulnerabilities,” and “small apps” but won't produce a single name, it's probably steering the narrative.
2. **Does its “vulnerability” have a CVE number, or a report from any security firm?** Real vulnerabilities come with identifiers and vendor advisories. A “vulnerability” you can't find anywhere is a prop for scaring people.
3. **Does it ever tell you to check what you've installed and what permissions you've granted?** Anyone who actually knows security asks, as their very first question, “what's installed on your phone?”

Fails all three? Treat it as a shill post: don't believe it, don't forward it, don't follow it.

## 5. Already installed these apps — or already been robbed? Do these four things now

1. **Secure the money first.** On a clean device, create a brand-new wallet (brand-new seed phrase) and move everything over. Treat every old wallet as compromised; never put funds back into it.
2. **Clean the album.** Delete every screenshot of seed phrases, private keys, and passwords. From now on, seed phrases go on paper only — no photos, no screenshots, no cloud drives.
3. **Clean the apps.** Check the phone for SafeW, SafeX, Kuaizi Life, Wukong Waimai, Baituo Baituo, and anything else installed because “the group” or “the escrow market” recommended it — revoke their photo and other permissions first, then uninstall.
4. **Move to a hardware wallet (recommended).** The one thing that shill post gets right is “use a hardware wallet.” But only after the first three steps — otherwise you screenshot the new wallet's seed phrase, and you're right back where you started.

Stop staying up all night replaying “which link did I click.” Do these four things first.

## One last line

**The links are taking the blame; the apps are taking your money.**

Next time you see a panic post shouting “never click on any website,” look down at your phone and check what's installed on it first. Full evidence, timeline, and recovery guide: [nosafew.com](https://nosafew.com/).
