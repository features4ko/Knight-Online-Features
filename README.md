
# Oyun Geliştirme Önerileri ve Proje Tasarımları

Bu repo, **[Knight Online]** için geliştirilmiş, oyun ekosistemini iyileştirmeyi, oyuncu deneyimini zenginleştirmeyi ve yeni ekonomik dinamikler yaratmayı hedefleyen kapsamlı proje önerilerini ve özellik tasarımlarını barındırmaktadır.

## 📜 Proje Vizyonu

Burada sunulan tüm öneriler, aşağıdaki temel prensipler üzerine inşa edilmiştir:

-   **Adalet ve Güvenlik:** Oyuncular arası etkileşimlerde dolandırıcılığı ve suistimali engelleyen, güvenli mekanizmalar oluşturmak.
-   **Ekonomik Sağlık:** Oyun içi enflasyonu kontrol altında tutan, "gold sink" mekanizmaları yaratan ve sürdürülebilir bir ekonomi sağlayan sistemler tasarlamak.
-   **Şeffaflık ve Hesap Verebilirlik:** Oyunculara, yaptıkları işlemler ve aldıkları hizmetler hakkında net, veri odaklı bilgiler sunmak.
-   **Oyuncu Bağlılığı:** Oyunculara yeni kariyer yolları ve hedefler sunarak oyuna olan bağlılıklarını artırmak.

---

## 🚀 Özellik Önerileri (Features)

Aşağıda, detaylı analizleri ve tasarımlarıyla birlikte sunulan özellik önerileri bulunmaktadır. Her bir başlık, ilgili özelliğin tam dokümantasyonunu içeren Markdown dosyasına yönlendirir.

| Durum          | ID  | Özellik Adı                                                              | Kısa Açıklama                                                                          |
| :------------- | :-- | :----------------------------------------------------------------------- | :------------------------------------------------------------------------------------- |
| 💡 **Taslak**  | 001 | [Gelişmiş Kontrat Piyasası](./features/001-advanced-contract-market.md) | "Gri pazarı" bitirecek, iki yönlü, veri odaklı ve güvenli hizmet alım-satım sistemi. |
| ⏳ Planlanıyor | 002 | [İtibar ve Klan Başarı Sistemi](./features/002-reputation-and-clan-achievements.md) | Oyuncuların ve klanların kontratlardaki başarılarına göre itibar puanı kazanması.      |
| ⏳ Planlanıyor | 003 | [Gelişmiş Zindan Eşleştirme Sistemi](./features/003-advanced-dungeon-matching.md)   | Belirli hedefler (örn: item düşürme) için otomatik ve güvenli parti kurma sistemi.     |
| 💡 **Taslak**  | 011 | [Transmog (Basit)](./features/011-transmog-and-wardrobe-lite.md)        | Stat etkilemeden görünüm sabitleme; küçük coin maliyetiyle kalıcı kozmetik.            |
| 💡 **Taslak**  | 013 | [Tezgah Yoğunluğu ve Stall QoS](./features/013-merchant-density-and-stall-qos.md)    | Tezgah yoğunluğu yönetimi ve görüntüleme kuyruğu (60s görüntüle, 60s blacklist).       |

---

## 🛠️ Nasıl Çalışır?

Her bir özellik önerisi, aşağıdaki yapıya uygun olarak `features/` klasörü altında kendi `.md` dosyasında detaylandırılmıştır:

1.  **Giriş ve Amaç:** Özelliğin hangi sorunu çözdüğü ve neyi hedeflediği.
2.  **Temel İşleyiş:** Sistemin çekirdek mekaniklerinin adım adım anlatımı.
3.  **Kullanıcı Arayüzü (UI/UX) Önerileri:** Oyuncunun göreceği ekranların ve etkileşimlerin tasviri.
4.  **İstisnai Durumların Yönetimi (Edge Cases):** Sistemin potansiyel açıklarının ve sorunlarının nasıl çözüleceğinin analizi.
5.  **Ekonomik ve Sosyal Etkiler:** Özelliğin oyun ekonomisine ve topluluğa olan potansiyel etkileri.

Şablon için bkz: [features/FEATURE_TEMPLATE.md](./features/FEATURE_TEMPLATE.md).

## 💬 Katkı ve Geri Bildirim

Bu projeler hakkındaki görüşleriniz, önerileriniz ve eleştirileriniz son derece değerlidir. Geri bildirimde bulunmak için:

1.  İlgili özellik hakkında bir **"Issue"** açabilirsiniz.
2.  Mevcut bir öneriyi geliştirmek veya yeni bir öneri sunmak için bir **"Pull Request"** oluşturabilirsiniz.

Katkı süreçleri için ayrıntılar: [CONTRIBUTING.md](./CONTRIBUTING.md).

## ⚖️ Lisans

Bu depodaki tüm fikirler ve tasarımlar [MIT License](./LICENSE) altında lisanslanmıştır.
 
