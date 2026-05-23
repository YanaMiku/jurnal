# Trading Journal Pro - Dokumentasi Lengkap

## 📋 Deskripsi

Trading Journal Pro adalah dashboard performa trading harian real-time yang dirancang untuk trader profesional. Aplikasi ini memungkinkan trader untuk memantau, menganalisis, dan mengevaluasi aktivitas trading mereka dengan berbagai metrik lanjutan dan visualisasi data interaktif.

## ✨ Fitur Utama

### 1. Dashboard Real-time
- Tampilan ringkasan performa trading harian
- Update data otomatis setiap 30 detik
- Indikator LIVE untuk status koneksi real-time
- Header dinamis yang menampilkan status profit/loss

### 2. Kalender Interaktif
- Navigasi bulan dengan tombol Previous/Next
- Pilih bulan dan tahun dari dropdown
- Tombol Today untuk kembali ke tanggal saat ini
- Indikator warna pada setiap tanggal:
  - Hijau = Profit
  - Merah = Loss
  - Kuning = BEP (Break Even Point)
  - Abu-abu = Tidak ada data
- Highlight ring biru untuk tanggal hari ini

### 3. Metrik Performa Utama
- **WIN**: Jumlah trade menang dan total profit
- **LOSS**: Jumlah trade kalah dan total loss
- **BEP**: Jumlah trade impas
- **NET P/L**: Net profit/loss hari ini

### 4. Metrik Keuangan
- **DEPOSIT**: Total deposit hari ini
- **WITHDRAW**: Total withdraw hari ini
- **NET CASH**: Selisih deposit dan withdraw

### 5. Statistik Lanjutan
- **Profit Factor**: Rasio gross profit terhadap gross loss
- **Expectancy**: Rata-rata profit per trade
- **Max Drawdown**: Penarikan maksimum dari puncak equity
- **Sharpe Ratio**: Ukuran risk-adjusted return
- **Total Trades**: Jumlah total transaksi
- **Win Rate**: Persentase kemenangan
- **Avg Win**: Rata-rata profit untuk trade menang
- **Avg Loss**: Rata-rata loss untuk trade kalah
- **Balance**: Saldo akhir
- **Start Equity**: Ekuitas awal

### 6. Visualisasi Data
- **Kurva Ekuitas**: Grafik line interaktif dengan fitur zoom (pinch 2 jari)
- **Distribusi Hasil**: Pie chart untuk melihat proporsi Win/Loss/BEP
- Warna dinamis pada grafik (hijau untuk profit, merah untuk loss)

### 7. Catatan Harian
- Ringkasan harian
- Catatan psikologi trading
- Catatan strategi trading

### 8. Manajemen Trade
- **Pencarian**: Cari trade berdasarkan simbol atau ID
- **Filter**: Filter berdasarkan tipe (Buy/Sell) dan hasil (Win/Loss/BEP)
- **Tabel Trade**: Menampilkan detail lengkap setiap trade
- **Mobile View**: Card layout untuk perangkat mobile
- **Modal Detail**: Klik pada trade untuk melihat detail lengkap

### 9. Activity Log
- Riwayat aktivitas trading
- Filter berdasarkan kategori (Trade/Deposit/Withdraw)
- Timestamp setiap aktivitas

### 10. Fitur Ekspor Data
- **CSV Export**: Ekspor data trade ke format CSV
- **PDF Export**: Ekspor dashboard ke PDF
- **JSON Export**: Ekspor data lengkap dengan metadata
- **Single Trade Export**: Ekspor detail trade individual

### 11. Auto Refresh
- Refresh otomatis setiap 30 detik
- Toggle ON/OFF
- Countdown timer menampilkan sisa waktu
- Silent refresh tanpa mengganggu user experience

### 12. Notifikasi & Alert
- Notifikasi browser untuk:
  - Alert 3x consecutive losses
  - Alert 3x consecutive wins
- Muncul hanya saat tab tidak aktif

### 13. Backup & Restore
- Auto-save data ke localStorage
- Restore otomatis jika data tidak tersedia
- Maksimal 30 backup tersimpan

### 14. Keyboard Shortcuts
| Shortcut | Fungsi |
|----------|--------|
| Ctrl+R | Refresh data |
| Ctrl+E | Export CSV |
| Ctrl+D | Go to Today |
| ← / → | Navigasi bulan |
| Escape | Tutup modal |

### 15. Performance Monitoring
- Tracking waktu eksekusi operasi berat
- Warning jika operasi > 100ms
- Optimasi rendering chart

### 16. Analytics Tracking
- Mencatat event user (export, refresh, view trade, dll)
- Tersimpan di localStorage
- Membantu analisis penggunaan aplikasi

### 17. Dark Mode
- Toggle tema gelap/terang
- Menyimpan preferensi user
- Seluruh komponen mengikuti tema

### 18. Responsive Design
- Fully responsive untuk desktop, tablet, dan mobile
- Mobile menu sidebar
- Touch-friendly untuk perangkat sentuh
- Adaptive font sizing

## 🛠️ Teknologi yang Digunakan

| Teknologi | Versi | Kegunaan |
|-----------|-------|----------|
| HTML5 | - | Struktur halaman |
| Tailwind CSS | 3.x | Styling dan responsive design |
| JavaScript (ES6+) | - | Logika aplikasi |
| Chart.js | 4.4.0 | Visualisasi grafik |
| chartjs-plugin-zoom | 2.0.1 | Zoom pada grafik equity |
| Lucide Icons | Latest | Icon library |
| html2pdf.js | 0.10.1 | Export ke PDF |

## 📁 Struktur Data

### Format JSON yang Diharapkan

```json
{
  "account_summary": {
    "trading_profit": 1250.50,
    "net_profit": 1250.50,
    "profit_percent": 5.2,
    "starting_balance": 25000,
    "ending_balance": 26250.50,
    "deposit": 1000,
    "withdraw": 500
  },
  "statistics": {
    "total_trades": 15,
    "win_rate": 66.67,
    "average_win": 150.25,
    "average_loss": 75.50
  },
  "trades": [
    {
      "id": "TRD001",
      "time": "10:30:00",
      "symbol": "XAUUSD",
      "type": "buy",
      "lot": 0.5,
      "entry_price": 2350.25,
      "exit_price": 2360.50,
      "profit": 512.50,
      "result": "WIN",
      "swap": 0,
      "commission": 10,
      "session": "London",
      "market_type": "Forex",
      "source": "Manual"
    }
  ],
  "deposits": [
    { "amount": 1000, "time": "09:00:00" }
  ],
  "withdrawals": [
    { "amount": 500, "time": "15:30:00" }
  ],
  "notes": {
    "daily_summary": "Good trading day",
    "psychology": "Stayed disciplined",
    "strategy": "Followed system rules"
  },
  "activity_history": [
    {
      "category": "trade",
      "description": "Opened position XAUUSD",
      "amount": 0,
      "time": "10:30:00"
    }
  ],
  "chart_data": {
    "equity_curve": [25000, 25100, 25250, 25150, 26250.50]
  }
}
```

## 🚀 Cara Penggunaan

### Instalasi

1. **Download** file `index.html`
2. **Tempatkan** di web server atau buka langsung di browser
3. **Pastikan** koneksi internet aktif (untuk mengakses CDN dan data)

### Konfigurasi Data Source

Ubah `DATA_BASE_URL` di dalam script sesuai dengan lokasi file JSON:

```javascript
const CONFIG = {
    DATA_BASE_URL: 'https://raw.githubusercontent.com/username/repo/main/database/json/',
    AUTO_REFRESH_INTERVAL: 30000,
};
```

### Penggunaan Sehari-hari

1. **Pilih Tanggal**: Klik pada kalender atau gunakan navigasi bulan
2. **Monitor Performa**: Lihat metrik utama di dashboard
3. **Analisis Grafik**: Zoom pada equity curve (pinch 2 jari di mobile)
4. **Filter Trade**: Gunakan search dan filter untuk menemukan trade spesifik
5. **Export Data**: Gunakan tombol CSV, PDF, atau JSON untuk backup
6. **Aktifkan Notifikasi**: Klik "Enable Notifications" untuk alert real-time

### Shortcut yang Berguna

- Tekan `Ctrl+R` untuk refresh data manual
- Gunakan `←/→` untuk navigasi bulan tanpa klik
- `Ctrl+E` untuk export cepat ke CSV
- `Ctrl+D` untuk kembali ke hari ini

## 🎨 UI/UX Features

### Color Coding
- **Profit**: Hijau (#10B981)
- **Loss**: Merah (#EF4444)
- **BEP**: Kuning (#F59E0B)
- **Neutral**: Abu-abu (#6B7280)
- **Accent**: Biru (#3B82F6)

### Animasi
- Fade-in untuk konten
- Slide-up untuk modal
- Pulse untuk live indicator
- Shimmer untuk skeleton loader
- Float untuk empty state icon
- Shine untuk performance badge

### Loading States
- Skeleton loader untuk initial load
- Overlay dengan spinner untuk perubahan bulan
- Progress indicator untuk auto-refresh

## 📊 Fitur Analytics

### Advanced Metrics Calculation

**Profit Factor**
```
Profit Factor = Gross Profit / |Gross Loss|
```

**Expectancy**
```
Expectancy = (Average Win × Win Rate) - (Average Loss × Loss Rate)
```

**Max Drawdown**
```
Drawdown = (Peak Equity - Trough Equity) / Peak Equity × 100%
```

**Sharpe Ratio**
```
Sharpe Ratio = √252 × (Average Return / Standard Deviation of Returns)
```

## 🔒 Privacy & Security

- **No External Tracking**: Tidak ada Google Analytics atau tracking pihak ketiga
- **Local Storage Only**: Data backup disimpan di localStorage pengguna
- **No Data Upload**: Aplikasi hanya membaca data dari GitHub repository
- **Read-Only**: Tidak ada fitur edit/write ke server

## 🌐 Browser Support

| Browser | Versi Minimal | Status |
|---------|---------------|--------|
| Chrome | 90+ | ✅ Full Support |
| Firefox | 88+ | ✅ Full Support |
| Safari | 14+ | ✅ Full Support |
| Edge | 90+ | ✅ Full Support |
| Opera | 76+ | ✅ Full Support |
| Mobile Chrome | 90+ | ✅ Full Support |
| Mobile Safari | 14+ | ✅ Full Support |

## 📱 Mobile Features

- **Sidebar**: Menu hamburger dengan overlay
- **Touch Events**: Pinch-to-zoom pada chart
- **Card Layout**: Tampilan trade dalam bentuk card
- **Responsive Typography**: Font size menyesuaikan layar
- **Viewport Meta**: Optimasi untuk mobile viewport

## 🎯 Performance Optimization

- **Lazy Loading**: Chart hanya dirender saat visible
- **Chart Reuse**: Destroy dan rebuild chart hanya saat perlu
- **Debounced Filters**: Event handler di-optimasi
- **Efficient Rendering**: Incremental update untuk perubahan data
- **Memory Management**: Chart instance dibersihkan sebelum rebuild

## 🧪 Testing

### Data Validation
```javascript
// Validasi otomatis untuk setiap trade
- Field required: id, symbol, profit, result, time
- Validasi tipe data profit (number)
- Warning console untuk data invalid
```

### Error Handling
- Fallback ke backup jika fetch gagal
- Graceful degradation untuk chart
- Toast notification untuk error user-friendly

## 🔧 Troubleshooting

### Masalah: Kalender tidak sesuai hari
**Solusi**: Refresh halaman (Ctrl+R) atau clear cache browser

### Masalah: Data tidak muncul
**Solusi**: 
1. Periksa koneksi internet
2. Pastikan URL data source benar
3. Cek console browser untuk error

### Masalah: Chart tidak tampil
**Solusi**:
1. Refresh halaman
2. Periksa konsol browser untuk error JavaScript
3. Pastikan CDN Chart.js dapat diakses

### Masalah: Export PDF gagal
**Solusi**:
1. Pastikan library html2pdf.js terload
2. Coba dengan data yang lebih sedikit
3. Gunakan export CSV atau JSON sebagai alternatif

## 📈 Roadmap Fitur Mendatang

- [ ] Multiple timeframe analysis (weekly, monthly)
- [ ] Performance comparison antar periode
- [ ] Trading journal dengan notes dan screenshot
- [ ] Integration dengan broker API (real-time)
- [ ] Risk metrics (RR ratio, position sizing)
- [ ] Email report harian/mingguan
- [ ] PWA installation support
- [ ] Multi-language support (EN, ID, CN)
- [ ] Custom dashboard widgets
- [ ] Trading session analysis

## 👥 Kontribusi

Fitur yang dapat dikembangkan:
1. **Backend Integration**: Node.js/Express untuk autentikasi user
2. **Database**: MongoDB/PostgreSQL untuk multi-user support
3. **Real-time WebSocket**: Untuk data live dari broker
4. **Machine Learning**: Prediksi performa berdasarkan pola
5. **Social Features**: Sharing insight dengan komunitas

## 📄 Lisensi

Private Use Only - Designed by YanaMiku

## 🙏 Credits

- **Design & Development**: YanaMiku
- **Icons**: Lucide Icons
- **Charts**: Chart.js
- **Styling**: Tailwind CSS
- **PDF Export**: html2pdf.js

## 📞 Kontak & Support

Untuk pertanyaan, saran, atau laporan bug:
- GitHub Issues: [Repository Link]
- Email: [Contact Email]
- Telegram: [Group Link]

---

**Version**: 4.0
**Last Updated**: 2026
**Status**: Production Ready ✅

*Trading Journal Pro - Empowering traders with data-driven insights*
