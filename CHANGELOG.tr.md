<div align="right">

🇬🇧 [English](CHANGELOG.md)

</div>

# Değişiklik Günlüğü

ArgilCAD'deki tüm önemli değişiklikler bu dosyada belgelenir.

Biçim [Keep a Changelog](https://keepachangelog.com/tr/1.1.0/) temel alınarak
hazırlanmıştır ve bu proje [Anlamsal Sürümleme](https://semver.org/lang/tr/)
kurallarına uyar.

## [1.0.2] - 2026-08-13

Kararlılık sürümü: ArgilCAD artık daha önce çöktüğü veya hiç açılmadığı
kurulumlarda çalışıyor ve 3B kamera yeniden öngörülebilir davranıyor.

### Eklendi

- Modelin üzerinde herhangi bir yere çift tıklayarak görünümü o noktaya
  merkezleyin — döndürme merkezini çalıştığınız yere taşımanın en hızlı yolu.
- 3B görüntüleyici bir bilgisayarda çalışamıyorsa ArgilCAD artık boş bir panel
  bırakmak yerine nedenini açıklıyor, ne yapmanız gerektiğini söylüyor ve destek
  için **Tanılamayı kopyala** düğmesi sunuyor. Uygulamanın geri kalanı çalışmaya
  devam ediyor.

### Düzeltildi

- **Eski ekran kartı sürücüsü olan bilgisayarlarda, sanal makinelerde ve Uzak
  Masaüstü üzerinden uygulama artık çökmüyor.**
- Tüm kullanıcılar için ya da korumalı bir klasöre kurulduğunda uygulamanın
  açılmaması giderildi. Ayarlar ve projeler artık standart kullanıcı klasöründe
  tutuluyor; önceki sürümden kalanlar oraya otomatik taşınıyor, veri kaybı yok.
- Aynı bilgisayarda birden fazla kullanıcı oturumu açıkken her hesap artık kendi
  modelleriyle çalışıyor.
- Windows'ta ilk açılış daha hızlı ve güvenilir: yeni kurulumda "motora
  ulaşılamadı" uyarısının çıkıp **Yeniden dene** ile düzelmesi sorunu giderildi.
- macOS'ta Belgeler klasörü izin sorması nedeniyle uygulamanın başlayamaması
  giderildi.
- **Görünümü sıfırla** artık parçanın tamamını, boyutu ne olursa olsun çerçeveye
  oturtuyor.
- Üst veya alt görünüme geçtikten sonra modelin eğik kalıp düzeltilememesi
  giderildi.
- Yakınlaştırma artık parçanızın boyutunu izliyor: büyük bir levhadaki küçük bir
  detaya yaklaşabiliyor, büyük bir parçada uzaklaşınca kırpılma yaşamıyorsunuz.
- Tekerlek imlecin altındaki noktaya doğru yakınlaştırıyor; kaydırma sonucu
  parçadan uzaklaşan görünüm kendini toparlıyor.
- Görüntüleyici kontrol ipuçları artık satır satır; dar pencerede eksen
  göstergesiyle üst üste binmiyor.
- macOS'ta derlenmiş bileşen içeren bir paket kurulamadığında artık sessizce
  başarısız olmak yerine net bir mesaj gösteriliyor.

## [1.0.1] - 2026-08-07

Doğrudan modelleme ArgilCAD'e geliyor: modeli fareyle şekillendirin, arkasındaki
Python kodunun tamamı sizde kalsın.

> ⚠️ Bu zorunlu bir güncellemeydi — eski sürümler artık model üretemiyor.

### Eklendi

- **Doğrudan modelleme araçları** — fareyle çalışan işlemler için yeni bir
  **Model** menüsü: kavis (fillet), pah (chamfer), it/çek (push/pull), delik,
  kabuk (shell), eğim (draft), taşı, döndür, aynala ve doğrusal / dairesel
  çoğaltma. Bunlar ayrı bir mod değil: her araç betiğinize gerçek
  [Build123d](https://build123d.readthedocs.io) kodu yazar; kodu yeniden
  düzenlenebilir tutan işaretlerin arasına. `.py` dosyasını dışa aktarın,
  çalışmaya devam eder.
- **Eskiz → katılaştırma / döndürme** — modelin herhangi bir yüzeyine çizin
  (yakalama destekli dikdörtgen, çember, çokgen ve yollar), sonra profili katıya
  dönüştürün veya bir eksen etrafında döndürün.
- **Bir değeri girmenin üç yolu** — seçtiğiniz geometrinin üzerinde duran ok
  tutamacını sürükleyin, panel kaydırıcısını kullanın veya değeri yazın. Üçü de
  onaylamadan önce sonucun canlı önizlemesini gösterir.
- **Dışa aktarma** — modelinizi doğrudan görüntüleyiciden STL, STEP veya GLB
  olarak kaydedin.
- Uygulama genelinde **klavye kısayolları**; tam liste
  **Yardım → Klavye Kısayolları** altında.
- Kod editörü için araç çubuğu.

### Değişti

- Model üretimi daha hızlı — CAD motoru artık her derlemede sıfırdan başlamak
  yerine arka planda hazır bekletiliyor.
- Derleme başarısız olduğunda daha anlaşılır, Türkçe hata mesajları.
- İnternet bağlantısı koptuğunda uygulama sizi uyarıyor.
- Model tuvali arayüz iyileştirmeleri.

### Düzeltildi

- 3B görüntüleyici ilk açılışta boş kalmıyor.
- Metin alanlarına yazma yeniden çalışıyor.
- Eskiz yakalama noktaları çokgen ve yollarda kaymıyor.
- Üst yüzeydeki bir eskizle kesme çalışıyor.
- Kod editörü terminal hatası giderildi.
- STL dosyaları modelin parametrelerine göre adlandırılıyor.

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
