# sisterdoula

Website for Rocco's sister, a doula.

## Project context

- **Practitioner:** _TBD — sister's name / how she wants to appear publicly_
- **Business name:** _TBD_
- **Location / service area:** _TBD — doulas typically serve a metro area; this drives SEO and copy_
- **Services offered:** _TBD — e.g. birth doula, postpartum doula, lactation, childbirth education, bereavement_
- **Primary goal of the site:** lead generation — prospective clients should be able to learn what she offers and book a free consult
- **Audience:** expectant parents researching doulas, typically 2nd/3rd trimester; mobile-first

## Stack

**Static site on GitHub Pages.** Plain HTML + CSS for now — no build step, deploys automatically on push to `main`.

- Hosted at `https://<username>.github.io/sisterdoula/` until a custom domain is added
- Custom domain will come later via Cloudflare (sister will buy it); when ready, add a `CNAME` file at the repo root and point DNS at GitHub Pages
- If the site outgrows plain HTML, migrate to Astro or 11ty (both static-export-friendly and Pages-compatible). Avoid Next.js — its Pages story is awkward and we don't need SSR.

## Pages (initial scope)

- `/` — hero, services summary, brief bio, testimonials, CTA to book consult
- `/about` — full bio, philosophy, training/certifications
- `/services` — detailed offerings + pricing (or "inquire for pricing")
- `/contact` — consult booking form, email, optional Calendly embed
- `/blog` — optional, defer until v2

## Design

_TBD — confirm with sister:_
- Tone: warm, calm, grounded (typical for doula sites); avoid clinical or overly corporate
- Imagery: real photos of her if available; otherwise tasteful stock (no stylized birth imagery without her approval)
- Color/typography: pick once we have her preference

## Booking & contact

- Contact form posts to email (Resend / Formspree) — pick once stack is decided
- Consider Calendly or SavvyCal embed for free consults
- **Important:** doulas often work with sensitive client info; do not collect medical/health details through the public form. Just name, email, due date, and a message field.

## Domain & hosting

- Hosting: GitHub Pages (free, public repo)
- Domain: TBD — sister will buy through Cloudflare later; we'll add a `CNAME` file and DNS records at that point
- Email: Google Workspace on the custom domain ($6/user/mo) recommended over generic gmail for client trust

## SEO basics to bake in from day one

- Local schema.org markup (`LocalBusiness` / `HealthAndBeautyBusiness`)
- City + "doula" in title tags and H1s
- Google Business Profile (separate from site, but link to it)
- Alt text on all images

## Working agreements

- Keep copy editable without code changes where possible (MDX or CMS, not hardcoded JSX)
- Mobile-first: design and test at 375px width before desktop
- Accessibility: semantic HTML, sufficient contrast, alt text — sister's audience includes people on phones in waiting rooms

## Open questions for Rocco

1. Sister's name and business name?
2. What city/region does she serve?
3. Which services? (birth, postpartum, both, other)
4. Does she want to maintain the site herself after launch, or will Rocco?
5. Any sites she likes the look of?
6. Does she already have a domain, logo, or photos?
