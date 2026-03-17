---
title: "Nier: Automata ver1.1.a"
slug: "nier-automata-ver1.1.a"
date: 2026-03-15T00:00:00+00:00
draft: false
summary: "A story about how an AI suggested writing a neural network using an AI. Absurdity squared — and one dot that changed everything."
categories: ["Technologies and Society"]
rubrics: ["Horizon Line"]
tags: ["AI", "neural network"]
---

An acquaintance of mine dreamed of getting rich trading stocks. One day, while discussing winning trading strategies with an AI, he received advice to use linear approximation via the least squares method to calculate trend lines, and to use pandas for handling large volumes of data — stock indices and share prices. And, the cherry on top: the AI suggested he build a neural network to predict results based on previous trading sessions.

My friend understood perhaps half of those words, but he firmly believed that AI wouldn't steer him wrong — and he knew I was working on something similar, so he came running to me with this immediately. At the time I was right in the middle of a six-month Data Analysis course: Python, pandas, SQL, and so on.

He knew who to turn to. The idea hooked me — an AI giving advice to write a neural network. And to push the surrealism further, I decided to write the neural network *using* an AI. Absolute absurdity squared — exactly the kind of thing I love most.

I gave the AI a detailed prompt (this was ChatGPT 2 or 3 — back when we still worked with prompts), ran it several times, and got several different solutions. Not one of them worked.

I went through each version line by line — and here's what I saw. The task was standard, but had no single idiomatic solution. There was clearly something similar in the training data — the code looked realistic. But it was written as if by a C-student who didn't understand what they were doing, yet diligently copied from A-students: part of a function from one source, part from another.

I remember sharing my first impressions in our work chat. Verbatim, original spelling preserved:

> *Guys, I read over lunch what ChatGTP wrote for us, and I am [impressed beyond words]. It didn't just do everything I asked. It did more, and did things I hadn't even thought of or accounted for. And it did it better than I would have!*

But I'd only read the first function.

> *Checked the second part. I take it all back. ChatGPT is a dumb animal. Feels like it just scraped code from the internet and threw it all together. It repeated the same action three times in different ways.*

Also me. Twenty minutes passed between those two messages.

We fed the AI the same spec twice, with different levels of detail, and each time got roughly the same output with minor variations. Like asking two different people to do the same thing — the result is identical, but the style and handwriting differ. The sigmoid function, for instance: one version used `math` as a standalone function, the other used `numpy` inline in the body.

---

The problem turned up in the last function — `feed_forward`, which computes neuron values during the forward pass. Here's what ChatGPT produced:

```python
def feed_forward(inputs, layers, weights):
    layers[0] = inputs
    for i in range(len(weights)):
        weights_i = np.array(weights[i])
        layers_i = np.array(layers[i])
        dot_product = np.dot(weights_i, layers_i)  # ← here
        layers[i+1] = 1 / (1 + np.exp(-dot_product))
    return layers, weights
```

Looks plausible. But it crashes.

The issue is that the weight matrix `weights[i]` is stored in shape `(n_in, n_out)` — for each input-layer neuron, a list of weights to each neuron in the next layer. The vector `layers[i]` has shape `(n_in,)`. The operation `np.dot(weights_i, layers_i)` tries to multiply `(n_in, n_out)` by `(n_in,)` — the dimensions don't match. You need to transpose the matrix: `weights_i.T` gives shape `(n_out, n_in)`, and then `(n_out, n_in) × (n_in,) = (n_out,)` — everything lines up.

The fix is one dot and one letter:

```python
def feed_forward(inputs, layers, weights):
    layers[0] = inputs
    for i in range(len(weights)):
        weights_i = np.array(weights[i])
        layers_i = np.array(layers[i])
        dot_product = np.dot(weights_i.T, layers_i)  # transpose the weight matrix
        layers[i+1] = 1 / (1 + np.exp(-dot_product))
    return layers, weights
```

After that, the network worked — and, more importantly, worked *correctly*.

> *"Upd: I figured it out, tweaked the ChatGPT code a bit, and now it works. And not only does it work, it works correctly."*

Our work was complete, and I announced it to the chat accordingly:

> *"OFFICIALLY NOTIFYING EVERYONE!!! Work on the neural network code is done. At this stage we can: create fully connected neural networks with any number of layers and neurons, and train them. [...] Thanks to ChatGPT for the work done (even though it's a C-student and I had to correct it CONSTANTLY). Thank you all for pulling me into this! Glory to Humanity!"*

I named the neural network **nier** — at the time I was deep into the newly released anime series [Nier: Automata Ver1.1a](https://en.wikipedia.org/wiki/Nier:_Automata_Ver1.1a). The story unfolds in the year 11945. Androids wage war against machine lifeforms — none of them remember why anymore. The war is utterly meaningless, because humanity, for whose sake it was fought, has long been extinct.

But this stunning story isn't only about androids. The series is full of profound questions: about the origins of culture, consciousness, religion, civilization. Questions that have refused to let go of generations of serious science fiction authors.

I consider it significant that this series came out precisely when the wave of AI hype was just beginning to crest. Two and a half years have passed since then — and every day we inch closer to technological singularity. The Turing Test has already been passed. Giving a clear answer to where the boundary lies between human consciousness and machine forms of life grows harder with each passing day. What is consciousness? What is the soul? What separates the living from the non-living? Can a machine feel, love, suffer, lose its mind — or is all of it just precise imitation, a mirror in which we see only ourselves? The questions posed in that series are now appearing in news feeds — and growing more urgent by the day.

I don't know whether copies of us will live on in androids after humanity is gone — but my neural network, written by an AI that was advised by an AI to write a neural network, will definitely live on on [GitHub](https://github.com/A1eksMa/nier). Specifically for this post, I dusted it off, packaged it as a Python library, and added examples using classic ML datasets — Iris flower classification, Celsius to Fahrenheit conversion, and tic-tac-toe winner prediction.

Unfortunately, we never did become fabulously wealthy stock traders. Trained on a dataset of stock indices, my neural network can predict price quotes. That's mathematics — not magic. But predicting *real* stock prices on an actual exchange? That, sadly, it cannot do.

Glory to Humanity!
