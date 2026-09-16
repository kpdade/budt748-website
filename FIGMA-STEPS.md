# How to rebuild this site in Figma (beginner steps)

Goal: three frames named **Landing Page**, **About Page**, and **Contact Page** that match the
live site at https://kpdade.github.io/budt748-website/

Figma is free. Sign up at https://figma.com, then click **New design file**.

Keep these values handy — they are exactly what the website uses:

| Thing | Value |
|---|---|
| Frame size | Desktop, 1440 x 1024 |
| Background | `#140708` (near-black), with a soft green glow top-left and an orange glow top-right |
| Font | Montserrat |
| Accent green | `#A8FF35` |
| Accent orange | `#FF7A4D` (used only in gradients) |
| Heading text | `#FFFFFF` |
| Body text | `#BDB0A8` |
| Card fill | White at 5% opacity, 1px white border at 10% opacity, corner radius 18 |

---

## 1. Set up the first frame (5 minutes)

1. Press **F** (Frame tool), then in the right-hand panel click **Desktop → Desktop (1440 x 1024)**.
2. In the **Layers** panel on the left, double-click the frame name and rename it to `Landing Page`.
3. With the frame selected, find **Fill** on the right. Click the color square and type `140708`.
4. Optional glow: press **O** (Ellipse), draw a big circle off the top-left corner, fill it `A8FF35`,
   drop **opacity to 10%**, then in **Layer blur** set about **200**. Repeat top-right with `FF7A4D`.
   Right-click each → **Send to back**.

## 2. Add the 12-column grid

1. Select the frame. On the right, find **Layout grid** and click **+**.
2. Click the grid settings icon and change **Grid** to **Columns**.
3. Set: **Count 12**, **Margin 80**, **Gutter 20**.
4. Toggle the grid on and off any time with **Ctrl + G**.

## 3. Navigation bar (this is where your name goes)

1. Press **R**, draw a **38 x 38** square at the top-left, corner radius **10**, fill `A8FF35`.
   Press **T** and type `KP` on top of it in near-black (`10240A`), size 15, Bold. Group them
   (**Ctrl/Cmd + G**) — this is the logo mark.
2. Press **T** next to it and type `Kushaal Pelluru Lakshminarasimhan`.
   Montserrat **Bold**, size **18**, white.
3. Press **T** again and add three text items near the top-right: `Homepage`, `About`, `Contact`.
   Montserrat Medium, **15**, color `#BDB0A8`. Make `Homepage` white (it is the active page).
4. Select the three and press **Shift + A** (Auto Layout), gap **26**.
5. Under `Homepage`, draw a **2px** line in `A8FF35` — that is the active underline.
6. Draw a 1px line all the way across under the whole bar in white at 10% opacity.

## 4. Hero section (homepage)

1. Press **T** and type `BUDT748 · FALL 2026 · CLIENT-SIDE TECHNOLOGIES`.
   Montserrat SemiBold, **13**, color `A8FF35`, letter spacing **2.4**, all caps. This is the eyebrow.
2. Below it add the headline `LET'S CREATE A WEBSITE DESIGN`.
   Montserrat **ExtraBold**, size **66**, line height **1.1**, letter spacing **-1**, centered, white.
   - For the two-tone effect: select just the words `WEBSITE DESIGN` inside the text box, then set
     that selection's fill to `A8FF35`. (Figma can do a real gradient on text too: select the whole
     text layer, set Fill to **Linear**, and use `A8FF35` → `FF7A4D`.)
3. Add the subtitle: `Today let's create a sample website design in Figma and export its corresponding
   HTML and CSS code.` Montserrat Regular, **24**, color `#BDB0A8`, centered, max width about 760.
4. The two buttons:
   - **Get Started:** press **R**, size **W 180 / H 52**, corner radius **10**, fill `A8FF35`.
     Add **Drop shadow** under Effects. Press **T** and put `Get Started` on it, 18, Bold, `10240A`.
   - **Contact the team:** another rectangle, same height, **no fill**, 1px border white at 10%,
     radius 10, with white text at 17.
   - Select both buttons and press **Shift + A**, gap **16**.
5. Select the eyebrow, headline, subtitle and button group, press **Shift + A**, set the direction to
   **vertical**, gap around **26**, and alignment **center**.

## 5. Feature cards (still on the homepage)

1. Press **R**, draw a card about **380 x 250**, corner radius **18**, fill white at **5%**,
   1px border white at **10%**.
2. Inside it add:
   - A **42 x 42** rounded square (radius 12) filled green at 15% with `01` in `A8FF35`.
   - `Design` — Montserrat Bold, 21, white.
   - The body line — Regular, 15.5, `#BDB0A8`.
   - `FIGMA` — SemiBold, 12, letter spacing 1.4, all caps, muted.
3. Select the card and press **Ctrl/Cmd + D** twice, then change the numbers to `02` / `03` and the
   titles to `Build` and `Deploy`.
4. Select all three cards, press **Shift + A**, direction **horizontal**, gap **24**.

## 6. About page (the easy way — duplicate)

1. Click the `Landing Page` frame name in Layers, then press **Ctrl + D** (Mac: **Cmd + D**).
2. Rename the copy to `About Page`.
3. Keep the nav bar. Delete the hero buttons and the feature cards.
4. Left-align the text and change:
   - Eyebrow → `ABOUT THE COURSE`
   - Headline → `BMGT407 — INFORMATION SYSTEMS PROJECTS`, size **52**
   - Lead paragraph → the course description
5. Add three detail cards (same card style as step 5). Each gets a small green all-caps label, a big
   value, and a muted note:
   - `SEMESTER DETAILS` / `Spring 2027`
   - `PROFESSOR` / `Paul T Shapiro`
   - `TEACHING ASSISTANTS` / `Bharath Sreekumar`, `Caifu Lin`, `Sumanth Devara`
6. Give each detail card a **4px** bar down the left edge, filled `A8FF35`.

## 7. Contact page

1. Duplicate the `About Page` frame and rename it `Contact Page`.
2. Change the eyebrow to `GET IN TOUCH`, the headline to `Contact Us`, and the lead to
   `Reach out to the course team for support or inquiries.`
3. On the left, make one small row per person: a **42px** green circle with their initials, their name
   in white 16, and the email under it in muted 14.
   - `Paul T Shapiro - pshapiro@umd.edu`
   - `Bharath Sreekumar - bsreekum@umd.edu`
   - `Caifu Lin - clin0817@terpmail.umd.edu`
   - `Sumanth Devara - sdevara@umd.edu`
4. On the right, draw a big card (radius 18) and put the form inside: `Name`, `Email`, `Subject`,
   `Message` — each a rounded rectangle (radius 10, white 5% fill, 10% border) with a small muted
   label above it. Finish with the green `Submit` button.

## 8. Export

1. Click a frame, then in the right panel scroll to **Export** and click **+**.
2. Choose **JPG** (or PNG) and click **Export [frame name]**. Do this for all three frames.
3. Screenshots of the Figma canvas also work fine for showing your design work.

## 9. Optional: the AutoHTML plugin

The tutorial mentions **AutoHTML | Components to Code** for generating HTML/CSS from a frame:
main menu → **Plugins → Manage plugins…**, search for it, install, then right-click your frame →
**Plugins → AutoHTML → Generate Code**.

The site in this repo is already written by hand in clean HTML/CSS/Bootstrap, so you do not need the
generated code — it is usually messier than hand-written code. Use the plugin only if your
instructor wants to see that step.
