## Özet

<!-- Bu PR hangi public dokümantasyonu değiştiriyor ve neden? -->

## Hedef kitle ve yayın kararı

<!-- Anonim hedef kitleyi ve bu değişikliğin somut public faydasını yazın. Ekip içi bir amaç public fayda değildir. -->

- Anonim hedef kitle:
- Somut public fayda:

- [ ] İçerik yalnız anonim ziyaretçi, müşteri veya dış entegrasyon geliştiricisi içindir.
- [ ] Ekip konuşması/notu, ajan çıktısı, görev/issue planı, spike/araştırma, iç karar veya operasyon ayrıntısı yoktur.
- [ ] Provider onboarding, private sandbox, ticari koşul, yayınlanmamış provider sırası/roadmap/capability yoktur.
- [ ] Private repo/issue/PR, local dosya yolu veya access-controlled kanıt bağlantısı yoktur.
- [ ] Şüpheli içerik bu repo ve Git geçmişi dışında tutulmuştur; hidden/orphan draft yoktur.

## Public güvenlik kontrolü

- [ ] İçerik `PUBLIC` sınıflandırmasına uygundur.
- [ ] Gerçek müşteri verisi, VKN/TCKN, kişi bilgisi, belge, XML/PDF veya production ekran görüntüsü yoktur.
- [ ] Secret, credential, token, private endpoint, internal hostname veya güvenlik runbook'u yoktur.
- [ ] NDA veya private sağlayıcı içeriği yoktur.
- [ ] Örnekler sentetiktir ve açıkça örnek olarak işaretlenmiştir.
- [ ] FaturaDev özel entegratör veya doğrudan GİB bağlantısı varmış gibi anlatılmamıştır.
- [ ] Yalnız yayımlanmış capability ve müşteri sözleşmeleri mevcut özellik olarak anlatılmıştır.
- [ ] Değişiklik kilitli Tahsil tasarımından yeni component, CSS, renk, tema veya layout türetmemiştir.

## Kaynaklar ve güncellik

<!-- Mevzuat veya sağlayıcı iddiası varsa resmî birincil kaynakları ve doğrulama tarihini ekleyin. -->

- Resmî kaynaklar:
- Son doğrulama tarihi:

## Yerel doğrulama

- [ ] `mint validate`
- [ ] `mint broken-links --check-anchors --check-redirects`
- [ ] `mint a11y`
- [ ] Yeni veya değişen her sayfa `docs.json` navigasyonundadır.
- [ ] Marka varlığı değiştiyse manifest, sürüm ve hash onayı eklenmiştir; aksi halde kilitli asset byte'ları değişmemiştir.
