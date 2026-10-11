# Naami Stable — Laman Web

Laman web satu halaman (HTML/CSS/JS tulen, tiada build) untuk Naami Stable, Pantai Senok, Bachok, Kelantan.

## Struktur
- `index.html` — keseluruhan laman (gaya & skrip sebaris)
- `assets/` — logo, gambar, poster pakej dan video promosi

## Voice note
Pemain voice note gaya WhatsApp berada di bahagian **Voice Note**.

- **Guna rakaman sebenar (disyorkan):** letak fail audio anda di `assets/voice-note.mp3`.
  Pemain akan memainkannya secara automatik dengan tempoh sebenar.
- **Tanpa fail:** pemain membaca skrip sapaan menggunakan suara sintesis pelayar
  (Bahasa Melayu jika tersedia). Ubah teks dalam tatasusunan `SCRIPT` dalam `index.html`.
  Kalau anda guna rakaman sendiri, kemas kini juga `SCRIPT` supaya transkrip sepadan.

Pelawat juga boleh merakam voice note sendiri dan menghantarnya melalui WhatsApp.
Rakaman mikrofon memerlukan HTTPS (contohnya GitHub Pages / Netlify).
