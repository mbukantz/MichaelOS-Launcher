# MichaelOS Launcher — iPhone test

This is a static wrapper around the existing MichaelOS Apps Script deployment.

## Target MichaelOS URL
https://script.google.com/macros/s/AKfycbyrW9FGCk2c4Hx51qH5Mbkmi9Nt2eibY1ubFZ66xzxAzgZDgq5PjNMTcQixt-4R03qz1Q/exec

## Recommended test host
GitHub Pages, in a separate repository such as `MichaelOS-Launcher`.

## Test sequence
1. Deploy MichaelOS 6.5.132 first. It adds `XFrameOptionsMode.ALLOWALL`.
2. Publish this folder as a static site.
3. Open the Pages URL on the iPhone in Safari.
4. Confirm MichaelOS renders without the Apps Script warning chrome.
5. Test:
   - Main → Calendar → Home → Rangers → Finance → Rules → Mail Home.
   - Refresh buttons.
   - Calendar data and event creation.
   - Gmail Rules / Mail Home data.
   - Gmail deep links to the Gmail app.
6. If authentication fails inside the frame, use the temporary “Open MichaelOS directly” fallback.
7. Only after the iframe works reliably, use Safari Share → Add to Home Screen.

## Important
Apps Script's `ALLOWALL` removes its default X-Frame-Options protection. Keep this as a test until you decide whether the launcher is worth making permanent.
