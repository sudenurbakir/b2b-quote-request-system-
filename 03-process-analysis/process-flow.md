# Süreç Akışı

## B2B Teklif Talep Süreci

Aşağıdaki akış, kurumsal müşterinin teklif talebi oluşturmasından teklifin sonuçlanmasına kadar olan hedef süreci göstermektedir.

```mermaid
flowchart TD
    A[Kurumsal Müşteri] --> B[Teklif Talep Formunu Doldurur]
    B --> C{Zorunlu Alanlar Eksiksiz mi?}

    C -->|Hayır| D[Hata Mesajı Gösterilir]
    D --> B

    C -->|Evet| E[Teklif Talebi Oluşturulur]
    E --> F[Talep Numarası Oluşturulur]
    F --> G[Durum: Yeni]
    G --> H[Satış Ekibi Talebi İnceler]

    H --> I{Ek Bilgi Gerekli mi?}

    I -->|Evet| J[Ek Bilgi Talebi Gönderilir]
    J --> K[Müşteri Bilgileri Tamamlar]
    K --> H

    I -->|Hayır| L[Teklif Hazırlanır]
    L --> M[Teklif Müşteriye İletilir]
    M --> N{Müşteri Kararı}

    N -->|Kabul| O[Durum: Kabul Edildi]
    N -->|Red| P[Durum: Reddedildi]
```

## Süreç Adımları

| Adım | Süreç                       | Sorumlu              |
| ---- | --------------------------- | -------------------- |
| 1    | Teklif talebi oluşturma     | Kurumsal Müşteri     |
| 2    | Bilgi doğrulama             | Sistem               |
| 3    | Talep oluşturma             | Sistem               |
| 4    | Talep inceleme              | Satış Ekibi          |
| 5    | Ek bilgi isteme             | Satış Ekibi          |
| 6    | Teklif hazırlama            | Satış Ekibi          |
| 7    | Teklifi müşteriye iletme    | Sistem / Satış Ekibi |
| 8    | Teklifi değerlendirme       | Kurumsal Müşteri     |
| 9    | Teklifi kabul veya reddetme | Kurumsal Müşteri     |
