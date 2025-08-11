# Minimal Anti-Bot Guardrails

Kısa özet: Sadece davranışsal basit eşikler; yanlış pozitif düşük, disiplin akışına yönlendirir.

- KPI'lar: Bot şüphesi tespit oranı, yanlış pozitif < %1.

---

## 1) Problem ve Hedef
- Sorun: Dış makro/botlar; 7/24 aynı rota.
- Hedef: Hafif telemetri ile uyarı → shadow nerf → jail sıradüzeni.

## 2) Kapsam ve Dışı
- Kapsam: Bölge/rota/uptime, hedef çeşitliliği, sohbet/parti aktivitesi.
- Dışı: İstemci tarafı anti-cheat.

## 3) Kullanıcı ve Kriter
- Given 6 saat aynı hücre + 0 sohbet/parti, Then uyarı.
- Given tekrar, Then shadow nerf; üçüncüde jail.

## 4) Akış
- Sample → Score → Action(warn/nerf/jail).

## 5) Veri Modeli
- BotScore(userId, window, score, actions[]).

## 6) Güvenlik
- Yalnız davranışsal metrik; latency-tolerant.

## 7) Ekonomi
- Bot arzı azalır; fiyat istikrarı artar.

## 8) Riskler
- Yanlış pozitif; eşikler geniş, sadece uyarı/nerf/jail.

## 9) İzleme
- Score dağılımı, action oranları.

## 10) Test Planı
- Simülasyon: insan vs bot profilleri.

---

## Kod Temas Noktaları (KO/OpenKO)
- Paket: `WIZ_SPEEDHACK_CHECK` yanına davranış puanı.
- Sunucu: `MoveProcess`, `Attack`, `ItemGet` sayaçları; `KickOutZoneUser` ile jail warp.
- UI: sadece uyarı mesajları; ceza ekranı yok.
