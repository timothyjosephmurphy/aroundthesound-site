---
title: "Around the Sound Guitar Studio: moving your site to Cloudflare Pages"
---

# Start here

Paste this one line to your Grok Bot:

> "Read https://github.com/timothyjosephmurphy/aroundthesound-site and follow GROKBOT.md to move my site off Canva."

That repository has your new site, already built from your Canva logo, graphics, photos and prices (preview: https://aroundthesound.tjm.art), plus these steps. The files are yours to keep. Grok Bot does the work and stops whenever it needs you.

- The quoted lines below are what Grok Bot will do at each step. You can also paste them yourself.
- **You do this:** marks the parts only you can do, like signing in, verifying, or entering card or bank details.
- Keep the Canva site running until the last step.

# 1. Cloudflare account

**You do this:** sign up at dash.cloudflare.com on the Free plan, then turn on two-factor sign-in.

> "Grok Bot, connect to my Cloudflare account and confirm it's on the Free plan."

# 2. Make the site files yours

> "Grok Bot, clone https://github.com/timothyjosephmurphy/aroundthesound-site to your box. Swap in my real bio, hours and testimonials. Before launch, remove the 'Design mockup' banner, the noindex tags, the X-Robots-Tag header and the block-everything robots.txt. Add a normal robots.txt and a sitemap.xml, and point the canonical links at aroundthesoundguitarstudio.com."

**You do this:** write your bio (3 to 5 sentences) and confirm your hours. Add testimonials only if they're real quotes from students who said it's OK to use them.

# 3. Put it on Cloudflare Pages

> "Grok Bot, create a Cloudflare Pages project called aroundthesound, deploy my site to it, and send me the preview link."

**You do this:** check every page on your phone.

# 4. Move your domain to Cloudflare

> "Grok Bot, find out where aroundthesoundguitarstudio.com is registered. Then add it to my Cloudflare account on the Free plan, copy any DNS records that matter, and tell me the two nameservers to set."

**You do this:** sign in where the domain is registered (probably Canva or Tucows; look for a receipt from around Sept 26, 2026). Replace the systemdns.com nameservers with Cloudflare's two. If it's locked, ask that company's support to unlock it.

> "Grok Bot, once the domain is Active in Cloudflare, connect aroundthesoundguitarstudio.com and www to my Pages project, send www to the main address, and check that both load over https."

# 5. Email on your domain

> "Grok Bot, set up Cloudflare Email Routing so hello@aroundthesoundguitarstudio.com forwards to my Gmail. Add SPF and DMARC records, put the new address on my contact page, and walk me through Gmail's 'Send mail as' so I can reply from it."

**You do this:** click the confirmation emails from Cloudflare and Gmail.

# 6. Stripe account (free; Stripe takes a small fee per payment)

**You do this:** sign up at stripe.com. Verify your identity (legal name, SSN or EIN), add your bank account for payouts, and switch to live mode.

> "Grok Bot, in Stripe set my public business name to Around the Sound Guitar Studio, the statement descriptor to AROUND THE SOUND, add my logo, and turn on email receipts."

# 7. Payment links

Prices: one lesson is $75 Mon-Thu or $90 Saturday. 10 lessons are $600 (Mon-Thu) or $720 (Saturday). Add-ons: GoPro recording $20, practice video $35, song breakdown $75, gear consultation $100 an hour.

> "Grok Bot, in Stripe create payment links for: Lesson Mon-Thu $75, Lesson Saturday $90, 10-Lesson Package Mon-Thu $600, 10-Lesson Package Saturday $720, Lesson Recording on GoPro $20, Personalized Practice Video $35, Song Breakdown $75, and Guitar Buying/Setup Consultation $100. Give me the list of links."

# 8. Your free booking page

You'll use one free Google Calendar booking page on your Gmail. It takes unlimited bookings, and Google sends each student a confirmation and a calendar invite.

> "Grok Bot, in my Google Calendar create one appointment schedule called 'Guitar or Bass Lesson'. Make it 60 minutes with a 15-minute buffer, require at least 24 hours' notice to book, and use my real teaching hours. Set the location to 'Home studio in West Seattle (address sent after booking)' or Google Meet. Add the booking question 'What's a song you'd love to learn?' Put this in the description, with my real Stripe links:
>
> 'Lessons: $75 Mon-Thu, $90 Saturday. 10-lesson packages: $600 (Mon-Thu) or $720 (Saturday). Pay online: [Mon-Thu lesson link] | [Saturday lesson link] | [10-pack links], or pay cash at the start of your lesson. Package holders just book; no payment needed. Please provide at least 24 hours' notice if you need to cancel or reschedule. Cancellations with less than 24 hours' notice will be charged the full lesson fee.'
>
> Show me the booking page before saving."

**You do this:** check the hours, prices and links on the booking page.

# 9. Payment and package sheet

> "Grok Bot, make a Google Sheet with three tabs. Bookings: date, student, paid by card or cash, amount. Packages: student, lessons bought, used and left. Cash log: date, student, item, amount, plus a monthly total. Each week, match my Google Calendar lessons against my Stripe payments and this sheet, and tell me who hasn't paid yet."

**You do this:** add each cash payment to the sheet the same day, and issue any refunds from the Stripe dashboard.

# 10. Reminders (free)

The free booking page doesn't send reminders. Students' calendar invites still notify them, and you can add a free email reminder too:

> "Grok Bot, add a free Google Apps Script to my payment sheet that runs every evening. It should find tomorrow's 'Guitar or Bass Lesson' bookings in my calendar and email each student from my Gmail: lesson time, location or Meet link, how to pay, and the 24-hour policy. Show me the email text and a test send to me first."

**You do this:** approve the script's Google permissions when asked.

# 11. Book button on your site

> "Grok Bot, get the booking button code for my 'Guitar or Bass Lesson' page. Put it on the Contact page and behind every 'Book a lesson' link, and load it only when someone clicks. Next to it, add 'Pay online' with my Stripe links and 'or pay cash at the start of your lesson'. Put the package and add-on links on the Pricing page. Update my privacy page to mention Google Calendar and Stripe, then deploy."

# 12. Test it

**You do this:** using a second email address, book a lesson. Check that:

- the confirmation and calendar invite arrive
- the lesson shows up in your calendar
- the reminder email arrives the evening before

Then pay one Stripe link with a real card, refund it in Stripe, and cancel the test lesson.

Docs: [Create a booking page](https://support.google.com/calendar/answer/11608416), [Booking page options and limits](https://support.google.com/calendar/answer/13762729).

# 13. Cash

> "Grok Bot, make a simple cash receipt template I can text or email: date, student, what it's for, amount, 'Paid in cash'."

**You do this:**

- Log every cash payment the same day.
- Give a receipt when someone asks.
- Cash lesson income is taxable like card income, so keep the log and the Stripe reports together for tax time. This is a records note, not tax advice; ask a tax preparer about your situation.

# 14. Google Business Profile

> "Grok Bot, help me create a Google Business Profile for Around the Sound Guitar Studio as a service-area business covering West Seattle, category 'Guitar instructor', with my website, hours, prices, photos and booking link. Don't show my home address."

**You do this:** sign in to Google and complete the verification.

# 15. Search Console and analytics

> "Grok Bot, add aroundthesoundguitarstudio.com to Google Search Console using a DNS record in Cloudflare, submit my sitemap, and request indexing for the home page. Then turn on Cloudflare Web Analytics and send me a short monthly summary."

**You do this:** sign in to Google and approve.

# 16. Reviews, privacy page and directories

> "Grok Bot, get my Google review link and draft a short text I can send students asking for a review. Then help me list my studio on Thumbtack, Superprof, TakeLessons, Nextdoor, Yelp, Apple Business Connect and Bing Places with exactly the same name, website and area."

**You do this:**

- Send the review requests yourself.
- Only quote students on the site with their permission.
- Read the privacy page and make sure it matches what you do.
- Verify each directory listing.

# 17. Turn off Canva

Wait until the new site, bookings and email have worked for about two weeks.

> "Grok Bot, confirm my domain is served by Cloudflare Pages and nothing points at Canva, then walk me through unpublishing the Canva site without cancelling my domain."

**You do this:** unpublish the Canva site. If the domain is still registered through Canva, either keep it there (it renews Sept 26, 2027) or transfer it to Cloudflare before you cancel any Canva plan.

# What it costs

Everything above is free except Stripe's per-payment fee. That covers Cloudflare Pages, email routing and Web Analytics; Google Calendar's booking page; Google Business Profile; Search Console; and Stripe (no monthly fee). Your only fixed cost is renewing the domain each year (next renewal Sept 26, 2027).

# Optional upgrade later

Google Workspace Individual, about $9.99 a month (US price, not verified), adds these to your booking page: payment required at booking, separate weekday and Saturday pages, automatic reminders, and email verification for bookers. [Payments for appointments](https://support.google.com/calendar/answer/16287038)

# Checklist: only you can do these

- [ ] Cloudflare signup and two-factor sign-in (1)
- [ ] Bio and hours (2); check the site on your phone (3)
- [ ] Change the domain's nameservers (4)
- [ ] Email confirmations (5)
- [ ] Stripe identity check, bank details and live mode (6)
- [ ] Check the booking page (8)
- [ ] Log cash the same day; issue refunds in Stripe (9)
- [ ] Approve the reminder script (10)
- [ ] Test booking and refund (12)
- [ ] Give cash receipts when asked (13)
- [ ] Google Business Profile verification (14); Search Console sign-in (15)
- [ ] Review requests, privacy page check, directory verification (16)
- [ ] Unpublish Canva (17)
