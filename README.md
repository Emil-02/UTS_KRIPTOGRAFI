# 🔐 UTS Kriptografi — Enkripsi File AES

Program **enkripsi & dekripsi file** menggunakan **AES mode EAX**
(*authenticated encryption*) dengan kunci yang diturunkan dari password.

## ⚙️ Cara Kerja

1. Password → SHA-256 → kunci AES 256-bit
2. File dienkripsi dengan AES-EAX; hasilnya disimpan sebagai `nonce + tag + ciphertext`
3. Saat dekripsi, *tag* diverifikasi — password salah atau file yang telah
   dimodifikasi akan langsung terdeteksi dan dekripsi digagalkan

## 🚀 Cara Menjalankan

```bash
pip install pycryptodome
python "UTS Ibu Desi/Kriptografi/UtsKriptografi.py"
```

Program akan meminta nama file yang ingin dienkripsi beserta password-nya,
lalu mendemonstrasikan proses dekripsi dengan verifikasi password.

## 📁 Contoh File

| File | Keterangan |
| --- | --- |
| `UtsEmil.txt` | File asli (plaintext) |
| `UtsEmil_Enkripsi` | Hasil enkripsi (nonce + tag + ciphertext) |
| `UtsEmil_Dekripsi.txt` | Hasil dekripsi kembali |
