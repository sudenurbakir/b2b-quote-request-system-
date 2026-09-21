# Requirements Traceability Matrix

## 1. Amaç

Requirements Traceability Matrix (RTM), projede tanımlanan gereksinimlerin analiz, geliştirme ve test süreçleri boyunca takip edilmesini sağlar.

Bu dokümanda iş gereksinimleri ile fonksiyonel gereksinimler, kullanıcı hikâyeleri, kabul kriterleri ve test senaryoları arasındaki bağlantı gösterilmektedir.

## 2. Gereksinim İzlenebilirlik Matrisi

| Business Requirement                                          | Functional Requirement                  | User Story | Acceptance Criteria                | Test Case           |
| ------------------------------------------------------------- | --------------------------------------- | ---------- | ---------------------------------- | ------------------- |
| BR-01 Kurumsal müşteri tarafından teklif talebi oluşturulması | FR-01 Teklif talebi oluşturma           | US-01      | AC-US01-01, AC-US01-02, AC-US01-03 | TC-01, TC-04        |
| BR-02 Teklif talebi bilgilerinin standart şekilde toplanması  | FR-02 Zorunlu alan kontrolü             | US-02      | AC-US02-01, AC-US02-02, AC-US02-03 | TC-02, TC-03        |
| BR-03 Teklif taleplerinin merkezi olarak takip edilmesi       | FR-05 Talep listesinin görüntülenmesi   | US-03      | AC-US03-01, AC-US03-02             | TC-05               |
| BR-03 Teklif taleplerinin merkezi olarak takip edilmesi       | FR-06 Talep detaylarının görüntülenmesi | US-04      | AC-US04-01, AC-US04-02             | TC-06               |
| BR-04 Talep durumlarının yönetilmesi                          | FR-07 Talep durumunun güncellenmesi     | US-05      | AC-US05-01, AC-US05-02, AC-US05-03 | TC-08, TC-10, TC-11 |
| BR-05 Eksik bilgilerin tamamlanabilmesi                       | FR-07 Talep durumunun güncellenmesi     | US-06      | AC-US06-01, AC-US06-02, AC-US06-03 | TC-09               |
| BR-06 Teklif oluşturulması                                    | FR-08 Teklif oluşturma                  | US-07      | AC-US07-01, AC-US07-02, AC-US07-03 | TC-12, TC-13, TC-14 |
| BR-07 Hazırlanan teklifin müşteriye iletilmesi                | FR-09 Teklifin müşteriye gönderilmesi   | US-08      | AC-US08-01, AC-US08-02             | TC-15, TC-16        |
| BR-08 Müşteri kararının sisteme kaydedilmesi                  | FR-10 Müşteri kabul/reddetme            | US-09      | AC-US09-01, AC-US09-02, AC-US09-03 | TC-17, TC-18, TC-19 |
| BR-09 Satış yöneticisinin süreçleri takip edebilmesi          | FR-05 Talep listesinin görüntülenmesi   | US-10      | AC-US10-01, AC-US10-02             | TC-05               |
| BR-10 Kullanıcı yetkilendirmelerinin yönetilmesi              | FR-11 Rol bazlı yetkilendirme           | US-11      | AC-US11-01, AC-US11-02, AC-US11-03 | TC-20, TC-21, TC-22 |
| BR-11 İşlem geçmişinin tutulması                              | FR-12 İşlem geçmişinin görüntülenmesi   | US-12      | AC-US12-01, AC-US12-02, AC-US12-03 | TC-23, TC-24        |
| BR-12 Teklif toplam tutarının doğru hesaplanması              | FR-08 Teklif oluşturma                  | US-07      | AC-US07-02                         | TC-13               |

## 3. İzlenebilirlik Kontrolü

Proje kapsamında gereksinimlerin aşağıdaki aşamalar boyunca takip edilebilir olması hedeflenmiştir:

**Business Requirement**
↓
**Functional Requirement**
↓
**User Story**
↓
**Acceptance Criteria**
↓
**Test Case**
↓
**UAT**

Bu yapı sayesinde:

* Her iş gereksiniminin sistem fonksiyonlarına nasıl dönüştüğü görülebilir.
* Her fonksiyonun hangi kullanıcı ihtiyacını karşıladığı takip edilebilir.
* Kullanıcı hikâyelerinin kabul kriterleriyle ilişkisi kontrol edilebilir.
* Gereksinimlerin test senaryolarıyla doğrulanması sağlanabilir.
* Gereksinimlerin karşılanmadığı noktalar daha kolay tespit edilebilir.

## 4. Kapsam Kontrolü

RTM oluşturulurken aşağıdaki kontroller dikkate alınmıştır:

| Kontrol                                                       | Durum |
| ------------------------------------------------------------- | ----- |
| İş gereksinimleri tanımlandı mı?                              | Evet  |
| Fonksiyonel gereksinimler tanımlandı mı?                      | Evet  |
| Gereksinimler kullanıcı hikâyelerine bağlandı mı?             | Evet  |
| Kullanıcı hikâyeleri kabul kriterleriyle ilişkilendirildi mi? | Evet  |
| Gereksinimler test senaryolarıyla ilişkilendirildi mi?        | Evet  |
| UAT kapsamında iş süreçleri doğrulandı mı?                    | Evet  |

## 5. Sonuç

Requirements Traceability Matrix sayesinde projenin başlangıcında tanımlanan iş ihtiyaçlarının analiz ve test süreçleri boyunca izlenebilir olması sağlanmıştır.

Bu yapı, gereksinimlerin unutulmasını veya herhangi bir gereksinimin analiz ve test sürecinin dışında kalmasını azaltmayı amaçlamaktadır.
