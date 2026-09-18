# Katherine Taylor — Portfolio

A single-page static site. No build step, no dependencies.

```
index.html        the whole site (HTML, CSS and JS in one file)
404.html          shown for any address that doesn't exist
images/           optional photos
_headers          security + caching headers
```

## Adding videos and photos

Everything is set in one list near the bottom of `index.html`. Search for `YOUR VIDEOS AND PHOTOS`.

- **youtube:** a YouTube link. It plays silently behind the hero, its thumbnail appears on the
  project tile, and it plays with sound in the case study.
- **video:** or a video file in the `videos` folder (under 25 MB), which plays with sound in the case study.
- **heroVideo:** an optional short, silent loop for the hero. If empty, `video` is used.
- **start / end:** the seconds that loop behind the hero (`0` = beginning / end).
- **shape:** `'wide'`, `'square'` or `'tall'`. Square and tall videos are shown whole in the hero.
- **image:** a photo in the `images` folder, used on the tile and while the hero video loads.
- **imageMobile / imagePosition / poster:** optional taller phone image, crop focus point for the tile, and a still for the case-study player.
- **SLIDE_SECONDS**, just below the list, sets how long each hero slide stays up.

Current setup:

| # | Project | Source |
|---|---------|--------|
| 1 | K-Pop Demon Hunters × Anua | YouTube (hero loop + case-study film); tile art is a temporary still |
| 2 | Create 100 | `videos/create-100.mp4` (hero: `create-100-loop.mp4`, a footage-only cut) |
| 3 | Disney Munchlings × Primark | `videos/munchlings-reel.mp4` (hero: `munchlings-reel-loop.mp4`, tall); `munchlings-square.mp4` plays in the gallery |
| 4 | Westin — Own Your Mornings | YouTube (hero loop, seconds 2–24, and the case-study film); link to the film on LBB |

Notes:
- YouTube videos must allow embedding, otherwise the thumbnail shows instead.
- Background videos don't play when the site is opened straight from your computer (YouTube), or
  when visitors have "reduce motion" or data saver switched on. The image or thumbnail shows instead.

## Case study pages (K-Pop Demon Hunters, Create 100, Munchlings, Westin)

The case study (`<section class="case" id="project-02">`) has extra sections: a numbers strip, the case study
text, an auto-scrolling **gallery** (images in `images/create-100/`), a **featuring** list and **in the press** links.

- **Your role:** the four rows under the case study text (`case-roles`) describe what you did.
- **Gallery:** each image is a `<figure>` inside `marquee-track`. Add or remove figures; the loop adjusts itself.
  Hovering pauses it.

## Other edits

- **Email:** search for `hello@example.com` and replace it.
- **Case study text:** each project's detail page is a `<section class="case" id="project-0X">`.
  Link straight to one with `yoursite.com/#project-03`.

## Deploying

Connected to Cloudflare via GitHub. Every commit to `main` redeploys automatically.
