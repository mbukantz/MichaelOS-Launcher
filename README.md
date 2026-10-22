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

Icons and the 72px loading mark use the approved MichaelOS artwork. Their content version is `8f833ecc0d4d`. Regenerate all sizes from the master in `mbukantz/MichaelOS` using `python scripts/generate-branding.py --launcher ../MichaelOS-Launcher`; add `--check` to verify. Do not edit generated icon sizes independently. Existing Home Screen installs may require removal and re-addition to refresh the installed icon.
