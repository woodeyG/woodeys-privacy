
# Woodeys Place V2 Testing
Thanks for being part of my little project, I hope its of some use to you, it's already proving useful to me as its the one place I can keep everything together. Whether i haev films store on a NAS, blu-ray disc or bought from APPLE TV, i can add everything to a single library, so i know what i have.

## More information
I will post the public testflight link here, if you think anyone else would benefit from using it, please share the link but if you can let me know by popping me an email.

### Contact me
Please email me at: **gundrywoodey@gmail.com** for any questions/issues or use the feedback function of testflight.  

# Setup Guide

Everything you need to get your library set up: connecting a media server, adding films by hand, laying out your seating, stocking the snack list, and sharing the whole thing with someone else.

## Contents

- [Connect a media server](#connect-a-media-server)
  - [Jellyfin](#jellyfin)
  - [Emby](#emby)
  - [Plex](#plex)
  - [If something doesn't go to plan](#if-something-doesnt-go-to-plan)
- [Add films manually](#add-films-manually)
- [Set up your seating](#set-up-your-seating)
- [Set up your snack list](#set-up-your-snack-list)
- [Share your library](#share-your-library)

---

## Connect a media server

Point the app at Jellyfin, Emby, or Plex and it pulls in your films automatically — posters, synopsis, and the Atmos / Dolby Vision / 4K badges read straight from the actual files, no typing required.

This is entirely optional. You can also [add films by hand](#add-films-manually), and the two work together — anything already in your library just gains the server as a location rather than being duplicated.

**Before you start**, you'll need:

- Your server running on your home network
- Its address
- One credential (an API key for Jellyfin/Emby, or a sign-in for Plex)

Set it up in **Settings → Library → Media server**.

### Jellyfin

A key generated once on your server, scoped to this app alone.

1. **Find your server's address** — the address and port Jellyfin is running on. On a NAS, that's the NAS's own address on your network, for example `http://192.168.1.50:8096`.
2. **Generate an API key** — on the Jellyfin web dashboard: `Dashboard → Advanced → API Keys → +`. Give it a name you'll recognise later, and copy the key it gives you.
3. **Connect in the app** — Settings → Library → Media server. Choose **Jellyfin**, paste the address and the key, tap **Connect**.
4. **Choose your libraries and import** — tick the library holding your films (not every library on a server is a film library) and tap **Import**. Films already in your collection aren't duplicated; they simply gain Jellyfin as a location.

**Starting films from your phone.** Jellyfin doesn't play to a device — it sends a command to a client that's already open and listening. Whether that's possible depends entirely on what you watch on:

| Works | Doesn't |
|---|---|
| Kodi, via the Jellyfin for Kodi add-on | Apple TV apps (Swiftfin, Infuse) |
| Jellyfin Media Player | The official Android TV app |

### Emby

Same idea as Jellyfin — a key generated once, scoped to this app.

1. **Find your server's address**, for example `http://192.168.1.50:8097`.
2. **Generate an API key** — `Settings (gear) → Advanced → API Keys → New API Key`. Name it and copy the key.
3. **Connect in the app** — choose **Emby**, paste the address and the key, tap **Connect**.
4. **Choose your libraries and import** — same as Jellyfin: pick your films library and tap **Import**. A film already in your collection just gains a location — nothing is ever duplicated.

**Starting films from your phone.** Emby uses the same session model as Jellyfin, so the same rule applies: whichever client you watch on has to already be open.

| Works | Doesn't |
|---|---|
| Emby Theater | Apple TV apps |
| Emby's web player | |
| Kodi, with the Emby add-on | |

### Plex

No key to find — you sign in on Plex's own site, and pick your server from a list.

1. **Tap "Sign in to Plex"** — Settings → Library → Media server → choose **Plex**. Plex's own page opens in Safari, already showing this app is asking for access.
2. **Approve it** — sign in with your Plex account if you're not already. Your password is only ever typed on Plex's site, never in this app — and you can withdraw access later from `plex.tv → Authorized Devices` without signing out anywhere else.
3. **Pick your server** — the app lists the servers on your account. Tap the one holding your films.
4. **Choose your libraries and import** — tick your films library and tap **Import**. This one takes a little longer than Jellyfin or Emby, since Plex needs one extra request per film to read its Atmos and HDR details — but nothing is duplicated here either.

**Starting films from your phone.** Plex plays through whichever devices are signed in and running, found via your Plex account rather than the server itself.

| Works | Doesn't |
|---|---|
| Apple TV (the Plex app) | Plex in a browser — that's what you cast *from* |
| Kodi, with the PlexKodiConnect add-on | Some smart-TV apps, which can't be driven remotely at all |

### If something doesn't go to plan

**"Couldn't reach the server."** Check your phone is on the same network as the server, and that no VPN is running. A NAS that's gone to sleep looks identical to this — try waking it. On first connection, iOS may ask for Local Network permission — allow it, or the app can never reach anything on your home network at all.

**"The server rejected the key" / sign-in fails.** For Jellyfin or Emby, check the key was copied in full with no extra spaces. For Plex, try signing in again — the code the app shows expires after a few minutes if left too long.

**Some films didn't come in.** A film with no match to an online film database can't be imported — the app tells you how many, and their names. It's almost always a handful of unusual rips or fan edits. Identify them properly on your server, then import again.

**"No player is switched on."** Open your player first — a device that isn't running doesn't appear, on any of the three servers. Then use **Check for players** in Settings to confirm it's found, and choose it if more than one shows up.

**Can I switch servers later?** Yes, any time, from the same screen. Switching doesn't touch your library — every film you've already got stays exactly as it is. It only changes which server the app asks for playback and formats going forward. One server at a time per device; each person in a shared household can point at their own.

---

## Add films manually

You don't need a media server to build a library — anything can be added by hand, whether it's on a shelf, a hard drive, or just something you own.

1. Open the **Library** tab and use the search bar at the top.
2. Search for the film by name — this searches both your existing library and an online film database.
3. On a result you don't already own, tap **Add**.
4. You'll be asked where it actually lives — **Physical Media**, **Apple TV**, your **NAS / Home Server**, or **Other**. A film can have more than one location (on disc *and* streaming, say), so this can be changed or added to later from the film's own page.

If you don't want to commit to owning it yet, tap **Add to wishlist** instead — the same search screen offers both.

---

## Set up your seating

Lay out real seats — rows, a sofa, an armchair — so everyone attending a booking can pick their own spot off a map rather than being assigned one.

Open **Settings → Library → Seating plan → Edit**.

- **Add a row** to create a labelled row of seats (Row A, Row B, …) — each one numbers its own seats automatically (Row A · 1, Row A · 2, and so on). Use the stepper to grow or shrink a row, and the trash icon to remove one.
- **Anything that isn't in a row** — a sofa, an armchair, a beanbag — goes in the list below the rows. Type a name (for example "The Armchair") and tap **Add**.
- A household with no rows at all is completely fine — just add the individual seats you actually have.

Only the library owner can edit the plan; everyone else sees it read-only. Tap **Save** when you're done — changes apply the next time someone books a seat, and don't disturb any booking already made.

---

## Set up your snack list

Choose what the snack picker offers when someone books a film.

Open **Settings → Library → Snack list → Edit**.

- Tap **Add a snack**, give it a name (for example "Popcorn") and pick a symbol to go with it.
- Tap an existing snack to rename it, change its symbol, or **Remove this snack**.
- Tap **Reorder** to drag the list into the order you want it to appear in.

Like seating, this is owner-only to edit and applies the next time someone books — existing bookings keep whatever was picked at the time.

---

## Share your library

One invite shares everything — films, bookings, reviews, and the wishlist — with whoever accepts it. From then on, everyone can add and edit, and changes appear on every phone automatically.

1. On the **Library** tab, tap the two-person icon in the top-left corner.
2. Tap **Share**. The standard iOS share sheet opens — send the invite however suits (Messages, Mail, AirDrop).
3. The other person opens the link, installs the app if they haven't already, and accepts.

That's it — both libraries merge into one, kept in sync by iCloud in the background.

**If something was added before you first shared it and doesn't seem to have come across**, use **Resync existing library to share** on the sharing screen. The normal share covers everything going forward automatically; this is a one-off repair for the rare case where something from before the invite was sent gets missed.

Each person's media server connection — if they've set one up — stays their own. Sharing a library never shares which Jellyfin, Emby, or Plex server it came from; that part is always per-device.
