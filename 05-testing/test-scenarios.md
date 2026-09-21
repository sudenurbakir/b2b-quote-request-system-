# Test Senaryoları

## 1. Teklif Talebi Oluşturma

| Test ID | Senaryo | Ön Koşul | Test Adımı | Beklenen Sonuç |
|---|---|---|---|---|
| TC-01 | Geçerli bilgilerle teklif talebi oluşturma | Kullanıcı sisteme giriş yapmış olmalı | Zorunlu alanlar doldurulur ve form gönderilir | Teklif talebi oluşturulur, benzersiz talep numarası atanır ve durum "Yeni" olur |
| TC-02 | Zorunlu alanların boş bırakılması | Teklif talep formu açık olmalı | Zorunlu alanlardan biri boş bırakılarak form gönderilir | Sistem ilgili alan için hata mesajı gösterir ve talep oluşturulmaz |
| TC-03 | Geçersiz miktar girilmesi | Teklif talep formu açık olmalı | Miktar alanına 0 veya negatif değer girilir | Sistem hata mesajı gösterir ve form gönderilemez |
| TC-04 | Talep numarasının oluşturulması | Geçerli bir teklif talebi gönderilmiş olmalı | Talep kaydedilir | Sistem benzersiz bir talep numarası oluşturur |

## 2. Teklif Talebi Görüntüleme

| Test ID | Senaryo | Ön Koşul | Test Adımı | Beklenen Sonuç |
|---|---|---|---|---|
| TC-05 | Satış ekibinin talepleri görüntülemesi | Satış kullanıcısı sisteme giriş yapmış olmalı | Teklif talepleri ekranı açılır | Kullanıcı yetkisi dahilindeki talepleri görüntüler |
| TC-06 | Talep detaylarının görüntülenmesi | Sistemde mevcut bir talep bulunmalı | Bir teklif talebi seçilir | Müşteri, ürün, miktar, tarih ve durum bilgileri görüntülenir |
| TC-07 | Yetkisiz kullanıcının talep görüntülemesi | Yetkisiz kullanıcı sisteme giriş yapmış olmalı | Yetkisi olmayan bir talep açılmaya çalışılır | Sistem erişimi engeller |

## 3. Talep Durum Yönetimi

| Test ID | Senaryo | Ön Koşul | Test Adımı | Beklenen Sonuç |
|---|---|---|---|---|
| TC-08 | Talebin "İnceleniyor" durumuna alınması | Talep "Yeni" durumunda olmalı | Satış kullanıcısı talebi incelemeye alır | Talebin durumu "İnceleniyor" olarak güncellenir |
| TC-09 | Ek bilgi talep edilmesi | Talep inceleniyor olmalı | Satış kullanıcısı eksik bilgi tespit eder | Talebin durumu "Ek Bilgi Bekleniyor" olur |
| TC-10 | Geçersiz durum değişikliği | Talep mevcut bir durumda olmalı | Tanımlı olmayan bir durum seçilmeye çalışılır | Sistem işlemi engeller |
| TC-11 | Durum değişikliğinin kayıt altına alınması | Yetkili kullanıcı işlem yapıyor olmalı | Talep durumu değiştirilir | Durum değişikliği kullanıcı ve tarih bilgisiyle kayıt altına alınır |

## 4. Teklif Oluşturma

| Test ID | Senaryo | Ön Koşul | Test Adımı | Beklenen Sonuç |
|---|---|---|---|---|
| TC-12 | Teklif oluşturma | Talep bilgileri eksiksiz olmalı | Satış kullanıcısı teklif oluşturur | Teklif oluşturulur ve talep ile ilişkilendirilir |
| TC-13 | Teklif toplam tutarının hesaplanması | Teklif oluşturma ekranı açık olmalı | Miktar ve birim fiyat girilir | Toplam tutar miktar × birim fiyat olarak hesaplanır |
| TC-14 | Geçerlilik tarihinin boş bırakılması | Teklif oluşturma ekranı açık olmalı | Geçerlilik tarihi girilmeden teklif kaydedilir | Sistem hata mesajı gösterir ve teklif kaydedilmez |
| TC-15 | Teklifin müşteriye iletilmesi | Geçerli bir teklif oluşturulmuş olmalı | Satış kullanıcısı teklifi müşteriye gönderir | Teklif müşteriye iletilir ve durum "Müşteriye İletildi" olur |

## 5. Müşteri Kararı

| Test ID | Senaryo | Ön Koşul | Test Adımı | Beklenen Sonuç |
|---|---|---|---|---|
| TC-16 | Müşterinin teklifi görüntülemesi | Müşteriye iletilmiş aktif teklif bulunmalı | Müşteri teklif ekranını açar | Teklif detayları ve geçerlilik tarihi görüntülenir |
| TC-17 | Müşterinin teklifi kabul etmesi | Aktif bir teklif müşteriye iletilmiş olmalı | Müşteri "Kabul Et" seçeneğine tıklar | Teklif kabul edilir ve durum "Kabul Edildi" olur |
| TC-18 | Müşterinin teklifi reddetmesi | Aktif bir teklif müşteriye iletilmiş olmalı | Müşteri "Reddet" seçeneğine tıklar | Teklif reddedilir ve durum "Reddedildi" olur |
| TC-19 | Sonuçlanmış teklif üzerinde tekrar işlem yapılması | Teklif kabul edilmiş veya reddedilmiş olmalı | Müşteri tekrar kabul/reddet işlemi yapmaya çalışır | Sistem işlemi engeller |

## 6. Yetkilendirme

| Test ID | Senaryo | Ön Koşul | Test Adımı | Beklenen Sonuç |
|---|---|---|---|---|
| TC-20 | Satış kullanıcısının teklif oluşturması | Kullanıcı "Satış Ekibi" rolüne sahip olmalı | Teklif oluşturma işlemi gerçekleştirilir | İşlem başarılı şekilde tamamlanır |
| TC-21 | Müşterinin yetkisiz işlem yapması | Kullanıcı "Kurumsal Müşteri" rolüne sahip olmalı | Müşteri satış ekibine ait bir işlem yapmaya çalışır | Sistem işlemi engeller |
| TC-22 | Sistem yöneticisinin rol yönetimi | Kullanıcı sistem yöneticisi rolüne sahip olmalı | Kullanıcı rolü değiştirilir | Rol değişikliği başarılı şekilde kaydedilir |

## 7. İşlem Geçmişi

| Test ID | Senaryo | Ön Koşul | Test Adımı | Beklenen Sonuç |
|---|---|---|---|---|
| TC-23 | İşlem geçmişinin görüntülenmesi | Sistemde kayıtlı işlem geçmişi bulunmalı | Yetkili kullanıcı geçmiş ekranını açar | İşlemler tarih, kullanıcı ve işlem bilgileriyle görüntülenir |
| TC-24 | İşlem geçmişinin değiştirilmesinin engellenmesi | İşlem geçmişinde kayıt bulunmalı | Kullanıcı mevcut geçmiş kaydını değiştirmeye çalışır | Sistem değişiklik yapılmasına izin vermez |

## Test Sonucu Değerlendirmesi

Testler sonucunda aşağıdaki durumlar kontrol edilmelidir:

- Teklif talebi doğru şekilde oluşturulabiliyor mu?
- Zorunlu alan kontrolleri çalışıyor mu?
- Talep numarası benzersiz şekilde oluşturuluyor mu?
- Talep durumları doğru şekilde güncelleniyor mu?
- Ek bilgi süreci doğru çalışıyor mu?
- Teklif toplam tutarı doğru hesaplanıyor mu?
- Teklif müşteriye doğru şekilde iletiliyor mu?
- Müşteri kabul/reddet işlemlerini gerçekleştirebiliyor mu?
- Yetkisiz işlemler engelleniyor mu?
- İşlem geçmişi doğru şekilde kayıt altına alınıyor mu?
