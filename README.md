# Little Cinema Productions

Website for filmmaker Noah Gold, served at https://littlecinemaproductions.com.

The whole site is one file, `index.html`, with no build step. Hosting on Vercel serves it as a static page.

## Editing the site

All content lives in the config block at the top of the `<script>` in `index.html`:

- `SITE`: contact email (shown on the Contact page when filled in) and the YouTube channel link.
- `FILMS`: one entry per film, with title, type, logline, synopsis, credits, festival laurels, cover image, and two photo lists: `stills` (frames from the film) and `bts` (behind the scenes). Move a line between the two lists to move a photo.
- `video`: paste a public YouTube link to make a film playable on its page. Any YouTube link format works.
- `TRIM`: crops a black strip left over from a screenshot, wherever that image appears.

## Images

Photos currently load from the image storage of the old Squarespace site (noahgoldfilms.com). If that site is closed, the photos stop loading. To host them here instead, add the files to an `images/` folder with the same sub-paths, set `IMAGE_BASE` to `"images/"` and `RESIZE` to `false`.

## Video

YouTube only plays embedded videos on a page served from a web address. Opening `index.html` directly from your computer shows a link to YouTube instead of the player.
