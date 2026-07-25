<div align="right">

🇬🇧 [English](CHANGELOG.md)

</div>

# Değişiklik Günlüğü

ArgilCAD'deki tüm önemli değişiklikler bu dosyada belgelenir.

Biçim [Keep a Changelog](https://keepachangelog.com/tr/1.1.0/) temel alınarak
hazırlanmıştır ve bu proje [Anlamsal Sürümleme](https://semver.org/lang/tr/)
kurallarına uyar.

## [1.0.0] - 2026-07-25

ArgilCAD'in ilk genel sürümü.

### Eklendi

- **Metinden CAD üretimi** — ihtiyacınız olan parçayı gündelik dille tarif edin,
  karşılığında bir mesh değil, gerçek bir parametrik 3B model alın.
- **Birden fazla yapay zekâ sağlayıcısı** — Anthropic, OpenAI, Google Gemini ve
  xAI modelleriyle üretim yapın. Model listesi yapılandırma tabanlıdır; yeni
  modeller uygulama güncellemesi beklemeden kullanıma açılabilir.
- **Dahili kod editörü** — her model gerçek [Build123d](https://build123d.readthedocs.io)
  Python kodudur. Üretilen kodu açın, dilediğiniz gibi düzenleyin ve yeniden
  çalıştırarak modeli güncelleyin — CAD çekirdeğinin tüm gücü sizde kalır.
- **Çoklu görüntüleme modları** — modelinizi köşeleri görünür gölgeli, köşesiz
  gölgeli, tel kafes (wireframe) veya X-ray görünümünde inceleyin.
- **Tek tuşla teknik çizim** — modelinizi tek bir düğmeyle teknik çizime
  dönüştürün, kredi harcamadan. *(Deneysel — çıktının gözden geçirilmesi
  gerekebilir.)*

### Platformlar

- Apple Silicon (M1 ve üzeri) işlemcili, macOS 11 veya üstü. Intel Mac'ler henüz
  desteklenmiyor; destek ilerleyen bir sürüm için planlanıyor.
- Windows 10 / 11 (64-bit).

<!--
Gelecek sürümler için şablon:

## [X.Y.Z] - YYYY-AA-GG

### Eklendi
- Yeni özellikler

### Değiştirildi
- Mevcut işlevlerdeki değişiklikler

### Düzeltildi
- Hata düzeltmeleri
-->
