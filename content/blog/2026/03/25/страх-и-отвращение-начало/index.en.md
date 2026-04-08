---
title: "Fear and Loathing in the IT Industry. The Beginning"
slug: "fear-and-loathing-the-beginning"
date: 2026-03-25T00:00:00+00:00
draft: false
summary: "The only worthy option, I felt, would be to sign up on Habr, get absolutely wrecked, blast through some vibe-coding, and file a report."
categories: ["Technology and Society"]
rubrics: ["Invisible Threads"]
tags: ["AI", "ИИ"]
---

> *He who makes a beast of himself gets rid of the pain of being a man.*
>
> — Dr. S. Johnson

I was somewhere near waking — on the edge of a sleep that no longer held any dreams — when it all went sideways.

I remember: October 2025, Saturday morning. Suddenly alerts started swarming me from every direction like a flock of bats. Someone was trying to get into the network through my service, and couldn't. The network had gone down — which meant it was time for me to get up.

The first few steps I usually take while holding the wall. Then the vestibular system kicks in — and I can walk, though still unevenly. Sounds not great — I know. Might just be age.

Each step brings the familiar pain — a thousand needles in a damaged foot. I take the long way round to the kitchen, put on coffee. By this point the muscles have come together, gathered the foot, and started working — it feels like putting on an exoskeleton. The pain doesn't disappear, it just recedes somewhere deeper — and by now I can walk in a straight line.

I brew the coffee, boot up the laptop. My fingers reflexively find the ridges on the keyboard and start hitting keys. Brain hasn't turned on yet. I stare blankly at the monitor.

And then an idea arrives. What if I gave the agent SSH access? Let's see what happens.

I'd always done this kind of thing by hand before, but today is Saturday! The coffee is hot, and the injectors in my head aren't warmed up yet. There was enough cortisol to drag me out of bed, but orexin still hadn't decided whether to declare it morning.

I hand the agent the server keys — and become an observer.

Over the next 15 minutes the agent runs a full diagnostic: queries everything it can, reads the logs, thinks — and summarizes: "Hm, yeah — it's not working." Then it notices the server is running inside a container, goes in, and finds that Xray is crashing on startup. Infrastructure fine, container alive — but the service itself won't come up.

It opens the Xray logs: config error. TLS certificate not specified. I'd removed it the day before for experiments — and, naturally, forgot to put it back. Now the broken config is failing the server on startup.

— Just nuke that config and be done with it.

The agent gets to work, sleeves rolled up. Nukes it. Restarts the container. No effect.

Long pause. Then a verdict: "It looks like your config is loaded from the database on container startup. As your attorney, I advise you to get in there and delete the damn thing."

I mumbled something like:

— I'm feeling a bit out of it; maybe you should drive...

The agent thinks. Then it goes into the database with its SQL queries, does something in there, and says: "Done."

Restarted. And just like that — everything works. Life is good again!

---

The takeaway is simple: it did exactly what I would have done. Except I would have spent a couple of ~~days~~ hours on it — googling, appealing to the heavens, brain periodically boiling over.

It handled it in 15 minutes. And also wrote a guide — what to do if it all falls over again. And me? I just sat there, drank my coffee, and pressed Enter.

That was my first experience giving an agent network access with server keys. At the time, I didn't yet understand that this was how it would always be from now on.

---

*Continued: Part 1 — Anamnesis*
