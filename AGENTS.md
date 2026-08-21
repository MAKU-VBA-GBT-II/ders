# AGENTS.md — VBA2 çalışma alanı

Bu klasör, VBA II (Veri Bilimi ve Analitik) dersinin planlama çalışma alanıdır. GitHub: `MAKU-VBA-GBT-II` organizasyonu (grup repoları + `ders` merkezi repo).

## Açık Görevler (hatırlatılması gerekenler)

- **Tarih placeholder'ları doldurulacak:** `is-ilanlari.md` ve `vba2-donem-plani.md` içindeki `<İLAN TARİHİ>`, `<BAŞVURU SON TARİHİ>`, `<SEÇİM GÜNÜ>`, `<TESLİM GÜNÜ/SAATİ>`, `<ARA TESLİM GÜNÜ/SAATİ>` ve `<KOD DONDURMA GÜNÜ>` placeholder'ları dönem başlamadan önce gerçek değerlerle doldurulacak. Kullanıcı "yapılacak bir şey var mı?" diye sorarsa veya başka bir iş yaparken bunu hatırlat.
- Hafta 5 başında her grup reposunda `main` branch protection açılacak (aşağıdaki plan §3 kural 5).

## Önemli dosyalar

- `vba2-donem-plani.md` — dönem planının Obsidian kopyası (aynı içerik)
- `ders/AGENTS.md` — bu dosyanın `ders` reposundaki yayını (GitHub'da, öğrenciler görür). **Senkron kuralı:** Plan her değiştiğinde üç kopya birden güncellenmeli: `AGENTS.md` ↔ `vba2-donem-plani.md` ↔ `ders/AGENTS.md` (sonuncusu commit + push gerektirir).
- `ders/is-ilanlari.md` — 6 proje lideri iş ilanı (GitHub'da)
- `group-a` … `group-f` — öğrenci repolarının lokal kopyaları

## Dönem Planı (tam metin)
# VBA II — Veri Şirketi Simülasyonu Dönem Planı
**VBA = Veri Bilimi ve Analitik · 6 Şirket × 5 Öğrenci = 30 Öğrenci · 15 Hafta · GitHub Tabanlı Ekip Çalışması**

> **TAKVİM NOTU:** Bu belgedeki takvim tarihleri henüz belirlenmemiştir; yerlerinde `<...>` placeholder'ları vardır ve dönem başlamadan önce ekleneceklerdir:
> - `<İLAN TARİHİ>` · `<BAŞVURU SON TARİHİ>` · `<SEÇİM GÜNÜ>` — iş ilanı takvimi (§1.4)
> - `<TESLİM GÜNÜ/SAATİ>` — haftalık rapor ve iş teslimlerinin varsayılan son tarihi (öneri: Pazar 23:59)
> - `<ARA TESLİM GÜNÜ/SAATİ>` — Görev 3 veri değişimi ara teslimi (Hafta 8)
> - `<KOD DONDURMA GÜNÜ>` — büyük proje kod dondurma günü (Hafta 14)
>
> Belgedeki tüm boş tarihleri `<` karakterini arayarak bulabilirsiniz.

---

## 0.1 Açık Görevler (TODO)

- [ ] **Tarih placeholder'larını doldur:** Yukarıdaki takvim notunda listelenen tüm `<...>` placeholder'ları dönem başlamadan önce gerçek değerlerle doldurulacak. Kapsam: `is-ilanlari.md` ve lokal `vba2-donem-plani.md`.
  - [ ] İsteğe bağlı: dönem haritasındaki hafta aralıklarının akademik takvime eşlenmesi (H1 = hangi tarih … H15 = hangi tarih)

---

## 0. Dersin Bağlamı ve Bu Plan Nasıl Çalışır

**Birinci dönemde ne yaptık:** Her öğrenci bireysel çalıştı — simülasyonlar kurdu, değişkenlerle oynayıp veri üretti, üretilen veriyi analiz etti ve görselleştirdi. Ödevler GitHub üzerinden toplandı; notlandırma eşik esaslıydı (eşiklerin hepsi geçilmezse puan 0).

**Bu dönem ne yapacağız:** Öğrenciler 5'er kişilik "veri şirketlerine" bölünür. Her şirkette biri veriyi **üretir** (backend), biri **analiz eder** (veri analisti), biri **görselleştirir** (frontend), biri **sınar ve belgeler** (QA), biri **yönetir** (PM). Aralarındaki **veri akışı** — kimin ürettiği veriyi kimin aldığı, hangi formatta teslim ettiği, karşılıklı sözleşmelere uyulup uyulmadığı — **notlandırmanın parçasıdır** ve hepsi GitHub'da iz olarak kaydedilir.

**Teknoloji serbest:** Programlama dili zorunluluğu yoktur. Her şirket, birinci dönemde öğrendiklerinden (Python, Jupyter, pandas, matplotlib vb.) kendi tercihini yapar ve Hafta 1'de README'ye yazar. Tek kural: **veri dosyaları CSV/JSON gibi açık, makinece okunabilir formatlarda** olur.

**Kurallar:**
1. Her hafta için her role ayrı, numaralı talimatlar verilmiştir. Öğrenci önce o haftaki rolünü Rol Rotasyon Matrisi'nden (§1.3) bulur, sonra kendi rolünün talimatlarını uygular.
2. GitHub terimleri (Issue, Pull Request, commit vb.) İngilizce bırakılmıştır; anlamı ve nasıl yapılacağı §2'deki sözlükte anlatılmıştır. Anlamadığınız terimde önce §2'ye bakın.
3. Her talimat kontrol edilebilir bir çıktı üretir: ya depoda (repository) vardır ya da yoktur. Notlandırma bu izlere göre yapılır.
4. Belgede geçen "Görev 1 / Görev 2 / Görev 3" dönemin üç küçük ekip görevidir; commit ve etiketlerde kısaltma olarak `gorev1`, `gorev2`, `gorev3` kullanılır.

**Dönem haritası (tek bakışta):**

| Haftalar | Aşama | Teslim (release) |
|---|---|---|
| H1 | Şirket kuruluşu: lider iş ilanı + başvurular, hesaplar, araçlar, teknoloji kararı, ilk commit | — |
| H2 | İş akışı provası (Issue döngüsü + mini veri üretimi) | — |
| H3–4 | **Görev 1** — Şirket sektöründe Mini Veri Hattı | `gorev1-final` |
| H5–6 | **Görev 2** — Şirket Mini Ürünü (**PR kuralı başlar**) | `gorev2-final` |
| H7–8 | **Görev 3** — B2B Veri Değişimi (partner şirketle sözleşmeli veri alışverişi) | `gorev3-final` |
| Ara sınav haftası | Vize: bireysel sınav (%60) + süreç notu (%40) | — |
| H9–15 | **Büyük Proje** (H11: Kilometre Taşı 1 · H13: Kilometre Taşı 2 · H14: kod dondurma · H15: demo) | `final` |

---

## 1. Şirket Yapısı

### 1.1 Şirketler ve Sektörleri

Her grup simüle edilmiş bir veri şirketidir. Hafta 1'de her grup kendine bir şirket adı seçer; o zamana kadar harfle anılır. Her şirketin **bir sektörü** vardır — Görev 2 ve Büyük Proje bu sektörün verisi üzerine kurulur. Sektörler, Görev 3'teki veri değişiminin anlamlı olması için eşleştirilmiştir.

| Şirket | Öğrenciler (liste sırasına göre) | Sektör | Görev 2 Mini Ürünü | Büyük Proje (H9–15) |
|---|---|---|---|---|
| **A** | 1–5 | E-ticaret | Sipariş akışı simülasyonu + ürün bazlı satış grafikleri | E-ticaret Satış Analiz Platformu |
| **B** | 6–10 | Lojistik | Sevkiyat simülasyonu + teslimat süresi grafikleri | Lojistik Takip ve Analiz Sistemi |
| **C** | 11–15 | Bankacılık | Banka işlemi simülasyonu + müşteri özet grafikleri | İşlem Analizi ve Anomali Tespit Aracı |
| **D** | 16–20 | Sigorta | Sigorta talebi simülasyonu + prim/ödeme grafikleri | Talep Analizi ve Risk Raporlama Sistemi |
| **E** | 21–25 | Perakende | Mağaza satış simülasyonu + stok grafikleri | Perakende Satış ve Stok Analiz Aracı |
| **F** | 26–30 | Tedarik | Tedarik siparişi simülasyonu + stok seviyesi grafikleri | Tedarik Zinciri İzleme Sistemi |

**Gruplar arası veri değişim eşleşmeleri (Görev 3):** A↔B (siparişler → sevkiyatlar), C↔D (banka işlemleri → sigorta ödemeleri), E↔F (mağaza satışları → tedarik siparişleri).

### 1.2 Roller

| Kod | Rol | Görev tanımı |
|---|---|---|
| **PM** | Proje Yöneticisi | Panonun, takvimin ve haftalık raporun sahibidir. Görevleri Issue olarak açar, atar, takip eder; işlerin zamanında bitmesini sağlar. Kendisi merge yapmaz; başkalarının doğru şekilde yapmasını sağlar. |
| **BE** | Backend / Veri Üretici | Verinin üretildiği kodun sahibidir: simülasyon betikleri, veri üretimi, dosya okuma/yazma. Ürettiği her veri kümesinin **şemasını** (alan adları, tipler, aralıklar) tesliminden önce yazar. |
| **FE** | Frontend / Görselleştirici | Grafiklerin, dashboard'ların ve kullanıcının gördüğü her çıktının sahibidir. Yalnızca BE'nin ürettiği ve DA'nın tanımladığı veriyi görselleştirir; kendi başına veri üretmez. |
| **DA** | Veri Analisti | Analizin sahibidir: hangi metrikler hesaplanacak, hangi sorular sorulacak, bulgular ne. Her analiz bir belgede (findings) sonuçlanır. |
| **QA** | Test ve Dokümantasyon Mühendisi | Veri kalitesi testlerinin, hata kayıtlarının (bug Issue), PR incelemelerinin ve kullanım kılavuzunun sahibidir. QA onayı olmadan hiçbir şey `main`'e girmez. |

**Veri akışı zinciri** (notlandırmanın omurgası):

```
BE üretir ──veri dosyası──▶ DA analiz eder ──bulgular──▶ FE görselleştirir ──çıktı──▶ QA sınar
```

Her ok bir "devir teslim"dir ve GitHub'da yazılı iz bırakmak zorundadır (§4'te her görevde ayrıntılı).

### 1.3 Rol Rotasyon Matrisi

Her şirkette **proje lideri dönem boyu PM'dir** — öğretim elemanı tarafından dönem başında seçilir (§1.4). PM, kalan 4 üyeyi BE, FE, DA ve QA başlangıç rolleri için açtığı ilanlarla seçer. Her öğrenci Görev 1–3 boyunca üç farklı başlangıç dışı rolü deneyimler; böylece ekip kurma tercihi, rol rotasyonunun öğrenme hedefini ortadan kaldırmaz.

| Başlangıç rolü | Görev 1 (H3–4) | Görev 2 (H5–6) | Görev 3 (H7–8) | Büyük Proje (H9–15) |
|---|---|---|---|---|
| **Lider** | PM | PM | PM | PM (sabit) |
| BE | BE | FE | DA | Hafta 9'da müzakere edilir |
| FE | FE | DA | QA | Hafta 9'da müzakere edilir |
| DA | DA | QA | BE | Hafta 9'da müzakere edilir |
| QA | QA | BE | FE | Hafta 9'da müzakere edilir |

Büyük projede kalan 4 rol (BE, FE, DA, QA) Hafta 9'da grup içi müzakereyle dağıtılır; son dağılımı öğretim elemanı onaylar.

### 1.4 Proje Lideri İş İlanı ve Seçimi (Hafta 1)

Roleplay'in ilk adımı **iki aşamalı işe alım sürecidir**: önce öğretim elemanı 6 proje liderini seçer, sonra her lider kendi şirketinin dört kişilik ekibini kurar.

1. **Lider ilanları (`<İLAN TARİHİ>`):** Öğretim elemanı 6 ilanı yayımlar — her biri bir sektöre bağlıdır (§1.1 tablosu). İlan metninde şirketin sektörü, PM görev tanımı (§1.2) ve aranan nitelikler bulunur.
2. **Lider başvuruları (`<BAŞVURU SON TARİHİ>`'a kadar):** Adaylar öğretim elemanının paylaştığı **Google Form** üzerinden başvurur. Form alanları:
   - Ad-soyad, öğrenci no.
   - Tek cümlelik gerekçe: "Neden bu sektörün proje lideri olmak istiyorsun?" (zorunlu).
   - İsteğe bağlı: birinci dönemden örnek bir çalışma linki (GitHub repo, grafik, ödev).
3. **Lider seçimi (`<SEÇİM GÜNÜ>`):** Öğretim elemanı başvuruları değerlendirir — gerekçenin açıklığı, birinci dönem izleri ve başvurulan sektörle uyum. 6 lider ilan edilir ve sonuçlar grup `README.md`'lerine işlenir.
4. **Ekip ilanları (Hafta 1):** Her PM, BE, FE, DA ve QA için ayrı bir iş ilanı açar. İlanda rolün görevleri, kabul edilecek katkı türü, başvuru yöntemi ve son başvuru zamanı bulunur.
5. **Ekip başvuruları:** Öğrenciler bir veya daha fazla role CV/portföy ile başvurur. CV'ler kamuya açık depoya konmaz; PM ve öğretim elemanı tarafından değerlendirilir.
6. **Ekip seçimi:** PM adayları açıklanmış ölçütlerle değerlendirir, dört üyeyi başlangıç rollerine yerleştirir ve listeyi öğretim elemanının onayına sunar. Her öğrenci bir şirkette yer almalıdır; açıkta kalan adayların son yerleştirmesini öğretim elemanı yapar.
7. **Liderin ilk görevleri (Hafta 1–2):** Şirket adını ekibe önerip oylatmak, teknoloji kararına öncülük etmek ve Hafta 2'de panoyu kurmak.

---

## 2. GitHub Kavramları Sözlüğü

Birinci dönemde GitHub'ı ödev teslimi için kullandınız (clone, commit, push). Bu dönem eklenen iş akışı kavramları:

### 2.1 Issue (İş Kaydı)
Yapılacak işin, hatanın veya kararın **yazılı ve numaralı kaydıdır**. Bu derste "görev vermek" = Issue açıp birine atamak demektir; sözlü veya WhatsApp üzerinden verilen görev **verilmemiş sayılır**.

**Nasıl açılır:** Depo → `Issues` → `New issue` → **Başlık** (örn. `G1-veri — Sektör verisini üret`) → **Açıklama**: ne yapılacak + tek cümlelik kabul kriteri + son tarih → sağ panelden **Assignees** (yapacak kişi) ve **Labels** (`bug`/`enhancement`) → `Submit new issue`.

**Nasıl kapatılır:** İş bitince Issue'nun altına kanıt içeren yorum yazın (örn. "Tamamlandı — commit `a3f9c21`, çıktı: `data/<sektor-verisi>.csv` 100 satır") → `Close issue`. Kanıtsız kapatılan Issue yapılmamış sayılır.

### 2.2 Branch (Dal) ve Pull Request (PR — Birleştirme İsteği)
`main` dalı ürünün çalışan halidir. Yeni özellik geliştirirken `feature/...` dalı açılır; iş bitince PR ile `main`'e katılır. **Hafta 5'ten itibaren `main`'e commit yalnızca PR yoluyla girer.**

**Akış:** dal aç (`feature/veri`) → commit'ler → `Publish branch` → github.com'da `Compare & pull request` → açıklamaya `Closes #5` (bağladığı Issue) → **Reviewers** kısmından QA'yı seç → `Create pull request`. QA inceleyip `Approve` verdikten sonra merge düğmesine PR sahibi basar.

**İnceleme (review):** `Files changed` sekmesinde değişen satırlara yorum yazılır. "LGTM" tek başına inceleme sayılmaz; geçerli yorum somut gözlem içerir: "Bu döngü negatif değer üretebiliyor", "`gun` değişkeni yerine `gun_sayisi` olmalı", "Bu grafikte eksen etiketi yok" gibi.

### 2.3 Label, Milestone, Project Board
- **Label:** Issue'ları sınıflandıran etiket. Zorunlu ikisi: `bug` (hata), `enhancement` (iyileştirme önerisi).
- **Milestone:** Birden çok Issue'yu ortak hedef + bitiş tarihi altında toplar (örn. `Görev 2`). Tüm Issue'lar kapanınca milestone kapatılır.
- **Project Board:** 4 sütunlu pano: `To Do` → `In Progress` → `Review` → `Done`. İşe başlarken kartınızı `In Progress`'e, PR açınca `Review`'a, merge olunca `Done`'a **kendiniz** sürüklersiniz. Panoyu güncel tutmak herkesin işidir.

### 2.4 Tag ve Release (Sürüm Etiketi)
Deponun belirli bir anını "teslim edilen sürüm" olarak mühürler. Her görevin sonunda PM bir release oluşturur (örn. `gorev1-final`); notlandırma bu mühürlü hâl üzerinden yapılır — sonradan yapılan değişiklik o görevin notunu etkilemez. (Depo → `Releases` → `Draft a new release` → tag adını yaz → `Publish release`.)

### 2.5 @Mention ve Bildirimler
Bir Issue/PR yorumunda `@kullaniciadi` yazarsanız o kişiye bildirim gider. **Kural: birinden bir şey bekliyorsanız yorumda mutlaka @mention kullanın.** Depo sayfasında `Watch → All activity` seçin ve her çalışma seansına GitHub bildirimlerinize (zil simgesi) bakarak başlayın. "Yorumu görmedim" geçerli mazeret değildir.

---

## 3. Altyapı Kuralları (Hafta 1'de ilan edilir, pazarlık edilmez)

1. **Tek GitHub organizasyonu:** `MAKU-VBA-GBT-II`; her grubun bir deposu (`group-a` … `group-f`). Öğretim elemanı organizasyonun sahibidir ve her şeyi görür. Depolar herkese açıktır (public) — mezuniyette portföy olarak kullanılabilirler; bu yüzden gerçek kişi verisi (TC no, telefon vb.) asla depoya girmez, tüm veriler simülasyon ürünüdür.

2. **Zorunlu depo yapısı:**

   ```
   /src/               ← kod: simülasyon, analiz ve görselleştirme betikleri (dil serbest)
   /data/              ← üretilen veri dosyaları (.csv, .json)
   /visuals/           ← dışa aktarılmış grafikler (.png)
   /docs/              ← veri-sozlugu.md, requirements.md, user-manual.md
   /tests/             ← test-cases.md (senaryolar), test-log.md (sonuçlar)
   /reports/           ← haftalık sprint raporları: report-w03.md, report-w04.md …
   /exchange/          ← Görev 3 veri değişimi (output.csv vb.)
   ```

3. **"GitHub'da yoksa, yapılmamıştır."** Görev atamaları, veri teslimleri, hata bildirimleri ve tasarım kararları Issue'larda ve Pull Request'lerde yapılır. WhatsApp yalnızca anlık koordinasyon içindir ve asla notlandırılmaz.

4. **Veri teslimi kuralı:** BE'nin ürettiği her veri dosyası, yanında **şemasıyla** teslim edilir: alan adları, tipler, aralıklar, satır sayısı. Şeması olmayan veri teslim edilmemiş sayılır. Şema bilgisi dosyanın commit mesajında veya Issue yorumunda olabilir (büyük projede `docs/veri-sozlugu.md` zorunludur).

5. **Hafta 5'ten itibaren `main`'e yalnızca PR ile girilir.** İnceleyici (reviewer) = QA; PR'ı açan QA ise inceleyici PM olur. Kendi PR'ını kendisi onaylayan öğrenci o PR için puan almaz. Teknik kilitleme: öğretim elemanı Hafta 5 başında her depoda `Settings → Branches → Add branch protection rule` → `main` → `Require a pull request before merging` işaretler (public depolarda ücretsizdir).

   **Kod/belge ayrımı:** Kod ve veri içeren PR'lar (`/src`, `/data`, `/visuals`) QA'nın `Approve` onayı olmadan merge edilmez. Yalnızca belge değiştiren PR'lar (`/docs`, `/reports`, `README`) inceleme beklemeden yazarı tarafından merge edilebilir — iz yine kalır.

6. **Notlandırma eşik esaslıdır** (birinci dönemle aynı felsefe): Her görevin ilan edilmiş kritik eşikleri vardır. Eşiklerin tamamını geçen öğrenci 90–100 arası puan alır; herhangi bir eşiği geçemeyen öğrencinin o görev puanı **0**'dır. Süreç §5'te tanımlıdır.

7. **İletişim kuralları — hangi konu hangi kanaldan:**

   | Konu | Kanal |
   |---|---|
   | Görev verme, veri teslimi, hata bildirimi, tasarım kararı | **Issue** (ilgiliyi @mention'la) |
   | Koda/veriye dair tartışma ("bu satır neden böyle?") | **PR yorumu** |
   | Hızlı koordinasyon ("bu akşam müsait misin?", "push'ladım bak") | WhatsApp — notlandırılmaz, karar alınmaz |
   | Yüz yüze konuşulması gerekenler | **Haftalık grup toplantısı** |
   | Partner şirketle her şey (Görev 3) | İki depodaki ortak Issue'lar + PM'lerin ortak toplantısı |

   **Haftalık grup toplantısı:** Her hafta 15 dakika. Gündem sabittir: herkes sırayla 3 soruyu cevaplar — *geçen hafta ne yaptım / bu hafta ne yapacağım / neye takıldım*. PM toplantıda alınan kararları ilgili Issue'lara yorum olarak işler ("toplantı kararı: …").

   **Tıkanınca yol (sırayla):** ① Sorunu ilgili Issue'ya yorum olarak yaz, ilgiliyi @mention'la, 24 saat bekle. ② Cevap yoksa PM'i @mention'la. ③ PM de çözemiyorsa haftalık rapora yazar **ve** Issue'da hocayı @mention'lar. Hocaya gitmenin yolu koridorda yakalamak değil, Issue'da etiketlemektir.

---

## 4. Hafta Hafta Talimatlar

> Talimatlar **rol bazındadır** ve "Şirkete özgü" denmedikçe 6 grup için aynıdır. Her madde kontrol edilebilir bir teslimattır: depoda ya vardır ya yoktur.

---

### HAFTA 1 — Şirket Kuruluşu ve Araç Kurulumu

**Herkes (30 öğrencinin tamamı) şu adımları uygular:**

1. **İş ilanlarını inceleyin; liderlik istiyorsanız başvurun:** Öğretim elemanının yayımladığı 6 proje lideri ilanını okuyun. Başvurmak isteyenler Google Form'u **`<BAŞVURU SON TARİHİ>`'a kadar** doldurur (süreç ve form alanları: §1.4).
2. **GitHub hesabınızı doğrulayın** (birinci dönemden hesabınız vardır); kullanıcı adınız profesyonel olsun — bu hesap mezuniyette CV'nize girecek.
3. **Organizasyon davetini kabul edin:** `MAKU-VBA-GBT-II` organizasyonundan gelen davet → `Join`. Gelmediyse hocaya kullanıcı adınızı bildirin.
4. **Araç kurulumunu tamamlayın:** GitHub Desktop (veya terminal + git) kurulu olsun; birinci dönemdeki çalışma ortamınız (Python/Jupyter vb.) hazır olsun.
5. **Grubunuzun deposunu clone'layın:** GitHub Desktop → `File → Clone Repository` → `MAKU-VBA-GBT-II/group-X` → `Clone`. Terminalciler için: `git clone git@github.com:MAKU-VBA-GBT-II/group-X.git`.
6. **Bildirimleri açın:** Depo sayfasında `Watch → All activity` (neden: §2.5). Her çalışma seansına `Fetch origin → Pull` ile başlama alışkanlığını edinin.
7. **İlk kişisel commit:** Ekip seçimi tamamlandıktan sonra `README.md`'yi açın ve kendi satırınızı başlangıç rolünüzle ekleyin: `- Ad Soyad — PM (lider)` veya `- Ad Soyad — BE/FE/DA/QA (başlangıç rolü)`. Kaydedin → commit (mesaj: `README'ye Ad Soyad eklendi`) → `Push origin`. Bu commit, "bu öğrenci araç zincirini kurdu" kanıtıdır.

**Proje liderleri (PM) şu adımları uygular:**

1. BE, FE, DA ve QA için ayrı iş ilanları açın; görevleri, aranan katkıyı, başvuru yöntemini ve son başvuru zamanını yazın.
2. Gelen CV ve portföyleri açıklanmış ölçütlerle değerlendirin. CV'leri kamuya açık depoya koymayın.
3. Dört üyeyi başlangıç rollerine yerleştirin ve ekip listesini öğretim elemanının onayına sunun.
4. Onaylanan ekip listesini `README.md`'ye işleyin; rol rotasyonunun Görev 1–3 boyunca §1.3'e göre uygulanacağını ekibe açıklayın.

**Derste (hoca anlatır):** 15 dakikada Issue/PR/milestone kavramları (§2), ardından 15 dakikalık uygulama: herkes kendi deposunda bir test Issue'su açıp kapatır.

**Hafta 1 sonu grup teslimatları (kontrol listesi):**
- [ ] Proje lideri ilan edildi ve `README.md`'ye `PM (lider)` olarak işlendi.
- [ ] PM dört rol ilanını yayımladı, CV'leri değerlendirdi ve ekip listesini öğretim elemanına onaylattı.
- [ ] Şirket adı liderin önerisiyle seçildi ve `README.md`'nin en üstüne yazıldı.
- [ ] **Teknoloji kararı** `README.md`'ye yazıldı (örn. "Dil: Python · Kütüphaneler: pandas, matplotlib · Görselleştirme: PNG grafikleri"). Şirket içinde tutarlı olunmalı.
- [ ] 5 üyenin 5'i de başlangıç rolüyle commit geçmişinde görünüyor.
- [ ] Depo klasör yapısı oluşturuldu (boş klasörler için `.gitkeep`; herhangi bir üye yapabilir).

---

### HAFTA 2 — İş Akışı Provası (mini veri üretimi)

**Hedef:** Gerçek işe başlamadan önce *Issue aç → işi yap → commit'le → Issue'yu kanıtla kapat* döngüsünü herkesin bir kez yaşaması — üstelik bu dersin özü olan **veri üretimiyle birlikte**. Bu haftaya not verilmez; ama döngüyü tamamlamak Görev 1'in ön koşuludur.

**PM (proje lideri) şu adımları uygular:**

1. Grubun Project Board'unu kurun (§2.3): 4 sütun — `To Do`, `In Progress`, `Review`, `Done`.
2. 5 Issue açın, her üyeye bir tane:
   - **Başlık:** `H2 ısınma — <üyenin adı>`
   - **Açıklama şablonu:** "Kendi dilinizde küçük bir betik yazın: 1'den 100'e 10 rastgele sayı üretsin, `data/prova-adiniz.csv` dosyasına tek sütun halinde yazsın (başlık satırı: `deger`). Betiği `/src` içine koyun. *Kabul kriteri:* `data/prova-adiniz.csv` dosyası senin commit'inle depoda; 10 satır veri içeriyor. *Son tarih:* `<TESLİM GÜNÜ/SAATİ>`."
   - **Assignee:** ilgili üye. Kendinize de bir tane açıp atayın.
3. 5 Issue'yu da panoya ekleyin, `To Do` sütununa koyun.

**Her üye (PM dahil) şu adımları uygular:**

1. Panoda kendi kartınızı `In Progress` sütununa sürükleyin; `Fetch origin → Pull` yapın.
2. Betiği yazın: 10 rastgele sayı üret, `data/prova-adiniz.csv` dosyasına yaz. (Örn. Python: `random.randint(1, 100)` ile liste üret, `csv` modülü veya elle yaz.) Betiği `/src` içine kaydedin.
3. Çıktıyı doğrulayın: CSV dosyasının ilk satırı `deger`, ardından 10 satır sayı.
4. Commit yapın (mesaj örneği: `H2 ısınma — prova-ayse.csv eklendi (10 satır)`) → `Push origin`.
5. Issue'nuza yorum yazın: "Tamamlandı — commit `<hash>`, dosya: `data/prova-adiniz.csv` (10 satır)" → `Close issue` → panoda kartı `Done`'a çekin.

**Hafta 2 sonu grup teslimatları:**
- [ ] Pano 4 sütunla kurulmuş; 5 Issue açılmış ve kanıt yorumuyla kapatılmış.
- [ ] `/data` içinde 5 farklı `prova-*.csv` dosyası; `/src` içinde bunları üreten 5 betik; her üye en az 1 commit atmış.

---

### GÖREV 1 — "Şirket Sektöründe Mini Veri Hattı" (Hafta 3–4)

**Ürün:** Her şirket kendi sektörüne uygun küçük bir **sentetik veri hattı** kurar. Uygulama konusu gruplara göre değişir; ortak olan, verinin BE'den DA'ya, DA'dan FE'ye ve FE'den QA'ya kontrollü biçimde devredilmesidir.

**Sektör veri konuları:**

| Şirket | Veri kümesi | Örnek metrikler | Örnek görseller |
|---|---|---|---|
| A — E-ticaret | Siparişler | toplam ciro · ortalama sipariş adedi · en çok sipariş edilen ürün | günlük ciro · ürün satış payı |
| B — Lojistik | Sevkiyatlar | ortalama teslimat süresi · gecikme oranı · en yoğun rota | rota yoğunluğu · teslimat süresi dağılımı |
| C — Bankacılık | İşlemler | toplam işlem hacmi · ortalama işlem tutarı · şüpheli işlem sayısı | günlük işlem hacmi · işlem türü dağılımı |
| D — Sigorta | Talepler ve ödemeler | toplam ödeme · ortalama talep tutarı · en sık talep türü | talep türleri · ödeme tutarı karşılaştırması |
| E — Perakende | Mağaza satışları | toplam ciro · kategori satış payı · günlük ortalama satış | günlük satış · kategori karşılaştırması |
| F — Tedarik | Tedarik siparişleri | ortalama teslim süresi · gecikme oranı · tedarikçi performansı | tedarikçi karşılaştırması · teslim süresi |

**Ortak asgari ölçütler:** Veri sentetik ve makinece okunabilir CSV formatında olmalıdır; en az 100 veri satırı, sektörün ana kategorik alanında en az 4 farklı değer ve belgelenmiş alan kuralları bulunmalıdır. Gerçek kişi verisi kullanılmaz. Her grup 3 metrik, 2 grafik ve en az 5 test senaryosu üretir.

**Pedagojik hedef:** Uygulamanın kendisi değil, **devir teslim zinciri**: BE üretir → DA analiz eder → FE görselleştirir → QA sınar → PM raporlar. Her ok (devir teslim), GitHub üzerinde yazılı bir izle kanıtlanır — notlandırılan budur.

#### Hafta 3

**PM (lider) şu adımları uygular:**

1. 4 Issue açın. Her Issue'nun açıklamasında **son tarih** ve **tek cümlelik kabul kriteri** bulunmak zorundadır:

   | Issue başlığı | Atanan | Kabul kriteri örneği |
   |---|---|---|
   | `G1-veri — Sektör verisini üret` | BE | `data/<sektor-verisi>.csv` depoda: en az 100 satır, sektör şeması `docs/veri-sozlugu-g1.md` içinde yazılı. |
   | `G1-analiz — 3 metriği hesapla` | DA | `docs/analiz-g1.md` depoda: sektöre uygun 3 metrik hesaplanmış ve yorumlanmış. |
   | `G1-gorsel — 2 grafik üret` | FE | Sektöre uygun 2 PNG grafik `/visuals` içinde; grafikler BE'nin verisinden üretilmiş. |
   | `G1-test — Veri kalitesi testleri` | QA | `tests/test-cases.md` en az 5 senaryo içeriyor. |

2. 4 Issue'yu panoya ekleyip `To Do` sütununa koyun; hafta boyunca kartların doğru sütunda olduğunu her gün kontrol edin.
3. `<TESLİM GÜNÜ/SAATİ>`'a kadar `reports/report-w03.md` dosyasını sprint şablonuyla (§7.1) doldurup commit'leyin: *planlanan / yapılan / tıkanan / kim-ne-yaptı*.

**BE şu adımları uygular:**

1. DA ile birlikte şirketin sektörüne uygun veri kümesini ve şemasını kesinleştirin. Simülasyon betiğini `/src` içine yazın; veri üretimi tekrarlanabilir olmalıdır.
2. `data/<sektor-verisi>.csv` dosyasını üretin. Alan adları, tipler, aralıklar, kategori değerleri, birimler ve satır sayısı `docs/veri-sozlugu-g1.md` içinde yazılı olmalıdır.
3. Dosyada en az 100 veri satırı ve sektörün ana kategorik alanında en az 4 farklı değer bulunmalıdır. Commit mesajına veya Issue yorumuna dosya yolunu, satır sayısını ve şemayı yazın.
4. **Devir teslim yorumu (notlandırılır):** `G1-analiz` ve `G1-gorsel` Issue'larının her birine şu bilgileri yazın: *"Veri hazır — commit `<hash>`. Dosya: `data/<sektor-verisi>.csv` (<satır sayısı> satır). Şema: `docs/veri-sozlugu-g1.md`."* Bu yorum, DA ve FE'nin başlayabileceği resmî devir teslimdir.

**DA şu adımları uygular:**

1. BE ile veri kümesinin sektör amacını, alanlarını ve geçerli aralıklarını netleştirip `docs/veri-sozlugu-g1.md` dosyasına yazın.
2. BE'nin devir teslim yorumunu bekleyin; veri hazır değilken analiz yazmayın.
3. `docs/analiz-g1.md` dosyasını yazın. İçerik zorunlu:
   - Sektöre uygun **3 metrik**; her metriğin formülü ve neyi ölçtüğü.
   - Her metriğin altında **1-2 cümle yorum**.
   - Kullanılan veri dosyası ve commit bilgisi.
4. Analiz kodunu `/src` içine kaydedin; hesaplama tekrarlanabilir olmalıdır.
5. **Devir teslim yorumu (notlandırılır):** `G1-gorsel` Issue'suna yazın: *"Analiz hazır — `docs/analiz-g1.md`, commit `<hash>`. 3 metrik + yorumlar. FE görselleştirebilir."*

**FE şu adımları uygular:**

1. Grafikleri **yapmadan önce** iki grafik için taslak hazırlayın; eksenleri, başlıkları ve gösterilecek metriği belirtin.
2. Taslağın fotoğrafını veya ekran görüntüsünü `G1-gorsel` Issue'suna ekleyin. **Taslak eklenmeden grafik yapımına başlamak kural ihlalidir.**
3. Sektöre uygun iki grafiği PNG olarak `/visuals` klasörüne kaydedin. Dosya adları grafiğin içeriğini açıklamalıdır; örneğin `gunluk-ciro.png`, `rota-yogunlugu.png` veya `tedarikci-gecikme.png`.
4. BE ve DA'nın devir teslim yorumlarını bekleyin; grafikler **BE'nin verisinden** ve DA'nın belirlediği metriklerden üretilmelidir. Grafik üretim kodunu `/src` içine kaydedin.
5. Commit + push; Issue'ya commit hash'ini ve iki çıktı dosyasını yazan kanıt yorumu ekleyin.

**QA şu adımları uygular:**

1. `tests/test-cases.md` dosyasını şablona (§7.3) göre yazın; en az 5 senaryo:
   - Veri dosyası var mı ve boş değil mi?
   - Satır sayısı şemada belirtilen hedefi karşılıyor mu?
   - Sütun adları ve sırası şemayla aynı mı?
   - Veri tipleri, aralıklar ve birimler doğru mu?
   - Ana kategorik alanda yalnızca şemada tanımlanan değerler var mı?
2. Her senaryoda ID, adımlar, girdi ve beklenen sonuç yazılı olmalıdır. "Gerçekleşen sonuç" ve "geçti/kaldı" sütunları Hafta 4'te doldurulacaktır.
3. Commit + push; `G1-test` Issue'suna kanıt yorumu yazıp kapatın.

#### Hafta 4

**QA:**
1. Tüm test senaryolarını gerçek sektör veri dosyası üzerinde tek tek çalıştırın; sonuçları `tests/test-log.md` dosyasına tarihli olarak işleyin.
2. **En az 2 hata Issue'su açın**, `bug` etiketiyle. Hata bulunamazsa `enhancement` etiketiyle iki somut iyileştirme önerisi açın. Her kayıtta yeniden üretme adımları, beklenen davranış ve gözlenen davranış bulunmalıdır.
3. Hata Issue'larını ilgili kişiye atayın (veri hatası → BE, grafik hatası → FE).

**BE + FE:** Size atanan hataları düzeltin. Düzeltme commit'inin mesajında hata numarasını `Fixes #7` biçiminde geçirin — Issue otomatik kapanır, hata-düzeltme bağı kurulmuş olur.

**DA:** Nihai sektör veri dosyasının `docs/veri-sozlugu-g1.md` içindeki şemayla uyumlu olduğunu doğrulayın; `G1-analiz` Issue'suna kapanış yorumu yazın: *"Analiz nihai veri üzerinde doğrulandı — onaylıyorum."* Uyumsuzluk varsa farkları listeleyip BE'ye atayın.

**PM:**
1. Tüm G1 Issue'larının kanıt yorumuyla kapandığını doğrulayın; açık kalan varsa sahibini dürtün.
2. `reports/report-w04.md` raporunu yazıp commit'leyin.
3. `gorev1-final` release'ini oluşturun (§2.4).

**Görev 1 kritik eşikleri (değerlendirme süreci: §5):**
- *Grup eşikleri:* `gorev1-final` release'i son tarihte mevcut · sektör veri dosyası ve şeması teslim edilmiş · devir teslim zinciri kanıtlı (BE'nin `G1-analiz`/`G1-gorsel`'e veri yorumu + DA'nın `G1-gorsel`'e analiz yorumu) · `bug` etiketli ≥2 Issue açılmış ve `Fixes #n` ile kapatılmış · `report-w03.md` ve `report-w04.md` zamanında commit'lenmiş.
- *Bireysel eşikler:* kendi rol teslimatı, Issue'sundaki kabul kriterini sağlıyor · ≥2 commit · üstlendiği Issue'lar kanıt yorumuyla kapatılmış.

---

### GÖREV 2 — "Şirket Mini Ürünü" (Hafta 5–6)

**Ürün:** Şirketin kendi sektöründe (§1.1) mini bir veri ürünü: parametreli bir **simülasyon** + **analiz** + **çoklu grafik**. Roller döndü (§1.3) — herkes yeni rolünün tanımını §1.2'den yeniden okusun.

**Bu görevle devreye giren yeni kural:** `main`'e doğrudan commit atılmaz; **her şey branch + Pull Request + inceleme + merge yoluyla girer** (§2.2, §3.5). Görev 2'nin asıl öğrenme hedefi budur.

#### Hafta 5

**PM (lider) şu adımları uygular:**

1. `Görev 2 — Mini Ürün` adında bir **milestone** oluşturun (§2.3); bitiş tarihi = Hafta 6'nın son günü.
2. Aşağıdaki **5 Issue'yu** açın, her birini milestone'a bağlayın, panoya ekleyin. Her Issue'da son tarih + kabul kriteri zorunlu:

   | # | Issue başlığı | Atanan | İşin tanımı ve kabul kriteri |
   |---|---|---|---|
   | 1 | `G2-sem — Veri şeması ve analiz planı` | DA | Sektörünüzün mini veri kümesinin şeması (alan adları, tipler, aralıklar, satır sayısı) ve hesaplanacak en az 3 metrik `docs/veri-sozlugu.md`'ye işlenmiş ve devir teslim yorumları atılmış olacak. |
   | 2 | `G2-veri — Parametreli simülasyon` | BE | En az 2 ayarlanabilir parametresi olan simülasyon `feature/veri` dalında yazılmış, PR açılmış, QA incelemesinden geçip merge edilmiş olacak. |
   | 3 | `G2-analiz — Metrik hesabı ve bulgular` | DA | Şemadaki 3 metrik hesaplanmış, bulgular `docs/analiz-g2.md`'de, devir teslim yorumu atılmış olacak. |
   | 4 | `G2-gorsel — Grafik seti` | FE | Taslak Issue'ya eklenmiş, en az 3 grafik `feature/gorsel` dalında üretilmiş, PR ile merge edilmiş olacak. |
   | 5 | `G2-test — Test senaryoları ve PR incelemesi` | QA | `tests/test-cases.md` güncel; BE'nin PR'ında ≥2 somut inceleme yorumu var. |

3. `reports/report-w05.md` raporunu `<TESLİM GÜNÜ/SAATİ>`'a kadar yazıp commit'leyin.

**DA şu adımları uygular:**

1. Sektörünüzün mini veri kümesi için `docs/veri-sozlugu.md` yazın: **her alanın** adı, tipi, aralığı/kuralı, örnek değeri + hedeflenen satır sayısı + **hesaplanacak en az 3 metrik** (adı + formülü + neyi ölçtüğü). Fikir vermesi için sektör bazında örnekler:

   | Şirket | Örnek veri kümesi | Örnek metrikler |
   |---|---|---|
   | A — E-ticaret | siparişler: musteri_id, urun, adet, fiyat, tarih | toplam ciro · sipariş başına ortalama adet · en çok sipariş edilen ürün |
   | B — Lojistik | sevkiyatlar: sevkiyat_id, kaynak, hedef, mesafe_km, sure_saat | ortalama teslimat süresi · geciken sevkiyat oranı · en yoğun rota |
   | C — Bankacılık | islemler: islem_id, musteri_id, tur, tutar, tarih | toplam işlem hacmi · ortalama işlem tutarı · şüpheli işlem sayısı (kural sizde) |
   | D — Sigorta | talepler: talep_id, musteri_id, tur, talep_tutar, prim | toplam ödeme · talep başına ortalama tutar · en sık talep türü |
   | E — Perakende | satislar: urun, kategori, adet, fiyat, tarih | toplam ciro · kategori bazlı satış payı · stok dönüş hızı |
   | F — Tedarik | siparisler: siparis_id, tedarikci, urun, miktar, teslim_gun | ortalama tedarik süresi · kritik stok ürün sayısı · tedarikçi bazlı gecikme oranı |

2. `feature/sozluk-g2` gibi bir branch'te commit + push yapıp PR açın. Belge PR'ları inceleme beklemeden yazarı tarafından merge edilebilir (§3.5): açın, merge edin — iki dakikalık iştir ama iz bırakır.
3. Devir teslim yorumlarını `G2-veri` Issue'suna yazın: *"Şema yayımlandı — commit `<hash>`. Alanlar, aralıklar ve 3 metrik `docs/veri-sozlugu.md`'de. BE üretebilir."*

**BE şu adımları uygular:**

1. `feature/veri` adında bir branch açın (§2.2).
2. Simülasyonu DA'nın şemasına birebir uyacak şekilde yazın. **En az 2 parametre** ayarlanabilir olsun (örn. gün sayısı, ürün/müşteri sayısı, rastgelelik tohumu) — parametreler betiğin başında veya komut satırından değiştirilebilsin.
3. Üretilen veriyi `/data` içine kaydedin; commit mesajına şemayı yazın (satır sayısı + sütun listesi).
4. Çıktıyı kendiniz doğrulayın: satır sayısı, alan adları, aralıklar şemayla uyumlu mu?
5. `Publish branch` → **PR açın**: başlık `G2 parametreli simülasyon`, açıklamaya `Closes #<G2-veri Issue numarası>`, **Reviewers** kısmından QA'yı seçin.
6. QA'nın yorumlarına **PR üzerinden** cevap verin; istenen düzeltmeleri aynı branch'e commit'leyin (PR otomatik güncellenir). QA `Approve` verdikten sonra merge düğmesine PR sahibi olarak siz basarsınız.

**FE şu adımları uygular:**

1. Önce taslak: 3 grafiğin mockup'ını `G2-gorsel` Issue'suna ekleyin (Görev 1'deki kural aynen geçerli).
2. `feature/gorsel` adında branch açın; en az 3 grafiği üretin (örn. zaman serisi + kategori karşılaştırması + dağılım/pasta). Grafikler `/visuals` klasörüne PNG olarak kaydedilsin; üretim kodu `/src` içinde olsun.
3. Commit → publish. PR'ı Hafta 6'da açacaksınız; bu hafta iskelet bitmiş olsun.

**QA şu adımları uygular:**

1. `tests/test-cases.md` dosyasını Görev 2'nin veri kümesi için yeniden yazın: en az 5 senaryo — satır sayısı, sütun adları, aralıklar, tip kontrolü ve parametre davranışı (örn. "gün sayısı 10'a çekilince satır sayısı şemaya göre değişiyor mu?").
2. **BE'nin PR'ını inceleyin** (§2.2): `Files changed` sekmesinde koda bakın, **en az 2 somut yorum** yazın. Sorular da geçerli yorumdur: "Bu fonksiyon negatif değer üretebilir mi?" Onay vermeden önce yorumlarınıza cevap alın; sonra `Approve` — merge işlemini PR sahibi yapar.

#### Hafta 6

**FE:**
1. Grafikleri merge edilmiş veri üzerinde son haline getirin; `feature/gorsel` dalına commit'leyin.
2. PR açın (reviewer: QA). QA'nın istediği düzeltmeleri yapın; onay sonrası merge edin.

**DA:**
1. `docs/analiz-g2.md` dosyasını yazın: şemadaki 3 metriği nihai veri üzerinde hesaplayın, her birini 1-2 cümleyle yorumlayın; kullandığınız veri commit'ini belirtin.
2. `docs/requirements.md` dosyasını geriye dönük yazın: 1 sayfalık resmî gereksinim belgesi — mini ürünün amacı, yaptıkları (numaralı liste), yapmadıkları. Bu belge büyük proje önerisinin şablonu olacak; özenli yazın.

**BE:**
1. Simülasyona **hata yönetimi** ekleyin: geçersiz parametrede (negatif gün sayısı, sıfır ürün vb.) program çökmemeli, anlamlı bir mesaj vermeli (Python'da `try/except` + `raise ValueError`; diğer dillerde eşdeğeri). Hata sessizce yutulmaz.
2. `fix/error-handling` gibi bir branch'te çalışın → commit → PR → QA incelemesi → merge.

**QA:**
1. Merge edilmiş ürün üzerinde tam test turu: tüm senaryoları çalıştırıp `tests/test-log.md`'ye işleyin.
2. En az 2 `bug` Issue'su açın (şablon Görev 1 Hafta 4'teki gibi), ilgililere atayın.
3. `docs/user-manual.md`'yi başlatın: kurulum bölümü (hangi ortam, hangi komutlar, veri nasıl üretilir) + ekran görüntülü 1 kullanım senaryosu.

**PM:**
1. Pano hijyenini denetleyin: yanlış sütunda kart, sahipsiz Issue, kapanmamış iş kalmasın.
2. Milestone'daki tüm Issue'lar kapanınca milestone'u kapatın.
3. `gorev2-final` release'ini oluşturun; `reports/report-w06.md` raporunu yazın.

**Görev 2 kritik eşikleri:**
- *Grup eşikleri:* `gorev2-final` release'i son tarihte mevcut · gerçek inceleme yorumları içeren ≥2 merge edilmiş PR · `/src` farkında hata yönetimi kodu görünüyor · kılavuz başlamış · milestone kapatılmış.
- *Bireysel eşikler:* kendi rol teslimatı kabul kriterini sağlıyor · PR akışına izlenebilir katılım (BE/FE: kendi işi PR ile merge edilmiş; QA: ≥2 somut inceleme yorumu; DA: şema + devir teslim yorumları; PM: milestone + raporlar) · ≥2 commit veya eşdeğer yazılı iz.

---

### GÖREV 3 — "B2B Veri Değişimi" (Hafta 7–8)

**Ürün:** Eşleşen iki şirket de kendi veri kümesini **dışa aktarır** (export); karşı şirketin dosyasını **içe aktarıp analiz eder ve görselleştirir** (import). Eşleşmeler: A↔B, C↔D, E↔F (§1.1). Her çift iki yönlü veri akışını kapsayan ortak bir **veri sözleşmesi** müzakere eder. Roller yine döner (§1.3).

**Sözleşme nedir:** İki tarafın da uyacağı yazılı dosya formatı tanımıdır — gerçek sektörde iki şirketin API/veri anlaşmasının küçük ölçekli hali. Sözleşmede hem `Şirket X → Şirket Y` hem de `Şirket Y → Şirket X` veri akışının şeması bulunur. **Veri değişiminin kendisi notlandırılır:** iki yön de gönderildi mi, karşı taraf dosyaları hatasız okuyabildi mi, sözleşmeye uyuldu mu.

**Zemin:** Görev 3, Görev 2'deki mini ürünün üzerine inşa edilir — aynı depoyla, aynı sektör verisiyle devam edersiniz.

**Dosya değişimi GitHub üzerinden yapılır:** Her şirket kendi deposundaki `exchange/output.csv` dosyasını kendi veri akışına göre üretir; partner şirket dosyayı oradan alır. Böylece her iki depoda da birer `exchange/output.csv` bulunur ve iki yönlü alışveriş tamamlanır. **Ara teslim:** Her iki `exchange/output.csv` dosyası en geç **Hafta 8'de, `<ARA TESLİM GÜNÜ/SAATİ>`'ne kadar** depoda olmalı — yoksa partnerin içe aktarmayı test edecek zamanı kalmaz.

#### Hafta 7 — Sözleşme haftası

**DA şu adımları uygular:**

1. Partner şirketin DA'sıyla iki yönlü veri sözleşmesini müzakere edin — **sözlü değil**, GitHub üzerinde: her iki depoda da `Veri sözleşmesi A↔B` (kendi eşleşmenize göre) başlıklı birer Issue açın; müzakere bu Issue'ların yorumlarında yürür.
2. Hem `Şirket X → Şirket Y` hem de `Şirket Y → Şirket X` akışı için dosya formatı, alan adları ve sırası, tipler, ayraç, kodlama, tarih formatı, ondalık ayracı, başlık satırı, birimler ve hatalı satır kuralında anlaşın.
3. İki akışın şemasını `docs/veri-sozlesmesi.md` içinde ayrı başlıklarla yazın ve **her iki depoya da birebir aynı** commit'leyin. İki dosya arasında tek karakter fark olması sözleşme ihlalidir.

**BE şu adımları uygular:**

1. Sözleşmeye birebir uyan `ExportCSV` (veya JSON ise `ExportJSON`) fonksiyonunu/betiğini yazın: şirketinizin Görev 2 verisini `exchange/output.csv` dosyasına yazar. Format sözleşmede yazanın aynısı olmalı: alan sırası, ayraç, tarih formatı, kodlama.
2. Branch + PR + QA incelemesi + merge (artık standart akış).

**FE:** Görev 2 çıktılarına bir "dışa aktarım" dokunusu ekleyin: şirketinizin kendi `exchange/output.csv` dosyası tek komutla/betikle üretilebilsin (örneğin `src/export.py`). Branch + PR + merge.

**QA:** Çapraz testleri tasarlayıp `tests/test-cases.md`'ye ekleyin. Her iki yöndeki dosya için eksik sütun, yanlış tarih formatı, tamamen boş dosya ve fazla sütun senaryolarını yazın. Her senaryo için beklenen davranışı belirtin ("program çöker" hiçbir senaryoda kabul edilebilir davranış değildir).

**PM (lider):** Partner şirketin PM'iyle 15 dakikalık ortak bir toplantı ayarlayın; tutanağı `reports/joint-meeting-w07.md` olarak **iki depoya da** commit'leyin. Tutanakta: katılanlar, konuşulanlar, alınan kararlar, açık kalan konular.

#### Hafta 8 — Değişim haftası

**BE:**
1. Kendi verinizden `exchange/output.csv` üretin ve commit'leyin (**ara teslim: `<ARA TESLİM GÜNÜ/SAATİ>`**).
2. Partnerin deposundaki `exchange/output.csv` dosyasını indirin; onu okuyup işleyen `ImportCSV` betiğini yazın. Sözleşmedeki ilgili akışın alan adlarını ve tiplerini doğrulayarak `data/partner-verisi.csv` olarak (veya doğrudan belleğe) yükleyin. Kendi ürettiğiniz test dosyasıyla değil, **partnerin gerçek çıktısıyla** test edin.

**DA:**
1. Partnerin gerçek verisi üzerinde bir analiz yazın: `docs/partner-analizi.md` — en az 3 metrik + yorumlar. Kullandığınız dosyanın hangi commit'ten alındığını belirtin.
2. Sözleşme anlaşmazlıklarında hakemlik yapın. Sözleşme değişirse sürümleyin: `veri-sozlesmesi.md` içinde `v1.1` başlığı + değişiklik günlüğü satırı ("v1.1 — tarih formatı netleştirildi, 2026-04-12"). Güncel sürüm yine iki depoda birebir aynı olmalı.

**FE:** Partnerin verisi üzerinden en az 2 grafik üretin (`visuals/partner-*.png`) ve `/src` içindeki görselleştirme betiğine "içe aktarım" yeteneği ekleyin.

**QA:**
1. Değişim testini çalıştırın: partnerin gerçek dosyasını alın, içe aktarın, sonuçları `test-log.md`'ye işleyin.
2. **Partner şirketin deposunda bir "Değişim sonucu" Issue'su açın — her durumda.** İçerik: kaç satır başarıyla içe aktarıldı, kaç satır reddedildi, tespit edilen sözleşme ihlalleri (varsa madde madde; yoksa "dosya sözleşmeye tam uyumlu, teşekkürler" teyidi). **Profesyonel dil zorunlu ve notlandırılır.** Kötü örnek: "dosyanız bozuk, düzeltin." İyi örnek: *"Sözleşme v1 §3'e göre tarih formatı `yyyy-mm-dd` olmalı; gönderilen dosyanın 12. satırında `05.03.2026` görünüyor. Yeniden üretme: dosyayı ekledim. Düzeltilmiş dosyayı bekliyoruz, teşekkürler."*

**PM:** `reports/report-w08.md` raporunu yazın; rapora bir paragraf zorunlu: **"değişimde ne bozuldu ve neden"** (hiçbir şey bozulmadıysa bu da yazılır ama inandırıcı olmalı). `gorev3-final` release'ini oluşturun.

**Görev 3 kritik eşikleri:**
- *Grup eşikleri:* `gorev3-final` release'i son tarihte mevcut · iki şirketin `exchange/output.csv` dosyaları `<ARA TESLİM GÜNÜ/SAATİ>` ara teslimine kadar depodaydı · iki depoda birebir aynı, iki yönlü sözleşme dosyası · partner dosyalarının iki yönde başarıyla içe aktarılması (hoca derste canlı test eder) · partner deposunda "Değişim sonucu" Issue'su açılmış, dili profesyonel ve somut.
- *Bireysel eşikler:* kendi rol teslimatı kabul kriterini sağlıyor · ≥2 commit veya eşdeğer yazılı iz (DA/PM için sözleşme müzakeresi ve tutanak kayıtları da izdir).

---

### VİZE HAFTASI (akademik takvimdeki ara sınav haftası)

- **Bireysel yazılı/uygulamalı sınav (vizenin %60'ı):** Birinci dönemin devamı olan temel veri becerileri — her öğrenci laboratuvar sınavında **tek başına** küçük bir simülasyon yazar, veri üretir, 2 metrik hesaplar ve 1 grafik çizer. Grup bileşeni yoktur; bu bölüm, gruba sırtını yaslayan öğrenciye karşı sigortadır.
- **Süreç notu (vizenin %40'ı):** Görev 1–3 puanlarının ortalaması (eşik sistemiyle verilmiş, §5). **Akran değerlendirme formu #1** bu hafta doldurulur (anonim Google Form: her takım arkadaşına 1–5 puan + bir cümle gerekçe; alanlar §7.4'te) ve görev puanlarının kalite bandına girdi olur.

---

### BÜYÜK PROJE (Hafta 9–15)

#### Hafta 9 — Başlangıç (Kickoff)

**Tüm şirketler şu adımları uygular:**

1. **Kalan 4 rolü müzakere edin.** PM, dönem başında seçilen proje lideridir ve sabittir. BE, FE, DA, QA rolleri diğer 4 üyeye müzakereyle dağıtılır — herkes 3 rol deneyimledi; kim neyi iyi yaptı, kim neyi sevdi, açık konuşun. Nihai rol listesini `README.md`'ye commit'leyin; öğretim elemanı onaylar.
2. **DA + PM birlikte 1 sayfalık proje önerisini yazar** (`docs/requirements.md`, Görev 2'de yazılan belge şablondur). Zorunlu içerik:
   - **Amaç:** ürün kimin hangi sorununu çözüyor (2–3 cümle).
   - **Özellikler:** 5–8 somut özellik, `R1`, `R2`, … diye numaralı. Her R maddesi test edilebilir bir cümledir. Kötü: "R1: Kullanıcı dostu olacak." İyi: "R1: Kullanıcı, gün sayısı ve ürün sayısı parametrelerini değiştirerek satış verisi üretebilecek."
   - **Veri modeli taslağı:** hangi veri kümeleri/dosyalar olacak, ana alanlar neler.
   - **Kapsam dışı listesi:** bilinçli olarak yapılmayacaklar (örn. "canlı API entegrasyonu yok"). Bu liste, dönem sonunda "ama şunu da yapsaydınız" tartışmasını önler.
3. **Hoca kapısı:** Öneri Hafta 10 dersinde onaylanır veya revize edilir. **Onaydan önce kod yazmak yasaktır.**

**Şirkete özgü zorunlu asgari özellik setleri** (her satır = olmazsa olmaz R maddeleri; şirketler üzerine 2–3 kendi özelliğini ekler):

| Şirket | Büyük projenin zorunlu özellikleri |
|---|---|
| **A — E-ticaret** | parametreli sipariş simülasyonu · ürün bazlı satış analiz raporu · aylık trend grafiği · satış verisinin CSV dışa aktarımı |
| **B — Lojistik** | parametreli sevkiyat simülasyonu · teslimat süresi analizi · geciken sevkiyat raporu · rota/hacim görselleştirmesi |
| **C — Bankacılık** | parametreli işlem simülasyonu · şüpheli işlem tespit kuralı · müşteri segment analizi · işlem hacmi trend grafiği |
| **D — Sigorta** | parametreli talep simülasyonu · prim/ödeme analizi · risk kategorisi hesabı · aylık özet dashboard |
| **E — Perakende** | parametreli satış simülasyonu · kategori bazlı performans raporu · stok dönüş analizi · kritik stok uyarı kuralı |
| **F — Tedarik** | parametreli sipariş simülasyonu · tedarik süresi analizi · kritik stok raporu · tedarikçi bazlı gecikme grafiği |

#### Hafta 10 — Temel Atma

- **DA:** Tam veri sözlüğü v1'i commit'leyin: **her** veri kümesi, **her** alan, **her** fonksiyon imzası (girdi/çıktı tipleriyle). Büyük projede sözlük eksikse BE ve FE durur; darboğaz sizsiniz, erken bitirin.
- **BE:** Sözlükteki her imza için içi boş (sadece imza + `TODO` yorumu) fonksiyonlardan oluşan iskelet betikler yazın. Ölçüt: iskelet çalıştırılabilir (boş çıktıyla da olsa hata vermeden çalışır).
- **FE:** Tüm grafik/dashboard taslaklarını ilgili Issue'lara ekleyin; ana dashboard iskeletini (tüm parçaların bir arada görüneceği çıktı, örn. tek sayfalık PNG/HTML) oluşturun.
- **QA:** Test planını yazın: **her R maddesi için en az 3 test senaryosu** `tests/test-cases.md`'de (normal + sınır + hatalı girdi).
- **PM:**
  1. İki milestone oluşturun: `M1 — Ara Kontrol` (bitiş: Hafta 11) ve `M2 — Özellik Tamamlama` (bitiş: Hafta 13).
  2. Her R maddesini bir veya birkaç Issue'ya bölün; hepsini atayın, milestone'a bağlayın, panoya koyun. Örnek bölme: "R3: kritik stok raporu" → `R3-veri: KritikStok hesaplama fonksiyonu (BE)` + `R3-gorsel: Rapor grafiği (FE)`.
  3. Haftalık raporlar aynen devam eder: `report-w10.md` … `report-w14.md`.

#### Hafta 11 — **KİLOMETRE TAŞI 1 (notlandırılan ara kontrol, final notunun %10'u)**

Derste canlı kontrol edilen zorunlu durum:

- [ ] Veri modeli dosyaları mevcut ve sözlükle birebir uyumlu.
- [ ] Ana dashboard tüm parçalara ulaşabiliyor (parçalar taslak/boş olabilir).
- [ ] En az **2 R maddesi uçtan uca çalışıyor** (parametre veriliyor → veri üretiliyor → metrik hesaplanıyor → grafik çıkıyor).
- [ ] Hafta 9'dan bu yana ≥4 merge edilmiş PR ve her birinde gerçek inceleme var.

Canlı kontrol nasıl işler: hoca şirketin bilgisayarında `main` dalının son halini açtırır; PM değil, **hocanın seçtiği rastgele bir üye** çalışan 2 özelliği gösterir.

#### Hafta 12 — İnşa

- **BE/FE:** Kalan özellikleri geliştirin. Değişmez kural: **her özellik = branch + PR + inceleme + merge.** Branch adı özelliği söylesin (`feature/R4-kritik-stok`), PR açıklaması R numarasını ve Issue'yu bağlasın (`Implements R4, closes #23`).
- **QA:** Merge edilen her özelliği bekletmeden test edin; hataları `bug` Issue'suyla kaydedin. **Regresyon kontrolü** yapın: yeni merge'ler, daha önce geçen testleri bozmuş mu — eski senaryoları yeniden koşun.
- **DA:** **Değişiklik kontrolü:** Sözlükten herhangi bir sapma (yeni alan, imza değişikliği), kod merge edilmeden **önce** sözlüğün sürümlü güncellemesini gerektirir (sözlüğe `v1.1 — gecikme_gun alanı eklendi` gibi değişiklik satırı işlenir). Önce belge, sonra kod.

#### Hafta 13 — **KİLOMETRE TAŞI 2 (notlandırılan ara kontrol, final notunun %10'u)**

- [ ] **Özellik-tamam (feature-complete):** tüm zorunlu R maddeleri merge edilmiş durumda.
- [ ] Hata eğilimi görünür: `test-log.md` en az 2 tam test turu içeriyor (tarihleriyle) ve ikinci turda kalan hata sayısı azalmış.
- [ ] `docs/user-manual.md` ekran görüntüleriyle en az %50 tamamlanmış.

#### Hafta 14 — Sağlamlaştırma

- **Kod dondurma (code freeze) `<KOD DONDURMA GÜNÜ>` (örn. Çarşamba):** O andan itibaren `main`'e yalnızca `bug` etiketli Issue'lara bağlı düzeltme PR'ları girebilir; yeni özellik girmez. Amaç: teslimden önce ürünü sarsmamak.
- **QA:** Son tam regresyon turu; ardından `M2` milestone'una imza yorumu: *"Tüm senaryolar koşuldu, bilinen kritik hata yok / bilinen hatalar: …"*
- **FE:** Cila turu: grafik başlıkları, eksen etiketleri, renk paleti ve tüm çıktılarda dil/üslup tutarlılığı.
- **DA:** Gereksinim ↔ ürün çapraz kontrol tablosu: `R1…Rn` için tek tablo — durum (tamamlandı / kısmen / iptal) + gerekçe. `docs/requirements.md`'nin sonuna eklenir.
- **PM:** `reports/report-w14.md` = 1 sayfalık proje retrospektifi: neler iyi gitti / neyi farklı yapardık / ekip için 3 ders.
- **Herkes:** **Akran değerlendirme formu #2**'yi doldurur.

#### Hafta 15 / Final — Teslim ve Demo

**Teslim** = deponun `final` etiketli (release) hali; içinde: tüm betikler, veri dosyaları, görselleştirmeler, eksiksiz kılavuz, test log'u, tüm haftalık raporlar.

**Canlı demo, şirket başına 10 dakika:** Hangi üyenin hangi özelliği göstereceğini **hoca o anda seçer ve ilan eder** + 5 dakika soru-cevap. Bu format, herkesin yalnızca kendi parçasını değil **ürünün bütününü** anlamasını test eder — "o kısmı arkadaşım yaptı, bilmiyorum" cevabı demo puanını düşürür.

**Final notu bileşimi:** %10 Kilometre Taşı 1 + %10 Kilometre Taşı 2 + %80 dönem sonu değerlendirmesi. Dönem sonu değerlendirmesinin içi: %50 ürün kalitesi (özellikler çalışıyor, veri doğru, görseller anlamlı) · %30 süreç izlenebilirliği (PR'lar, Issue'lar, raporlar, milestone'lar) · %20 demo + akran değerlendirmesi.

---

## 5. Değerlendirme Süreci (Şeffaflık Beyanı)

Bu bölüm, notların nasıl oluştuğunu herkesin baştan bilmesi için yazılmıştır. Sürpriz kriter yoktur: aşağıda ve görev bölümlerinin sonundaki eşik listelerinde yazmayan hiçbir şey puanlamaya girmez.

1. **Teslim anı = release.** Her görevin teslimi, son tarihte PM'in oluşturduğu release'tir (`gorev1-final` vb.). Değerlendirme yalnızca bu mühürlü hâl üzerinden yapılır; son tarihten sonraki commit'ler o görevin notunu etkilemez. Release son tarihte yoksa görev teslim edilmemiş sayılır (grup eşiği ihlali).

2. **Denetim.** Son tarihten sonra öğretim elemanı depoları denetler — yapay zekâ destekli otomatik tarama dahil: kritik eşik listesi kalem kalem kontrol edilir (commit'ler ve zaman damgaları, Issue ve devir teslim yorumları, PR incelemeleri, dosya içerikleri, veri dosyalarının satır sayıları). Denetimin çıktısı şirket ve üye başına bir geçti/kaldı tablosudur. **Nihai kararı her zaman öğretim elemanı verir**; otomatik denetim hızlandırıcı bir araçtır, hakem değildir.

3. **İki katmanlı eşik kontrolü:**
   - **Grup eşikleri** görevin bir bütün olarak teslim edilmiş sayılması için gerekenlerdir (release, ortak dosyalar, PR/milestone düzeni, devir teslim zinciri). Bir grup eşiği sağlanmamışsa **görev tüm grup için 0**'dır — bu yüzden PM'in son gün kontrol listesi hayatidir.
   - **Bireysel eşikler** üyenin kendi rolünün teslimatı ve kişisel izleridir. Bireysel eşiği kaçıran **yalnızca o üye 0** alır; grubun geri kalanı etkilenmez.

4. **Puanlama: 0 veya 90–100.** Eşiklerin tamamını geçen öğrenci 90–100 arası puan alır; bandın neresinde olduğunu işinin kalitesi belirler:
   - kodun okunabilirliği ve hata yönetiminin özeni (BE),
   - grafiklerin ve çıktıların açıklığı, etiket ve başlık özeni (FE),
   - analizlerin derinliği, belge ve raporların açıklığı (DA/PM),
   - inceleme yorumlarının ve hata kayıtlarının derinliği (QA),
   - işin haftaya yayılması — her şeyin son gece tek commit'te gelmemesi (zaman damgaları görünürdür).

   Eşik geçilmemişse puan 0'dır; kısmi puan yoktur. Eşikler bu yüzden bilinçli olarak asgari düzeyde tutulmuştur: haftalık talimatları normal şekilde uygulayan bir öğrencinin takılacağı hiçbir eşik yoktur.

5. **Sonuçların ilanı ve itiraz.** Denetim çıktısı (hangi eşik geçildi/geçilmedi) isteyen öğrenciyle paylaşılır. İtiraz, ilandan itibaren 1 hafta içinde, karşı kanıt gösterilerek yapılır — kanıt yine GitHub izidir ("şu yorum/commit şurada" gibi).

6. **Akran değerlendirmesi** bir eşik değildir; kalite bandı (90–100) içindeki yerin girdilerinden biridir ve izi az görünen ama ekibe katkısı büyük üyeleri (fikir üreten, arkadaşına öğreten) korumak için kullanılır.

Bu süreç Görev 1–3'te aynen uygulanır; büyük projede eşik işlevini Kilometre Taşı 1–2 kontrol listeleri ve final teslim listesi görür.

---

## 6. Haftalık Öğretim Elemanı Rutini (planın hoca tarafı)

| Ne zaman | Eylem | Süre |
|---|---|---|
| Pazartesi | 6 sprint raporunu (`/reports/report-wXX.md`) tara; eksik/tıkanma sinyali ara | ~20 dk |
| Çarşamba | GitHub org → her depo → Insights → Contributors; anomali not et (sıfır commit'li üyeler) | ~15 dk |
| Derste | Şirket başına 5 dk ayakta toplantı: PM 2 dk konuşur, sen PM olmayan rastgele bir üyeye soru sorarsın | ~30 dk |
| Her görev sonrası (son tarihin ertesi günü) | Eşik denetimini çalıştır; çıktı tablosunu doğrula, puanları ilan et (§5) | ~30 dk |

**Anomali protokolü:** 2 hafta üst üste hiç iz bırakmayan öğrenciye özel uyarı yapılır. İz bırakmamaya devam eden öğrenci, görevin bireysel eşiklerini geçemeyeceği için o görevden 0 alır (§5) — uyarının amacı bunu sürpriz olmaktan çıkarmaktır.

---

## 7. Hafta 1'de Dağıtılacak Şablonlar (tam içerikleriyle)

### 7.1 Sprint Raporu Şablonu (`reports/report-wXX.md`)

```markdown
# Sprint Raporu — Hafta XX
**Şirket:** <şirket adı> · **PM:** <ad> · **Tarih:** <yyyy-mm-dd>

## Planlanan
- <bu hafta başında hedeflenen işler>

## Yapılan
- <biten işler; Issue/PR numaralarıyla: "G2-veri tamamlandı (#12, PR #15)">

## Tıkanan
- <bloke olan işler ve nedeni; yoksa "yok" yazılır>

## Kim Ne Yaptı
| Üye | Rol | Bu haftaki katkı (Issue/commit referanslı) |
|---|---|---|
| ... | ... | ... |

## Gelecek Hafta Planı
- <öncelikli 3–5 iş>
```

### 7.2 Veri Sözlüğü Şablonu (`docs/veri-sozlugu.md`)

```markdown
# Veri Sözlüğü — <ürün adı>
**Sürüm:** v1 · **DA:** <ad> · **Tarih:** <yyyy-mm-dd>

## Veri Kümesi: <dosya adı>
| Alan | Tip | Kural/Aralık | Örnek |
|---|---|---|---|
| tarih | Tarih | yyyy-mm-dd | 2026-03-05 |
| urun | Metin | 4 sabit değerden biri | Ürün-A |
| adet | Tam sayı | 0–50 | 12 |

**Hedef boyut:** 120 satır + başlık.

## Metrikler
| Metrik | Formül | Neyi ölçer |
|---|---|---|
| Toplam gelir | Σ(adet × birim_fiyat) | Dönem cirosu |

## Fonksiyon İmzaları (büyük projede zorunlu)
| İmza | Ne yapar | Kim çağırır |
|---|---|---|
| `simule(gun_sayisi, urun_sayisi) -> csv` | Veri üretir | BE |

## Değişiklik Günlüğü
- v1 — ilk sürüm (<tarih>)
```

### 7.3 Test Senaryosu Şablonu (`tests/test-cases.md`)

```markdown
| ID | Özellik (R# / görev) | Adımlar | Girdi | Beklenen | Gerçekleşen | Geçti/Kaldı |
|---|---|---|---|---|---|---|
| T1 | G1 | Sektör veri dosyasını aç, satır say | — | Şemada belirtilen hedef satır sayısı sağlanır | | |
| T2 | R1 | Simülasyonu gun_sayisi=10 ile çalıştır | 10 | 40 satır veri üretilir | | |
```

"Gerçekleşen" ve "Geçti/Kaldı" sütunları test koşulduğunda `test-log.md`'de tarihli olarak doldurulur.

### 7.4 Akran Değerlendirme Formu (Google Form, anonim)

Her takım arkadaşı için:
- Katkı düzeyi (1–5)
- Güvenilirlik — sözünü tutma, teslim tarihine uyma (1–5)
- Tek cümlelik gerekçe (zorunlu, boş bırakılamaz)

### 7.5 Veri Sözleşme Şablonu (`docs/veri-sozlesmesi.md`, Görev 3 için)

```markdown
# Veri Sözleşmesi — <Şirket X> ↔ <Şirket Y>
**Sürüm:** v1 · **Tarih:** <yyyy-mm-dd> · **İmzacılar (DA'lar):** <ad>, <ad>

## Veri akışı: <Şirket X> → <Şirket Y>

| Alan | Karar |
|---|---|
| Dosya adı ve format | output.csv (CSV) |
| Alanlar (sıralı) | <ör: tarih; urun; adet; birim_fiyat> |
| Tipler | <ör: tarih; metin; tam sayı; sayı> |
| Ayraç | `;` (noktalı virgül) |
| Kodlama | UTF-8 |
| Tarih formatı | yyyy-mm-dd |
| Ondalık ayracı | . (nokta) |
| Birimler | <ör: TL, adet, km> |
| Başlık satırı | var (1. satır) |
| Hatalı satır kuralı | <ör: atlanır ve özet raporda sayılır> |

## Veri akışı: <Şirket Y> → <Şirket X>

| Alan | Karar |
|---|---|
| Dosya adı ve format | output.csv (CSV) |
| Alanlar (sıralı) | <ör: sevkiyat_id; rota; sure_saat; durum> |
| Tipler | <ör: metin; metin; sayı; metin> |
| Ayraç | `;` (noktalı virgül) |
| Kodlama | UTF-8 |
| Tarih formatı | yyyy-mm-dd |
| Ondalık ayracı | . (nokta) |
| Birimler | <ör: saat, km, adet> |
| Başlık satırı | var (1. satır) |
| Hatalı satır kuralı | <ör: atlanır ve özet raporda sayılır> |

## Değişiklik Günlüğü
- v1 — ilk sürüm
```
