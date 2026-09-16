# How to rebuild this site in Figma (beginner steps)

Goal: three frames named **Landing Page**, **About Page**, and **Contact Page** that match the
live site at https://kpdade.github.io/budt748-website/

Figma is free. Sign up at https://figma.com, then click **New design file**.

Keep these values handy — they are exactly what the website uses:

| Thing | Value |
|---|---|
| Frame size | Desktop, 1440 x 1024 |
| Background | `#240A0A` (dark maroon) |
| Font | Montserrat |
| Accent green | `#A8FF35` |
| Body text color | `#CBBFB6` |
| Heading text color | `#FFFFFF` |

---

## 1. Set up the first frame (5 minutes)

1. Press **F** (Frame tool), then in the right-hand panel click **Desktop → Desktop (1440 x 1024)**.
2. In the **Layers** panel on the left, double-click the frame name and rename it to `Landing Page`.
3. With the frame selected, find **Fill** on the right. Click the color square and type `240A0A`.

## 2. Add the 12-column grid

1. Select the frame. On the right, find **Layout grid** and click **+**.
2. Click the grid settings icon (⋮⋮⋮ or the slider icon) and change **Grid** to **Columns**.
3. Set: **Count 12**, **Margin 80**, **Gutter 20**.
4. Toggle the grid on and off any time with **Ctrl + G** (Mac: **Ctrl + G**).

## 3. Navigation bar (this is where your name goes)

1. Press **T** (Text tool) and click near the top-left of the frame. Type `Kushaal Pelluru Lakshminarasimhan`.
2. With the text selected, set the font to **Montserrat**, weight **Bold**, size **24**, color **white**.
3. Press **T** again and add three separate text items near the top-right: `Homepage`, `About`, `Contact`.
   Set each to Montserrat Regular, 16, color `#CBBFB6`.
4. Select all three with Shift-click, then press **Shift + A** (Auto Layout). Set the spacing between
   them to **28**. This keeps them evenly spaced.

## 4. Hero section (homepage)

1. Press **T**, draw a wide text box across the middle, and type `LET'S CREATE A WEBSITE DESIGN`.
   Montserrat **Bold**, size **60**, color white, alignment **center**.
2. Below it add: `Today let's create a sample website design in Figma and export its corresponding
   HTML and CSS code.` Montserrat Regular, size **32**, color `#CBBFB6`, center.
3. Select both text boxes and press **Shift + A**, then set the gap to **30**.
4. The button:
   - Press **R** (Rectangle), draw it, then set **W 180** and **H 57** in the right panel.
   - Set **Fill** to `A8FF35`.
   - Find **Corner radius** and set it to **10**.
   - Under **Effects**, click **+** and choose **Drop shadow**.
   - Press **T**, type `Get Started` on top of it, size **24**, color near-black (`10240A`).
   - Select the rectangle and the text, then **Ctrl/Cmd + G** to group them.
5. Select everything in the hero and use the alignment buttons at the top-right to **center horizontally**.

## 5. About page (the easy way — duplicate)

1. Click the `Landing Page` frame name in the Layers panel, then press **Ctrl + D** (Mac: **Cmd + D**).
2. Rename the copy to `About Page`.
3. Delete the hero button and the feature cards.
4. Change the big heading to `BMGT407 - INFORMATION SYSTEMS PROJECTS` and left-align it (size 48).
5. Under it, add the course paragraph, then three text blocks:
   - `Semester Details - Spring 2027`
   - `Professor - Paul T Shapiro`
   - `Teaching Assistants - Bharath Sreekumar, Caifu Lin, Sumanth Devara`
6. Select the three blocks and press **Shift + A** so they sit in a neat row or column.

## 6. Contact page

1. Duplicate the `About Page` frame and rename it `Contact Page`.
2. Change the heading to `Contact Us` and the subtitle to
   `Reach out to the course team for support or inquiries.`
3. Replace the details with the contact list:
   - `Paul T Shapiro - pshapiro@umd.edu`
   - `Bharath Sreekumar - bsreekum@umd.edu`
   - `Caifu Lin - clin0817@terpmail.umd.edu`
   - `Sumanth Devara - sdevara@umd.edu`

## 7. Export

1. Click a frame, then in the right panel scroll to **Export** and click **+**.
2. Choose **JPG** (or PNG) and click **Export [frame name]**. Do this for all three frames.
3. Screenshots of the Figma canvas also work fine for showing your design work.

## 8. Optional: the AutoHTML plugin

The tutorial mentions **AutoHTML | Components to Code** for generating HTML/CSS from a frame:
main menu → **Plugins → Manage plugins…**, search for it, install, then right-click your frame →
**Plugins → AutoHTML → Generate Code**.

The site in this repo is already written by hand in clean HTML/CSS/Bootstrap, so you do not need the
generated code — it is usually messier than hand-written code. Use the plugin only if your
instructor wants to see that step.
