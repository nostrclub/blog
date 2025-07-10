---
title: "How to set up NIP-05 on Netlify (like a hacker with a budget) 😎"
date: 2025-07-10
tags: ["NIP-05", "nostr", "netlify", "identity", "lightning"]
---

> Want a custom Nostr identity like `you@nostr.club`?  
> Don’t want to run a server or spend a sat?  
> Here’s how to do it — hacker-style, free on Netlify.

---

## 🧠 What is NIP-05?

NIP-05 lets you connect a Nostr name like `you@yourdomain.com` to your real `npub` (Nostr public key). Think of it like DNS for Nostr — readable and verifiable identities.

Without NIP-05, your identity looks like:

npub1sjlkfjsl...48characterslong


With NIP-05:

you@yourdomain.com ✅


---

## ⚙️ What You Need

- A domain name (like `nostr.club`)
- A GitHub account
- A free Netlify account

---

## 🛠 Step-by-Step Setup

### 1. Create a GitHub repo

Create a new repo, e.g. `nostr-club-verification`. Inside it, make a folder:

.well-known/


Inside that folder, add a file called:

nostr.json


### 2. Write your `nostr.json`

Here’s the format:
<pre>
```json
{
  "names": {
    "yourname": "npub1yourpublickeyhere...",
    "anothername": "npub1anotherkey..."
  }
}
</pre>

✅ This makes yourname@yourdomain.com verifiable.

### 3. Deploy to Netlify
Go to netlify.com, click "Add new site" > "Import from Git"

Choose your GitHub repo

For build command, leave it blank

For publish directory, set:

.well-known

Click Deploy site. Boom. 🚀

### 4. Set up your domain
In Netlify, go to Site Settings > Domain management.
Add your custom domain (yourdomain.com) and verify it.

Also set the root domain to point to Netlify’s DNS — follow their steps.

### 5. Test it
Go to:

https://yourdomain.com/.well-known/nostr.json

It should show your JSON.

Then try verifying on a Nostr client (like Primal.net or Amethyst) by entering:

yourname@yourdomain.com

💸 Budget? What Budget?
This setup is:

✅ Free

✅ Easy to update via GitHub

✅ Works with Netlify’s CDN

No servers. No backend. Just pure static power. 🔥

🧪 Bonus Tips
Add multiple usernames to support friends or a community

Use GitHub Actions to auto-update your file

Redirect /yourname to a Nostr client with Netlify _redirects

/yourname  https://njump.me/npub1yourpubkey  301

🧑‍🎤 Done Like a Hacker
Now you're verified and unstoppable.
NIP-05 on a budget? You nailed it.
Next stop? Zaps, vanity profiles, and global domination.



