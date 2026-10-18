# AI Receptionist Showcase

A black-and-white showcase site for the AI Receptionist project by Akash Nagar. Plain HTML, CSS and JavaScript — no build step, no backend, free on GitHub Pages.

## Folder structure

```text
ai-receptionist-showcase/
├── index.html
├── README.md
└── videos/
    ├── ai-receptionist-1.mp4   <- you add this
    ├── ai-receptionist-2.mp4   <- you add this
    └── ai-receptionist-3.mp4   <- you add this
```

## Add your videos

Copy your videos into `videos/` with exactly these names. The site shows a clear error message until they are there.

## Preview locally

Open `index.html` in your browser, or from this folder run:

```bash
python3 -m http.server 8000
```

then visit http://localhost:8000.

## Change video titles

Open `index.html` and edit the `VIDEOS` list (titles and file names; add or remove lines to change the number of videos) near the bottom (marked `EDIT HERE`).

## Check file sizes first

Check all three videos. GitHub blocks regular files over **100 MB**. If a video is bigger, compress a *copy* (keep your original) to MP4 with H.264 video and AAC audio, about 720p. With ffmpeg:

```bash
ffmpeg -i original.mp4 -c:v libx264 -vf scale=-2:720 -crf 26 -preset slow -c:a aac -b:a 128k -movflags +faststart ai-receptionist-1.mp4
```

## Publish with GitHub Pages (free)

1. On GitHub, create a **public** repository named `ai-receptionist-showcase`.
2. Upload `index.html`, `README.md` and the `videos` folder (with all three videos) to the `main` branch.
3. Go to **Settings → Pages**.
4. Under "Build and deployment", choose **Deploy from a branch**.
5. Select branch **main** and folder **/(root)**, then **Save**.
6. Wait a minute or two, then open:

`https://YOUR-GITHUB-USERNAME.github.io/ai-receptionist-showcase/`

Replace `YOUR-GITHUB-USERNAME` with your real GitHub username. All paths are relative, so it works at this project URL.

## Before you publish

- In the "Technology stack" section of `index.html`, keep only technologies you actually used.
- Optional: add your GitHub repo link in the footer (a commented example is included).
