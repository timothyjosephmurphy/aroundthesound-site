# Instructions for Grok Bot: move Around the Sound Guitar Studio off Canva

You are helping Chris, the owner of Around the Sound Guitar Studio, move **aroundthesoundguitarstudio.com** from Canva to his own Cloudflare Pages project. These files are Chris's to keep and change. Nothing here belongs to or depends on anyone else's accounts.

## How to work

1. Clone this repository to your box: `git clone https://github.com/timothyjosephmurphy/aroundthesound-site`
2. Read `README.md`. It is the plan, steps 1 to 17. Go through it **in order**, one step at a time.
3. At each step, do every part you can yourself (editing files, deploying, DNS records, settings Chris has connected you to). When a step is marked **You do this**, stop and tell Chris exactly what to do, where to click, and what to send you back. Wait until he confirms before you go on.
4. Never type Chris's passwords, card, bank or ID details yourself unless he gives you a secure form for it. Signing in, buying Google Workspace Individual, Stripe identity and bank verification, nameserver changes at his registrar, Google verification, and refunds are his.
5. Show Chris a preview before any change goes live, and before anything is sent to students.
6. After each step, give him a one-line status: done, waiting on him, or blocked and why.

## The site files (`/site`)

These are plain static files (HTML, one inline stylesheet per page, WebP images). There is no build step.

Before launch you must:

- [ ] Remove the yellow `Design mockup ... not the live site` banner (`<div class="banner">`) from every page.
- [ ] Remove `<meta name="robots" content="noindex,nofollow">` from every page.
- [ ] Delete `site/_headers`, or remove its `X-Robots-Tag: noindex, nofollow` rule.
- [ ] Replace `site/robots.txt` with `User-agent: *` / `Allow: /` / `Sitemap: https://aroundthesoundguitarstudio.com/sitemap.xml`, and create `site/sitemap.xml` listing every page.
- [ ] Change every `https://aroundthesound.tjm.art` URL (og:image and the JSON-LD image) to `https://aroundthesoundguitarstudio.com`. Remove the footer line "Mockup by TJ Murphy. Not indexed. Real site: ..."
- [ ] Replace everything marked **Example content** (search for `class="ex"`) with Chris's real details:
  - **Bio** on the home page: ask Chris for 3 to 5 sentences.
  - **Hours** on the home and contact pages, plus `openingHoursSpecification` in the JSON-LD on every page. Ask for his real teaching days and times, including Friday and Sunday.
  - **Testimonials** on the home page: only real quotes, with the student's permission. If there are none yet, remove the section.
  - **Booking section** on the contact and pricing pages: replace the placeholder buttons and the demo form with his Google Calendar booking buttons (README steps 8 and 11), "Book and pay online" and "Book and pay cash at your lesson". Delete the demo form and its script.
  - **Recordings & Links**: replace the placeholder slots with his real videos and links, or remove them.
  - **Privacy page**: update it to match what he actually uses, and let him read it.
  - **Contact email**: use hello@aroundthesoundguitarstudio.com once README step 5 is done.
- [ ] Keep his real prices and policies exactly as written unless Chris changes them.
- [ ] Check that every page fits a 375 px-wide phone with no sideways scroll.

## Deploying

Deploy to **Chris's own** Cloudflare account, in a Pages project named `aroundthesound` (README step 3), using the Cloudflare connector or `npx wrangler pages deploy site --project-name aroundthesound` after Chris signs in. Then attach his domain (README step 4). Don't use any other account or domain.

## When done

Confirm with Chris that the site, booking, payments, email and reminders all work. Then do README step 17: turn off the Canva site without cancelling his domain.
