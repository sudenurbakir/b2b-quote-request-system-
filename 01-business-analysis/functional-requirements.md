# Fonksiyonel Gereksinimler

## FR-01 — Teklif Talebi Oluşturma

Sistem, kurumsal müşterinin yeni bir teklif talebi oluşturmasına izin vermelidir.

Talep oluşturulurken aşağıdaki bilgiler alınmalıdır:

* Firma adı
* Yetkili kişi
* E-posta adresi
* Telefon numarası
* Ürün veya hizmet
* Miktar
* Açıklama

---

## FR-02 — Zorunlu Alan Kontrolü

Sistem, teklif talebi gönderilmeden önce zorunlu alanların doldurulup doldurulmadığını kontrol etmelidir.

Eksik bilgi bulunması durumunda kullanıcı bilgilendirilmelidir.

---

## FR-03 — Teklif Talebi Kaydetme

Sistem, başarılı şekilde gönderilen teklif taleplerini benzersiz bir talep numarası ile kaydetmelidir.

Örnek:

```text
TR-2026-0001
```

---

## FR-04 — Talep Durumu Oluşturma

Yeni oluşturulan teklif talebinin başlangıç durumu **"Yeni"** olarak atanmalıdır.

---

## FR-05 — Talep Listeleme

Satış ekibi, sistem üzerinden oluşturulan teklif taleplerini listeleyebilmelidir.

Liste üzerinde en az aşağıdaki bilgiler gösterilmelidir:

* Talep numarası
* Firma adı
* Oluşturulma tarihi
* Talep durumu
* Sorumlu satış çalışanı

---

## FR-06 — Talep Detaylarını Görüntüleme

Satış ekibi, bir teklif talebinin detaylarını görüntüleyebilmelidir.

---

## FR-07 — Talep Durumu Güncelleme

Yetkili kullanıcılar teklif talebinin durumunu güncelleyebilmelidir.

Durumlar:

```text
Yeni
İnceleniyor
Ek Bilgi Bekleniyor
Teklif Hazırlandı
Müşteriye İletildi
Kabul Edildi
Reddedildi
```

---

## FR-08 — Teklif Oluşturma

Satış ekibi, incelenen teklif talebi üzerinden teklif oluşturabilmelidir.

Teklif içerisinde en az aşağıdaki bilgiler bulunmalıdır:

* Teklif numarası
* Teklif tarihi
* Ürün veya hizmet
* Miktar
* Birim fiyat
* Toplam tutar
* Geçerlilik tarihi

---

## FR-09 — Teklif Müşteriye İletme

Sistem, hazırlanan teklifin müşteriye iletilmesini sağlamalıdır.

Teklif müşteriye iletildiğinde teklif talebinin durumu **"Müşteriye İletildi"** olarak güncellenmelidir.

---

## FR-10 — Teklif Sonucunu Kaydetme

Müşterinin teklifi kabul veya reddetmesi sistem tarafından kaydedilmelidir.

Müşteri teklifi kabul ettiğinde durum:

```text
Kabul Edildi
```

Müşteri teklifi reddettiğinde durum:

```text
Reddedildi
```

olarak güncellenmelidir.

---

## FR-11 — Yetkilendirme

Sistem, kullanıcı rollerine göre işlem yetkilerini kontrol etmelidir.

Kullanıcı yalnızca sahip olduğu rol kapsamında izin verilen işlemleri gerçekleştirebilmelidir.

---

## FR-12 — İşlem Geçmişi

Sistem, teklif talebi üzerinde gerçekleştirilen önemli işlemleri tarih, kullanıcı ve işlem bilgisiyle kaydetmelidir.
