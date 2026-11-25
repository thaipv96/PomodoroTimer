# Pomodrone — Precision Pomodoro & Flowtime Web Application

> **Zero-Dependency · Offline-First PWA · Drift-Free Web Worker Timer · Synthesized Web Audio · Material Design 3 + AMOLED Pure Black**

[Tiếng Việt](#tiếng-việt) | [English](#english)

---

## Tiếng Việt

**Pomodrone** là ứng dụng web đồng hồ Pomodoro & Flowtime được thiết kế theo triết lý **không phụ thuộc thư viện ngoài (Zero-Dependency)** và **ưu tiên hoạt động ngoại tuyến (Offline-First)**. Toàn bộ giao diện, bộ đếm thời gian chống trễ nhịp và bộ tổng hợp âm thanh đều gói gọn trong tệp `index.html` duy nhất, khởi chạy tức thì dưới 50ms và sẵn sàng xuất bản trực tiếp lên **GitHub Pages**.

### Tính năng nổi bật

* **Bộ đếm chống trễ nhịp (Drift-Free Engine):** Sử dụng mốc thời gian đích tuyệt đối (`Date.now()`) kết hợp **Inline Web Worker** chạy ngầm và sự kiện `visibilitychange` — đảm bảo đồng hồ không bao giờ bị sai lệch khi chuyển tab hay tắt màn hình.
* **Chế độ Flowtime (Overtime):** Tùy chọn đếm tiếp thời gian làm thêm (`+00:01`, `+00:02`...) khi hết giờ tập trung thay vì ngắt ngang trạng thái tập trung sâu (Deep Work).
* **Tổng hợp âm thanh 100% bằng Web Audio API:**
  * 4 âm báo kết thúc phiên không cần tệp `.mp3`: *Crystal Bell*, *Warm Marimba*, *Digital Pulse*, *Soft Gong*.
  * Bộ phát tiếng ồn tập trung toán học thời gian thực: **White Noise**, **Pink Noise**, **Brown Noise** kèm bộ lọc thông thấp và điều chỉnh âm lượng mượt mà.
* **3 Giao diện tối ưu thị giác:** **AMOLED Pure Black (`#000000`)**, **Material Dark (`#121214`)**, và **Material Light (`#F6F8FA`)** với bảng màu động thay đổi theo từng pha làm việc / nghỉ ngơi.
* **Song ngữ ổn định bố cục (VI / EN):** Chuyển đổi tức thì giữa Tiếng Việt và Tiếng Anh với kích thước nút và lưới cố định (Zero Layout Shift).
* **Quản lý tác vụ & Thống kê năng suất cục bộ:** Theo dõi số phiên thực tế/dự kiến trên từng đầu việc, chuỗi ngày duy trì liên tục (Streak), biểu đồ cột 7 ngày, biểu đồ nhiệt 24 giờ, sao lưu/khôi phục JSON và xuất báo cáo CSV.
* **Cài đặt như ứng dụng gốc (PWA):** Hỗ trợ Service Worker (`sw.js`) và `manifest.json` để cài đặt lên Desktop, Android và iOS.

### Phím tắt bàn phím

| Phím tắt | Chức năng |
| :--- | :--- |
| `Space` | Bắt đầu / Tạm dừng / Hoàn tất phiên Flowtime |
| `R` | Đặt lại phiên hiện tại |
| `S` | Bỏ qua phiên hiện tại |
| `F` | Bật / Tắt chế độ tối giản toàn màn hình (Zen Mode) |
| `M` | Tắt / Bật toàn bộ âm thanh |
| `Esc` | Thoát hộp thoại cài đặt hoặc chế độ Zen |

### Hướng dẫn triển khai lên GitHub Pages

1. Tạo một kho lưu trữ (Repository) mới trên GitHub và tải toàn bộ mã nguồn này lên nhánh `main`.
2. Truy cập **Settings → Pages** trong kho lưu trữ của bạn.
3. Tại mục **Build and deployment → Source**, chọn **GitHub Actions**.
4. Workflow `.github/workflows/deploy-pages.yml` sẽ tự động kích hoạt và xuất bản ứng dụng với chứng chỉ HTTPS đầy đủ.

---

## English

**Pomodrone** is a precision-engineered, zero-dependency, offline-first Pomodoro & Flowtime Progressive Web App (PWA). Built entirely with semantic HTML5, modern CSS3 (Material Design 3 + Pure Black AMOLED), and Vanilla ES2023+ JavaScript, it boots in under 50ms with zero external CDNs or tracking.

### Core Highlights

* **Drift-Free Timing Engine:** Uses absolute target timestamps (`Date.now()`), an **Inline Web Worker** background ticker, and `visibilitychange` synchronization so background tab throttling never affects timer accuracy.
* **Flowtime (Overtime) Mode:** Optionally transition smoothly into an upward overtime counter when a focus block finishes instead of abruptly interrupting deep work.
* **Pure Web Audio API Synthesizer:**
  * 4 procedural completion chimes (*Crystal Bell*, *Warm Marimba*, *Digital Pulse*, *Soft Gong*) — zero `.mp3` assets required.
  * Real-time procedural **White, Pink, and Brown Noise** generator with low-pass filtering and optional auto-pause during breaks.
* **Three Adaptive Themes:** **AMOLED Pure Black (`#000000`)**, **Material Dark (`#121214`)**, and **Material Light (`#F6F8FA`)** with phase-aware dynamic accents.
* **Zero-Layout-Shift Bilingual UI (`VI` / `EN`):** Instant Vietnamese and English switching using fixed-dimension grids and `tabular-nums` typography.
* **Integrated Task Drawer & Local Analytics:** Track estimated vs. completed Pomodoros per task, daily streaks, 7-day bar chart, 24-hour focus heatmap, JSON backup/restore, and CSV export.

### Repository Structure

```text
pomodoro-web-app/
├── .github/
│   ├── workflows/
│   │   ├── ci-quality.yml        # Automated zero-dependency & PWA integrity check
│   │   └── deploy-pages.yml      # Automated GitHub Pages deployment
│   └── ISSUE_TEMPLATE/
│       ├── bug_report.md
│       └── feature_request.md
├── icons/
│   ├── icon.svg
│   ├── icon-192.png
│   └── icon-512.png
├── index.html                    # Complete standalone single-file web application
├── manifest.json                 # PWA Web App Manifest
├── sw.js                         # Offline-first Service Worker
├── README.md                     # Bilingual documentation
├── CHANGELOG.md                  # Release history
└── LICENSE                       # MIT License
```
