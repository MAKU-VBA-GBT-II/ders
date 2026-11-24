# VBA II — Vize Değerlendirme Rubriği

Vize notu **125 puanlık** çatı üzerinden hesaplanır: **Ana görevler 100 puan + Yan görevler 25 puan.**

- **Vize notu = toplam puan.** Yan görevler ek puan niteliğindedir; 100'ü aşan toplamlar **100** sayılır.
- Yuvarlama en yakın tam sayıya yapılır (`0,5` yukarı).
- H2 ısınma alıştırması puanlanmaz. Görev 3 / Çok Ajanlı Şirket Programı finalde değerlendirilir.

---

## Puan Çatısı

| Kalem | Tür | Puan |
|---|---|---:|
| Görev 1 — Sektörde mini veri hattı (Hafta 3–4) | Ana | 40 |
| Görev 2 — Şirket mini ürünü (Hafta 5–6) | Ana | 45 |
| Dönem Raporu 1 (Duyuru 7, Bölüm 2) | Ana | 15 |
| **Ana görevler toplamı** | | **100** |
| Yan Görev 1 — Git keşfi raporu | Yan | 5 |
| Yan Görev 2 — Keşfedilen reponun derste sunumu | Yan | 5 |
| Yan Görev 3 — Çapraz skill incelemesi | Yan | 5 |
| Yan Görev 4 — TÜBİTAK 2209-A başvurusu | Yan | 10 |
| **Yan görevler toplamı** | | **25** |
| **GENEL TOPLAM** | | **125** |

---

## Genel Kurallar

1. **Yalnızca iz puanlanır:** Puan depodaki dosya, commit, Issue/PR yorumu ve zaman damgasına göre verilir (Yan Görev 2'de ders sonrası Issue/yorum sunum bildirimi esas alınır).
2. **Zaman çarpanı (yalnız ana görev grup puanlarına uygulanır):** Son tarihte teslim `%100`, son tarihten sonra `%75`, teslim yok `%0`. Geç release durumunda yalnızca zaman çarpanı uygulanır; release maddesi ayrıca çift cezalandırılmaz.
3. **Grup puanları** gruptaki tüm üyelere aynı yansır; kısmi puan uygulanır.
4. **Kanıt şartı:** Dosya olup kanıt yorumu olmayan ya da yorum olup dosyası olmayan maddeler tam puan almaz.
5. **Aynı iş iki görevde sayılmaz:** Önceki görevde teslim edilen işlerin sonraki görevin teslimi gibi sunulması puan getirmez.
6. **Rol esası:** Her üye, ilgili görevdeki kendi rolünün maddelerinden puan alır.
7. **Kopya / intihal:** Başka bir grubun veya öğrencinin dosyasını/skill'ini birebir kopyalama durumunda ilgili madde(ler) **0** puanlanır ve genel toplamdan ek **−10 puan** ceza kesilir.
8. **Kalite bandı (G1-9, G2-9, DR-5):** İşin haftaya yayılması (son gece tek commit olmaması), dosya/commit adlarının açıklayıcılığı, somut gerekçeli inceleme yorumları ve varsayım/kaynakların yazılması değerlendirilir.
9. **Force-push koruması:** Bir üyenin son tarihten önce commit'lediği ancak başka bir üyenin `force-push` işlemiyle `main` dalından silinen iş, git geçmişinde doğrulandığında ilgili maddelerde geçerli sayılır.

---

## Görev 1 — 40 puan

### Grup puanları (24 puan — zaman çarpanı uygulanır)

| # | Madde | Tam | Kısmi | Yok |
|---|---|---:|---|---:|
| G1-1 | `gorev1-final` release'i son tarihte mevcut | 4 | Release var, adı yanlış (2) | 0 |
| G1-2 | Sektör verisi + şema: `data/*.csv` ≥100 satır, ≥6 alan, ≥4 kategori değeri; `docs/veri-sozlugu-g1.md` tam | 5 | Biri eksik (2,5) | 0 |
| G1-3 | `docs/analiz-g1.md`: ≥5 metrik (toplam + ortalama + 2 kırılım + top-N), her metriğe 1–2 cümle yorum, bulgular (3 gözlem + 1 eylem) | 5 | Metrikler tam / bulgular eksik veya tersi (2,5) | 0 |
| G1-4 | Devir teslim zinciri: 4 halka (BE→DQ, DQ→FE, FE→DQ test, DQ→PM) — yazılı yorum + alıcı çıktısı girdiyi kullanmış | 6 | Halka başına 1,5 (eksik halka −1,5) | 0 |
| G1-5 | Test turu: `tests/test-cases.md` ≥5 senaryo + `tests/test-log.md` dolu + ≥2 bug/enhancement Issue + `Fixes #n` commit'i | 4 | 2–3 kalem (2) | ≤1 kalem: 0 |

### Bireysel puanlar (16 puan)

| # | Madde | Tam | Kısmi | Yok |
|---|---|---:|---|---:|
| G1-6 | Rol teslimatı kabul kriterini karşılıyor | 6 | 1 kalem eksik (4) · 2+ eksik (1,5) | 0 |
| G1-7 | Kişisel skill (`skills/<rol>-<iş>/SKILL.md`): amaç + adım adım talimat + dosyalar/çalıştırma tam; çıktı skill ile üretilmiş | 5 | İçerik eksik veya üretim izi yok (2,5) | 0 |
| G1-8 | Kişisel iz: ≥2 commit + üstlendiği Issue'lar kanıt yorumuyla kapalı + kapanışta "hangi skill, hangi araç" satırı | 2 | 2/3 kalem (1) | ≤1: 0 |
| G1-9 | **İş kalitesi** (rol bazlı ölçütler) | 3 | İyi (2) · Asgari (1) | Özensiz / kopya: 0 |

---

## Görev 2 — 45 puan

### Grup puanları (24 puan — zaman çarpanı uygulanır)

| # | Madde | Tam | Kısmi | Yok |
|---|---|---:|---|---:|
| G2-1 | `gorev2-final` release'i + milestone açılmış ve kapatılmış | 3 | Biri eksik (1,5) | 0 |
| G2-2 | PR disiplini: `main`'e doğrudan commit yok; ≥2 merge edilmiş PR; kod/veri PR'larında somut inceleme yorumları ve Approve | 6 | PR var, inceleme yüzeysel / onaysız kod PR'ı / doğrudan commit var (3) | PR yok: 0 |
| G2-3 | Ürün: ≥2 parametreli simülasyon (3) + hata yönetimi (2) + 3 grafik (zaman serisi, kırılım, dağılım; başlık/eksen/birim) (4) | 9 | Alt kalem başına yarım (1,5 / 1 / 2) | 0 |
| G2-4 | Belgeler: `docs/veri-sozlugu.md` (2) + `docs/analiz-g2.md` (5 metrik + 3 gözlem + 1 eylem) (2) + `docs/requirements.md` (2) | 6 | Belge başına yarım (1) | 0 |

### Bireysel puanlar (21 puan)

| # | Madde | Tam | Kısmi | Yok |
|---|---|---:|---|---:|
| G2-5 | Rol teslimatı kabul kriterini karşılıyor | 8 | 1 kalem eksik (5) · 2+ eksik (2,5) | 0 |
| G2-6 | Kişisel rol skill'i: amaç + çıktı formatı + 1 örnek giriş/çıkış + reddetme koşulları; PR/Issue'da üretim ve prompt özeti izi | 5 | 2 kalem eksik veya üretim izi yok (2,5) | 0 |
| G2-7 | Kapanış disiplini: 5 Kasım 23:59'da açık Issue yok *(Duyuru 7 m.2 "Ertelendi + tarih" gerekçeli kapatma geçerli; işsiz ve gerekçesiz sessiz kapatma sorumlu kişi/PM için açık sayılır; Görev 2 hiç yapılmamışsa 0)* | 2 | 1–2 açık / gerekçesiz kapatma (1) | ≥3 açık veya görev yok: 0 |
| G2-8 | Kişisel iz: ≥2 commit + üstlendiği Issue'lar kanıt yorumuyla kapalı | 2 | Kısmi (1) | 0 |
| G2-9 | **İş kalitesi** (rol bazlı ölçütler) | 4 | İyi (3) · Asgari (1) | Özensiz / kopya: 0 |

---

## Dönem Raporu 1 — 15 puan

### Grup puanları (11 puan — zaman çarpanı uygulanır)

| # | Madde | Tam | Kısmi | Yok |
|---|---|---:|---|---:|
| DR-1 | Raporda 7 bölümün tamamı (yönetici özeti, teslim edilenler, sayılarla dönem, tıkananlar, kim ne yaptı, dersler, Görev 3 hazırlığı) | 4 | 5–6 bölüm (3) · ≤4 bölüm (1,5) | 0 |
| DR-2 | Süreç KPI'ları: açılan/kapatılan Issue, merge edilmiş PR, PR başına ortalama ilk yorum süresi, üye bazında commit + kapatılan Issue, geciken iş | 2 | 3–4 kalem (1) | ≤2 kalem: 0 |
| DR-3 | Teslim izi: `reports/donem-raporu-1.md` + `@eofdred` etiketli "Dönem Raporu 1 teslim" Issue'su | 1 | Dosya var, bildirim Issue'su yok (0) | 0 |
| DR-4 | `pm-rapor` skill'i ile üretim + sonunda prompt/araç özeti | 2 | Biri (1) | 0 |
| DR-5 | **Rapor kalitesi:** olgusal dil, kanıt linkleri, tablo düzeni, ~1 sayfa + tablolar | 2 | İyi (1) | Özensiz / gerçeğe aykırı beyan: 0 |

### Bireysel puan (4 puan)

| # | Rol | Tam | Kısmi | Yok |
|---|---|---:|---|---:|
| DR-6 | Üye: PM'e 3 yanıtını verdi (ne teslim ettim + kanıt, neye takıldım, sonraki dönem hedefi) | 4 | 2 yanıt (2,5) · 1 yanıt (1) | 0 |
| DR-6 | PM: üyelerden toplama izi + kendi 3 yanıtı + imza | 4 | Toplama izi veya kendi yanıtlarından biri eksik (2,5) | 0 |

---

## Kalite Bandı Ölçütleri (G1-9, G2-9, DR-5)

| Rol | Tam puan | Orta | Asgari |
|---|---|---|---|
| **BE** | Okunabilir kod (anlamlı isimler, fonksiyon ayrımı), parametreler belgeli, commit'ler haftaya yayılmış | Bir kalem eksik | Çalışıyor ama tek blok / tek commit, açıklama yok |
| **FE** | Grafiklerde başlık + eksen + birim, okunabilir renk, açıklayıcı dosya adı, taslak (mockup) ile tutarlı | Bir kalem eksik | Grafik var; etiketler eksik veya taslak atlanmış |
| **DQ** | Analizde formül + yorum, geniş test kapsamı, dosya/satır gösteren inceleme yorumları | Bir kalem eksik | Tablo var yorum yok; inceleme yüzeysel |
| **PM** | Kabul kriterli Issue'lar, pano hijyeni, koordinasyon izi, olgusal ve açık raporlama | Bir kalem eksik | Şablonsuz Issue'lar, güncellenmemiş pano |

> Ortak ölçüt: İş son gece tek commit ile geldiyse kalite bandı en çok "asgari" düzeyinde değerlendirilir.

---

## Yan Görevler — 25 puan

### YG1 — Git keşfi raporu (5 puan)

| Madde | Tam | Kısmi | Yok |
|---|---:|---|---:|
| Konum: `reports/yan-gorev-1/kesif-<ad>.md` | 1 | Yanlış yolda (0) | 0 |
| İçerik: repo adı + link; çözdüğü problem (2–3 cümle); 2–3 güçlü yan; kendi projesinde kullanacağı 1 fikir | 3 | Bölüm başına 0,75 (eksik bölüm −0,75) | 0 |
| Zaman: 14 Ekim 23:59 | 1 | Geç (0) | 0 |

### YG2 — Derste sunum (5 puan)

| Madde | Tam | Kısmi | Yok |
|---|---:|---|---:|
| 22 Ekim dersinde sunum (~2 dk + soru-cevap) ve ders sonrası Issue/yorum bildirimi *(ders öncesi hazırlık yorumu sunum bildirimi sayılmaz)* | 3 | Kısa / geçiştirilmiş (2) | 0 |
| İçerik: repo ne işe yarıyor + kim geliştiriyor / ilginç bulgu / neden seçildi + ne öğrenildi | 2 | Başlık başına ~0,67 | 0 |

> YG1'i yapmayan ancak derste sunum yapıp bildiren öğrenci YG2'den tam puan alır (Duyuru 4 telafi hükmü), YG1'den 0 alır.

### YG3 — Çapraz skill incelemesi (5 puan)

| Madde | Tam | Kısmi | Yok |
|---|---:|---|---:|
| Hedef: eşleştiği şirketin, kendi rolünün skill'i | 1 | Yanlış skill (0) | 0 |
| Kayıt: karşı repoda `Skill incelemesi: <skill adı> (<Adın>, Grup X)` başlıklı Issue *(karşı repoda etiket yetkisi olmadığından `enhancement` etiketi aranmaz)* | 1 | Başlık formatı eksik/bozuk (0,5) | 0 |
| İçerik: 1 güçlü yan + 1 eksik + 1 somut öneri (dosya/satır göstererek) | 2 | 2/3 madde (1) · genel ifadeler (0,5) | 0 |
| Zaman: 27 Ekim 23:59 | 1 | Geç (0) | 0 |

### YG4 — TÜBİTAK 2209-A başvurusu (10 puan)

Önce 0–10 arası **temel puan** hesaplanır, ardından rol katsayısı uygulanır.

| Madde | Tam | Kısmi | Yok |
|---|---:|---|---:|
| Başvuru: TYBS'de doldurulmuş ve danışman onayına gönderilmiş / onaylanmış, ekran görüntüsüyle kanıtlı | 4 | Taslak / onaya gönderilmemiş (2) | 0 |
| Kayıt: grup reposunda `Yan Görev 4: TÜBİTAK 2209-A başvurusu (<ad>)` Issue'su + proje başlığı + danışman adı | 2 | Eksik kalem başına −0,7 | 0 |
| PDF: `TÜBİTAK/<ad-soyad>.pdf` grup reposunda + `@eofdred` etiketli Issue'da link *(başvuru formunun PDF dışı görsel/dosya hâli 1,5; yalnızca TYBS durum tablosu ekran görüntüsü Başvuru kanıtıdır, PDF maddesi sayılmaz)* | 3 | PDF var, Issue yok (1,5) · PDF yerine başvuru formunun başka dosya formatı (1,5) | 0 |
| Zaman: başvuru ve akademik danışman onayı son tarih (`23 Kasım 2026 17:30`) öncesi *(geç yüklenen PDF zaman puanını kırmaz)* | 1 | — | 0 |

**Rol katsayıları:**

| Durum | Katsayı | Tam puanda (10 üzerinden) |
|---|---:|---:|
| Tek başına başvuru (yürütücü, ortak yok) | %100 | 10 |
| Ekipli başvuruda yürütücü | %80 | 8 |
| Ekipli başvuruda yardımcı / ortak (her biri) | `%60 ÷ yardımcı sayısı` | 2 yardımcı → 3 · 3 yardımcı → 2 |
| Aynı öğrenci birden çok başvuruda | En yüksek puan sayılır, toplanmaz | Tavan 10 |
