# PixelGuard: Akıllı Güvenlik Sistemi 🛡️

PixelGuard, Arduino platformu üzerinde geliştirilmiş, şifre tabanlı bir güvenlik kontrol sistemidir. Bu proje, fiziksel güvenliği dijital bir arayüzle birleştirerek yetkisiz erişimleri engellemeyi amaçlar.

## 🚀 Proje Hakkında
Sistem, kullanıcının 4x4 Keypad üzerinden girdiği şifreyi doğrular. Doğru şifre girildiğinde erişim izni verirken, hatalı girişlerde görsel ve işitsel uyarılar oluşturur. Veriler I2C protokolü üzerinden LCD ekrana aktarılarak düşük kablo karmaşası ve yüksek verimlilik hedeflenmiştir.

## 🛠️ Kullanılan Donanım Bileşenleri
Projede kullanılan temel donanım bileşenleri şunlardır:
* **Kontrolcü:** DCcEle DCcduino Uno (Arduino Uno uyumlu)
* **Ekran:** QC1602A LCD Ekran (I2C Haberleşme Modüllü)
* **Giriş Birimi:** 4x4 Membran Tuş Takımı (Keypad)
* **Geri Bildirim:** Buzzer ve LED göstergeler

## 💡 Öne Çıkan Özellikler
* **Şifreli Erişim:** Güvenli giriş için özelleştirilebilir şifre yapısı.
* **I2C Entegrasyonu:** LCD ekran bağlantısı için sadece 2 pin (SDA, SCL) kullanılarak donanım tasarımı optimize edilmiştir.
* **Görsel Geri Bildirim:** QC1602A ekran üzerinde kullanıcıya anlık durum mesajları (Şifre Girin, Erişim İzni Verildi, Hatalı Şifre vb.) gösterilir.
* **Hata Yönetimi:** Üst üste hatalı denemelerde sistemin uyarı vermesi sağlanmıştır.

## 📂 Kurulum ve Kullanım
1.  **Donanım Bağlantısı:** Keypad ve LCD ekranı şemaya uygun şekilde Arduino'ya bağlayın (LCD için SDA -> A4, SCL -> A5).
2.  **Kütüphaneler:** Arduino IDE üzerinden `Keypad` ve `LiquidCrystal_I2C` kütüphanelerini kurun.
3.  **Yükleme:** `pixelguard.ino` dosyasını Arduino IDE ile açın ve karta yükleyin.
4.  **Başlatma:** Seri port üzerinden veya LCD ekrandan yönergeleri takip ederek sistemi kullanmaya başlayın.
