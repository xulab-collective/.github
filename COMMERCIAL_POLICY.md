```text
X U L A B   C O L L E C T I V E  //  C O M M E R C I A L   P O L I C I E S   &   T E M P L A T E
[ YAZILIM TÜZEL POLİTİKALARI · MİNİMUM HAVUZ ORANLARI · KURUCU BAZ PUANI · PROJE BEYANNAMESİ ]
```

> **[ [MANIFESTO // MANİFESTO](MANIFESTO.md) ]** · **[ [PROTOCOL // KURAL KİTABI](PROTOCOL.md) ]** · **[ [ROADMAP // YOL HARİTASI](ROADMAP.md) ]** · **[ [TR // TÜZEL POLİTİKALAR](#tr--xulab-tüzel-politikalar-minimum-paylar-ve-proje-başlangıç-rehberi) ]** · **[ [EN // COMMERCIAL POLICIES](#en--xulab-commercial-policies-minimum-floors--project-charter-guide) ]**

---

# TR // XULAB TÜZEL POLİTİKALAR, MİNİMUM PAYLAR VE PROJE BAŞLANGIÇ REHBERİ

Bu belge, **Xulab Collective** çatısı altında **Yazılım, Motor ve AI Geliştirme** amacıyla **Model B Tüzel ve Çift Lisanslı** veya **Model A Tamamen Ücretsiz `AGPLv3`** proje başlatmak isteyen geliştirici ve şirketler için hazırlanmış **standart referans tablosu ve hazır başlangıç şablonudur**.

> **SÜRÜM VE TASLAK ORANLAR NOTU // `v1.0 (FINE-TUNE AŞAMASINDA)`:** Bu belgedeki yüzdeler, puan aralıkları ve `vesting-cap-decay` çarpanları **kesinleşmiş katı kurallar değil, başlangıç için hazırlanmış taslak referans aralıklarıdır**. Kesin oranlar ince ayar (`fine-tune`) aşamasındadır ve her projenin kendi başında (kimin hangi görevi yaparsa ne kadar pay alacağıyla birlikte) proje şartnamesinde (`Charter`) netleştirilir.

> **ÖNCE NETLEŞTİRELİM: SİSTEMİN TÜM MANTIĞI (`2 MÜLKİYET YAPISI`)**  
> 1. **Açık Kaynak (`Müşterek Mal = AGPLv3`):** Kodları açık tuttuğun sürece kendin geliştir ve kendi işlerinde kullan. Kodu kapatıp ticari bir yazılım ürünü olarak satmadığın sürece her kullanıma açıktır; tek şartı açık kalmak zorunda olmasıdır.  
> 2. **Ticari Proje (`Commercial Project = Açık Çekirdek + Dual-License`):**  
>    - Çekirdeği ve temel kullanımları diğer insanlar geliştirebilsin diye açık olmalıdır (`JUCE` / `Unreal Engine` mantığı).  
>    - Ticari kısmını ve ticari değer getiren kısmını kendi ticari lisansına göre yapabilirsin. Lisans `Dual-License` olmalıdır:  
>      - **Freelancer (`Individual`):** Bağımsız üreticiler için makul düzeyde olmalıdır.  
>      - **Commercial (`B2B / Kurumsal`):** B2B çalışanlara veya şirketlere istediğin ticari bedeli kesebilirsin.  
> 3. **Xulab Bir Dağıtımcı Değildir; Ödeme Çatıya Değil Bireye Olur:** Xulab altında geliştirilmemiş veya şartları karşılamayan hiçbir şey Xulab’a ait değildir. Xulab bir dağıtımcı (publisher) değil, ortak AR-GE ve ürün geliştirme kolektifidir. Ticari projeyi Xulab çatısı altında geliştirdiysen, **ödeme çatıya değil, doğrudan burada senin yazılımın için çalışan ve `feature` geliştiren insanlara (bireylere)** kâr üzerinden yapılır (çatı en fazla `%1–2` sunucu gideri vs. alırsa alır).  
> 4. **Tüm Mantığı Bu:** *Buraya gel, buradaki insanlarla bir şeyler üret, istiyorsan ticari sat. Ama bağımsız üreticiye adil ol ve burada emeğini kullandığın yazılımcılara geri ödeme yap.*

> **KAPSAM AYRIMI // YAZILIM GELİŞTİRME VE PİYASA MEDYA HİZMETİ:**  
> Bu belgedeki `Dual-License` gelir havuzu ve puan sistemi **yalnızca Yazılım, DSP ve AI Araç Geliştirme** projeleri içindir.  
> **Piyasada yürütülecek medya üretimi ve post-prodüksiyon hizmet projelerinin kazançları bu yazılım havuzundan tamamen bağımsızdır ve yüzde yüz olarak doğrudan işi üstlenen aktif proje ekibine bırakılır.** Sahada medya ve post-prodüksiyon işi yapan ekiplerin de Xulab Manifestosu'ndaki taşeron sömürüsü yapmama, mobbing yasağı ve ekip içi şeffaf ve adil paylaşım ilkelerine uyması zorunludur.

---

## 01 // YAZILIM KATKICI KÂR PAYI HAVUZU: MİNİMUM TABAN VE TAVSİYE EDİLEN ORANLAR

> **Hesaplama Kuralı // Net Ticari Gelir:** Havuz payı `%X`, ödeme altyapısı komisyonları ve varsa doğrudan bulut GPU/API sunucu faturası düşüldükten sonra kalan **Net Lisans ve Hizmet Geliri** üzerinden hesaplanır.

| Yazılım Proje Kategorisi | Zorunlu Minimum Taban | Tavsiye Edilen Standart Oran | Kapsam ve Açıklama |
| :--- | :---: | :---: | :--- |
| **1. Saf Yazılım ve Lokal Motor**<br>*DAW, NLE, DSP Eklentisi, Masaüstü ve CLI Araçları* | **Min. `%10`** | **`%12 – %15`**<br>*Tavan: `%20`* | Sunucu ve GPU maliyeti olmayan, çekirdeği `AGPLv3` açık kaynak olup kurumsal sektöre `Dual-License` satan projeler. |
| **2. Hibrit: Açık Motor ve Özel Eğitilmiş AI Ağırlıkları**<br>*Lokal/Şifreli Ağırlıklar + Ticari Lisans* | **Min. `%7.5`** | **`%10 – %15`** | Tüzel kişiliğin yüksek veri temizliği, telif ve model eğitimi maliyeti üstlendiği hibrit AI ve DSP projeleri. |
| **3. Yoğun Bulut ve GPU Servisi**<br>*Bulut Tabanlı AI, Mix ve Render* | **Min. `%5`** *Net* | **`%10 – %12`** *Net* | Doğrudan bulut GPU ve VRAM faturası düşüldükten sonra kalan net hizmet geliri üzerinden dağıtılır. |
| **4. Xulab Ortak Altyapı ve AR-GE Kesintisi** | **`%0 – %2.5`** | **`%1 – %2`** | Xulab'ın ortak sunucu, test ve organizasyon altyapısını kullanan tüzel projelerin kolektif AR-GE kasasına bıraktığı sembolik pay. |

---

## 02 // ÖRNEK GÖREV PUANLAMA MODELİ, KURUCU BAZ PUANI VE TIER AYRIMI

> **PROJE BAŞI ŞEFFAFLIK İLKESİ (`EX-ANTE CHARTER`):**  
> Xulab’da tüm projelere yukarıdan tek tip bir şablon dayatılmaz; her otonom proje ekibi kendi puanlama ve hak ediş yapısını kendi doğasına göre kurmakta özgürdür. **Tek zorunlu lonca kuralı; kurucu baz puanının, görev puanlama yönteminin ve hak ediş sürelerinin daha projenin ilk gününden (`Proje Başında`) `XULAB_CHARTER.md` içinde açıkça ilan edilmesi ve sonradan emekçi aleyhine değiştirilmemesidir.** Aşağıdaki yapı, projelerin doğrudan kullanabileceği **önerilen standart referans modeldir**:

### 1. Örnek Görev Puanlama Yaklaşımı (İş Öncesi Şeffaf Puanlama)
Saat bazlı mesai takibi yerine, açılan her mühendislik görevinin (`Issue`) kodlama başlamadan önce zorluk ve katman değerine göre puanlanması tavsiye edilir:
- **Örnek Formül:** $\text{Görev Puanı} = \text{Zorluk } (1..13 \text{ Fibonacci}) \times \text{Katman Çarpanı } (\text{Core/DSP/AI: } 3\text{x}, \text{ Protokol/AAF/MCP: } 2\text{x}, \text{ UI/Araç: } 1\text{x}) \times \text{Erken Faz Riski } (1\text{x}..3\text{x})$.
- Küçük ekiplerde (`Minimum Viable Guild`) puanlamayı doğrudan `Project Lead` belirler; ekip büyüdükçe ortak oylama veya sahipsiz kalan görevlerin puanını otomatik artırma yöntemleri kullanılabilir.

### 2. Kurucu Çekirdek Puanı // Havuz Koruma Kuralı (Örnek Referans)
- Proje dış katkıya açılırken, kurucu ekibin ortaya koyduğu mevcut çekirdek kod ve mimari puan havuzunun tabanını (örneğin `v1.0` hedef havuzunun `%65–%75`'ine denk gelen sabit bir sayı, **örn. `10.000 Puan`**) oluşturur ve proje başında `Charter` içine yazılır.
- Dışarıdan katılan bir Co-Yazılımcı `1.000 Puanlık` görev tamamladığında havuzun $\frac{1.000}{10.000 + 1.000} = \%9.09$’unu alır; kalan `%90.91` kurucu ekipte kalır. Böylece **küçük bir katkının tüm havuzu yutması matematiksel olarak engellenir; dışarıdan ne kadar gerçek mühendislik katkısı gelirse havuzdan sadece o kadarı çıkar.**

### 3. Co-Yazılımcı Kâr Havuzu ve Debug/QA Lisans Ödülü Ayrımı
Maaş ödemeden üst düzey mühendis çekmek ile saha testçilerini ödüllendirmek birbirine karıştırılmaz:

| Katkı Seviyesi ve Discord Rolü | Kimler Dahildir? | Karşılık, Yetki ve Ödüllendirme Modeli | Puanlama Modeli |
| :--- | :--- | :--- | :---: |
| **`Tier 0` // Community** | Topluluğa katılan tüm üyeler ve açık kaynak kullanıcıları | Tüm açık kaynak `AGPLv3` araçlara, ortak AR-GE kanallarına ve açık eğitimlere ücretsiz erişim | **Açık Erişim** |
| **`Tier 1` // Tester & Creator** | Saha testi ve debug yapanlar, somut bug raporu paylaşanlar, video/eğitim/içerik üretenler, küçük yama gönderenler ve aktif destek verenler | **Kâr havuzuna girmez:** **İlk 50 Seçkisi Doğrudan `Lifetime V1 Access` / Ücretsiz Pro Lisans** ve proje kâra geçtiğinde **Tek Seferlik Ödül (`Bug Bounty`)** | **Lifetime V1 Access ve Sabit Ödül** |
| **`Tier 2` // Major Developer** | Yeni fonksiyonel modül, major feature, masaüstü UI/UX mimarisi, yeni DAW/format entegrasyonu ve algoritma geliştirenler | **Kâr Payı Havuzu Ortağı** | **Proje Başında İlan Edilen Görev Puanı (`Örn: Zorluk × Katman × Risk`)** |
| **`Tier 3` // Council & Team Lead** | Hem çekirdek mimari, DSP/AI motoru geliştiren Major Developer ve Team Lead olan, hem de tüm Manifesto, Protokol ve Meclis kurallarını eksiksiz kabul etmiş **Üretici Meclisi** üyeleri | **Kâr Payı Havuzu Ortağı + Üretici Meclisi Üyeliği + Proje `Lead / Council Sponsor` Yetkisi** | **Proje Başında İlan Edilen Görev Puanı (`Örn: Zorluk × Katman × Risk`)** |

---

## 03 // HAK EDİŞ, MOLA HAKKI VE ERİME (ÖRNEK REFERANS DEĞERLERİ)

> **Not:** Aşağıdaki süre ve oranlar **örnek referans aralıklarıdır**. Her proje kendi sürelerini **proje başında (`XULAB_CHARTER.md` içinde)** netleştirerek ilan eder:

| Mekanizma | Örnek Referans Aralığı | Tavsiye Edilen Standart Örnek | Lonca ve Emek Koruma Mantığı |
| :--- | :---: | :---: | :--- |
| **1. `Cliff` // Kod Olgunlaşma Süresi** | **Örn: `3 – 6 Ay`** | **`6 Ay` veya ilk ticari sürüm** | Kod `main` dalına girdikten sonra belirlenen süre boyunca çalışır durumda kalmalı ve temel hataları temizlenmelidir. Kötü niyetle kod silip puan yakmak geçersizdir. |
| **2. `Vesting` // Kademeli Hak Ediş** | **Örn: `%25 – %50` Cliff sonunda** | **`%25` 6. Ay + `%25 x 3 Sürüm`** | Puanın ilk dilimi `Cliff` sonunda kesinleşir; kalan kısmı takip eden sürümlerde bakım desteği verdikçe açılır. |
| **3. `Freeze` // İnsani Mola ve Dürüst Devir Hakkı** | **Örn: Yılda `30 – 45 Gün` Mola** | **Mola ve Dürüst Devirde `%0 Ceza`** | Yoğun prodüksiyon (`crunch`), hastalık veya mola dönemlerinde puan erimesi durur. Yazar yoğunluk nedeniyle acil bir hataya bakamayacağını dürüstçe bildirirse ceza uygulanmaz; yalnızca hatayı çözen arkadaşına küçük bir bakım payı (örn. `%15–%20`) aktarılır. Yalnızca haber vermeden projeyi tamamen terk edenlerde (`ghosting`) askıdaki puan kesintisi uygulanır. |
| **4. `Roll-off / Decay` // Pasiflik Erimesi** | **Örn: Yıllık `%15 – %35`** | **Yıllık `%25` Erime** | Mola hakkı dışında projeyi tamamen bırakan kişinin puanı yıllık bazda kademeli erir; böylece havuz aktif üretenleri beslemeye devam eder. |
| **5. `Cap` // Tavan Ödeme Çarpanı** | **Örn: `5x – 10x`** | **`5x – 8x` Nakit Çarpanı** | Katkıcının aldığı kümülatif ödeme, yaptığı işin başlangıç referans değerinin belirlenen katına ulaştığında o puanlar emekli olur. |
| **6. `Payout` // Dağıtım Takvimi** | **Örn: `Aylık` veya `3 Ayda Bir`** | **Her Çeyrek Sonu** | Havuz gelir tablosu şeffaf olarak açıklanır ve ödemeler düzenli periyotlarla dağıtılır. |

---

## 04 // KADEMELİ `DUAL-LICENSE` FİYATLANDIRMA REHBERİ

> **Bölgesel Satın Alma Gücü (`PPP`) ve Kapsam Sınırı Notu:**
> 1. **Yıllık `$50.000` (PPP-Uyarlı) Freelancer Sınırı ve Teknik Kapsam:** Tablodaki `$50.000` ve `$250.000` yıllık brüt gelir eşikleri küresel referans bantlarıdır ve her projenin kendi `Charter` belgesinde ülkeye (`PPP`) göre adil biçimde uyarlanır. Bağımsız emekçilerin banka hesabı denetlenmez; bunun yerine **Bireysel/Freelance (`<$50.000`)** lisanslar tekil kişisel iş istasyonu ve yerel kullanım kapsamındayken, çoklu koltuk (`Floating License`), paylaşımlı kurumsal ağ depolaması (`SAN / NAS`), toplu stüdyo otomasyonu ve kurumsal B2B fatura/SLA özellikleri **Butik / Kurumsal Stüdyo (`>$50.000`)** lisans kapsamındadır.
> 2. **Kurumsal Referans Ödülü (`Örn: %15 – %20 Finder's Fee`):** `Model B` projelerde, çalıştığı kurumsal stüdyonun ticari `Studio / Enterprise` lisansı satın almasına vesile olan emekçilere ilk yıl kurumsal lisans bedelinden doğrudan referans ödülü verilmesi tavsiye edilir.

| Kademe | Hedef Kitle | Lisans Türü | Tavsiye Edilen Fiyat Çarpanı |
| :--- | :--- | :--- | :--- |
| **Kademe 0 // Lokal Bağımsız, Kolektif ve Açık Kod** | Bağımsız emekçiler, öğrenciler, kolektifler ve ciro sınırı altındaki bireysel üreticiler | **`AGPLv3` ve `Copyfarleft` Ciro Sınırlı Açık Lisans** | **`$0` // Tamamen Ücretsiz** |
| **Kademe 1 // Indie ve Freelancer** | Yıllık brüt geliri `< $50.000` olan bağımsız profesyoneller | **Indie Ticari Lisans** | **`1x` Baz Fiyat // Erişilebilir** |
| **Kademe 2 // Butik Stüdyo** | Yıllık geliri `$50.000 – $250.000` arası, `2–5 koltuk` küçük ekipler | **Pro Ticari Lisans** | **`3x – 5x` Baz Fiyat // Koltuk başı** |
| **Kademe 3 // Kurumsal Sermaye** | Yıllık geliri `> $250.000` olan büyük post-prodüksiyon stüdyoları ve medya tekelleri | **Enterprise `Dual-License`** | **`10x – 25x` Baz Fiyat // Koltuk başı + SLA** |
| **Kademe 4 // 3. Parti Kapalı Şirketler** | Motoru veya modülü kendi kapalı ticari ürününe gömmek isteyen şirketler | **OEM `Dual-License`** | **Yüksek Peşin Lisans + Brüt Cirodan `%5 – %15` Pay** |

---

## 05 // HAZIR YAZILIM PROJE BAŞLANGIÇ BEYANNAMESİ // `XULAB_CHARTER.md`

Xulab bünyesinde bir projeye başlamak için izin almaya gerek yoktur; ancak projeye **özel Discord kanalları ve kolektif altyapı desteği talep edildiğinde** veya **`Model B` gelir paylaşımlı bir proje başlatıldığında**, aşağıdaki şablon doldurulup projenin ana dizinine `CONTRIBUTING.md` veya `XULAB_CHARTER.md` olarak eklenir ve **Xulab Üretici Meclisi** onayına sunulur:

```markdown
# XULAB SOFTWARE PROJECT CHARTER // YAZILIM PROJE BAŞLANGIÇ BEYANNAMESİ

- **Proje Adı:** [Örn: ProjectName]
- **Proje Yöneticisi // Chair / Project Lead:** [@kullanici_adi]
- **Meclis Sponsoru // Council Sponsor:** [@sponsor_kullanici_adi]
- **Proje Kapsamı // In-Scope & Out-of-Scope:** [Bu projenin ne yaptığı ve hangi alanlara karışmadığı]
- **Proje Modeli:** [ ] Model A // %100 Free AGPLv3  |  [ ] Model B // Tüzel / Açık Motor AGPLv3 + Dual-License
- **Tüzel Kişilik // Sadece Model B ise:** [Şirket Adı ve Ülke]
- **Açık Çekirdek ve Kaynak Lisansı:** [ ] Saf AGPLv3 // Model A  |  [ ] Copyfarleft Ciro Sınırlı Açık Lisans + AGPLv3 Derin SDK + Dual-License // Model B
- **Co-Yazılımcı Kâr Payı Havuzu Oranı // Model B:** Net Ticari Gelirin %[15]'i // Zorunlu Taban: %5-%10
- **Kurucu Çekirdek Baz Puanı // Founder Baseline:** [10.000 Puan]
- **Ödüllendirme Ayrımı:**
  - Tier 2 & Tier 3 // Major Developer & Council Lead: Slicing Pie Kâr Havuzu Ortağı
  - Tier 1 // Tester & Creator / Debug / QA / Video: Doğrudan Lifetime V1 Access / Ücretsiz Pro Lisans ve Tek Seferlik Bug Bounty
- **Hak Ediş Parametreleri // Model B:**
  - Cliff // Uçurum Süresi: [6 Ay]
  - Vesting // Kademeli Hak Ediş: [%25 Cliff sonunda + %75 takip eden 3 sürümde]
  - Pasiflik Erimesi // Annual Decay: [Yıllık %25]
  - Tavan Çarpanı // Payout Cap: [6x - 8x]
  - Dağıtım Periyodu: [Her Çeyrek Sonu / 3 Ayda Bir]
- **İdari Denetim ve Taahhüt:** Bu proje Xulab Collective Manifesto ve Protokolü'ne tabidir. İdari denetim Xulab Üretici Meclisi'ne, teknik yürütme Proje Yöneticisi'ne aittir.
```

---

# EN // XULAB COMMERCIAL POLICIES, MINIMUM FLOORS & PROJECT CHARTER GUIDE

This document defines the **mandatory minimum floors, Founder Baseline protection, Co-Developer vs. QA reward separation, and ready-to-use Project Charter template** for launching **Software, Engine, and AI Development** projects under **Xulab Collective**.

> **VERSION & DRAFT RATES NOTE // `v1.0 (BEING FINE-TUNED)`:** The percentages, point ranges, and `vesting-cap-decay` multipliers in this document are **draft reference ranges, not rigid final numbers**. Exact weights and task shares are currently being fine-tuned and are defined upfront at the start of each project in its `Charter`.

> **READ FIRST: THE ENTIRE LOGIC OF THE SYSTEM (`2 OWNERSHIP TIERS`)**  
> 1. **Open Source (`Shared Commons = AGPLv3`):** As long as you keep the code open, develop it and use it in your own work for `$0`. It is open to everything except enclosing and selling the code itself as a closed commercial software product; it must remain open commons.  
> 2. **Commercial Project (`Open Core + Dual-License`):**  
>    - Its core and foundational functionality must remain open so others can build on it (`JUCE` / `Unreal Engine` logic).  
>    - You license the commercial value-add part under your own commercial `Dual-License`:  
>      - **Freelancer (`Individual`):** Must remain fair and accessible for independent practitioners.  
>      - **Commercial (`B2B / Enterprise`):** You can charge corporate studios and B2B clients whatever commercial rate you set.  
> 3. **Xulab Is Not a Publisher; Payouts Go to Individual Builders, Not the Umbrella:** Nothing built outside Xulab or outside these terms belongs to Xulab. Xulab is a shared R&D and product development collective, not a publisher. If you develop a commercial project under Xulab, **payouts from profits go directly to the individual developers who built features for your software, not to the umbrella** (the umbrella takes at most `1%–2%` only if shared server costs apply).  
> 4. **The Entire Logic:** *Come here, build things with the people here, and sell commercially if you want. Just be fair to independent workers and pay back the developers whose labor you used here.*

> **SCOPE SEPARATION // SOFTWARE R&D vs. MARKET MEDIA SERVICES:**  
> The `Dual-License` revenue pool and point system defined here apply **strictly to Software, DSP, and AI Tool Development** projects.  
> **Revenues generated from market media production and post-production service engagements are completely independent of this software pool and belong 100% to the active squad executing the work**, provided the squad strictly adheres to the Xulab Manifesto: zero subcontractor exploitation, zero mobbing, and fair internal revenue sharing among the active team.

---

## 01 // SOFTWARE CONTRIBUTOR PROFIT POOL: MINIMUM FLOORS & RECOMMENDED RATES

| Software Project Category | Mandatory Minimum Floor | Recommended Standard Rate | Scope & Description |
| :--- | :---: | :---: | :--- |
| **1. Pure Software & Local Engine**<br>*DAW, NLE, DSP Plugins, Desktop/CLI Tools* | **Min. `10%`** | **`12% – 15%`**<br>*Max: `20%`* | Zero cloud cost projects keeping the core `AGPLv3` while selling `Dual-Licenses` to enterprise studios. |
| **2. Hybrid: Open Engine + Trained AI Weights**<br>*Local/Encrypted Weights + Commercial License* | **Min. `7.5%`** | **`10% – 15%`** | Hybrid AI/DSP projects where the legal entity funds heavy dataset curation, legal clearance, and model training. |
| **3. Heavy Cloud / GPU Service**<br>*Cloud AI, Mix, Render* | **Min. `5%`** *Net* | **`10% – 12%`** *Net* | Distributed from net service revenue after deducting direct cloud GPU/VRAM server bills. |
| **4. Xulab Shared Infrastructure / R&D Pool** | **`0% – 2.5%`** | **`1% – 2%`** | Symbolic contribution to Xulab's shared GPU, testing, and collective R&D treasury. |

---

## 02 // REFERENCE TASK SCORING MODEL, FOUNDER BASELINE & TIER SEPARATION

> **UPFRONT TRANSPARENCY PRINCIPLE (`EX-ANTE CHARTER`):**  
> Xulab does not impose a rigid central planning formula from above; every autonomous project squad is free to tailor its own scoring and vesting rules. **The single mandatory guild rule is that the founder baseline, task scoring method, and vesting timelines must be declared transparently upfront from day one (`At Project Inception`) in `XULAB_CHARTER.md` and never altered retroactively against contributors.** The structure below serves as our **recommended reference model**:

### 1. Reference Task Scoring Approach (Upfront Task Valuation)
Rather than tracking hours, projects are encouraged to score engineering `Issues` upfront before coding begins based on complexity and architectural layer:
- **Reference Formula:** $\text{Task Points} = \text{Difficulty } (1..13 \text{ Fibonacci}) \times \text{Layer Multiplier } (\text{Core/DSP/AI: } 3\text{x}, \text{ Protocol/AAF/MCP: } 2\text{x}, \text{ UI/Tools: } 1\text{x}) \times \text{Early Phase Risk } (1\text{x}..3\text{x})$.
- In small squads (`Minimum Viable Guild`), the `Project Lead` sets task points directly; larger squads may use peer voting or automatic point step-ups for unclaimed tasks.

### 2. Founder Baseline Points // Pool Protection (Reference Example)
- When opening a project to external contributors, the founding team's existing core codebase establishes the pool's baseline denominator (e.g., a fixed integer calibrated around `65%–75%` of the projected `v1.0` pool, **such as `10,000 Points`**) and locks it upfront in the `Charter`.
- If an external Co-Developer completes `1,000 Points` of modules, they receive $\frac{1,000}{10,000 + 1,000} = 9.09\%$ of the pool, while `90.91%` stays with the founding team. **No small contribution can ever swallow the entire pool.**

### 3. Co-Developers vs. Debug / QA
| Contribution Tier & Discord Role | Who Qualifies? | Authority & Compensation Model | Scoring Model |
| :--- | :--- | :--- | :---: |
| **`Tier 0` // Community** | All community members and open-source practitioners | Free access to all `AGPLv3` open-source tools, R&D channels, and open education | **Open Access** |
| **`Tier 1` // Tester & Creator** | Field testers, debug/bug reporters, tutorial/video & content creators, minor patch contributors, and active supporters | **Not in equity pool:** **First-50 Roster Direct `Lifetime V1 Access` / Free Pro License** + **One-Off Cash `Bug Bounty`** | **Lifetime V1 Access & Fixed Bounty** |
| **`Tier 2` // Major Developer** | Builders of major features, new functional modules, UI/UX architecture, and DAW/format integrations | **Profit Pool Partner** | **Upfront Declared Task Score (`e.g., Difficulty × Layer × Risk`)** |
| **`Tier 3` // Council & Team Lead** | Senior builders serving as Core Architecture / DSP / AI Major Developers & Team Leads who explicitly accept all Manifesto, Protocol, and Producer Council rules | **Profit Pool Partner + Producer Council Seat + Project `Lead / Council Sponsor` Authority** | **Upfront Declared Task Score (`e.g., Difficulty × Layer × Risk`)** |

---

## 03 // VESTING, HUMANE LEAVE & DECAY (REFERENCE EXAMPLES)

> **Note:** The durations and rates below are **reference examples**. Each project locks its own exact parameters **upfront at project inception in `XULAB_CHARTER.md`**:

| Mechanism | Reference Example Range | Recommended Standard Example | Guild & Labor Protection Logic |
| :--- | :---: | :---: | :--- |
| **1. `Cliff` // Code Maturity Period** | **e.g., `3 – 6 Months`** | **`6 Months` or v1.0 release** | Code remains healthy in `main` for the defined period with basic bug maintenance. Malicious code deletion to burn points is invalid. |
| **2. `Vesting` // Gradual Unlock** | **e.g., `25% – 50%` at Cliff** | **`25%` Month 6 + `25% x 3 Releases`** | The first tranche unlocks at the `Cliff`; the remainder unlocks across subsequent releases with active maintenance. |
| **3. `Freeze` // Humane Leave & Honest Handoff** | **e.g., `30 – 45 Days/Yr` Leave** | **`0% Penalty` on Leave or Honest Handoff** | During film crunch, illness, or leave, point decay pauses. If an author notifies the squad that they are busy and hands off an urgent fix, zero penalty applies—only a small maintenance share (e.g., `15%–20%`) goes to the helper. Unvested point reductions apply only to complete abandonment (`ghosting`). |
| **4. `Roll-off / Decay` // Inactivity** | **e.g., `15% – 35% / Year`** | **`25% Annual Decay`** | Outside active leave, points of contributors who permanently leave the project gradually decay so the pool keeps rewarding active builders. |
| **5. `Payout Cap`** | **e.g., `5x – 10x` Multiplier** | **`5x – 8x` Cash Multiplier** | Points retire once cumulative payouts reach the defined multiple of the task's initial baseline valuation. |
| **6. `Payout Cadence`** | **e.g., `Monthly` or `Quarterly`** | **Every Quarter** | Pool financials are published transparently and distributed on a regular schedule. |

---

## 04 // READY-TO-USE SOFTWARE PROJECT CHARTER // `XULAB_CHARTER.md`

No permission is required to start building a project; however, when requesting **dedicated Discord project channels and collective support** or launching a **`Model B` profit-sharing project**, fill out the template below as `CONTRIBUTING.md` or `XULAB_CHARTER.md` in the repository root and submit it for **Xulab Producer Council** approval:

```markdown
# XULAB SOFTWARE PROJECT CHARTER

- **Project Name:** [e.g., ProjectName]
- **Project Lead // Chair / Lead:** [@username]
- **Council Sponsor // Founding Architect or Governing Council Member:** [@sponsor_username]
- **Project Scope // In-Scope & Out-of-Scope:** [Explicit boundaries of what the project builds and what is out of scope]
- **Project Model:** [ ] Model A // 100% Free AGPLv3  |  [ ] Model B // Incorporated / AGPLv3 Engine + Dual-License
- **Legal Entity // Model B only:** [Company Name & Jurisdiction]
- **Core & Source License:** [ ] Strict AGPLv3 // Model A  |  [ ] Copyfarleft Revenue-Bounded Source-Available + AGPLv3 Deep SDK + Dual-License // Model B
- **Co-Developer Profit Pool Share // Model B:** [15]% of Net Commercial Revenue // Mandatory Floor: 5%–10%
- **Founder Baseline Points:** [10,000 Points]
- **Reward Separation:**
  - Tier 2 & Tier 3 // Major Developers & Council Leads: Slicing Pie Profit Pool Partners
  - Tier 1 // Testers & Creators / Debug / QA / Video: Direct Lifetime V1 Access / Free Pro License & One-Off Bug Bounties
- **Vesting & Point Parameters // Model B:**
  - Cliff Period: [6 Months]
  - Vesting Schedule: [25% at Cliff + 75% across next 3 releases]
  - Annual Inactivity Decay: [25% / year]
  - Payout Cap Multiplier: [6x - 8x]
  - Payout Cadence: [Quarterly]
- **Oversight & Commitment:** This project operates under the Xulab Collective Manifesto and Rulebook. Administrative oversight belongs to the Xulab Producer Council; technical execution belongs to the Project Lead.
```
