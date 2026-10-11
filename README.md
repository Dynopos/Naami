# Naami Stable — Laman Web

Laman web satu halaman (HTML/CSS/JS tulen, tiada build) untuk Naami Stable, Pantai Senok, Bachok, Kelantan.

## Struktur
- `index.html` — keseluruhan laman (gaya & skrip sebaris)
- `assets/` — logo, gambar, poster pakej dan video promosi

## Voice note
Pemain voice note gaya WhatsApp berada di bahagian **Voice Note** dan memainkan
rakaman sebenar di `assets/voice-note.mp3` (40 saat). Untuk tukar rakaman, ganti fail itu
dengan nama yang sama.

- **Transkrip:** bahagian "Baca transkrip" disembunyikan selagi `RECORDING_TRANSCRIPT`
  dalam `index.html` kosong. Tampal teks voice note di situ untuk memaparkannya.
- **Sandaran:** jika fail audio tiada, pemain membaca tatasusunan `SCRIPT` menggunakan
  suara sintesis pelayar (Bahasa Melayu jika tersedia).

Pelawat juga boleh merakam voice note sendiri dan menghantarnya melalui WhatsApp.
Rakaman mikrofon memerlukan HTTPS (contohnya GitHub Pages / Netlify).
