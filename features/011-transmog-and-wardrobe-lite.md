# Transmog (Basit)

Kısa özet: Eşyaların sadece görünümünü değiştir, gücü değiştirme. Küçük coin maliyetiyle kalıcı kozmetik.

---

## 1) Problem ve Hedef
- Sorun: Görsel çeşitlilik az, motivasyon düşük.
- Hedef: Statları etkilemeden görünüm sabitleme.

## 2) Nasıl Çalışır?
- Wardrobe: Bir eşyanın görünümü “koleksiyona” kilitlenir (tek seferlik).
- Transmog: Koleksiyondan mevcut ekipmana görünüm uygularsın.
- Maliyet: Küçük coin ücreti (saf sink). Statlar değişmez.

## 3) Kabul Kriterleri
- Given görünüm uygulama, Then sadece görünüm değişir, statlar aynı kalır.
- Given trade/market, Then transmog sadece görsel katman, eşya ticaretine engel olmaz.
- Given remove, Then oyuncu görünümü sıfırlayabilir (ücretsiz veya düşük ücretli).

## 4) Akış
- Unlock → Preview → Apply → (Opsiyonel) Remove.

## 5) UI/UX
- Envanterde “Görünüm Uygula” düğmesi + küçük önizleme.

## 6) Güvenlik
- Wardrobe kaydı tradeable olmayan kopya üzerinden yapılır (dup yok).

## 7) İzleme
- Uygulama sayısı, coin sink tutarı.

---

## Kod Temas Noktaları (KO/OpenKO)
- Paket: `WIZ_USERLOOK_CHANGE` (görünüm apply/remove).
- Sunucu: `UserLookChange()` içinde skin-id yetkilendirme, coin kesimi.
- İstemci: DX9 render’da görsel katman (skin overlay) + basit UI tetikleyici.
