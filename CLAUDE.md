# Simon Says | Seans Rehberim — çalışma notları

## Projenin amacı
Simon Says Uygulayıcı Kılavuzu'nu kullanan uygulayıcılar için seans yardım portalı (APAMER Psikoloji Yayınları).
Portal basılı kılavuzun **yanında** kullanılır; kılavuzun yerini tutmaz.

- Kılavuz metnini kopyalamaz. Kısa, eyleme dönük maddeler verir ve ayrıntı için kılavuz sayfasına ya da R- referansına yönlendirir.
- 20 oturum, beş grupta: Giriş (1–2), Çalışma Kitabı 1 (3–7), ÇK2 (8–11), ÇK3 (12–16), ÇK4 (17–20). Her grubun kendi kitap rengi, her oturumun kendi ikonu var.
- Her oturumun üç bölümü var: **Seansa hazırlan / Seansı uygula / Seansı tamamla**. N. oturumun "tamamla" bölümüne kaydedilen notlar N+1. oturumun "hazırlan" bölümünde görünür.
- Veriler yalnızca tarayıcıda (localStorage, `ssr:` önekiyle) saklanır. Sunucu, hesap ya da veri gönderimi yok.

## Dosya yapısı
- `index.html`: portalın tamamı (CSS, JS, oturum verisi ve gömülü logo tek dosyada). Oturum içeriği `const DATA={...}` nesnesinde.
- `simon-beyin.png`, `robots.txt` (arama motorlarını engeller), `README.md`.
- Not: 21 Ekim 2026'da lacivert arayüz pilotu (yalnızca 1–2. oturum) `index.html`'in yerine geçti. 20 oturumluk önceki sürüm git geçmişinde `28700b4` commit'inde duruyor; içerik oradan alınacak.

## Terim kuralları
- **Koç** (Rehber değil), **Uygulayıcı** (Terapist değil), **çocuk** (Danışan değil).
- Beceri adları: Çalışma Belleği, Tepki Engelleme, Bilişsel Esneklik, Sonuç Odaklı Düşünme (Planlama).
  Kısa adlar: Hatırlama, Durdurma, Değiştirme, Planlama. "Fren" dili kullanılmaz.
- "Ödev" değil **ev çalışması**; "yoldan çıkmak" değil **rotadan çıkmak**.
- Sabit adlar: **Bravo, Başardın!**, **Aferin biletleri**, **Beceri Kontrol Kartları**.
- Kesin, abartılı ya da tanı/etiket dili kullanılmaz.

## İçerik kuralları
- Kaynak belgeyi (kılavuzun son hâli) okumadan içerik üretme. Elde olmayan dosyayı kullanıcıdan iste.
- Telif: kılavuzun ve hikâyelerin uzun metinlerini portala aktarma; kısa madde + sayfa referansı yeterli.
- Depo public olabilir: depoya klinik ayrıntı, kişisel veri ya da kılavuzdan uzun alıntı koyma.
- Kayıt alanlarında çocuk/aile adı istenmez; kod ya da kısaltma kullanılır.

## Çalışma kuralları
- Her değişiklik ayrı dalda yapılır. `main`'e birleştirme ve canlı siteye çıkış yalnızca kullanıcı onayıyla.
- Bozulmaması gerekenler: logo/ana ekran düğmesi, "kaldığın yere dön", süre notu ("süreler tahminidir"), işaretleri temizle, notların sonraki oturuma aktarımı.
- Yalnızca 1. oturumda Hızlı Hazırlık var. 7, 11 ve 16. oturumlarda kitap kapanış listeleri, 20. oturumda program sonu notları var.
- Her değişiklikten sonra masaüstü ve telefon genişliğinde (≈375 px) test et; görünüm değişmemesi gereken işlerde öncesi/sonrası ekran görüntüsüyle karşılaştır.
- Kendi başına karar verilebilir: kod yapısı ve teknik çözümler, kılavuza dayalı içerik güncellemeleri, yazım ve terim düzeltmeleri.
- Önce sorulur: kılavuzla çelişen ya da anlam değiştiren klinik ifade; kılavuzda olmayan yeni özellik ya da metin; `main`'e veya canlı siteye çıkış; silme ya da geri alınamaz işlemler.
- Kullanıcı kod bilmiyor ama deneyimli bir webmaster: her adımda ne yapıldığını ve nedenini sade Türkçeyle anlat.
- Basılı kitabın kaynak dosyalarına (INDD, INDB, Links) dokunulmaz; yalnızca okunur.
