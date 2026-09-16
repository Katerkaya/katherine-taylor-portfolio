# Katherine Taylor — Portfolio

A single-page static site. No build step, no dependencies.

```
index.html        the whole site (HTML, CSS and JS in one file)
images/           put your photos here
  hero.jpg        hero slideshow + project 01 tile (also the video's fallback image)
videos/           short, silent background clips
  kpop-anua.mp4   hero slide 1
404.html          shown for any address that doesn't exist
_headers          security + caching headers for Cloudflare Pages
```

## Editing

- **Hero photo:** save it as `images/hero.jpg`. If you use a different name, change the `--hero-img` line near the top of `index.html`.
- **Project tiles:** each tile is a `.project-0X` rule in the CSS. Replace the gradient with
  `url('images/your-file.jpg') center/cover no-repeat`.
- **Hero video:** save a short, silent MP4 (6–12 seconds, ideally under 5 MB; Cloudflare's hard limit is 25 MB per file)
  as `videos/kpop-anua.mp4`. Until it's there, slide 1 shows `images/hero.jpg`.
  Any other slide can get a video the same way: copy the `<video class="hero-video">` block into it.
- **YouTube in a case study:** in `#project-01`, replace `YOUTUBE_VIDEO_ID` with the video's ID.
  Add `is-vertical` to the class for Shorts. YouTube won't play when you open the file straight from your computer;
  check it on the live site.
- **Email:** search for `hello@example.com` and replace it.
- **Case studies:** each project's detail page is a `<section class="case" id="project-0X">` further down the file.
  Link straight to one with `yoursite.com/#project-03`.

## Deploying

Hosted on Cloudflare Pages, connected to this GitHub repo.
Every commit to `main` redeploys the site automatically in about a minute.

Build settings: Framework preset **None**, build command **empty**, build output directory **/**.
