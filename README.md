# PocketBook — PWA Bahasa Malaysia

## Terbitkan melalui GitHub Pages
1. Cipta repositori GitHub baharu.
2. Muat naik **semua kandungan folder ini** ke akar repositori. Pastikan `index.html`, `manifest.webmanifest`, `sw.js`, dan folder `icons` berada di akar.
3. Dalam repositori, buka **Settings → Pages**.
4. Di bawah Build and deployment, pilih **Deploy from a branch**, branch `main`, folder `/(root)`, kemudian tekan **Save**.
5. Tunggu GitHub Pages menerbitkan laman HTTPS.
6. Buka pautan laman tersebut pada telefon. Android: menu Chrome → **Install app**. iPhone: Safari → Share → **Add to Home Screen**.

## Nota
- PWA memerlukan HTTPS atau localhost untuk pemasangan dan service worker.
- Fail luar seperti Tailwind CSS, Font Awesome, Google Fonts, dan html2pdf.js masih dimuatkan daripada CDN; oleh itu ciri teras mungkin boleh dibuka luar talian selepas cache, tetapi sumber CDN tertentu memerlukan internet.
- Rekod aplikasi asal disimpan dalam storan pelayar peranti. Eksport CSV dan sambungan Google Sheets boleh digunakan untuk sandaran. Memasang pada peranti lain tidak memindahkan rekod secara automatik.
- Semak dan uji pengiraan penyata sebelum digunakan untuk pemfailan rasmi atau tujuan cukai.
