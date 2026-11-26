# Sanwar Technologies: 3D scroll-film video prompts

Six clips that play back to back as one continuous film while the visitor scrolls. Works with any image-to-video tool (Kling, Higgsfield, Runway, Luma, Veo).

## Settings for every clip
- Aspect ratio **16:9**, at least **1080p**, **5 seconds** each (10s is fine for chapters 1 and 5 if you want them slower)
- Mode: **image-to-video**, with a start frame (and an end frame where noted)
- Smooth, slow camera only. No cuts, no shake, no text, no logos, no people, no hands.
- Paste the **Style line** at the end of every prompt so all six clips match.

**Style line (append to every prompt):**
> Photoreal 3D render, cinematic product-film look. Near-black void background (#07080b), a single electric-blue accent light (#3b82f6) with soft bloom and glow, frosted glass with soft reflections and rim light, subtle floating dust particles, shallow depth of field, slow smooth camera motion, high detail, no text, no letters, no logos, no people.

**Negative prompt (if your tool has one):**
> text, words, letters, watermark, logo, brand names, people, hands, faces, camera shake, fast cuts, flicker, distorted UI, extra panels, cluttered background, bright background, colors other than blue

## Step 0: make two still images first
Use text-to-image (Higgsfield Soul, Midjourney, Flux etc.) at 16:9.

**Still A, chaos:**
> Dozens of floating paper sticky notes, printed spreadsheet sheets, envelope icons and chat-bubble cards drifting and tumbling in dark empty space, scattered at different depths, softly lit in cool blue, slightly messy and overwhelming. + Style line

**Still B, the hero dashboard (most important image):**
> A single large floating 3D glass dashboard panel, slightly angled toward the camera, centered in dark space. The panel shows an abstract CRM interface made of glowing shapes only: a contact list column on the left, four pipeline columns of cards in the middle, a blue bar chart and checklist on the right. Thin glowing blue edges, frosted glass, soft blue glow underneath. + Style line

Pick the best Still B before making any video. Everything is anchored to it.

## The six clips
Chain them: start each clip from the **last frame of the previous clip** (most tools have "use last frame" or "extend"; otherwise screenshot the final frame).

**Clip 1 · Chaos** (start frame: Still A)
> Camera slowly drifts forward through a swirl of floating sticky notes, spreadsheets, envelopes and chat cards. The papers tumble and rotate slowly around the camera in a gentle vortex, a sense of overwhelming clutter. + Style line

**Clip 2 · Order** (start frame: last frame of Clip 1, end frame: Still B)
> All the floating papers, envelopes and cards are pulled toward the center as if by a magnet, shrinking and streaking into light, and merge into one glowing glass dashboard panel that forms in the middle of the frame. Camera eases back slightly as the panel settles. + Style line

**Clip 3 · Assembly** (start frame: Still B, end frame: Still B if your tool allows it)
> The glass dashboard panel separates into four parallel transparent glass layers that slide apart in depth like an exploded view: contact list layer, pipeline cards layer, tasks layer, chart layer. The camera orbits slightly to the side to show the layered depth, then the layers glide back together and lock into one panel with a soft blue pulse. + Style line

**Clip 4 · Connection** (start frame: last frame of Clip 3)
> Small glowing glass icon spheres fade in, floating around the dashboard panel at different depths: an envelope, a chat bubble, a form, a calendar, a receipt and a megaphone. Thin glowing blue lines draw themselves from each sphere and curve into the edges of the dashboard, connecting everything. Camera slowly pulls back to reveal the whole network. + Style line

**Clip 5 · Automation** (start frame: last frame of Clip 4)
> Bright pulses of blue light travel along the glowing connection lines into the dashboard on their own, one after another. On the panel a card slides from one pipeline column to the next, a contact row lights up, a checkbox fills in. Everything runs smoothly and rhythmically by itself. Camera holds steady with a very slow push in. + Style line

**Clip 6 · Calm** (start frame: last frame of Clip 5)
> The finished dashboard panel rotates very slowly in calm dark space, connection lines glowing softly in the background. The bar chart on the panel rises smoothly and a rising trend line glows. Light, peaceful, premium, a feeling of everything under control. Camera does a slow gentle orbit. + Style line

## Tips
- If a clip invents letters or fake words on the dashboard, add "abstract shapes only, no readable text" and regenerate just that clip.
- If Clip 3's layers duplicate or warp (common in AI video), skip it and send me Still B. I'll animate the layers in code instead.
- Keep the panel roughly centered in every clip. The site places captions in the lower left.

## How to send them to me
- Files named **ch1.mp4, ch2.mp4, ch3.mp4, ch4.mp4, ch5.mp4, ch6.mp4** (MP4/H.264, 16:9, 1080p or higher), plus **still-b.png**
- Upload them in this thread.
- I'll crossfade them into one film, slice it into about 400 lightweight WebP frames scrubbed by scroll, and line the captions up with each chapter. You don't need to edit anything.
