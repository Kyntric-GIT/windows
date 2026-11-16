# Windows 11 Web Edition

A Windows 11-inspired desktop environment that runs as a static website.

## Deploy with GitHub Pages

1. Open the repository's **Settings → Pages**.
2. Under **Build and deployment**, choose **GitHub Actions** as the source.
3. The included workflow deploys the site automatically whenever you push to `main`.
4. Open the Pages URL shown in the repository settings or in the successful Actions deployment.

## Included features

- Desktop, taskbar, Start menu and app search
- Draggable, minimizable and maximizable app windows
- File Explorer-style workspace
- Browser window (some websites block iframe embedding)
- Settings, wallpaper and accent color controls
- Terminal-style command prompt and local Notepad
- Game Library with URL-based game shortcuts

## Importing games

The Game Library can open a game at a public web URL inside a window.

For GitHub projects, the most reliable method is:

1. Publish the game repository using GitHub Pages.
2. In Windows Web Edition, open **Game Library → Import from GitHub**.
3. Paste the game's GitHub Pages URL (or its GitHub repository URL), give it a name, and save.
4. Select **Play** in the library.

A repository URL is converted to the usual `https://OWNER.github.io/REPOSITORY/` address. This assumes the game is published at that standard Pages address. Projects that are not deployed as websites cannot automatically run from their source repository. Browser games and HTML5 builds work best; native Windows `.exe` files do not run directly in a browser.

## Important limitations

This is a browser-based desktop simulation, not a real Windows installation. It cannot run arbitrary Windows applications, access the host computer's full filesystem, or bypass browser security restrictions. Files and game shortcuts stored by this first version use browser-local storage.

## Development

The first version is intentionally static: edit `index.html` and push to `main`. GitHub Pages serves it without a build step.
