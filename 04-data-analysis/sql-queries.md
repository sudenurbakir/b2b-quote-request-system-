-- B2B Quote Request System
-- SQL Queries

-- 1. Tüm teklif taleplerini müşteri bilgileriyle birlikte listeleme
SELECT
    qr.talep_id,
    c.firma_adı,
    c.yetkili_adı,
    qr.talep_tarihi,
    qr.durum
FROM QUOTE_REQUEST qr
JOIN CUSTOMER c
    ON qr.müşteri_id = c.customer_id
ORDER BY qr.talep_tarihi DESC;


-- 2. Belirli bir durumdaki teklif taleplerini listeleme
-- Örnek: İnceleniyor durumundaki talepler
SELECT
    talep_id,
    müşteri_id,
    talep_tarihi,
    durum
FROM QUOTE_REQUEST
WHERE durum = 'İnceleniyor'
ORDER BY talep_tarihi ASC;


-- 3. Teklif taleplerindeki ürün ve miktar bilgilerini görüntüleme
SELECT
    qr.talep_id,
    c.firma_adı,
    p.ürün_adı,
    ri.miktar
FROM QUOTE_REQUEST qr
JOIN CUSTOMER c
    ON qr.müşteri_id = c.customer_id
JOIN REQUEST_ITEM ri
    ON qr.talep_id = ri.talep_id
JOIN PRODUCT p
    ON ri.ürün_id = p.ürün_id
ORDER BY qr.talep_id;


-- 4. Teklif detaylarını müşteri bilgileriyle birlikte listeleme
SELECT
    q.teklif_id,
    qr.talep_id,
    c.firma_adı,
    q.teklif_tarihi,
    q.geçerlilik_tarihi,
    q.toplam_tutar,
    q.durum
FROM QUOTE q
JOIN QUOTE_REQUEST qr
    ON q.talep_id = qr.talep_id
JOIN CUSTOMER c
    ON qr.müşteri_id = c.customer_id
ORDER BY q.teklif_tarihi DESC;


-- 5. Teklif kalemlerinin toplam tutarını hesaplama
SELECT
    qi.teklif_id,
    p.ürün_adı,
    qi.miktar,
    qi.birim_fiyat,
    qi.miktar * qi.birim_fiyat AS hesaplanan_toplam
FROM QUOTE_ITEM qi
JOIN PRODUCT p
    ON qi.ürün_id = p.ürün_id;


-- 6. Kabul edilmiş teklifleri listeleme
SELECT
    q.teklif_id,
    qr.talep_id,
    c.firma_adı,
    q.toplam_tutar,
    q.teklif_tarihi
FROM QUOTE q
JOIN QUOTE_REQUEST qr
    ON q.talep_id = qr.talep_id
JOIN CUSTOMER c
    ON qr.müşteri_id = c.customer_id
WHERE q.durum = 'Kabul Edildi'
ORDER BY q.teklif_tarihi DESC;


-- 7. Durumlara göre teklif talebi sayısını hesaplama
SELECT
    durum,
    COUNT(*) AS talep_sayisi
FROM QUOTE_REQUEST
GROUP BY durum
ORDER BY talep_sayisi DESC;


-- 8. En çok talep edilen ürünleri listeleme
SELECT
    p.ürün_adı,
    SUM(ri.miktar) AS toplam_talep_miktari
FROM REQUEST_ITEM ri
JOIN PRODUCT p
    ON ri.ürün_id = p.ürün_id
GROUP BY p.ürün_id, p.ürün_adı
ORDER BY toplam_talep_miktari DESC;
