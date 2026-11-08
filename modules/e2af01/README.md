# tema-kuyumcu · e2af01 — Altın Fiyat Bandı (Bilgilendirme)

## Nedir

tema-kuyumcu sitesinin matrix modülü. `Altın Fiyat Bandı (Bilgilendirme)` şablonu (section kökü,
sınıf `modulex-af`) render sırasında sitenin sayfa akışına eklenir. Şablon içeriği
`index.html`'deki `{{...}}` soketleriyle, veri/tema değerleri `index.json`'la
beslenir.

## Dosyalar

| Dosya | Rol |
|-------|-----|
| `back.js` | Modül davranışı (vanilla JS) (2 KB) |
| `index.html` | Modül şablonu (render hedefi) (4 KB) |
| `index.json` | Veri + tema token'ları (3 KB) |

## Girdiler
| Değişken | Örnek değer |
|--------|-------------|
| `bgcolor` | `var(--mx-site-surface, #f6f6f4)` |
| `textcolor` | `var(--mx-site-text, #1b1b1b)` |
| `mutedcolor` | `color-mix(in srgb, var(--mx-site-text, #1b1b1b) 72%, var(--mx-site-bg, #fff))` |
| `surface` | `var(--mx-site-bg, #ffffff)` |
| `accent` | `var(--mx-site-primary, #2563eb)` |
| `accentText` | `var(--mx-site-primary-contrast, #ffffff)` |
| `bordercolor` | `color-mix(in srgb, var(--mx-site-text, #1b1b1b) 18%, transparent)` |
| `speed` | `40` |

- `name`: `Altın Fiyat Bandı (Bilgilendirme)`
- `data`: 2 kayıt. Örnek: `{"updatedAt": "2026-10-30T10:30:00+03:00", "rows": [{"name": {"tr": "Gram altın", "en": "Gold gram", "ar": "غرام الذهب"}, "gram": 1, "ayar"…`
- Diğer anahtarlar: `description`, `version`, `icon`, `category`, `tags`

## Temaya bağımlılık
Tema token'ları `index.json -> desing` üzerinden gelir (önceki tablo): **bgcolor**, **textcolor**, **mutedcolor**, **surface**, **accent**.

## Test

Webmaker render hattında site sayfası üretilir; çıktı HTML'de bu modülün kök bloğu
(`modulex-af`) yerleşik görünmelidir. Render ucu: mcp/webmaker
render aracı / proje site dizini çıktısı.

## Kullanım örneği

Modül tema-kuyumcu sitesinde `web/matrix/modules/e2af01/` yolunda tanımlıdır; sayfa
yapılandırması bu yolu referans alır. Veri örneği (`index.json`):
```
{
  "name": "Altın Fiyat Bandı (Bilgilendirme)",
  "desing": {
    "bgcolor": "var(--mx-site-surface, #f6f6f4)",
    "textcolor": "var(--mx-site-text, #1b1b1b)",
    "mutedcolor": "color-mix(in srgb, var(--mx-site-text, #1b1b1b) 72%, var(--mx-site-bg, #fff))",
    "surface": "var(--mx-site-bg, #ffffff)",
    "accent": "var(--mx-site-primary, #2563eb)",
    "accentText": "var(--mx-site-primary-contrast, #ffffff)",
    "bordercolor": "color-mix(in srgb, var(--mx-site-text, #1b1b1b) 18%, transparent)",
    "speed": 40,
    "title": {
      "tr": "Bilgilendirme amaçlı altın fiyatları",
      "en": "Gold prices — for information only",
      "ar": "أسعار الذهب — للاطلاع فقط"
    },
    "karatFmt"
```

## Notlar

- Oluşturuldu: 2026-11-01 — modül envanterinde otomatik tamamlanan README (kaynak dosyalar: index.json, index.html).
- İçerik bu klasördeki gerçek dosyalardan okunarak yazıldı; modül değişikliğinde elden güncellenmelidir.
