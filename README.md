# The 200 Club of Monmouth County — Site Bundle

## What's new in this version

- **Events and Media now separate pages**
  - `events.html` — upcoming events only
  - `media.html` — press releases + videos
- **New nav order:** Home / About / Programs / Galleries / Events / Media / Join / Donate
- **Galleries page cleaned up** — removed the "Browse albums by year" intro and "Photography by Tom Zapcic" credit
- **Two new hero background photos needed** (see below)

## Files in this bundle

| File | Purpose |
|---|---|
| `index.html` | Home |
| `about.html` | About / leadership / board |
| `programs.html` | Scholarships + Valor + Spotlight 200 |
| `galleries.html` | Photo galleries (modal viewer + lightbox) |
| `events.html` | **NEW** — Events only |
| `media.html` | **NEW** — Press + Videos only |
| `join.html` | Membership + Donate + Contact |
| `config.json` | All content |
| `admin/config.yml` | Decap CMS field definitions |
| `admin/index.html` | Decap CMS entry point |

## Photos you need to add to `assets/images/`

| Filename | Where it shows |
|---|---|
| `events-hero-bg.jpg` | **NEW** — Events page header background |
| `media-hero-bg.jpg` | Media page header background (you may already have this) |

## Page header reference

| Page | Eyebrow | Title | Background image |
|---|---|---|---|
| Home | (slideshow) | (rotates) | hero-1.jpg / hero-2.jpg / hero-3.jpg |
| About | About Us | Standing Watch for Monmouth County's First Responders | about-hero-bg.jpg |
| Programs | Our Programs | Scholarships, Valor, and the Lives Behind Them | programs-hero-bg.jpg |
| Galleries | Galleries | Photo Galleries | galleries-hero-bg.jpg |
| Events | Events | Join Us This Year | **events-hero-bg.jpg** |
| Media | Press & Media | The 200 Club in the News | media-hero-bg.jpg |
| Join | Get Involved | Stand With First Responders | join-hero-bg.jpg |

## What to do in your local repo

1. **Replace** these files with the ones from this bundle:
   - All HTML files (note: `events.html` and `media.html` are now both included)
   - `config.json`
   - `admin/config.yml`
2. **Add the two hero background photos** to `assets/images/`:
   - `events-hero-bg.jpg` (required, new)
   - `media-hero-bg.jpg` (if not already present)
3. **Keep** your `assets/images/` folder otherwise as-is — all 936 album photos stay where they are
4. Commit + push
5. Netlify rebuilds; both new pages go live

## Pre-launch checklist

- [ ] Add `events-hero-bg.jpg` to `assets/images/`
- [ ] Confirm `media-hero-bg.jpg` is in `assets/images/`
- [ ] Replace phone number `(732) 555-0200` with real number
- [ ] Configure Formspree on contact form (currently in demo mode)
- [ ] Replace membership form `mailto:` with real form URL when ready
- [ ] Add `heather-magenheimer.jpg` (currently shows placeholder on Programs page)
- [ ] Verify Netlify Identity is enabled before sharing admin link with Sophia
- [ ] Walk Sophia through admin panel during handoff
