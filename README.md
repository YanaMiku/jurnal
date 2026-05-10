# Trading Journal Pro 📊

Dashboard performa trading harian real-time dengan kurva ekuitas, distribusi hasil, dan activity log lengkap. Dirancang untuk trader profesional yang ingin mencatat dan menganalisis performa trading secara visual dan interaktif.

![Version](https://img.shields.io/badge/version-2.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Status](https://img.shields.io/badge/status-production%20ready-brightgreen)

---

## 🎯 Fitur Utama

### 📈 Dashboard Real-Time
- **Ringkasan Performa** — Win/Loss/BEP, Net P/L, Win Rate, Average Win/Loss
- **Kurva Ekuitas** — Visualisasi pergerakan balance secara real-time
- **Distribusi Hasil** — Pie chart Win/Loss/BEP yang interaktif
- **Cash Flow** — Tracking deposit dan withdraw harian
- **Activity Log** — Timeline lengkap semua aktivitas trading

### 📅 Kalender Interaktif
- Navigasi bulan dengan highlight otomatis
- Indikator warna berdasarkan profit/loss/BEP harian
- Auto-select ke tanggal hari ini saat pertama dibuka
- Klik untuk melihat detail performa tanggal tertentu

### 📋 Tabel Trade Lengkap
- **STATUS terpisah** — WIN (hijau), LOSS (merah), BEP (kuning)
- **Profit/Loss terpisah** — Tidak digabung dengan status
- Filter by Type (Buy/Sell) dan Result (Win/Loss/BEP)
- Search real-time by symbol atau ID
- Klik trade untuk detail lengkap dalam modal

### 📱 Fully Responsive & Mobile-First
- **Mobile**: Ultra-compact UI, tabel diubah jadi card, chart touch-friendly
- **Tablet**: Adaptive grid layout
- **Desktop**: Dashboard multi-column profesional
- **Touch Optimized**: Swipe, pinch zoom, drag chart dengan jari

### 🌙 Dark Mode Default
- Dark mode premium dengan warna #0B0F19
- Toggle light/dark dengan transisi halus
- Tersimpan di localStorage

### 🔄 Auto Refresh
- Refresh otomatis setiap 5 detik (bisa toggle ON/OFF)
- Countdown timer untuk refresh berikutnya
- Indikator LIVE dengan animasi pulse
- Tombol Refresh Now untuk update manual

### 💰 Deposit & Withdraw Tracking
- Card khusus Total Deposit dan Total Withdraw
- Net Cash Flow kalkulasi otomatis
- Timeline activity dengan icon berbeda (deposit/withdraw/trade)
- Filter activity berdasarkan kategori

### 📝 Catatan Harian
- Daily Summary (ringkasan harian)
- Psychology Notes (catatan psikologi)
- Strategy Notes (catatan strategi)
- Expandable section yang rapi

### 📤 Export & Share
- Export CSV semua trade
- Export detail individual trade
- Copy Trade ID dengan satu klik

### 🎨 UI/UX Premium
- **Glassmorphism** header dengan backdrop blur
- Hover effects & smooth transitions
- Skeleton loading states
- Toast notifications (success/error/info)
- Empty states yang informatif
- Splash screen dengan branding

---

## 🚀 Cara Menggunakan

### 1. Struktur Folder
```
project/
├── index.html          # Single file aplikasi
└── database/
    └── json/
        ├── 2026-05-08.json
        ├── 2026-05-09.json
        └── ...
```

### 2. Format JSON
Setiap file JSON merepresentasikan data trading satu hari. Format lengkap:

```json
{
  "date": "2026-05-08",
  "platform": {
    "name": "MetaTrader 5",
    "account_currency": "USD"
  },
  "account_summary": {
    "profit": 182.40,
    "deposit": 863.00,
    "withdraw": 0.00,
    "swap": 0.00,
    "commission": 0.00,
    "balance": 1045.40,
    "starting_balance": 863.00,
    "ending_balance": 1045.40,
    "trading_profit": 182.40,
    "net_profit": 182.40,
    "profit_percent": 21.14
  },
  "statistics": {
    "total_trades": 10,
    "winning_trades": 5,
    "losing_trades": 2,
    "break_even_trades": 3,
    "win_rate": 50.0,
    "gross_profit": 300.00,
    "gross_loss": -120.00,
    "largest_win": 60.00,
    "largest_loss": -60.00,
    "average_win": 60.00,
    "average_loss": -60.00,
    "average_bep": 0.60,
    "buy_trades": 6,
    "sell_trades": 4
  },
  "deposits": [
    {
      "id": "DEP-0001",
      "time": "14:31:24",
      "amount": 863.00,
      "type": "deposit",
      "method": "Internal Transfer",
      "reference": "18649694",
      "note": "Int. Trans. from: 18649694"
    }
  ],
  "withdrawals": [],
  "activity_history": [
    {
      "category": "trade",
      "time": "15:04:42",
      "symbol": "XAUUSDc",
      "status": "WIN",
      "profit_loss": 60.00
    }
  ],
  "trades": [
    {
      "id": "TRD-0001",
      "time": "15:04:42",
      "symbol": "XAUUSDc",
      "type": "sell",
      "lot": 0.06,
      "entry_price": 4723.42,
      "exit_price": 4713.42,
      "profit_loss": 60.00,
      "status": "WIN",
      "swap": 0.00,
      "commission": 0.00,
      "session": "Unknown",
      "market_type": "Gold",
      "source": "MT5 History Screenshot"
    }
  ],
  "chart_data": {
    "equity_curve": [863.00, 923.00, 983.00, ...],
    "profit_distribution": {
      "win": 5,
      "loss": 2,
      "bep": 3
    }
  },
  "notes": {
    "daily_summary": "Profitable trading day.",
    "psychology": "Discipline maintained.",
    "strategy": "Support/resistance breakout."
  }
}
```

### 3. Menjalankan Aplikasi
Cukup buka `index.html` di browser. Tidak perlu server, build tools, atau dependency tambahan.

> **Catatan**: Karena membaca file JSON lokal, disarankan menggunakan local server sederhana untuk menghindari CORS:
> ```bash
> # Python 3
> python -m http.server 8000
>
> # Node.js
> npx serve .
> ```

---

## 🛠️ Teknologi

| Teknologi | Penggunaan |
|-----------|------------|
| **Tailwind CSS** | Utility-first CSS framework via CDN |
| **Chart.js** | Library chart interaktif dengan plugin zoom |
| **Lucide Icons** | Icon library profesional (no emoji) |
| **Vanilla JavaScript** | No framework, pure JS ES6+ |
| **Inter Font** | Typography modern dari Google Fonts |

---

## ✨ Fitur Detail

### Tabel Trade
- **8 Kolom Desktop**: ID/Waktu, Symbol, Tipe, Lot, Entry, Exit, P/L, STATUS
- **STATUS dipisah** dari Profit/Loss: Badge WIN (hijau), LOSS (merah), BEP (kuning)
- **Profit/Loss**: Hanya angka dengan format currency, warna otomatis
- **Mobile View**: Card layout compact dengan informasi esensial

### Chart Interaktif
- **Equity Curve**: Line chart dengan gradient fill, draggable, pinch zoom, tooltip currency
- **Pie Chart**: Doughnut chart Win/Loss/BEP dengan legend dan animasi
- **Touch Support**: `touch-action: pan-x pan-y pinch-zoom` untuk mobile

### Kalender
- Grid 7 kolom (Senin-Minggu)
- Dot indicator warna: Hijau (profit), Merah (loss), Kuning (BEP)
- Navigasi bulan dengan tombol prev/next
- Auto-highlight hari ini dengan ring biru
- Klik tanggal untuk load data

### Activity Log
- Icon berbeda per kategori (chart, download, upload)
- Warna background berbeda (biru, hijau, orange)
- Filter dropdown: All, Trade, Deposit, Withdraw
- Format currency otomatis dengan warna profit/loss

### Modal Detail Trade
- Full trade info: Entry, Exit, Swap, Commission, Session, Market, Source
- Timeline visual entry → exit dengan dot indikator
- Tombol Copy ID & Export Trade
- Backdrop blur + animasi slide-up

---

## 📐 Responsive Breakpoints

| Breakpoint | Layout | Spesifikasi |
|------------|--------|-------------|
| **< 640px** | Mobile | Ultra-compact, card trade, chart 170px, font lebih kecil |
| **640-1024px** | Tablet | Adaptive grid, tabel muncul, chart sedang |
| **> 1024px** | Desktop | Multi-column dashboard, tabel penuh, chart 260px |

---

## 🎨 Design System

| Elemen | Light Mode | Dark Mode |
|--------|------------|-----------|
| Background | `#f3f4f6` | `#0B0F19` |
| Surface | `#ffffff` | `#111827` |
| Card | `#ffffff` | `#0F172A` |
| Border | `#e5e7eb` | `#1F2937` |
| Profit | `#10B981` | `#10B981` |
| Loss | `#EF4444` | `#EF4444` |
| BEP | `#F59E0B` | `#F59E0B` |
| Accent | `#3B82F6` | `#3B82F6` |

---

## 🔧 Konfigurasi

Semua konfigurasi ada di dalam `CONFIG` object di JavaScript:

```javascript
const CONFIG = {
    DATA_BASE_PATH: './database/json/',  // Path folder JSON
    AUTO_REFRESH_INTERVAL: 5000,          // Interval refresh (ms)
};
```

---

## 🏷️ Branding

- **Nama**: Trading Journal Pro
- **Subtitle**: Dashboard performa harian
- **Icon**: Line chart dengan gradient biru
- **Design By**: YanaMiku
- **Versi**: v2.0

---

## 📋 Fitur yang Belum Diimplementasi

- [ ] Pagination untuk tabel trade (saat ini semua ditampilkan)
- [ ] Sorting kolom tabel (click header)
- [ ] Multi-currency support
- [ ] Import JSON via drag & drop
- [ ] Grafik tambahan (Buy vs Sell, Profit Distribution Bar)
- [ ] PWA manifest untuk install ke homescreen

---

## 🤝 Kontribusi

Project ini adalah single-file application. Untuk mengembangkan:

1. Edit langsung `index.html`
2. Test dengan local server
3. Pastikan tetap single file (no external CSS/JS selain CDN)
4. Jaga kompatibilitas mobile-first

---

## 📄 Lisensi

MIT License — bebas digunakan, dimodifikasi, dan didistribusikan.

---

## 👨‍💻 Credits

**Design & Development by YanaMiku**

Dibangun dengan:
- [Tailwind CSS](https://tailwindcss.com/)
- [Chart.js](https://www.chartjs.org/)
- [Lucide Icons](https://lucide.dev/)
- [Inter Font](https://fonts.google.com/specimen/Inter)

---

*© 2026 Trading Journal Pro. All rights reserved.*