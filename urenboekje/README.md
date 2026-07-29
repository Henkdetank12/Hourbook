# HourBook

A small static web app for tracking work hours and estimating monthly pay. The app uses only HTML, CSS, and JavaScript — no server or database required.

## Files

- `index.html` — full interface and application logic
- `sw.js` — offline cache after the first visit
- `manifest.webmanifest` — metadata for iPhone and other mobile devices
- `icon.svg` — app icon

## Usage

1. Upload the full folder to a website reachable over HTTPS.
2. Open `index.html` on the iPhone in Safari.
3. The app then also works offline, as long as Safari does not clear the offline cache.
4. Optional: in Safari choose **Share > Add to Home Screen** for an app-like shortcut. This is not required.

## Storage and backups

- Primary data is stored locally in IndexedDB.
- Where the browser supports it, a second copy is kept in the local Origin Private File System vault.
- There is also a fallback copy in localStorage.
- These three storage forms belong to Safari and can disappear if website data is cleared.
- Therefore, regularly use **Share backup file** under **Settings > Data & backup**, and keep the JSON file in iCloud Drive or **On My iPhone**.
- **Restore from backup** can later re-import that file.

A regular web page on iPhone cannot silently keep overwriting an arbitrary file in iCloud Drive. An external backup therefore always requires a deliberate tap from the user.
