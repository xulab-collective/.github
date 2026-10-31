```text
X U L A B   C O L L E C T I V E  //  T H E   R U L E B O O K
[ FOUNDING ARCHITECTS & GOVERNING COUNCIL · WORKING GROUPS · AGPLv3 + DUAL-LICENSE · SLICING PIE POOL ]
```

> **[ [MANIFESTO // MANİFESTO](MANIFESTO.md) ]** · **[ [TR // PROTOKOL VE KURAL KİTABI](#tr--xulab-collective-protokolü-ve-kural-kitabı) ]** · **[ [EN // PROTOCOL & RULEBOOK](#en--xulab-collective-protocol--rulebook) ]** · **[ [TÜZEL POLİTİKALAR // COMMERCIAL POLICY](COMMERCIAL_POLICY.md) ]** · **[ [ROADMAP // YOL HARİTASI](ROADMAP.md) ]**

---

# TR // XULAB COLLECTIVE PROTOKOLÜ VE KURAL KİTABI

> **ÖNCE RAHATLAYIN: BU KURALLAR KİMİN İÇİN?**
> Bu sayfadaki kurallar, meclis yapıları ve lisans maddeleri insanları dışarıda tutmak, hiyerarşi kurmak veya kimseye kapı bekçiliği yapmak için yazılmadı. Sunucuda takılmak, meslektaşlarınla sohbet etmek, hazır araçları indirip kullanmak ya da bir şeyler öğrenmek için buradaki hiçbir kuralı bilmene gerek yok.
>
> Buradaki iç kurallar sadece **ileri aşamada**, yani birden fazla kişinin bir araya gelip ortak bir yazılım ürettiği, şirketleştiği veya gelir paylaşımına girdiği noktada kimsenin emeği sömürülmesin diye devreye girer.
>
> **Kendi Aracını veya Modülünü Üreten Doğrudan Tier 2 Olur:** Daha önce hiç kod yazmamış olman önemli değil. Yapay zeka ajanlarıyla bile olsa sahada çalışan bağımsız bir açık kaynak araç, eklenti veya major modül üretip toplulukla paylaştığın an (`#📩・ticket-submit` veya ilgili `WG` kanalında repo linkini ileterek) Tier 0 veya Tier 1 basamaklarını beklemeden **doğrudan Tier 2 (`Major Developer`)** rolünü alırsın. (`Model B` ticari kâr havuzu puanlarının kesinleşmesi için ise standart `6 ay Cliff` bakım kuralı geçerlidir; ufak betik, yama ve saha testleri `Tier 1` kapsamındadır.)
>
> **Üretime Başlamadan Önce Hatırlatma (`Clean-Room & Güncel Kaynak Taraması`):** Önerilen çözümler ve açık kaynak depolar zamanla eskimiş olabilir. Bir üretime veya çözüm yazılımına başlamadan önce lütfen güncel açık kaynakları tarayınız, `clean-room` yaklaşımı ve AI yardımı ile var olan hangi programların veya kütüphanelerin kullanılabileceğini planlayınız; üretime sonra başlayınız.

Bu doküman, **[Xulab Manifestosu](MANIFESTO.md)**’nun sahadaki operasyonel kural kitabıdır. **Kurucu Mimarlar**ın ve **Üretici Meclisi**’nin yapısını, **Çalışma Grupları** ve **Proje Hücreleri**nin nasıl kurulup denetleneceğini, kurumsal sektöre nasıl `Dual-License` uygulanacağını ve emekçilerin **Katkıcı Kâr Payı Havuzu** ile nasıl ödüllendirileceğini düzenler.

> **SÜRÜM NOTU // `v1.0`:** Bu Protokol ve eki olan **[Tüzel Politikalar](COMMERCIAL_POLICY.md)** ilk sürümdür. Sahadaki pratik ihtiyaçlara, yeni proje deneyimlerine ve ekosistemin büyümesine paralel olarak **Xulab Üretici Meclisi** kararı ile ileride değiştirilmeye ve geliştirilmeye açıktır.

---

## 01 // KOLEKTİF ÇATI, MESLEK LONCASI VE DAYANIŞMA İLKESİ (`CRAFT GUILD & SOLIDARITY ETHOS`)

**Xulab Collective**, yukarıdan aşağıya emir veren merkeziyetçi bir komite veya hantal bir kurumsal yapı değildir; **Meslek Loncası ve Dayanışma İlkesi (`Craft Guild & Solidarity Ethos`)** temelinde — bilginin saklanmadan akran dayanışmasıyla paylaşılması, her üretim ekibinin kendi işinde özerk olması, sömürücü işin reddedilmesi ve ortak AR-GE havuzu — yüksek teknoloji ve açık kaynakla kurulmuş bir üretim kolektifidir. Sistem büyüdükçe, Xulab ilkelerine uyan otonom ekiplerin ve bağımsız stüdyoların ortak GPU ve altyapı maliyetlerini bölüşmek üzere federatif bir ağ kurma yetisi açıktır.

### 1. İki Katmanlı Ekosistem: Ortak Meydan ve Federatif Üretici Meclisi
- **Ortak Meydan // Açık Zanaat ve Dayanışma Alanı:** Herkese açık GitHub repoları, Discord topluluğu, ücretsiz kullanıcılar, lokal AI bağlayan bağımsız üreticiler, hata raporu ve `Pull Request` gönderenlerden oluşur. Maksimum erişilebilirlik ve açık eğitim esastır.
- **Üretici Meclisi // Federatif Koordinasyon ve İlkeler Kurulu:** Ortak Meydan’da somut üretimle (`Proof-of-Work`) rüştünü ispatlayan üreticilerin oluşturduğu yatay koordinasyon meclisidir. Görevi otonom projelerin günlük işine karışmak değil; ortak teknik standartları koordine etmek ve Xulab’ın temel ilkelerini (açık çekirdek, sıfır emek sömürüsü ve temiz-oda güvenliği) korumaktır.

### 2. Üretici Meclisi’nin 4 Bileşeni
Ekosistemdeki tüm üretici güçlerin dengeli temsili için Meclis **4 bileşenden** oluşur:

1. **Kurucu Mimarlar ve Manifesto Koruyucuları (`Anayasal Sigorta`):**
   - Kolektifin kurucu mimarları `@Rhinofug` ve `@Parapazula`, Xulab’ın günlük yöneticileri değil, anayasal koruyucularıdır. Görevleri yalnızca Xulab’ın sermaye tekellerine satılmasını, açık kaynak çekirdeğin kapatılmasını ve emekçi sömürüsü yasağının delinmesini engelleyen **"Anayasal Veto" (`Negatif Yetki`)** sigortasını tutmaktır.
   - Mimarlık makamı dokunulmaz bir taht değildir: Ekosistem büyüdükçe üst düzey mimari katkı sunan kıdemli üreticiler Meclis nitelikli çoğunluğuyla konseye katılabilir; ilkeleri ihlal eden veya sistemi kilitleyen mimarların yetkisi yine Meclis nitelikli çoğunluğuyla kaldırılabilir. Ayrıca tüm çekirdek motorlar `AGPLv3` olduğu için herkesin çatallanma (`Right-to-Fork`) hakkı mutlak güvence altındadır.
2. **Çekirdek Mimari ve Protokol Ekibi:**
   - Xulab’ın ana teknik standartlarını, `AAF/OTIO/MCP` protokollerini ve çekirdek DSP/AI mimarisini koruyan ve denetleyen kıdemli mühendislerdir.
3. **Açık Kaynak Proje Liderleri, Co-Yazılımcılar ve Çalışma Grubu Temsilcileri:**
   - Çatı altında `Model A` tamamen ücretsiz proje yürüten liderler, çalışma grubu yürütücüleri ve en yüksek aktif katkı puanına sahip bağımsız Co-Yazılımcılardır.
4. **Tüzel ve Kâr Paylaşımlı Proje Temsilcileri:**
   - Çatı altında `Model B` çift lisans ile kurumsal sektöre lisans kesip **Katkıcı Kâr Payı Havuzu**’nu ve ortak AR-GE altyapısını besleyen tüzel projelerin temsilcileridir. Mecliste söz hakları vardır ancak `Kurucu Mimarlar` onayını veya `AGPLv3` açık kaynak çekirdeğini asla geçersiz kılamazlar.

---

## 02 // ÇALIŞMA GRUPLARI VE PROJE YÖNETİŞİMİ

> **ALTIN YÖNETİŞİM KURALI:**  
> **Ortak ilkelere ve kurallara uyduğu sürece, Xulab bünyesinde bir projeye veya üretime başlamak için kimseden izin almaya gerek yoktur; herkes dilediği girişimi özgürce başlatabilir ve yürütebilir.**  
> **Meclis Onayı ve Kolektif Destek:** Projenin günlük teknik yürütmesi tamamen proje ekibine aittir. **Üretici Meclisi onayı** ise yalnızca ilgili projeye **özel Discord proje kanallarının açılması, resmi `github.com/xulab-collective` organizasyon çatısına dahil edilmesi ve ortak GPU/sunucu/duyuru gibi kolektif desteklerin tahsis edilmesi** aşamasında devreye girer.  
> **Tekil Xulab Yetkisi:** Xulab yetkisi ile proje katkı yetkileri birbirinden kopuk bürokratik duvarlarla ayrılmaz. Xulab bünyesindeki her geliştirici ve üretici, **istediği her projeye ve çalışma grubuna özgürce katkı sağlayabilir ve katkı verdiği her tüzel projenin havuzundan doğrudan puanını ve payını alır.**

### 1. Otonom Başlangıç ve Kolektif Destek Süreci
Xulab’da ön-izin bürokrasisi yoktur; **aşağıdan yukarıya otonom üretim** esastır:
- **İzinsiz Otonom Başlangıç (`Permissionless Initiative`):** Ortak kurallara (`Manifesto`, `AGPLv3` ve `temiz-oda` güvenliği) uyduğu sürece her üye veya ekip, onay beklemeden çalışma gruplarında veya kendi реposunda istediği aracı geliştirmeye başlayabilir.
- **Kolektif Destek ve Resmi Çatıya Kabul (`Meclis Onayı`):** Bir proje; Xulab sunucusunda **özel proje kanalları** açılmasını, resmi GitHub organizasyonuna (`xulab-collective`) alınmasını, kolektif altyapı/GPU desteğini veya `Model B` kapsamında kurumsal `Dual-License` geliri paylaşmayı talep ettiğinde şu **4 temel alanı** şeffafça tanımlayarak Üretici Meclisi onayına sunar:

| Alan | Tanımı ve Yetki Sınırı |
| :--- | :--- |
| **1. `Project Lead` // Yürütücü Lider** | Projenin günlük teknik yönetiminden, mimari kararlarından ve kod birleştirme süreçlerinden tam özerklikle sorumlu yürütücüdür. |
| **2. `Council Sponsor` // Meclis Köprüsü** | Kolektif destek alan projelerde Üretici Meclisi’nden **1 kişi**, proje ekibi ile Meclis arasında koordinasyon köprüsü olur. Görevi günlük üretime karışmak değil; projenin açık kaynak sınırlarına ve gelir paylaşım şeffaflığına uyumunu gözetmektir. |
| **3. `Charter & Scope` // Başlangıç Beyannamesi** | Projenin `Model A` ücretsiz mi yoksa `Model B` çift lisanslı mı olduğunu, gelir havuzu oranlarını ve hak ediş sürelerini **daha projenin ilk gününden** herkese açıkça ilan eder. Örnek şablon [`COMMERCIAL_POLICY.md`](COMMERCIAL_POLICY.md) içindedir. |
| **4. `Autonomous Squad` // Otonom Proje Ekibi** | Küçük ekiplerde (`Minimum Viable Guild`) komite bürokrasisi işletilmez; `Project Lead` ve aktif geliştiriciler kararları doğrudan ve hızlıca alır. |

### 2. Xulab Çekirdek Çalışma Grupları (`WG-01 .. WG-08`)
Yazılım projelerinin yanı sıra, [`ROADMAP.md`](ROADMAP.md) içindeki sürekli hedeflerimizi ve Discord Ar-Ge kanallarımızı yürüten **8 Çekirdek Çalışma Grubu** şunlardır:

- **`WG-01 // Audio & DAW Working Group`:** Açık kaynak DAW, DSP, miks/mastering, `AAF/OTIO/EDL/MIDI` dönüşüm motorları (`VCut2DAW` dahil) ve stüdyo entegrasyonu (`Audio Team` ile koordineli).
- **`WG-02 // Editing & Color Working Group`:** Kurgu (NLE), asistan kurgu otomasyonu, VFX plan yerleştirme (`shot drop-in`), `ACES/OCIO` renk boru hattı ve timeline araçları.
- **`WG-03 // VFX & 3D Working Group`:** Compositing (`Nuke/Fusion/Natron`), 3D/CG (`Blender/Houdini`), `OpenUSD/OpenEXR` boru hattı ve render doğrulama araçları.
- **`WG-04 // TouchDesigner & Live AV Working Group`:** Gerçek zamanlı görsel-işitsel sistemler, `GLSL`, `OSC/DMX/Art-Net`, sensör/kurulum izleme ve projeksiyon kalibrasyonu (`Studio Node` ile koordineli).
- **`WG-05 // Game Design & Game Audio Working Group`:** Oyun motorları (`Unreal/Godot/Unity`), interaktif ses ara katmanları (`Wwise/FMOD`) ve oyun içi ses/veri senkronizasyon araçları.
- **`WG-06 // Local AI & MCP Working Group`:** Lokal silikon üzerinde çalışan ses/medya AI modelleri (`WhisperX/Demucs/CLAP`), DAW/NLE/DCC `MCP` ajan köprüleri ve kolektif model ağırlıkları.
- **`WG-07 // Field QA & Test Working Group`:** Sahadaki araçların gerçek prodüksiyonlarda test edilmesi, çapraz platform `AAF/XML/OTIO` doğrulaması, teslimat (`QC/LUFS`) kontrolleri ve hata raporlama hattı.
- **`WG-08 // Clean-Room Working Group`:** Kapalı endüstriyel medya protokollerinin ve formatlarının yasal, sıfır telif ihlalli (`clean-room`) birlikte çalışabilirlik spesifikasyonlarının çıkarılması ve açık kaynak motorlara dönüştürülmesi.

*(Açık mesleki eğitimler ve anti-mobbing / görev tanımı standartları tüm çalışma gruplarının ve Ortak Meydan'ın ortak taban görevidir.)*

---

## 03 // XULAB ÇATISI ALTINDAKİ İKİ PROJE MODELİ VE KAPSAM AYRIMI

> **ÖZET: SİSTEMİN TÜM MANTIĞI (`2 MÜLKİYET YAPISI`)**  
> 1. **Açık Kaynak (`Müşterek Mal = AGPLv3`):** Kodları açık tuttuğun sürece kendin geliştir ve kendi işlerinde kullan. Kodu kapatıp ticari bir yazılım ürünü olarak satmadığın sürece her kullanıma açıktır; tek şartı açık kalmak zorunda olmasıdır.  
> 2. **Ticari Proje (`Commercial Project = Açık Çekirdek + Dual-License`):**  
>    - Çekirdeği ve temel kullanımları diğer insanlar geliştirebilsin diye açık olmalıdır (`JUCE` / `Unreal Engine` mantığı).  
>    - Ticari değer getiren kısmını (dolu paket, özel eğitilmiş AI modeli vb.) kendi ticari lisansına göre yapabilirsin. Lisans `Dual-License` olmalıdır:  
>      - **Freelancer (`Individual`):** Bağımsız üreticiler için makul ve erişilebilir düzeyde olmalıdır.  
>      - **Commercial (`B2B / Kurumsal`):** B2B çalışanlara veya şirketlere istediğin ticari bedeli kesebilirsin.  
>    - **Xulab Bir Dağıtımcı Değildir; Ödeme Çatıya Değil Bireye Olur:** Xulab altında geliştirilmemiş veya şartları karşılamayan hiçbir şey Xulab’a ait değildir. Xulab dağıtımcı (publisher) değil, ortak AR-GE ve ürün geliştirme kolektifidir. Ticari projeyi Xulab çatısı altında geliştirdiysen, **kâr üzerinden çatıya değil, doğrudan burada senin yazılımın için çalışan ve `feature` geliştiren insanlara (bireylere)** ödeme yapmak zorundasın (`vesting-cap-decay` gibi puan kuralları ve hangi görevin ne kadar pay alacağı proje başında belirlenir; çatı en fazla `%1–2` sunucu gideri vs. alırsa alır).  
>    - **Tüm Mantığı Bu:** *Buraya gel, buradaki insanlarla bir şeyler üret, istiyorsan ticari sat. Ama bağımsız üreticiye adil ol ve burada emeğini kullandığın yazılımcılara geri ödeme yap.*

> **TEMEL PROTOKOL İLKESİ VE KAPSAM AYRIMI:**  
> 1. **Yazılım, Motor ve AI Geliştirme Projeleri:** Xulab çatısı altındaki **her yazılım projesi tüzel veya tamamen açık kaynak olabilir.** Ancak **sektörel rekabet yaratacak araçların `Dual-License` modeliyle emekçilere doğrudan gelir kazandırması; çekirdek motorun tam açık kaynak `AGPLv3`, kurumsal hizmetin ise `Dual-License` olması şiddetle önerilir.** Tüzel yazılım projeleri daha en baştan buna göre katkı şartlarını kilitleyip Üretici Meclisi’ne sunmak, şeffafça açıklamak ve oluşan gelir havuzunun belirli bir kısmını, minimum `%5–%10` ve tavsiye edilen `%10–%15` oranında, puan sistemiyle projeyi inşa eden **Co-Yazılımcılara** geri ödemek zorundadır. Saha testi, hata ayıklama ve QA katkıları ise kâr havuzunu sulandırmadan Ücretsiz Pro/Lifetime Lisans ve tek seferlik ödüllerle karşılık bulur. **Açık kaynak geliştirme modeli, piyasadaki şirketlerin yaptığı gibi geliştiriciler üzerinden ücretsiz iş gücü sömürüsü yapmak için asla kullanılmayacaktır.**  
> 2. **Piyasa Medya Üretimi ve Post-Prodüksiyon Hizmet Projeleri:** Yukarıdaki `Dual-License` ve puan havuzu sistemi **yalnızca yazılım ve motor geliştirme** içindir. **Piyasada yapılacak medya üretimi ve post-prodüksiyon hizmet etkinliklerinin kazançları bu yazılım havuzundan tamamen bağımsızdır ve yüzde yüz olarak doğrudan işi üstlenen aktif proje ekibine bırakılır.** Bu ekiplerin de Xulab Manifestosu'ndaki taşeron sömürüsü yapmama, mobbing yasağı ve ekip içi adil paylaşım kurallarına uyması zorunludur.

```text
                 [ XULAB COLLECTIVE // KURUCU MİMARLAR & ÜRETİCİ MECLİSİ ]
                                                 │
        ┌────────────────────────────────────────┼────────────────────────────────────────┐
        ▼                                        ▼                                        ▼
[ WORKING GROUPS // WG-01..08 ]  [ MODEL A: %100 FREE PROJELER ]      [ MODEL B: TÜZEL / DUAL-LICENSE PROJELER ]
• Otonom AR-GE & Zanaat Grupları • İzinsiz ve otonom olarak başlar    • Kilitli Charter + Meclis Onayı ile başlar
• Eğitim, Anti-Mobbing, QA, AI   • Meclis onayıyla özel kanal/destek  • Motor tam açık AGPLv3, Hizmet Dual-License
• Ortak AR-GE ve Standartlar     • Saf AGPLv3 ile herkese ücretsiz    • ZORUNLU: Havuzun %5-%15'ini Co-Yazılımcılara
                                                                        puan sistemiyle geri öder!
```

### MODEL A // Tamamen Açık Kaynak ve Ücretsiz Projeler
- **Başlangıç ve Kolektif Destek:** Ortak kurallara ve `AGPLv3` lisansına uyduğu sürece herkes izin almaksızın projeyi başlatabilir ve **Proje Yöneticisi (`Project Lead`)** olarak yürütmeyi üstlenir. Projeye özel Discord kanallarının açılması ve diğer kolektif desteklerin (`github.com/xulab-collective` çatısı, ortak duyuru ve altyapı) sağlanması **Üretici Meclisi** onayıyla gerçekleşir.
- **Lisans ve Fonlama:** Saf **`AGPLv3`** lisansıyla yayınlanır ve tüm meslektaşlara ücretsizdir. Geliştirici ekip, açık kaynak sürdürülebilirliği için araç içinde gönüllü bireysel destek bağlantıları kullanabilir.

### MODEL B // Tüzel Kişilikli, Copyfarleft Korumalı ve Kâr Paylaşımlı Rekabetçi Projeler
- **Başlangıç, Mimari ve Üçlü Lisans Kilidi:** Sektörel rekabet yaratacak büyük çaplı araçlarda büyük stüdyo tekellerinin aracı kendi iç iş akışlarında bedava çalıştırmasını engellemek için **Üçlü Kilit** uygulanır: Çekirdek SDK ve protokol katmanı derin entegrasyonlu `AGPLv3`, açık ve lite uygulama sürümleri **Ciro ve Ölçek Sınırlı `Copyfarleft` Kaynağı Açık Lisans**, ileri teknoloji otomasyon motoru ve özel AI ağırlıkları ise kurumsal **`Dual-License`** altındadır. Böylece bağımsız emekçiler ve küçük ekipler kodu ücretsiz kullanırken, ciro sınırını aşan kurumsal stüdyolar iç prodüksiyon kullanımları için dahi ticari lisans almak zorundadır.
- **Baştan Kilitlenen Katkı Şartları ve Zorunlu Geri Ödeme Kuralı:** Xulab çatısı altında yer alan her tüzel proje, **daha projenin ilk gününden `CONTRIBUTING.md` ve `CLA` ile katkı ve gelir paylaşım şartlarını açıkça ilan etmek** ve kurumsal sermaye stüdyolarına kestiği `Dual-License` gelir havuzunun **belirli bir yüzdesini puan sistemiyle projeye emek veren Co-Yazılımcılara geri ödemek zorundadır.**

---

## 04 // LİSANSLAMA VE EKOSİSTEM KİLİDİ

Xulab’da üretilen bilgi müşterektir; ancak kurumsal stüdyo tekellerinin bu müşterek emeği bedava sömürmesine izin verilmez:

1. **Taban Araçlarda Saf `AGPLv3`, Rekabetçi Motorlarda `Copyfarleft` Ciro Sınırlı Açık Lisans ve Derin SDK Kilidi:**
   - Taban topluluk araçlarında (`Model A`) herkes kendi telifini korur ve bulut/SaaS kaçaklarını önlemek için **Saf `AGPLv3`** kullanılır.
   - Sektörel rekabet yaratan ileri teknoloji araçlarda (`Model B`) ise büyük stüdyoların iç iş akışı sömürüsünü kesmek için **Ciro Sınırlı Kaynağı Açık `Copyfarleft` Lisanslama** ve **Derin SDK Mimari Kilidi** uygulanır: Bağımsız emekçiler ve küçük ekipler kodu ücretsiz kullanırken, ciro sınırını aşan kurumsal şirketler ticari lisans almak zorundadır.
2. **Sıfır İstisna ve Rekabet Duvarı:**
   - İnşa ettiğimiz DAW, NLE ve MCP ekosistemine entegre olacak her 3. parti eklenti, MCP aracı veya AI modeli ya kodunu tamamen açık kaynak **`AGPLv3`** yaparak ortak havuzu büyütür ya da kapalı kalmak istiyorsa ilgili proje ekibinden **ücretli ticari lisans** satın alır.
3. **Kademeli Fiyatlandırma Matrisi:**
   - **Açık Kaynak ve Lokal Bağımsız Üretici:** **ÜCRETSİZ**, `AGPLv3` Açık Kaynak Motor ve lokal donanımda açık AI modelleri.
   - **Bağımsız Freelancer ve Indie:** Erişilebilir bireysel lisans.
   - **Kurumsal Sermaye Stüdyosu:** Koltuk başı ve ağ depolama (`SAN/NEXIS`) kapsamlı kurumsal lisans.
   - **3. Parti Kapalı Şirketler:** Ekosistemde kapalı ürün satmak isteyen şirketlerden ticari lisans bedeli ve ciro payı.

---

## 05 // KATKICI KÂR PAYI HAVUZU VE PROJE BAŞI ŞEFFAFLIK İLKESİ

`Model B` projelerde açık kaynak geliştiricileri üzerinden asla ücretsiz iş gücü sömürüsü yapılmaması için **Proje Başı Şeffaflık (`Ex-Ante Charter`)** ve **Karşılıklı Katkı Sözleşmesi** uygulanır:

- **Karşılıklı Katkı Sözleşmesi (`Two-Way CLA`):** Proje tüzel kişiliğinin kurumsal stüdyolara `Dual-License` faturası kesebilmesi için katkıcı ticari lisanslama yetkisi verir; tüzel kişilik ise net ticari gelirinin sabit **`%X`** oranını şeffaf biçimde **Katkıcı Kâr Payı Havuzu**’na dağıtmayı en baştan sözleşmeyle taahhüt eder.
- **Kurucu Çekirdek Baz Puanı ve Görev Puanlaması:** Proje başlarken mevcut çekirdek kodun baz puanı ve açılacak görevlerin nasıl puanlanacağı (örneğin zorluk, mimari katman ve risk çarpanı) **proje başında (`Charter` içinde)** açıkça ilan edilir:
  $$\text{Co-Yazılımcının Payı} = \frac{\text{Aktif Katkıcı Puanı}}{\text{Kurucu Baz Puanı} + \text{Toplam Katkıcı Puanı}}$$
- **Proje Başında Belirlenen Denge ve İnsani Koruma Kuralları:**
  Her otonom proje ekibi; kodun ana dalda kalma süresini (`Cliff`, örn. `3–6 ay`), kademeli hak edişi (`Vesting`), tamamen pasifleşen puanların erimesini (`Decay`), tavan ödemeyi (`Cap`) ve yoğun iş/hastalık dönemlerindeki **koşulsuz mola ve cezasız görev devri (`Freeze / Humane Handoff`)** sürelerini **daha projenin ilk gününden `XULAB_CHARTER.md` içinde netleştirir.**

### Minimum Havuz Payları, Kurucu Baz Puanı ve Hazır Proje Başlangıç Belgesi
Xulab altında yeni bir yazılım projesi açacak geliştirici veya tüzel kişiliklerin doğrudan kullanacağı **Minimum Zorunlu Havuz Taban Oranları**, **Kurucu Çekirdek Baz Puanı**, **Co-Yazılımcı ile Debug/QA Ayrımı** ve kopyalanıp doldurulmaya hazır **Proje Başlangıç Beyannamesi Şablonu** için **[`COMMERCIAL_POLICY.md`](COMMERCIAL_POLICY.md)** belgesine bakınız.

---

# EN // XULAB COLLECTIVE PROTOCOL & RULEBOOK

> **READ THIS FIRST: WHO ARE THESE RULES FOR?**
> The rules, council structures, and licensing terms in this document were not written to gatekeep, rank people, or keep anyone out. If you are here to talk shop with fellow practitioners, use open-source tools, or learn how to build your own utilities, you can ignore this entire rulebook.
>
> These internal rules only kick in at the **advanced stage**, when multiple people team up to ship shared software, form a project squad, or split commercial revenue, so that nobody's work gets exploited.
>
> **Build a Tool or Major Module, Go Straight to Tier 2:** Your coding background does not matter. The moment you ship and share a working standalone open-source tool, plugin, or major feature module—even by directing an AI Agent from scratch (submit your repo link in `#📩・ticket-submit` or your `WG` channel)—you skip Tier 0 and Tier 1 and go **straight to Tier 2 (`Major Developer`)**. (For `Model B` commercial profit-pool equity points, the standard `6-month Cliff` maintenance rule still applies; smaller scripts, minor patches, and field QA start at `Tier 1`.)
>
> **Pre-Production Reminder (`Clean-Room & Current Open-Source Scan`):** Proposed solutions and open-source repositories may become outdated over time. Before starting any production or software solution, please scan current open-source repositories and use AI with a `clean-room` approach to plan which existing programs or libraries can be used; start building only after that planning pass.

This document is the operational rulebook of the **[Xulab Manifesto](MANIFESTO.md)**. It defines the role of the **Founding Architects** and the **Governing Council**, how **Working Groups** and **Project Cells** are chartered and overseen, how `AGPLv3 + Dual-Licensing` is enforced against corporate monopolies, and how contributors are rewarded through the **Slicing Pie Point System**.

> **VERSION NOTE // `v1.0`:** This Protocol and the accompanying **[Commercial Policies](COMMERCIAL_POLICY.md)** are in their initial release and remain open to future revision, adaptation, and evolution by decision of the **Xulab Governing Council** as real-world practice requires.

---

## 01 // COLLECTIVE UMBRELLA, CRAFT GUILD & SOLIDARITY ETHOS, AND PRODUCER COUNCIL

**Xulab Collective** is not a top-down central committee or a bureaucratic corporation; it is built on a modern **Craft Guild & Solidarity Ethos** equipped with open source and AI—grounded in open peer-to-peer knowledge sharing, autonomous project workshops, ethical craft standards, zero labor exploitation, and a shared R&D commonwealth. As the ecosystem grows, autonomous squads and independent studios can federate to share GPU and infrastructure costs.

### 1. Two-Layer Ecosystem: Open Commons & Federative Producer Council
- **Open Commons // Open Craft & Solidarity Ground:** Public GitHub repositories, Discord community, free users, local-AI practitioners, QA testers, and contributors. Built for maximum accessibility and open vocational education.
- **Producer Council // Federative Coordination Table:** The horizontal coordination council of builders proven through concrete `Proof-of-Work`. Its role is never to micromanage autonomous project squads, but to coordinate shared technical standards and safeguard Xulab's core principles (open core, zero labor exploitation, and clean-room integrity).

### 2. The 4 Pillars of the Producer Council
To ensure balanced representation across the guild, the Council comprises **4 pillars**:

1. **Founding Architects & Constitutional Stewards (`Circuit-Breaker`):**
   - The founding architects `@Rhinofug` and `@Parapazula` serve as constitutional stewards, not day-to-day bosses. Their sole mandate is holding the **"Constitutional Veto" (`Negative Authority`)** safeguard to ensure Xulab is never sold out to capital monopolies, the open-source core is never enclosed, and anti-exploitation rules remain intact.
   - The Architect role is not an untouchable throne: senior builders with sustained architectural `Proof-of-Work` may join the stewards by Council supermajority, and any steward violating the Manifesto or deadlocking the collective may be restricted by Council supermajority. Because all core engines are `AGPLv3`, the `Right-to-Fork` remains permanently guaranteed.
2. **Spec & Core Architecture Team:**
   - Senior engineers safeguarding Xulab's core technical standards across `AAF/OTIO/MCP` protocols and core DSP/AI architecture.
3. **Commons & Working Group Delegates:**
   - Leads of `Model A` 100% Free projects, `Working Group` Chairs/Leads, and top point-earning independent Co-Developers.
4. **Dual-License Entity Delegates:**
   - Representatives of `Model B` Dual-License incorporated projects that bill enterprise studios and fund the **Contributor Profit Pool** and shared R&D infrastructure. They hold representation seats but can never override the `Founding Architects` or enclose the `AGPLv3` open-source core.

---

## 02 // WORKING GROUPS & PROJECT GOVERNANCE

> **GOLDEN GOVERNANCE RULE:**  
> **As long as an initiative abides by our shared principles and rules, no permission is required to start building; anyone in Xulab is free to initiate and run any project.**  
> **Council Endorsement & Collective Support:** Day-to-day technical execution belongs entirely to the project squad. **Producer Council approval** is required only when a project seeks **dedicated Discord project channels, adoption under the official `github.com/xulab-collective` organization, or access to shared collective support and infrastructure (GPU, servers, official announcements).**  
> **Unified Xulab Standing:** Xulab permissions and project contribution rights are never split into bureaucratic silos. Every developer and practitioner in Xulab **is free to contribute to any project or working group and earn points and profit shares directly from each commercial project they help build.**

### 1. Autonomous Initiation & Collective Support Process
Xulab operates on **bottom-up workshop autonomy**, not prior-restraint bureaucracy:
- **Permissionless Initiation:** As long as shared rules (`Manifesto`, `AGPLv3`, and `clean-room` integrity) are respected, any member or squad may start building tools, scripts, or libraries in working groups or their own repositories without waiting for approval.
- **Collective Support & Official Umbrella Adoption (`Council Approval`):** When a project requests **dedicated Discord project channels**, adoption into the official `github.com/xulab-collective` organization, shared collective infrastructure/GPU support, or `Model B` commercial `Dual-License` revenue sharing, it declares **4 fields** transparently upfront for Producer Council approval:

| Field | Definition & Authority Boundary |
| :--- | :--- |
| **1. `Project Lead`** | Holds full autonomous execution authority over day-to-day technical architecture, task routing, and PR merges. |
| **2. `Council Sponsor`** | For collectively supported projects, **1 member** of the Producer Council serves as a peer liaison who ensures alignment with open-source boundaries and revenue-sharing transparency without micromanaging execution. |
| **3. `Charter & Scope`** | Declares upfront from day one whether the project is `Model A` (100% Free) or `Model B` (Dual-License), along with its profit-pool rates and vesting timelines. Reference template in [`COMMERCIAL_POLICY.md`](COMMERCIAL_POLICY.md). |
| **4. `Autonomous Squad`** | Small bootstrap squads (`Minimum Viable Guild`) operate with zero committee overhead; the `Project Lead` and active builders make decisions directly. |

### 2. Core Xulab Working Groups (`WG-01 .. WG-08`)
Alongside dedicated software repositories, **8 Core Working Groups** drive our continuous R&D tracks in [`ROADMAP.md`](ROADMAP.md) and on Discord:

- **`WG-01 // Audio & DAW Working Group`:** Open-source DAW, DSP, mixing/mastering, `AAF/OTIO/EDL/MIDI` engines (including `VCut2DAW`), and studio integration (in coordination with `Audio Team`).
- **`WG-02 // Editing & Color Working Group`:** Picture editing (NLE), assistant editing automation, VFX turnover/shot drop-in, `ACES/OCIO` color pipelines, and timeline utilities.
- **`WG-03 // VFX & 3D Working Group`:** Compositing (`Nuke/Fusion/Natron`), 3D/CG (`Blender/Houdini`), `OpenUSD/OpenEXR` pipelines, and render verification tools.
- **`WG-04 // TouchDesigner & Live AV Working Group`:** Real-time audiovisual systems, `GLSL`, `OSC/DMX/Art-Net`, sensor/installation watchdogs, and projection calibration (in coordination with `Studio Node`).
- **`WG-05 // Game Design & Game Audio Working Group`:** Game engines (`Unreal/Godot/Unity`), interactive audio middleware (`Wwise/FMOD`), and game data/audio sync utilities.
- **`WG-06 // Local AI & MCP Working Group`:** Local-silicon audio/media AI models (`WhisperX/Demucs/CLAP`), DAW/NLE/DCC `MCP` agent bridges, and collective model weights.
- **`WG-07 // Field QA & Test Working Group`:** Production field testing, cross-platform `AAF/XML/OTIO` conform verification, delivery QC (`LUFS/True Peak`), and bug triage.
- **`WG-08 // Clean-Room Working Group`:** Zero-contamination clean-room interoperability specifications for closed industrial formats and protocols, paired with open-source engine implementation.

*(Open vocational education and anti-mobbing / professional scope standards run across all Working Groups and the Open Commons.)*

---

## 03 // TWO PROJECT MODELS UNDER XULAB & SCOPE SEPARATION

> **SUMMARY: THE ENTIRE LOGIC OF THE SYSTEM (`2 OWNERSHIP TIERS`)**  
> 1. **Open Source (`Shared Commons = AGPLv3`):** As long as you keep the code open, develop it and use it in your own work for `$0`. It is open to everything except enclosing and selling the code itself as a closed commercial software product; it must remain open commons.  
> 2. **Commercial Project (`Open Core + Dual-License`):**  
>    - Its core and foundational functionality must remain open so others can build on it (`JUCE` / `Unreal Engine` logic).  
>    - You license the commercial value-add part (turnkey package, custom-trained AI weights, service) under your own commercial `Dual-License`:  
>      - **Freelancer (`Individual`):** Must remain fair and accessible for independent practitioners.  
>      - **Commercial (`B2B / Enterprise`):** You can charge corporate studios and B2B clients whatever commercial rate you set.  
>    - **Xulab Is Not a Publisher; Payouts Go to Individual Builders, Not the Umbrella:** Nothing built outside Xulab or outside these terms belongs to Xulab. Xulab is a shared R&D and product development collective, not a publisher. If you develop a commercial project under Xulab, **you must pay a profit share not to the umbrella, but directly to the individual developers who built features for your software** (`vesting-cap-decay` point rules and task weights are set at project start; the umbrella takes at most `1%–2%` only if shared server costs apply).  
>    - **The Entire Logic:** *Come here, build things with the people here, and sell commercially if you want. Just be fair to independent workers and pay back the developers whose labor you used here.*

> **CORE PROTOCOL MANDATE & SCOPE SEPARATION:**  
> 1. **Software, Engine & AI Development Projects:** **Every software project under Xulab may be either incorporated or 100% open-source.** However, **for tools built to create real industry competition, we strongly recommend the `Dual-License` model so that the tool directly generates income for workers, keeping the core engine 100% open-source under `AGPLv3` while licensing the commercial service layer via `Dual-License`.** Incorporated software projects must lock and submit their contributing terms to the Governing Council from day one, publish them transparently, and pay back a defined percentage of their net revenue pool to **Co-Developers** via a point system anchored by **Founder Baseline Points**, while rewarding **Field QA / Debug** with Free Pro/Lifetime Licenses and one-off Bug Bounties. **Open-source development under Xulab will never be used, as it is in the corporate market, to exploit unpaid developer labor.**  
> 2. **Market Media Production & Post-Production Services:** The `Dual-License` and point-pool system above applies **strictly to software and engine development**. **Revenues from market media production and post-production service engagements are completely independent of this software pool and belong 100% to the active squad executing the work**, provided they strictly abide by the Xulab Manifesto: zero subcontractor exploitation, zero mobbing, and fair distribution among the active production team.

### MODEL A // 100% Free & Open-Source Projects
- **Initiation & Collective Support:** Anyone may initiate a `Model A` project without prior permission and lead day-to-day execution autonomously as **Project Lead**, provided shared rules and `AGPLv3` terms are respected. **Producer Council** approval unlocks dedicated Discord project channels, adoption into `github.com/xulab-collective`, and shared collective support.
- **Licensing & Funding:** Released under **Strict `AGPLv3`**, 100% free for all practitioners. May include voluntary peer support links.

### MODEL B // Incorporated, Copyfarleft-Protected & Profit-Sharing Competitive Projects
- **Initiation, Architecture & Triple Licensing Lock:** For high-impact competitive tools, we enforce a **Triple Lock** so studio monopolies cannot run our engines for free inside their internal pipelines: deep-linked SDK libraries under `AGPLv3`, open and lite application builds under **Revenue-Bounded `Copyfarleft` Source-Available Licenses**, and advanced automation engines plus trained AI weights under commercial **`Dual-Licensing`**. Independent workers and small peer teams run the code for free, while corporate studios exceeding the revenue threshold must purchase a commercial license even for internal production use.
- **Upfront Contributing Terms & Mandatory Payout Rule:** Every incorporated project under Xulab **must publish its contributing and profit-sharing terms upfront from day one** and **must return a fixed percentage of its commercial revenue pool to Co-Developers via the `Slicing Pie` point system.**

---

## 04 // LICENSING & ECOSYSTEM LOCK

1. **Strict `AGPLv3` for Foundational Tools + `Copyfarleft` Revenue-Bounded Source-Available & Deep SDK Lock for Competitive Engines:**
   - Foundational community tools under `Model A` use **Strict `AGPLv3`** to close cloud and SaaS loopholes.
   - Competitive industrial engines and their open or lite editions under `Model B` combine **Revenue-Bounded `Copyfarleft` Source-Available Licensing** with **in-process Deep SDK locks** so large corporations cannot bypass licensing through internal pipeline use or microservice wrappers.
2. **Zero Linking Exception:** Every plugin, MCP tool, or AI model integrating into the Xulab DAW/MCP stack must either be **100% open-source under `AGPLv3`** or purchase a **Commercial `Dual-License`**.
3. **4-Tier Pricing Matrix:**
   - **Open-Source / Local Independent Practitioner:** **FREE**, `AGPLv3` Engine + Local open AI models.
   - **Freelancer / Indie:** Affordable indie license & API key.
   - **Corporate Studio:** High-ticket per-seat commercial license & cloud speed.
   - **3rd-Party Closed Vendors:** Commercial license fee + revenue share.

---

## 05 // CONTRIBUTOR PROFIT POOL & UPFRONT CHARTER PRINCIPLE

- **Two-Way Contributing Agreement (`CLA`):** Solely so a `Model B` project entity can issue commercial `Dual-Licenses` to corporate studios (`>$50k`), contributors grant commercial licensing authority in exchange for a contractually locked **`%X` net revenue share** flowing back into the **Contributor Profit Pool**. (In `Model A` 100% Free projects, no CLA is used and every builder retains individual copyright).
- **Founder Baseline & Transparent Task Scoring:** At project inception, the baseline points of the initial core codebase and the task scoring method (e.g., difficulty, architectural layer, and risk multipliers) are declared transparently upfront in the project's `Charter`:
  $$\text{Co-Developer Share} = \frac{\text{Active Contributor Points}}{\text{Founder Baseline Points} + \text{Total Contributor Points}}$$
- **Upfront Vesting & Humane Leave Terms (`Ex-Ante Transparency`):**
  Every autonomous `Model B` squad defines its exact maintenance period (`Cliff`, e.g., `3–6 months`), `Vesting` schedule, inactivity `Decay`, `Payout Cap`, and unconditional burnout/production leave (`Freeze / Humane Handoff`) durations **upfront from day one in `XULAB_CHARTER.md`**. See **[`COMMERCIAL_POLICY.md`](COMMERCIAL_POLICY.md)** for recommended reference examples and the ready-to-use template.
- **Minimum Pool Floors, Founder Baseline & Ready-to-Use Project Charter:**
  See **[`COMMERCIAL_POLICY.md`](COMMERCIAL_POLICY.md)** for the mandatory minimum profit-pool percentages, **Founder Baseline Points**, **Co-Developer vs. Debug/QA separation**, and the copy-pasteable **Software Project Charter Template**.

```text
------------------------------------------------------------------------
MANIFESTO          See MANIFESTO.md
COMMERCIAL POLICY  See COMMERCIAL_POLICY.md
ROADMAP            See ROADMAP.md
COLLECTIVE         https://github.com/xulab-collective
ARCHITECTS         Furkan Utku Gerçik // @Rhinofug // Founding Architect
                   Muhammed Kol // @Parapazula // Co-Architect
LICENSE            GNU Affero General Public License v3.0 // AGPLv3 // Dual-License
------------------------------------------------------------------------
```
