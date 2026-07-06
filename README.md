# 🇺🇸 Floating Clock / 🇻🇳 Đồng hồ nổi / 🇯🇵 フローティングクロック

🇺🇸 A native macOS floating clock widget. Borderless, always on top, and designed to sit flush against your screen edges. Built with SwiftUI and AppKit.
🇻🇳 Widget đồng hồ nổi gốc cho macOS. Không viền, luôn trên cùng, sát mép màn hình. Xây dựng bằng SwiftUI và AppKit.
🇯🇵 macOS 向けのネイティブ浮動時計ウィジェット。枠なし、常に最前面、画面端にぴったり配置。SwiftUI と AppKit で構築。

🇺🇸 **Author:** [Fong Thai](https://github.com/fongthai) · **Version 1.1** · **Released July 6, 2026**
🇻🇳 **Tác giả:** [Fong Thai](https://github.com/fongthai) · **Phiên bản 1.1** · **Phát hành 6 tháng 7, 2026**
🇯🇵 **作者:** [Fong Thai](https://github.com/fongthai) · **バージョン 1.1** · **リリース 2026年7月6日**

## 🇺🇸 Features / 🇻🇳 Tính năng / 🇯🇵 機能

### 🇺🇸 Clock / 🇻🇳 Đồng hồ / 🇯🇵 時計

- 🇺🇸 **Floating panel**: draggable, position saved between launches, snaps to screen edges
- 🇻🇳 **Bảng nổi**: kéo được, lưu vị trí giữa các lần mở, bám sát mép màn hình
- 🇯🇵 **浮動パネル**: ドラッグ可能、起動間で位置を保存、画面端にスナップ
- 🇺🇸 **Four clock faces**: Analog, Digital, Segment, and Day progress
- 🇻🇳 **Bốn mặt đồng hồ**: Analog, Digital, Segment và Day progress
- 🇯🇵 **4つの文字盤**: アナログ、デジタル、セグメント、デイ進捗
- 🇺🇸 **Timezone-aware**: shows the city from your system timezone (e.g. `TOKYO`)
- 🇻🇳 **Theo múi giờ**: hiển thị thành phố theo múi giờ hệ thống (ví dụ `TOKYO`)
- 🇯🇵 **タイムゾーン対応**: システムのタイムゾーンから都市を表示（例: `TOKYO`）
- 🇺🇸 **Holiday highlighting**: weekends and public holidays shown in red (timezone-based country detection)
- 🇻🇳 **Đánh dấu ngày lễ**: cuối tuần và ngày lễ hiển thị màu đỏ (nhận diện quốc gia theo múi giờ)
- 🇯🇵 **祝日ハイライト**: 週末と祝日を赤で表示（タイムゾーンから国を判定）
- 🇺🇸 **Configurable**: 12/24-hour time, seconds on/off, three size presets
- 🇻🇳 **Tùy chỉnh**: giờ 12/24, bật/tắt giây, ba cỡ hiển thị
- 🇯🇵 **カスタマイズ**: 12/24時間表示、秒のオン/オフ、3段階のサイズ

### 🇺🇸 Weather (optional) / 🇻🇳 Thời tiết (tùy chọn) / 🇯🇵 天気（任意）

- 🇺🇸 **Hourly timeline**: scrollable +/-12 hour forecast in 1-hour blocks
- 🇻🇳 **Dòng thời gian theo giờ**: cuộn dự báo +/-12 giờ, mỗi ô một giờ
- 🇯🇵 **時間別タイムライン**: +/-12時間の予報を1時間単位でスクロール
- 🇺🇸 **Current location**: uses GPS when permitted; falls back to timezone city center if denied
- 🇻🇳 **Vị trí hiện tại**: dùng GPS khi được phép; nếu từ chối thì dùng thành phố theo múi giờ
- 🇯🇵 **現在地**: 許可時は GPS を使用、拒否時はタイムゾーンの都市中心にフォールバック
- 🇺🇸 **Location label**: neighborhood and region via reverse geocoding (e.g. `Oshitate, Inagi; Tokyo`)
- 🇻🇳 **Nhãn địa điểm**: khu phố và vùng qua reverse geocoding (ví dụ `Oshitate, Inagi; Tokyo`)
- 🇯🇵 **位置ラベル**: 逆ジオコーディングで地区と地域を表示（例: `Oshitate, Inagi; Tokyo`）
- 🇺🇸 **Emoji weather icons**: sunny, rain, snow, thunderstorm, and more
- 🇻🇳 **Biểu tượng thời tiết emoji**: nắng, mưa, tuyết, giông và hơn nữa
- 🇯🇵 **天気絵文字アイコン**: 晴れ、雨、雪、雷雨など
- 🇺🇸 **Navigation**: left/right arrows to pan the timeline; reset button jumps back to the current hour
- 🇻🇳 **Điều hướng**: mũi tên trái/phải để cuộn dòng thời gian; nút reset về giờ hiện tại
- 🇯🇵 **ナビゲーション**: 左右矢印でタイムラインを移動、リセットで現在時刻に戻る

### 🇺🇸 System / 🇻🇳 Hệ thống / 🇯🇵 システム

- 🇺🇸 **Launch at login**: optional toggle in the settings menu
- 🇻🇳 **Khởi động khi đăng nhập**: bật/tắt trong menu cài đặt
- 🇯🇵 **ログイン時に起動**: 設定メニューでオン/オフ
- 🇺🇸 **About window**: personal story, donation links, and TPBank QR code
- 🇻🇳 **Cửa sổ Giới thiệu**: câu chuyện cá nhân, liên kết ủng hộ và mã QR TPBank
- 🇯🇵 **このアプリについて**: 作者のメッセージ、寄付リンク、TPBank QR コード
- 🇺🇸 **No dock icon clutter**: runs as a lightweight utility panel
- 🇻🇳 **Không chiếm Dock**: chạy như tiện ích nhẹ trên màn hình
- 🇯🇵 **Dock を占有しない**: 軽量なユーティリティパネルとして動作

## 🇺🇸 Requirements / 🇻🇳 Yêu cầu / 🇯🇵 動作環境

- 🇺🇸 macOS 14.0 (Sonoma) or later
- 🇻🇳 macOS 14.0 (Sonoma) trở lên
- 🇯🇵 macOS 14.0（Sonoma）以降
- 🇺🇸 Xcode 15 or later
- 🇻🇳 Xcode 15 trở lên
- 🇯🇵 Xcode 15 以降

## 🇺🇸 Build & Run / 🇻🇳 Biên dịch và chạy / 🇯🇵 ビルドと実行

1. 🇺🇸 Open `FloatingClock.xcodeproj` in Xcode
1. 🇻🇳 Mở `FloatingClock.xcodeproj` trong Xcode
1. 🇯🇵 Xcode で `FloatingClock.xcodeproj` を開く
2. 🇺🇸 Select the **FloatingClock** scheme and your Mac as the run destination
2. 🇻🇳 Chọn scheme **FloatingClock** và máy Mac của bạn làm đích chạy
2. 🇯🇵 **FloatingClock** スキームと Mac を実行先に選択
3. 🇺🇸 Press **Cmd+R** to build and run
3. 🇻🇳 Nhấn **Cmd+R** để biên dịch và chạy
3. 🇯🇵 **Cmd+R** でビルドして実行

🇺🇸 Command-line build:
🇻🇳 Biên dịch dòng lệnh:
🇯🇵 コマンドラインでビルド:

```bash
xcodebuild -project FloatingClock.xcodeproj -scheme FloatingClock -configuration Debug build
```

### 🇺🇸 Distribution (DMG installer) / 🇻🇳 Phân phối (cài đặt DMG) / 🇯🇵 配布（DMG インストーラー）

🇺🇸 Build a drag-to-Applications installer DMG:
🇻🇳 Tạo file cài đặt DMG kéo-thả vào Applications:
🇯🇵 Applications にドラッグする DMG インストーラーを作成:

```bash
chmod +x scripts/build-dmg.sh
./scripts/build-dmg.sh
```

🇺🇸 Output: `dist/FloatingClock-<version>.dmg`
🇻🇳 Kết quả: `dist/FloatingClock-<version>.dmg`
🇯🇵 出力: `dist/FloatingClock-<version>.dmg`

🇺🇸 Opening the DMG shows **Floating Clock.app**, an **Applications** folder, and installation guides (`instruction.txt`, `huong-dan-cai-dat.txt`). Users drag the app into Applications to install.
🇻🇳 Mở DMG sẽ thấy **Floating Clock.app**, thư mục **Applications** và hướng dẫn cài đặt (`instruction.txt`, `huong-dan-cai-dat.txt`). Kéo app vào Applications để cài.
🇯🇵 DMG には **Floating Clock.app**、**Applications** フォルダ、インストールガイド（`instruction.txt`、`huong-dan-cai-dat.txt`）が含まれます。アプリを Applications にドラッグしてインストールします。

🇺🇸 Requires Xcode and `xcodebuild` on your PATH. For distribution outside your Mac, code sign and notarize the app before building the DMG.
🇻🇳 Cần Xcode và `xcodebuild` trên PATH. Để phân phối ra ngoài máy bạn, hãy ký code và notarize trước khi tạo DMG.
🇯🇵 Xcode と `xcodebuild` が PATH に必要です。他の Mac に配布する場合は、DMG 作成前にコード署名と公証を行ってください。

🇺🇸 Publish the DMG to the public releases repo:
🇻🇳 Đăng DMG lên repo phát hành công khai:
🇯🇵 公開リリースリポジトリに DMG を公開:

```bash
chmod +x scripts/publish-release.sh
./scripts/publish-release.sh --build
```

### 🇺🇸 Manual installation (for users) / 🇻🇳 Cài đặt thủ công (cho người dùng) / 🇯🇵 手動インストール（ユーザー向け）

🇺🇸 Floating Clock is not notarized. On first launch, macOS may show a security warning. Users should:
🇻🇳 Floating Clock chưa được notarize. Lần mở đầu, macOS có thể cảnh báo bảo mật. Người dùng nên:
🇯🇵 Floating Clock は公証されていません。初回起動時に macOS のセキュリティ警告が出る場合があります。次の手順で開いてください:

1. 🇺🇸 Open the DMG and drag **Floating Clock.app** to **Applications**.
1. 🇻🇳 Mở DMG và kéo **Floating Clock.app** vào **Applications**.
1. 🇯🇵 DMG を開き、**Floating Clock.app** を **Applications** にドラッグします。
2. 🇺🇸 Open **Applications** in Finder.
2. 🇻🇳 Mở **Applications** trong Finder.
2. 🇯🇵 Finder で **Applications** を開きます。
3. 🇺🇸 **Right-click** Floating Clock.app and choose **Open**, then click **Open** again.
3. 🇻🇳 **Nhấp chuột phải** Floating Clock.app, chọn **Open** (Mở), rồi nhấn **Open** (Mở) lần nữa.
3. 🇯🇵 **Floating Clock.app** を右クリックして **開く** を選び、再度 **開く** をクリックします。

🇺🇸 Alternatively: **System Settings → Privacy & Security → Open Anyway**.
🇻🇳 Hoặc: **System Settings → Privacy & Security → Open Anyway** (Vẫn mở).
🇯🇵 または: **システム設定 → プライバシーとセキュリティ → このまま開く**。

🇺🇸 The DMG also includes `instruction.txt` (English) and `huong-dan-cai-dat.txt` (Vietnamese).
🇻🇳 DMG còn có `instruction.txt` (tiếng Anh) và `huong-dan-cai-dat.txt` (tiếng Việt).
🇯🇵 DMG には `instruction.txt`（英語）と `huong-dan-cai-dat.txt`（ベトナム語）も含まれます。

## 🇺🇸 Usage / 🇻🇳 Cách dùng / 🇯🇵 使い方

### 🇺🇸 Moving the clock / 🇻🇳 Di chuyển đồng hồ / 🇯🇵 時計の移動

- 🇺🇸 **Drag** anywhere on the clock face to reposition it
- 🇻🇳 **Kéo** bất kỳ đâu trên mặt đồng hồ để đổi vị trí
- 🇯🇵 **ドラッグ** で文字盤上の任意の場所を掴んで移動
- 🇺🇸 The window stays within the visible screen area (above the Dock and below the menu bar)
- 🇻🇳 Cửa sổ luôn nằm trong vùng màn hình (trên Dock và dưới thanh menu)
- 🇯🇵 ウィンドウは Dock の上、メニューバーの下の表示領域内に留まります
- 🇺🇸 Position is restored on the next launch
- 🇻🇳 Vị trí được khôi phục ở lần mở sau
- 🇯🇵 次回起動時に位置が復元されます

### 🇺🇸 Settings menu / 🇻🇳 Menu cài đặt / 🇯🇵 設定メニュー

🇺🇸 **Right-click** the clock to open settings:
🇻🇳 **Nhấp chuột phải** đồng hồ để mở cài đặt:
🇯🇵 時計を**右クリック**して設定を開きます:

| 🇺🇸 Option / 🇻🇳 Tùy chọn / 🇯🇵 オプション | 🇺🇸 Description / 🇻🇳 Mô tả / 🇯🇵 説明 |
|--------|-------------|
| 🇺🇸 **Clock Style**<br>🇻🇳 **Kiểu đồng hồ**<br>🇯🇵 **時計スタイル** | 🇺🇸 Analog / Digital / Segment / Day<br>🇻🇳 Analog / Digital / Segment / Day<br>🇯🇵 アナログ / デジタル / セグメント / デイ |
| 🇺🇸 **24-Hour Time**<br>🇻🇳 **Giờ 24h**<br>🇯🇵 **24時間表示** | 🇺🇸 Switch between 12h and 24h display<br>🇻🇳 Chuyển giữa hiển thị 12h và 24h<br>🇯🇵 12時間と24時間表示を切り替え |
| 🇺🇸 **Show Seconds**<br>🇻🇳 **Hiện giây**<br>🇯🇵 **秒を表示** | 🇺🇸 Show or hide seconds on all faces<br>🇻🇳 Bật/tắt giây trên mọi mặt đồng hồ<br>🇯🇵 すべての文字盤で秒の表示/非表示 |
| 🇺🇸 **Show Weather**<br>🇻🇳 **Hiện thời tiết**<br>🇯🇵 **天気を表示** | 🇺🇸 Toggle the hourly weather band below the clock<br>🇻🇳 Bật/tắt dải thời tiết theo giờ dưới đồng hồ<br>🇯🇵 時計下の時間別天気バンドのオン/オフ |
| 🇺🇸 **Sweep Second Hand**<br>🇻🇳 **Kim giây quét**<br>🇯🇵 **秒針スイープ** | 🇺🇸 Smooth vs ticking second hand (Analog only)<br>🇻🇳 Kim giây mượt hoặc giật (chỉ Analog)<br>🇯🇵 秒針のスムーズ/刻み切り替え（アナログのみ） |
| 🇺🇸 **Size**<br>🇻🇳 **Cỡ**<br>🇯🇵 **サイズ** | 🇺🇸 Small (0.7x) / Medium (1.0x) / Large (1.4x)<br>🇻🇳 Nhỏ (0.7x) / Vừa (1.0x) / Lớn (1.4x)<br>🇯🇵 小 (0.7x) / 中 (1.0x) / 大 (1.4x) |
| 🇺🇸 **Launch at Login**<br>🇻🇳 **Khởi động khi đăng nhập**<br>🇯🇵 **ログイン時に起動** | 🇺🇸 Start automatically when you log in<br>🇻🇳 Tự chạy khi bạn đăng nhập<br>🇯🇵 ログイン時に自動起動 |
| 🇺🇸 **About**<br>🇻🇳 **Giới thiệu**<br>🇯🇵 **このアプリについて** | 🇺🇸 App info, release date, and donation options<br>🇻🇳 Thông tin app, ngày phát hành và ủng hộ<br>🇯🇵 アプリ情報、リリース日、寄付オプション |
| 🇺🇸 **Quit Floating Clock**<br>🇻🇳 **Thoát Floating Clock**<br>🇯🇵 **Floating Clock を終了** | 🇺🇸 Exit the app<br>🇻🇳 Đóng ứng dụng<br>🇯🇵 アプリを終了 |

### 🇺🇸 Weather controls / 🇻🇳 Điều khiển thời tiết / 🇯🇵 天気の操作

🇺🇸 When weather is enabled:
🇻🇳 Khi bật thời tiết:
🇯🇵 天気を有効にした場合:

- 🇺🇸 **Left / Right arrows**: pan the timeline one hour at a time (past / future)
- 🇻🇳 **Mũi tên trái / phải**: cuộn dòng thời gian từng giờ (quá khứ / tương lai)
- 🇯🇵 **左右矢印**: タイムラインを1時間ずつ移動（過去 / 未来）
- 🇺🇸 **Reset** (top right): snap back so the current hour is the leftmost bar
- 🇻🇳 **Reset** (góc trên phải): đưa giờ hiện tại về cột ngoài cùng bên trái
- 🇯🇵 **リセット**（右上）: 現在時刻を左端のバーに戻す
- 🇺🇸 **Location permission**: macOS prompts on first use; if denied, weather uses your timezone city (e.g. `Asia/Tokyo` to Tokyo)
- 🇻🇳 **Quyền vị trí**: macOS hỏi lần đầu; nếu từ chối, thời tiết dùng thành phố theo múi giờ (ví dụ `Asia/Tokyo` → Tokyo)
- 🇯🇵 **位置情報の許可**: 初回使用時に macOS が確認、拒否時はタイムゾーンの都市を使用（例: `Asia/Tokyo` → 東京）

## 🇺🇸 Clock Faces / 🇻🇳 Các mặt đồng hồ / 🇯🇵 文字盤

| 🇺🇸 Style / 🇻🇳 Kiểu / 🇯🇵 スタイル | 🇺🇸 Description / 🇻🇳 Mô tả / 🇯🇵 説明 |
|-------|-------------|
| **Analog** | 🇺🇸 Round dial with cardinal markers, celeste city label, and optional sweeping red second hand<br>🇻🇳 Mặt tròn với vạch hướng, nhãn thành phố màu celeste và kim giây đỏ quét (tùy chọn)<br>🇯🇵 方位マーカー付きの丸文字盤、セレスト色の都市ラベル、赤いスイープ秒針（任意） |
| **Digital** | 🇺🇸 Bold rounded numerals with blinking colon and white halo shadows<br>🇻🇳 Số đậm bo tròn, dấu hai chấm nhấp nháy và viền sáng trắng<br>🇯🇵 太字の丸数字、点滅コロン、白いハロー影 |
| **Segment** | 🇺🇸 Seven-segment display style digits<br>🇻🇳 Chữ số kiểu bảy đoạn<br>🇯🇵 7セグメント表示スタイルの数字 |
| **Day** | 🇺🇸 Circular day-progress arc with percent-of-day label<br>🇻🇳 Cung tiến độ ngày tròn kèm phần trăm trong ngày<br>🇯🇵 1日の進捗を示す円弧とパーセント表示 |

## 🇺🇸 Design / 🇻🇳 Thiết kế / 🇯🇵 デザイン

🇺🇸 The **Chronos** design system uses a transparent background, celeste blue (`#74ACDF`) city labels, dark ink numerals, and red accents for seconds and holidays. Weather cells use a frosted glass look with a dark highlight on the current hour.
🇻🇳 Hệ thống thiết kế **Chronos** dùng nền trong suốt, nhãn thành phố xanh celeste (`#74ACDF`), số mực đậm và điểm nhấn đỏ cho giây và ngày lễ. Ô thời tiết kiểu kính mờ, giờ hiện tại được tô đậm.
🇯🇵 **Chronos** デザインシステムは透明背景、セレストブルー（`#74ACDF`）の都市ラベル、濃い数字、秒と祝日の赤アクセントを使用。天気セルはすりガラス風で、現在時刻を強調表示。

🇺🇸 Reference mockups live in `stitch_macos_ui_with-weather/` and `stitch_macos_ui_enhancement/`.
🇻🇳 Mockup tham khảo nằm trong `stitch_macos_ui_with-weather/` và `stitch_macos_ui_enhancement/`.
🇯🇵 参考モックアップは `stitch_macos_ui_with-weather/` と `stitch_macos_ui_enhancement/` にあります。

## 🇺🇸 Version History / 🇻🇳 Lịch sử phiên bản / 🇯🇵 バージョン履歴

### 🇺🇸 1.1 (July 6, 2026) / 🇻🇳 1.1 (6 tháng 7, 2026) / 🇯🇵 1.1（2026年7月6日）

- 🇺🇸 Four clock faces: Analog, Digital, Segment, Day
- 🇻🇳 Bốn mặt đồng hồ: Analog, Digital, Segment, Day
- 🇯🇵 4つの文字盤: アナログ、デジタル、セグメント、デイ
- 🇺🇸 Optional hourly weather band with GPS location and Open-Meteo data
- 🇻🇳 Dải thời tiết theo giờ tùy chọn với GPS và dữ liệu Open-Meteo
- 🇯🇵 GPS と Open-Meteo データによる任意の時間別天気バンド
- 🇺🇸 Scrollable 1-hour timeline with emoji weather icons
- 🇻🇳 Dòng thời gian cuộn theo giờ với biểu tượng thời tiết emoji
- 🇯🇵 絵文字天気アイコン付きの1時間単位スクロールタイムライン
- 🇺🇸 Holiday and weekend highlighting by timezone region
- 🇻🇳 Đánh dấu ngày lễ và cuối tuần theo vùng múi giờ
- 🇯🇵 タイムゾーン地域に基づく祝日と週末のハイライト
- 🇺🇸 Window sizing that fits content and snaps flush to screen edges
- 🇻🇳 Cỡ cửa sổ vừa nội dung, sát mép màn hình
- 🇯🇵 コンテンツに合わせたウィンドウサイズ、画面端にぴったり配置
- 🇺🇸 About window with donation links and TPBank QR code
- 🇻🇳 Cửa sổ Giới thiệu với liên kết ủng hộ và mã QR TPBank
- 🇯🇵 寄付リンクと TPBank QR コード付きの「このアプリについて」ウィンドウ
- 🇺🇸 Launch at login support
- 🇻🇳 Hỗ trợ khởi động khi đăng nhập
- 🇯🇵 ログイン時起動のサポート

### 🇺🇸 1.0 (initial) / 🇻🇳 1.0 (ban đầu) / 🇯🇵 1.0（初版）

- 🇺🇸 Borderless floating always-on-top clock panel
- 🇻🇳 Bảng đồng hồ nổi không viền, luôn trên cùng
- 🇯🇵 枠なしの常に最前面の浮動時計パネル
- 🇺🇸 Analog and digital clock styles
- 🇻🇳 Kiểu đồng hồ Analog và Digital
- 🇯🇵 アナログとデジタルの時計スタイル
- 🇺🇸 Draggable window with saved position
- 🇻🇳 Cửa sổ kéo được, lưu vị trí
- 🇯🇵 ドラッグ可能で位置を保存するウィンドウ
- 🇺🇸 Size presets and 12/24-hour time
- 🇻🇳 Cỡ sẵn và giờ 12/24
- 🇯🇵 サイズプリセットと12/24時間表示

## 🇺🇸 Project Structure / 🇻🇳 Cấu trúc dự án / 🇯🇵 プロジェクト構成

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
└── release-notes.md              # Trilingual GitHub Release notes template
```

## 🇺🇸 Data Sources / 🇻🇳 Nguồn dữ liệu / 🇯🇵 データソース

- 🇺🇸 **Weather**: [Open-Meteo](https://open-meteo.com/) (no API key required)
- 🇻🇳 **Thời tiết**: [Open-Meteo](https://open-meteo.com/) (không cần API key)
- 🇯🇵 **天気**: [Open-Meteo](https://open-meteo.com/)（API キー不要）
- 🇺🇸 **Geocoding**: Open-Meteo Geocoding API + Apple `CLGeocoder` reverse geocoding
- 🇻🇳 **Địa lý**: Open-Meteo Geocoding API + reverse geocoding `CLGeocoder` của Apple
- 🇯🇵 **ジオコーディング**: Open-Meteo Geocoding API + Apple `CLGeocoder` 逆ジオコーディング
- 🇺🇸 **Holidays**: bundled public holiday data per country/region
- 🇻🇳 **Ngày lễ**: dữ liệu ngày lễ công cộng theo quốc gia/vùng có sẵn trong app
- 🇯🇵 **祝日**: 国/地域ごとの祝日データをアプリに同梱

## 🇺🇸 Privacy / 🇻🇳 Quyền riêng tư / 🇯🇵 プライバシー

- 🇺🇸 Location is requested only when **Show Weather** is enabled
- 🇻🇳 Vị trí chỉ được hỏi khi bật **Show Weather** (Hiện thời tiết)
- 🇯🇵 位置情報は **天気を表示** が有効なときのみ要求
- 🇺🇸 Coordinates are sent to Open-Meteo for forecast data
- 🇻🇳 Tọa độ được gửi tới Open-Meteo để lấy dự báo
- 🇯🇵 座標は予報取得のため Open-Meteo に送信
- 🇺🇸 No analytics or third-party tracking
- 🇻🇳 Không có phân tích hay theo dõi bên thứ ba
- 🇯🇵 アナリティクスや第三者トラッキングなし

## 🇺🇸 Author / 🇻🇳 Tác giả / 🇯🇵 作者

🇺🇸 **Fong Thai** is the creator and maintainer.
🇻🇳 **Fong Thai** là người tạo và duy trì dự án.
🇯🇵 **Fong Thai** が作成者兼メンテナーです。

| | |
|---|---|
| 🇺🇸 **GitHub**<br>🇻🇳 **GitHub**<br>🇯🇵 **GitHub** | [@fongthai](https://github.com/fongthai) |
| 🇺🇸 **Donate**<br>🇻🇳 **Ủng hộ**<br>🇯🇵 **寄付** | [Buy Me a Coffee](https://buymeacoffee.com/fongthai) |

🇺🇸 If Floating Clock is useful to you, a small donation helps support ongoing development. Bug reports and feature ideas are welcome on GitHub.
🇻🇳 Nếu Floating Clock hữu ích với bạn, một khoản ủng hộ nhỏ giúp duy trì phát triển. Báo lỗi và ý tưởng tính năng được chào đón trên GitHub.
🇯🇵 Floating Clock が役に立ったら、少額の寄付が開発の継続に役立ちます。バグ報告や機能提案は GitHub で歓迎します。

### 🇺🇸 TPBank transfer (Vietnam) / 🇻🇳 Chuyển khoản TPBank (Việt Nam) / 🇯🇵 TPBank 送金（ベトナム）

🇺🇸 You can also send a local bank transfer by scanning this TPBank QR code:
🇻🇳 Bạn cũng có thể chuyển khoản nội địa bằng cách quét mã QR TPBank này:
🇯🇵 この TPBank QR コードをスキャンして国内送金もできます:

![TPBank donation QR code](FloatingClock/Assets.xcassets/QR-TP-bank-for-donation.imageset/QR-TP-bank-for-donation.png)

## 🇺🇸 License / 🇻🇳 Giấy phép / 🇯🇵 ライセンス

🇺🇸 MIT
🇻🇳 MIT
🇯🇵 MIT
