# Hafta 3 — Linux, Ağ Trafiği Analizi, Nmap ve Metasploit

Bu hafta en çok pratik yaptığım ve en çok keyif aldığım haftaydı. Gerçek araçlarla sızma testi adımlarını deneyimledim.

## 📖 Öğrendiğim Konular

### Linux Temelleri
- Dosya sistemi hiyerarşisi (`/`, `/home`, `/etc`, `/root`), yollar (mutlak/göreli).
- Temel komutlar: `ls`, `cd`, `pwd`, `cat`, `grep`, `find`, `chmod`, `whoami`, `hostname`, `id`.
- Dosya izinleri (okuma/yazma/çalıştırma, `rwx`), gizli dosyalar (`.` ile başlar, `ls -la`).
- Kali Linux: pentester'lar için Debian tabanlı, araçları hazır gelen dağıtım.

### Ağ Trafiği Analizi (Wireshark / tcpdump)
- Paketleri yakalama ve inceleme; **Follow TCP Stream**, **Export Objects**.
- Şifresiz protokollerin (FTP, Telnet, HTTP, SMTP) kullanıcı adı/parolayı **açık metin** taşıdığını görme.
- Filtreleme: `http`, `tcp.port == 80`, `ip.addr == ...`, `contains`.
- `tshark` / `tcpdump` ile komut satırından analiz.

### Nmap ile Ağ Tarama
- Host keşfi ve port tarama mantığı.
- Önemli parametreler:
  - `-sV` → servis/versiyon tespiti
  - `-p-` → tüm portları (1–65535) tara
  - `-T4` → hız şablonu
  - `--top-ports` → en sık kullanılan portları tara
- Açık portlardan çalışan servisleri ve versiyonları belirleme.

### Metasploit Framework
- Modül türleri: **Exploit** (zafiyet istismarı), **Payload** (sonra çalışan kod), **Auxiliary** (tarama/destek), **Meterpreter** (gelişmiş, RAM'de çalışan payload).
- **Bind shell** (hedef port açar) vs **Reverse shell** (hedef saldırgana geri bağlanır).
- Temel akış: `search` → `use` → `set RHOSTS/LHOST` → `check` → `exploit`.
- Önemli ayarlar: **RHOSTS** = hedef IP, **LHOST** = kendi IP'in (reverse bağlantı için), **LPORT**.
- Meterpreter komutları: `getuid`, `sysinfo`, `shell`, `download/upload`.
- `msfvenom` ile payload üretme.

## 🧪 Pratik — Alıştırmalar
- **Wireshark lab'ları:** çeşitli protokollerde trafik analizi, şifresiz verinin riskleri.
- **Nmap taraması:** gerçek bir hedefi tarayıp servis/versiyonlarını çıkarma.
- **Metasploit:** bilinen bir web servisi zafiyetini (RCE) istismar edip oturum alma.
- **Arrow (Telnet istismarı):** açık Telnet servisini bulma → varsayılan/zayıf parolayla giriş → temel keşif.

> *Not: Lab cevapları/flag'leri gizlilik gereği burada paylaşılmıyor — sadece adımlar ve öğrenilen kavramlar anlatılıyor.*

## 💡 Bu Hafta Aklımda Kalan
- **Reverse shell** mantığı: hedef güvenlik duvarı gelen bağlantıyı engellese bile, hedef *bize* bağlandığı için çalışır — bu yüzden `LHOST` = **kendi IP'in**.
- Varsayılan parolalar (`root:root`, `admin:admin`) hâlâ en büyük zafiyetlerden biri.
- `nmap -sV` küçük harf — büyük `-Sv` hata verir (detaylara dikkat!).
- Telnet şifresiz olduğu için modern sistemlerde yerini SSH'a bırakmalı.

## ✅ Durum
Hafta 3 görevleri tamamlandı. Üç haftanın tüm görevleri bitti. 🎉
