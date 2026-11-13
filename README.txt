H2 ACADEMY – HOW TO ADD VIDEOS

Folder layout
  index.html            the website (open it in a browser)
  assets/
    logohydro.mp4       your logo video
    videos.js           the list of videos to display  <-- edit this
    videos/             put your video files here
    images/             put cover images here

Add a video
  1. Copy lesson1.mp4 into assets/videos/
  2. Open assets/videos.js and add:
       { title: "Lesson 1", file: "assets/videos/lesson1.mp4", time: "3:20" },
  3. Reload index.html.

Tips
  - Use .mp4 (H.264 video + AAC audio) so every browser can play it.
  - Keep each file under about 100 MB, or upload to a video host.
  - To publish, upload the whole folder to any web host.

HOMEPAGE BACKGROUND (photos and videos)
  Open assets/hero.js and list the photos and videos you want behind the title.
    { type: "image", src: "assets/images/my-photo.jpg" }
    { type: "video", src: "assets/videos/my-clip.mp4", poster: "assets/images/my-clip.jpg" }
  Photos show for 6 seconds (change with seconds: 8). Videos play to the end, muted.

PAGES
  index.html     homepage with the background slideshow
  courses.html   course list and video playlist (edit assets/videos.js)

RESEARCH & PUBLICATIONS (live feed)
  index.html loads recent papers from OpenAlex, and falls back to Crossref if
  OpenAlex does not answer. No API key or backend is needed. It needs an
  internet connection. Optional: set MAILTO to your email in the script at the
  bottom of index.html for faster "polite" API access.
  To change the topics, edit the CATS list in that same script.
