# Farica Studio — GitHub Pages sitesi

Bu klasör, Farica Studio için hazırlanmış tek sayfalık, İngilizce, responsive statik web sitesidir.

## 0. Yerel önizleme

`index.html` dosyasına çift tıklayıp tarayıcıda açın. Harici JavaScript veya ücretli altyapı gerekmez.

## 1. GitHub üzerinde yayınlama

1. GitHub hesabınıza girin: https://github.com
2. **New repository** ile `farica-studio-site` adında **Public** bir depo oluşturun.
3. **Add file > Upload files** bölümünden bu klasördeki `index.html`, `favicon.svg`, `CNAME` dosyalarını depoya yükleyin ve Commit changes yapın. README dosyasını isterseniz ayrıca yükleyebilirsiniz.
4. Depoda **Settings > Pages > Build and deployment** bölümünü açın. Source: **Deploy from a branch**; Branch: **main**; Folder: **/(root)**; Save.
5. Aynı Pages ekranında **Custom domain** alanı `faricastudio.com` olmalı. Değilse girip Save deyin. GitHub DNS kontrolü yapabilir.

**Önemli:** GitHub Pages ücretsiz hesaplarda public repo ile çalışır. Yüklediğiniz site dosyaları herkese açık olur.

## 2. Wix DNS ayarları — yalnızca Pages yayınlandıktan sonra

GitHub ayarlarında `faricastudio.com` özel alan adını önce kaydedin. Ardından Wix'te `faricastudio.com` için **DNS kayıtlarını yönet** ekranına gidin.

Kök domain (`@`, Wix'te bazen boş sunucu adı / faricastudio.com) için eski Wix **A** kayıtlarını, yalnız web sitesini işaret eden **A** kayıtları olmak şartıyla, GitHub Pages'in dört A adresiyle değiştirin:

- 185.199.108.153
- 185.199.109.153
- 185.199.110.153
- 185.199.111.153

`www` CNAME kaydı için hedef `<GITHUB_KULLANICI_ADI>.github.io` olmalıdır. Wix'in mevcut `www` CNAME kaydı (`cdn3.wixdns.net` gibi) yalnızca kullanıcı adı öğrenilip GitHub'a geçildikten sonra düzenlenmelidir.

**ASLA değiştirmeyin:** `mx1.improvmx.com` ve `mx2.improvmx.com` MX kayıtları veya `v=spf1 include:spf.improvmx.com ~all` TXT kaydı. Bunlar çalışan e-posta yönlendirmesi için gerekli.

**Ön koşul:** Kök domainedeki diğer `A` / `AAAA` / `ALIAS` / `ANAME` kayıtlarının çakışmadığını denetleyin; ne oldukları anlaşılmadan silmeyin. Doğru `www` CNAME için gerçek GitHub kullanıcı adı gereklidir.

## 3. HTTPS ve doğrulama

DNS yayılımı zaman alabilir. GitHub > Repository > Settings > Pages bölümünde DNS durumu doğrulandıktan sonra **Enforce HTTPS** seçeneğini aktif edin. `https://faricastudio.com` ve `https://www.faricastudio.com` adreslerini ayrı ayrı test edin.

## 4. İletişim ve ürün linkleri

- E-posta: `fatih@faricastudio.com` (ImprovMX gelen e-posta yönlendirmesi)
- Lirelya: https://play.google.com/store/apps/details?id=com.farica.lirelya

E-posta yönlendirmesi, bu adresten Gmail aracılığıyla doğrudan gönderim (SMTP) yeteneği sağladığı anlamına gelmez. Yanıt göndermenin ayrıca kurulması gerekebilir.

## Site notları

- Tek sayfa, İngilizce; mobil ve masaüstü uyumlu.
- Üçüncü taraf analiz, izleme scripti, çerez, iletişim formu veya harici font kullanmaz.
- Görsel alan ürün ekran görüntüsü değil, açıkça 'Concept illustration' olarak etiketlenmiş özgün bir tasarımdır.
- Yapay zekâ destekli video üretim sistemi 'in development' olarak açıklanır; tamamlanmış ürün izlenimi verilmez.
