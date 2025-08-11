Merhabalar 

Benzer konuyu oyunun forumunda açmıştım fakat tekrar kontrol ettiğimde konunun kaldırıldığını gördüm. Oysa konuda herhangi bir illegallikten veya ilişkili olduğu rezilliklerden bahsetmemiştim..

Neyse, benim meramım oyundaki taksi hizmetinin ölçülebilir hale getirilip taksi pt arayan ve taksi exp/np sağlayan kişilerin kullanabileceği oyunla entegre çalışan bir sistemin yapay zeka destekli bir sunumuydu. Oradan ambargo yediğim için şansımı frmtr de denemek istedim fakat orada da konu silindi.
> # Proje Tasarımı: "Gri Pazarı" Bitirecek, Veri Odaklı ve Güvenli Kontrat Piyasası
>
> **Konu:** Oyuncu Ticaretini Kökten Değiştirecek, Kapsamlı Kontrat Sistemi Önerisi
>
> Sayın Yöneticiler, Değerli Geliştirici Ekibi ve Oyuncu Arkadaşlar,
>
> Yıllardır oyunumuzun bir parçası olan hizmet alım-satımı (taksi, reb için veya Rank için NP, görev yardımı vb.), maalesef şeffaflıktan uzak, güvene dayalı ve çoğu zaman hayal kırıklığıyla sonuçlanan bir **"gri pazar"** üzerinde işliyor. Bu durum, hem emeğiyle bir şeyler yapmaya çalışan dürüst oyuncuları mağdur ediyor hem de oyunun sosyal dokusuna zarar veriyor.
>
> Bu sorunu kökten çözmek ve bu güvensiz yapıyı ortadan kaldırmak için, üzerinde uzunca düşündüğüm; teknik, kalite güvence (QA) ve oyuncu deneyimi bakış açılarını birleştiren, **iki yönlü, adil ve veri odaklı bir hizmet piyasası** projesini sizlerle paylaşmak istiyorum.
>
> ## 1. Temel Vizyon: "Gri Pazardan" Resmi ve Güvenli Piyasaya
>
> Vizyonumuz, oyuncuların hem hizmet talep edebildiği hem de kendi hizmetlerini sunabildiği, tam entegre bir pazar yeri yaratmaktır.
>
> - **Müşteri İlanı (Hizmet Almak İsteyen):** Bir oyuncu, *"10 Milyar EXP'ye 4 GB (400m) ödül"* veya *"20k National Point (NP) için 1 GB (100m) ödül"* gibi bir ilan açar. Ödül, anında sistemin **güvenli emanet hesabına** aktarılır.
> - **Hizmet Sunan İlanı (Hizmet Vermek İsteyen):** Bir oyuncu, *"Partinizde 3 günde 10 Milyar EXP hedefini 4 GB (400m) karşılığında tamamlarım"* diye kendini pazarlayan bir ilan açar. Bir müşteri onu "kiralar" ve ödül yine **güvenli emanet hesabına** geçer.
>
> Bu emanet sistemi, dolandırıcılığı temelden engeller.
>
> ## 2. Sistemin Kalbi: Ölçülebilir ve Şeffaf Hizmet
>
> Sadece güven değil, aynı zamanda şeffaflık da sağlamalıyız.
>
> > Oyunumuzun başarı (achievement) sistemi, sunucu tarafında zaten birçok veriyi tutuyor. Kontrat aktifken Hizmet Sunan Karakter'in partide olduğu sürece kesilen yaratık sayısı gibi veriler, bu sistem için mükemmel ve hazır bir altyapı sunuyor.
>
> Hedef Türleri: **EXP/NP Kazanımı, Belirli Bir Yaratıktan Kesilen Adet, Görev Eşyası Toplama.**
>
> ## 3. Gelişmiş Şeffaflık: Kontrat Performans Paneli
>
> Bu, sistemin devrim niteliğindeki özelliğidir. Müşteri, parasının karşılığını alıp almadığını anlık olarak görebilir:
>
> - **Zaman Ekseni Grafiği:** Saatlik bazda kazanılan EXP/NP'yi gösteren bir grafik. Grafikteki düşüşler, performans sorununu anında belli eder.
> - **Ölüm Sayacı:** Hizmet Sunan Karakter'in kontrat boyunca kaç kez öldüğünü gösterir.
> - **Ortalama Performans Metriği:** Sistemin hesapladığı ortalama "EXP/Saat" değeri.
> - **Aktivite Durumu:** EXP akışının uzun süre durması durumunda sistemin bunu "Pasif Zaman" olarak işaretlemesi.
>
> Bu panel, iyi hizmet veren oyuncuların kalitesini kanıtlaması için bir vitrin görevi görür.
>
> ## 4. Adalet Mekanizması: Kapsamlı Durum Yönetimi (QA Gözüyle)
>
> <details>
> <summary>Potansiyel Sorunlar ve Çözüm Önerileri (Tüm Detaylar)</summary>
>
> **Kontrat Erken Sonlandırılırsa:** Taraflar **karşılıklı anlaşarak** tamamlanan iş oranında ödeme yapabilir. Anlaşma olmazsa, tek taraflı fesheden taraf (eğer bir ihlal yoksa) haklarından feragat eder.
>
> **Kötü Niyetli Sabotaj:** Müşteri, Hizmet Sunan Karakter'i hedefe yakınken partiden atarsa, bu net bir **kontrat ihlalidir**. Emanetteki ödülün tamamı, anında Hizmet Sunan Karakter'e ödenir.
>
> **Yanıt Vermeme (AFK Kalma):** Anlaşma sağlandıktan sonra Müşteri party kurmazsa, Hizmet Sunan Karakter 30 dakika sonra kontratı **cezasız iptal etme hakkına** sahip olur.
>
> **Piyasa Manipülasyonu:** Sahte ilanlarla piyasayı doldurmayı engellemek için, her oyuncunun aynı anda sadece **bir adet "Hizmet Teklifi"** ilanı açabilmesine izin verilir.
>
> **Teknik Sorunlar ve Ban Durumu:** Sunucu bakımı veya bağlantı kopması durumunda ilerleme kaydedilir, kontrat kaldığı yerden devam eder. Süre limitleri duraklatılır. Taraflardan biri yasaklanırsa, kontrat iptal edilir ve emanetteki para her zaman Müşteri'ye iade edilir.
> </details>
>
> ## 5. Oyuncu Deneyimi: Sistemi "Yaşayan" Kılan Özellikler
>
> - **İtibar Her Şeydir (Puanlama ve Yorum Sistemi):** Her tamamlanan kontrat sonunda, taraflar birbirlerine 1-5 yıldız arası puan vermeli ve kısa bir yorum bırakabilmelidir.
> - **Mola Hakkı (Duraklatma Özelliği):** Uzun kontratlarda, tarafların karşılıklı onayıyla kontratın günde belirli bir süre için duraklatılabilmesi gerekir.
> - **Geçmiş Kontratları İnceleme:** Bir oyuncuyla anlaşmadan önce, onun profilinden daha önceki kontratlarındaki başarı oranını ve aldığı yorumları görebilmeliyiz.
>
> ## 6. Ekonomik Etki: Oyunun Sağlığı İçin
>
> - **Platform Hizmet Bedeli:** Tamamlanan her kontratın ödülünden, Pazar'daki gibi **%3'lük bir komisyon** kesintisi yapılır.
> - **"Coin Sink" Mekanizması:** Bu kesilen miktar, piyasadaki altın miktarını dengelemek ve enflasyonu kontrol altında tutmak amacıyla sistem tarafından oyundan silinir veya mevcut **Pazar Vergi Fonu'na aktarılır.**
>
> Bu, oyun para biriminin değerini korur ve sağlıklı bir ekonomik döngü yaratır.
>
> ## Sonuç
>
> Bu veri odaklı piyasa modeli, oyuncu ticaretindeki tehlikeli "gri pazarı" ortadan kaldıracak ve yerine şeffaf, güvenli ve hesap verebilir bir sistem getirecektir. Bu sistem, oyunculara sadece iş yapma değil, aynı zamanda **somut verilerle kanıtlanmış bir itibar inşa etme** ve "Hizmet Sağlayıcılığı"nı oyunda geçerli bir meslek haline getirme imkanı sunarak oyunumuzun sosyal ve ekonomik dokusunu kökten güçlendirecektir.
>
> Bu projenin hayata geçirilmesinin, tüm oyuncu topluluğu için stratejik bir başarı olacağına inanıyorum.
>
> Saygılarımla,
>

---

# Ek: Yapısal Tasarım Ayrıntıları

Bu bölüm, öneriyi uygulamaya dönük teknik/ürün iskeletiyle tamamlar. Şablon için bkz: `features/FEATURE_TEMPLATE.md`.

## 1) Durum Makinesi (Contract Lifecycle)

- Draft → Funded (Escrow) → Active → Paused → Completed → Disputed → Settled/Cancelled
- Geçiş Kuralları (örnekler):
  - Funded: Müşteri ödülü emanet cüzdana aktarır, sözleşme kilitlenir.
  - Active: Parti kurulur ve hizmet sağlayıcı katılır; telemetri akışı başlar.
  - Paused: Karşılıklı onay ile saatlik limitlerde duraklatma.
  - Completed: Hedef metrikleri karşılandığında otomatik; aksi halde tarafların mutabakatıyla manuel.
  - Disputed: Kural ihlali iddiası, kayıtlı telemetri ve durum logları üzerinden çözülür.
  - Settled/Cancelled: Sonlandırma ve ücret tahsisi kuralları uygulanır (komisyon, iade vb.).

## 2) Veri Modeli (Örnek)

- Contract
  - id, creatorId, providerId, type (exp|np|kill|collect), targetValue, deadline, status
  - rewardAmount, currency, escrowId, createdAt, updatedAt
- Escrow
  - id, contractId, amount, feeRate, state (locked|released|refunded), operations[]
- PerformanceSnapshot
  - contractId, ts, expDelta, npDelta, killsDelta, deathsDelta, activityFlag (active|idle)
- Reputation
  - userId, score, decayRate, ratings[], reviews[]

İlişkiler: `Contract.escrowId -> Escrow.id`, `PerformanceSnapshot.contractId -> Contract.id`.

## 3) API Taslakları

- POST /contracts
  - body: { type, targetValue, rewardAmount, deadline }
- POST /contracts/{id}/fund
- POST /contracts/{id}/start
- POST /contracts/{id}/pause
- POST /contracts/{id}/resume
- POST /contracts/{id}/complete
- POST /contracts/{id}/dispute
- GET  /contracts/{id}/performance?from=...&to=...

Yanıtlar; durum, kalan hedef, saatlik performans, ücret/komisyon kırılımları içerir.

## 4) Güvenlik ve Kötüye Kullanım Önlemleri

- Sahte performans şişirme: Partide bulunma, aktivite, konum ve düşman kesim korelasyonu.
- Parti atma istismarı: Hedefe yakın atma → ihlal; otomatik tespit ve sağlayıcı lehine tahsis.
- Spam ilan: Eşzamanlı ilan limiti, ilan başına küçük depozito, oran limiti.
- AFK: Uzun pasiflikte otomatik uyarı, tekrarında sözleşme fesih kuralları.

## 5) İzleme ve Telemetri

- Metrikler: exp/hour, np/hour, idle ratio, death count, completion ratio, dispute rate.
- Loglar: Durum geçişleri, parti olayları, escrow işlemleri, anomali işaretleri.
- Paneller: Zaman serisi grafikleri, sözleşme durumu, sağlayıcı vitrin skoru.

## 6) Test Planı (Kısa)

- Birim: durum makinesi geçişleri, komisyon hesapları.
- Entegrasyon: escrow → performans → tamamlama → ödeme.
- E2E: ilan oluşturma, fonlama, başlatma, duraklatma, tamamlama.
- Yük: performans akışı (snapshot/sa), eşzamanlı sözleşme.
