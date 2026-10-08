---
title: GT-PriceAlert Privacy Policy
---

# GT-PriceAlert Privacy Policy

**Effective date:** 8 October 2026
**Operator and contact:** Huttie (Discord: `Huttie`)

GT-PriceAlert is a free, hobby Discord bot for the game Galactic Tycoons. It is run by one person and is not affiliated with Discord, Galactic Tycoons or its developer. This policy explains what the bot stores, why, and how to have it deleted.

## What the bot stores

When you register with `/register`, the bot saves the following, linked to your Discord user ID:

- **Your Galactic Tycoons API key**, and its access level (Limited or Extended).
- **Your bot settings:** your global alert threshold and any per-material alert rules you set with `/threshold material` (a percentage, or the prices you chose), rebuy target, materials you added or removed with `/track`, low-stock and repair alert settings, whether price, ship arrival, contract, research and auction alerts are on, your listing undercut alert settings, your alert style (detailed or compact), and mute status.
- **Alert history needed to avoid repeat alerts:** which price, low-stock, repair and ship-arrival alerts have already been sent (including the IDs of buildings already reported for repair), a snapshot of your open trade contracts (contract IDs, materials, quantities, prices, status and the other company's name), your technology levels at the last check, so finished research can be spotted, and, if auction alerts are on, the ID of the newest cash history entry already checked, when you turned auction alerts on, and the IDs of the executives in your roster, so only new auction activity and new executives get a DM, and, if listing alerts are on, the lowest competing price last reported for each of your undercut products.

Separately, for bases that produce something they also use, the bot keeps **running averages of how much of each material the base makes and uses per hour**. These are stored by base ID and material, together with when they were last updated. They aren't stored with your Discord ID or API key, but they do describe your bases' production.

While it's running, the bot also keeps some short-lived data in memory only, such as each building's last production task, your base and ship names for command suggestions, and recent exchange prices. This is never written to disk, and is cleared whenever the bot restarts.

The bot does **not** store your Discord messages, your in-game password, or payment information. It never asks for any of these.

## What the bot reads from Galactic Tycoons

Using your API key, the bot reads your company's data from the official Galactic Tycoons API: company details, technology levels, bases, buildings and their condition, warehouses and stock, production, workforce, ships and their cargo, wishlists, trade contracts, and your exchange listings. If auction alerts are on, it also reads your cash history (your exchange, contract and auction transactions) and your executive roster. It also reads public exchange prices, order books, daily price history and game data. This information is used to work out your alerts and command replies. Apart from the items listed above, it is not kept after each check.

**Access level used:** a Limited key is enough for everything except wishlist changes. With an Extended key, the bot **only** changes your planet wishlists, and only when you run `/restock` or `/repair wishlist`, or press a restock or repair button. It never accepts, creates or cancels contracts, moves ships, trades, or touches your credits. The Galactic Tycoons API does not allow it to.

## Why the bot uses this data

Only to provide the bot's features to you: price, low-stock, repair, ship-arrival, contract, research, auction and listing alerts sent to you by Discord direct message, the information shown by its commands, and updating your wishlists when you ask it to.

## Who the data is shared with

Your data is **not sold, and not shared with anyone for advertising or analytics.** It is only passed to the services needed to run the bot:

- **Galactic Tycoons API:** your API key is sent with each request so the game can return your data.
- **Discord:** alerts and command replies are delivered to you through Discord.
- **Oracle Cloud Infrastructure:** the server the bot runs on.

## How it is stored and protected

Data is stored in files on a private server that only the operator can access, using SSH key login. API keys are stored **unencrypted**. To limit the risk, use a **Limited** key unless you need `/restock` or `/repair wishlist`. You can revoke your key in-game at any time under **Settings → API Keys**, which immediately stops the bot from accessing your account.

The server also keeps technical logs (for example error messages, which may include your Discord user ID). Logs are kept for up to 30 days.

## How long data is kept, and how to delete it

Your data is kept until you delete it. To delete everything the bot has stored about you, run **`/unregister`** in a DM with the bot. This immediately removes your API key, settings, alert history and your bases' production averages. If your key has already stopped working, the bot can't look up which bases are yours; their production averages are then deleted automatically within 7 days. Production averages for a base are also deleted automatically if they haven't been updated for 7 days. You can also ask Huttie on Discord to delete your data for you. Logs expire on their own within 30 days.

## Age

You must meet Discord's minimum age requirement (at least 13, or older where your country requires it) to use the bot.

## Changes to this policy

If this policy changes, the new version will be posted at this address with a new effective date. If you keep using the bot after a change, the updated policy applies.

## Contact

Questions or deletion requests: **Huttie** on Discord.
