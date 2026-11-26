# Mindscape

A living visual workspace for projects, thoughts and research, by **Zenith AI**.

[Download the desktop preview](https://github.com/Razahamid2003/mindscape-releases/releases/tag/v0.1.4-preview.1) · [Get help or report a problem](https://github.com/Razahamid2003/mindscape-releases/issues)

## Choose your download

| Computer | Download | Installation |
|---|---|---|
| Windows, Intel/AMD 64-bit | Windows `.exe` | Run the setup application; choose installation for your account. |
| Mac with an Apple chip | macOS `arm64.dmg` | Open the disk image and drag Mindscape to Applications. |
| Mac with an Intel chip | macOS `x64.dmg` | Open the disk image and drag Mindscape to Applications. |
| Linux, Intel/AMD 64-bit | Linux `.AppImage` | Mark the file executable in your file manager, then open it. |
| Debian/Ubuntu, Intel/AMD 64-bit | Linux `.deb` | Open with your package installer. |

On a Mac, **Apple menu → About This Mac** shows whether you have an Apple chip or an Intel processor. ARM Windows and ARM Linux are not validated release targets yet.

Use the Debian package on Ubuntu/Debian systems that restrict unprivileged user namespaces; it installs Electron's sandbox helper correctly. AppImage availability depends on the distribution's FUSE and sandbox support. Do not use a `--no-sandbox` workaround.

These are **unsigned/ad-hoc preview builds**. Windows may show an unknown-publisher warning; macOS may block first launch because Developer ID signing and notarization are not present. The publisher name in application metadata is Zenith AI; it is not an OS-verified signing identity. Do not disable your computer's security protections globally. A signed, notarized stable release is a separate release milestone.

## Open the same workspace on another computer

1. Install Mindscape and open **Account & sync**.
2. Choose **Sign in with Google** and complete sign-in in your browser.
3. Use the same Google account as on your original computer. Account-synced projects download automatically.

You do not need Node.js, a terminal, Firebase settings or a configuration file. On the original computer, add any device-only projects to the account through Account & sync before expecting them on another device.

Version **0.1.4-preview.1** adds shared projects, collaborative rich-text notes and adaptive graph performance while retaining the child-visibility fix and verified updater. Existing projects, Google sign-in and offline changes remain in the same data directory. Reopening Mindscape focuses its existing window instead of opening a second copy against the same workspace.

Edits are saved on the device while offline and queued for sync when connectivity returns. Google sync uses a quota-limited free service. If the shared quota is exhausted, work remains saved on the device and retries back off. Local work remains available without signing in.

## Manage large maps

Folded branches show an arrow and a `+N` hidden-thought count on their canvas label. Select the label or node to expand it. **Show hidden** clears folds, hidden groups and filters in one click. Selecting a deep branch reveals its immediate children; zooming out still reduces small details. Find and Add Child reveal the thought you choose.

In Outline, **Select thoughts** enables checkboxes, Shift-click range selection and **Select all shown**. In Graph, use **Select** or Shift-click. **Delete selected** opens a permanent-deletion review: keep surviving children or include whole branches. The central thought is protected, and a changed hierarchy invalidates the review. Deletion cannot be undone; export a backup first if you may need the content later.

Separated branches keep independent hierarchies. They can cross-link to any thought in the project without reparenting it. Use **Move to branch** when you want to change a parent. **Add child** closes when you click outside its popup or select another thought.

## Shared projects and scene performance

Create an organization using **Team**, then invite a member using their Google email. Invitations are single-use, with Owner, Editor and Viewer access. Sharing creates an explicit copy of the chosen project; its private original remains private. File contents and local paths are excluded from that copy.

Members can edit a shared map and its notes together, with live cursors and selections. Offline note edits merge when the connection returns. Conflicting graph edits open a review rather than silently replacing another person's work. Note history and local recovery protect drafts. Collaborators need a current Mindscape version and must sign in with the Google account named in their invitation.

In Appearance, choose the adaptive scene setting or battery-saving mode to reduce ambient animation and particle work. Camera movement stays responsive. Firebase remains on its quota-limited free plan; an exhausted shared allowance can delay live updates, while local edits remain saved. This preview does not promise an unlimited team size.

## Files, backups and privacy

File copies remain local by default. Uploads to Google Drive require a separate connection and a deliberate upload action. Automatic backups are opt-in per project. A link to a local file still refers to the file on the computer where it was linked.

Workspace content is stored locally and, when cloud sync is enabled, in the account's Firebase workspace. This is not end-to-end encrypted sync. Google sign-in credentials use the operating system's secure storage when it is available. Mindscape currently has no analytics or crash-report upload feature.

## Preview updates and verification

Starting with **0.1.2**, Mindscape checks for updates shortly after opening and approximately every six hours. New updates download automatically from this public repository, without Google sign-in or configuration files. Open **Workspace menu → App updates** in V2 or **Updates** in V1 to see progress, release notes, retry, or show a verified download.

Installation always needs your approval in a native confirmation dialog. **Later** keeps Mindscape open and also prevents installation on ordinary quit. Before installation, open notes must save successfully; Mindscape creates local recovery copies and preserves pending offline changes.

- **Windows:** after approval, the per-user installer updates the existing application and restarts it. Windows may request system approval.
- **Linux AppImage:** after approval, the image is replaced and Mindscape restarts. One `.previous` image remains for recovery. Keep the AppImage in a folder you own and can write to.
- **macOS:** the verified disk image opens after approval and Mindscape closes. Drag the replacement into Applications, replace the existing app, and reopen it. This free preview keeps the final installation step visible.
- **Debian/Ubuntu:** the verified package opens in the system installer after approval. Authorize installation and reopen Mindscape. If no package installer is available, Mindscape reveals the verified file and stays open.

### Update on Linux

For an existing Mindscape **0.1.2 or newer**, open **Workspace menu → App updates → Check for updates**. Wait for **0.1.4** to finish downloading and verifying.

- **AppImage:** choose **Install & restart…**, then approve the confirmation. Keep the AppImage in a writable folder owned by your account.
- **Debian/Ubuntu:** choose **Review & install…**, approve the confirmation, finish the system package installer and reopen Mindscape. Use **Show download** if you need to locate the verified package.

For an older installation or a manual update, download [Mindscape-0.1.4-preview-linux-amd64.deb](https://github.com/Razahamid2003/mindscape-releases/releases/download/v0.1.4-preview.1/Mindscape-0.1.4-preview-linux-amd64.deb). Close Mindscape and open that file in your package installer to install it over the current version. If you saved it in Downloads, you can also run:

```sh
cd ~/Downloads
sudo apt install ./Mindscape-0.1.4-preview-linux-amd64.deb
```

Reopen Mindscape afterward. Keep the existing application data; no uninstall or configuration copying is needed. If you are signed out, use the same Google account to retrieve account-synced projects. Device-only projects remain on the computer where they were created.

The update feed is signed with Ed25519. Trust keys are built into the installed app; every downloaded file is checked against its signed SHA-256 digest, device target and size, and checked again before installation. These free release signatures authenticate the download; they do not replace Windows publisher certificates or Apple Developer ID/notarization. Interrupted downloads can be retried and verified downloads can be installed offline.

The release includes SHA-256 checksums, dependency SBOMs and build provenance. Third-party license notices are included inside each application. The application source is private; this repository contains downloads, release notes, support information and a small release-publishing workflow. Distributed desktop code can still be inspected, so private account credentials and release keys are never included in the application payload.

## Help

Open an issue with your operating system, processor type and Mindscape version. Describe what happened and what you expected. Avoid attaching private workspace content or sign-in credentials to a public issue.
