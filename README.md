# Mindscape

A living visual workspace for projects, thoughts and research, by **Zenith AI**.

[Download the desktop preview](https://github.com/Razahamid2003/mindscape-releases/releases/tag/v0.1.1-preview.1) · [Get help or report a problem](https://github.com/Razahamid2003/mindscape-releases/issues)

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

Close Mindscape before installing an update. Reopening the installed application focuses its existing window instead of opening a second copy against the same workspace.

Edits are saved on the device while offline and queued for sync when connectivity returns. Google sync uses a quota-limited free service. If the shared quota is exhausted, work remains saved on the device and retries back off. Local work remains available without signing in.

## Manage large maps

In Outline, **Select thoughts** enables checkboxes, Shift-click range selection and **Select all shown**. In Graph, use **Select** or Shift-click. **Delete selected** opens a permanent-deletion review: keep surviving children or include whole branches. The central thought is protected, and a changed hierarchy invalidates the review. Deletion cannot be undone; export a backup first if you may need the content later.

Separated branches keep independent hierarchies. They can cross-link to any thought in the project without reparenting it. Use **Move to branch** when you want to change a parent. **Add child** closes when you click outside its popup or select another thought.

## Files, backups and privacy

File copies remain local by default. Uploads to Google Drive require a separate connection and a deliberate upload action. Automatic backups are opt-in per project. A link to a local file still refers to the file on the computer where it was linked.

Workspace content is stored locally and, when cloud sync is enabled, in the account's Firebase workspace. This is not end-to-end encrypted sync. Google sign-in credentials use the operating system's secure storage when it is available. Mindscape currently has no analytics or crash-report upload feature.

## Preview updates and verification

Install updates manually from this repository for now. Automatic verified downloads and an explicit **Restart and update** action remain planned; this preview does not silently replace itself.

The release includes SHA-256 checksums, dependency SBOMs and build provenance. Third-party license notices are included inside each application. The application source is private; this repository contains downloads, release notes, support information and a small release-publishing workflow. Distributed desktop code can still be inspected, so private account credentials and release keys are never included in the application payload.

## Help

Open an issue with your operating system, processor type and Mindscape version. Describe what happened and what you expected. Avoid attaching private workspace content or sign-in credentials to a public issue.
