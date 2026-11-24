# Hafta 2 — Ağ, Web, LLM Güvenliği, OSINT ve Kriptoloji

## 📖 Öğrendiğim Konular

### Ağ Temelleri
- **OSI** ve **TCP/IP** katman modelleri; verinin katmanlar arası yolculuğu.
- **IP adresi, port, protokol** kavramları; TCP vs UDP farkı.
- Temel protokoller: HTTP/HTTPS, DNS, FTP, SSH, Telnet.

### Web Temelleri
- İstemci–sunucu mimarisi, HTTP istek/yanıt döngüsü.
- HTTP metotları (GET, POST...), durum kodları (200, 404, 500...).
- Temel web zafiyet mantığına giriş (girdi doğrulamanın önemi).

### LLM Güvenliği
- Büyük dil modellerine (LLM) özgü riskler: **prompt injection**, veri sızıntısı, güvenilmeyen çıktı.
- Kullanıcı girdisinin asla doğrudan güvenilir komut gibi işlenmemesi gerektiği.

### OSINT (Açık Kaynak İstihbaratı)
- Herkese açık kaynaklardan (web, sosyal medya, kayıtlar) bilgi toplama.
- Keşif aşamasında hedef hakkında ayak izi (footprint) çıkarma.
- Etik sınır: sadece halka açık ve izinli bilgiler.

### Kriptoloji
- **Encoding vs Encryption vs Hashing** farkı:
  - *Encoding* (base64, base32): geri döndürülebilir, gizlilik sağlamaz.
  - *Encryption*: anahtarla şifreleme, geri döndürülebilir.
  - *Hashing* (MD5, SHA): tek yönlü, geri döndürülemez (parola saklama, bütünlük).
- Zayıf/eski algoritmaların (MD5, SHA1) neden riskli olduğu.

## 🧪 Pratik — Laboratuvarlar
- **Encoding çözme:** base64/base32/binary metinleri çözme pratiği.
- **Hash kırma:** zayıf hash'lerin sözlük/rainbow table ile nasıl çözülebildiğini görme (parolaların neden güçlü olması gerektiğini anlama).

> *Not: Lab cevapları/flag'leri gizlilik gereği burada paylaşılmıyor — sadece yöntem anlatılıyor.*

## 💡 Bu Hafta Aklımda Kalan
- "Encode edilmiş" bir şey **şifrelenmiş değildir** — base64 gizlilik sağlamaz!
- Zayıf parolalar saniyeler içinde kırılabiliyor; güçlü parola + güçlü hash şart.

## ✅ Durum
Hafta 2 görevleri tamamlandı.
