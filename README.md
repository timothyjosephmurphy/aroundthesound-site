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

# 6. Google Workspace Individual (for paid bookings)

Google Calendar's booking page is the scheduler. A plain Gmail account gets one free booking page, with no payments and no reminders. Google Workspace Individual on your existing Gmail adds:

- paid bookings through Stripe
- more than one booking schedule
- email reminders
- email verification for people who book

It costs **$9.99 a month, or $99.99 a year**, after a 14-day free trial ([Google Workspace Individual](https://workspace.google.com/individual/)). Google One Premium does not include payments.

**You do this:** sign in to your Gmail at workspace.google.com/individual, start the plan and enter your card.

> "Grok Bot, confirm Workspace Individual is active on my Gmail and that Calendar shows 'Appointment schedules' with payment options."

# 7. Stripe account

**You do this:** sign up at stripe.com. Verify your identity (legal name, SSN or EIN), add your bank account for payouts, and switch to live mode.

> "Grok Bot, in Stripe set my public business name to Around the Sound Guitar Studio, the statement descriptor to AROUND THE SOUND, add my logo, and turn on email receipts."

**You do this:** in Google Calendar, go to Settings, then General, then Appointment schedules, then Connect Stripe, and sign in to Stripe to approve.

# 8. Booking schedules

You'll have three. Your cancellation text goes on all three:

*"Please provide at least 24 hours' notice if you need to cancel or reschedule. Cancellations with less than 24 hours' notice will be charged the full lesson fee."*

> "Grok Bot, in my Google Calendar create these appointment schedules. Make each one 60 minutes with a 15-minute buffer, at least 24 hours' notice to book, location 'Home studio in West Seattle (address sent after booking)' or Google Meet, and the booking question 'What's a song you'd love to learn?'
>
> 1. 'Guitar or Bass Lesson, pay online (Mon-Thu)': Monday to Thursday hours only. Under 'Payments & cancellation policy', check 'Require payment when booking', set $75, and add my cancellation text.
> 2. 'Guitar or Bass Lesson, pay online (Saturday)': Saturday hours only, $90, same settings.
> 3. 'Lesson, pay cash at lesson': all my teaching days, no payment. In the description, put: 'Cash is due at the start of the lesson ($75 Mon-Thu, $90 Saturday). 10-lesson package holders, book here too.' Add my cancellation text.
>
> Turn on email verification for bookers on all three. Show me each booking page before saving."

Students can pay online by card, Apple Pay or Google Pay. Google takes no extra fee beyond Stripe's, and refunds aren't automatic. **You do this:** issue any refunds from the Stripe dashboard.

Docs: [Create a booking page](https://support.google.com/calendar/answer/11608416), [Payments for appointments](https://support.google.com/calendar/answer/16287038), [Booking page options and limits](https://support.google.com/calendar/answer/13762729).

# 9. Packages and extras

Prices: 10 lessons for $600 (Mon-Thu) or $720 (Saturday). Add-ons: GoPro recording $20, practice video $35, song breakdown $75, gear consultation $100 an hour.

> "Grok Bot, in Stripe create payment links for: 10-Lesson Package Mon-Thu $600, 10-Lesson Package Saturday $720, Lesson Recording on GoPro $20, Personalized Practice Video $35, Song Breakdown $75, and Guitar Buying/Setup Consultation $100. Set each package link's confirmation message to: 'Thanks! Book your lessons with the pay-at-lesson link I'll email you.' Add the links to my Pricing page, and note that packages and extras can also be paid in cash."

> "Grok Bot, make a Google Sheet that tracks each package student (lessons bought, used and left, and whether they paid by card or cash). Update it whenever I tell you a lesson happened."

Package holders book on the pay-at-lesson schedule.

# 10. Reminders

> "Grok Bot, turn on email reminders for all three booking schedules, 24 hours before each lesson, and include the cancellation policy."

# 11. Book buttons on your site

> "Grok Bot, get the booking button and inline embed code for my three Google Calendar booking schedules. Put a 'Book and pay online' button (Mon-Thu and Saturday) and a 'Book and pay cash at your lesson' button on the Contact page and on every 'Book a lesson' link. Load the embed only when someone clicks. Update my privacy page to mention Google Calendar and Stripe, then deploy."

# 12. Test each booking

**You do this:** using a second email address, book one lesson on each of the three schedules. Pay the online ones with a real card. Check each of these:

- the confirmation email arrives
- the event shows up in your calendar
- the reminder arrives
- the cancellation policy is shown

Then refund your card payments in Stripe and cancel the test lessons.

# 13. Cash

> "Grok Bot, make a simple cash receipt template I can text or email (date, student, what it's for, amount, 'Paid in cash'). Add a 'Cash log' tab to my package sheet with date, student, item and amount, and add a monthly total."

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

# Checklist: only you can do these

- [ ] Cloudflare signup and two-factor sign-in (1)
- [ ] Bio and hours (2); check the site on your phone (3)
- [ ] Change the domain's nameservers (4)
- [ ] Email confirmations (5)
- [ ] Buy Google Workspace Individual (6)
- [ ] Stripe identity check, bank details and live mode; connect Stripe in Calendar (7)
- [ ] Issue refunds in Stripe (8)
- [ ] Test bookings and refund them (12)
- [ ] Log cash and give receipts (13)
- [ ] Google Business Profile verification (14); Search Console sign-in (15)
- [ ] Review requests, privacy page check, directory verification (16)
- [ ] Unpublish Canva (17)
