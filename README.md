# IMAJINASIKU🤖 🧠 

[![Downloads](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1rOvQNs0Cmn_yU1bKWjCOHzGVDgZkaTtO?usp=sharing)
[![Unduhan] (https://pepy.teknologi / lencana / imajinasi)] https://pepy.teknologi / proyek / imaginairy)
[! [gambar] (https://img.shields.io/pypi/v/imaginairy.svg)] (https://pypi.org/project/imaginairy/)
[![image](https://img.shields.io/badge/license-MIT-green)](https://github.com/brycedrennan/imaginAIry/blob/master/LICENSE/)
[! [Perselisihan] (https://flat.badgen.net/discord/members/FdD7ut3YjW)] (https://discord.gg/FdD7ut3YjW)

AI membayangkan gambar. Generasi Pythonic dari gambar difusi stabil** dan video***!.

"hanya berfungsi" di Linux dan macOS (M1) (dan terkadang windows).


"'bash
# di macOS, pastikan rust diinstal terlebih dahulu
# pastikan untuk menggunakan Python 3.10, Python 3.11 saat ini tidak didukung
> > pip install imaginairy
> > bayangkan "pemandangan yang indah" "foto seekor anjing" "foto mangkuk buah" "foto potret seorang wanita berbintik-bintik" "sebuah bluejay"
# Buat video AI
> > videogen aimg --roket gambar awal.png
```
## Difusi Video yang Stabil
<p float= "kiri">
<img src= " dokumen / aset / svd-roket.gif "tinggi= "190">
<img src= " dokumen / aset / svd-athena.gif "tinggi= "190">
<img src= " dokumen / aset/svd-gadis mutiara.gif "tinggi= "190">
<img src= " dokumen / aset/svd-malam berbintang.gif "tinggi= "190">
<img src= " dokumen / aset/svd-anjing.gif "tinggi= "190">
<img src= " dokumen / aset / svd-xpbliss.gif "tinggi= "190">
< / p>

### Rilis Video Difusi Stabil yang terburu-buru!
Bekerja dengan GPU Nvidia.  Tidak berfungsi di Mac atau CPU.

Di Windows, Anda harus menginstal torch 2.0 terlebih dahulu melalui https://pytorch.org/get-started/locally/
"'teks
Penggunaan: videogen aimg [OPSI]

  AI menghasilkan video dari sebuah gambar

  Contoh:

      videogen aimg --aset gambar awal / seluruh roket.png

Opsi:
  -- mulai-jalur Input TEKS gambar untuk file gambar.
  -- num-frames Bilangan bulat Jumlah bingkai.
  -- num-langkah Bilangan BULAT Jumlah langkah.
  -- model Model TEKS untuk digunakan. Salah satu dari: svd, svd_xt, svd_image_decoder, svd_xt_image_decoder
  -- fps INTEGER FPS untuk ditargetkan AI saat membuat video
  -- keluaran-fps FPS BILANGAN BULAT untuk video keluaran
  -- gerak-jumlah BILANGAN BULAT Berapa banyak gerakan yang dihasilkan. nilai antara 0 dan 255.
  - r, --mengulang BILANGAN BULAT Berapa kali mengulang render.   [bawaan: 1]
  -- augmentasi Bersyarat FLOAT cond-aug.
  -- seed INTEGER Seed untuk generator bilangan acak.
  -- decoding_t Bilangan BULAT Jumlah bingkai yang didekodekan dalam satu waktu.
  -- folder Keluaran Teks output_folder.
  -- bantu Tampilkan pesan ini dan keluar.
```

### Gambar
<p float= "kiri">
<img src= " dokumen / aset/026882_1_ddim50_PS7. 5_a_scenic_landscape_ [dihasilkan].jpg "tinggi= "256">
<img src= " dokumen / aset/026884_1_ddim50_PS7. 5_photo_of_a_dog_[dihasilkan].jpg "tinggi= "256">
<img src= " dokumen / aset/026890_1_ddim50_PS7. 5_photo_of_a_bowl_of_fruit._masih hidup_[dihasilkan].jpg "tinggi= "256">
<img src= " dokumen / aset/026885_1_ddim50_PS7. 5_girl_with_a_pearl_earring_ [dihasilkan].jpg "tinggi= "256">
<img src= " dokumen / aset/026891_1_ddim50_PS7. 5_close-up_photo_of_a_bluejay_[dihasilkan].jpg "tinggi= "256">
<img src= " dokumen / aset/026893_1_ddim50_PS7. 5_macro_photo_of_a_flower_[dihasilkan].jpg "tinggi= "256">
< / p>

### Apa yang Baru
[Lihat Log Perubahan lengkap di sini] (. / docs / changelog.md)


**14.3.0**
- fitur: mengintegrasikan [spandrel] (https://github.com/chaiNNer-org/spandrel) untuk peningkatan skala 
- perbaiki: izinkan memuat model sdxl dari jalur lokal. 

**14.2.0**
- feature fitur: tambahkan dukungan prompt gambar melalui '--image-prompt` dan ' --image-prompt-strength`

**14.1.1**
- tes: tambahkan tes instalasi untuk windows, mac, dan conda
- perbaiki: masalah ketergantungan

**14.1.0**
- feature fitur: membuat pembuatan video menjadi lancar dengan menambahkan interpolasi bingkai
- fitur: Bobot SDXL dalam format compvis sekarang dapat digunakan
- fitur: memungkinkan pembuatan video dalam berbagai ukuran yang ditentukan oleh pengguna
- fitur: keluaran generasi video dalam format" bouncing"
- fitur: pilih format keluaran video: mp4, webp, atau gif
- fitur: perbaiki penanganan benih acak dalam pembuatan video
- dokumen: terbitkan dokumen secara otomatis saat didorong ke master
- build: hapus ketergantungan imageio
- build: vendorize facexlib sehingga kami tidak menginstal dependensinya yang tidak diperlukan


**14.0.4**
- docs: tambahkan situs web dokumentasi di https://brycedrennan.github.io/imaginAIry/
- build: hapus ketergantungan fairscale
- perbaiki: pembuatan video rusak

**14.0.3**
- perbaiki: beberapa bug kritis dengan paket
- tes: tambahkan tes asap roda untuk mendeteksi masalah ini di masa mendatang

**14.0.0**
- generation pembuatan video menggunakan [Difusi Video Stabil] (https://github.com/Stability-AI/generative-models)
  - tambahkan ' --videogen` ke pembuatan gambar apa pun untuk membuat video pendek dari gambar yang dihasilkan
  - atau gunakan 'aimg videogen' untuk membuat video dari sebuah gambar
- Model SD SDXL (Stable Diffusion Extra Large) sekarang didukung.
  - coba '--model opendalle 'atau' --model sdxl`
  - inpainting dan controlnets belum didukung untuk SDXL
- imagin imaginairy sekarang didukung oleh [perpustakaan penyuling] (https://github.com/finegrain-ai/refiners)
  - Ini adalah penulisan ulang yang sangat besar, itulah sebabnya beberapa fitur belum didukung.  Di sisi positifnya, penyuling mendukung
fitur canggih (SDXL, image prompt, dll) yang akan segera ditambahkan ke imaginairy.
  - [panduan perhatian diri](https://github.com/SusungHong/Self-Attention-Guidance) yang membuat detail gambar lebih akurat
- feature fitur: generasi gambar yang lebih besar sekarang bekerja JAUH lebih baik dan tetap setia pada gambar yang sama seperti yang terlihat pada ukuran yang lebih kecil. 
Misalnya '--size 720p --seed 1 ' dan '--size 1080p --seed 1 ' akan menghasilkan gambar yang sama untuk SD15
- feature fitur: memuat model berbasis diffusers sekarang didukung. Contoh ' --model https://huggingface.co/ainz/diseny-pixar --model-arsitektur sd15`
- feature fitur: qrcode controlnet!


### Jalankan server API dan antarmuka web StableStudio (alfa)
Hasilkan gambar melalui API atau antarmuka web.  Fitur yang jauh lebih kecilset dibandingkan dengan alat baris perintah.
"'bash
> > aimg server
```
Kunjungi http://localhost:8000 / dan http://localhost:8000/docs

< img src="https://github.com/Stability-AI/StableStudio/blob/a65d4877ad7d309627808a169818f1add8c278ae/misc/GenerateScreenshot.png?raw=true" lebar= "512">

### Kontrol Struktur Gambar [oleh ControlNet] (https://github.com/lllyasviel/ControlNet)
#### (Belum didukung untuk SDXL)
Hasilkan gambar yang dipandu oleh pose tubuh, peta kedalaman, tepi cerdik, batas hed, atau peta normal.

** Kontrol Openpose**

"'bash
bayangkan -- kontrol-aset gambar / indiana.jpg --mode kontrol openpose --teks keterangan openpose "foto beruang kutub"
```

<p float= "kiri">
    <img src= " dokumen / aset / indiana.jpg "tinggi= "256">
    <img src= " dokumen / aset / pose indiana.jpg "tinggi= "256">
    <img src= " dokumen / aset / indiana-pose-beruang kutub.jpg "tinggi= "256">
< / p>

#### Kontrol Tepi yang Cerdik

"'bash
bayangkan --control-image assets / lena.png --control-mode canny "foto seorang wanita bertopi melihat ke kamera"
```

<p float= "kiri">
    <img src= " dokumen / aset / lena.png "tinggi= "256">
    <img src= " dokumen / aset / lena-cerdik.jpg "tinggi= "256">
    <img src= " dokumen / aset / lena-canny-generated.jpg "tinggi= "256">
< / p>

### Kontrol Batas # HED

"'bash
bayangkan -- anjing gambar kontrol.jpg --mode kontrol menampilkan "foto dalmasi"
```

<p float= "kiri">
    <img src= " dokumen / aset/000032_337692011_PLMS40_PS7. 5_a_photo_of_a_dog.jpg "tinggi= "256">
    <img src= " dokumen / aset / dog-hed-boundary.jpg "tinggi= "256">
    <img src= " dokumen / aset / dog-hed-boundary-dalmation.jpg "tinggi= "256">
< / p>

#### Kontrol Peta Kedalaman

"'bash
bayangkan -- hidup mewah gambar kontrol.jpg --kedalaman mode kontrol "ruang tamu modern"
```

<p float= "kiri">
    <img src= " dokumen / aset/kehidupan mewah.jpg "tinggi= "256">
    <img src= " docs / assets / fancy-living-depth.jpg "tinggi= "256">
    <img src= " dokumen / aset / fancy-living-dibuat secara mendalam.jpg "tinggi= "256">
< / p>

#### Kontrol Peta Normal

"'bash
bayangkan -- burung gambar kontrol.jpg --mode kontrol normal "seekor burung"
```

<p float= "kiri">
    <img src= " dokumen / aset/013986_1_kdpmpp2m59_PS7. 5_a_bluejay_ [dihasilkan].jpg "tinggi= "256">
    <img src= " dokumen / aset / burung-normal.jpg "tinggi= "256">
    <img src= " dokumen / aset / burung-dibuat secara normal.jpg "tinggi= "256">
< / p>

#### Kontrol Pengocokan Gambar

Menghasilkan gambar berdasarkan elemen gambar kontrol. Agak mirip dengan transfer gaya.
"'bash
bayangkan -- gadis mutiara gambar kontrol.jpg --mode kontrol acak "badut"
```
Gambar tengah adalah gambar masukan yang "dikocok" 
<p float= "kiri">
    <img src= " dokumen / aset/girl_with_a_pearl_earring.jpg "tinggi= "256">
    <img src= " dokumen / aset/pearl_shuffle_019331_1_kdpmpp2m15_PS7. 5_img2img-0. 0_a_clown.jpg "tinggi= "256">
    <img src= " dokumen / aset/pearl_shuffle_clown_019331_1_kdpmpp2m15_PS7. 5_img2img-0. 0_a_clown.jpg "tinggi= "256">
< / p>

#### Kontrol Instruksi Pengeditan

Mirip dengan instructPix2Pix (di bawah) tetapi berfungsi dengan model berbasis SD 1.5 apa pun.
"'bash
bayangkan -- gadis mutiara gambar kontrol.jpg -- edit mode kontrol --init-image-strength 0.01 --langkah 30 --negative-prompt ""--model openjourney-v2 "jadikan itu anime" "buat di pantai" 
```

<p float= "kiri">
    <img src= " dokumen / aset/girl_with_a_pearl_earring.jpg "tinggi= "256">
    <img src= " dokumen / aset/pearl_anime_019537_521829407_kdpmpp2m30_PS9. 0_img2img-0. 01_make_it_anime.jpg "tinggi= "256">
    <img src= " dokumen / aset/pearl_beach_019561_862735879_kdpmpp2m30_PS7. 0_img2img-0. 01_make_it_at_the_beach.jpg "tinggi= "256">
< / p>

#### Tambahkan Kontrol Detail (peningkatan skala / resolusi super)

Mengganti detail yang ada dalam gambar. Bagus untuk digunakan dengan --init-image-strength 0.2
"'bash
bayangkan -- control-image "aset / tulang harapan.jpg " --detail mode kontrol "fokus tajam, resolusi tinggi" --init-image-strength 0.2 --langkah 30-w 2048-h 2048 
```

<p float= "kiri">
    <img src= " dokumen / aset/wishbone_headshot_badscale.jpg "tinggi= "256">
    <img src= " dokumen / aset/wishbone_headshot_details.jpg "tinggi= "256">
< / p>


### Pewarnaan Gambar (ulang) (menggunakan kontrol kecerahan)
Warnai gambar hitam putih atau warnai ulang gambar yang ada.

