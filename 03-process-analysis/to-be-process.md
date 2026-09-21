# Hedef Süreç — TO-BE

## Süreç Tanımı

Kurumsal müşterilerin teklif taleplerini sistem üzerinden standart bir form kullanarak oluşturduğu ve satış ekibinin bu talepleri merkezi olarak yönettiği hedef süreçtir.

## Hedef Süreç Akışı

```text 
Kurumsal Müşteri
       ↓
Sisteme Giriş
       ↓
Teklif Talebi Formunu Doldurur
       ↓
Sistem Zorunlu Alanları Kontrol Eder
       ↓
Bilgiler Eksiksiz mi?
   ↙           ↘
 Hayır          Evet
  ↓              ↓
Hata Mesajı    Talep Oluşturulur
                  ↓
              Talep Numarası
              Oluşturulur
                  ↓
              Durum: Yeni
                  ↓
             Satış Ekibi İnceler
                  ↓
           Eksik Bilgi Var mı?
             ↙          ↘
           Evet          Hayır
            ↓             ↓
       Ek Bilgi          Teklif
       Talebi            Hazırlanır
            ↓             ↓
       Bilgiler        Müşteriye
       Tamamlanır       İletilir
                          ↓
                    Müşteri Kararı
                     ↙         ↘
                  Kabul       Red
                    ↓           ↓
              Kabul Edildi   Reddedildi
```

## Hedef Süreçte Sağlanan İyileştirmeler

| Mevcut Problem                    | Hedef Çözüm                                        |
| --------------------------------- | -------------------------------------------------- |
| Standart olmayan bilgiler         | Standart teklif talep formu                        |
| Manuel takip                      | Merkezi talep yönetimi                             |
| Eksik bilgiler                    | Zorunlu alan ve doğrulama kontrolleri              |
| Süreç görünürlüğünün düşük olması | Talep durumlarının sistem üzerinden takip edilmesi |
| İşlem geçmişinin dağınık olması   | Merkezi işlem geçmişi                              |
| Talep takibinin zor olması        | Benzersiz talep numarası                           |

## Hedef Süreç Sonucu

Teklif talebinin oluşturulmasından sonuçlanmasına kadar tüm süreç sistem üzerinden izlenebilir hale getirilir.
