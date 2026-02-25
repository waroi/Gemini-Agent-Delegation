# Teknik Dokümantasyon: Ajan Yapılandırması

## Dizin Yapısı (Güncellenmiş)
```
.agent/skills/multi_agent_system/roles/
├── _TEMPLATE.md       # Rol Oluşturma Şablonu
├── core/              # Temel Mühendislik Rolleri
│   ├── team_lead.md
│   ├── principal_developer.md
│   ├── analyst.md
│   ├── designer.md
│   ├── qa_engineer.md
│   ├── researcher.md
│   └── architect.md
└── game/              # Oyun Geliştirme (xGame) Rolleri
    ├── game_architect.md
    ├── gameplay_developer.md
    ├── art_director.md
    ├── project_manager.md
    └── marketing_specialist.md
```

## Yönetişim ve Kurallar
Ajan yapısının güvenliği ve ölçeklenebilirliği için `GOVERNANCE.md` dosyasındaki kurallara uyulmalıdır.
1.  **Yeni Rol Ekleme:** `_TEMPLATE.md` dosyasını kopyalayın ve ilgili alt dizine (`core/`, `game/` vb.) ekleyin.
2.  **Referans:** Yeni rolü `SKILL.md` ve `README.md` dosyalarına eklemeyi unutmayın.

## Ajan Konfigürasyonu (x7 Standardı)
`SKILL.md` dosyası `x7` tetiklendiğinde şu 7 ajanı başlatacak şekilde ayarlanmıştır:
1.  Team Lead (`roles/core/team_lead.md`)
2.  Principal Dev One & Two (`roles/core/principal_developer.md`)
3.  Analyst Alpha & Beta (`roles/core/analyst.md`)
4.  Designer Aura (`roles/core/designer.md`)
5.  QA Engineer (`roles/core/qa_engineer.md`)

## Oyun Geliştirme Entegrasyonu (xGame)
Oyun geliştirme süreçleri için `xGame` modu, `roles/game/` dizinindeki özelleşmiş rolleri kullanır.

### Rol Tanımları
- `game_architect.md`: Motor ve Sistem Lideri.
- `gameplay_developer.md`: Mekanik ve Kodlama.
- `art_director.md`: Görsel ve UX.
- `project_manager.md`: Planlama ve GDD.
- `marketing_specialist.md`: ASO ve Topluluk.
