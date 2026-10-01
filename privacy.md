---
title: GT-PriceAlert Privacy Policy
---

# GT-PriceAlert Privacy Policy

**Effective date:** 1 October 2026
**Operator and contact:** Huttie (Discord: `Huttie`)

GT-PriceAlert is a free, hobby Discord bot for the game Galactic Tycoons. It is run by one person and is not affiliated with Discord, Galactic Tycoons or its developer. This policy explains what the bot stores, why, and how to have it deleted.

## What the bot stores

When you register with `/register`, the bot saves the following, linked to your Discord user ID:

- **Your Galactic Tycoons API key**, and its access level (Limited or Extended).
- **Your bot settings:** alert threshold, rebuy target, materials you added or removed with `/track`, low-stock alert settings, mute status, and whether ship arrival and contract alerts are on.
- **Alert history needed to avoid repeat alerts:** which price, low-stock and ship-arrival alerts have already been sent, and a snapshot of your open trade contracts (contract IDs, materials, quantities, prices, status and the other company's name).

The bot does **not** store your Discord messages, your in-game password, or payment information. It never asks for any of these.

## What the bot reads from Galactic Tycoons

Using your API key, the bot reads your company's data from the official Galactic Tycoons API: company details, bases, warehouses and stock, production, workforce, ships and their cargo, wishlists, and trade contracts. It also reads public exchange prices and game data. This information is used to work out your alerts and command replies. Apart from the items listed above, it is not kept after each check.

**Access level used:** a Limited key is enough for everything except wishlist changes. With an Extended key, the bot **only** changes your planet wishlists, and only when you run `/restock` or press a restock button. It never accepts, creates or cancels contracts, moves ships, trades, or touches your credits. The Galactic Tycoons API does not allow it to.

## Why the bot uses this data

Only to provide the bot's features to you: price, low-stock, ship-arrival and contract alerts sent to you by Discord direct message, the information shown by its commands, and restocking your wishlists when you ask it to.

## Who the data is shared with

Your data is **not sold, and not shared with anyone for advertising or analytics.** It is only passed to the services needed to run the bot:

- **Galactic Tycoons API:** your API key is sent with each request so the game can return your data.
- **Discord:** alerts and command replies are delivered to you through Discord.
- **Oracle Cloud Infrastructure:** the server the bot runs on.

## How it is stored and protected

Data is stored in a file on a private server that only the operator can access, using SSH key login. API keys are stored **unencrypted** in that file. To limit the risk, use a **Limited** key unless you need `/restock`. You can revoke your key in-game at any time under **Settings → API Keys**, which immediately stops the bot from accessing your account.

The server also keeps technical logs (for example error messages, which may include your Discord user ID). Logs are kept for up to 30 days.

## How long data is kept, and how to delete it

Your data is kept until you delete it. To delete everything the bot has stored about you, run **`/unregister`** in a DM with the bot. This removes your API key, settings and alert history immediately. You can also ask Huttie on Discord to delete it for you. Logs expire on their own within 30 days.

## Age

You must meet Discord's minimum age requirement (at least 13, or older where your country requires it) to use the bot.

## Changes to this policy

If this policy changes, the new version will be posted at this address with a new effective date. If you keep using the bot after a change, the updated policy applies.

## Contact

Questions or deletion requests: **Huttie** on Discord.
