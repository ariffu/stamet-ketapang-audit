# Audit Metrologi & Stabilitas Operasional Sensor AWS vs SYNOP (2018–2026)
### Stasiun Meteorologi Kelas III Rahadi Oesman Ketapang (WMO ID: 96685)
Badan Meteorologi, Klimatologi, dan Geofisika (BMKG)

🌐 **Live Web Report (GitHub Pages):** [https://ariffu.github.io/stamet-ketapang-audit/](https://ariffu.github.io/stamet-ketapang-audit/)

---

## 📌 Ringkasan Eksekutif
Repositori ini memuat laporan interaktif dan hasil audit metrologi komprehensif terhadap kinerja sensor otomatis **AWS Digital** berdampingan dengan pengamatan manual **SYNOP (Termometer Gelas & Barometer Konvensional)** selama periode **8 tahun (2018–2025)** serta verifikasi kalibrasi komparasi lapangan (*on-site standard*) tahun **2023, 2024, 2025, dan 2026**.

### Temuan Utama:
1. **Kesesuaian Ekstrem Suhu ($T_{\max}$ & $T_{\min}$):**
   - $T_{\max}$: Selisih rerata (MAE) hanya **$0.12^\circ\text{C}$** dengan kepatuhan WMO ($\le \pm 0.5^\circ\text{C}$) mencapai **98.4%**.
   - $T_{\min}$: Selisih rerata (MAE) hanya **$0.05^\circ\text{C}$** dengan kepatuhan WMO mencapai **99.1%**.
   - Suhu Jam-jaman ($T_{\text{hr}}$): MAE **$0.09^\circ\text{C}$** dengan kepatuhan WMO **98.5%**.
2. **Kesesuaian Kelembapan Udara (RH):**
   - MAE hanya **$0.96\%$** dengan kepatuhan WMO ($\le \pm 3\%$) mencapai **98.7%**.
3. **Harmonisasi Tekanan Udara (QFE vs QFF):**
   - Perbedaan pelaporan SYNOP ($QFF$) dan AWS ($QFE$) adalah murni reduksi elevasi barometrik $\Delta P = \rho \cdot g \cdot h \approx 1.5\text{ hPa}$. Setelah penyamaan datum, kepatuhan WMO mencapai **97.2%**.
4. **Stabilitas & Interval Kalibrasi 2 Tahun:**
   - Laju degradasi (*sensor drift*) mendekati $0.00^\circ\text{C}/\text{tahun}$.
   - Simulasi 2 tahun tanpa kalibrasi komparasi lapangan membuktikan deviasi sensor tetap berada jauh di dalam batas toleransi WMO No. 8 ($\pm 0.3^\circ\text{C}$), sehingga perpanjangan siklus kalibrasi komparasi menjadi 2 tahun aman dan valid secara operasional.

---

## 📊 Struktur Repositori & Visualisasi
- `index.html` : Halaman dashboard web interaktif lengkap dengan ringkasan eksekutif, tabel metrologi, komparasi grafik resolusi tinggi, dan rekomendasi operasional.
- `assets/` : Grafik audit analitis:
  - `plot_parameter_diurnal_aws_synop.png` : Siklus diurnal suhu, kelembapan, gelombang pasang surut atmosfer semidiurnal, dan korelasi hujan harian.
  - `plot_perbedaan_synop_aws_tmax_tmin_qfe_qff_wmo_8tahun.png` : Evaluasi 8 tahun komparasi parameter sesuai standar WMO No. 8.
  - `plot_pemetaan_kalibrasi_standar_aws_synop_2023_2026.png` : Pemetaan hasil kalibrasi komparasi terhadap AWS Standar BMKG (2023–2026).
  - `plot_evaluasi_interval_kalibrasi_2tahun_aws.png` : Evaluasi margin toleransi interval kalibrasi 2 tahun.
  - `plot_audit_boxplot_degradasi_sensor_2018_2025.png` : Audit kestabilan tahunan boxplot degradasi sensor 2018–2025.
  - `plot_audit_boxplot_deviasi_standar_aws_synop.png` : Sebaran deviasi kalibrasi komparasi lapangan terhadap standar BMKG.

---
© 2018–2026 Stasiun Meteorologi Kelas III Rahadi Oesman Ketapang - BMKG.
