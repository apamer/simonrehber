# Simon Says | Seans Rehberim

Simon Says Uygulayıcı Kılavuzu'nu kullanan uygulayıcılar için seans yardım portalı (APAMER Psikoloji Yayınları). Basılı kılavuzun yanında kullanılır; kılavuzun yerini tutmaz.

Her oturum üç bölümden oluşur: Seansa hazırlan, Seansı uygula, Seansı tamamla.

- `index.html`: portalın arayüzü (ana ekran, 20 oturum, seans planı çıktısı)
- `oturumlar/`: her oturumun içeriği (`oturum-01.json` … `oturum-20.json`); alanlar `oturumlar/README.md`'de
- `robots.txt`: arama motorlarının siteyi listelemesini engeller

Durum: 20 oturum kılavuzun son hâline göre hazır.

Yayın: Cloudflare Pages (`simonrehber.pages.dev`). `main` dalı canlı siteyi, diğer dallar önizlemeyi besler. Site bir web sunucusu üzerinden açılmalıdır (`file://` ile çalışmaz). Form PDF'leri depoya konmaz.
