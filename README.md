# 5x8 LED Sistemi ile Harf Yazdırma (8085 Mikroişlemci)

Bu proje, **Mikroişlemciler** dersi kapsamında 8085 mikroişlemci kullanarak 5x8 LED matris üzerinde harf yazdırma uygulamasını içerir.  
Satır seçimi ve veri saklama işlemleri **74HC238** ve **74LS373** entegreleri ile yapılmıştır.

## 📌 Proje Amacı
- 8085 mikroişlemcisi ile LED matris üzerinde veri gösterimi yapmak
- Donanım devre elemanlarını (decoder, latch) kullanarak satır seçimi ve veri saklama mantığını uygulamak
- LED matris üzerinde isim veya karakterlerin gösterimini sağlamak

## ⚙️ Kullanılan Donanım
- 8085 Mikroişlemci Deney Seti
- 5x8 LED Matris
- **74HC238** (3-to-8 Decoder/Demultiplexer)
- **74LS373** (Octal Transparent Latch)
- Bağlantı kabloları, breadboard vb.

## 🔍 Çalışma Mantığı
1. **Satır Seçimi**: 74HC238 decoder ile 3 bitlik giriş verisi kullanılarak 8 farklı satırdan biri seçilir.
2. **Veri Saklama**: 74LS373 latch entegresi ile seçilen satırdaki sütun bilgisi saklanır.
3. **Veri Gönderimi**: 8085 mikroişlemcisi ile sütun verileri LED matrisine aktarılır.
4. **Görüntüleme**: Latch sayesinde LED’ler sabit yanar ve istenilen karakter oluşturulur.

## 💡 Örnek Uygulama
Proje kapsamında LED matris üzerinde **"SEDANUR"** kelimesi gösterilmiştir.  
Her harf, ilgili satır ve sütun kombinasyonları ile ayrı ayrı oluşturulmuştur.

## 📂 Dosya İçeriği
- `proje_kodu.asm` → 8085 assembly dilinde yazılmış proje kodu
- `devre_şeması.png` → Donanım bağlantı şeması
- `readme.md` → Proje bilgileri ve çalışma mantığı

## 🚀 Çalıştırma
1. Donanımı bağlantı şemasına göre kurun.
2. 8085 mikroişlemci deney setine proje kodunu yükleyin.
3. Programı çalıştırarak LED matris üzerinde harflerin sırasıyla gösterilmesini izleyin.

## 📜 Lisans
Bu proje, eğitim amaçlı olarak geliştirilmiştir. Serbestçe kullanılabilir ve geliştirilebilir.
