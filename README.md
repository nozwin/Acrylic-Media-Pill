# Acrylic Media Pill – a Windhawk mod

A glass-style light weight media pill for the Windows 11 taskbar. It shows whatever is playing
(Edge, Chrome, Spotify, VLC, Media Player, ...) and works with dock-style taskbars.
It runs entirely inside `explorer.exe`.

> Status: experimental. Tested by the author on Windows 11 only.

## Features

* **Real-Time Glass Rendering:** Available in **Dark**, **Light**, and **Liquid Glass** themes. The backdrop is rendered directly by the mod using a blurred snapshot of the area behind the pill, paired with a subtle tint and rim for crisp, anti-aliased rounded edges *(refreshes automatically once a minute)*.
* **Clean Three-Part Layout:**
  * **Left:** Center-cropped album cover art, downscaled with high-quality bicubic filtering.
  * **Middle:** Lightweight 5-bar mini audio visualizer driven directly by the Windows system output peak meter.
  * **Right:** Track title and artist name.
* **Interactive Player Card:** Click the pill to expand a floating media card with a live progress bar, interactive seeking, and **Previous / Play-Pause / Next** controls. Click anywhere outside to dismiss.
* **Dock-Style Taskbar Compatible:** Built as an independent top-level window owned by `explorer.exe` rather than an injected XAML element—preventing layout conflicts with mods like **Windows 11 Taskbar Styler**.
* **Adaptive Sizing:** Automatically scales to match your taskbar height (customizable via the **Pill height** setting). *Supports horizontal taskbars.*

## Install

1. Install [Windhawk](https://windhawk.net/).
2. In Windhawk click **Create a new mod**, replace the template with the contents of
   `acrylic-media-pill.wh.cpp`, then click **Compile Mod** and enable it.
3. Adjust everything in the mod's **Settings** tab.

## Notes

- Horizontal taskbars only.
- The glass is a blurred snapshot of what is behind the pill, taken when it appears
  (optionally refreshed every N seconds in settings; the pill blinks briefly when refreshed).
- "Open the playing tab" in browsers is best effort (uses UI Automation).

## Author
* **GitHub:** [@nozwin](https://github.com/nozwin)

## License

MIT – see `LICENSE`.
