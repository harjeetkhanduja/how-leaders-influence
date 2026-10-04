# How Leaders Influence · Book website

A single page site for How Leaders Influence by Harjeet Khanduja, built in the style of the HR Mastermind page. No build step. It runs on GitHub Pages as it is.

## The 8 sections

Each section ends with Buy buttons, just like HR Mastermind.

1. Hero with cover and buy buttons
2. Author credibility strip with 12 awards
3. Problem, research facts, potter story and the 3 directions of influence
4. Inside the book. Chapters, outcomes, sample pages and the 25 leaders
5. Testimonials, 8 frameworks, 7 techniques and 37 concepts
6. Questions the book answers and 6 reader personas
7. Meet the author with photos, badges and short quotes
8. FAQ, comparison with a leadership program, price card, Notify me form and bulk orders

## What to edit

Almost everything you need to change sits in one block near the bottom of `index.html`, called `CONFIG`.

| Setting | What to put |
|---|---|
| `amazon` | Amazon product link |
| `flipkart` | Flipkart product link |
| `email` | Contact email, set to hello@howleadersinfluence.com |
| `reach` | Combined followers, for example `3 lakh+` |
| `formAction`, `formName`, `formEmail` | Google Form details for the Notify me box (see below) |

Until the Google Form is added, the Notify me box opens an email instead.

## Photos you can drop in

No code changes needed. Name the file as shown and it appears automatically. Missing files fall back to initials.

| Folder | File name example |
|---|---|
| `assets/endorsers/` | `marshall-goldsmith.jpg`, `kiran-bedi.jpg`, `r-seshasayee.jpg` |
| `assets/leaders/` | `himanshu-rai.jpg`, `sarika-naik.jpg` |
| `assets/logos/` | `iit-roorkee.png`, `insead.png`, `tedx.png`, `shrm.png`, `economic-times.png`, `cii.png`, `nasscom.png` |

Rule for names. Lowercase, drop Dr. and Prof., spaces become hyphens. Square photos work best.

## Connect the Notify me box to Google Forms

1. Create a Google Form with two short answer questions, Name and Email.
2. Open the form preview, right click, View page source, search for `entry.` to find the two field ids.
3. Copy the form link, change `viewform` at the end to `formResponse`.
4. Paste these into `CONFIG` as `formAction`, `formName` and `formEmail`.
5. Responses land in the form's linked Google Sheet.

## Publish on GitHub Pages

1. Create a new public repository on GitHub, for example `how-leaders-influence`.
2. Upload everything in this folder, keeping the `assets` folder structure.
3. Go to Settings, then Pages. Under Source pick Deploy from a branch, branch `main`, folder `/ (root)`. Save.
4. In a minute or two the site appears at `https://<your-username>.github.io/how-leaders-influence/`.

## Connect howleadersinfluence.com

1. Buy the domain at any registrar such as GoDaddy, Namecheap, Hostinger or Cloudflare.
2. The `CNAME` file already contains `howleadersinfluence.com`.
3. At the registrar, add these DNS records.

   Four A records for the root domain
   ```
   A   @   185.199.108.153
   A   @   185.199.109.153
   A   @   185.199.110.153
   A   @   185.199.111.153
   ```
   One CNAME record for www
   ```
   CNAME   www   <your-username>.github.io
   ```
4. In GitHub, Settings, Pages, type the domain under Custom domain and save.
5. Once the DNS check passes, which can take up to 24 hours, tick Enforce HTTPS.

## Email at the new domain

GitHub Pages does not provide email. For hello@howleadersinfluence.com use your registrar's email forwarding (often free) to forward to your Gmail, or Zoho Mail or Google Workspace for a full mailbox.
