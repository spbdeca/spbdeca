# SPB DECA website

Seven pages, one stylesheet, no build step. Open `index.html` in a browser and it works.

```
index.html      Home — nine sections, from hero to join CTA
about.html      What DECA is, the chapter, officers, advisor
compete.html    Filterable directory of competitive events
prep.html       Prep Center — role plays, exams, written events, checklist
calendar.html   Live Google Calendar embed + season overview
join.html       Why join, eligibility, steps, interest form, FAQ
contact.html    Contact, advisor, sponsorship tiers
styles.css      The whole design system
assets/         Logo file
```

## Before this goes live

1. **Replace the logo.** `assets/spb-logo.svg` is a stand-in built to the right proportions. Drop in the real SPB DECA file under the same name and every page picks it up.
2. **Fill the eight yellow boxes.** Every unfinished item on the site is marked with a gold-bordered note. Search the HTML for `class="todo"` to find them all. Delete each note once the content is in.
3. **Add photos.** Dashed grey boxes marked `class="slot"` are photo placeholders. Replace each with `<img src="assets/your-photo.jpg" alt="description">`.
4. **Real numbers on the homepage.** The four stats currently show dashes. Put actual figures in as soon as you have them — even small ones. Monta Vista's "179 top-10 ICDC placements" does more for their credibility than anything else on their site.
5. **Check the calendar embed.** It points at `spbdeca42@gmail.com`. The calendar must be set to public (Calendar settings → Access permissions → Make available to public) or visitors will see an error.
6. **Embed the Google Forms.** Two placeholder slots, on `join.html` and `contact.html`. In the form: Send → `<>` tab → copy the iframe → paste it in place of the slot div.

## Hosting

Any static host works and all of these are free:

- **GitHub Pages** — create a repo, upload the folder, Settings → Pages → deploy from main. Point `spbdeca.org` at it with a CNAME.
- **Netlify** — drag the folder onto the dashboard. Custom domain in two clicks.
- **Cloudflare Pages** — same idea, connected to a repo.

## About Google Sites

Your notes leaned toward Google Sites so students can edit with a Google account, and that reasoning is sound — but Google Sites cannot reproduce this layout. Its editor has fixed section types, limited CSS, and no support for the filter interaction on the events page.

Two workable options:

**Ship this as-is on Netlify or GitHub Pages.** Students edit HTML directly in the GitHub web editor, which is genuinely not hard for the kind of edits a chapter makes — changing text, swapping a photo, adding an officer card. The calendar and forms stay dynamic through their embeds regardless, which covers most of what changes during a year.

**Or rebuild in Google Sites using this as the spec.** You lose the event filter and some of the polish, and you keep drop-dead-simple editing. The color values, section order and copy all transfer directly.

The honest middle: whoever maintains this next year matters more than the platform. If there is one officer comfortable with GitHub, take option one. If there isn't, take option two and accept a plainer site.

## Continuity

The failure mode for chapter sites is officer graduation. Harker's resource page is three links into a Google Drive folder — that works right up until the owning account is deactivated.

Put every shared file in a folder owned by `spbdeca42@gmail.com`, not any student's personal Drive. Same for the calendar and every Google Form. Then handing over the chapter is handing over one password.

## Trademark

The DECA name and diamond belong to DECA Inc. The disclaimer in the footer of every page covers this — leave it there.
