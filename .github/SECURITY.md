# Güvenlik politikası

## Kapsam

Bu politika, `FaturaDev/docs` reposu ile [fatura.dev](https://fatura.dev)
public dokümantasyon yüzeyinde bulunan güvenlik sorunlarını kapsar. Güvenlik
düzeltmeleri yalnız reponun güncel varsayılan branch'i için değerlendirilir.

## Güvenlik açığı bildirme

Bir güvenlik sorununu public issue, discussion veya pull request içinde
paylaşmayın. [GitHub Private Vulnerability
Reporting](https://github.com/FaturaDev/docs/security/advisories/new) üzerinden
özel bir bildirim oluşturun.

Bildirimde mümkünse aşağıdaki public-safe bilgileri paylaşın:

- etkilenen public URL veya repo dosyası,
- güvenlik etkisinin kısa açıklaması,
- sentetik veriyle hazırlanmış yeniden üretim adımları,
- önerilen düzeltme veya azaltma yaklaşımı.

Gerçek müşteri belgesi, VKN/TCKN, kişisel veri, parola, token, API anahtarı,
sertifika, cookie, authorization header, private endpoint veya erişim kontrollü
sağlayıcı içeriği eklemeyin. Bir secret'ın açığa çıktığından şüpheleniyorsanız
değerin kendisini bildirim metnine kopyalamayın.

Bildirim, repo sahipleri tarafından kapsam ve etki açısından değerlendirilir.
Geçerli bir sorun doğrulandığında düzeltme ve açıklama, gereksiz güvenlik
ayrıntıları public alana taşınmadan koordine edilir.
