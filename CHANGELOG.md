# Sürüm notları

İndirme: [Sürümler](https://github.com/0xxnr/GameTranslator/releases)

## 1.7.0 — Sesli dublaj, tema arka planları, mikrofon çevirisi ve çok dilli arayüz
- **Sesli dublaj:** çeviriler canlı olarak sesli okunur; altyazılar, altyazısız NPC konuşmaları, ek bölgeler ve mikrofon çevirisi ayrı ayrı açılabilir. Ana penceredeki **Sesli dublaj** anahtarıyla açılır, ayarları Ayarlar › Sesli dublaj'da.
- Ses seçenekleri: ücretsiz ve internetsiz **macOS sesleri** (Gelişmiş ve Premium sesler dahil) ya da daha doğal bulut sesleri: **ElevenLabs**, **OpenAI uyumlu** servisler (kendi TTS sunucun da olur) ve **Azure Speech**. Hız, ses düzeyi, yeni cümlede öncekini kesme ve bulut sesi çalışmazsa macOS sesine geçme ayarlanabilir.
- Dublaj oyunun orijinal sesinin üstüne gelir; en iyi sonuç için oyunun diyalog sesini kısıp altyazıları açık tut.
- **Çok dilli arayüz:** uygulama Mac'in sistem dilinde açılır: Türkçe, English, Deutsch, Français, Español, Italiano, Português (Brasil), Русский, 日本語, 한국어 ve 简体中文. Desteklenmeyen dillerde İngilizce açılır. İlk kurulumda çeviri dili de sistem diline göre seçilir.
- **Temalar:** isim plakası tarzında çizimli arka planlar: **Palmiye gün batımı**, **Neon şehir**, **Gece sahili** ve **Retro ızgara**. Sağ kenarda çizim, neon parlayan yazı ve parıldayan çerçeve; altyazıda, her ek bölgede ve ses balonunda seçilebilir (Oyun Profili › Arka plan… › Temalar). Ekranda ve OBS'te aynı görünür.
- **Mikrofon çevirisi:** mikrofonunu seçip konuştuklarını istediğin dile çevirebilirsin (ör. yayında Türkçe konuşurken izleyiciler İngilizcesini görür). Ana penceredeki **Mikrofon çevirisi** anahtarıyla açılır; mikrofon, konuştuğun dil ve çeviri dili Ayarlar › Mikrofon çevirisi'nden seçilir.
- Mikrofon çevirisi OBS'te kendi adresinde: `/mikrofon`; balonun görünümü ayrıca seçilir. Oyun çevirisi başlatılmamış olsa da çalışır.
- Ayarlar › Mikrofon çevirisi'ndeki balon konuştukça canlı değişir: konuşurken tanınan yazı, ardından çevirisi görünür.
- **Genel arka plan:** Ayarlar › Görünüm › **Hazır arka plan** ile hazır geçişler ve temalar tüm bölgelere varsayılan olarak verilebilir; Ayarlar › OBS / Yayın › **Kutu rengi**'nde de aynı seçenekler var.

## 1.6.0 — Her bölgeye ayrı OBS adresi, yazı tipi ve arka plan
- **Her bölge OBS'te ayrı kaynak:** altyazı, her ek bölge ve ses çevirisinin kendi adresi var: `/altyazi`, `/bolge-1` … `/bolge-4`, `/ses`. Her birini OBS'te ayrı bir Tarayıcı kaynağı olarak ekleyip istediğin yere koyabilirsin.
- **Adresler iki yerde:** Ayarlar › OBS / Yayın › **Yazıları OBS'te ayrı yerlere koy** altında ve Oyun Profili'nde bölge seçilince; her birinin yanında **Kopyala** düğmesi.
- **Her bölgeye ayrı yazı tipi:** altyazı, ek bölgeler ve ses çevirisi için ayrı yazı tipi ve kalınlık; ekranda ve OBS'te aynı anda geçerli. "Genel" seçiliyken Ayarlar'daki yazı tipi kullanılır.
- **Her bölgeye ayrı arka plan:** Oyun Profili'nde **Arka plan…** düğmesi örnek yazılı bir panel açar. Düz seçenekler (Siyah, Beyaz, Şeffaf, istediğin renk ve saydamlık) ya da hazır geçişler seçilip kaydedilir; ekranda ve OBS'te birlikte geçerli.
- **Hazır geçişli arka planlar:** **Mor cam**, **Neon gün batımı**, **Okyanus** ve **Gece neonu**; altyazıda, her ek bölgede ve ses balonunda kullanılabilir.
- Ek bölge sayısı 4'e çıktı.
- Eski `?only=subtitle|speech|zone` OBS adresleri çalışmaya devam eder.

## 1.5.1 — Sadeleştirme
- Uygulamadaki oyun ve şirket adları kaldırıldı; dil dosyası türleri yalnızca uzantılarıyla gösteriliyor.
- `.yml` dil dosyası desteği kaldırıldı.
- Uygulama içindeki rehber bağlantıları kaldırıldı.
- Ana penceredeki geliştirici bağlantısı kaldırıldı; Ayarlar › Hakkında'da duruyor.

## 1.5.0 — Oyun dil paketleri
- **İnternetsiz çeviri:** oyun profiline bir dil paketi ("orijinal metin → çeviri" listesi) bağla; o oyunda okunan yazı önce pakette aranır, internet olmadan ve anında çevrilir.
- **Akıllı eşleşme:** küçük okuma hataları, eksik noktalama ve baştaki konuşmacı adı tolere edilir; emin olunamayan yazılar çeviri motoruna bırakılır.
- **Ne zaman kullanılsın:** "Önce dil paketi, bulamazsa çeviri motoru" ya da "Yalnızca internet yokken".
- **Paket oluştur:** oyunun orijinal ve Türkçe dil dosyalarından (.locres, .gxt2, .strings, XML, JSON, CSV, PO) ya da çok dilli tablodan otomatik oluşturulur; biçim kodları temizlenir.
- **Elle hazırla ve paylaş:** CSV / TSV, TXT, JSON ve PO desteklenir; paketler dışa aktarılıp paylaşılabilir.

## 1.4.0 — Yazı tipi seçimi
- **Ayarlar › Görünüm › Yazı tipi:** çeviri yazısının yazı tipi artık seçilebiliyor. Hazır seçenekler: Sistem (SF Pro), Yuvarlak, Serif ve Eş aralıklı.
- **Bilgisayardaki yazı tipleri:** Mac'inde yüklü tüm yazı tipleri aranabilir bir listede, her biri kendi görünümüyle; tek tıkla seç.
- **Kendi yazı tipini ekle:** .ttf ya da .otf dosyası ekleyip kullanabilirsin. Dosya yalnızca uygulamaya eklenir, sisteme kurulmaz; istediğin zaman kaldırabilirsin.
- **Kalınlık:** Normal, Orta, Yarı kalın, Kalın, Çok kalın.
- Seçilen yazı tipi ekrandaki çeviride, ek bölgelerde, sesli konuşma balonunda ve **OBS yayınında** aynı anda kullanılır; değişiklik anında yansır.
- **OBS:** eklediğin yazı tipi dosyasını uygulama yayın sayfasına kendisi sunar; OBS'te ve iki bilgisayarlı yayında da aynı yazı tipi görünür. Kaynak başına farklı yazı tipi için adrese `?font=Arial&weight=800` eklenebilir.

## 1.3.2 — Güncelleme denetimi düzeltmesi
- "GitHub geçici olarak sınırladı" hatası giderildi: GitHub'ın saatlik sorgu sınırına takılınca güncelleme denetimi sınırsız yedek yoldan devam ediyor.

## 1.3.1 — Yeni indirme adresi
- bug fix

## 1.3.0 — Yazı arka planı seçenekleri
- **Ayarlar › Görünüm › Yazı arka planı:** çeviri yazısının arkasındaki kutu artık **Siyah**, **Beyaz**, **Şeffaf** ya da istediğin bir **Renk** olabilir.
- **Saydamlık** kaydırıcısıyla kutuyu koyulaştırıp açabilirsin; değişiklik ekrandaki çeviriye anında yansır.
- Yazı rengi kutuya göre kendiliğinden beyaz ya da siyah olur. Kutu şeffaf ya da çok saydamken yazı, her zeminde okunsun diye ince siyah kenar çizgisi alır.
- Ayarlarda canlı önizleme.
- **OBS'te de renkli kutu:** Ayarlar › OBS / Yayın › Arka plan › **Kutu** seçiliyken kutu rengi Siyah, Beyaz, Renk ya da **Ekrandakiyle aynı** olabilir; saydamlık ayrı ayarlanır. Değişiklik yayına anında düşer, OBS'te bir şey yapmak gerekmez.
- OBS adres parametresi: `?box=ff3366&alpha=0.7` ile kaynak başına kutu rengi verilebilir (ör. altyazı kırmızı, bildirimler siyah).

## 1.2.0 — Uygulama içi güncellemeler
- **Uygulama içinden güncelleme:** Ayarlar › Güncellemeler'den üç seçenek: yalnızca elle denetle, otomatik denetle ve haber ver (varsayılan), otomatik indir ve kur.
- Yeni sürüm bulununca sürüm notlarıyla birlikte bir pencere açılır: **İndir ve kur**, **Sonra** ya da **Bu sürümü atla**.
- Otomatik modda güncelleme arka planda indirilir ve uygulamayı kapattığında kurulur; ana penceredeki şeritten hemen yeniden başlatabilirsin.
- Güncellemeler dijital imzayla (Ed25519) doğrulanır; imzası, paket kimliği ya da sürümü tutmayan dosya kurulmaz. Kurulum başarısız olursa eski sürüm geri konur.
- Uygulama menüsünde **Güncellemeleri Denetle…**

## 1.1.0 — OBS yayın desteği
- **OBS Tarayıcı kaynağı:** Uygulama yerel bir adres açar (varsayılan `http://127.0.0.1:8765/`). OBS'e bu adresle Tarayıcı
  kaynağı eklenince çeviriler yayına şeffaf arka planla canlı düşer. Oyunu Pencere Yakalama ile aldığında da çalışır.
- Yazı boyutu, konum (alt / orta / üst), arka plan (siyah kutu / kenar çizgisi / yok), orijinal metin, ses çevirisi ve ek
  bölgeler uygulamadan **canlı** ayarlanır; OBS'te adresi yeniden girmek gerekmez.
- Ses çevirisi yayında da ayrı (mor) görünümde; ek bölgeler biraz daha küçük yazıyla.
- **⌃⌥Y:** çevirileri yalnızca yayında gizle/göster (Mac ekranındaki yazılardan bağımsız).
- "Test metni gönder": çeviri çalışmıyorken de OBS'te konum ve boyutu ayarlamak için 6 sn örnek metin.
- "Tarayıcıda önizle": sayfayı örnek metinlerle tarayıcıda açar.
- İsteğe bağlı **metin dosyası** çıktısı (OBS Metin kaynağı › Dosyadan oku).
- İsteğe bağlı ağ erişimi: ikinci bir yayın bilgisayarındaki OBS de bağlanabilir. Varsayılan kapalı, yalnızca bu Mac.
- Başlıkta OBS durum rozeti; "Çeviri" menüsünde OBS seçenekleri.
- Tanılama: Ayarlar'da bağlı yayın sayfası sayısı ve son gönderilen çeviri saati; "Bağlantıyı tarayıcıda test et" (`?debug=1`).
- Yayın sayfası canlı akış (SSE) kurulamazsa kendiliğinden yarım saniyede bir sorgulamaya geçer.
- **Ayrı kaynaklar:** altyazı (`?only=subtitle`), ses çevirisi (`?only=speech`) ve bildirimler (`?only=zone`) OBS'te ayrı Tarayıcı kaynakları olarak eklenip ayrı yerlere konabilir. Ayarlar'da her biri için kopyalanabilir adres var.
- Düzeltme: ses çevirisi kalkıp kısa süre içinde yenisi geldiğinde yeni satırın yayında takılı kalması giderildi.
- Sunucu yalnızca geri döngü arayüzüne bağlanır (daha uyumlu yöntem); yanıtlar tamamen gönderildikten sonra kapanır.
