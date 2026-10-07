---
title: GT-PriceAlert Changelog
---

# GT-PriceAlert Changelog

Versions follow `major.minor.patch`: a new **major** version means something that worked before has changed (e.g. a command was renamed), a **minor** version adds features, and a **patch** fixes bugs.

## 2.3.0 — 7 October 2026

- **New:** `/listingalert on|off|status` — a DM when one of your exchange listings is meaningfully undercut. To avoid spam it only counts when someone is at least 2% cheaper **and** others have listed at least 10% of your remaining amount below your price (both adjustable). You get one DM per undercut, and another only if the price keeps dropping; it resets once you're cheapest or tied again. Checked every 20 minutes, grouped into one DM.
- `/alertstyle` has a new *Listings* type.
- Privacy Policy updated.

## 2.2.0 — 7 October 2026

- **New:** `/listings` — your exchange listings per product, next to the cheapest price other sellers are asking: 🟢 you're cheapest, 🟡 tied, or 🔴 undercut (by how much, with the Federal Reserve marked). Also shows how much is left and sold, how much others have listed below your price, the average price, and the total value of your listings. Undercut products are listed first.

## 2.1.0 — 7 October 2026

- **New:** `/auctionalert on|off` — DMs for the new Executive Auction House: when you're outbid (bid refunded), win an auction (unused bid refunded), an executive you listed sells, and when a new executive joins your roster. Checked every 30 minutes. The game's API has no auction endpoints yet, so the bot reads these from your cash history and roster: amounts and companies are shown, executive names only for new arrivals.
- **New:** price alerts show 30-day price history: the range of daily average prices, and a note like "lowest in 12 days" when the current price beats every recent day.
- `/alertstyle` has a new *Auctions* type.
- Privacy Policy updated.

## 2.0.0 — 5 October 2026

**⚠️ Breaking change:** `/threshold percent:10` has been replaced by `/threshold global percent:10`.

- **New:** `/pricealert on|off` — price alerts can now be turned on and off like the other alerts (on by default).
- **New:** `/threshold material` — your own alert rule per material: a percentage from its average, or fixed prices (alert at or below / at or above a price in cr). Fixed prices also work for materials with no average price yet.
- **New:** `/threshold reset` and `/threshold status` to remove or list per-material rules.
- Price alerts now show which rule triggered them, and `/prices` marks materials with their own rule (🎯).
- `/help` shows which version of the bot is running.
- Privacy Policy updated for the new settings.

## 1.6.0

- **New:** `/help` — how to use the bot, by topic, with a personal setup checklist showing what's on and what to set up next.
- **New:** first-time `/register` now ends with a short "next steps" guide.
- **New:** `/alertstyle` — choose detailed cards or compact one-line alerts, for all alerts or per type. In compact mode, price alerts from one check are combined into a single message.
- **New:** `/track status` lists materials you've added or removed by hand; `/track reset` puts a material back to automatic.
- **Fixed:** `/track` couldn't pick a material whose name is part of another's (e.g. *Iron* vs *Iron Ore*). An exact name now wins, the field suggests materials as you type, and material ids work too.

## 1.5.0 — 2 October 2026

- **New:** `/researchalert on|off` — a DM when a research project finishes.
- `/unregister` now also deletes your bases' production averages.
- Privacy Policy and Terms updated.

## 1.4.1 — 2 October 2026

- **Fixed:** false low-stock and restock alerts for materials a base makes for itself (e.g. Cohesilite for Apex Prefab Kits). Buildings switch between recipes from batch to batch, so the bot now compares production with use as running averages over several batches (longer for slow recipes) instead of a single snapshot. The averages survive restarts.

## 1.4.0 — 2 October 2026

- **New:** `/repair` — puts the materials needed to repair a base's buildings on its planet wishlist, minus stock already there or on its way. Options: `base`, `percent` (only buildings at or under a condition) and `duration` (plan ahead for wear).
- **New:** `/repairalert on|off` — a DM when buildings drop under a condition (default 80%, where output starts to drop), with a Repair button per base.
- Repair costs are checked against the in-game repair screen on Tier 2 and Tier 4 planets. Totals for many buildings at once can be 1–2% above the game's figure.

## 1.3.0 — 2 October 2026

- **New:** chain production. A base that makes something it also uses is no longer told to buy it. `/watchlist` lists such materials as made in-house.
- **New:** `/restock` options `duration` (a different period for one run) and `weight` (scale the amounts to a cargo weight, or pick a ship to use its real cargo capacity).
- `/restock` option `amount` replaced by a simpler `full` on/off switch.

## 1.2.0 — 1 October 2026

- **New:** price alerts show the exchange order book: the cheapest prices and how much is listed at each, how much is listed below average, the Federal Reserve price, and what buying your shortfall would really cost.
- **New:** two restock buttons on price and low-stock alerts: **Fill up** (to your target) and **Full** (a whole rebuy period).

## 1.1.0 — 1 October 2026

- `/arrivalalert` renamed to `/shiparrivalalert`.
- `/watchlist` grouped into recipe inputs, workforce consumables and products, sorted alphabetically.

## 1.0.0 — 1 October 2026

- **Terms of Service and Privacy Policy published.** The bot is ready to share publicly.
- **New:** `/contracts` — your open trade contracts and anything stopping them from going through.
- **New:** `/contractalert on|off` — DMs for new offers, accepted, completed or cancelled contracts, contracts that become blocked, and recurring contracts about to expire.

## 0.8.0 — 30 September 2026

- **New:** API budget handling. The bot tracks each key's 500 points per 10 minutes, pauses instead of going over, and DMs you when you're running low. Exchange prices are cached and shared.

## 0.7.0 — 30 September 2026

- **New:** `/ships` — where each ship is or is heading, arrival time, cargo and fuel.
- **New:** ship arrival DMs, sent at the actual arrival time.
- Restocking now counts cargo already on ships heading to a base.

## 0.6.0 — 30 September 2026

- **New:** `/mute` — pause all alert DMs, until turned off or for a set time.
- **New:** `/restock` can target one base (with autocomplete).
- **New:** price alerts for what you produce: sell signal when the price is high, price drop when it's low.

## 0.5.0 — 30 September 2026

- **New:** workforce consumables (food, water, tools…) are tracked alongside recipe inputs.
- **New:** `/warehousealert` — a DM when a base is running low on something it uses.

## 0.4.0 — 30 September 2026

- **New:** `/restock all` and `/restock discounted` — set each base's planet wishlist to exactly what it's missing.
- **New:** an "Add to wishlists" button on price alerts.
- The bot detects whether your key is Limited or Extended, and explains what's needed for wishlist features.

## 0.3.0 — 30 September 2026

- **New:** alerts show your stock per base and how long it lasts.
- **New:** `/rebuy` — set how much stock to keep; alerts show how much to buy and what it costs.
- **Fixed:** production in progress wasn't read correctly from the game's API.

## 0.2.0 — 28 September 2026

- **Multi-user:** everyone registers their own key with `/register` (DM only; a key posted in a server channel is refused) and gets alerts by DM. `/unregister` deletes your data.
- Hosted around the clock on its own server.

## 0.1.0 — 28 September 2026

- First version: price alerts for the materials your production uses, when a price moves more than a set percentage from its average.
- Commands: `/prices`, `/watchlist`, `/threshold`, `/track`, `/refresh`.
