# Launch day

Everything that changes when Sum Rockets goes live on the App Store.

1. **Get the App Store ID** – the numeric Apple ID from App Store Connect → App Information (e.g. `6712345678`).
2. **Add Apple's official badge** – download "Download on the App Store" (black, UK English) from
   https://developer.apple.com/app-store/marketing/guidelines/ and save it, **unmodified**, as
   `assets/badges/app-store-badge.svg`. Never redraw, recolour or edit the badge.
3. **Turn on the badge** – in `index.html`, set the one config line:
   `const APP_STORE_ID = "6712345678";`
   Both download spots (hero and the final call to action) then show the badge (54 px tall, which
   is above Apple's 40 px minimum, with clear space around it) linking to
   `https://apps.apple.com/gb/app/sum-rockets/id<ID>`, and the Apple trademark line appears in the footer.
4. **Smart App Banner** – on all three pages (`index.html`, `privacy/index.html`,
   `support/index.html`) replace the `<!-- LAUNCH: … -->` comment with:
   `<meta name="apple-itunes-app" content="app-id=<ID>">`
5. **Check** – open https://www.sumrockets.co.uk on an iPhone and a desktop: badge visible and
   tappable, link opens the App Store page, trademark line in the footer, Smart App Banner on iPhone.
6. **Commit and push** to `main` – GitHub Pages publishes it within a minute or two.

(In the app: set `AppConfig.appStoreID` to the same ID so the parent area's "Rate Sum Rockets" row appears.)
