# LYK-2026-YAZ

[Türkçe](#türkçe) · [English](#english)

---

## Türkçe

Sınıfta işlediğimiz derslerin ortak arşivi. **Ders notları, slaytlar, ödevler,
simülasyonlar, örnek kodlar ve e-kitaplar** burada toplanır.

Bu repoyu öğrenciler birlikte yürütür — bir "öğretmen" ya da teslim sistemi
yoktur. Herkes elindeki materyali yükler, herkes ihtiyacı olanı buradan alır.

### 30 saniyede kural

> **Materyalin hangi konuya ait?** → `topics/<konu>/`
> **Ne tür bir dosya?** → o konunun içindeki alt klasör
> **Hiçbir konuya ait değil mi, emin değil misin?** → [`resources/`](resources/)
> **Kendi tanıtımın mı?** → [`resources/cv/`](resources/cv/)

### Ne nereye koyulur?

| Elimde bu var | Buraya koy |
|---|---|
| Ders notu (`.md`, `.pdf`) | `topics/<konu>/notes/` |
| Sunum / slayt | `topics/<konu>/slides/` |
| Ödev ya da ödev çözümü | `topics/<konu>/assignments/` |
| Simülasyon, notebook | `topics/<konu>/simulations/` |
| Örnek kod | `topics/<konu>/examples/` |
| **E-kitap, makale, cheat sheet** | `topics/<konu>/books/` |
| **Kendini tanıtan sunum / CV** | [`resources/cv/`](resources/cv/) |
| Hiçbir konuya ait olmayan her şey | [`resources/`](resources/) — aşağıya bak |

### Dosya adlandırma

Her materyal **sahibinin adıyla ve sürüm numarasıyla** durur:

```
Ad Soyad - Konu - v1.pdf
```

Örnek: `Sevgi Deniz - Kara Delikler ve Olay Ufku - v1.pdf`

- **Türkçe karakter ve boşluk serbest** — dosya adı ilk bakışta okunsun.
- **Sürüm:** ilk yüklemede `v1`. Aynı çalışmanın yeni halini eklerken eskisini
  silme, yanına `v2` olarak koy.
- **Sahibi olmayan ortak kaynaklar** (whitepaper, ders notu, çeviri) isimsiz
  yazılır: `Konu - v1.pdf` — örn. `Bitcoin Whitepaper (TR) - v1.pdf`
- Aynı kişinin aynı konuda birden fazla varyantı varsa ayırt edici kısmı
  parantez içinde ekle: `Musa Buğra Demir - Bitcoin Özeti (Marked) - v1.pdf`

Bu kural sayesinde bir klasöre bakınca **kimin neyi hazırladığı** ve
**hangi sürümün elde olduğu** dosya adından anlaşılır.

### Klasör iskeleti

```
LYK-2026-YAZ/
├── README.md                   # bu dosya
├── .gitignore
├── resources/                  # hiçbir konuya ait olmayan kaynaklar
│   ├── README.md
│   ├── cv/                     # kendini tanıtan sunumlar (Ben Kimim)
│   ├── books/                  # konu bağımsız e-kitaplar
│   ├── guides/                 # kurulum ve araç rehberleri (Git, Python…)
│   ├── cheatsheets/            # kısa başvuru kağıtları
│   ├── slides/                 # konu dışı sunumlar, seminerler
│   ├── videos/                 # video kayıtları / bağlantı listeleri
│   └── misc/                   # yeri belli olmayan her şey
└── topics/                     # her konu kendi klasöründe
    ├── _TEMPLATE/              # yeni konu açarken kopyalanacak şablon
    │   ├── README.md
    │   ├── notes/              # ders notları
    │   ├── slides/             # sunum ve slaytlar
    │   ├── assignments/        # ödevler ve çözümleri
    │   ├── simulations/        # simülasyonlar, notebook'lar
    │   ├── examples/           # örnek kodlar
    │   └── books/              # e-kitaplar, makaleler
    ├── ai/                                          # aynı alt klasörler
    ├── astronomy/                                   # aynı alt klasörler
    ├── big(o)-notations/                            # aynı alt klasörler
    ├── blockchain/                                  # aynı alt klasörler
    ├── cryptography/                                # aynı alt klasörler
    └── rotation-functions-in-different-dimensions/  # aynı alt klasörler
```

Her konu klasörü **aynı altı alt klasörü** içerir — bir konuda nasıl
çalıştığını öğrenirsen hepsinde aynıdır.

`topics/_TEMPLATE/` bir şablondur, **içine dosya konmaz**; yeni konu açarken
kopyalanır.

### Konuya bağlanamayan kaynaklar

Bir materyal tek bir derse ait değilse — genel bir e-kitap, Git kurulum
rehberi, bir seminer sunumu, faydalı bir video listesi — [`resources/`](resources/)
altına gider. Oradaki alt klasörler: `cv/`, `books/`, `guides/`, `cheatsheets/`,
`slides/`, `videos/`, `misc/`.

Kendini tanıtan "Ben Kimim" sunumları [`resources/cv/`](resources/cv/) altında
toplanır. Henüz bir konu klasörü olmayan tek seferlik sunumlar
[`resources/slides/`](resources/slides/) altında durur; o konudan ikinci bir
materyal gelirse yeni bir `topics/<konu>/` açıp oraya taşırız.

**Emin değilsen `resources/misc/` klasörüne koy.** Yanlış konunun altına
gömülmesindense burada durması iyidir; sonradan yeri belli olursa taşırız.

### Konular

| Konu | Klasör |
|---|---|
| Yapay Zeka | [`topics/ai/`](topics/ai/) |
| Astronomi | [`topics/astronomy/`](topics/astronomy/) |
| Big(O) Notasyonu | [`topics/big(o)-notations/`](topics/big%28o%29-notations/) |
| Blockchain | [`topics/blockchain/`](topics/blockchain/) |
| Kriptografi | [`topics/cryptography/`](topics/cryptography/) |
| Farklı Boyutlarda Rotasyon Fonksiyonları | [`topics/rotation-functions-in-different-dimensions/`](topics/rotation-functions-in-different-dimensions/) |

### Nasıl yüklerim?

1. Yukarıdaki tablodan dosyanın gideceği yeri bul.
2. Dosyayı **Dosya adlandırma** bölümündeki kurala göre adlandır:
   `Ad Soyad - Konu - v1.pdf`
3. Aynı çalışmanın güncel halini yüklüyorsan eskisini silme, sürümü artır (`v2`).
4. Commit at ve gönder (ya da pull request aç).

**E-kitaplar için:** serbestçe paylaşılabilen ve 25 MB'tan küçük dosyaları
doğrudan `books/` klasörüne koy. Dosya büyükse ya da telifliyse **yükleme** —
ilgili `README.md` dosyasındaki kaynak tablosuna bağlantı ekle.

### Yeni konu nasıl açılır?

1. `topics/_TEMPLATE/` klasörünü kopyala ve konu adıyla yeniden adlandır
   (küçük harf, tireli): `topics/lineer-cebir/`
2. İçindeki `README.md` dosyasındaki `<...>` yerlerini doldur, en üstteki
   açıklama satırlarını sil.
3. Yukarıdaki **Konular** tablosuna bir satır ekle.

---

## English

A shared archive for the courses we cover in class: **lecture notes, slides,
assignments, simulations, example code and e-books** all live here.

This repo is run by the students together — there is no "teacher" and no
submission system. Everyone uploads what they have, everyone takes what they need.

### The rule in 30 seconds

> **Which topic is it about?** → `topics/<topic>/`
> **What kind of file is it?** → the matching subfolder inside that topic
> **Not tied to any topic, or unsure?** → [`resources/`](resources/)
> **Your own intro deck?** → [`resources/cv/`](resources/cv/)

### Where does it go?

| What you have | Put it here |
|---|---|
| Lecture notes (`.md`, `.pdf`) | `topics/<topic>/notes/` |
| Presentation / slides | `topics/<topic>/slides/` |
| Assignment or its solution | `topics/<topic>/assignments/` |
| Simulation, notebook | `topics/<topic>/simulations/` |
| Example code | `topics/<topic>/examples/` |
| **E-book, paper, cheat sheet** | `topics/<topic>/books/` |
| **Personal intro deck / CV** | [`resources/cv/`](resources/cv/) |
| Anything not tied to a topic | [`resources/`](resources/) — see below |

### File naming

Every file carries **its author's name and a version number**:

```
Ad Soyad - Konu - v1.pdf
```

Example: `Sevgi Deniz - Kara Delikler ve Olay Ufku - v1.pdf`

- **Spaces and Turkish characters are fine** — names should be readable at a glance.
- **Version:** start at `v1`. When you upload a newer take on the same work,
  don't delete the old one — add it as `v2` alongside.
- **Shared sources with no personal author** (whitepapers, lecture notes,
  translations) drop the name: `Konu - v1.pdf`, e.g. `Bitcoin Whitepaper (TR) - v1.pdf`
- If one person has several variants of the same work, put the distinguishing
  part in parentheses: `Musa Buğra Demir - Bitcoin Özeti (Marked) - v1.pdf`

This way a single glance at a folder tells you **who made what** and **which
version you have**.

### Folder structure

```
LYK-2026-YAZ/
├── README.md                   # this file
├── .gitignore
├── resources/                  # material not tied to any topic
│   ├── README.md
│   ├── cv/                     # personal intro decks ("Ben Kimim")
│   ├── books/                  # topic-independent e-books
│   ├── guides/                 # setup and tool guides (Git, Python…)
│   ├── cheatsheets/            # quick reference sheets
│   ├── slides/                 # off-topic talks, seminars
│   ├── videos/                 # recordings / link lists
│   └── misc/                   # anything that fits nowhere else
└── topics/                     # one folder per topic
    ├── _TEMPLATE/              # skeleton to copy when adding a new topic
    │   ├── README.md
    │   ├── notes/              # lecture notes
    │   ├── slides/             # presentations and slides
    │   ├── assignments/        # assignments and solutions
    │   ├── simulations/        # simulations, notebooks
    │   ├── examples/           # example code
    │   └── books/              # e-books, papers
    ├── ai/                                          # same subfolders
    ├── astronomy/                                   # same subfolders
    ├── big(o)-notations/                            # same subfolders
    ├── blockchain/                                  # same subfolders
    ├── cryptography/                                # same subfolders
    └── rotation-functions-in-different-dimensions/  # same subfolders
```

Every topic folder has **the same six subfolders** — learn one topic and you
know your way around all of them.

`topics/_TEMPLATE/` is a skeleton — **don't put files in it**; copy it when
starting a new topic.

### Material that fits no topic

If something isn't tied to a single course — a general e-book, a Git setup
guide, a seminar deck, a useful video list — it goes under
[`resources/`](resources/), which holds `cv/`, `books/`, `guides/`,
`cheatsheets/`, `slides/`, `videos/` and `misc/`.

Personal "Ben Kimim" intro decks collect in [`resources/cv/`](resources/cv/).
One-off talks with no matching topic folder sit in
[`resources/slides/`](resources/slides/); once a second file shows up on the
same subject we open a `topics/<topic>/` folder and move them there.

**When in doubt, drop it in `resources/misc/`.** Better there than buried under
the wrong topic; we can move it once its place is clear.

### Topics

| Topic | Folder |
|---|---|
| Artificial Intelligence | [`topics/ai/`](topics/ai/) |
| Astronomy | [`topics/astronomy/`](topics/astronomy/) |
| Big(O) Notation | [`topics/big(o)-notations/`](topics/big%28o%29-notations/) |
| Blockchain | [`topics/blockchain/`](topics/blockchain/) |
| Cryptography | [`topics/cryptography/`](topics/cryptography/) |
| Rotation Functions in Different Dimensions | [`topics/rotation-functions-in-different-dimensions/`](topics/rotation-functions-in-different-dimensions/) |

### How do I upload?

1. Find the destination in the table above.
2. Name the file following the **File naming** section:
   `Ad Soyad - Konu - v1.pdf`
3. Uploading a newer take on existing work? Don't delete the old file — bump
   the version (`v2`).
4. Commit and push (or open a pull request).

**For e-books:** put freely shareable files under 25 MB directly into `books/`.
If a file is larger or copyrighted, **don't upload it** — add a link to the
resource table in the relevant `README.md` instead.

### How do I add a new topic?

1. Copy `topics/_TEMPLATE/` and rename it after the topic
   (lowercase, hyphenated): `topics/lineer-cebir/`
2. Fill in the `<...>` placeholders in its `README.md` and delete the note
   at the top.
3. Add a row to the **Topics** table above.
