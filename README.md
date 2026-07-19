# LUXFRAME STUDIO — Email Template

A premium, cinematic/retro-portrait themed responsive HTML email template.

File: `luxframe-studio-email.html`

## What's inside

- Single self-contained HTML file — inline styles + a `<style>` block, table-based
  layout for email-client compatibility, Outlook `mso` conditionals for the hero
  image and rounded corners.
- Responsive down to mobile (breakpoint at 600px): nav collapses, service cards
  and portfolio cards stack full-width.
- Sections, top to bottom: header/nav → hero with CTA → 3 service cards →
  3 portfolio cards → offer banner → testimonial → social icons → footer.

## Before you send it

1. **Swap the images.** Every image is a placeholder from `picsum.photos`,
   tagged by section:
   - `luxframe-hero` — hero background
   - `luxframe-golden` — Golden Hour Portrait
   - `luxframe-street` — Vintage Street Photography
   - `luxframe-studio` — Luxury Studio Portrait
   Replace each `src="https://picsum.photos/seed/..."` with a hosted URL to
   your real photography (use an image CDN — most inboxes block local/relative
   paths). Keep the `filter:` CSS on each `<img>` if you want to keep the
   sepia/duotone grade, or delete it once real color-graded images are in.

2. **Update the copy placeholders:**
   - Contact info in the footer (email, phone, address)
   - Testimonial name/quote
   - Social links (`#` → real Instagram/Behance/Facebook/Pinterest URLs)
   - Copyright year/company name if needed

3. **Fonts.** Playfair Display, Cormorant Garamond, and Poppins are loaded via
   Google Fonts in `<head>`. Some email clients (Outlook desktop, some Gmail
   contexts) strip web fonts and fall back to the Georgia/Arial fallbacks
   already set — this is expected and by design, not a bug.

4. **Test before sending.** Run it through Litmus, Email on Acid, or send test
   sends to Gmail/Outlook/Apple Mail — email client CSS support varies a lot
   more than browsers. Known intentional limitation: no `backdrop-filter`
   glassmorphism (unsupported in most clients), so "glass" cards are faked
   with layered gradients + a soft border instead.

## Editing tips

- Global colors are set as CSS variables at the top of the `<style>` block
  (`--matte-black`, `--burnt-orange`, `--copper-gold`, `--warm-white`), but
  since most email clients ignore `var()`, the actual hex values are also
  hardcoded inline throughout — if you change a color, update it in both
  places (or find/replace the hex value across the file).
- CTA buttons use the `.btn-orange` class for the gradient + glow shadow.
- Section dividers use the `.filmstrip` class (repeating gradient that mimics
  film perforations) — reuse it anywhere you want a themed rule instead of a
  plain `<hr>`.
