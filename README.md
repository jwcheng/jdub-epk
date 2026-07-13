# JDub — EPK

Electronic press kit for **JDub**, a Taiwanese-American DJ based in Taipei
(electro · acid · house · breaks). Single-page site with bio, live videos,
recent shows, the Greenhouse Effect collective, media links, and booking contact.

**Live:** https://jdub-epk.vercel.app

## Structure

- `index.html` — the entire site. Self-contained: fonts, the cover/bio/media
  photos, and the React runtime are bundled inline; the page unpacks them at
  load. The tab title, copy, links, and layout all live here.
- `images/` — show flyers (`flyer-01..08.png`) and collective photos
  (`collective-*`) loaded at runtime by relative path. Also holds loose source
  copies of the hero/bio/media photos (`jdubs-hero.jpg`, `jdubs-bio.png`,
  `dj-media.png`) that are otherwise embedded in `index.html`.

## Deploy

Static site, no build step. From this folder:

```
vercel deploy --prod
```

The `.vercel/` link (gitignored) points at the existing `jdub-epk` Vercel
project, so redeploys keep the same URL.