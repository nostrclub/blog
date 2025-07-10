---
title: "What is a NIP-05 and Why Do We Even Care?"
date: 2025-07-09
tags: ["nip-05", "identity", "decentralization"]
categories: ["Guides"]
---

> `coffee@nostr.club` looks more human than `npub1xyzq3...`, doesn’t it?

Welcome to the world of **NIP-05** — the protocol that gives your Nostr identity a face, a name, and a story.

---

## 🧠 Okay... What *is* NIP-05?

**NIP-05** is a [Nostr Improvement Proposal](https://github.com/nostr-protocol/nips/blob/master/05.md)  
It links your long Nostr public key (`npub...`) to a human-readable name like:

you@yourdomain.com


Or, if you’re on the right side of the internet:
coffee@nostr.club


This makes your profile:

- **Searchable**
- **Recognizable**
- **Zappable**

Instead of being a cryptographic hash in the void, you’re now an actual person people can interact with.

---

## 🤔 Why Should Anyone Care?

Here’s why NIP-05 matters:

### ✅ It’s Portable Identity
Your NIP-05 can live on **any domain you control**. It’s yours — not owned by a platform.

### ✅ It’s Social Proof
Clients like **Primal**, **Damus**, and **Amethyst** display NIP-05 badges to show “this person is verified at their domain.”

It's like an old-school verified check... but self-hosted.

### ✅ It’s Zap-Friendly
People are more likely to zap:
coffee@nostr.club
than
npub1xx934a...d9f9af2

Because humans like names, not hashes.

---

## 🔍 Behind the Scenes: How It Works

Clients (like Primal) ask your domain for:

https://yourdomain.com/.well-known/nostr.json


And they expect to find something like this:

<pre>
{
  "names": {
    "coffee": "npub1xyz..."
  }
}
</pre>

That’s it. Static JSON = portable identity.

No blockchain. No database. Just a file.

---

## 🧠 But What’s the Catch?

It’s not encrypted. Anyone can see who’s linked to what.

It’s centralized to a domain (unless you decentralize your hosting)

It’s opt-in — not everyone uses it, which is fine.

NIP-05 isn’t perfect. But it’s damn useful.

---

## 🌍 Why We Like It at nostr.club

Because we believe:

Your name shouldn’t belong to someone else’s platform.

NIP-05 is about taking that name back,
making it yours, and
using it how you want — with zaps, with presence, with style.

TL;DR
Without NIP-05	With NIP-05
npub1x9xq...	you@nostr.club
no search	search in clients
less zappable	more human

Want one? You don’t need to ask permission.
You just need a domain and a .json.

This is Nostr.
You own it.

---

## ✅ Ready to use

- Copy → paste into `content/posts/what-is-nip05.md`
- Netlify will auto-deploy
- You’ve now got an **opinionated, educational, and legit first blog post**

Let me know if you want me to follow up with post #2:
> 👉 [How to set up NIP-05 on Netlify (like a hacker with a budget) 😎](/blog/nip05-on-netlify/)

