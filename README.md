# Sanwar Technologies website

Open `index.html` in a browser, or serve the folder locally:

    python3 -m http.server 8000      # then visit http://localhost:8000

## Things to edit before going live
- **Contact details**: search for `EDIT:` in `index.html` (email and WhatsApp number are placeholders).
- **Results numbers**: the four stats are sample figures. Replace them and delete the "Sample figures" label.
- **Case studies and testimonials**: these are examples. Replace with real client work and quotes.
- **Contact form**: set `FORM_ENDPOINT` near the top of the script to a form service URL (for example Formspree) so messages reach your inbox.

## Adding the 3D videos
The hero currently plays an animated placeholder drawn in code. When the six chapter videos are ready:
1. Name them `ch1.mp4` ... `ch6.mp4` and put them in a `clips/` folder.
2. Convert them into frames (Claude can do this step for you):

       ffmpeg -i ch1.mp4 -i ch2.mp4 -i ch3.mp4 -i ch4.mp4 -i ch5.mp4 -i ch6.mp4 \
         -filter_complex "[0][1]xfade=duration=0.4:offset=4.6[a];[a][2]xfade=duration=0.4:offset=9.2[b];[b][3]xfade=duration=0.4:offset=13.8[c];[c][4]xfade=duration=0.4:offset=18.4[d];[d][5]xfade=duration=0.4:offset=23.0,fps=14,scale=1600:-2" \
         frames/frame_%04d.webp
   (offsets assume 5-second clips; each offset = previous offset + clip length - 0.4)
3. In `index.html`, set `window.FILM = { frames: <number of frames>, ... }` and adjust `CHAPTERS` if clip lengths differ.

The captions and chapter markers stay the same; only the background changes from the placeholder to your film.

## Deploy
Push this folder to a GitHub repository and enable GitHub Pages (Settings > Pages > Deploy from branch), or drag the folder into Netlify.

## Call booking (Cal.com)
Every "Book a free call" button opens the Cal.com popup for `hamza-manzoor-peqlsi/15min`, and a floating "Book a free call" button sits in the corner. To change the calendar, edit `CAL_LINK` and the `data-cal-link` attributes in `index.html`. If the Cal.com script is blocked (ad blockers, the claude.ai preview), the buttons open the booking page in a new tab instead.
The Contact area also shows the Cal.com calendar inline (the `#book` section), in dark mode. If Cal.com can't load, a button to open the booking page appears instead.
