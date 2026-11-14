# NOCCA DYNAMIC — rilis

Repo ini hanya menampung installer dan feed pembaruan otomatis untuk NOCCA DYNAMIC.
Kode aplikasinya tidak ada di sini.

## Cara aplikasi memperbarui diri

Aplikasi membaca feed statis:

```
https://github.com/atrijuniawan/nocca-dynamic-releases/releases/latest/download/latest.json
```

Isi feed menunjuk installer di folder rilis yang sama, beserta sha256 dan catatan
rilis. Panel **Pengaturan → Tentang** menawarkan unduhan, memverifikasi sha256,
lalu memasangnya dan memulai ulang aplikasi.

## Rilis baru

1. `NOCCA_UPDATE_BASE=https://github.com/atrijuniawan/nocca-dynamic-releases/releases/latest/download`
2. `npm run dist:win:unsafe` (atau `npm run release` dengan sertifikat)
3. `gh release create vX.Y.Z --repo atrijuniawan/nocca-dynamic-releases --notes-file release-notes.md "release/NOCCA DYNAMIC Setup X.Y.Z.exe" release/latest.json`
