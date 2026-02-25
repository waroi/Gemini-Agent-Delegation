# Çoklu Ajan Sistemi Kullanım Kılavuzu

Bu çalışma alanı, Gemini CLI'ı tam teşekküllü bir mühendislik ekibine dönüştüren **Çoklu Ajan Sistemi (MAS-7)** ile donatılmıştır.

## 🚀 Hızlı Başlangıç
`N` adet ajandan oluşan bir ekibi etkinleştirmek için isteminizin (prompt) sonuna `xN` eklemeniz yeterlidir.

| Tetikleyici | Ekip Yapısı | En İyi Kullanım Alanı |
| :--- | :--- | :--- |
| **x2** | **1 Lider + 1 Geliştirici** | Hata düzeltmeleri, küçük scriptler. |
| **x4** | **1 Lider + 1 Geliştirici + 1 Analist + 1 Tasarımcı** | Yeni özellikler, UI bileşenleri. |
| **x7** | **Tam Kadro** (Lider, 2 Dev, 2 Analist, 1 Tasarımcı, 1 QA) | **Karmaşık Projeler**, Üretim Hazır Kod. |
| **xGame** | **Oyun Geliştirme Ekibi** (Mimar, Gameplay, Sanat, Proje, Pazarlama) | **Oyun Projeleri**, Prototipleme, Yayın Stratejisi. |
| **x10+** | **Ölçeklenmiş Kadro** | Çok büyük sistemler (Ekstra ajanlar Dev/Analist olarak dağıtılır). |

---

## 👥 Ekip Rolleri (x7 Konfigürasyonu)

`x7` tetiklendiğinde aşağıdaki ajanlar paralel olarak çalışır:

### 1. 👑 Takım Lideri (Mimar)
- **Rol:** Orkestratör & Proje Yöneticisi.
- **Sorumluluk:** Görevleri dağıtır ve nihai cevabı sentezler.

### 2. ⚡ Kıdemli Geliştiriciler (x2)
- **Rol:** Kıdemli Yazılım Mühendisleri.
- **Sorumluluk:** Çekirdek mantık, veritabanı, %100 tip güvenliği.

### 3. 🔍 Sistem Analistleri (x2)
- **Rol:** Gereksinim & Güvenlik Uzmanları.
- **Sorumluluk:** İş mantığı doğrulama, uç durum (edge case) analizi.

### 4. 🎨 Yaratıcı Tasarımcı (x1)
- **Rol:** UI/UX Uzmanı.
- **Sorumluluk:** Görsel dil, kullanıcı akışları, erişilebilirlik.

### 5. 🛡️ QA Mühendisi (x1)
- **Rol:** Test Uzmanı (SDET).
- **Sorumluluk:** Test stratejisi, hata avcılığı, kod kalitesi onayı.

---

## 🎮 Oyun Geliştirme Ekibi (xGame Konfigürasyonu)

`xGame` tetiklendiğinde aşağıdaki özelleşmiş ajanlar devreye girer:

### 1. 🏗️ Oyun Mimarı (Lider)
- **Rol:** Teknik Vizyoner.
- **Sorumluluk:** Motor seçimi (Unity/Unreal), sistem mimarisi.

### 2. 🎮 Gameplay Geliştirici
- **Rol:** Mekanik Mühendisi.
- **Sorumluluk:** Oynanış kodları (C#/C++), Blueprint sistemleri.

### 3. 🎨 Sanat Direktörü
- **Rol:** Görsel Lider.
- **Sorumluluk:** Sanat stili, UX/UI tasarımı, varlık yönetimi.

### 4. 📅 Proje Yöneticisi
- **Rol:** Üretim Koordinatörü.
- **Sorumluluk:** Agile sprint planlama, GDD (Game Design Doc) güncelleme.

### 5. 📢 Pazarlama Uzmanı
- **Rol:** Topluluk Yöneticisi.
- **Sorumluluk:** Mağaza optimizasyonu (ASO), lansman stratejisi.

---

## 📈 Ölçeklenebilirlik Kuralı (xN > 7)
Eğer `x7`'den daha büyük bir sayı (örn. `x10`) girerseniz, sistem otomatik olarak **Geliştirici** ve **Analist** sayısını artırarak ekibi genişletir.
Örneğin `x9` = x7 Kadrosu + 1 Dev + 1 Analist.

## 🛠️ İş Akışı
1.  **İstek:** *"Redis panelini oluştur. x7"*
2.  **Yuvarlak Masa:** Lider, Analist ve QA planı tartışır.
3.  **Uygulama:** Geliştiriciler kodlar, QA test yazar.
4.  **Teslimat:** Lider sonucu sunar.
