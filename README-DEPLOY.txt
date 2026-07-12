================================================================
 DEPLOY KE RENDER.COM (STATIC SITE) - PIXYO LANDING PAGE
================================================================

STRUKTUR FOLDER (semua kongsi SATU subdomain = jimat):
  render-site/
    index.html          -> auto-redirect ke /wedding/
    wedding/index.html   -> Landing page Versi A
    wedding-b/index.html -> Landing page Versi B
    images/              -> gambar dikongsi semua page

URL selepas deploy (contoh):
  https://pixyo.onrender.com/          -> redirect ke /wedding/
  https://pixyo.onrender.com/wedding/    (Versi A)
  https://pixyo.onrender.com/wedding-b/  (Versi B)

  -> SATU static site, SATU subdomain, DUA (atau lebih) landing page.
     Nak tambah landing page baru? Buat folder baru je, cth:
     render-site/raya/index.html -> /raya/  (tak perlu subdomain baru)

----------------------------------------------------------------
 LANGKAH DEPLOY
----------------------------------------------------------------
1. Push folder "render-site" ni ke satu repo GitHub
   (atau push seluruh projek; nanti set publish directory)

2. Render Dashboard -> New +  ->  Static Site

3. Connect repo GitHub anda

4. Setting:
     - Build Command    : (KOSONGKAN - tak perlu build)
     - Publish Directory : render-site
       (kalau repo anda ADALAH folder render-site, guna: . )

5. Create Static Site -> siap!
   Render bagi subdomain *.onrender.com PERCUMA + SSL percuma.

----------------------------------------------------------------
 CUSTOM DOMAIN (pilihan)
----------------------------------------------------------------
Render -> Settings -> Custom Domains -> tambah:
     pixyophoto.com  atau  wedding.pixyophoto.com
Render benarkan domain + subdomain TANPA caj tambahan.
Anda cuma bayar pada pendaftar domain (cth Namecheap/Exabytes).
SSL auto-provision (Let's Encrypt) percuma.

----------------------------------------------------------------
 GAMBAR
----------------------------------------------------------------
Di Render, gambar dalam folder images/ terus berfungsi
(tak perlu host di tempat lain macam Blogger).
Letak fail baru dalam render-site/images/ :
     produk-utama.jpg  (sudah ada)
     galeri-1.jpg / galeri-2.jpg / galeri-3.jpg  (galeri auto-muncul)
Rujuk dalam HTML guna path: /images/namafail.jpg

----------------------------------------------------------------
 NOMBOR WHATSAPP
----------------------------------------------------------------
Sudah diset: 60199572015 (semua butang)

================================================================
