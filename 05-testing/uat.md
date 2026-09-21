# Kullanıcı Kabul Testi (UAT)

## 1. UAT Amacı

Bu UAT çalışmasının amacı, B2B Teklif Talep Sistemi'nin tanımlanan iş gereksinimlerini ve kullanıcı ihtiyaçlarını karşılayıp karşılamadığını kontrol etmektir.

UAT kapsamında sistemin özellikle aşağıdaki iş süreçleri doğrulanır:

- Teklif talebi oluşturma
- Talep bilgilerinin kontrol edilmesi
- Ek bilgi talep edilmesi
- Teklif oluşturulması
- Teklifin müşteriye iletilmesi
- Müşterinin teklifi kabul veya reddetmesi
- Kullanıcı yetkilendirmeleri
- İşlem geçmişinin tutulması

---

## 2. UAT Kapsamı

| Alan | Açıklama |
|---|---|
| Teklif Talebi | Kurumsal müşterinin teklif talebi oluşturabilmesi |
| Talep Yönetimi | Satış ekibinin talepleri görüntüleyebilmesi ve yönetebilmesi |
| Ek Bilgi Süreci | Eksik bilgiler için müşteriden ek bilgi istenebilmesi |
| Teklif Yönetimi | Satış ekibinin teklif oluşturabilmesi |
| Müşteri Kararı | Müşterinin teklifi kabul veya reddedebilmesi |
| Yetkilendirme | Kullanıcıların rollerine göre işlem yapabilmesi |
| İşlem Geçmişi | Kritik işlemlerin kayıt altına alınması |

---

## 3. UAT Senaryoları

### UAT-01: Teklif Talebi Oluşturma

**Amaç:**  
Kurumsal müşterinin geçerli bilgilerle yeni bir teklif talebi oluşturabildiğini doğrulamak.

**Test Adımları:**

1. Kurumsal müşteri sisteme giriş yapar.
2. Teklif talep ekranını açar.
3. Firma ve yetkili bilgilerini girer.
4. E-posta ve telefon bilgilerini girer.
5. Ürün ve miktar bilgilerini girer.
6. Talebi gönderir.

**Beklenen Sonuç:**

- Teklif talebi başarıyla oluşturulmalıdır.
- Sistem benzersiz bir talep numarası oluşturmalıdır.
- Talebin ilk durumu "Yeni" olmalıdır.

**Kabul Kriteri:**  
Talep eksiksiz şekilde oluşturulabiliyorsa UAT başarılı kabul edilir.

---

### UAT-02: Eksik Bilgi Kontrolü

**Amaç:**  
Sistemin zorunlu bilgilerin eksik olması durumunda talep oluşturulmasını engellediğini doğrulamak.

**Test Adımları:**

1. Teklif talep ekranı açılır.
2. Zorunlu alanlardan biri boş bırakılır.
3. Form gönderilmeye çalışılır.

**Beklenen Sonuç:**

- Sistem eksik alanı belirtmelidir.
- Talep oluşturulmamalıdır.
- Kullanıcı eksik bilgiyi tamamlayabilmelidir.

**Kabul Kriteri:**  
Eksik bilgiler nedeniyle hatalı bir talep oluşturulamıyorsa UAT başarılı kabul edilir.

---

### UAT-03: Ek Bilgi Talebi

**Amaç:**  
Satış ekibinin eksik bilgi bulunan bir talep için müşteriden ek bilgi isteyebildiğini doğrulamak.

**Test Adımları:**

1. Satış kullanıcısı sisteme giriş yapar.
2. Mevcut bir teklif talebini açar.
3. Talepte eksik bilgi olduğunu tespit eder.
4. Ek bilgi talebi oluşturur.

**Beklenen Sonuç:**

- Talebin durumu "Ek Bilgi Bekleniyor" olmalıdır.
- Müşteri eksik bilgileri tamamlayabilmelidir.
- Bilgiler tamamlandıktan sonra talep yeniden değerlendirmeye alınabilmelidir.

**Kabul Kriteri:**  
Ek bilgi süreci baştan sona doğru şekilde çalışıyorsa UAT başarılı kabul edilir.

---

### UAT-04: Teklif Oluşturma

**Amaç:**  
Satış ekibinin tamamlanmış bir teklif talebi üzerinden teklif oluşturabildiğini doğrulamak.

**Test Adımları:**

1. Satış kullanıcısı tamamlanmış bir talebi açar.
2. Teklif oluşturma ekranını açar.
3. Ürün, miktar ve birim fiyat bilgilerini girer.
4. Geçerlilik tarihini belirler.
5. Teklifi kaydeder.

**Beklenen Sonuç:**

- Teklif başarıyla oluşturulmalıdır.
- Toplam tutar doğru hesaplanmalıdır.
- Teklif talep ile ilişkilendirilmelidir.
- Teklif geçerlilik tarihi kaydedilmelidir.

**Kabul Kriteri:**  
Geçerli bir teklif oluşturulabiliyor ve bilgiler doğru hesaplanıyorsa UAT başarılı kabul edilir.

---

### UAT-05: Teklifin Müşteriye İletilmesi

**Amaç:**  
Hazırlanan teklifin müşteriye iletilebildiğini doğrulamak.

**Test Adımları:**

1. Satış kullanıcısı oluşturulan teklifi açar.
2. Teklifi müşteriye iletir.

**Beklenen Sonuç:**

- Teklif müşterinin hesabında görüntülenebilmelidir.
- Talebin durumu "Müşteriye İletildi" olmalıdır.
- Teklif bilgileri değişmeden müşteriye gösterilmelidir.

**Kabul Kriteri:**  
Müşteri gönderilen teklifi görüntüleyebiliyorsa UAT başarılı kabul edilir.

---

### UAT-06: Teklifin Kabul Edilmesi

**Amaç:**  
Müşterinin geçerli bir teklifi kabul edebildiğini doğrulamak.

**Test Adımları:**

1. Müşteri sisteme giriş yapar.
2. Müşteriye iletilmiş teklifi açar.
3. Teklif bilgilerini kontrol eder.
4. "Kabul Et" seçeneğine tıklar.

**Beklenen Sonuç:**

- Teklif kabul edilmelidir.
- Talebin durumu "Kabul Edildi" olmalıdır.
- Müşteri kararının sistemde kayıt altına alınması gerekir.

**Kabul Kriteri:**  
Teklif kabul işlemi başarıyla tamamlanıyorsa UAT başarılı kabul edilir.

---

### UAT-07: Teklifin Reddedilmesi

**Amaç:**  
Müşterinin geçerli bir teklifi reddedebildiğini doğrulamak.

**Test Adımları:**

1. Müşteri sisteme giriş yapar.
2. Müşteriye iletilmiş teklifi açar.
3. "Reddet" seçeneğine tıklar.

**Beklenen Sonuç:**

- Teklif reddedilmelidir.
- Talebin durumu "Reddedildi" olmalıdır.
- Müşteri kararının sistemde kayıt altına alınması gerekir.

**Kabul Kriteri:**  
Teklif reddetme işlemi başarıyla tamamlanıyorsa UAT başarılı kabul edilir.

---

## 4. UAT Sonuç Durumları

| Durum | Açıklama |
|---|---|
| PASS | Senaryo beklenen şekilde tamamlandı |
| FAIL | Beklenen sonuç alınamadı |
| BLOCKED | Testin gerçekleştirilmesini engelleyen bir problem bulunuyor |
| NOT TESTED | Senaryo henüz test edilmedi |

---

## 5. UAT Kabul Kriterleri

Sistemin kullanıcı kabul sürecinin tamamlanabilmesi için:

- Kritik iş süreçleri başarıyla tamamlanmalıdır.
- Teklif talebi oluşturulabilmelidir.
- Zorunlu alan kontrolleri çalışmalıdır.
- Teklif oluşturma süreci çalışmalıdır.
- Toplam tutar doğru hesaplanmalıdır.
- Teklif müşteriye iletilebilmelidir.
- Müşteri kabul veya ret işlemi gerçekleştirebilmelidir.
- Yetkilendirme kuralları uygulanmalıdır.
- Kritik işlemler kayıt altına alınmalıdır.

Kritik işlevlerden birinin çalışmaması durumunda ilgili UAT senaryosu "FAIL" olarak değerlendirilir.

---

## 6. UAT Sonuç Özeti

| UAT ID | Sonuç | Açıklama |
|---|---|---|
| UAT-01 | PASS / FAIL | Teklif talebi oluşturma |
| UAT-02 | PASS / FAIL | Eksik bilgi kontrolü |
| UAT-03 | PASS / FAIL | Ek bilgi talebi |
| UAT-04 | PASS / FAIL | Teklif oluşturma |
| UAT-05 | PASS / FAIL | Teklifin müşteriye iletilmesi |
| UAT-06 | PASS / FAIL | Teklifin kabul edilmesi |
| UAT-07 | PASS / FAIL | Teklifin reddedilmesi |

> Not: Sonuç alanları gerçek bir uygulama üzerinde test gerçekleştirildiğinde doldurulacaktır.
