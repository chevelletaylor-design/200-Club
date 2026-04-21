# The 200 Club of Monmouth County — Website

A custom multi-page website with a built-in admin panel. Staff can update every piece of text, every link, every photo, and every press release without touching code.

## 🎯 Editing the Site

You DON'T need to edit code to update the website. Everything lives in a visual admin panel.

### To edit any text, photo, link, or section:

1. Go to **`[SITE URL]/admin/`** (e.g. `monmouth200club.netlify.app/admin/`)
2. Log in with your email + password
3. Click **"🛡️ Edit Site Content"**
4. Expand the section for the page you want to update (🏠 Home, 👥 About, 🎓 Programs, 📰 Media, or 🤝 Join)
5. Make your edits in the form fields
6. Click **"Publish"** (top right)
7. Your live site updates within 60 seconds ✨

## 📚 Page Structure

| Page | File | What's on it |
|---|---|---|
| Home | `index.html` | Hero slideshow, 3 mission pillars, featured Valor story, president's message |
| About | `about.html` | Our story, full board & trustees listing, president's message |
| Programs | `programs.html` | Scholarships, Valor Awards, Spotlight 200 stories |
| Media | `media.html` | Upcoming events, press releases, photo galleries, video gallery |
| Join | `join.html` | Membership info, donation with PayPal QR, contact form |

All 5 pages share the same logo, nav, and footer — edit those in the global "🏷️ Brand & Logo", "🧭 Navigation Menu", "🌐 Social Media", and "📎 Footer" sections at the top of the admin.

## 🗂️ Admin Panel Map — Common Edits

| What you want to change | Where |
|---|---|
| Add or edit a press release | 📰 MEDIA PAGE → Press & Media → Category → Press items |
| Add a new event with ticket link | 📰 MEDIA PAGE → Events Section → Events list |
| Replace the logo | 🏷️ Brand & Logo → Logo image |
| Swap the featured Valor story on the homepage | 🏠 HOME PAGE → Featured Story |
| Update the president's message | 🏠 HOME PAGE → President's Message (also appears on About page) |
| Add a new Spotlight 200 story | 🎓 PROGRAMS PAGE → Spotlight 200 Stories → Stories |
| Update board members | 👥 ABOUT PAGE → Board & Trustees |
| Update the PayPal link (in 4 places at once) | 🧭 Navigation Menu → Donate button link AND 🤝 JOIN → Donation Card → Button link |
| Add a social media link | 🌐 Social Media Links |
| Link the contact form to real email | 🤝 JOIN → Contact Section → Form provider → formspree + paste URL |

## 📁 File Structure (for reference only — don't edit directly)

```
200-club/
├── index.html              ← Home
├── about.html              ← About + Board
├── programs.html           ← Scholarships + Valor + Spotlight 200
├── media.html              ← Events + Press + Galleries + Videos
├── join.html               ← Membership + Donate + Contact
├── config.json             ← all content (admin edits this)
├── README.md               ← this file
├── ASSET-GUIDE.md          ← how to name photos
├── admin/
│   ├── index.html          ← admin panel login
│   └── config.yml          ← admin panel field definitions
└── assets/
    └── images/             ← photos uploaded via admin panel
```

## 📸 Uploading Photos

Photos upload directly through the admin panel (📷 icons throughout the editor). See `ASSET-GUIDE.md` for photo sizing, naming, and orientation rules — **the site uses landscape photos everywhere except for two specific portrait slots** (Officer Russo on the homepage + Mary Pat Angelini's headshot).

Event photography is generously provided by Tom Zapcic Photography. Each gallery card links out to the full SmugMug gallery.

## 📧 Contact Form Setup

The contact form on `/join.html` is wired to Formspree (free tier = 50 submissions/month).

### To activate the form:
1. Sign up at [formspree.io](https://formspree.io)
2. Create a new form → copy the endpoint URL
3. Admin panel → 🤝 JOIN PAGE → Contact Section
4. Paste the Formspree URL into "Formspree URL"
5. Change "Form provider" from `demo` to `formspree`
6. Publish

Formspree will email to confirm the owner's address once. After that, submissions flow directly to staylor@monmouth200club.com.

## 👥 New Membership Form (TO DO)

The old membership form lived on Squarespace and is being replaced. Options for the new form:

- **Recommended:** Create a new JotForm (to match the Scholarship and Valor nomination forms) and paste the URL into the admin panel → 🤝 JOIN → Membership Card → Button link
- **Alternative:** Use Formspree for the membership form as well

Until a new form is live, the button defaults to a mailto: link to `staylor@monmouth200club.com`.

## 🎬 Video Gallery

The Media page video gallery uses YouTube. To add a new video:

1. Get the YouTube URL (e.g. `https://youtu.be/ABC123`)
2. Admin panel → 📰 MEDIA PAGE → Video Gallery → Videos
3. Paste the full URL into "Full YouTube URL"
4. Copy just the ID (the part after `youtu.be/` — `ABC123` in the example) into "YouTube video ID"
5. Add a title
6. Publish

The site auto-generates the video thumbnail from the ID and makes the card open YouTube in a new tab.

## 📰 Press Releases

The Media page has 41+ press items organized into 3 categories: "Recent Press Releases," "In The News," and "Radio & Broadcast."

**All URLs default to `#` (placeholder).** To make a press item actually link to the article:

1. Admin panel → 📰 MEDIA PAGE → Press & Media → (category) → Press items → (item)
2. Paste the real article URL into "Article URL"
3. Publish

Items with URL `#` still display but won't open anything when clicked.

## 🌐 Deployment

This site is deployed on Netlify. Every admin-panel publish triggers an auto-rebuild and push within 60 seconds.

- **Live site:** `[SITE URL]`
- **Admin panel:** `[SITE URL]/admin/`
- **GitHub repo:** `[REPO URL]`

## 🎨 Design Credit

Designed by [Chevelle](https://www.bychevelle.com) — brands, built the right way.

## 🆘 Need Help?

Email chevelle@bychevelle.com or check the admin panel — most issues can be fixed by editing in there and clicking "Publish" again.
