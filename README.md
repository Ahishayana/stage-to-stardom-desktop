# Stage to Stardom: desktop apps

This folder builds the game as a real app for Windows (.exe), Mac (.app in a zip) and Linux (AppImage).
GitHub builds all three for free.

## Build

1. On github.com, create a new repository called `stage-to-stardom-desktop`.
2. Click **uploading an existing file** and drag in everything inside this folder, including the hidden
   `.github` folder. Click **Commit changes**.
   - If the `.github` folder is hidden on your computer, use **Add file → Create new file**, name it
     `.github/workflows/build-desktop.yml`, and paste in that file's contents.
3. Open the **Actions** tab. **Build desktop apps** runs on its own (about 5 to 10 minutes).
4. When it shows a green tick, open the run and download the three files under **Artifacts**:
   - **StageToStardom-windows-latest**: contains `Stage to Stardom 1.0.0.exe`
   - **StageToStardom-macos-latest**: contains the Mac app as a `.zip`
   - **StageToStardom-ubuntu-latest**: contains the Linux `.AppImage`

## What players will see

The apps are not code-signed (that costs money), so the first launch shows a warning:
- **Windows:** "Windows protected your PC". Click **More info → Run anyway**.
- **Mac:** right-click the app, choose **Open**, then **Open** again.

## Updating the game

Replace `index.html` with the newer game file, raise `version` in `package.json`, and upload both.
GitHub builds new apps automatically. Saves are kept between versions.
