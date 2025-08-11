# Tezgah Yoğunluğu ve Stall QoS

Kısa özet: Kalabalık bölgelerde tezgah sayısını ve kaynak kullanımını yönetme; görünürlük ve performans. Tezgah görüntüleme kuyruğu ve adil erişim.

- KPI'lar: Moradon FPS iyileşmesi, tezgah başına görüntülenme.

---

## 1) Problem ve Hedef
- Sorun: Tezgah kalabalığı lag ve görünürlük sorunları yaratıyor. Tezgah sahibi ekranı “bloklayınca” başkaları bakamıyor.
- Hedef: Bölge başına yumuşak limit, bekleme kuyruğu, adil görüntüleme süresi ve kısa blacklist.

## 2) Kapsam ve Dışı
- Kapsam: Stall slot limiti, yoğunluk bazlı bakım ücreti, bekleme kuyruğu, görüntüleme süresi yönetimi.
- Dışı: Mevcut %3 satış vergisi değişmez.

## 3) Kullanıcı ve Kriter
- Given Moradon dolu, Then yeni tezgah sıraya alınır ve slot açılınca otomatik açılır.
- Given bir tezgahı görüntülemeye başladım, Then max 60 saniye görüntüleyebilirim; süre dolunca otomatik kapanır.
- Given görüntüleme sürem doldu, Then 60 saniye boyunca aynı tezgahı yeniden görüntüleyemem (blacklist).

## 4) Akış
- Open → (Full) Queue → Admit → Close.
- View → 60s timer → Auto close → 60s blacklist.

## 5) Veri Modeli
- StallSlot(zoneId, capacity, queue[]).
- StallView(userId, stallId, startedAt, expiresAt, blacklistUntil).

## 6) UI/UX
- “Sıradasınız” bildirimi; tahmini bekleme süresi.
- Tezgah görüntüleme sayacında kalan süre göstergesi.

## 7) Güvenlik
- Çoklu hesap spam: aynı IP/HWID için sırada sert limit; blacklist kullanıcı/cihaz bazlı.

## 8) Ekonomi
- Yoğunlukta küçük bakım ücreti; sink (tezgah sahibine uygulanır, görüntüleyene değil).

## 9) Riskler
- Uzayan kuyruklar; alternatif bölge önerisi ve kapasite artırımı pencereleri.

## 10) İzleme
- Kuyruk uzunluğu, ortalama bekleme, kişi başı görüntüleme süresi.

## 11) Test Planı
- Kapasite dolumu, sıraya giriş/çıkış; görüntüleme süresi ve blacklist zamanlayıcıları.

---

## Kod Temas Noktaları (KO/OpenKO)
- Paket: `WIZ_MERCHANT` (`MERCHANT_OPEN/CLOSE/ITEM_LIST`), `MERCHANT_ITEM_LIST` görüntüleme başlat/bitir alt-olayı.
- Sunucu: bölge bazlı kapasite sayacı ve `StallView` yönetimi (timer, blacklist). `User::MarketBBS*` değil, doğrudan merchant görüntüleme.
- UI: tezgah açılışında durum mesajları ve görüntüleme sayaç UI.
