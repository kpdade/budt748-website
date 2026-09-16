# How to rebuild this site in Figma (beginner steps)

Goal: three frames named **Landing Page**, **About Page**, and **Contact Page** that match the
live site at https://kpdade.github.io/budt748-website/

Figma is free. Sign up at https://figma.com, then click **New design file**.

Keep these values handy — they are exactly what the website uses:

| Thing | Value |
|---|---|
| Frame size | Desktop, 1440 x 1024 |
| Page background | `#FFFFFF`, with a very light `#F6F8FB` band across the top ~420px |
| Font | Montserrat |
| Navy (headings, buttons, logo) | `#13355C` (darker shade `#0D2440`) |
| Accent blue (small labels, links) | `#2F6FB0` |
| Body text | `#55647A` |
| Heading text | `#101A2B` |
| Borders | `#E3E8EF` (stronger: `#CFD8E4`) |
| Card style | White fill, 1px `#E3E8EF` border, corner radius 16, very soft shadow |

The palette is deliberately restrained: navy and slate on white, one blue accent, no bright colors.

---

## 1. Set up the first frame (5 minutes)

1. Press **F** (Frame tool), then in the right-hand panel click **Desktop → Desktop (1440 x 1024)**.
2. In the **Layers** panel on the left, double-click the frame name and rename it to `Landing Page`.
3. With the frame selected, find **Fill** on the right, click the color square and type `FFFFFF`.
4. For the soft top band: press **R**, draw a rectangle across the full width, about 420 tall, fill it
   `F6F8FB`, then right-click → **Send to back**.

## 2. Add the 12-column grid

1. Select the frame. On the right, find **Layout grid** and click **+**.
2. Click the grid settings icon and change **Grid** to **Columns**.
3. Set: **Count 12**, **Margin 80**, **Gutter 20**.
4. Toggle the grid on and off any time with **Ctrl + G**.

## 3. Navigation bar (this is where your name goes)

1. Press **R**, draw a **38 x 38** square at the top-left, corner radius **8**, fill `13355C`.
   Press **T** and type `KP` on top of it in white, size 14, Bold. Group them (**Ctrl/Cmd + G**).
2. Press **T** next to it and type `Kushaal Pelluru Lakshminarasimhan`.
   Montserrat **Bold**, size **17**, color `#101A2B`.
3. Press **T** again and add three text items near the top-right: `Homepage`, `About`, `Contact`.
   Montserrat Medium, **15**, color `#55647A`. Make `Homepage` navy (`#13355C`) — it is the active page.
4. Select the three and press **Shift + A** (Auto Layout), gap **26**.
5. Under `Homepage`, draw a **2px** line in `13355C` — that is the active underline.
6. Draw a 1px line all the way across under the whole bar in `E3E8EF`.

## 4. Hero section (homepage)

1. Press **T** and type `BUDT748 · FALL 2026 · CLIENT-SIDE TECHNOLOGIES`.
   Montserrat Bold, **12**, color `2F6FB0`, letter spacing **2.2**, all caps. This is the eyebrow.
2. Below it add the headline `LET'S CREATE A WEBSITE DESIGN`.
   Montserrat **Bold**, size **60**, line height **1.12**, letter spacing **-0.8**, centered,
   color `#0D2440`.
   - Select just the words `WEBSITE DESIGN` inside the text box and set that selection's color to
     `2F6FB0`, so the headline reads in two tones.
3. Add the subtitle: `Today let's create a sample website design in Figma and export its corresponding
   HTML and CSS code.` Montserrat Regular, **21**, color `#55647A`, centered, max width about 720.
4. The two buttons:
   - **Get Started:** press **R**, size **W 180 / H 50**, corner radius **10**, fill `13355C`.
     Press **T** and put `Get Started` on it, 16, SemiBold, white.
   - **Contact the team:** another rectangle, same height, fill white, 1px border `CFD8E4`,
     radius 10, text `#101A2B` at 16.
   - Select both buttons and press **Shift + A**, gap **14**.
5. Select the eyebrow, headline, subtitle and button group, press **Shift + A**, direction
   **vertical**, gap about **24**, alignment **center**.

## 5. Feature cards (still on the homepage)

1. Press **R**, draw a card about **380 x 250**, corner radius **16**, fill **white**,
   1px border `E3E8EF`. Under **Effects** add a **Drop shadow**: Y 1, Blur 2, black at 6%.
2. Inside it add:
   - A **40 x 40** rounded square (radius 8) filled `EEF4FA` with `01` in navy `13355C`.
   - `Design` — Montserrat Bold, 20, `#101A2B`.
   - The body line — Regular, 15.5, `#55647A`.
   - A 1px `E3E8EF` divider, then `FIGMA` — SemiBold, 11.5, letter spacing 1.3, all caps, `#8A97A8`.
3. Select the card and press **Ctrl/Cmd + D** twice, then change the numbers to `02` / `03` and the
   titles to `Build` and `Deploy`.
4. Select all three cards, press **Shift + A**, direction **horizontal**, gap **24**.

## 6. The navy panel (bottom of the homepage)

1. Press **R**, draw a wide block, corner radius **16**, fill `13355C`.
2. Add `Built with Bootstrap 5` in white Bold 27, and a line of body copy in white at 78% opacity.
3. On the right, add a **white** button with navy text reading `See the course`.

## 7. About page (the easy way — duplicate)

1. Click the `Landing Page` frame name in Layers, then press **Ctrl + D** (Mac: **Cmd + D**).
2. Rename the copy to `About Page`.
3. Keep the nav bar. Delete the hero buttons, the feature cards and the navy panel.
4. Left-align the text and change:
   - Eyebrow → `ABOUT THE COURSE`
   - Headline → `BMGT407 — INFORMATION SYSTEMS PROJECTS`, size **46**
     (put `INFORMATION SYSTEMS PROJECTS` in the accent blue)
   - Lead paragraph → the course description
5. Add three detail cards (same card style as step 5). Each gets a small blue all-caps label, a big
   value in `#101A2B`, and a muted note:
   - `SEMESTER DETAILS` / `Spring 2027` / `Capstone term`
   - `PROFESSOR` / `Paul T Shapiro` / `Course instructor`
   - `TEACHING ASSISTANTS` / `Bharath Sreekumar`, `Caifu Lin`, `Sumanth Devara`
6. Give each detail card a **3px** bar down the left edge, filled `13355C`.

## 8. Contact page

1. Duplicate the `About Page` frame and rename it `Contact Page`.
2. Change the eyebrow to `GET IN TOUCH`, the headline to `Contact Us` (with `Us` in accent blue),
   and the lead to `Reach out to the course team for support or inquiries.`
3. On the left, make one small white card per person: a **42px** circle filled `EEF4FA` with their
   initials in navy, their name in `#101A2B` 16, and the email under it in `#55647A` 14.
   - `Paul T Shapiro - pshapiro@umd.edu`
   - `Bharath Sreekumar - bsreekum@umd.edu`
   - `Caifu Lin - clin0817@terpmail.umd.edu`
   - `Sumanth Devara - sdevara@umd.edu`
4. On the right, draw a big white card (radius 16) and put the form inside: `Name`, `Email`,
   `Subject`, `Message` — each a rounded rectangle (radius 8, white fill, 1px `CFD8E4` border) with a
   small muted label above it. Finish with the navy `Submit` button.

## 9. Export

1. Click a frame, then in the right panel scroll to **Export** and click **+**.
2. Choose **JPG** (or PNG) and click **Export [frame name]**. Do this for all three frames.
3. Screenshots of the Figma canvas also work fine for showing your design work.

## 10. Optional: the AutoHTML plugin

The tutorial mentions **AutoHTML | Components to Code** for generating HTML/CSS from a frame:
main menu → **Plugins → Manage plugins…**, search for it, install, then right-click your frame →
**Plugins → AutoHTML → Generate Code**.

The site in this repo is already written by hand in clean HTML/CSS/Bootstrap, so you do not need the
generated code — it is usually messier than hand-written code. Use the plugin only if your
instructor wants to see that step.
