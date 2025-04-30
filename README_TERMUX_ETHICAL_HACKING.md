
# Termux untuk Keamanan Siber (Etical Hacking Dasar)

Belajar dasar-dasar ethical hacking menggunakan Termux langsung dari perangkat Android. Semua langkah di sini ditujukan untuk pembelajaran dan uji coba sistem milik sendiri secara legal.

## 1. Persiapan Awal
### Instalasi Dasar
```bash
pkg update && pkg upgrade
pkg install git python curl wget
pkg install tsu nano
```

### Instalasi `x11-repo` untuk dukungan GUI tools:
```bash
pkg install x11-repo
```

---

## 2. Tools Penting

### **1. Nmap (Network Mapper)**
Digunakan untuk memetakan jaringan dan memindai port terbuka.
```bash
pkg install nmap
nmap -v scanme.nmap.org
```

### **2. Hydra**
Untuk pengujian brute-force login (misal: FTP, SSH, dll) – hanya untuk sistem milik sendiri.
```bash
pkg install hydra
hydra -l admin -P wordlist.txt ftp://192.168.1.1
```

### **3. sqlmap**
Untuk mendeteksi celah SQL Injection.
```bash
pkg install sqlmap
sqlmap -u "http://target.com/page.php?id=1" --batch
```

### **4. Nikto**
Scanner untuk mencari kerentanan pada web server.
```bash
git clone https://github.com/sullo/nikto
cd nikto/program
pkg install perl
perl nikto.pl -h http://targetsite.com
```

---

## 3. Wordlists

Untuk pengujian password, kamu bisa gunakan wordlist dari `SecLists`:
```bash
git clone https://github.com/danielmiessler/SecLists
```

---

## 4. Tools Tambahan

### **Metasploit Framework** (berat, opsional)
```bash
pkg install unstable-repo
pkg install metasploit
```

---

## 5. Legal Disclaimer
> Semua tutorial ini hanya untuk **pembelajaran pribadi** dan **pengujian sistem milik sendiri**. Jangan digunakan untuk tindakan ilegal!

---

## 6. Kontak
Tutor oleh: d3wali  
Email: d3wali@yahoo.com  
GitHub: [https://github.com/d3wali](https://github.com/d3wali)
