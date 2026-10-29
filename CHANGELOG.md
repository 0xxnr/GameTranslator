# Sürüm notları

İndirme: [Sürümler](https://github.com/0xxnr/GameTranslator/releases)

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
