---
title: "The Procedure: a bureaucratic horror game"
date: 2026-03-18
draft: false
tags: ["the-procedure", "game-dev", "bureaucracy", "horror"]
---

I've just released a small browser game called **The Procedure**. It's a bureaucratic horror piece where you play as a clerk processing citizen cases in a dystopian administrative system. Each day you must decide which cases to escalate—knowing that escalation means disappearance—and which to close, erasing the person from the records. The game is intentionally dry, monotonous, and suffocating, because that's the point.

You can play it here: [https://jmiller.social/projects/the-procedure](https://jmiller.social/projects/the-procedure). It's free, runs in any modern browser, and takes about 10-15 minutes to complete once.

## Why this game

Bureaucracy is a soft horror. It doesn't scream; it whispers in triplicate. The terror isn't in monsters or jumpscares, but in the slow, predictable machinery that grinds people into paperwork. The Procedure tries to capture that feeling—the weight of a decision that feels like just another checkbox, but carries a human cost you're never allowed to see.

The mechanics are simple: you read case descriptions, you choose whether to escalate or close. Escalation makes your compliance score go up; closing cases lowers it. If your compliance drops too low, you're reassigned—game over. So you're trapped between preserving your own position and sparing the faceless citizens on your screen. The horror is structural, never stated.

## Technical notes

The game is built with vanilla HTML/CSS/JavaScript, no frameworks. The audio is procedural Web Audio API: a 50Hz electrical hum with harmonics, keystroke clicks every third character, and two ascending notes for routing confirmation. The code is on GitHub under AGPL-3.0, the content under CC BY-NC-SA 4.0.

## Reflections

Making this felt like building a small, precise trap. The challenge wasn't writing dramatic prose, but removing drama—letting the bureaucratic language do the work. The most chilling lines are the driest: "housing reassignment without request", "identity record duplicates", "unregistered children". They're real things that happen in real systems, just stripped of context and empathy.

That's the core of the horror: when people become entries in a database, and morality becomes a compliance metric.

If you play it, let me know what you think. And if you work in any kind of administration… maybe take a break afterwards.
