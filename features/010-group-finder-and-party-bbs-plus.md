# Grup Bulucu ve Party BBS+

Kısa özet: Rol/amaç filtreleriyle hızlı parti kurma; mevcut Party BBS üzerine hafif geliştirme.

- KPI'lar: Eşleşme süresinde düşüş, tamamlanan run oranında artış.

---

## 1) Problem ve Hedef
- Sorun: Doğru rol ve hedefe uygun parti bulmak yavaş.
- Hedef: Rol (Tank/DMG/Support), hedef (EXP/NP/Item) ve minimum GS/level filtreleriyle hızlı eşleşme.

## 2) Kapsam ve Kapsam Dışı
- Kapsam: Party BBS liste/filtre, hızlı davet.
- Dışı: Tam otomatik matchmaking (sadece rehberli).

## 3) Kullanıcı Hikayeleri ve Kabul Kriterleri
- Bir oyuncu olarak; rolümü ve hedefimi seçip uygun partileri filtreleyebilmeliyim.
- Given rol=Support, When filtre uygularım, Then sadece uygun ilanlar listelenir.

## 4) Akış
- Create/Join → Filter → Invite → Accept.

## 5) Veri Modeli
- PartyPost: id, rolesNeeded[], goal, minLevel, zone, expiresAt.

## 6) API Taslakları
- POST /party/posts, GET /party/posts?role=&goal=&zone=

## 7) UI/UX
- Party BBS’de yeni filtre paneli ve hızlı davet butonları.

## 8) Güvenlik
- Spam önleme: ilan başına kısa cooldown ve otomatik silinen süre.

## 9) Ekonomik Etki
- Run verimliliği artar, oyuncu memnuniyeti yükselir.

## 10) Riskler
- Aşırı filtre → eşleşme azalır; varsayılan geniş aralık.

## 11) İzleme
- Ortalama eşleşme süresi, ilan başına görüntülenme/katılım.

## 12) Test Planı
- Filtre doğruluğu, davet/katıl akışı.

---

## Kod Temas Noktaları (KO/OpenKO)
- Paket: `WIZ_PARTY_BBS` alt-opkodları (register/list/report).
- DB: PartyPost tablosu (opsiyonel) ya da hafif bellek içi kuyruk.
- UI: Party BBS liste ekranına filtre ve hızlı davet düğmeleri.
