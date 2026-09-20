# İş Kuralları

## BR-01 — Kurumsal Müşteri Zorunluluğu

Teklif talebi yalnızca kurumsal müşteriler tarafından oluşturulabilmelidir.

## BR-02 — Zorunlu Bilgiler

Teklif talebi oluşturulabilmesi için firma adı, yetkili kişi, e-posta, telefon, ürün veya hizmet ve miktar bilgileri doldurulmalıdır.

## BR-03 — Pozitif Miktar

Teklif talebindeki ürün veya hizmet miktarı 0'dan büyük olmalıdır.

## BR-04 — Talep Durumu

Yeni oluşturulan teklif talebinin başlangıç durumu **"Yeni"** olmalıdır.

## BR-05 — Durum Geçişleri

Teklif talebinin durumu yalnızca tanımlanmış süreç akışına uygun şekilde değiştirilebilmelidir.

Örnek:

```text
Yeni
  ↓
İnceleniyor
  ↓
Teklif Hazırlandı
  ↓
Müşteriye İletildi
  ↓
Kabul Edildi / Reddedildi
```

## BR-06 — Ek Bilgi Bekleme

Satış ekibi gerekli bilgilerin eksik olduğunu tespit ederse talep **"Ek Bilgi Bekleniyor"** durumuna alınabilmelidir.

## BR-07 — Teklif Geçerlilik Tarihi

Hazırlanan teklifin bir geçerlilik tarihi bulunmalıdır.

## BR-08 — Teklif Kabul / Red

Müşteri yalnızca kendisine iletilmiş aktif bir teklifi kabul veya reddedebilmelidir.

## BR-09 — Yetki Kontrolü

Kullanıcıların gerçekleştirebileceği işlemler sistemdeki rollerine göre belirlenmelidir.

## BR-10 — Talep Numarası

Her teklif talebi sistem tarafından benzersiz bir talep numarası ile oluşturulmalıdır.

## BR-11 — İşlem Kaydı

Teklif talebi üzerinde gerçekleştirilen kritik işlemler kullanıcı, tarih ve işlem bilgisiyle kayıt altına alınmalıdır.

## BR-12 — Teklif Tutarı

Teklifin toplam tutarı ürün veya hizmet miktarı ile birim fiyatın çarpılmasıyla hesaplanmalıdır.

```text
Toplam Tutar = Miktar × Birim Fiyat
```
