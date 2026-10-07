# GitHub Rehberi — VBA II

Bu derste tüm çalışma GitHub üzerinden yürür ve tek bir altın kural vardır:

> **GitHub'da yoksa, yapılmamıştır.** (Dönem planı §3.3)

Bir işi yaptıysanız bile GitHub'da iz bırakmadıysanız, süreç gözünde o iş yapılmamış sayılır. Bu rehber, bu izleri doğru bırakmanız için bilmeniz gereken her şeyi anlatır.

---

## 1. Hesap, organizasyon, depo, takım

| Kavram | Nedir | Bu dersteki karşılığı |
|---|---|---|
| **Hesap** | Kişisel GitHub kimliğiniz | `github.com/<kullanici-adiniz>` |
| **Organizasyon** | Bir grup insanın ve depoların çatısı | `MAKU-VBA-GBT-II` — dersin "şirketler birliği" |
| **Depo (repo)** | Bir projenin tüm dosyaları + tüm geçmişi | `ders` (duyurular ve plan), `group-a`…`group-g` (şirket depoları) |
| **Takım (team)** | Organizasyon içindeki erişim grubu | Her grup bir takım; **yalnızca kendi deponuzda yazma (Write) hakkınız var**, diğer depoları okuyabilirsiniz |
| **README** | Deponuzun vitrini | Şirket adı, üyeler, roller, teknoloji kararı — burada yazılıysa vardır |

Organizasyon davetini e-postanızdan veya GitHub bildirimlerinizden kabul ettiğinizde takımınıza dahil olursunuz.

## 2. Günlük çalışma döngüsü

Her iş oturumunda aynı beş adım:

```text
pull (uzaktakini al) → değişikliği yap → commit (kaydet) → push (gönder) → kanıt yorumu (Issue'da)
```

- **clone** — depoyu bilgisayarınıza indirme. Depo başına **bir kez** yapılır.
- **pull** — uzak depodaki yenilikleri bilgisayarınıza alma. **Her çalışmaya başlarken** yapın; GitHub Desktop'ta **Fetch origin** düğmesinin yaptığı iş budur.
- **push** — bilgisayarınızdaki commit'leri uzak depoya gönderme. Yaptığınız iş, push edilmeden ekip arkadaşlarınız tarafından görünmez.
- **commit** — aşağıda.

Araç fark etmez: GitHub Desktop, tarayıcı üzerinden GitHub.com, VS Code veya terminal hepsi aynı sonucu verir. Nasıl rahat ediyorsanız öyle çalışın.

## 3. Commit nedir?

Commit, deponuzun o anki hâlinin **imzalı bir fotoğrafıdır**. Her commit'in:

- **bir kimliği (hash)** vardır — kısa hâliyle `a3f92b1` gibi görünür; kanıt yorumlarında bunu kullanırsınız,
- **bir yazarı** vardır — kimin neyi yaptığını gösterir; bireysel eşikler commit geçmişinden okunur,
- **bir mesajı** vardır — ne yaptığınızı kısa ve emir kipinde anlatır.

İyi commit mesajları:

```text
H2 ısınma — prova-ali.csv eklendi (10 satır)
README: şirket adı düzeltildi
Fixes #7 — hatalı satır sayısı düzeltildi
```

Kötü commit mesajları: `update`, `değişiklikler`, `son hali`, `dosya`.

## 4. Issue nedir?

Issue, GitHub'daki **görev kaydıdır**. Bu derste size gelen her iş bir Issue'dur; sizin de açacağınız işler Issue olacak.

Bir görev Issue'sunda şu üç şeyin olması zorunludur (dönem planı §2.1):

1. **Son tarih** — ne zamana kadar?
2. **Kabul kriteri** — tek cümlelik "bitmiş" tanımı (örn. *"`data/prova-ali.csv` dosyası senin commit'inle depoda; 10 satır veri içeriyor"*)
3. **Atanan (assignee)** — iş kime ait?

### Kanıt yorumu

İşi bitirdiğinizde Issue'yu **kanıt yorumu olmadan kapatmayın**. Şablon:

```text
Tamamlandı — commit a3f92b1, dosya: data/prova-ali.csv (10 satır)
```

Bu yorum, yaptığınız işi commit'e bağlar; süreç notu bu bağlantılardan okunur. Yorumsuz kapatılan Issue, iz bırakmamış sayılır.

### `Fixes #n` — hata-düzeltme bağı

Bir hata Issue'sunu düzeltirken commit mesajınıza `Fixes #7` yazarsanız, commit main'e girdiğinde **Issue otomatik kapanır**. Görev 1'deki bug akışının merkezinde bu vardır: bir hata bildirilir → düzeltilir → commit `Fixes #n` ile bağlanır → Issue kanıtla kapanır.

## 5. Pull, Push ve Fetch arasındaki fark

| Komut | Yön | Ne yapar | Ne zaman |
|---|---|---|---|
| `fetch` | uzak → bilgisayar (bakar) | Uzakta ne olduğunu gösterir, birleştirmez | Merak ettiğinizde |
| `pull` | uzak → bilgisayar | Uzaktaki yeni commit'leri dosyalarınıza getirir | **Her çalışma başında** |
| `push` | bilgisayar → uzak | Commit'lerinizi ekibin görmesi için uzak depoya yazar | **Her commit'ten sonra** |

Bilgisayarınızda commit'leyip push etmeyi unutursanız: siz yaptınız ama depoda yoktur → §3.3 gereği yapılmamıştır. Push etmeden ayrılmayın.

## 6. Branch ve Pull Request (Görev 2'den itibaren zorunlu)

**Hafta 5'ten itibaren yeni kural:** `main` dalına doğrudan commit atılmaz. Her şey **branch + Pull Request** yoluyla girer.

- **Branch (dal)** — depoyu bozmadan izole çalışmak için açtığınız kol. Adlandırma örneği: `feature/veri`, `feature/gorsel`.
- **Pull Request (PR)** — "dalımı main'e katın" isteği. PR açınca ekibiniz değişikliğinizi **dosya dosya, satır satır** görebilir.
- **İnceleme yorumu** — PR'ın altına somut yorum yazmak ("bu sütun eksik", "şu satır hatalı"). Görev 2'de BE'nin PR'ında en az 2 somut inceleme yorumu istenir; inceleyen DQ'dur.
- **Merge** — PR incelemeden geçtikten sonra dalın main'e katılması. Merge sonrası branch silinir.

Akış: `pull` → `branch aç` → `değişiklik + commit + push` → `PR aç` → `inceleme yorumları` → `merge`.

## 7. Project Board (Pano)

Her grubun **Projects** sekmesinde 4 sütunlu bir panosu olacak:

```text
To Do  →  In Progress  →  Review  →  Done
```

Issue açıldığında kart `To Do`'ya düşer. Bir işe başladığınızda kartınızı `In Progress`'e, incelemeye gönderdiğinizde `Review`'a, kanıtla kapattığınızda `Done`'a sürükleyin. Pano, ekibinizin nerede durduğunu bir bakışta gösterir — ve PM'niz raporunu buradan yazar.

## 8. Etiket, Milestone, Release

- **Etiket (label)** — Issue'ları türüne göre işaretler. Görev 1'de en az 2 adet `bug` etiketli Issue açacaksınız.
- **Milestone** — Issue'ları bir görev paketine bağlar ("Görev 2"). Panoda ve Issue sayfasında aynı görevin işlerini topluca gösterir.
- **Release** — göreve görece sabit bir versiyon. Görev teslimleri release ile yapılır: Görev 1'in teslimi **`gorev1-final`** adlı release'dir. Release yoksa görev teslim edilmemiş sayılır.

## 9. Ders kurallarına bağ

Bu rehberdeki her şey şu üç plan kuralına hizmet eder:

1. **§3.3 — "GitHub'da yoksa, yapılmamıştır."** Her işin izi commit + Issue + yorum'dur.
2. **§2.1 — Issue düzeni.** Son tarih, kabul kriteri, atanan zorunlu.
3. **§2.2 — PR kuralı.** Hafta 5'ten itibaren main'e doğrudan commit yok.

Ayrıntılar dönem planında: [`AGENTS.md`](AGENTS.md)

## 10. En sık yapılan beş hata

| Hata | Sonucu | Doğrusu |
|---|---|---|
| Commit'leyip push etmemek | İş ekipte görünmez | Her commit'ten sonra push |
| Kanıt yorumu yazmadan Issue kapatmak | İş "iz bırakmadı" sayılır | Kapatmadan önce kanıt yorumu |
| Pull yapmadan çalışmaya başlamak | Çakışma, ezilen dosya | Her başlangıçta pull / Fetch origin |
| README'de başkasının satırını ezerek yazmak | Ekip bilgisi kaybolur | Yalnız kendi satırınızı değiştirin |
| `update` gibi anlamsız commit mesajı | Kimse ne yaptığınızı anlayamaz | Kısa, emir kipi, dosya adıyla |

---

## Sözlük — bir bakışta

| Terim | Anlamı |
|---|---|
| Org (organizasyon) | Depoların çatısı: `MAKU-VBA-GBT-II` |
| Repo (depolar) | Dosyalar + tüm geçmiş |
| README | Deponun vitrin sayfası |
| clone | Depoyu bilgisayara indirme (bir kez) |
| pull / Fetch | Uzaktan yeni commit'leri alma |
| commit | İmzalı değişiklik kaydı (hash + yazar + mesaj) |
| push | Commit'leri uzak depoya gönderme |
| Issue | Görev kaydı (son tarih + kabul kriteri + atanan) |
| Kanıt yorumu | İşi commit'e bağlayan kapanış yorumu |
| `Fixes #n` | Commit ile Issue'yu otomatik bağlayan/kapatan ifade |
| Branch | İzole çalışma dalı (`feature/veri`) |
| Pull Request | Dalın main'e katılma isteği (incelemeli) |
| Merge | PR'ın onaylanıp main'e katılması |
| Project Board | To Do / In Progress / Review / Done panosu |
| Milestone | Issue'ları göreve bağlayan paket |
| Release | Görev teslimi (`gorev1-final`) |
| Label (etiket) | Issue türü işareti (`bug`) |
