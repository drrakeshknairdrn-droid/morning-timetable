# Morning Timetable app

A student timetable that shows your first class, what is on now and what is next.
This folder builds three installable apps from one page (`www/index.html`):

| App | File you get | Works on |
|---|---|---|
| Windows | `Morning-Timetable-1.0.0-win-x64.exe` | Windows 10 and 11 |
| Mac | `Morning-Timetable-1.0.0-mac-arm64.dmg` and `...-mac-x64.dmg` | Apple chip (M1 and later) and Intel Macs |
| Android | `Morning-Timetable-Android.apk` | Android phones |

## Get the installers (no coding, free)

GitHub builds all three apps for you in the cloud. You need a free GitHub account (github.com).

1. Sign in to GitHub. Click **+** at the top right, then **New repository**. Name it `morning-timetable`, keep it **Private**, and click **Create repository**.
2. On the new repository page, click **uploading an existing file**.
3. Unzip this project on your computer. Open the unzipped folder, select **everything inside it** (including the hidden `.github` folder) and drag it into the browser. Click **Commit changes**.
   - If the `.github` folder did not upload (you can't see it in the file list): click **Add file > Create new file**, type `.github/workflows/build.yml` as the name, paste the contents of that file from this project, and commit.
4. Click the **Actions** tab. A run called **Build apps** starts by itself. Wait about 10 to 15 minutes until it shows a green tick. (If it does not start, open **Build apps** in the left list and click **Run workflow**.)
5. Go back to the main page of your repository (click the repository name at the top). On the right side, under **Releases**, click the newest release. It lists the download links:
   - `Morning-Timetable-...-win-x64.exe` for Windows
   - `Morning-Timetable-...-mac-arm64.dmg` for Apple chip Macs, `...-mac-x64.dmg` for Intel Macs
   - `Morning-Timetable-Android.apk` for Android

   Click a file to download it. To install on your phone, open this same page on the phone and tap the `.apk` link.

**To let friends or classmates download it:** in the repository, open **Settings**, scroll to the bottom, click **Change visibility**, and choose **Public**. Then anyone with your Releases page link can download the apps without a GitHub account. (The page only holds this app. There are no passwords in it.)

## Install the apps

**Windows.** Double-click the `.exe`. If Windows shows "Windows protected your PC", click **More info**, then **Run anyway**. This appears because the app is not signed with a paid certificate.

**Mac.** Open the `.dmg` that matches your Mac (arm64 for Apple chip, x64 for Intel) and drag the app into Applications. The first time, right-click the app, choose **Open**, then **Open** again.

**Android.** Copy `Morning-Timetable-Android.apk` to your phone (WhatsApp, email or a USB cable). Tap it. Android will ask you to allow installs from this source; allow it, then tap **Install**. Delete the file afterwards if you like.

## Build on your own computer instead (optional)

Install Node.js (nodejs.org), open a terminal in this folder, then:

```
npm install
npm start            # try the desktop app
npm run dist:win     # build the Windows installer (run this on Windows)
npm run dist:mac     # build the Mac installer (run this on a Mac)
```

The installers appear in the `dist` folder. The Android app needs Android Studio, so the GitHub method above is easier.

## Good to know

- Your timetable is saved inside each app on each device. It does not sync between your laptop and phone. Use **Backup and restore** (at the bottom of the app) to copy it across.
- Fonts load from the internet the first time. Offline, the app uses your system fonts and still works.
- There are no morning notifications yet. They can be added as a next step.
- To change the timetable page itself, edit `www/index.html` and upload the file again. GitHub rebuilds the apps.
