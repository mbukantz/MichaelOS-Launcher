# MichaelOS Launcher

[Open MichaelOS](https://mbukantz.github.io/MichaelOS-Launcher/) · [Download the approved icon](michaelos-app-icon.png?v=57f1c0d3b1b2)

## Approved branding

The approved shield has centennial-blue outer trim and a solid ivory (#F5EBDD) background. The artwork content version is `57f1c0d3b1b2`. The loading mark, browser favicon, Apple touch icon and manifest icons are generated from the full-resolution approved master in `mbukantz/MichaelOS`. Existing layout, application target, authentication controls and navigation behavior are unchanged.

From the MichaelOS repository, generate or verify both repositories with:

```sh
python3 scripts/generate-branding.py --launcher ../MichaelOS-Launcher
python3 scripts/generate-branding.py --launcher ../MichaelOS-Launcher --check
```

`favicon-57f1c0d3b1b2.png` provides the same approved 32px artwork at a URL ending in `.png` for Apps Script metadata. Retain older versioned favicon files for existing app releases. Historical comparison PNGs remain available at their original download URLs; they are not used as active app icons.

## iPhone: choose the exact image with Shortcuts

1. In Chrome, open [the approved icon](michaelos-app-icon.png?v=57f1c0d3b1b2), press and hold it, and save it to Photos.
2. In Shortcuts, create a shortcut named **MichaelOS**.
3. Add a **URL** action with this address, followed by **Open URLs**:

```text
googlechromes://script.google.com/macros/s/AKfycbyrW9FGCk2c4Hx51qH5Mbkmi9Nt2eibY1ubFZ66xzxAzgZDgq5PjNMTcQixt-4R03qz1Q/exec
```

4. Open the shortcut’s name menu, choose **Add to Home Screen**, tap its icon, and choose the saved shield from Photos.
5. Tap **Add**. The address opens MichaelOS directly in Chrome and remains valid through app updates. A custom shortcut photo does not automatically refresh when the website’s artwork changes.

Chrome also offers **Share → Add to Home Screen** from the launcher URL. Existing iOS installations may retain an older icon; Shortcuts provides explicit image selection.

## Google sign-in and the embedded launcher

The launcher embeds the existing Apps Script application. Its **Initialize MichaelOS** and **Open directly instead** controls open Google in the top-level browser when an embedded session is unavailable. Complete Google sign-in as needed. Embedded access depends on the browser’s cookie/session behavior; this branding update does not change it. The Shortcuts address above opens the app directly rather than depending on the launcher iframe.

## Publication order

Merge and verify the launcher’s GitHub Pages publication before releasing the matching MichaelOS branding PR. The app’s merged commit must pass its required validation and publish to Preview before the owner runs a fresh **Test & Deploy**. Merging the app PR alone does not deploy production.
