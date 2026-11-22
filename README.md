# Echo

**Private chat, voice and video for groups of friends, on Windows.**
Messages and calls go straight between your computers, encrypted. Free,
no account, no email, no subscription.

This page is where you download Echo. It holds only the finished installers
(no source code).

### ⬇️ [Download Echo for Windows](https://github.com/killr789/echo-releases/releases/latest/download/Echo-setup.exe)

That link always gets the newest version. Windows 10 or 11, 64-bit.

---

## Quick start (about 2 minutes)

1. [Download Echo](https://github.com/killr789/echo-releases/releases/latest/download/Echo-setup.exe) and open the file.
2. If Windows warns you, click **More info → Run anyway** (see [why](#windows-warns-me-about-the-download)).
3. Pick a username and a display name. That's your account; nothing else is needed.
4. Go to **Friends → Add friend**, click **Copy link**, and send the link to your friend (WhatsApp, Discord, anything).
5. Your friend clicks the link: Echo opens and asks them to confirm. You get a popup: click **Accept**. Done: you can chat and call.

The detailed steps follow.

---

## 1. Download

**Easiest:** click
[**Download Echo for Windows**](https://github.com/killr789/echo-releases/releases/latest/download/Echo-setup.exe).

**Or from the releases page:**

1. Open the [latest release](https://github.com/killr789/echo-releases/releases/latest).
2. Scroll down to **Assets** (click it if it's folded).
3. Click **`Echo-setup.exe`** (or `Echo_<version>_x64-setup.exe`; they're the same file).

Leave the other files alone: the `.sig` file and `latest.json` are for Echo's
automatic updates, not for you.

### My browser blocks the download

Edge and Chrome sometimes say a new program "isn't commonly downloaded".

- **Edge:** point at the download, click **⋯ → Keep**, then **Show more → Keep anyway**.
- **Chrome:** click the download's arrow (or **⋮**) and choose **Keep**.

## 2. Install

1. Open **`Echo-setup.exe`** (in your Downloads folder).
2. **Windows warns you** ("Windows protected your PC"): click **More info**,
   then **Run anyway**.
3. Follow the installer. It installs for your Windows user only and needs no
   administrator rights. Start Echo from the installer's last page or the
   Start menu.

### Windows warns me about the download

Echo isn't signed with a paid Microsoft code-signing certificate, so Windows
doesn't know the publisher yet. That's the only reason for the warning. Only
run it if you got the link from someone you trust. Echo's own updates are
signed with its release key and checked before they install.

## 3. First start

1. Choose a **username** (like `ali`) and a **display name** (what friends see).
2. Click **Create identity**. Echo makes your identity on your PC: no email, no password,
   no server account. It's encrypted with your Windows account.

### "Windows Defender Firewall has blocked some features"

If you see this (usually when you turn on hosting a server), tick **both**
**Private networks** and **Public networks**, then click **Allow access**.
Windows often treats home Wi-Fi as "public", and if only "Private" is ticked,
friends can't reach you.

## 4. Add your friend

You need each other once; after that Echo finds them by itself.

**You:**

1. Click **Friends** (top left) → **Add friend**.
2. Under **Your invite link**, click **Copy link**. It starts with
   `https://killr789.github.io/echo-releases/add/#…`.
3. Send it to your friend however you like.

**Your friend:** clicks the link. The browser asks to open Echo (allow
it), and Echo shows who invited them: they click **Send friend request**.
No Echo yet? The page has the download: install it, create a profile, then
click the link again.

**You again:** a popup says they want to be your friend: click **Accept**
(or **Deny**). If you closed it, it's under **Friends → Pending**.

Pasting the link (or an Echo ID) into **Friends → Add friend** works too.

When you're both online, the conversation header shows **Direct** (or
**Relayed**), and messages go straight between your PCs.

### How Echo finds your friend

You don't need to set anything up:

- **Public relays (on by default):** Echo meets your friends through free
  public relays. They only pass encrypted messages along, and every Echo
  user's messages look alike to them: they can't read them, or see which
  Echo user you are or who your friends are. They do see your IP address
  (as any website does) and when you're online. One switch turns them off:
  **Settings → Privacy & security**. You both need Echo 0.1.5 or newer for
  this.
- **Your own server (optional):** one friend can tick **Settings → Network →
  Host a server on this PC**. Echo opens the port on the router by itself
  (UPnP) and shows the address; the invite includes it. This also gives
  friends on strict networks (some mobile connections) a relay through the
  host.

## Share your screen with sound

In a call or voice channel, click the **screen** button. Pick **Clear
text** (documents, code) or **Smooth motion** (games, videos), keep
**Include sound** ticked, then click **Choose what to share**. Windows only
shares sound with an **entire screen**: pick your screen and tick the sound
box it shows. Friends hear your computer's sound in stereo (never their own
voices back) and can set its volume on your screen's picture.

Tip: use headphones, so your microphone doesn't pick up the sound a second
time.

## 5. Updates

Echo updates itself. When a new version is out, a bar appears at the top of
the window: **Echo x.y.z is available → Update now**. It checks the update's
signature, installs it and restarts Echo. Nothing installs unless you click.

You can also check by hand: **Settings → About Echo → Check for updates**.

## Problems?

**A yellow bar says RivaTuner's overlay can crash Echo.**
RivaTuner Statistics Server (part of MSI Afterburner) hooks into Echo's window
and can crash it. Click **How to fix** in the bar. In short: open RivaTuner →
**Add** → choose `msedgewebview2.exe` under
`C:\Program Files (x86)\Microsoft\EdgeWebView\Application\<version>\` → set
**Application detection level** to **None** → restart Echo. Your games keep
their overlay.

**My friend shows as offline, or "Can't connect".**

- Make sure you're **both on the latest version** (Settings → About Echo).
- In **Settings → Network**, check that **Public relays** says connected.
- If one of you hosts a server and Echo says **Windows Firewall is blocking
  Echo**, click **Firewall settings**, find Echo and tick **Public**.
- Restart Echo on both PCs.

**Clicking an invite link doesn't open Echo.**
Make sure Echo 0.1.5 or newer is installed, then click **Open in Echo** on
the page again. Or copy the link and paste it into **Friends → Add friend**.

**Echo's window goes blank or closes.**
Update to the latest version, and see the RivaTuner tip above.

## Uninstall

**Windows Settings → Apps → Installed apps → Echo → Uninstall.**
The uninstaller asks whether to delete Echo's data. Leave that unticked if
you might come back: your identity, friends and messages are in it.

## Is it really free?

Yes. There's no server to pay for. Echo runs on your PCs, and these
downloads are hosted by GitHub for free.

## Files from friends

Echo marks the files you save as downloaded from the internet, so Windows
SmartScreen and your antivirus check them before they open, and it asks
before saving programs and scripts. Friends' PCs can be hacked too: only
open programs you expected.

## For the curious

Every installer here is signed with Echo's release key, and Echo checks that
signature before it installs an update, so a modified file is refused. The
`.sig` file next to each installer is that signature, and `latest.json` is
the list Echo reads to find updates.

## Contributors

- [**killr789**](https://github.com/killr789): creator and maintainer
- **Claude** (Anthropic's AI): co-author of the code, including hosting
  across the internet, invite links, public relays and their privacy,
  screen-share sound and quality, and the firewall check
