# Simon Says | Seans Rehberim — çalışma notları

## Projenin amacı
Simon Says Uygulayıcı Kılavuzu'nu kullanan uygulayıcılar için seans yardım portalı (APAMER Psikoloji Yayınları).
Portal basılı kılavuzun **yanında** kullanılır; kılavuzun yerini tutmaz.

- Kılavuz metnini kopyalamaz. Kısa, eyleme dönük maddeler verir ve ayrıntı için kılavuz sayfasına ya da R- referansına yönlendirir.
- 20 oturum, beş grupta: Giriş (1–2), Çalışma Kitabı 1 (3–7), ÇK2 (8–11), ÇK3 (12–16), ÇK4 (17–20). Her grubun kendi kitap rengi, her oturumun kendi ikonu var.
- Her oturumun üç bölümü var: **Seansa hazırlan / Seansı uygula / Seansı tamamla**. N. oturumun "tamamla" bölümüne kaydedilen notlar N+1. oturumun "hazırlan" bölümünde görünür.
- Veriler yalnızca tarayıcıda (localStorage, `ssr:` önekiyle) saklanır. Sunucu, hesap ya da veri gönderimi yok.

## Dosya yapısı
- `index.html`: portalın arayüzü (CSS, JS, gömülü logo ve görseller, oturum adları `SESS`, oturum ikonları `SICON`).
- `oturumlar/oturum-01.json` … `oturum-20.json`: her oturumun içeriği. Alanların anlamı `oturumlar/README.md`'de. Sayfa açılırken 20 dosya birlikte yüklenir; bu yüzden site bir web sunucusu üzerinden açılmalıdır (`file://` ile çalışmaz).
- `simon-beyin.png` (şu an kullanılmıyor), `robots.txt` (arama motorlarını engeller), `README.md`.
- Geçmiş: 21 Ekim 2026'da `main`'de lacivert pilot `index.html`'in yerine geçmişti; 20 oturumluk sürüm `28700b4` commit'inden geri getirildi. Pilot bir süre `v2/` klasöründe tutuldu, sonra kaldırıldı (kullanıcı kararı; git geçmişinde duruyor). Seans modu ve "plandan sapmalar" özellikleri de bilinçli olarak eklenmedi.
- Görünümü değiştirmemesi gereken işlerde öncesi/sonrası karşılaştırması yapılır: aynı örnek işaret ve notlarla bütün ekranlar (ana ekran ve 20 oturumun 3 bölümü) oluşturulup HTML çıktısı karşılaştırılır.

## Terim kuralları
- **Koç** (Rehber değil), **Uygulayıcı** (Terapist değil), **çocuk** (Danışan değil).
- Beceri adları: Çalışma Belleği, Tepki Engelleme, Bilişsel Esneklik, Sonuç Odaklı Düşünme (Planlama).
  Kısa adlar: Hatırlama, Durdurma, Değiştirme, Planlama. "Fren" dili kullanılmaz.
- "Ödev" değil **ev çalışması**; "yoldan çıkmak" değil **rotadan çıkmak**.
- Sabit adlar: **Bravo, Başardın!**, **Aferin biletleri**, **Beceri Kontrol Kartları**.
- Kesin, abartılı ya da tanı/etiket dili kullanılmaz.

## Portalın yeri (kullanıcı açıklaması)
Uygulayıcıyı hazırlayan asıl araçlar: ayrıntılı basılı kılavuz, iki günlük yüz yüze eğitim ve öyküleştirilmiş seans simülasyon rehberi. Portal bunların yanında **ek destek**tir: uygulayıcı bir yerde takılırsa açıp bakar. Eksiksiz olması gerekmez; amacı anlaşılırlığı güçlendirmek ve karmaşık görünen süreci basit göstermektir. Bu yüzden her oturumda bir satırlık "oturumun fikri" ve her adımda bir satırlık "amaç" (kılavuzdaki "Neden:" kutusunun özü) maddelerden daha önemlidir.

## Yazım ölçüsü: kısa spot bilgi (kullanıcı kararı)
Uygulayıcı seans sırasında uzun liste okuyamaz. Portal kılavuzu anlatmaz; ne yapılacağını, neyin kullanılacağını ve ayrıntının hangi sayfada olduğunu söyler. Karmaşık görünen süreci basit göstermek amaçtır.
- Oturum başında `fikir`: oturumun özü tek cümle (kılavuzdaki "Oturumun fikri").
- "Seansı uygula": kılavuzdaki her **adım için tek kart**; kartta süre, materyal, Koç durumu ve kılavuz sayfası; `neden`: adımın amacı tek kısa cümle; **en fazla 3 kısa madde** (yalnızca kaçırılmaması gerekenler: kilit soru, not edilecek şey, verilecek ürün).
- "Seansa hazırlan": Oku (sayfalarıyla) · Yazdır (form numarasıyla) · Masaya · Önceki oturumdan gelen. Her grup 1–2 satır.
- "Seansı tamamla": Ver · Doldur (form adı) · kayıt alanları · sonraki oturum için tek satır.
- Beklenmedik durumlar, yaşa göre uyarlama, çıkış kontrol listeleri gibi tablolar portala taşınmaz; yalnızca sayfa numarası verilir.
- Maddeler tam cümle olmak zorunda değil; "·" ile ayrılmış kısa ifadeler yeterli.

## İçerik kuralları
- Kaynak belgeyi (kılavuzun son hâli) okumadan içerik üretme. Elde olmayan dosyayı kullanıcıdan iste.
- Telif: kılavuzun ve hikâyelerin uzun metinlerini portala aktarma; kısa madde + sayfa referansı yeterli.
- Depo public olabilir: depoya klinik ayrıntı, kişisel veri ya da kılavuzdan uzun alıntı koyma.
- Kayıt alanlarında çocuk/aile adı istenmez; kod ya da kısaltma kullanılır.

## Sayfa referansları
- "Kılavuz s. N" her zaman **kitap sayfa numarasıdır** (kılavuz PDF'inin ve form envanterinin kullandığı numara). Oturum içi sayfa numarası kullanılmaz.
- Her oturumun başlığında o oturumun kitaptaki sayfa aralığı gösterilir (ör. "Kılavuz s. 47–58"); maddelerdeki sayfalar bu aralıkta olmalıdır.
- Sayfa numarası tahmin edilmez; kılavuzun son hâlinin PDF'inden okunur. Eski kayıtlardaki "s. 2", "s. 9" gibi oturum içi numaralar Adım 2'deki yeniden eşleştirmede kitap numarasına çevrilir.

## Çalışma kuralları
- Her değişiklik ayrı dalda yapılır. `main`'e birleştirme ve canlı siteye çıkış yalnızca kullanıcı onayıyla.
- Tek görünüm (kullanıcı kararı): Oturum kartına tıklanınca doğrudan rehber (3 bölüm) açılır; "Hızlı Hazırlık" ve onunla gelen "kaldığın yere dön" kaldırıldı. Her oturumda "Seans planını yazdır" düğmesi tek sayfalık A4 çıktı verir.
- Bozulmaması gerekenler: logo/ana ekran düğmesi, süre notu ("süreler tahminidir"), işaretleri temizle, notların sonraki oturuma aktarımı, kayıt alanı gizlilik uyarısı, A4 seans planının tek sayfaya sığması.
- 7, 11 ve 16. oturumlarda bölüm değerlendirmesi (Bölüm Kapanışı), 20. oturumda isteğe bağlı program kapanışı ve program sonu notları var.
- Form PDF'leri portala ve GitHub'a yüklenmez (kullanıcı kararı, 24 Kasım 2026). `formlar/` klasörü ve `*.pdf` `.gitignore`'dadır; PDF'ler yalnızca kullanıcının bilgisayarında kalır. Hiçbir commit'e PDF girmez.
- Portalda PDF bağlantısı ya da etiketi yoktur. Formlar yalnızca adı, numarası ve sayfasıyla anılır (ör. "Form 5 · İpucu Listesi (s. 54 · Formlar Kitapçığı s. 9)"). Kitapçık sayfası ekler envanterinin (`Form ve R Envanteri.csv`, "Kitapçık sayfa" sütunu) verdiği numaradır; "Yazdır" maddelerinde kılavuz sayfasının yanında yazılır. A4 seans planında "Kitapçık s." diye kısaltılır. Sayfası olmayan formlar (Form 1, 2 ve beceri takip formları 3/9/25/34) yalnızca numara ve adla yazılır; sayfa uydurulmaz.
- Depo: `apamer/simonrehber`. Yayın: Cloudflare Pages `simonrehber.pages.dev`; `main` = canlı, diğer dallar = önizleme. Bu yüzden bir dalı GitHub'a göndermek de onun önizlemesini yayına çıkarır: göndermeden önce kullanıcıya sorulur.
- Her değişiklikten sonra masaüstü ve telefon genişliğinde (≈375 px) test et; görünüm değişmemesi gereken işlerde öncesi/sonrası ekran görüntüsüyle karşılaştır.
- Kendi başına karar verilebilir: kod yapısı ve teknik çözümler, kılavuza dayalı içerik güncellemeleri, yazım ve terim düzeltmeleri.
- Önce sorulur: kılavuzla çelişen ya da anlam değiştiren klinik ifade; kılavuzda olmayan yeni özellik ya da metin; `main`'e veya canlı siteye çıkış; silme ya da geri alınamaz işlemler.
- Kullanıcı kod bilmiyor ama deneyimli bir webmaster: her adımda ne yapıldığını ve nedenini sade Türkçeyle anlat.
- Basılı kitabın kaynak dosyalarına (INDD, INDB, Links) dokunulmaz; yalnızca okunur.
