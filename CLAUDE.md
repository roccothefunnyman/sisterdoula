# sisterdoula

Website for Rocco's sister, a doula.

## Project context

- **Practitioner:** Melissa Cunningham (publicly: Melissa)
- **Business name:** the tending (`@thetendingdoula` on Instagram)
- **Location / service area:** Los Angeles and surrounding county
- **Services offered:** birth doula only (no postpartum, lactation, or childbirth ed)
- **Primary goal of the site:** lead generation. Prospective clients should be able to learn what she offers and reach out for a free consult.
- **Audience:** expectant parents researching doulas, typically 2nd/3rd trimester. Mobile-first.
- **Brand cues from her IG:** wordmark "the tending" set in a light classical serif (Italiana / Cormorant family); palette of cream, terracotta, sage, forest, warm brown, near-black brown; tagline "for your kind of birth" with circle-bullet ornaments.

## Stack

**Static site on GitHub Pages.** Plain HTML + CSS for now, no build step, deploys automatically on push to `main`.

- Hosted at `https://roccothefunnyman.github.io/sisterdoula/` until a custom domain is added
- Custom domain will come later via Cloudflare (sister will buy it). When ready, add a `CNAME` file at the repo root and point DNS at GitHub Pages.
- If the site outgrows plain HTML, migrate to Astro or 11ty (both static-export-friendly and Pages-compatible). Avoid Next.js, its Pages story is awkward and we don't need SSR.
- During the design-decision phase, three preview directions live at `/a/`, `/b/`, `/c/` with a picker at `/`. Once a direction is chosen, the picker and unused previews come out.

## Pages (initial scope)

Single-page for v1 (the previews are all single-page). Sections:

- Hero with wordmark and tagline
- Tending / philosophy
- The circle (services list, six items pulled from her IG tile copy: village, vision, choices, partner, questions, care team)
- About Melissa
- Write me (email, IG link)

Multi-page split (`/about`, `/contact`) is deferred until there's reason to.

## Design

- Tone: warm, calm, grounded. Avoid clinical or overly corporate. Avoid the AI-default look (Inter sans + single accent + rounded cards + soft shadows + emoji-decorated headers).
- Typography: lean serif. Candidates in current previews are Cormorant Garamond, Italiana, Source Serif 4, Fraunces, Crimson Pro, IBM Plex Mono / JetBrains Mono for metadata. No Inter, no Geist, no generic system-font sans.
- Imagery: she has none yet. The previews are typography-only. When she has photos, they replace placeholder copy/quotes, not augment them.
- Color: stick to her IG palette. Cream `#ece1cd`, terracotta `#c47a5e`, sage `#a3b59c`, forest `#506753`, warm brown `#6b4a2b`, near-black brown `#2a1c12`.

## Booking & contact

- For v1, contact is a `mailto:` link. No form, no backend. Easy on a static site, and avoids handling client data on a public form.
- A contact form (Formspree, Web3Forms, or Cloudflare-hosted equivalent) can come later if the volume justifies it.
- Consider Calendly or SavvyCal embed for free consults once we have her availability.
- **Important:** doulas often work with sensitive client info. Do not collect medical/health details through any public form. If we add one, keep it to name, email, due date, and a free-text message.

## Domain & hosting

- Hosting: GitHub Pages (free, public repo)
- Domain: TBD. Sister will buy through Cloudflare later. When she does, we add a `CNAME` file and DNS records at that point.
- Email: Google Workspace on the custom domain ($6/user/mo) recommended over generic gmail for client trust

## SEO basics to bake in from day one

- Local schema.org markup (`LocalBusiness` / `HealthAndBeautyBusiness`)
- City + "doula" in title tags and H1s
- Google Business Profile (separate from site, but link to it)
- Alt text on all images

## Working agreements

- Keep copy editable without code changes where possible (MDX or CMS, not hardcoded JSX)
- Mobile-first: design and test at 375px width before desktop
- Accessibility: semantic HTML, sufficient contrast, alt text. Sister's audience includes people on phones in waiting rooms.

## Open questions for Rocco

1. Sister's name and business name?
 - Melissa Cunningham
2. What city/region does she serve?
 - LA area
3. Which services? (birth, postpartum, both, other)
 - birth
4. Does she want to maintain the site herself after launch, or will Rocco?
- rocco and claude code
5. Any sites she likes the look of?
6. Does she already have a domain, logo, or photos?
-not yet - just what's on her instagram as of right now


## Writing Style

Write in a direct, natural, professional voice. Keep the tone friendly, grounded, and credible. Favor clarity over performance. Use concrete wording, specific examples, and plain English. Avoid hype, inflated claims, marketing language, and abstract filler.

Use clear, declarative sentences. Sound thoughtful and competent, not theatrical or overly eager to impress.

Do not use em dashes. Use commas, parentheses, or colons instead.

Avoid rhetorical contrast framing, paired-sentence echo patterns, and artificial pivots. Do not use phrases like "bottom line," "why it matters," or "sits at the intersection of." Avoid buzzwords like "cutting-edge," "transformative," "game-changing," or "best-in-class."

Prefer substance over flourish. Do not overuse bullets. Do not pad responses with repetitive summaries, vague transitions, or obvious filler. Keep structure clean and useful.

Acknowledge uncertainty when it is real. Do not sound overly certain or falsely definitive. Note trade-offs, assumptions, or what may still be missing where appropriate.

When giving recommendations, make them practical and specific. Explain reasoning clearly. Keep claims proportional to the evidence.

Match the user's context: precise and structured for technical content, crisp and concrete for strategic writing, warm and natural for conversation.

Never use emojis in files, reports, or documentation unless the user explicitly asks for them. Use numbers, letters, or descriptive labels instead.