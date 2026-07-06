# Floating Clock

A native macOS floating clock widget. Borderless, always on top, and designed to sit flush against your screen edges. Built with SwiftUI and AppKit.

**Author:** [Fong Thai](https://github.com/fongthai) · **Version 1.1** · **Released July 6, 2026**

## Features

### Clock

- **Floating panel**: draggable, position saved between launches, snaps to screen edges
- **Four clock faces**: Analog, Digital, Segment, and Day progress
- **Timezone-aware**: shows the city from your system timezone (e.g. `TOKYO`)
- **Holiday highlighting**: weekends and public holidays shown in red (timezone-based country detection)
- **Configurable**: 12/24-hour time, seconds on/off, three size presets

### Weather (optional)

- **Hourly timeline**: scrollable +/-12 hour forecast in 1-hour blocks
- **Current location**: uses GPS when permitted; falls back to timezone city center if denied
- **Location label**: neighborhood and region via reverse geocoding (e.g. `Oshitate, Inagi; Tokyo`)
- **Emoji weather icons**: sunny, rain, snow, thunderstorm, and more
- **Navigation**: left/right arrows to pan the timeline; reset button jumps back to the current hour

### System

- **Launch at login**: optional toggle in the settings menu
- **About window**: personal story, donation links, and TPBank QR code
- **No dock icon clutter**: runs as a lightweight utility panel

## Requirements

- macOS 14.0 (Sonoma) or later
- Xcode 15 or later

## Build & Run

1. Open `FloatingClock.xcodeproj` in Xcode
2. Select the **FloatingClock** scheme and your Mac as the run destination
3. Press **Cmd+R** to build and run

Command-line build:

```bash
xcodebuild -project FloatingClock.xcodeproj -scheme FloatingClock -configuration Debug build
```

### Distribution (DMG installer)

Build a drag-to-Applications installer DMG:

```bash
chmod +x scripts/build-dmg.sh
./scripts/build-dmg.sh
```

Output: `dist/FloatingClock-<version>.dmg`

Opening the DMG shows **Floating Clock.app**, an **Applications** folder, and installation guides (`instruction.txt`, `huong-dan-cai-dat.txt`). Users drag the app into Applications to install.

Requires Xcode and `xcodebuild` on your PATH. For distribution outside your Mac, code sign and notarize the app before building the DMG.

### Manual installation (for users)

Floating Clock is not notarized. On first launch, macOS may show a security warning. Users should:

1. Open the DMG and drag **Floating Clock.app** to **Applications**.
2. Open **Applications** in Finder.
3. **Right-click** Floating Clock.app and choose **Open**, then click **Open** again.

Alternatively: **System Settings → Privacy & Security → Open Anyway**.

The DMG also includes `instruction.txt` (English) and `huong-dan-cai-dat.txt` (Vietnamese) with full installation steps.

## Usage

### Moving the clock

- **Drag** anywhere on the clock face to reposition it
- The window stays within the visible screen area (above the Dock and below the menu bar)
- Position is restored on the next launch

### Settings menu

**Right-click** the clock to open settings:

| Option | Description |
|--------|-------------|
| **Clock Style** | Analog / Digital / Segment / Day |
| **24-Hour Time** | Switch between 12h and 24h display |
| **Show Seconds** | Show or hide seconds on all faces |
| **Show Weather** | Toggle the hourly weather band below the clock |
| **Sweep Second Hand** | Smooth vs ticking second hand (Analog only) |
| **Size** | Small (0.7x) / Medium (1.0x) / Large (1.4x) |
| **Launch at Login** | Start automatically when you log in |
| **About** | App info, release date, and donation options |
| **Quit Floating Clock** | Exit the app |

### Weather controls

When weather is enabled:

- **Left / Right arrows**: pan the timeline one hour at a time (past / future)
- **Reset** (top right): snap back so the current hour is the leftmost bar
- **Location permission**: macOS prompts on first use; if denied, weather uses your timezone city (e.g. `Asia/Tokyo` to Tokyo)

## Clock Faces

| Style | Description |
|-------|-------------|
| **Analog** | Round dial with cardinal markers, celeste city label, and optional sweeping red second hand |
| **Digital** | Bold rounded numerals with blinking colon and white halo shadows |
| **Segment** | Seven-segment display style digits |
| **Day** | Circular day-progress arc with percent-of-day label |

## Design

The **Chronos** design system uses a transparent background, celeste blue (`#74ACDF`) city labels, dark ink numerals, and red accents for seconds and holidays. Weather cells use a frosted glass look with a dark highlight on the current hour.

Reference mockups live in `stitch_macos_ui_with-weather/` and `stitch_macos_ui_enhancement/`.

## Version History

### 1.1 (July 6, 2026)

- Four clock faces: Analog, Digital, Segment, Day
- Optional hourly weather band with GPS location and Open-Meteo data
- Scrollable 1-hour timeline with emoji weather icons
- Holiday and weekend highlighting by timezone region
- Window sizing that fits content and snaps flush to screen edges
- About window with donation links and TPBank QR code
- Launch at login support

### 1.0 (initial)

- Borderless floating always-on-top clock panel
- Analog and digital clock styles
- Draggable window with saved position
- Size presets and 12/24-hour time

## Project Structure

```
FloatingClock/
├── FloatingClockApp.swift          # App entry point
├── AppDelegate.swift               # Launches floating panel
├── Window/
│   ├── FloatingPanelController.swift
│   └── WindowSizeManager.swift     # Panel sizing & edge clamping
├── Clock/
│   ├── ClockEngine.swift           # Time snapshots & angles
│   ├── ClockStyle.swift
│   ├── ChronosStyle.swift          # Shared labels & design tokens
│   ├── ClockContainerView.swift    # Face switcher & settings menu
│   ├── HolidayChecker.swift
│   ├── HolidayData.swift
│   ├── RegionResolver.swift
│   └── Views/
│       ├── AnalogClockView.swift
│       ├── SkeuDigitalClockView.swift
│       ├── SegmentDigitalClockView.swift
│       └── DayProgressClockView.swift
├── Weather/
│   ├── WeatherService.swift        # Open-Meteo API & geocoding
│   ├── WeatherStore.swift
│   ├── WeatherTimelineView.swift
│   └── LocationManager.swift       # Core Location permission & GPS
└── Settings/
    ├── LoginItemManager.swift
    └── AboutView.swift

distribution/
├── instruction.txt               # DMG install guide (English)
└── huong-dan-cai-dat.txt         # DMG install guide (Vietnamese)
```

## Data Sources

- **Weather**: [Open-Meteo](https://open-meteo.com/) (no API key required)
- **Geocoding**: Open-Meteo Geocoding API + Apple `CLGeocoder` reverse geocoding
- **Holidays**: bundled public holiday data per country/region

## Privacy

- Location is requested only when **Show Weather** is enabled
- Coordinates are sent to Open-Meteo for forecast data
- No analytics or third-party tracking

## Author

**Fong Thai** is the creator and maintainer.

| | |
|---|---|
| **GitHub** | [@fongthai](https://github.com/fongthai) |
| **Donate** | [Buy Me a Coffee](https://buymeacoffee.com/fongthai) |

If Floating Clock is useful to you, a small donation helps support ongoing development. Bug reports and feature ideas are welcome on GitHub.

### TPBank transfer (Vietnam)

You can also send a local bank transfer by scanning this TPBank QR code:

![TPBank donation QR code](FloatingClock/Assets.xcassets/QR-TP-bank-for-donation.imageset/QR-TP-bank-for-donation.png)

## License

MIT
