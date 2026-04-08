---
title: "All In MAX"
slug: "all-in-max"
date: 2026-03-09T00:00:00+00:00
draft: false
summary: "On the irony of running a private network project's channel inside a messenger that actively detects VPN usage."
categories: ["Technology and Society"]
rubrics: ["Digital Borders"]
tags: ["communications", "telegram", "MAX", "privacy", "security"]
---

In an earlier post I was already mulling over the idea of moving from Telegram to MAX — or at least opening a channel there to mirror our cozy Telegram content. Given the ongoing restrictions on Telegram in Russia, having a backup platform for project news seems like a reasonable precaution.

On one hand, logic suggests it: stable, domestic platform, Russian-speaking audience... On the other hand, running a channel in MAX for a project dedicated to building secure private networks is, to put it plainly, **MAX**imally strange. Because **MAX** isn't just a messenger — it's also a rather specific tool for detecting network nodes that use VPN to bypass regional restrictions.

As a recent study showed, **MAX** makes requests to foreign IP-detection services and even to competitor domains like Telegram and WhatsApp. Naturally, this raised a few questions.

The official response from the **MAX** developers was predictable: no surveillance, just technical necessity. All those "foreign trips" are explained by WebRTC for voice and video calls, and by the need to verify push notification delivery under "complex network conditions."

The facts in the study, however, tell a different story. Collecting your device's IP address from multiple parallel sources is more characteristic of checking whether your device is using a VPN. Modern client devices that use censorship circumvention often rely on **multipath routing** or **selective proxying** to conceal this. Some traffic — say, access to Russian sites — goes out directly, while traffic bound for foreign resources is routed through a VPN. Querying multiple IP-detection services in this scenario will return different results from different services routed under different rules — a fairly unambiguous marker of VPN usage.

Similarly, reaching out to competitor addresses that are blocked in Russia amounts to probing the network environment and flagging that blocked resources are reachable. So **MAX** has built-in mechanisms aimed squarely at identifying user devices that use VPN for traffic routing, and at detecting the network nodes involved.

Of course, you could turn to third-party apps built on its open API. These clients generally offer less reliability and reduced functionality — though functionality trimmed in the right places is exactly what we need here. The official MAX team fights these alternatives and warns users against them, citing potential security risks (though given the recent scandal over user media files — who are they to lecture anyone about security; Habr link: [source](https://habr.com/ru/news/1007576/)) and the usual reduced reliability disclaimers. The messenger's motivation here is understandable.

Amusingly, the same access pattern is now actively spreading among Telegram users too (the "Telega" app, for instance). The original messenger's attitude toward its clones is similar — but the user motivation is the polar opposite. MAX users turn to clones to escape surveillance built into the official app; Telegram users turn to clones precisely because the official app is blocked, and the clones give them full functionality through the censorship wall. Oh, these complicated times we live in!

Good news: you can still uninstall MAX (for now, at least). Though some users may already face friction: devices are going on sale with MAX mandatory pre-installed. Physically removing pre-installed apps is possible but may require some technical know-how — similar to trying to strip Google apps from Android. In most cases you may not even need full removal — disabling the app in the system installer might be enough. Just watch your hands: after an update you might find that the deleted app, service, or daemon is back and active.

Bad news: MAX is just one component of this system. The tip of the iceberg. And you cannot guarantee that similar functionality isn't baked into other apps on your device — Yandex services, Gosuslugi, or your domestic banking app.

So there's no point trying to avoid the inevitable. And however **MAX**imally cringe it may be — the **Sigil Gate** channel is now available. In MAX too.

P.S. If you want to dive into the details of this "digital drama," the original Habr articles are [here](https://habr.com/ru/articles/1006394/), [here](https://habr.com/ru/articles/1006666/), and [here](https://habr.com/ru/news/1006950/). A gripping read, I promise.
