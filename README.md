# Utter: downloads and updates

Utter turns what you say into text in whatever app you are using, entirely on
your Mac. This repository only hosts the installers and the update feed; the
source is private to Mindbee Labs. Utter is a modified version of
[Handy](https://github.com/cjpais/Handy) by CJ Pais (MIT licence).

## Install

1. Download `Utter_<version>_aarch64.dmg` from the
   [latest release](https://github.com/mindbee-labs/utter-releases/releases/latest)
   (Apple Silicon Macs).
2. Open the DMG and drag **Utter** to **Applications**.
3. The builds are not notarized by Apple yet: the first time, right-click
   **Utter.app → Open**, then confirm.
4. Allow **Microphone** and **Accessibility** (Accessibility lets Utter paste
   the text for you).

Installed copies check this page and offer updates themselves; every update
is signed with Utter's own key and refused if the signature does not match.

## Use

- **Tap Option+Space**, speak, and stop talking: Utter stops after the silence
  you set (Settings → General → Auto-stop After Silence) and pastes the text.
- **Hold Option+Space** while you speak and let go to paste.
- **Escape** cancels a recording without pasting.

## Shortcuts stopped working on macOS (Secure Input)

When another app turns on macOS **Secure Keyboard Entry**, apps like Utter
stop seeing the keyboard shortcut. Password fields do this while focused, and
some terminals (for example Ghostty, Terminal or iTerm2) turn it on by
themselves when they think a password is being typed. Utter shows a warning
and falls back to a system shortcut where it can.

To fix it, turn Secure Keyboard Entry off in the app that holds it:

- **Ghostty:** add `macos-auto-secure-input = false` to
  `~/.config/ghostty/config` and restart Ghostty (or turn it off from the
  Ghostty menu).
- **Terminal / iTerm2:** untick *Secure Keyboard Entry* in the app menu.

## Linux

Utter is built for macOS only at the moment.

## Support

Open an issue in this repository.
