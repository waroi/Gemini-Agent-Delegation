# Mimari: Ajan Delegasyon Sistemi

## "Ortak Akıl" (Hive Mind) Kavramı
Geleneksel doğrusal zincirlerin aksine, bu sistem Gemini CLI'ın bağlam penceresi tarafından yönetilen bir "Yuvarlak Masa" mimarisi kullanır.

### 1. Orkestratör (Takım Lideri)
`Takım Lideri`, standart anlamda nihai çıktı akışına doğrudan "yazan" tek ajandır. Bağlam yöneticisi olarak hareket eder.
- **Girdi:** Kullanıcı İstemi + `x7` tetikleyicisi.
- **Süreç:**
    1.  `x7`'yi ayrıştırır -> 6 alt personayı yükler.
    2.  Her personanın bağlam tamponuna katkıda bulunduğu bir "düşünce döngüsünü" simüle eder.
    3.  Gürültüyü (gereksiz nezaket sözlerini) filtreler.
    4.  Her persona için en iyi araçları seçer.

### 2. Rol Özelleşmesi & Model Yönlendirme
CLI tek bir çıkarım akışı üzerinde çalışırken, yanıtın her bölümü için **Sistem Talimatı** sıcaklığını (temperature) ve stilini ayarlayarak "Model Yönlendirmesi"ni simüle ederiz.

- **Analist Modu:** Yüksek Sıcaklık (Yaratıcı uç durum bulma), Katı Mantık.
- **Geliştirici Modu:** Düşük Sıcaklık (Deterministik kod), Katı Sözdizimi.
- **Tasarım Modu:** Yüksek Sıcaklık (Yaratıcı görsel betimlemeler).
- **QA Modu:** Düşük Sıcaklık (Eleştirel, Kuralcı).

### 3. Bağlam Yönetimi ve Token Optimizasyonu
Ajan sayısı x10'a (Enterprise Team) çıktığında bağlam penceresini verimli kullanmak kritik hale gelir. Bunu sağlamak için:
- **Paylaşılan Durum (Shared State):** Lider (Orchestrator) tüm sürecin başında bir `State Manager` (Durum Yöneticisi) gibi davranarak kullanıcı gereksinimlerini "Gereksinim ID: 1.1" formatında numaralandırır. Diğer ajanlar metni tekrar etmek yerine sadece ID numarası ile referans verirler.
- **Kademeli Çalıştırma (Lazy Loading):** Tüm ajanların aynı anda konuşmaya başlaması bağlamı zehirleyebilir (Context Poisoning). x10 kurgusunda ajanlar sırayla devreye girer:
  1. *Keşif Aşaması:* Analistler (Alpha & Beta) ve Tasarımcılar (Aura & Nova).
  2. *Mimari Aşama:* Sistem Mimarı (Architect).
  3. *Uygulama Aşaması:* Geliştiriciler (Dev One, Two, Three).
  4. *Doğrulama Aşaması:* QA Mühendisi.
- **Artımlı Fark (Diff):** Ajanlar planın tamamını her seferinde değil, sadece plandaki *değişiklikleri* veya *eklemeleri* çıktı olarak verirler.
- **Sentezlenmiş Çıktı:** Kullanıcı, 10 ajanın uzun iç tartışmasını değil, yalnızca işbirliğinin sonucunu görür.

### 4. Yuvarlak Masa Yapısı (x7 Standardı)
`x7` tetiklendiğinde masa şu şekilde kurulur:
1.  **Lider (1):** Oturumu açar/kapatır.
2.  **Analistler (2):** Biri iş mantığına, diğeri güvenliğe odaklanır.
3.  **Geliştiriciler (2):** Biri Backend/Core, diğeri Frontend/Entegrasyon yazar.
4.  **Tasarımcı (1):** Görsel ve UX kararlarını verir.
5.  **QA Mühendisi (1):** Test stratejisini belirler ve son onayı verir.

### 5. Genişletilmiş Yuvarlak Masa Yapısı (x10 Standardı)
`x10` (Enterprise Team) tetiklendiğinde bağlam penceresi maksimum verimle kullanılır ve masa şu şekilde genişler:
1.  **Takım Lideri (1):** Tüm süreci ve çıktıları orkestre eder.
2.  **Sistem Mimarı (1):** Mimari desenleri ve sistem tasarımını belirler.
3.  **Geliştiriciler (3):** Backend, Frontend ve DevOps/Altyapı olarak üçe ayrılır.
4.  **Analistler (2):** İş mantığı ve uç durumlar/güvenlik senaryolarını inceler.
5.  **Tasarımcılar (2):** Biri UI/Görsel, diğeri UX/Erişilebilirlik (A11y) üzerinde çalışır.
6.  **QA Mühendisi (1):** Test stratejisi ve son doğrulama aşamasını (Validation) yürütür.

### 6. Oyun Geliştirme Mimarisi (xGame)
Oyun geliştirme süreçleri için özelleştirilmiş `xGame` tetikleyicisi, farklı bir uzmanlık dağılımı kullanır:

1.  **Oyun Mimarı (Lider):** Motor (Engine) ve sistem kararlarını verir.
2.  **Gameplay Geliştirici:** Mekanik ve oynanış döngülerini kodlar (C#/C++/Blueprint).
3.  **Sanat Direktörü:** Görsel dil, varlık yönetimi ve UX tasarımını yönetir.
4.  **Proje Yöneticisi:** GDD, Agile süreçleri ve kapsam yönetimini sağlar.
5.  **Pazarlama Uzmanı:** Topluluk ve mağaza optimizasyonunu yürütür.

Bu yapı, teknik kod üretiminden ziyade "deneyim tasarımı" ve "yayın stratejisi" odaklıdır.
