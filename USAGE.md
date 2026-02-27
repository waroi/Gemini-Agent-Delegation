# Çoklu Ajan Sistemi Kullanım Kılavuzu

Bu çalışma alanı, Gemini CLI'ı tam teşekküllü bir mühendislik ekibine dönüştüren **Çoklu Ajan Sistemi (MAS-7)** ile donatılmıştır.

## 🚀 Hızlı Başlangıç
`N` adet ajandan oluşan bir ekibi etkinleştirmek için isteminizin (prompt) sonuna `xN` eklemeniz yeterlidir.

| Tetikleyici | Ekip Yapısı | En İyi Kullanım Alanı |
| :--- | :--- | :--- |
| **x2** | **1 Lider + 1 Geliştirici** | Hata düzeltmeleri, küçük scriptler. |
| **x4** | **1 Lider + 1 Geliştirici + 1 Analist + 1 Tasarımcı** | Yeni özellikler, UI bileşenleri. |
| **x7** | **Standart Ürün Ekibi** (Lider, 2 Dev, 2 Analist, 1 Tasarımcı, 1 QA) | **Karmaşık Projeler**, Üretim Hazır Kod. |
| **x10** | **Kurumsal Ekip (Enterprise)** (1 Lider, 1 Mimar, 3 Dev, 2 Analist, 2 Tasarımcı, 1 QA) | **Büyük Ölçekli Sistemler**, Uçtan Uca CI/CD. |
| **xGame** | **Oyun Geliştirme Ekibi** (Mimar, Gameplay, Sanat, Proje, Pazarlama) | **Oyun Projeleri**, Prototipleme, Yayın Stratejisi. |
| **x11+** | **Ölçeklenmiş Kadro** | x10 üzerindeki ek ajanlar Dev/Analist olarak dağıtılır. |

---

## 👥 Ekip Rolleri (x10 Kurumsal Konfigürasyonu)

`x10` tetiklendiğinde masa maksimum verim için 10'a bölünür:

### 1. 👑 Takım Lideri (Orchestrator)
- **Rol:** Proje Yöneticisi ve Durum Yöneticisi (State Manager).
- **Sorumluluk:** Kademeli yüklemeyi yönetir (Lazy Loading), çıktıyı sentezler.

### 2. 📐 Sistem Mimarı (Architect)
- **Rol:** Tasarım Desenleri Uzmanı.
- **Sorumluluk:** Mimari yönü çizer, bağımlılıkları belirler.

### 3. ⚡ Kıdemli Geliştiriciler (Dev One, Two, Three)
- **Rol:** Çekirdek Mühendislik Ekibi.
- **Sorumluluk:** Dev One (Backend), Dev Two (Frontend), Dev Three (DevOps & CI/CD).

### 4. 🔍 Sistem Analistleri (Alpha & Beta)
- **Rol:** İş ve Güvenlik Uzmanları.
- **Sorumluluk:** Alpha (İş mantığı), Beta (Güvenlik ve uç durumlar).

### 5. 🎨 Tasarımcılar (Aura & Nova)
- **Rol:** UI/UX ve A11y Ekibi.
- **Sorumluluk:** Aura (Görsel ve UI), Nova (UX, Erişilebilirlik ve Motion).

### 6. 🛡️ QA Mühendisi
- **Rol:** Test Uzmanı (SDET).
- **Sorumluluk:** Uçtan uca (E2E) doğrulama ve kod onayı.

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
