# Focus Gate

Blocks these sites the entire time the extension is enabled — no popup, no on/off switch inside it. Enabling/disabling the extension itself in Chrome *is* the switch.

- youtube.com (+ youtu.be)
- instagram.com
- delugerpg.com
- slither.io
- deadshot.io
- krunker.io

## Install (Chrome / Edge / Brave)

1. Unzip this folder somewhere permanent — don't delete it after installing, Chrome reads from it directly.
2. Go to `chrome://extensions`.
3. Turn on **Developer mode** (top-right toggle).
4. Click **Load unpacked** and select the `focus-gate` folder.
5. Done. The blocklist is active immediately. Visiting any of the sites above redirects to a "blocked" page instead.

## To pause or stop blocking

Go back to `chrome://extensions` and either toggle the extension off, or remove it. There's no in-page way to disable it — that's intentional.

## Editing the blocklist

Open `rules.json`. Each entry blocks one domain. To add a site, copy a block and change:
- `id` — must be a unique number
- `urlFilter` — `"||example.com^"` blocks `example.com` and all its subdomains
- the `site=` value in `redirect.extensionPath` — just the label shown on the blocked page

Save the file, then hit the refresh icon on the extension's card at `chrome://extensions` for the change to take effect.
