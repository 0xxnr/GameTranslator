# Güvenlik

## Güvenlik açığı bildirme
Bir güvenlik açığı bulduysan lütfen herkese açık bir Issue **açma**. Bunun yerine bu deponun
**Security › [Report a vulnerability](https://github.com/0xxnr/GameTranslator/security/advisories/new)** bölümünden gizli olarak bildir.
Açığın ne olduğunu, nasıl tekrarlanacağını ve etkilenen sürümü yaz. En kısa sürede dönüş yapılır.

## Desteklenen sürümler
Güvenlik düzeltmeleri yalnızca **en son sürüme** gelir. Ayarlar › Güncellemeler'den güncel olduğundan emin ol.

## Güncellemeler nasıl korunuyor
- Her sürüm zip'i, uygulamanın içine gömülü genel anahtarla eşleşen **Ed25519** imzasıyla yayınlanır (`.sig` dosyası).
- Uygulama güncellemeyi kurmadan önce imzayı, paket kimliğini (`com.gametranslator.app`), sürüm numarasını ve `codesign`
  bütünlüğünü denetler. Biri tutmazsa kurulmaz; kurulum yarıda kalırsa eski sürüm geri konur.
- Uygulamayı yalnızca bu sayfadan indir. Başka sitelerdeki kopyalar resmî değildir.

## Uygulamanın kullandığı izinler
| İzin | Neden |
|---|---|
| Ekran ve Sistem Ses Kaydı | Seçtiğin oyun penceresindeki yazıyı okumak ve sesli konuşmayı dinlemek |
| Konuşma Tanıma | Altyazısız konuşmaları metne çevirmek (cihazda) |
| Yerel Ağ (isteğe bağlı) | OBS tarayıcı kaynağı ve yerel çeviri sunucuları |

Ekran görüntüsü ve ses kaydedilmez, hiçbir yere gönderilmez.
