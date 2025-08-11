# Gelişmiş Zindan Eşleştirme Sistemi

Kısa özet: Hedefe (item düşürme/NP/EXP) yönelik, güvenli ve şeffaf otomatik parti kurma ve ilerleme takibi.

- KPI'lar:
  - Eşleşme süresinde azalma
  - Tamamlanan run oranında artış
  - İhtilaf oranında azalma

---

## 1) Problem ve Hedef
- Doğru kompozisyonu hızlı bulmak ve hedefe uyum sağlamak zor.

## 2) Kapsam ve Kapsam Dışı
- Kapsam: Rol bazlı eşleştirme, hedef tanımı, ilerleme ölçümü.
- Kapsam dışı: PvP odaklı eşleştirme.

## 3) Kullanıcı Hikayeleri ve Kabul Kriterleri
- Bir oyuncu olarak; hedefimi belirleyip uygun partiyi hızlı bulabilmeliyim.

## 4) Akış Diyagramı / Durum Makinesi
- Queue → Matched → Formed → In-Run → Completed/Abandoned.

## 5) Veri Modeli
- QueueEntry, Party, RunProgress, RewardPolicy.

## 6) API Taslakları
- POST /matching/queue
- POST /matching/accept
- GET /runs/{id}/progress

## 7) UI/UX Akışları
- Eşleşme ekranı, parti onayları, ilerleme paneli.

## 8) Güvenlik ve Kötüye Kullanım
- Rol/GS puan sahteciliği, AFK → anomali tespiti, minimum aktivite kuralları.

## 9) Ekonomik Etki
- Verimli eşleşme, kontrat pazarını da besler.

## 10) Riskler ve Mitigasyon
- Yanlış eşleşme maliyeti → hızlı iptal ve yeniden eşleşme penceresi.

## 11) İzleme ve Telemetri
- Ortalama bekleme süresi, başarı oranı, iptal nedenleri.

## 12) Test Planı
- Yük testi: yoğun saatlerde kuyruk.
- E2E: run tamamlama akışı.
