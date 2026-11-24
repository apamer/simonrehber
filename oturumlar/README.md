# Oturum dosyaları

Her oturumun içeriği ayrı bir dosyada: `oturum-01.json` … `oturum-20.json`.
`index.html` sayfa açılırken bu 20 dosyayı yükler. Oturum adı, kitap grubu ve oturum ikonu `index.html` içindeki `SESS` ve `SICON` listelerinde kalır.

Not: Dosyalar tarayıcıya bir web sunucusu üzerinden gelir (GitHub Pages, Cloudflare Pages ya da yerel önizleme). `index.html` çift tıklanarak (`file://`) açılırsa oturumlar yüklenmez.

## Dosyanın yapısı

```
{
  "facts":  ["≈ 50 dk", "Uygulayıcı ve çocuk", ...],   // başlıktaki kısa bilgiler
  "phases": [ [...], [...], [...] ],                    // 0 Seansa hazırlan · 1 Seansı uygula · 2 Seansı tamamla
  "quick":  { "once": [...], "flow": [...], "after": [...] }   // yalnızca 1. oturumda: Hızlı Hazırlık
}
```

### Hazırlan ve Tamamla bölümlerindeki gruplar
| Alan | Anlamı |
|---|---|
| `g` | Grup başlığı (ör. "Yazdır", "Masaya", "Koça söyle") |
| `ic` | Grup ikonu: `phone`, `book`, `print`, `box`, `back`, `hand`, `form`, `save`, `next` |
| `i` | Maddeler (aşağıya bakın) |
| `note` | Madde yerine tek satırlık not |
| `prev`, `pf` | Önceki oturumdan gelen notlar: `prev` oturum no, `pf` gösterilecek alanlar `[alan, etiket]` |
| `f` | Sonraki oturum için kayıt alanları `[alan, etiket]`; bir sonraki oturumun `pf` listesiyle aynı alan adlarını kullanır |
| `done` | "Seansı tamamlandı olarak işaretle" düğmesinin yeri |

### Seansı uygula bölümündeki etkinlikler
| Alan | Anlamı |
|---|---|
| `a` | Etkinlik numarası |
| `t` | Etkinlik adı |
| `dk` | Tahmini süre (dakika) |
| `ref` | Kılavuz sayfası (kitap sayfa numarası; bkz. CLAUDE.md) |
| `mat` | Materyal (isteğe bağlı) |
| `koc` | Koçun durumu (isteğe bağlı, ör. "Koç odada") |
| `i` | Maddeler |

### Maddeler
- Düz metin: `"Kartları yan yana diz."`
- Beceri etiketli: `["Sahne 1 · Pijamalı Can", "CB"]`. Etiketler: `CB` Hatırlama, `TE` Durdurma, `BE` Değiştirme, `SO` Planlama, `ALL` Dört beceri.
- Çıktı: `["Beyin Becerileri Haritası", "pdf"]`

## Dikkat
- Maddelerin sırası işaretlerin kaydına bağlıdır (işaret anahtarı oturum/bölüm/grup/madde sırasından oluşur). Madde eklemek ya da sırayı değiştirmek, o oturumda cihazlarda kayıtlı eski işaretleri kaydırabilir.
- Kayıt alanı adları (`f` ve `pf` içindeki ilk değer) değişirse önceki oturumdan gelen notlar görünmez; iki oturumda birlikte değiştirilmelidir.
