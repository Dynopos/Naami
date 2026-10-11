# Naami Stable — Laman Web

Laman web satu halaman (HTML/CSS/JS tulen, tiada build) untuk Naami Stable, Pantai Senok, Bachok, Kelantan.

## Struktur
- `index.html` — keseluruhan laman (gaya & skrip sebaris)
- `assets/` — logo, gambar, poster pakej, video dan voice note
- `CNAME` — domain GitHub Pages (`naamistable.my`)

## Video (reels)
Bahagian **Video** memaparkan tiga video menegak: `reel-beach-ride.mp4`, `reel-stable-horses.mp4`
dan `naami-promo.mp4`. Video main sendiri tanpa bunyi bila kelihatan; pelawat tekan ikon bunyi
untuk dengar. Hanya satu sumber audio berbunyi pada satu masa (video atau voice note).
Video baharu dimampatkan dengan ffmpeg sebelum dimuat naik, contohnya:

    ffmpeg -i asal.mp4 -c:v libx264 -crf 26 -maxrate 1500k -bufsize 3000k -c:a aac -b:a 96k -movflags +faststart assets/reel-baru.mp4

## Voice note
Pemain voice note gaya WhatsApp berada di bahagian **Voice Note** dan memainkan
rakaman sebenar di `assets/voice-note.mp3` (40 saat). Untuk tukar rakaman, ganti fail itu
dengan nama yang sama.

- **Autoplay:** voice note mula main sendiri pada sentuhan/klik pertama di mana-mana bahagian
  laman (pelayar tidak membenarkan audio berbunyi sebelum pelawat berinteraksi). Skrol sahaja
  tidak memulakannya. Butang kecil terapung di kiri bawah membolehkan pelawat menjeda audio.
  Untuk matikan, padam baris `AUTOPLAY_EVENTS.forEach(t => addEventListener(...))` dalam `index.html`.
- **Transkrip:** bahagian "Baca transkrip" disembunyikan selagi `RECORDING_TRANSCRIPT`
  dalam `index.html` kosong. Tampal teks voice note di situ untuk memaparkannya.
- **Sandaran:** jika fail audio tiada, pemain membaca tatasusunan `SCRIPT` menggunakan
  suara sintesis pelayar (Bahasa Melayu jika tersedia).

Pelawat juga boleh merakam voice note sendiri dan menghantarnya melalui WhatsApp.
Rakaman mikrofon memerlukan HTTPS (contohnya GitHub Pages / Netlify).
