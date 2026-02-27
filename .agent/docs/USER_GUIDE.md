# Kullanıcı Kılavuzu: Çoklu Ajan Sistemi (x7)

## Genel Bakış
Bu hazır kalıp (boilerplate), Gemini CLI'ınızı yüksek performanslı bir mühendislik ekibine dönüştürür.

## Nasıl Kullanılır
Görevinizi tanımlayın ve sonuna `xN` ekleyin.

### Tetikleyiciler

| Tetikleyici | Ekip Yapısı | Açıklama |
| :--- | :--- | :--- |
| **x2** | Lider + Dev | Hızlı düzeltmeler. |
| **x4** | Lider + Dev + Analist + Tasarımcı | Özellik geliştirme. |
| **x7** | **Standart Kadro** (Lider, 2 Dev, 2 Analist, 1 Tasarımcı, 1 QA) | **Standart Ürün Ekibi.** |
| **x10** | **Kurumsal Kadro** (Lider, Mimar, 3 Dev, 2 Analist, 2 Tasarımcı, QA) | **Büyük Ölçekli Projeler (Enterprise).** |
| **x11+** | Genişletilmiş Kadro | Çok büyük projeler için otomatik ölçeklendirme. |

## `x10` Deneyimi (Enterprise Team)
`x10` kullandığınızda, sistem dengeli ve kademeli (Lazy Loading) bir **Kurumsal Ürün Geliştirme Ekibi** simüle eder:
1.  **Keşif:** Analistler (İş/Güvenlik) ve Tasarımcılar (UI/UX) gereksinimleri çıkarır.
2.  **Mimari:** Sistem Mimarı teknik desenleri belirler.
3.  **Uygulama:** Geliştiriciler (Backend, Frontend, DevOps) kodu yazar ve CI/CD ayarlarını yapar.
4.  **Doğrulama:** QA Mühendisi uçtan uca test senaryolarını onaylar.
5.  **Sentez:** Lider (Orkestratör) iç tartışmaları filtreler ve sadece nihai sonucu size sunar.

## Ölçeklenebilirlik Notu
Sistem `xN` parametresini dinamik olarak yorumlar. `x10` üzerindeki her ek sayı, projeye daha fazla "kas gücü" (Geliştirici/Analist) ekler.
