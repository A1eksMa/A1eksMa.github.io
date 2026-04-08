---
title: "The AI Sysadmin"
slug: "the-ai-sysadmin"
date: 2026-03-24T00:00:00+00:00
draft: true
summary: "October, Saturday morning. VPN down. Coffee hot, brain not yet — and for the first time I gave an agent SSH access."
categories: ["Author's Perspective"]
rubrics: ["Point of Origin"]
tags: ["new", "AI", "ИИ", "инфраструктура"]
---

October 2025. Saturday morning. I wake up to a message in the chat: everything's gone. The VPN is down.

I head to the kitchen, brew coffee. While it's still hot — I open the laptop. Motor skills are slowly waking up, brain hasn't yet. I stare blankly at the monitor.

And then an idea: why not bring in an agent? I'd always done this kind of thing by hand before, but today — it's Saturday, it's morning, there's coffee, and my head hasn't switched on yet. I give it SSH access. Let's see what happens.

After that, I just watched.

Over the next 15 minutes, the agent ran a full diagnostic: queried everything it could, read the logs, thought it over — and summarized: "Hm, yeah, it's not working." Then it noticed the server was running inside a container, went in, found that Xray was crashing on startup. Infrastructure fine, container alive — but the service itself wouldn't come up.

It opened the Xray logs: config error. TLS certificate not specified. I'd removed it the day before for some experiments — and, naturally, forgot to put it back.

I said: just delete that config, to hell with it.

Deleted. Restarted the container. No effect.

It paused. Then: "Your config is loaded from the database on container startup. Can I go in and remove it?"

— Sure, go ahead.

It went into the database with its SQL queries, did something in there. "Done." Restarted. And just like that — everything works.

Life immediately improved. VPN up, the kids are back on YouTube.

The takeaway is simple: it did exactly what I would have done. Except I would have spent a couple of days on it — googling, appealing to the heavens, brain overheating periodically. And running into "access denied" from Roskomnadzor, because even Habr has taken down everything related to Project X by now.

It handled it in 15 minutes. And also wrote a guide — what to do if it all goes down again. And me? I just sat there, drank my coffee, and pressed Enter.
