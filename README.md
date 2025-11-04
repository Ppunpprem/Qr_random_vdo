# Qr_random_vdo

This simple single-page site plays one random video from a configured list and then redirects the user to a website when the video ends (or when the user skips).

How to use

- Open `index.html` and edit the `videos` array in the script to include direct URLs to your video files (MP4, WebM, etc.).
- By default the page will redirect to the URL in `DEFAULT_REDIRECT` inside the script. You can override it at runtime by appending `?next=` to the page URL (URL-encoded).
  - Example: `index.html?next=https%3A%2F%2Fexample.com`

Notes

- Many browsers require muted playback for autoplay; the player starts muted. The user can unmute with the Unmute button.
- Do not use drive.google.com _share_ page URLs — the video src must point to a raw video file URL (hosted on a CDN, S3, or similar).
- If no videos are configured, the page will show a message and redirect shortly after.

Customization ideas

- Add more controls or a loading spinner.
- Use a server-side endpoint that returns a random video URL so you don't need to edit the page when updating videos.

License: MIT
