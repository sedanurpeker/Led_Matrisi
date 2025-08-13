# 5x8 LED Sistemi ile Harf Yazdırma

Bu proje, **8085 mikroişlemcisi** tabanlı bir mikrobilgisayar deney seti kullanılarak 5x8’lik LED matris üzerinde harf yazdırmayı amaçlamaktadır.  
Donanım ve yazılım entegrasyonu sayesinde seçilen karakterler LED’lerde net bir şekilde görüntülenmektedir.

## Projenin Amacı
- 8085 mikroişlemcisini kullanarak temel giriş/çıkış kontrolünü öğrenmek
- 74HC238 **3-to-8 line decoder/demultiplexer** ile satır seçimi yapmak
- 74LS373 **octal latch** ile LED verilerini sabit tutmak
- 8085 makine dili ile donanım kontrollü bir karakter gösterim sistemi kurmak

## Kullanılan Donanımlar
- **8085 Mikroişlemci**
- **74HC238 Demultiplexer**
- **74LS373 Latch**
- **5x8 LED Matris**
- Bağlantı kabloları

## Çalışma Mantığı
1. **Satır Seçimi:** 3 bitlik veri, demultiplexer üzerinden ilgili satırın seçilmesini sağlar.
2. **Veri Gönderimi:** 7 bitlik sütun verisi, seçili satıra gönderilir.
3. **Latch Kullanımı:** Veriler latch üzerinden saklanarak LED’lerin sürekli yanması sağlanır.
4. **8085 Makine Kodları:** Her satır ve sütun için gerekli bit kombinasyonları 8085 makine dili ile yazılır.

## Kod Örneği
```asm
; Satır 1 için
mvi A, 01       ; Satır 1'i seç
out 30
mvi A, 7F       ; Sütun verisi
out 30
mvi A, FF       ; Latch kontrolü
out 30
call 004C       ; Gecikme
```

## Öne Çıkan Özellikler
- Donanım ve yazılımın birlikte çalıştığı bir mikroişlemci projesi
- Temel mantık devreleri (decoder, latch) ile veri akışı yönetimi
- Harflerin LED matris üzerinde düzgün gösterimi
