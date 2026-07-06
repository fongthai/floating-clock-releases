# Floating Clock / Đồng hồ nổi

A native macOS floating clock widget. Borderless, always on top, and designed to sit flush against your screen edges. Built with SwiftUI and AppKit.
Widget đồng hồ nổi gốc cho macOS. Không viền, luôn trên cùng, sát mép màn hình. Xây dựng bằng SwiftUI và AppKit.

**Author:** [Fong Thai](https://github.com/fongthai) · **Version 1.1** · **Released July 6, 2026**
**Tác giả:** [Fong Thai](https://github.com/fongthai) · **Phiên bản 1.1** · **Phát hành 6 tháng 7, 2026**

## Features / Tính năng

### Clock / Đồng hồ

- **Floating panel**: draggable, position saved between launches, snaps to screen edges
- **Bảng nổi**: kéo được, lưu vị trí giữa các lần mở, bám sát mép màn hình
- **Four clock faces**: Analog, Digital, Segment, and Day progress
- **Bốn mặt đồng hồ**: Analog, Digital, Segment và Day progress
- **Timezone-aware**: shows the city from your system timezone (e.g. `TOKYO`)
- **Theo múi giờ**: hiển thị thành phố theo múi giờ hệ thống (ví dụ `TOKYO`)
- **Holiday highlighting**: weekends and public holidays shown in red (timezone-based country detection)
- **Đánh dấu ngày lễ**: cuối tuần và ngày lễ hiển thị màu đỏ (nhận diện quốc gia theo múi giờ)
- **Configurable**: 12/24-hour time, seconds on/off, three size presets
- **Tùy chỉnh**: giờ 12/24, bật/tắt giây, ba cỡ hiển thị

### Weather (optional) / Thời tiết (tùy chọn)

- **Hourly timeline**: scrollable +/-12 hour forecast in 1-hour blocks
- **Dòng thời gian theo giờ**: cuộn dự báo +/-12 giờ, mỗi ô một giờ
- **Current location**: uses GPS when permitted; falls back to timezone city center if denied
- **Vị trí hiện tại**: dùng GPS khi được phép; nếu từ chối thì dùng thành phố theo múi giờ
- **Location label**: neighborhood and region via reverse geocoding (e.g. `Oshitate, Inagi; Tokyo`)
- **Nhãn địa điểm**: khu phố và vùng qua reverse geocoding (ví dụ `Oshitate, Inagi; Tokyo`)
- **Emoji weather icons**: sunny, rain, snow, thunderstorm, and more
- **Biểu tượng thời tiết emoji**: nắng, mưa, tuyết, giông và hơn nữa
- **Navigation**: left/right arrows to pan the timeline; reset button jumps back to the current hour
- **Điều hướng**: mũi tên trái/phải để cuộn dòng thời gian; nút reset về giờ hiện tại

### System / Hệ thống

- **Launch at login**: optional toggle in the settings menu
- **Khởi động khi đăng nhập**: bật/tắt trong menu cài đặt
- **About window**: personal story, donation links, and TPBank QR code
- **Cửa sổ Giới thiệu**: câu chuyện cá nhân, liên kết ủng hộ và mã QR TPBank
- **No dock icon clutter**: runs as a lightweight utility panel
- **Không chiếm Dock**: chạy như tiện ích nhẹ trên màn hình

## Requirements / Yêu cầu

- macOS 14.0 (Sonoma) or later
- macOS 14.0 (Sonoma) trở lên
- Xcode 15 or later
- Xcode 15 trở lên

## Build & Run / Biên dịch và chạy

1. Open `FloatingClock.xcodeproj` in Xcode
1. Mở `FloatingClock.xcodeproj` trong Xcode
2. Select the **FloatingClock** scheme and your Mac as the run destination
2. Chọn scheme **FloatingClock** và máy Mac của bạn làm đích chạy
3. Press **Cmd+R** to build and run
3. Nhấn **Cmd+R** để biên dịch và chạy

Command-line build:
Biên dịch dòng lệnh:

```bash
xcodebuild -project FloatingClock.xcodeproj -scheme FloatingClock -configuration Debug build
```

### Distribution (DMG installer) / Phân phối (cài đặt DMG)

Build a drag-to-Applications installer DMG:
Tạo file cài đặt DMG kéo-thả vào Applications:

```bash
chmod +x scripts/build-dmg.sh
./scripts/build-dmg.sh
```

Output: `dist/FloatingClock-<version>.dmg`
Kết quả: `dist/FloatingClock-<version>.dmg`

Opening the DMG shows **Floating Clock.app**, an **Applications** folder, and installation guides (`instruction.txt`, `huong-dan-cai-dat.txt`). Users drag the app into Applications to install.
Mở DMG sẽ thấy **Floating Clock.app**, thư mục **Applications** và hướng dẫn cài đặt (`instruction.txt`, `huong-dan-cai-dat.txt`). Kéo app vào Applications để cài.

Requires Xcode and `xcodebuild` on your PATH. For distribution outside your Mac, code sign and notarize the app before building the DMG.
Cần Xcode và `xcodebuild` trên PATH. Để phân phối ra ngoài máy bạn, hãy ký code và notarize trước khi tạo DMG.

Publish the DMG to the public releases repo:
Đăng DMG lên repo phát hành công khai:

```bash
chmod +x scripts/publish-release.sh
./scripts/publish-release.sh --build
```

### Manual installation (for users) / Cài đặt thủ công (cho người dùng)

Floating Clock is not notarized. On first launch, macOS may show a security warning. Users should:
Floating Clock chưa được notarize. Lần mở đầu, macOS có thể cảnh báo bảo mật. Người dùng nên:

1. Open the DMG and drag **Floating Clock.app** to **Applications**.
1. Mở DMG và kéo **Floating Clock.app** vào **Applications**.
2. Open **Applications** in Finder.
2. Mở **Applications** trong Finder.
3. **Right-click** Floating Clock.app and choose **Open**, then click **Open** again.
3. **Nhấp chuột phải** Floating Clock.app, chọn **Open** (Mở), rồi nhấn **Open** (Mở) lần nữa.

Alternatively: **System Settings → Privacy & Security → Open Anyway**.
Hoặc: **System Settings → Privacy & Security → Open Anyway** (Vẫn mở).

The DMG also includes `instruction.txt` (English) and `huong-dan-cai-dat.txt` (Vietnamese) with full installation steps.
DMG còn có `instruction.txt` (tiếng Anh) và `huong-dan-cai-dat.txt` (tiếng Việt) với hướng dẫn đầy đủ.

## Usage / Cách dùng

### Moving the clock / Di chuyển đồng hồ

- **Drag** anywhere on the clock face to reposition it
- **Kéo** bất kỳ đâu trên mặt đồng hồ để đổi vị trí
- The window stays within the visible screen area (above the Dock and below the menu bar)
- Cửa sổ luôn nằm trong vùng màn hình (trên Dock và dưới thanh menu)
- Position is restored on the next launch
- Vị trí được khôi phục ở lần mở sau

### Settings menu / Menu cài đặt

**Right-click** the clock to open settings:
**Nhấp chuột phải** đồng hồ để mở cài đặt:

| Option / Tùy chọn | Description / Mô tả |
|--------|-------------|
| **Clock Style**<br>**Kiểu đồng hồ** | Analog / Digital / Segment / Day<br>Analog / Digital / Segment / Day |
| **24-Hour Time**<br>**Giờ 24h** | Switch between 12h and 24h display<br>Chuyển giữa hiển thị 12h và 24h |
| **Show Seconds**<br>**Hiện giây** | Show or hide seconds on all faces<br>Bật/tắt giây trên mọi mặt đồng hồ |
| **Show Weather**<br>**Hiện thời tiết** | Toggle the hourly weather band below the clock<br>Bật/tắt dải thời tiết theo giờ dưới đồng hồ |
| **Sweep Second Hand**<br>**Kim giây quét** | Smooth vs ticking second hand (Analog only)<br>Kim giây mượt hoặc giật (chỉ Analog) |
| **Size**<br>**Cỡ** | Small (0.7x) / Medium (1.0x) / Large (1.4x)<br>Nhỏ (0.7x) / Vừa (1.0x) / Lớn (1.4x) |
| **Launch at Login**<br>**Khởi động khi đăng nhập** | Start automatically when you log in<br>Tự chạy khi bạn đăng nhập |
| **About**<br>**Giới thiệu** | App info, release date, and donation options<br>Thông tin app, ngày phát hành và ủng hộ |
| **Quit Floating Clock**<br>**Thoát Floating Clock** | Exit the app<br>Đóng ứng dụng |

### Weather controls / Điều khiển thời tiết

When weather is enabled:
Khi bật thời tiết:

- **Left / Right arrows**: pan the timeline one hour at a time (past / future)
- **Mũi tên trái / phải**: cuộn dòng thời gian từng giờ (quá khứ / tương lai)
- **Reset** (top right): snap back so the current hour is the leftmost bar
- **Reset** (góc trên phải): đưa giờ hiện tại về cột ngoài cùng bên trái
- **Location permission**: macOS prompts on first use; if denied, weather uses your timezone city (e.g. `Asia/Tokyo` to Tokyo)
- **Quyền vị trí**: macOS hỏi lần đầu; nếu từ chối, thời tiết dùng thành phố theo múi giờ (ví dụ `Asia/Tokyo` → Tokyo)

## Clock Faces / Các mặt đồng hồ

| Style / Kiểu | Description / Mô tả |
|-------|-------------|
| **Analog** | Round dial with cardinal markers, celeste city label, and optional sweeping red second hand<br>Mặt tròn với vạch hướng, nhãn thành phố màu celeste và kim giây đỏ quét (tùy chọn) |
| **Digital** | Bold rounded numerals with blinking colon and white halo shadows<br>Số đậm bo tròn, dấu hai chấm nhấp nháy và viền sáng trắng |
| **Segment** | Seven-segment display style digits<br>Chữ số kiểu bảy đoạn |
| **Day** | Circular day-progress arc with percent-of-day label<br>Cung tiến độ ngày tròn kèm phần trăm trong ngày |

## Design / Thiết kế

The **Chronos** design system uses a transparent background, celeste blue (`#74ACDF`) city labels, dark ink numerals, and red accents for seconds and holidays. Weather cells use a frosted glass look with a dark highlight on the current hour.
Hệ thống thiết kế **Chronos** dùng nền trong suốt, nhãn thành phố xanh celeste (`#74ACDF`), số mực đậm và điểm nhấn đỏ cho giây và ngày lễ. Ô thời tiết kiểu kính mờ, giờ hiện tại được tô đậm.

Reference mockups live in `stitch_macos_ui_with-weather/` and `stitch_macos_ui_enhancement/`.
Mockup tham khảo nằm trong `stitch_macos_ui_with-weather/` và `stitch_macos_ui_enhancement/`.

## Version History / Lịch sử phiên bản

### 1.1 (July 6, 2026) / 1.1 (6 tháng 7, 2026)

- Four clock faces: Analog, Digital, Segment, Day
- Bốn mặt đồng hồ: Analog, Digital, Segment, Day
- Optional hourly weather band with GPS location and Open-Meteo data
- Dải thời tiết theo giờ tùy chọn với GPS và dữ liệu Open-Meteo
- Scrollable 1-hour timeline with emoji weather icons
- Dòng thời gian cuộn theo giờ với biểu tượng thời tiết emoji
- Holiday and weekend highlighting by timezone region
- Đánh dấu ngày lễ và cuối tuần theo vùng múi giờ
- Window sizing that fits content and snaps flush to screen edges
- Cỡ cửa sổ vừa nội dung, sát mép màn hình
- About window with donation links and TPBank QR code
- Cửa sổ Giới thiệu với liên kết ủng hộ và mã QR TPBank
- Launch at login support
- Hỗ trợ khởi động khi đăng nhập

### 1.0 (initial) / 1.0 (ban đầu)

- Borderless floating always-on-top clock panel
- Bảng đồng hồ nổi không viền, luôn trên cùng
- Analog and digital clock styles
- Kiểu đồng hồ Analog và Digital
- Draggable window with saved position
- Cửa sổ kéo được, lưu vị trí
- Size presets and 12/24-hour time
- Cỡ sẵn và giờ 12/24

## Project Structure / Cấu trúc dự án

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
├── huong-dan-cai-dat.txt         # DMG install guide (Vietnamese)
└── release-notes.md              # Bilingual GitHub Release notes template
```

## Data Sources / Nguồn dữ liệu

- **Weather**: [Open-Meteo](https://open-meteo.com/) (no API key required)
- **Thời tiết**: [Open-Meteo](https://open-meteo.com/) (không cần API key)
- **Geocoding**: Open-Meteo Geocoding API + Apple `CLGeocoder` reverse geocoding
- **Địa lý**: Open-Meteo Geocoding API + reverse geocoding `CLGeocoder` của Apple
- **Holidays**: bundled public holiday data per country/region
- **Ngày lễ**: dữ liệu ngày lễ công cộng theo quốc gia/vùng có sẵn trong app

## Privacy / Quyền riêng tư

- Location is requested only when **Show Weather** is enabled
- Vị trí chỉ được hỏi khi bật **Show Weather** (Hiện thời tiết)
- Coordinates are sent to Open-Meteo for forecast data
- Tọa độ được gửi tới Open-Meteo để lấy dự báo
- No analytics or third-party tracking
- Không có phân tích hay theo dõi bên thứ ba

## Author / Tác giả

**Fong Thai** is the creator and maintainer.
**Fong Thai** là người tạo và duy trì dự án.

| | |
|---|---|
| **GitHub**<br>**GitHub** | [@fongthai](https://github.com/fongthai) |
| **Donate**<br>**Ủng hộ** | [Buy Me a Coffee](https://buymeacoffee.com/fongthai) |

If Floating Clock is useful to you, a small donation helps support ongoing development. Bug reports and feature ideas are welcome on GitHub.
Nếu Floating Clock hữu ích với bạn, một khoản ủng hộ nhỏ giúp duy trì phát triển. Báo lỗi và ý tưởng tính năng được chào đón trên GitHub.

### TPBank transfer (Vietnam) / Chuyển khoản TPBank (Việt Nam)

You can also send a local bank transfer by scanning this TPBank QR code:
Bạn cũng có thể chuyển khoản nội địa bằng cách quét mã QR TPBank này:

![TPBank donation QR code](FloatingClock/Assets.xcassets/QR-TP-bank-for-donation.imageset/QR-TP-bank-for-donation.png)

## License / Giấy phép

MIT
MIT
