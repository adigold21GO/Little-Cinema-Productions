# Little Cinema Productions

Website for filmmaker Noah Gold, served at https://littlecinemaproductions.com.

The whole site is one file, `index.html`, with no build step. Hosting on Vercel serves it as a static page.

## Editing the site

All content lives in the config block at the top of the `<script>` in `index.html`:

- `SITE`: contact email (where contact-form messages are delivered, also shown on the Contact page) and the YouTube channel link.
- `FILMS`: one entry per film, with title, type, logline, synopsis, credits, festival laurels, cover image, and three photo lists: `stills` (frames from the film), `bts` (behind the scenes) and `extras`. Move a line between the lists to move a photo; an empty list hides its section.
- `video`: paste a public YouTube link to make a film playable on its page. Any YouTube link format works.
- `TRIM`: cuts black bars baked into an image (the Morpho stills are 4:3 frames inside a 16:9 file) and fills the frame with the rest of the picture, wherever that image appears.

## Contact form

The form on the Contact page sends each message to `SITE.email` through [FormSubmit](https://formsubmit.co), with no account or server needed. The first message sent from the live site triggers a one-time "Activate Form" email to that address; click the button in it once and every later message arrives as a normal email whose Reply-To is the sender. If the service is ever down, the form tells the visitor to email the address directly.

## Images

Photos currently load from the image storage of the old Squarespace site (noahgoldfilms.com). If that site is closed, the photos stop loading. To host them here instead, add the files to an `images/` folder with the same sub-paths, set `IMAGE_BASE` to `"images/"` and `RESIZE` to `false`.

## Video

YouTube only plays embedded videos on a page served from a web address. Opening `index.html` directly from your computer shows a link to YouTube instead of the player.
