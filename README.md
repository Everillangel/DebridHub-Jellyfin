# DebridHub — Jellyfin plugin repository

Install source for the **DebridHub** Jellyfin plugin (stream & batch-download from Real-Debrid / AllDebrid, Torznab search, watchlist, Seerr/Jellyseerr request webhook, and a library organizer).

This repository hosts only the plugin **manifest** and **release binaries** — no source. It exists so Jellyfin can install and auto-update the plugin from a repository URL, without touching your container.

## Install

1. In Jellyfin: **Dashboard → Plugins → Repositories → +**
   - **Name:** `DebridHub`
   - **URL:**
     ```
     https://raw.githubusercontent.com/Everillangel/DebridHub-Jellyfin/main/manifest.json
     ```
2. **Dashboard → Plugins → Catalog → DebridHub → Install**
3. **Restart Jellyfin.** DebridHub then appears under Plugins (Active) with a settings page.

Requires **Jellyfin 10.10 or newer**.

## After installing

Open **Dashboard → Plugins → DebridHub** and set your debrid API key, the stream/download library folders, and (optionally) your Jackett Torznab URL and Seerr webhook. See the settings page descriptions for details.

## Releases

Each version's plugin package (`debridhub_<version>.zip`, containing the plugin DLL + `meta.json`) is attached to the matching [GitHub Release](../../releases). The `manifest.json` in this repo lists every published version with its checksum; Jellyfin uses it to offer in-app updates.
