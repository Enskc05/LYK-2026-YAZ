# Yapay Zeka / Artificial Intelligence

**TR:** Yapay zekanın temelleri, makine öğrenmesi ve derin öğrenme yaklaşımları, modellerin eğitimi ve uygulama alanları.
**EN:** Foundations of artificial intelligence, machine learning and deep learning approaches, model training and application areas.

## Ne nereye? / What goes where?

| Klasör / Folder | Buraya koy / Put here |
|---|---|
| [`notes/`](notes/) | Ders notları · Lecture notes |
| [`slides/`](slides/) | Sunum ve slaytlar · Presentations and slides |
| [`assignments/`](assignments/) | Ödevler ve çözümleri · Assignments and solutions |
| [`simulations/`](simulations/) | Simülasyonlar, notebook'lar · Simulations, notebooks |
| [`examples/`](examples/) | Örnek kodlar · Example code |
| [`books/`](books/) | E-kitaplar, makaleler, cheat sheet'ler · E-books, papers, cheat sheets |

## E-kitaplar ve kaynaklar / E-books and resources

Serbestçe paylaşılabilen dosyaları `books/` klasörüne koy. Dosya 25 MB'tan
büyükse ya da telifliyse dosyayı yükleme — aşağıdaki tabloya bağlantı ekle.
_Put freely shareable files in `books/`. If a file is over 25 MB or
copyrighted, don't upload it — add a link to the table below instead._

| Ad / Title | Tür / Type | Bağlantı / Link |
|---|---|---|
| _(henüz yok / none yet)_ | | |


## Bu slaytları hazırlarken neyden ne kadar faydalanıldı?

Bu dokümanın tamamı **Claude Opus 5** (Anthropic) ile high efor ile, tek bir prompt üzerinden üretildi.

**Kullanılan prompt:**

> Abi selam sayısal kriptografi ve blockchain ile ilgili 7 gün sürecek bir ders var. Bana 7 gün sürecek şekilde pdf hazırla ve içerisinde de alt başlıklarını yapay zekaya soracağım promptları da hazırla ona göre bir pdf sunumu hazırla kısacası alt başlıklarını da öğretecek bir pdf hazırla

**Üretilen çıktı:** 27 sayfalık PDF · 7 günlük müfredat · 38 alt başlık · 110+ hazır prompt.
Model, içeriği yazmakla kalmadı; PDF'i Python (ReportLab) ile kendi yazdığı tasarım koduyla oluşturdu ve sayfaları görsel olarak kontrol edip düzeltti.

### Token kullanımı

| | Karakter | ≈ Token |
|---|---:|---:|
| İçerik dosyası (`icerik.py` — 7 günün metni ve promptlar) | 52.996 | ~21.000 |
| PDF üretim/tasarım kodu (`olustur.py`) | 17.588 | ~5.300 |
| Sohbet yanıtları ve düzeltmeler | ~4.000 | ~1.600 |
| Model içi akıl yürütme (reasoning) | — | ~2.000–4.000 |
| **Toplam üretim (output)** | | **~30.000** |

Girdi tarafında kullanıcı prompt'u yalnızca **~60 token**. Asıl yük, üretim sırasındaki
**14 araç çağrısından** geliyor: her çağrıda tüm bağlam yeniden gönderildiği için
bağlam ~15.000'den ~50.000 token'a büyüdü ve kümülatif girdi
**~450.000 token** seviyesine ulaştı.

> **Not:** Bu rakam gerçek maliyetten yüksek görünür. Prompt caching sayesinde tekrar
> eden bağlamın büyük kısmı indirimli işlenir; efektif maliyet yaklaşık
> **60.000–100.000 tam fiyatlı input token** seviyesindedir.

### Özetle

| Kaynak | Katkı |
|---|---|
| Claude Opus 5 | İçerik, müfredat kurgusu, promptlar, PDF tasarımı ve kodu |
| İnsan katkısı | Konu belirleme ve tek satırlık yönlendirme (~60 token) |
| Harici kaynak | Yok — dış veri çekilmedi, tüm içerik modelin bilgisiyle üretildi |
