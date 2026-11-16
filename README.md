# MichaelOS Launcher — Authentication Bootstrap Test

## Before testing
Deploy MichaelOS 6.5.133.

## iPhone test
1. Push this launcher to the existing `MichaelOS-Launcher` GitHub Pages repo.
2. Remove the old Home Screen MichaelOS launcher.
3. Open `https://mbukantz.github.io/MichaelOS-Launcher/` in Safari.
4. Add to Home Screen with **Open as Web App ON**.
5. Launch the M/B icon.
6. When the standalone launcher shows the 401, wait for the initialization card and tap **Initialize MichaelOS**.
7. Apps Script loads top-level. If Google needs an account/auth step, complete it.
8. The bootstrap page redirects automatically back to the launcher.
9. Check whether embedded MichaelOS now loads instead of 401.

If it still returns 401 after this sequence, the first-party cookie is not being accepted in the third-party iframe context and this iframe architecture is not viable on iOS standalone mode.

Custom M/B Home Screen icons are retained.

## Approved branding

Icons and the 72px loading mark use the approved MichaelOS artwork. Their content version is `6716ae216af6`. Regenerate all sizes from the master in `mbukantz/MichaelOS` using `python scripts/generate-branding.py --launcher ../MichaelOS-Launcher`; add `--check` to verify. Do not edit generated icon sizes independently. Existing Home Screen installs may require removal and re-addition to refresh the installed icon.

The 2026-11-16 approved shield has a transparent exterior, jersey-reference blue, subtle skate texture, stitched border and small puck. Existing loading dimensions and authentication behavior are unchanged.

`favicon-6716ae216af6.png` is the same approved 32px artwork at a versioned filename ending in `.png`. Apps Script uses this direct URL so image-type identification does not depend on parsing a cache-busting query string. Existing launcher favicon/touch links are unchanged.

## iPhone Shortcuts image options

Save one PNG below, then choose it in Shortcuts under **Add to Home Screen → icon → Choose Photo**. Each 512px RGB image composites the approved shield onto a solid background without redrawing it. App and launcher icons retain the approved transparency.

- [Warm ivory — #F5EBDD](michaelos-shortcuts-ivory-6716ae216af6.png)
- [Soft silver — #E6E9EF](michaelos-shortcuts-silver-6716ae216af6.png)
- [Slate gray — #758394](michaelos-shortcuts-slate-6716ae216af6.png)

### Richer shortcut background options

- [Burgundy — #7B2D3E](michaelos-shortcuts-burgundy-6716ae216af6.png)
- [Burnished copper — #A96542](michaelos-shortcuts-copper-6716ae216af6.png)
- [Deep teal — #285F64](michaelos-shortcuts-teal-6716ae216af6.png)

### Three horizontal bands

[Ivory / centennial blue / ivory shortcut icon](michaelos-shortcuts-ivory-blue-stripes-6716ae216af6.png): three approximately equal horizontal bands behind the approved shield. Ivory is #F5EBDD; blue #0B4F9E is the median of the approved shield’s blue field. The download is a 512px RGB PNG for Shortcuts.

### Outer centennial-blue outline

[Striped shortcut icon with outer centennial-blue outline](michaelos-shortcuts-blue-outline-stripes-6716ae216af6.png) · [Transparent outlined shield](michaelos-shield-blue-outline-6716ae216af6.png). A smooth five-pixel outside contour uses the approved shield’s median centennial blue (#0B4F9E). All opaque original shield pixels, the three background bands and 512px canvas are preserved. These are optional review/download images; app icon references are unchanged.

### Solid ivory with centennial-blue outer trim

[Current solid-ivory shortcut icon](michaelos-shortcuts-blue-outline-ivory-6716ae216af6.png): the same blue-outlined shield on a uniform #F5EBDD background, with no background stripe. 512px RGB PNG for iPhone Shortcuts.
