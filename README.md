# moonhug-editor.github.io

The front page of [MoonHug Editor](https://github.com/MoonHug-Editor/moonhug), served by GitHub Pages at https://moonhug-editor.github.io/.

## Files

- `index.html` is the page: plain HTML, no build step, no script.
- `style.css` is its stylesheet.
- `media/` holds the images the page serves: the logo (a copy of `readme_files/Logo1.png` from the editor repo) and the favicon (the logo at 64 px).
- `.nojekyll` tells Pages to serve the files as they are, without running Jekyll.

Every link into the editor repo is a full GitHub URL on `main`. The version badge comes from shields.io and the video thumbnails from YouTube, so neither is updated by hand.

## Preview

Serve the folder and open http://localhost:7280:

```bash
python3 -m http.server 7280
```

A double-clicked `index.html` also works in most browsers, since every path in the page is relative.

## Publishing

Pages serves the `main` branch as it is. The repository setting is made once: Settings → Pages → Build and deployment → Source: Deploy from a branch, Branch: `main`, folder `/ (root)`. A push to `main` goes live about a minute later.

## Content

The page follows the editor's [Architecture](https://github.com/MoonHug-Editor/moonhug/blob/main/docs/core/Architecture.md): the three layers (libs, Editor, plugins), the plugins with Engine and App as special roles, then the prebuild that turns attributes into code. After the videos come the local documentation (`make docs OPEN=1`, see the editor's [Documentation](https://github.com/MoonHug-Editor/moonhug/blob/main/docs/general/Documentation.md)) and a Get started link to Install, Build and Run. A change to one of those in the editor repo changes the matching section here. The plugin tiles list the plugins in the editor repo's `plugins/` folder except the examples and the app.
