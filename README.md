# Echo releases

Windows installers for **Echo**, a private chat, voice and video app for
groups of friends. This repository only holds the signed releases and the
update manifest that Echo checks; it contains no source code.

## Installing

1. Open the [latest release](https://github.com/killr789/echo-releases/releases/latest).
2. Download `Echo_<version>_x64-setup.exe` and run it. It installs for
   your Windows user only and doesn't need administrator rights.
3. The installer isn't signed with a Windows code-signing certificate yet,
   so SmartScreen may say the publisher is unknown. Choose
   *More info → Run anyway* only if you got the link from the person who
   runs your group's Echo.

## Updates

Once installed, Echo keeps itself up to date: it checks this repository's
latest release a few seconds after it starts and every few hours, and
offers new versions at the top of its window. Nothing installs until you
click **Update now**.

Every installer here is signed with Echo's release key, and Echo checks
that signature before installing an update, so a modified file is
refused. The `.sig` file next to each installer is that signature, and
`latest.json` is the manifest Echo reads.
