<div align="right">

🇬🇧 [English](CHANGELOG.md)

</div>

# Değişiklik Günlüğü

ArgilCAD'deki tüm önemli değişiklikler bu dosyada belgelenir.

Biçim [Keep a Changelog](https://keepachangelog.com/tr/1.1.0/) temel alınarak
hazırlanmıştır ve bu proje [Anlamsal Sürümleme](https://semver.org/lang/tr/)
kurallarına uyar.

## [1.0.5] - 2026-09-14

ArgilCAD artık tarayıcıda da çalışıyor ve yapay zekâ ile üretim Starter ve Pro
planlarına geçiyor. Kendi bilgisayarınızda çalışan her şey — kod editörü,
modelleme araçları, örnekler, dışa aktarma ve teknik resim — hesap açmadan
ücretsiz kalıyor.

### Eklendi

- **Tarayıcıda ArgilCAD**:
  [argildesign.com/argilcad](https://argildesign.com/argilcad/) adresinde aynı
  uygulama; modeller kendi cihazınızda kurulur.
- **Proje yedekleri.** Giriş yaptığınızda projelerinizin kodu hesabınızda da
  saklanır ve tarayıcı dahil diğer cihazlarınızda açılır. Profil'den
  kapatabilirsiniz; bir projeyi silmek yedeğini de siler.
- **Prompt kutusunda örnekler.** Planınız yokken üç hazır örnek (düz dişli,
  vazo, elektronik kutusu) bilgisayarınızda ücretsiz kurulur; yanında kendi
  yapay zekânıza prompt yazıp kodu geri yapıştırma yolu var.
- **Üret, ihtiyacınız olana götürür.** Planınız yokken Üret'e basınca önce
  kayıt, sonra planlar açılır; prompt'unuz yerinde kalır. Plan etkinleşince
  üretim tek dokunuş uzaktadır.
- **Starter kredisi bitmeden haber**: ayın kredisinin %80'i ve tamamı
  harcandığında, Pro'ya yerinde yükseltme önerisiyle.
- **Katlanabilir prompt kutusu.** Boş kutuda Esc ya da Görünüm › Prompt kutusu
  ile küçük bir düğmeye iner; **P** ile geri gelir.

### Değiştirildi

- **Yapay zekâ ile üretim Starter ya da Pro planı gerektiriyor.** Ücretsiz aylık
  ve deneme kredileri sona erdi; elinizdeki krediler bitene kadar
  kullanılabilir.
- **Başlamak için hesap gerekmiyor.** Uygulama hesap açmadan başlar; plan almak
  ya da projelerinizi hesabınızda tutmak istediğinizde kaydolursunuz.
- **Kullanım analizi yalnızca izninizle.** İlk açılıştaki soruya cevap
  vermeden hiçbir şey gönderilmez; cevabınızı Ayarlar'dan değiştirebilirsiniz.
- CAD motorunun sürümleri sabitlendi; masaüstü uygulaması ve tarayıcı aynı
  modelleri üretir.
- Gizlilik Politikası ve Kullanım Koşulları güncellendi (yürürlük: 14 Eylül
  2026).

### Düzeltildi

- Değiştirilmemiş bir örneğe uygulanan ilk modelleme aracı artık `NameError`
  ile başarısız olmuyor.
- Geçmişten yeniden açılan bir modelin dışa aktarımı ve teknik resmi, gömülü
  motor yeniden başladıktan sonra da çalışıyor.
- Küçük ya da kısa pencerelerde üst çubuk, paneller ve pencereler artık
  kesilmiyor.

## [1.0.4] - 2026-08-29

Yalnızca düzeltme içeren, zorunlu bir sürüm: kurulu uygulamada model indirme,
modeli dosya ya da teknik resim olarak dışa aktarma ve model silme, geri kalan
her şey sapasağlam görünürken başarısız oluyordu.

### Düzeltildi

- **Kurulu uygulamada model indirme, teknik resim ve dosya dışa aktarma ile
  model silme başarısız oluyordu.** Bu istekler sabit bir bağlantı noktasına
  gidiyordu; oysa gömülü motor her açılışta başka bir bağlantı noktasında
  başlıyor, bu yüzden bağlantı reddediliyordu. Uygulama motoru yine de sağlıklı
  gösterip modelleri sorunsuz ürettiğinden, hata nedenini işaret etmek yerine
  rastgeleymiş gibi görünüyordu. Bağlantı noktasının hiç değişmediği geliştirme
  kurulumu bundan etkilenmiyordu.
- Motora giden bir istek başarısız olduğunda mesaj artık denenen adresi de
  yazıyor; salt bir bağlantı hatası bırakmıyor.

## [1.0.3] - 2026-08-29

Eskiz sürümü: konturunuzu çizgi, yay ve spline ile çizin, sonra dolu ya da içi
boş duvar olarak çıkarın. Yanında daha ucuz model üretimi ve gözle görülür
şekilde hızlanmış bir editör ve görüntüleyici.

### Eklendi

- **Yeni eskiz çizim araçları** — **Çizgi**, **Yay**, **Spline** ve **Ofset**;
  kontur artık yalnızca dikdörtgen ve dairelerden kurulmak zorunda değil.
- **Extrude için Duvar modu.** Eskiz artık yalnızca kontur ile ofseti arasındaki
  bandı bırakabiliyor, böylece çıkardığınız hacim içi boş oluyor. Duvar
  kalınlığını ve duvarın konturun içinde mi dışında mı kalacağını siz
  belirliyorsunuz.
- **Biten konturu yeniden çizmeden büyütüp küçültme.**
- Kod editörü, kodda hata varken ücretli yapay zekâ düzenlemesini artık
  başlatmıyor — aynı hatayla dönecek bir düzenlemeye kredi harcanmıyor.

### Değiştirildi

- **Model üretimi daha az kredi harcıyor.** Aynı proje üzerinde çalışırken
  istem mümkün olduğunca önbellekten kullanılıyor ve bu tasarruf doğrudan
  faturalanan krediye yansıyor.
- **Uygulama en yavaş olduğu yerlerde hızlandı.** Proje ve üretim geçmişi büyük
  projelerde beklemeden açılıyor, uzun dosyalarda kod editöründe yazarken
  takılma kalmadı, 3B görüntüleyici çalışırken çok daha az yeniden çiziliyor.

### Düzeltildi

- Keşfet bölümünden ve üretim panelinden model indirmenin başarısız olması
  giderildi.
- Modele uygulanan her özellikte bellek kullanımı artıyordu; her düzenleme artık
  yerini aldığı geometriyi serbest bırakıyor.
- Görünüm değiştirdikten sonra 3B görünümün bir bölümünün temizlenmeden kalmasına
  yol açan çizim hatası giderildi.
- Uzun süren bir işlem — örneğin paket kurulumu — sürerken motor artık yanıt
  vermeyi kesmiyor: model indirmeleri ve durum kontrolleri anında geçiyor.

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
