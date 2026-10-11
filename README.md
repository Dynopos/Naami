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
Voice note (`assets/voice-note.mp3`) mula berbunyi pada sentuhan/klik pertama di mana-mana
bahagian laman — pelayar tidak membenarkan audio berbunyi sebelum pelawat berinteraksi, dan
skrol sahaja tidak memulakannya. Butang bulat kecil di kiri bawah menghidupkan/mematikan bunyi.
Untuk tukar rakaman, ganti fail itu dengan nama yang sama.
