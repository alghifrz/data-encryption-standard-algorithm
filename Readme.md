# Kuis 3 Kriptografi dan Keamanan Siber
## Alghifari Rasyid Zola (105222006)

# 🔐 DES Encryption in Python

Implementasi algoritma **Data Encryption Standard (DES)** menggunakan bahasa pemrograman **Python**, sebagai bagian dari kuis 3 mata kuliah Kriptografi dan Keamanan Siber.

---

## 📌 Deskripsi

Program ini mengenkripsi teks 64-bit (8 karakter) menggunakan algoritma kriptografi simetris **DES**. Algoritma ini bekerja dengan 16 ronde dan menerapkan proses **Initial Permutation**, **Feistel Function**, **S-Box Substitution**, dan **Final Permutation**.

---

## 🧪 Contoh Penggunaan

```python
plaintext = "computer"
key = "12345678"

ciphertext = des_encrypt(plaintext, key)
print("Hasil Enkripsi (HEX):", bytes_to_hex(ciphertext))
print("Hasil Enkripsi (BIN):", bytes_to_bin(ciphertext))
print("Hasil Enkripsi (Base64):", bytes_to_base64(ciphertext))
```	
Output:
```python
Hasil Enkripsi (HEX): 3036a53c609d04a3
Hasil Enkripsi (BIN): 00110000 00110110 10100101 00111100 01100000 10011101 00000100 10100011
Hasil Enkripsi (Base64): MDbCpTxgwp0EwqM=
```

## ⚙️ Struktur Proyek
- `des_encrypt()`: Fungsi utama untuk enkripsi plaintext.
- `generate_keys()`: Membentuk 16 subkey dari key utama.
- `feistel()`: Fungsi Feistel untuk setiap ronde.
- `sbox_substitution()`: Substitusi menggunakan S-box.
- `permute()`, `text_to_bits()`, `xor()`, dll: Fungsi pembantu untuk manipulasi bit.
