# XULAB // #1 PRIORITY: SOLVE YOUR OWN PROBLEMS, AUTOMATE YOUR WORKFLOW | NO IDEAS? HERE ARE SOME (`2026-10-30`)
# XULAB // #1 ÖNCELİK: KENDİ SORUNUNU ÇÖZ, İŞ AKIŞINI OTOMATİKLEŞTİR | FİKRİN YOKSA SAHADAN ÖNERİLER (`2026-10-30`)

> **#1 Priority / #1 Öncelik:** Solve your own problems and automate your own daily workflow first (`-> Direct Tier 2`). If you don't have an idea yet, pick any of the researched studio bottlenecks below.
> **Üretime Başlamadan Önce Hatırlatma (`Clean-Room & Güncel Kaynak Taraması`):** Buradaki çözümler ve açık kaynak depo önerileri zamanla eskimiş olabilir. Lütfen bir üretime veya çözüm yazılımına başlamadan önce güncel açık kaynakları tarayınız, `clean-room` yaklaşımı ve AI yardımı ile var olan hangi programların kullanılabileceğini planlayınız; üretime sonra başlayınız.
> **Pre-Production Reminder (`Clean-Room & Current Open-Source Scan`):** Proposed solutions and repository recommendations may become outdated over time. Before starting any production or software solution, scan current open-source repositories and use AI with a `clean-room` approach to plan which existing tools can be used; start building only after that planning pass.
> **Tarih / Date:** `2026-10-30`
> **Konum / Location:** `D:\Xulab\RESEARCH_BOTTLENECKS_2026-10-30.md` (`D:\Xulab\PROTOCOL.md` yanında / alongside `PROTOCOL.md`)

---

## BÖLÜM A // ÇALIŞMA GRUPLARI ÖZETLERİ VE 1 CÜMLELİK ÇÖZÜM ÖNERİLERİ (`WG-01` .. `WG-07`)

# WG-01 // AUDIO, DAW & DSP (`#wg01-audio-daw-and-dsp`)

## TR // #1 Kendi Sorununu Çöz & Otomatikleştir | Fikir Yoksa Öneriler (`2026-10-30`)

1. **Premiere/Resolve -> Pro Tools AAF `PolyWAV` Kopması & Türkçe Karakter (`ğ, ü, ş, ı, ö, ç`) Çökmesi**
- **Sorun:** Premiere `Merged Clips` veya Türkçe karakterli dosya/iXML adları yüzünden Pro Tools AAF'i açamaz ya da çok kanallı set seslerini (`Boom / Lav`) bağsız mono parçalara böler.
- **Çözüm:** AAF/XML içindeki ASCII dışı karakterleri temizleyip kesmeleri ham `PolyWAV` klasörüyle timecode ve dalga formu üzerinden bağlayan bir `pyaaf2` aracı yazılabilir.

2. **Uluslararası Teslimatta `Fully Filled M&E` Stem QC, Unutulan `PFX` Delikleri & Faz Hatası**
- **Sorun:** Mikserler 120dk filmi 1x hızda dinleyerek diyalog kanalında olup `M&E` içinde unutulan fiziksel sesleri (`PFX` deliklerini), diyalog sızıntılarını ve `DX+MX+FX != Printmaster` faz hatalarını arar.
- **Çözüm:** `Printmaster`, `DX` ve `M&E` dosyalarını 100x hızda tarayıp konuşma dışı `DX` darbe enerjisini `M&E` ile kıyaslayarak eksik PFX deliklerini ve sızıntıları raporlayan QC aracı yazılabilir.

3. **Diyalog Kurgusunda `PFX` Ayıklama Sonrası Gerçek Set `Room Tone` Hasadı**
- **Sorun:** *RX Ambience Match* yapay gürültü ürettiği için kurgucular ham `PolyWAV` dosyalarının handle boşluklarından gerçek oda tonunu elle kesip yüzlerce boşluğa döşer.
- **Çözüm:** Ham `PolyWAV` dosyalarının handle bölgelerini tarayıp her sahneye gerçek oda tonu bankası çıkaran ve diyalog kesiklerini otomatik dolduran bir araç yapılabilir.

4. **DAW Ses Otomasyonunu Okuyan Müzik `Cue Sheet` (`RapidCue / ASCAP`) Üreticisi**
- **Sorun:** Basit EDL betikleri mikserin ses otomasyonuyla erken kıstığı müzikleri veya klip sonundaki sessizliği anlamadığı için telif sürelerini yanlış çıkarır.
- **Çözüm:** Klip sınırlarını DAW ses otomasyon eğrileri ve `-60 dBFS` sessizlik eşiğiyle birleştirip müziğin gerçek duyulma süresini Excel telif tablosuna döken araç yazılabilir.

## EN // #1 Solve Your Own Problems, Automate Workflow | No Ideas? Here Are Some (`2026-10-30`)

1. **Premiere/Resolve -> Pro Tools AAF `PolyWAV` Loss & Non-ASCII (`UTF-8`) Relink Failure**
- **Problem:** Premiere *Merged Clips* strip `iXML/BWF` tags and AAF parsers choke on non-ASCII/Turkish chars (`ğ, ü, ş, ı, ö, ç`) or `NFD/NFC` Unicode, unlinking field recorder iso tracks.
- **Solution:** Build `pyaaf2`/XML sanitizer that normalizes non-ASCII strings and relinks timeline edits back to raw `PolyWAV` tracks via timecode and acoustic cross-correlation.

2. **"Fully Filled" `M&E` Stem QC, Missing `PFX` Holes & Sum-to-Master Null Verification**
- **Problem:** Mixers listen to 120-min features at 1x speed to catch missing production effects (`PFX` holes muted with dialogue), vocal bleed in `M&E`, and `DX+MX+FX != Printmaster` null errors.
- **Solution:** Build 100x offline analyzer that compares non-speech transient energy between `DX` and `M&E` stems for `PFX` holes, runs VAD on `M&E` for bleed, and checks phase-inverted stem nulling.

3. **Real Production Room-Tone Harvesting from `PolyWAV` Handles for Dialogue Gaps**
- **Problem:** Synthetic room tone (*RX Ambience Match*) sounds frozen on gaps over 1.5s, forcing editors to manually harvest real room tone from raw `PolyWAV` pre/post-roll handles.
- **Solution:** Scan raw production `PolyWAV` handles per Scene/Take to extract clean 3-to-10s real room-tone windows and auto-fill dialogue cut gaps with equal-power crossfades.

4. **Automation-Aware Music Cue Sheet Generator (`RapidCue / ASCAP / BMI`)**
- **Problem:** Basic EDL scripts only read clip container boundaries, logging wrong durations when a mixer fades a cue early via volume automation or leaves silent tail in a stem.
- **Solution:** Combine clip boundaries with DAW volume/mute automation curves and a `-60 dBFS` RMS threshold to export frame-accurate audible In/Out Excel cue sheets.

---

# WG-02 // EDITING, COLOR & CAMERA (`#wg02-editing-color-and-camera`)

## TR // #1 Kendi Sorununu Çöz & Otomatikleştir | Fikir Yoksa Öneriler (`2026-10-30`)

1. **VFX Planlarının (`v001 -> v003`) Sekansa Elle Dizilmesi, `Frame 1000` Slate ve Handle Matematiği**
- **Sorun:** Gelen VFX planlarında `Frame 1000` slate, `+8/+12f` handle payı ve `00:00:00:00` timecode yüzünden yerleşik *Replace / Reconform* çöker; asistan yüzlerce planı elle kırpıp üst kanala (`V2->V4`) dizer.
- **Çözüm:** Dosya adından plan/versiyon kodunu okuyan, `Frame 1000` slate ve handle paylarını kırpıp `v003` klibini üst kanala oturtan ve eskiyi kapatan araç yazılabilir.

2. **Değişken Hız Eğrilerinin (`Bezier Speed Ramp`) Premiere, Resolve ve Nuke Arasında Bozulması**
- **Sorun:** Kurgudaki eğrisel hız değişimleri XML/AAF ile Resolve veya VFX'e giderken sabit hıza döner veya onlarca kare kayar; VFX için hangi ham kamera karelerinin çekileceği elle hesaplanır.
- **Çözüm:** Premiere/Avid hız eğrilerini entegre edip ham kare aralığını ve Nuke `TimeWarp` / Resolve kare eşleme tablosunu üreten araç yazılabilir.

3. **Premiere -> Resolve XML Aktarımında `Nested Sequence` ve Karışık Çözünürlük Kadraj Kayması**
- **Sorun:** Premiere `Nested Sequence` yapıları ve 4K/6K/8K kliplerdeki `Set to Frame Size` / `Scale to Frame Size` farkları Resolve'a geçerken tüm kadrajları kaydırır.
- **Çözüm:** XML'i Resolve'a almadan önce iç içe sekansları düzleştiren ve Premiere piksel koordinatlarını Resolve `Zoom / Pan / Tilt` değerlerine normalize eden araç yazılabilir.

4. **`.drx` Düğüm Okuyucu (`CDL + Look` Ayırıcı) & Gelen VFX Planlarında Donmuş Handle / Renk QC**
- **Sorun:** Resolve API'si düğüm içini okuyamadığı için VFX'e `Primary CDL` ile `Look LUT` ayırmak ve dönen VFX planlarında donmuş handle karelerini veya `Rec.709` kaymalarını yakalamak elle yapılır.
- **Çözüm:** `.drx` XML dosyalarını dışarıdan ayrıştırıp teknik dengeyi `.cdl` olarak ayıran ve dönen VFX planlarını orijinal plakayla `OpenCV` ile kıyaslayıp donmuş kareleri bulan araç yazılabilir.

## EN // #1 Solve Your Own Problems, Automate Workflow | No Ideas? Here Are Some (`2026-10-30`)

1. **Manual VFX Shot Drop-In (`v001 -> v003`), `Frame 1000` Slate Stripping, Handle Math & Track Stacking**
- **Problem:** Native NLE *Replace Clip* and Resolve *Reconform* fail when VFX renders include a `Frame 1000` slate, `+8/+12f` handles, or `00:00:00:00` timecode, forcing manual trim and stacking (`V2->V4`).
- **Solution:** Build drop-in tool that matches shot IDs via regex/markers, strips Frame 1000 slate, computes `(N_returned - N_slate - N_cut) / 2` handle trims, stacks `v003` on top, and disables `v002`.

2. **Bezier Variable Speed Ramps Breaking Across Premiere, Resolve & Nuke Turnovers**
- **Problem:** FCP7 XML and AAF strip or misalign non-linear bezier speed ramps, forcing manual frame-by-frame `Difference` matching and manual calculation of raw camera frame extents for VFX pulls.
- **Solution:** Parse Premiere/Avid velocity curves to compute exact raw camera frame extents and export an exact per-frame retime curve for Nuke `TimeWarp` and Resolve.

3. **Premiere -> Resolve XML Un-Nesting & Mixed-Resolution Sizing Math Normalization**
- **Problem:** Colorists spend hours flattening Premiere *Nested Sequences* and fixing broken reframing caused by mixing *Set to Frame Size* and *Scale to Frame Size* across 4K/6K/8K clips.
- **Solution:** Build XML/OTIO pre-processor that unrolls nested sequences and converts Premiere transforms into Resolve Edit Sizing (`Zoom/Pan/Tilt`).

4. **External `.drx` XML Node Parser (`CDL + Look` Splitter) & Inbound VFX Freeze-Handle QC**
- **Problem:** Resolve's API is blind to internal node/DCTL parameters during VFX turnovers, and AEs manually scrub returned VFX shots in `Difference` mode to catch frozen handle frames or `Rec.709` clamping.
- **Solution:** Parse `.drx` XML sidecars externally to split `ASC CDL` nodes from look nodes, and scan returned plates in `OpenCV` to flag frozen handles and color shifts.

---

# WG-03 // VFX & 3D PIPELINE (`#wg03-vfx-and-3d-pipeline`)

## TR // #1 Kendi Sorununu Çöz & Otomatikleştir | Fikir Yoksa Öneriler (`2026-10-30`)

1. **Lens Bozulması (`STMap`) Overscan Hesabı ve Kamera Optik Metadata Kaybı (`Nuke <-> Blender/Houdini/Unreal`)**
- **Sorun:** Kamera takibi sonrası CG kenarları `STMap` bükülmesinde kesilmesin diye gereken `overscan` ve sensör çarpanı her yazılımda farklı hesaplandığından sanatçılar elle tablo hesabı yapar.
- **Çözüm:** Bir `STMap` EXR sınır kutusunu (`BBox`) okuyup Nuke, Blender, Houdini ve Unreal kameraları için çözünürlük ve overscan çarpanını üreten araç yazılabilir.

2. **Blender <-> Houdini Solaris <-> Unreal Engine 5 Arasında `OpenUSD` ve `MaterialX` Çökmesi**
- **Sorun:** Yazılımlar arası eksen/birim farkları (`Z-up/m`, `Y-up/m`, `Z-up/cm`) yüzünden USD sahneleri 100 kat büyür; Houdini paketli objeleri boş gelir ve mutlak yollar yüzünden `UDIM / MaterialX` kopar.
- **Çözüm:** USD dosyasını hedef programa almadan önce `metersPerUnit` ve `upAxis` değerlerini normalize eden, paketli geometrileri açan ve UDIM yollarını göreli (`relative`) yapan araç yazılabilir.

3. **Gece Renderlarında Bozuk `OpenEXR` Kareleri, Silinen `Cryptomatte` Başlıkları ve `v01 -> v02` AOV Kopmaları**
- **Sorun:** Yarım yazılmış EXR karelerini bulmak, `DWAA` yüzünden bozulan `Cryptomatte` verisini ve `v02` render'da değişen AOV adlarını yakalamak elle yapılır.
- **Çözüm:** `OpenEXR` sekanslarını Nuke'e girmeden tarayıp bozuk scanline karelerini, `Cryptomatte` başlık sağlığını ve `v01-v02` AOV kanal farklarını raporlayan bekçi yazılabilir.

4. **Butik VFX Ekipleri İçin Temiz `EXR` vs. Burn-In `MOV` Çıktı ve Excel Takip Otomasyonu**
- **Sorun:** ShotGrid/AYON olmayan ekiplerde sanatçılar her müşteriye ayrı Nuke `Slate / Burn-In` kurmak ve Excel tablosunu elle güncellemek zorunda kalır.
- **Çözüm:** CSV/Excel plan listesini okuyup hem saf `ACEScg EXR` hem de müşteri kurallarına uygun `Frame 1001` burn-in `MOV` çıktısını tek seferde üreten bir Nuke/Fusion aracı yazılabilir.

## EN // #1 Solve Your Own Problems, Automate Workflow | No Ideas? Here Are Some (`2026-10-30`)

1. **Lens Distortion `STMap` Overscan Bounding-Box Math & Camera Sensor Mismatch Across DCCs**
- **Problem:** Moving tracked cameras across Nuke, Blender, Houdini, and Unreal requires manual math per lens because each DCC uses incompatible sensor-fit and overscan formulas for `STMap` redistortion.
- **Solution:** Build utility that reads a 32-bit `STMap` EXR bounding box and outputs exact camera overscan settings for Blender, Houdini, Unreal, and Nuke.

2. **`OpenUSD` & `MaterialX` Cross-DCC Translation Breakage (`Blender <-> Houdini Solaris <-> Unreal 5`)**
- **Problem:** Stage metric collisions (`Z-up/m` vs `Y-up/m` vs `Z-up/cm`), unpacked Houdini primitives, and hardcoded absolute texture/UDIM paths cause 100x scale errors and untextured meshes across DCCs.
- **Solution:** Build `pxr.Usd` sanitizer that normalizes `metersPerUnit`/`upAxis`, unpacks geometry, and rewrites `MaterialX`/UDIM textures to relative paths.

3. **Corrupted Multi-Part `OpenEXR` Farm Frames, `Cryptomatte` Manifest Stripping & Version-Up AOV Diffing**
- **Problem:** Artists manually hunt truncated EXR frames, lose `Cryptomatte` IDs to lossy `DWAA` compression or ACES IDTs, and get black channels in Nuke when 3D artists rename AOV layers between `v01` and `v02`.
- **Solution:** Build `OpenImageIO`/`OpenEXR` scanner that detects truncated frames, verifies `exr/cryptomatte/*` headers, and diffs AOV channel schemas before Nuke opens.

4. **Boutique VFX Dual-Write (`Clean EXR` + `Burn-In Review MOV`) & Spreadsheet Sync**
- **Problem:** Small VFX teams without ShotGrid spend hours manually wiring per-client Nuke slates/burn-ins and updating Excel shot trackers by hand.
- **Solution:** Generate pre-wired Nuke `.nk` / Fusion `.comp` shot templates directly from a CSV turnover sheet with dual Write nodes (`Clean EXR` + `LUT/Burn-in QuickTime`) and tracker sync.

---

# WG-04 // TOUCHDESIGNER & REALTIME (`#wg04-touchdesigner-and-realtime`)

## TR // #1 Kendi Sorununu Çöz & Otomatikleştir | Fikir Yoksa Öneriler (`2026-10-30`)

1. **TouchDesigner İkili Dosyalarının (`.toe / .tox`) Git Versiyon Kontrolü ve Birleştirme İmkansızlığı**
- **Sorun:** `.toe` ve `.tox` dosyaları sıkıştırılmış binary olduğu için iki kişi aynı projede çalıştığında `git diff / merge` yapılamaz; ekipler her `.py` ve `.glsl` dosyasını elle dışarı ayırır.
- **Çözüm:** `.toe / .tox` içindeki betikleri, shader'ları ve tabloları dış klasöre ayıran ve düğüm/kablo farklarını metin olarak çıkaran Git aracı yazılabilir.

2. **7/24 Müzelerde Derinlik Kamerası (`Orbbec Femto / OAK-D PoE / Kinect`) Donmaları ve PoE Port Kilitlenmesi**
- **Sorun:** Sergilerde tavana asılı `OAK-D PoE` veya `Orbbec` kameralar USB/PoE kilitlenmesi yüzünden donar; `CrashAutoSave` ise projeyi durdurduğu için sahne ekibi merdivenle kablo söker.
- **Çözüm:** TouchDesigner kare hızını ve sensör akışını dışarıdan izleyen, donma anında USB veya PoE switch portunu (`SNMP/SSH`) sıfırlayıp projeyi başlatan bekçi yazılabilir.

3. **Standart Dışı LED Enstalasyonlarda `DMX / Art-Net` 510-Kanal Evren Sınırı ve Serpantin Kablolama**
- **Sorun:** Her DMX evreni 170 RGB pikselde (`510 kanal + 2 boş`) dolar; zikzak (`serpantin`) şeritlerde evren geçişi ortada kaldığında 1 byte kayma tüm renkleri `RGB` yerine `BRG` yapar.
- **Çözüm:** CSV/CAD LED koordinatlarını okuyup 510-kanal evren geçişlerini ve serpantin satır dönüşlerini otomatik hesaplayan ve UV haritası + `DMX Out CHOP` tablosu üreten araç yazılabilir.

4. **DAW <-> TouchDesigner Saat Kayması (`MIDI/OSC` Jitter) ve Projeksiyon Kalibrasyon (`camSchnappr`) Çökmesi**
- **Sorun:** Uzun gösterilerde MIDI/OSC saat kayması yaşanır ve `camSchnappr / Kantan Mapper` kalibrasyon verisi ufak bir hatada bozulup tüm noktaları gösteri öncesi baştan seçtirir.
- **Çözüm:** Örneklem kilitli `SMPTE LTC + OSC` köprüsü ile projeksiyon kalibrasyon matrislerini JSON olarak yedekleyip tek tıkla geri yükleyen `.tox` yazılabilir.

## EN // #1 Solve Your Own Problems, Automate Workflow | No Ideas? Here Are Some (`2026-10-30`)

1. **TouchDesigner Binary (`.toe / .tox`) Git Version Control & Collaborative Diffing Paralysis**
- **Problem:** Because `.toe/.tox` files are compressed binaries, `git diff` fails, forcing teams to manually externalize `.py` DATs, `.glsl` shaders, and tables without wire-change visibility.
- **Solution:** Build auto-externalizer and structural diff tool that unpacks `.toe/.tox` operator trees, parameters, and wire connections into clean JSON/text diffs before Git commits.

2. **Unattended 24/7 Museum Sensor Dropouts (`Orbbec Femto / OAK-D PoE / Kinect`) & Hardware Bus Watchdog**
- **Problem:** Depth cameras in permanent exhibitions freeze due to Windows USB Selective Suspend or PoE switch lock-ups ("the ladder problem"), while `CrashAutoSave.toe` halts cooking instead of self-healing.
- **Solution:** Build external watchdog daemon that monitors TD/sensor heartbeats, resets USB hubs (`pnputil`) or PoE ports (`SNMP/SSH`), and restarts the `.toe`.

3. **`DMX / Art-Net / sACN` Non-Grid Pixel Mapping, 510/512 Universe Rollover & Serpentine Wiring Math**
- **Problem:** Crossing 512-byte DMX universe limits at 170 RGB pixels (`510ch`) on serpentine LED strips causes `RGB -> BRG` byte shifts and manual `DMX Out CHOP` table work.
- **Solution:** Build fixture patcher that reads CSV/CAD coordinates, computes 510ch universe rollovers and serpentine flips, and outputs UV maps + `DMX Out CHOP` tables.

4. **DAW-to-TouchDesigner Clock Drift & Multi-Projector Calibration (`camSchnappr`) State Corruption**
- **Problem:** MIDI/OSC jitter causes sync drift over long shows, and solver glitches inside `camSchnappr` / `Kantan Mapper` corrupt internal Camera COMP storage right before showtime.
- **Solution:** Combine sample-locked `SMPTE LTC + OSC` bridge `.tox` with an external JSON snapshot manager that versions and restores projector calibration matrices in one click.

---

# WG-05 // GAME DESIGN & INTERACTIVE (`#wg05-game-design-and-interactive`)

## TR // #1 Kendi Sorununu Çöz & Otomatikleştir | Fikir Yoksa Öneriler (`2026-10-30`)

1. **Yüzlerce Karakter Animasyonuna Elle `AnimNotify` Dizme ve Retarget Sonrası Kare Kayması (`Unreal / Blender`)**
- **Sorun:** Ses tasarımcıları Unreal `Persona` içinde yüzlerce animasyonu kare kare izleyip ayak basma sesleri için `AnimNotify` ekler; animasyon başka iskelete aktarıldığında (`retargeting`) bildirimler kayar.
- **Çözüm:** Klasördeki tüm animasyonların kemik hızlarını ve `ik_foot_l / ik_foot_r` temas karelerini Python ile okuyup otomatik `AnimNotify` dizen araç yazılabilir.

2. **Wwise/FMOD `SoundbanksInfo.json` ile Unreal `DataTable & GameplayTag` Arasındaki Sessiz Kopukluklar**
- **Sorun:** Wwise/FMOD içinde bir olayın adı, `GUID` kimliği veya `Switch` değeri değiştiğinde Unreal `DataTable` satırları derleme hatası vermez; ses oyunda sessizce kaybolur.
- **Çözüm:** `SoundbanksInfo.json` ile Unreal `DataTable` ve `GameplayTag` dosyalarını karşılaştırıp kopuk referansları oyun paketlenmeden önce raporlayan köprü yazılabilir.

3. **10.000+ Satırlık Çok Dilli Diyaloglarda (`Lokalizasyon`) Sinematik Süre Taşması ve Eksik Dosya Denetimi**
- **Sorun:** Almanca/Fransızca dublaj kayıtları İngilizce orijinalden %25-35 daha uzun sürer; ses süresi Unreal `Sequencer` içindeki sabit kamera planı süresini aştığında replik yarıda kesilir.
- **Çözüm:** Tüm dil klasörlerini ana Excel tablosu ve Unreal `Sequencer` kesme süreleriyle kıyaslayıp süre taşmalarını yakalayan QC aracı yazılabilir.

4. **Unreal `ObjectRedirector` Şişmesi ve 3D Akustik Oda/Portal (`AkSpatialAudioVolume`) Sızıntı Tespiti**
- **Sorun:** Unreal'da klasör taşırken oluşan `ObjectRedirector` zincirleri Git LFS'i şişirir; Wwise Spatial Audio'da ise iki oda hacmi arasındaki milimetrik boşluktan ses duvardan sızar.
- **Çözüm:** Klasör taşıma öncesi Git LFS etki çapını ve `CoreRedirects` satırlarını üreten, aynı zamanda akustik oda/portal geometrilerindeki açık kenarları bulan araç yazılabilir.

## EN // #1 Solve Your Own Problems, Automate Workflow | No Ideas? Here Are Some (`2026-10-30`)

1. **Manual `AnimNotify` Placement & Post-Retargeting Frame Drift Across Hundreds of Skeletal Animations**
- **Problem:** Sound designers spend days scrubbing hundreds of animations in Unreal `Persona` to place footstep notifies by eye, which drift out of sync after skeletal retargeting.
- **Solution:** Build Python (`unreal.AnimationLibrary` / `bpy`) extractor reading `ik_foot_l/r` Z-minimums and zero-velocity frames to batch-insert `AnimNotify` events.

2. **Silent Desync Between Wwise/FMOD `SoundbanksInfo.json` GUIDs and Unreal `DataTables / GameplayTags`**
- **Problem:** Renaming or recreating Events and Switches in Wwise/FMOD silently breaks Unreal `DataTable` structs and `GameplayTag` mappings without a compile error, causing missing audio at runtime.
- **Solution:** Build pre-cook validator that checks `SoundbanksInfo.json` GUIDs/Switches against Unreal `DataTables` and `GameplayTags`.

3. **10,000+ Line Multi-Language VO Duration Overflow vs. Fixed Unreal Sequencer Cutscene Windows**
- **Problem:** Localized VO tracks (German, French, Spanish) expand duration by 20-35%, overflowing fixed cutscene camera cuts in Unreal `Sequencer` and suffering from filename padding errors (`_1.wav` vs `_01.wav`).
- **Solution:** Build batch auditor that compares localized `.wav/.wem` durations against Excel sheets and Unreal `Sequencer` cut budgets before bank builds.

4. **Unreal `ObjectRedirector` LFS Bloat & 3D Acoustic Room/Portal (`AkSpatialAudioVolume`) Seam Leaks**
- **Problem:** Moving UE5 assets creates `ObjectRedirector` webs that bloat Git LFS, while tiny gaps between `AkSpatialAudioVolume` brushes or flipped `AcousticPortal` axes leak sound through walls.
- **Solution:** Build headless dependency analyzer that auto-generates `CoreRedirects` and topology-checks acoustic room/portal bounding boxes for seam gaps and flipped normals.

---

# WG-06 // LOCAL AI & AUTOMATION (`#wg06-local-ai-and-automation`)

## TR // #1 Kendi Sorununu Çöz & Otomatikleştir | Fikir Yoksa Öneriler (`2026-10-30`)

1. **Pro Tools `PTSL` API Sınırı ve İkili `.aaf` + `PTSL` Hibrit `MCP` Sunucusu Eksikliği**
- **Sorun:** Avid'in resmi `PTSL` API'si timeline üzerinde cerrahi klip kaydırma ve yoğun otomasyon yazma işlemlerine izin vermez; `pyaaf2` ise tek başına canlı Pro Tools oturumunu yönetemez.
- **Çözüm:** İkili `.aaf` dosya üretimini (`pyaaf2`) canlı `PTSL` gRPC komutlarıyla birleştirerek ajanların Pro Tools'da tam kurgu/otomasyon yapmasını sağlayan hibrit bir `ProTools-MCP` yazılabilir.

2. **Gizlilik Sözleşmeli (`NDA`) Stüdyolar İçin %100 Çevrimdışı, Negatif Sorgu ve `UCS` Destekli `LAION-CLAP` Arama Motoru**
- **Sorun:** Bulut AI'ın yasak olduğu stüdyolarda ham `LAION-CLAP` betikleri uzun kayıtlardaki 2sn darbeyi bulamaz, negatif sorguları (*"yankısız metal"*) anlamaz ve `UCS` BWF başlığı yazamaz.
- **Çözüm:** Uzun sesleri darbe pencerelerine bölerek indeksleyen, negatif vektör çıkarması yapan ve bulduğu seslere `UCS` BWF metadata başlığı yazan çevrimdışı bir motor yazılabilir.

3. **`WhisperX` + `iXML` Çok Kanallı Set Sesi (`PolyWAV`) ve Senaryo Otomatik Hizalayıcı**
- **Sorun:** Standart deşifre araçları sadece stereo sesi altyazıya çevirir; 12 kanallı `PolyWAV` `iXML` oyuncu/kanal adlarını okuyup senaryoyla eşleştirerek mikrofonları DAW kanalına dizemez.
- **Çözüm:** `WhisperX` zamanlamasını `iXML` ve senaryoyla eşleştirip ham kayıtlardan çok kanallı diyalog kurgusu (`.aaf / .rpp`) üreten araç yazılabilir.

4. **Ağır Ses Ayırma Modellerini (`HT-Demucs ONNX`) DAW ve Wwise Alt Kanallarına Bağlayan Arka Plan Köprüsü**
- **Sorun:** `HT-Demucs` gibi ağır modeller gerçek zamanlı 5ms ses tamponunda çalışamadığı için sesçiler klipleri dışa aktarıp komut satırında ayırarak tekrar DAW'a alır.
- **Çözüm:** Seçili DAW veya Wwise klibini arka planda ekran kartıyla (`demucs-onnx`) ayrıştırıp faz uyumlu alt kanallar olarak oturuma otomatik yerleştiren köprü yazılabilir.

## EN // #1 Solve Your Own Problems, Automate Workflow | No Ideas? Here Are Some (`2026-10-30`)

1. **Pro Tools `PTSL` API Ceiling & Lack of a Hybrid Binary-`.aaf` + `PTSL` Surgical MCP Server**
- **Problem:** Avid's `PTSL` gRPC SDK cannot perform surgical clip-level slip edits or write dense automation curves, while `pyaaf2` alone cannot trigger live Pro Tools session actions.
- **Solution:** Build hybrid `ProTools-MCP` server that pairs binary `.aaf` timeline construction (`pyaaf2`) with live `PTSL` gRPC commands for agentic session building.

2. **100% Offline, NDA-Safe `LAION-CLAP` SFX Search with Negative Prompts, Sub-Clip Windowing & `UCS` Writeback**
- **Problem:** Raw local `LAION-CLAP` scripts fail to locate short transients inside long field recordings, fail on negative queries (*"metal impact WITHOUT reverb"*), and cannot write `UCS` BWF headers.
- **Solution:** Build offline desktop SFX indexer with transient-windowed `LAION-CLAP`, negative vector math, and `UCS` `bext/iXML` tagging.

3. **Offline Field-Recorder `PolyWAV` Script Aligner (`WhisperX` + `iXML` Multi-Track Assembler)**
- **Problem:** Standard Whisper scripts only transcribe stereo scratch tracks into `.srt` files; they cannot parse 12-channel `PolyWAV` `iXML` headers to line up isolated Boom/Lav takes against a script.
- **Solution:** Chain local `WhisperX` word-level alignment with `iXML` track parsing and fuzzy script matching to auto-assemble isolated character Boom/Lav tracks into an `.aaf` or `.rpp` timeline.

4. **Zero-Copy Background `HT-Demucs ONNX` De-Bleed & DAW/Wwise Sub-Track Spawner**
- **Problem:** STFT/Transformer separation models (`HT-Demucs`) require multi-second lookahead windows that crash real-time audio callbacks, forcing manual export/import roundtrips.
- **Solution:** Build background GPU `demucs-onnx` worker that processes selected DAW/Wwise regions offline and automatically spawns phase-coherent stem sub-tracks in place.

---

# WG-07 // FIELD QA & BENCHMARKS (`#wg07-field-qa-and-benchmarks`)

## TR // #1 Kendi Sorununu Çöz & Otomatikleştir | Fikir Yoksa Öneriler (`2026-10-30`)

1. **Hemen Şimdi `VCut2DAW v1.0.2` Saha Testi (`-> Tier 1 & İlk 50 Lifetime V1 Access`)**
- Elinizdeki gerçek bir kurgu videosunu (`.mp4 / .mov`) veya `.edl` dosyasını `VCut2DAW v1.0.2` içine atıp çıkan **Dummy `.aaf`** ve **`960 PPQ .mid`** dosyalarını DAW içinde açarak 1 ekran görüntüsü paylaşın.

2. **Açık Kaynak Kurgu/Ses `.aaf / .edl / .xml` İşkence Testi Veri Seti & Ön-Doğrulayıcı (`-> Tier 2`)**
- **Sorun:** Farklı kurgu yazılımlarından (`Premiere`, `Resolve`, `Avid`, `Final Cut`) çıkan Türkçe karakterli, karışık kare hızlı (`23.976` + `25` + `29.97 DF`), hız eğrili ve MP4 AAC kaymalı dosyalar DAW/color aktarımını çökertir.
- **Çözüm:** Tüm NLE'lerin ürettiği en sorunlu `.aaf / .edl / .xml` örneklerinden açık kaynak bir test veri seti oluşturup, DAW öncesi Unicode, DF/NDF ve hız eğrisi hatalarını onaran doğrulayıcı yazılabilir.

3. **Dolby Atmos `ADM BWF` (`axml`) Başlık, `24fps` Timecode ve Downmix True-Peak Ön-QC Tarayıcısı**
- **Sorun:** Onlarca GB boyutundaki Dolby Atmos `ADM BWF` dosyaları; `axml` başlığında kare hızının 24fps yerine 25/30fps kalması, stereo yedekle örneklem farkı veya 5.1/Binaural katlama sırasındaki `-1.0 dBTP` aşımı yüzünden QC'den döner.
- **Çözüm:** Devasa `ADM BWF` dosyasını Dolby Renderer açmadan saniyeler içinde `axml/chna` başlığı, örneklem sayısı ve downmix True-Peak açısından denetleyen QC aracı yazılabilir.

4. **Ses Eklentilerinde (`VST3 / CLAP / AU`) Gerçek Zamanlı Bellek Ayırma (`malloc`) ve `PDC` Gecikme Kayması Testi**
- **Sorun:** `pluginval` aracı Windows/Linux üzerinde ses thread'i içindeki gizli `malloc/mutex` kilitlenmelerini yakalayamaz ve eklentinin DAW'a bildirdiği `PDC` gecikmesi ile gerçek akustik gecikmesinin tutarlılığını ölçmez.
- **Çözüm:** Eklentiye birim dürtü (`impulse`) sinyali gönderip akustik gecikmeyi `PDC` ile kıyaslayan ve ses thread'i bellek ihlallerini bulan doğrulayıcı yazılabilir.

## EN // #1 Solve Your Own Problems, Automate Workflow | No Ideas? Here Are Some (`2026-10-30`)

1. **Immediate 2-Minute `VCut2DAW v1.0.2` Field Test (`-> Tier 1 & First 50 Lifetime V1 Access`)**
- Drop any real reference video (`.mp4 / .mov`) or `.edl` into `VCut2DAW v1.0.2`, open the generated **Dummy `.aaf`** and **`960 PPQ .mid`** markers in your DAW, and post 1 screenshot + OS/DAW version in <#1564427991709130825>.

2. **Cross-NLE `.aaf / .edl / .xml` Conform Torture Corpus & Pre-Flight Validator (`-> Direct Tier 2`)**
- **Problem:** Non-ASCII/Turkish characters (`NFD` vs `NFC` Unicode), `23.976` vs `24.000` pull-down mismatches, `29.97 DF/NDF` drift, and unrendered speed ramps regularly corrupt DAW/NLE conforms.
- **Solution:** Curate an open-source torture-test corpus across Premiere, Resolve, Avid, and Final Cut alongside a pre-flight validator that normalizes Unicode and flags frame-rate/speed-ramp drift.

3. **Dolby Atmos `ADM BWF` (`axml`) Structural Metadata, `24fps` Timecode & Downmix True-Peak Pre-QC Scanner**
- **Problem:** Multi-GB Dolby Atmos `ADM BWF` deliveries fail distributor QC due to mismatched `axml` frame-rate flags (25/30fps vs 24fps), sample-length discrepancies against Stereo stems, or `> -1.0 dBTP` spikes during 5.1/Binaural fold-downs.
- **Solution:** Build fast CLI/GUI scanner that checks `ADM BWF` `axml/chna` chunks, sample counts, and 5.1/Binaural downmix True-Peak without Dolby Renderer.

4. **Audio Plugin (`VST3 / CLAP / AU`) Real-Time Allocation (`malloc`) & Acoustic `PDC` Latency Drift Verifier**
- **Problem:** `pluginval` lacks cross-platform real-time allocation interception on Windows/Linux and never checks whether a plugin's actual acoustic impulse delay matches its host-reported `PDC` latency after parameter changes.
- **Solution:** Build headless CI test suite that hooks real-time thread allocations and measures impulse-response acoustic delay against reported `PDC` across sample rates and buffers.

---

# WG-08 // CLEAN-ROOM DESIGN & LEGAL REVERSE ENGINEERING (`#wg08-clean-room-and-legal-re`)

# WG-08 // CLEAN-ROOM DESIGN & LEGAL REVERSE ENGINEERING (`Interoperability`)

> **#1 PRIORITY // Solve Your Own Problems, Automate Your Workflow (`-> Direct Tier 2`)**
> **EN:** Automating your workflow is #1 priority; no ideas? See repos & bottlenecks below. *Before coding, scan current open-source repos and plan with AI (`clean-room`) which existing tools can be used.*
> **TR:** #1 öncelik kendi iş akışınızı otomatikleştirmektir; fikriniz yoksa aşağıdaki depo ve önerilere bakın. *Üretime başlamadan güncel açık kaynakları tarayın, `clean-room` ve AI ile var olan hangi programların kullanılabileceğini planlayın.*

> **⚖️ KESİN YASAL SINIR // STRICT LEGAL BOUNDARY (`100% Clean-Room & Interoperability ONLY`):**
> **TR:** Yalnızca birlikte çalışabilirlik (`EU Dir. 2009/24/EC Madde 6` & `17 U.S.C. § 1201(f)`) kapsamında kendi ürettiğimiz dosyaların yapısal analizi (`black-box`) ve sıfırdan özgün kod üretimi (`clean-room`) yapılır. **Lisans/DRM/iLok kırma (`cracking`), korsan paylaşım veya kapalı kaynak kod kopyalama kesinlikle yasaktır.**
> **EN:** Strictly limited to lawful interoperability (`EU Dir. 2009/24/EC Art. 6` & `17 U.S.C. § 1201(f)`), black-box file inspection, and clean-room code. **DRM/iLok bypass, cracking, piracy, or copying proprietary code is strictly prohibited.**

### Open-Source Repos // Açık Kaynak Depolar
- **[kaitai-io/kaitai_struct](https://github.com/kaitai-io/kaitai_struct)**: İkili (`.aaf`, `.wav/iXML`) dosya yapılarını `.ksy` şemalarıyla tanımlayıp Python/C++/Rust okuyucu üreten açık standart.
- **[WerWolv/ImHex](https://github.com/WerWolv/ImHex)**: Kendi test dosyalarınızın byte/chunk yapısını inceleyip temiz format şartnamesi çıkarmak için açık Hex editörü.
- **[markreidvfx/pyaaf2](https://github.com/markreidvfx/pyaaf2)** & **[AcademySoftwareFoundation/OpenTimelineIO](https://github.com/AcademySoftwareFoundation/OpenTimelineIO)**: Kurgu/ses formatlarının (`AAF`, `EDL`, `XML`, `OTIO`) yasal `clean-room` referansları.

## TR // #1 Kendi Sorununu Çöz & Otomatikleştir | Fikir Yoksa Öneriler (`2026-10-30`)

1. **DaVinci Resolve `.drx / .drp` ve Reaper `.rpp` Dosyaları İçin Clean-Room Şema Sözlüğü**
- **Sorun:** Yazılımların iç API'leri (`DaVinciResolveScript`) düğüm parametrelerinin çoğunu gizlediği için stüdyolar kendi proje dosyalarındaki verileri dışarıdan toplu yönetemez.
- **Çözüm:** Kendi örnek `.drx / .drp / .rpp` dosyalarımızda tek tek parametre değiştirip (`black-box diffing`) hangi XML/metin alanının ne işe yaradığını belgeleyen yasal bir `JSON / Kaitai` şeması hazırlanabilir.

2. **Belgelenmemiş `.aaf / iXML / BWF` Metadata Blokları İçin `Kaitai Struct` Haritası**
- **Sorun:** Farklı NLE ve saha kayıt cihazlarının `.aaf` ve `PolyWAV` içine yazdığı özel metadata blokları belgelenmediği için aktarımda sessizce kaybolur.
- **Çözüm:** `ImHex` ve `Kaitai Struct` ile kendi test kayıtlarımız üzerinden bu metadata bloklarının temiz yapısal şartnamesini çıkaran ve `OpenTimelineIO` içine bağlayan araç yazılabilir.

3. **Stüdyo Kontrolcüleri ve Sahne Cihazları İçin Yasal `OSC / MIDI SysEx / Art-Net` Protokol Belgeleyici**
- **Sorun:** Donanım kontrol yüzeyleri veya sensörler çoğu zaman eksik belgelenmiş UDP/MIDI paketleri gönderdiği için Linux/macOS veya TouchDesigner/Reaper bağlantısı kurulamaz.
- **Çözüm:** Cihazın kendi ağ/MIDI trafiğini gözlemleyip (`Wireshark / MIDI Monitor`) mesaj yapısını temiz şartnameye döken ve açık TouchDesigner/Reaper sürücüsü üreten araç yazılabilir.

4. **AI Agent İle İki Odalı (`Two-Room Clean-Room`) Şartname ve Kod Üretim Şablonu**
- **Sorun:** Geliştiriciler mevcut bir aracın işlevini kendi açık kaynak projelerine eklerken telif sınırlarını nasıl koruyacaklarını ve açık kütüphaneleri nasıl birleştireceklerini bilemez.
- **Çözüm:** Önce girdi/çıktı gözleminden saf matematiksel `CLEAN_SPEC.md` üreten, ardından ikinci bir AI ajanıyla sıfırdan özgün `AGPLv3` kod yazdıran iki aşamalı şablon repo kurulabilir.

## EN // #1 Solve Your Own Problems, Automate Workflow | No Ideas? Here Are Some (`2026-10-30`)

1. **Clean-Room Schema Dictionary for DaVinci Resolve `.drx / .drp` & Reaper `.rpp` Files**
- **Problem:** Internal scripting APIs (`DaVinciResolveScript`) hide most node-graph parameters, preventing studios from batch-managing their own project files externally.
- **Solution:** Perform black-box input/output diffing on self-generated `.drx / .drp / .rpp` test files to document an open `JSON / Kaitai` schema dictionary without touching proprietary binaries.

2. **`Kaitai Struct` Specification for Undocumented `.aaf / iXML / BWF` Metadata Chunks**
- **Problem:** Vendor-specific metadata chunks inside `.aaf` and `PolyWAV` files are poorly documented, causing silent track/timecode loss across NLEs and DAWs.
- **Solution:** Inspect self-created test recordings in `ImHex` to author clean `.ksy` (`Kaitai Struct`) format specs and open-source `OpenTimelineIO` adapters.

3. **Clean-Room `OSC / MIDI SysEx / Art-Net` Hardware Protocol Logger & Open Driver Generator**
- **Problem:** Studio fader banks, sensors, and lighting controllers often use undocumented MIDI SysEx or UDP packets, locking them out of Linux, Reaper, or TouchDesigner.
- **Solution:** Capture lawful wire traffic (`Wireshark / MIDI Monitor`) from your own hardware to write a clean protocol specification and generate open-source TouchDesigner/Reaper bridges.

4. **Two-Step AI Clean-Room Workflow Template (`Black-Box Spec -> Original Code`)**
- **Problem:** Practitioners want to replicate high-level studio workflows using open-source libraries without accidentally tainting their project with proprietary code.
- **Solution:** Build a two-stage AI prompt/repo template where Agent A writes a pure mathematical `CLEAN_SPEC.md` from black-box I/O observations and Agent B implements original `AGPLv3` code strictly from that spec.

---

## BÖLÜM B // DERİNLEMESİNE TEKNİK REFERANS VE KANIT RAPORU (DEEP-DIVE EVIDENCE LEDGER)



# XULAB // 2026 CROSS-INDUSTRY UNSOLVED BOTTLENECK & MANUAL-LABOR ("AMELELİK") RESEARCH REPORT

*Generated: 2026-10-30 | Scope: WG-01 through WG-07 | Methodology: Multi-Agent Evidence-First Search across Reddit, LiftGammaGain, Gearspace, JWSoundGroup, VI-Control, OdForce, Derivative Forum & GitHub Issues*

---

## 0. Prior-Art Exclusion Ledger (What Is Already Solved and Must Not Be Re-Invented)

| Working Group | Solved Problem (Prior Art) | Existing Native Feature or Commercial Tool | Why Excluded / Where the Real Gap Starts |
| :--- | :--- | :--- | :--- |
| **WG-01 (Audio Post)** | Picture cut reconforming & EDL ripple | *The Cargo Cult Matchbox* ($379-$600+), *Conformalizer* | Solved for high-end studios; gap is broken non-ASCII/Turkish AAFs and Premiere Merged Clips destruction. |
| **WG-01 (Audio Post)** | Boom/Lav phase alignment | *Sound Radix Auto-Align Post 2*, *VocAlign* | Solved algorithmically; do not rebuild basic phase alignment. |
| **WG-01 (Audio Post)** | Single-clip denoising | *iZotope RX*, *Accentize dxRevive*, *Hush*, *Cedar* | Solved; the unsolved gap is harvesting real production room-tone from PolyWAV handles and PFX hole QC. |
| **WG-02 (Picture / Color)** | Timeline cut comparison & grade migration | *DaVinci Resolve Timeline Compare* & *ColorTrace* | Built natively into Resolve; do not build basic timeline cut diffing. |
| **WG-02 (Picture / Color)** | Camera RAW metadata to ACES IDT | *DaVinci Wide Gamut / ACES Auto-IDT* | Built natively into Resolve for BRAW/RED/ARRI/Sony MXF. |
| **WG-03 (VFX / 3D)** | Enterprise studio shot tracking | *Autodesk Flow (ShotGrid) + Flame / Hiero* | Costs $50k+/yr and requires dedicated Pipeline TDs; completely inaccessible to boutique/indie studios. |
| **WG-05 (Game Audio)** | Basic Reaper-to-Wwise transfer | *Audiokinetic ReaWwise* (Official C++ extension) | Already free and official; real gap is `SoundbanksInfo.json <-> Unreal DataTable` desync and `AnimNotify` placement. |
| **WG-06 (Local AI / MCP)** | Basic Reaper / Blender / Resolve MCP wrappers | `xDarkzx/Reaper-MCP`, `ahujasid/blender-mcp`, `samuelgursky/davinci-resolve-mcp` | Basic read/trigger wrappers exist; real gap is deep binary `.aaf` / `.drx` / `PTSL` hybrid surgical manipulation. |
| **WG-07 (Field QA)** | Basic VST3/AU parameter fuzzing | `Tracktion/pluginval`, `free-audio/clap-validator` | Basic state/crash fuzzing exists; real gap is acoustic PDC latency drift and real-time allocation (`malloc`) interception on Windows/Linux CI. |

---

## 1. WG-01 // AUDIO POST-PRODUCTION, DIALOGUE/ADR/FOLEY & DAW CONFORM

### Bottleneck WG01-01: Premiere Pro / Resolve -> Pro Tools AAF Metadata Stripping, "Merged Clips" Destruction & Non-ASCII (Turkish UTF-8) Corruption
- **Evidence Sources:** `r/AudioPost`, `r/editors`, `JWSoundGroup`, `Avid DUC`, `Blackmagic Forum`.
- **The Manual Labor ("Amelelik"):**
  1. Legacy AAF SDK (v1.1/1.2) implementations in Premiere and Pro Tools choke on non-ASCII characters (`ğ, ü, ş, ı, ö, ç, İ`) and macOS NFD vs. Windows NFC/CP1254 Unicode normalization inside folder paths, clip names, or Sound Devices `iXML` track labels. Pro Tools throws `"Error reading AAF WAVE Data"` or fails Field Recorder Guide Track relinking, forcing assistants to relink hundreds of files manually.
  2. When Premiere editors sync sound using *Merged Clips* or *Multicam*, Premiere generates synthetic master clip IDs that strip original BWF `OriginatorReference`, `TimeReference` sample offsets, and `TAPE` / Sound Roll tags—collapsing 8-channel PolyWAV iso tracks (`Boom`, `Lav 1..6`) into unlinked mono tracks.
- **Target Open-Source Tool:** **Pre-Flight AAF/XML Unicode Sanitizer & PolyWAV Acoustic/Timecode Relink Rebuilder** (`pyaaf2` + `OpenTimelineIO` + BWF/iXML chunk normalizer).

### Bottleneck WG01-02: "Fully Filled" M&E (Music & Effects) Stem QC, PFX Hole Detection & Mathematical Sum-to-Master Verification
- **Evidence Sources:** `r/AudioPost`, `Gearspace Post-Production Forum` (Netflix / Disney / Amazon theatrical & OTT delivery QC rejection threads).
- **The Manual Labor ("Amelelik"):**
  Re-recording mixers and QC engineers must listen through 90-to-120-minute mixes at **1x real-time speed** toggling between Printmaster, Dialogue (`DX`), and `M&E` stems to catch three fatal rejection causes:
  1. **Unfilled PFX Holes:** A physical sound on set (footstep, door close, prop grab, cloth rustle) was on the production DX track during a non-speech interval, got muted for the foreign dub, and was missed by Foley/FX—leaving dead silence on screen in the M&E.
  2. **Dialogue Bleed in M&E:** Faint vocal bleed or shared dialogue reverb leaking into the M&E stem.
  3. **Summation Null Failure (`DX + MX + FX != Printmaster`):** Master-bus compression causing the summed stems to diverge from the Printmaster.
- **Target Open-Source Tool:** **100x Offline M&E Stem QC & PFX Hole Detector** (Cross-compares non-phoneme transient energy in `DX_Stem.wav` against `ME_Stem.wav`, runs high-sensitivity VAD on `ME_Stem.wav` to catch vocal bleed, and runs phase-inverted null tests against `Printmaster.wav`).

### Bottleneck WG01-03: PFX Excavation & Real Production Room-Tone Harvesting from PolyWAV Handles
- **Evidence Sources:** `r/AudioPost` dialogue editorial workflow threads.
- **The Manual Labor ("Amelelik"):**
  Dialogue editors spend 60%+ of their time cutting out breaths/PFX and backfilling every single cut gap on dialogue tracks with room tone. Mixers dislike *iZotope RX Ambience Match* because synthesized spectral noise sounds frozen/phasey on gaps >1.5s. Editors still manually scrub the pre-roll/post-roll handles of raw production PolyWAVs to harvest real room tone for every scene.
- **Target Open-Source Tool:** **Automated PolyWAV Handle Room-Tone Harvester & Gap Backfiller** (Scans raw production PolyWAV heads/tails referenced in an `.aaf/.rpp`, extracts clean 3-10s real room-tone windows per Scene/Take, and auto-fills dialogue cut gaps with equal-power crossfades).

### Bottleneck WG01-04: Automation-Aware Music & SFX Cue Sheet Generation (RapidCue / ASCAP / BMI / PRS)
- **Evidence Sources:** `r/AudioPost`, `VI-Control`, `Gearspace`.
- **The Manual Labor ("Amelelik"):**
  Basic EDL-to-CSV scripts only read clip container start/end boundaries. In real dubs, mixers fade music cues out early using **Pro Tools volume/mute automation** or VCA groups, or stems have 15 seconds of silent tail. Assistants spend 1-2 days manually logging actual audible In/Out timecodes into Excel for RapidCue/PRO delivery.
- **Target Open-Source Tool:** **Automation- & RMS-Silence-Aware Cue Sheet Generator** (Combines clip boundaries + DAW volume automation curves + `-60 dBFS` RMS silence detection to output frame-accurate ASCAP/BMI/PRS Excel cue sheets).

---

## 2. WG-02 // PICTURE EDITING, ASSISTANT EDITING, VFX TURNOVER & COLOR GRADING

### Bottleneck WG02-01 (FLAGSHIP): Boutique VFX Shot Drop-In (`v001` -> `v003`), Frame-1000 Slate Stripping, Handle Math & Vertical Track Stacking
- **Evidence Sources:** `r/editors`, `LiftGammaGain`, `Blackmagic Forum` (*"Reconform from Bins Resolve VFX versions fail timecode handles slate"*).
- **The Manual Labor ("Amelelik"):**
  Without a $50k+ *ShotGrid + Flame/Hiero* infrastructure, Assistant Editors receive folders of 50-200 returned VFX shots (`SH010_comp_v001.mov`, `v002.mov`, `1001-1088.exr`) and must **manually drop them into the sequence one by one**. Native *Replace Clip* (Premiere) and *Reconform from Bins* (Resolve) fail for 4 mathematical reasons:
  1. **Frame `1000` Technical Slate:** VFX vendors render a 1-frame technical slate at Frame `1000` and start picture at Frame `1001`. Native replacement puts the slate into the edit or shifts sync by +1 frame.
  2. **Head/Tail Handle Offset (`+8f` / `+12f` / `+24f`):** The timeline cut is `64 frames`, but the returned VFX file is `89 frames` (`1 slate + 12 head handle + 64 cut + 12 tail handle`). Native replacement aligns to Frame 0, throwing the cut `13 frames` out of sync.
  3. **Zeroed Timecode (`00:00:00:00`):** Freelance AE/Blender/Nuke renders often reset container timecode to `00:00:00:00`, causing Resolve's *Reconform from Bins* to abort completely.
  4. **Non-Destructive Vertical Version Stacking:** Editors never overwrite `v001`; they need `v003` stacked on track `V4` directly above `v002` (`V3`) and `v001` (`V2`), with older versions disabled so the director can toggle comparison in 1 second.
- **Target Open-Source Tool:** **Smart VFX Drop-In, Slate/Handle Trimmer & Vertical Track Stacker** (Matches shot IDs via regex/markers, strips Frame 1000 slate, computes exact `(N_returned - N_slate - N_cut) / 2` handle trim points, stacks `v003` on the top VFX track, and disables `v002`).

### Bottleneck WG02-02: Variable Speed Ramps (Bezier Time-Remapping) & Optical Flow Translation Between Premiere, Resolve & Nuke
- **Evidence Sources:** `r/editors`, `r/colorists`, `LiftGammaGain`.
- **The Manual Labor ("Amelelik"):**
  FCP7 XML and AAF cannot translate Premiere/Avid bezier variable speed ramps into DaVinci Resolve or Nuke. Clips arrive at constant speed or slipped by dozens of frames, and AEs pulling raw VFX plates cannot easily calculate the exact minimum/maximum source camera frames consumed by a non-linear speed curve.
- **Target Open-Source Tool:** **Bezier Speed-Ramp Integrator & Nuke/Resolve Retime Curve Exporter** (Reads Premiere/Avid speed keyframes, calculates exact raw camera frame extents for VFX pulls, and generates an exact per-frame ASCII retime curve / Nuke `TimeWarp` node).

### Bottleneck WG02-03: Premiere Pro -> DaVinci Resolve XML Un-Nesting & Mixed-Resolution Sizing Math Normalization
- **Evidence Sources:** `r/colorists`, `LiftGammaGain`.
- **The Manual Labor ("Amelelik"):**
  Colorists waste 4-8 hours per conform flattening Premiere *Nested Sequences* and fixing broken X/Y/Scale framing because Premiere mixes pixel-relative *Set to Frame Size* and percentage-based *Scale to Frame Size* across 4K/6K/8K camera clips.
- **Target Open-Source Tool:** **Pre-Conform XML Un-Nester & Sizing Matrix Normalizer** (`OpenTimelineIO` / XML pre-processor that flattens nests and converts Premiere spatial transforms into exact Resolve Edit Sizing `Zoom/Pan/Tilt` coordinates).

### Bottleneck WG02-04: `.drx` Node-Graph XML Parsing for VFX `CDL + Look` Splitting & Inbound VFX "Freeze-Handle / Color-Shift" QC
- **Evidence Sources:** `r/colorists`, `LiftGammaGain`.
- **The Manual Labor ("Amelelik"):**
  1. Resolve's `DaVinciResolveScript` API is blind to internal node parameters and `DCTL` sliders, forcing manual node surgery when separating primary `ASC CDL` balance from creative `Show LUT` looks across 200 shots.
  2. When VFX shots return, AEs manually scrub every shot in `Difference` mode to catch accidental frozen handle frames (`Frame[n] == Frame[n-1]`), 1px blanking edges, or accidental `Rec.709` clamping on `ACEScg/Log` plates.
- **Target Open-Source Tool:** **External `.drx` XML Node Parser & Automated Inbound VFX Plate QC Scanner**.

---

## 3. WG-03 // VFX COMPOSITING, 3D / CG PIPELINES & OpenUSD

### Bottleneck WG03-01: Lens Distortion `STMap` Overscan Bounding-Box Math & Optical Metadata Loss Across Nuke, Blender, Houdini & Unreal
- **Evidence Sources:** `r/NukeVFX`, `r/vfx`.
- **The Manual Labor ("Amelelik"):**
  Moving a tracked camera (`3DEqualizer / SynthEyes / Nuke`) into Blender, Houdini, or Unreal requires rendering CG with exact **Overscan** so that when the 32-bit float `STMap` redistorts the CG in Nuke, the edges don't clip. Every DCC uses incompatible sensor/overscan math (Blender single sensor fit vs. Nuke `window_scale`/BBox vs. Houdini aperture), forcing artists to do manual spreadsheet math per lens.
- **Target Open-Source Tool:** **Universal Lens `STMap` Overscan & Camera Sensor Calculator** (Reads an `STMap` EXR bounding box or lens grid and outputs exact copy-paste camera focal/aperture/resolution scripts for Blender `bpy`, Houdini `hou`, Unreal, and Nuke).

### Bottleneck WG03-02: `OpenUSD` & `MaterialX` Cross-DCC Breakage (Blender <-> Houdini Solaris <-> Unreal Engine 5)
- **Evidence Sources:** `r/Houdini`, `OdForce`, `r/blender`.
- **The Manual Labor ("Amelelik"):**
  1. Stage metric collisions: Blender (`Meters, Z-up`), Houdini (`Meters, Y-up`), and Unreal (`Centimeters, Z-up`) strip or override `metersPerUnit` and `upAxis`, causing 100x scale explosions or 90-degree rotations.
  2. Houdini RBD packed primitives exported without explicit `name`/`path` unpacking arrive as empty locators in Blender/Unreal.
  3. Hardcoded absolute texture paths and broken `UDIM` / `MaterialX` bindings result in pink/white untextured geometry on import.
- **Target Open-Source Tool:** **OpenUSD Stage Sanitizer & Relative MaterialX/UDIM Repather** (`pxr.Usd` CLI/GUI pre-flight validator that enforces `metersPerUnit`/`upAxis`, unpacks instancers cleanly, and rewrites absolute texture/UDIM paths to portable relative schemas).

### Bottleneck WG03-03: Multi-Part `OpenEXR` Corrupted Farm Frames, `Cryptomatte` Manifest Stripping & Version-Up AOV Relink Fragility
- **Evidence Sources:** `r/NukeVFX`, `r/vfx`.
- **The Manual Labor ("Amelelik"):**
  1. Overnight renders produce truncated or 0-byte EXR frames; artists manually hunt broken frame numbers (`1004-1007, 1042`) to resubmit to Deadline.
  2. Rendering `Cryptomatte` with lossy `DWAA/DWAB` compression or letting ACES apply an IDT to data AOVs destroys matte IDs; upstream Nuke `Shuffle/Reformat` nodes strip `exr/cryptomatte/*` manifest metadata.
  3. When 3D artists version up (`v01 -> v02`) and rename/drop an AOV layer, downstream Nuke `Shuffle` and `Cryptomatte` nodes silently output black.
- **Target Open-Source Tool:** **EXR Sequence Integrity, Cryptomatte Manifest & AOV Schema Diff Doctor** (`OpenImageIO` / `OpenEXR` header scanner that detects truncated scanlines, verifies raw data-pass compression, and diffs AOV channel schemas between `v01` and `v02` before Nuke opens).

### Bottleneck WG03-04: Boutique VFX Plate Pull, Clean-EXR vs. Review Burn-In Slate & Spreadsheet Sync
- **Evidence Sources:** `r/vfx`, `r/NukeVFX`.
- **The Manual Labor ("Amelelik"):**
  Freelancers and small VFX teams manually configure Nuke `Text/Slate` and `Write` nodes for every client spec—separating clean working EXRs from editorial review QuickTimes (requiring baked LUT, Frame `1001` counter, shot code, and slate) while manually updating Google Sheets/Excel trackers.
- **Target Open-Source Tool:** **CSV-Driven Nuke/Fusion Shot Template, Slate & Dual-Write Generator**.

---

## 4. WG-04 // TOUCHDESIGNER, GLSL SHADERS, SHOW CONTROL & LIVE AV (`Studio Node`)

### Bottleneck WG04-01: TouchDesigner Monolithic Binary (`.toe / .tox`) Git Version Control & Collaborative Diffing Paralysis
- **Evidence Sources:** `r/TouchDesigner`, `Derivative Forum`.
- **The Manual Labor ("Amelelik"):**
  Because `.toe` and `.tox` files are compressed binaries, standard `git diff` and merge workflows fail. Multi-developer teams (`Studio Node` style) must manually externalize every `.py` DAT, `.glsl` shader, and sub-system `.tox` into external folder trees, and still cannot cleanly diff or merge parameter/wiring changes inside binary `.tox` containers.
- **Target Open-Source Tool:** **TouchDesigner `.toe / .tox` Structural Inspector, Auto-Externalizer & Visual Node-Graph Diff Utility** (Automates `tox` modularization + `.py/.glsl/.json` parameter table externalization and generates a human-readable structural diff of operators, parameters, and wire connections before Git commit).

### Bottleneck WG04-02: Unattended 24/7 Museum Installation Sensor Dropouts (`Orbbec Femto / OAK-D PoE / Kinect`) & Hardware Bus Watchdog
- **Evidence Sources:** `Derivative Forum`, `r/TouchDesigner`.
- **The Manual Labor ("Amelelik"):**
  In permanent exhibitions, USB depth cameras (`Orbbec Femto Bolt/Mega`, `Azure Kinect`) and overhead `Luxonis OAK-D PoE` sensors freeze due to USB Selective Suspend, ESD drops, or PoE firmware lock-ups ("the ladder problem"), while `CrashAutoSave.toe` halts cooking instead of self-healing.
- **Target Open-Source Tool:** **Hardware-Aware Exhibition Watchdog & PoE/USB Auto-Healer** (External daemon monitoring TD UDP heartbeat + sensor frame delta; automatically resets Windows USB hub power states via `pnputil` or power-cycles locked PoE switch ports via SNMP/SSH and restarts the `.toe` in kiosk mode).

### Bottleneck WG04-03: `DMX / Art-Net / sACN` Non-Grid Pixel Mapping, 510/512 Universe Rollover Math & Serpentine Wiring Hell
- **Evidence Sources:** `Derivative Forum`, `r/lightingdesign`.
- **The Manual Labor ("Amelelik"):**
  Each DMX universe holds 512 channels, capping RGB strips at 170 pixels (`510 channels` + 2 dead channels) or 128 RGBW pixels. When custom LED sculptures or serpentine (zigzag) strips cross universe boundaries mid-strip, off-by-one byte shifts corrupt RGB into BRG. Engineers manually wrangle CSV fixture coordinates and hand-build `DMX Out CHOP` routing tables.
- **Target Open-Source Tool:** **Visual 3D/2D LED Fixture Patcher & Automatic 510/512 Universe Rollover `.tox` Generator** (Ingests CAD/CSV fixture coordinates, handles serpentine row flipping and 510-channel universe rollover math automatically, and outputs ready-to-use UV lookup textures + `DMX Out CHOP` unicast routing tables).

### Bottleneck WG04-04: DAW-to-TouchDesigner Clock Drift (`MIDI/OSC` Jitter vs. `SMPTE LTC`) & Multi-Projector Calibration State Corruption
- **Evidence Sources:** `Derivative Forum`, `r/TouchDesigner`.
- **The Manual Labor ("Amelelik"):**
  1. MIDI Clock over USB jitter and OSC packet variance cause audio-visual sync drift over long shows unless SMPTE LTC audio timecode is striped and sample-rate locked.
  2. Native calibration tools (`camSchnappr`, `Kantan Mapper`, `Stoner`) store calibration matrices inside fragile internal storage; a solver glitch corrupts the Camera COMP, forcing technicians to re-pick 3D-to-2D points from scratch minutes before doors open.
- **Target Open-Source Tool:** **Deterministic LTC/OSC Show-Control Bridge & Versioned Projector Calibration Snapshot Manager**.

---

## 5. WG-05 // GAME DESIGN, TECHNICAL DESIGN, GAME AUDIO (`Wwise / FMOD`) & ENGINES (`Unreal / Godot`)

### Bottleneck WG05-01: Manual `AnimNotify` Placement & Post-Retargeting Frame Drift Across Hundreds of Skeletal Animations
- **Evidence Sources:** `r/gameaudio`, `r/unrealengine`, `Unreal Engine Forums`.
- **The Manual Labor ("Amelelik"):**
  Technical sound designers spend days scrubbing hundreds of `.uasset` animations in Unreal `Persona` to place footstep, scuff, and foley `AnimNotify` markers by hand. Worse, when animations are retargeted to different character skeletons or blended in `BlendSpaces`, notify frames drift away from actual foot-to-ground contact.
- **Target Open-Source Tool:** **Batch Kinematic Bone-Contact `AnimNotify` Auto-Extractor & Retarget Drift Validator** (Reads `ik_foot_l` / `ik_foot_r` Z-height minimums and zero-velocity inflection frames across entire animation folders via `unreal.AnimationLibrary` / `bpy` and batch-writes frame-accurate `AnimNotify` tracks).

### Bottleneck WG05-02: Silent Desync Between Wwise/FMOD `SoundbanksInfo.json` GUIDs and Unreal `DataTables / GameplayTags`
- **Evidence Sources:** `Audiokinetic Community`, `r/gameaudio`.
- **The Manual Labor ("Amelelik"):**
  When sound designers rename Events, Switches, or States or delete-and-recreate items in Wwise/FMOD, Unreal `DataTables` and `GameplayTags` referencing those GUIDs/names silently break without throwing a compiler error—only failing at runtime during QA playtests.
- **Target Open-Source Tool:** **Bidirectional `SoundbanksInfo.json` <-> Unreal `DataTable / GameplayTag` CI Validator & Auto-Fixer**.

### Bottleneck WG05-03: 10,000+ Line Multi-Language VO Spreadsheet Duration Overflow vs. Unreal Sequencer Cutscene Windows
- **Evidence Sources:** `r/gameaudio`.
- **The Manual Labor ("Amelelik"):**
  Localized voice-over recordings (German, French, Spanish) routinely run 20-35% longer than English source lines. Middleware bank builds do not check whether `VO_Line_042_DE.wav` is 1.4 seconds longer than the fixed camera cut or animation state in Unreal `Sequencer`, nor do they catch vendor filename padding errors (`_1.wav` vs `_01.wav`) before cooking.
- **Target Open-Source Tool:** **Multi-Language VO Duration Overflow & Cutscene Budget Auditor**.

### Bottleneck WG05-04: Unreal `ObjectRedirector` Binary Bloat, `UStruct` Rename Data Loss & Acoustic Room/Portal Seam Leak Detection
- **Evidence Sources:** `r/unrealengine`, `r/gameaudio`, `godotengine/godot-proposals#5704`.
- **The Manual Labor ("Amelelik"):**
  1. Moving folders in UE5 creates `ObjectRedirector` chains that lock up RAM and dirty hundreds of GBs in Git LFS/Perforce, while renaming a `UStruct` field without manual `CoreRedirects` wipes `DataTable` data.
  2. Microscopic seam gaps between `AkSpatialAudioVolume` brushes or flipped `AcousticPortal` Z-axes cause audio to leak through solid walls, requiring manual level walks with a debugger.
- **Target Open-Source Tool:** **Headless Unreal Redirector Blast-Radius Analyzer, `CoreRedirects` Generator & Acoustic Volume Seam Topology Checker**.

---

## 6. WG-06 // LOCAL AI MODELS, AUDIO/VISION ML & `MCP` STUDIO BRIDGES

### Bottleneck WG06-01: Pro Tools `PTSL` gRPC Ceiling & Lack of a Hybrid Binary-`.aaf` + `PTSL` Surgical MCP Server
- **Evidence Sources:** `github.com/skrul/protools-mcp-server`, `AcademySoftwareFoundation/OpenTimelineIO`, `markreidvfx/pyaaf2`.
- **The Manual Labor ("Amelelik"):**
  Avid's official `PTSL` gRPC API cannot perform surgical clip-level slip/ripple edits or read/write dense volume automation curves, while `pyaaf2` / `otio-aaf-adapter` drops proprietary clip-gain `OperationGroup` envelopes.
- **Target Open-Source Tool:** **Hybrid `ProTools-PTSL + Binary AAF` MCP Server** (Combines direct binary `.aaf` manipulation via `pyaaf2` with live `PTSL` session commands so AI agents can construct full multi-track sessions, markers, and clip-gain structures).

### Bottleneck WG06-02: 100% Offline, NDA-Compliant Local SFX Semantic Search (`LAION-CLAP`) with Negative Prompts, Sub-Clip Windowing & `UCS` Metadata Writeback
- **Evidence Sources:** `r/gameaudio`, `r/AudioPost`.
- **The Manual Labor ("Amelelik"):**
  Cloud AI tools are banned by studio NDAs, and raw local `LAION-CLAP` scripts fail on long field recordings (where a 2-second transient gets washed out by global averaging), fail on negative queries (*"metal impact WITHOUT reverb"*), and don't write Universal Category System (`UCS`) tags back into BWF `bext`/`iXML` headers.
- **Target Open-Source Tool:** **Offline Transient-Windowed `CLAP` SFX Search & Non-Destructive `UCS` BWF Header Tagger**.

### Bottleneck WG06-03: Offline Field-Recorder PolyWAV Script Aligner (`WhisperX` + `iXML` Boom/Lav Auto-Assembler)
- **Evidence Sources:** `r/AudioPost`, `github.com/m-bain/whisperX`.
- **The Manual Labor ("Amelelik"):**
  Existing Whisper tools only turn stereo camera scratch audio into `.srt` subtitles; they cannot read 12-channel production PolyWAV `iXML` chunks, align paraphrased actor takes against a shooting script, and assemble isolated character Lav and Boom channels onto a DAW timeline.
- **Target Open-Source Tool:** **Offline `WhisperX` + `iXML` Multi-Track Dialogue Script Assembler**.

### Bottleneck WG06-04: Bridging Heavy Offline Neural Separation (`HT-Demucs ONNX`) into Non-Destructive DAW/Wwise Sub-Track Workflows
- **Evidence Sources:** `r/audioprogramming`, `sevagh/demucs.onnx`.
- **The Manual Labor ("Amelelik"):**
  Transformer/STFT models like `HT-Demucs` cannot run inside 5ms real-time audio callbacks without buffer underruns, forcing engineers to manually export clips, run command-line separation, and re-import stems.
- **Target Open-Source Tool:** **One-Click Background GPU `Demucs-ONNX` De-Bleed & Phase-Coherent DAW/Wwise Sub-Track Spawner**.

---

## 7. WG-07 // STUDIO FIELD QA, DELIVERABLES QC, CONFORM TORTURE & BENCHMARKS

### Bottleneck WG07-01: Open-Source Cross-NLE `.aaf / .edl / .xml` Conform Torture Test Suite & Pre-Flight Validator
- **Evidence Sources:** `r/AudioPost`, `r/editors`.
- **The Manual Labor ("Amelelik"):**
  Every NLE exports edge-case quirks (Turkish/UTF-8 characters, mixed `23.976` vs `24.000` pull-down, `29.97 DF` vs `NDF`, unrendered speed ramps, MP4 AAC fractional frame offsets) that crash DAW/color imports.
- **Target Open-Source Tool:** **Public Cross-NLE Conform Torture Corpus & Automated Pre-Flight Timeline Sanitizer**.

### Bottleneck WG07-02: Dolby Atmos `ADM BWF` (`axml`) Structural Metadata, 24fps Timecode & Downmix True-Peak Pre-QC Scanner
- **Evidence Sources:** `r/AudioPost`, `r/DolbyAtmosMixing`.
- **The Manual Labor ("Amelelik"):**
  Multi-GB Dolby Atmos `ADM BWF` masters get rejected by Netflix/Apple/Amazon QC due to wrong `axml` frame-rate flags (25/30fps instead of 24fps), sample-count mismatch against the Stereo fallback WAV, or True Peak (`> -1.0 dBTP`) excursions occurring specifically during the 5.1/Binaural downmix fold-down.
- **Target Open-Source Tool:** **Instant Header-Level `ADM BWF` (`axml / chna`) & Downmix True-Peak Pre-QC Validator**.

### Bottleneck WG07-03: Automated Plugin (`VST3 / CLAP / AU`) Real-Time Allocation (`malloc`), Xrun & Acoustic PDC Latency Drift Verifier
- **Evidence Sources:** `github.com/Tracktion/pluginval`, `free-audio/clap-validator`.
- **The Manual Labor ("Amelelik"):**
  `pluginval` only checks `rtcheck` on macOS and does not measure whether a plugin's actual acoustic impulse delay matches its host-reported PDC latency when parameters change dynamically, nor does it handle headless Linux/Windows GUI context crashes cleanly out of the box.
- **Target Open-Source Tool:** **Cross-Platform Real-Time Allocation Interceptor & Impulse-Response PDC Drift Verifier**.
