# İtibar ve Klan Başarı Sistemi

Kısa özet: Kontrat performansına dayalı bireysel ve klan itibarı; görünür puan, yorum ve rozetlerle güven artırımı.

- KPI'lar:
  - Tekrar eden eşleşmelerde artış %
  - Ortalama puan dağılımının stabilitesi
  - İhtilaf oranında azalma %

---

## 1) Problem ve Hedef
- Güvenilir hizmet sağlayıcı/müşteri ayrıştırması zor.
- Hedef: Şeffaf, anlaşılırlığı yüksek itibar ve rozet sistemi.

## 2) Kapsam ve Kapsam Dışı
- Kapsam: Kontrat sonrası puan/yorum, puanların ağırlıklandırılması, rozetler.
- Kapsam dışı: Oyun dışı sosyal puanların entegrasyonu.

## 3) Kullanıcı Hikayeleri ve Kabul Kriterleri
- Bir müşteri olarak; yüksek puanlı sağlayıcıları filtreleyebilmeliyim.
- Bir sağlayıcı olarak; rozetlerimi profilimde gösterebilmeliyim.
- Kabul kriterleri: Given/When/Then maddeleri eklenecek.

## 4) Durum Makinesi
- ReputationScore: hesaplanıyor → yayınlandı → decay → güncellendi.

## 5) Veri Modeli
- Reputation(userId, score, decayRate, ratings[], reviews[])
- ClanReputation(clanId, score, achievements[])

## 6) API Taslakları
- GET /profiles/{id}
- GET /profiles/{id}/reputation
- POST /contracts/{id}/rate

## 7) UI/UX Akışları
- Profil sayfası, rozet duvarı, filtreler.

## 8) Güvenlik ve Kötüye Kullanım
- Sybil/spam, karşılıklı puan şişirme, hızlı puan manipülasyonu → ağırlıklandırma, decay, anomali tespiti.

## 9) Ekonomik Etki
- İyi davranışı ödüllendirerek pazar verimini artırır.

## 10) Riskler ve Mitigasyon
- Yeni hesapların dezavantajı → "yeni ama doğrulanmış" rozeti.

## 11) İzleme ve Telemetri
- Ortalama puan, varyans, anomali sayısı.

## 12) Test Planı
- E2E: sözleşme sonrası puanlama akışı.
- Yük testi: profil listeleme/filtreleme.
