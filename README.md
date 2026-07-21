# FaturaDev dokümantasyonu

Bu repo, [fatura.dev](https://fatura.dev) sitesinin public Mintlify kaynağını
içerir.

Repodaki her dosya, commit mesajı ve pull request anonim ziyaretçilere açık
kabul edilir. Kimlik doğrulaması olmadan yayımlanmaya uygun olmayan hiçbir
bilgi; taslak, göz ardı edilen dosya veya bağlantısız sayfa olarak dahi bu
repoya eklenmemelidir.

FaturaDev, çok sağlayıcılı bir e-Belge API ve orkestrasyon platformudur. Yazılım
ekiplerine, müşterinin yetkilendirdiği özel entegratör bağlantıları için ortak
bir entegrasyon yüzeyi sunar. FaturaDev özel entegratör değildir; GİB'e doğrudan
bağlanmaz ve mali mühür, e-imza, XAdES veya GİB'e belge iletimi görevlerini
üstlenmez.

## Yayımlanan kapsam

Bu repo aşağıdaki public içeriklerin kaynağıdır:

- ürün konumlandırması ve kullanım senaryoları,
- entegrasyon kavramları ve kullanım rehberleri,
- resmî kaynaklarla desteklenen e-Belge rehberleri,
- kilitli FaturaDev marka varlıkları.

API referansı yalnız kanonik OpenAPI sözleşmesi public olarak yayımlandıktan
sonra bu kapsama eklenebilir. İç mimari, erişim bilgileri, gerçek müşteri
belgeleri, kişisel veriler, sağlayıcı NDA içeriği, private endpoint'ler, ekip
notları ve operasyon runbook'ları bu repoda yer alamaz.

İçerik değiştirmeden önce [public yayın politikasını](./AGENTS.md), [katkı
adımlarını](#katkı-ve-yayın) ve [güvenlik
politikasını](./.github/SECURITY.md) okuyun.

## Kilitli dokümantasyon sunumu

Public sunum, [`muhasip/tahsil`](https://github.com/muhasip/tahsil) reposunun
`a86e7650bc0a5a24fbf384679ab60db853d0dd5f` commit'indeki Mintlify tasarımını
izler. FaturaDev yalnız kilitli marka varlıklarını, public ürün metinlerini,
navigasyonu ve alan adına özgü bağlantıları kullanır. Bağımsız tema, bileşen,
CSS kuralı veya görsel dil eklenmez.

Public landing ve bilgi mimarisi,
[`twentyhq/twenty/packages/twenty-docs`](https://github.com/twentyhq/twenty/tree/c503d4c4aaa29c978d8c190ad8232658e970d06c/packages/twenty-docs)
yapısının `c503d4c4aaa29c978d8c190ad8232658e970d06c` commit'indeki üç yüzeyli
içerik ritmini izler. Tahsil görsel kilidi sunum için belirleyici olmaya devam
eder.

## Yerel geliştirme

`docs.json` dosyasının bulunduğu dizinde sabitlenmiş Mintlify sürümüyle yerel
önizlemeyi başlatın:

```bash
npx -y mint@4.2.722 dev
```

Önizleme varsayılan olarak `http://localhost:3000` adresinde açılır.

## Doğrulama

İnceleme istemeden önce zorunlu dokümantasyon kontrollerini çalıştırın:

```bash
npx -y mint@4.2.722 validate
npx -y mint@4.2.722 broken-links --check-anchors --check-redirects
npx -y mint@4.2.722 a11y
```

Kilitli marka dosyalarını ayrıca doğrulayın:

```bash
shasum -a 256 \
  images/brand/fatura-type.svg \
  images/brand/fatura-icon.png \
  images/brand/brand-assets.json
```

Beklenen değerler `images/brand/brand-assets.json` dosyasında kayıtlıdır ve
public policy iş akışı tarafından denetlenir. [Marka varlıkları
sayfası](https://fatura.dev/project/brand-assets), yalnız dış kullanıcıların
indirme ve kullanım ihtiyaçlarını açıklar.

## Katkı ve yayın

1. Güncel `main` branch'inden başlayın.
2. `codex/123-kisa-aciklama` biçiminde issue-scoped bir branch oluşturun.
3. Yalnız public-safe değişiklikler yapın ve her yeni sayfayı `docs.json`
   navigasyonuna ekleyin.
4. Yerel doğrulama komutlarını çalıştırın.
5. Public güvenlik kontrol listesini tamamlayan bir pull request açın.
6. Gerekli insan ve code owner incelemelerini alın.
7. Korumalı branch akışı üzerinden birleştirin; `main` branch'ine doğrudan
   push yapmayın.

Güvenlik açığını public issue olarak paylaşmayın. Bu repo veya public
dokümantasyon sitesiyle ilgili güvenlik bildirimleri için [güvenlik
politikasındaki](./.github/SECURITY.md) özel bildirim kanalını kullanın.

## Marka varlıkları

Kanonik ve değiştirilemez marka dosyaları [`images/brand`](./images/brand)
dizinindedir. Dosya byte'larını değiştirmeyin; alternatif logo veya wordmark
üretmeyin. Hash ve kullanım kuralları için [Marka
varlıkları](https://fatura.dev/project/brand-assets) sayfasını inceleyin.
