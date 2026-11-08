# tema-kuyumcu · e2tv01 — E-ticaret Tab Vitrin (Tema3)

## Nedir

tema-kuyumcu sitesinin matrix modülü. `E-ticaret Tab Vitrin (Tema3)` şablonu (section kökü,
sınıf `t3vSection`) render sırasında sitenin sayfa akışına eklenir. Şablon içeriği
`index.html`'deki `{{...}}` soketleriyle, veri/tema değerleri `index.json`'la
beslenir.

## Dosyalar

| Dosya | Rol |
|-------|-----|
| `back.js` | Modül davranışı (vanilla JS) (5 KB) |
| `index.html` | Modül şablonu (render hedefi) (6 KB) |
| `index.json` | Veri + tema token'ları (1 KB) |

## Girdiler
| Değişken | Örnek değer |
|--------|-------------|
| `max` | `1200px` |
| `bgcolor` | `--bgAlt--` |
| `cardbg` | `--bgcolor--` |
| `bordercolor` | `--bordercolor--` |
| `color` | `--color--` |
| `pricecolor` | `--pricecolor--` |
| `oldpricecolor` | `--oldpricecolor--` |
| `badgecolor` | `#ffffff` |

- `name`: `E-ticaret Tab Vitrin (Tema3)`
- `data`: 1 kayıt. Örnek: `{"products": []}`
- Diğer anahtarlar: `category`, `description`, `version`, `icon`

## Temaya bağımlılık
Tema token'ları `index.json -> desing` üzerinden gelir (önceki tablo): **max**, **bgcolor**, **cardbg**, **bordercolor**, **color**.

## Test

Webmaker render hattında site sayfası üretilir; çıktı HTML'de bu modülün kök bloğu
(`t3vSection`) yerleşik görünmelidir. Render ucu: mcp/webmaker
render aracı / proje site dizini çıktısı.

## Kullanım örneği

Modül tema-kuyumcu sitesinde `web/matrix/modules/e2tv01/` yolunda tanımlıdır; sayfa
yapılandırması bu yolu referans alır. Veri örneği (`index.json`):
```
{
  "name": "E-ticaret Tab Vitrin (Tema3)",
  "desing": {
    "max": "1200px",
    "bgcolor": "--bgAlt--",
    "cardbg": "--bgcolor--",
    "bordercolor": "--bordercolor--",
    "color": "--color--",
    "pricecolor": "--pricecolor--",
    "oldpricecolor": "--oldpricecolor--",
    "badgecolor": "#ffffff",
    "badgebg-new": "--accent--",
    "badgebg-sale": "--accent--",
    "buttonbg": "#111111",
    "buttoncolor": "#ffffff",
    "accent": "--accent--",
    "showCount": 8,
    "columns": 4,
    "tab1Label": {
      "tr": "YENİ GELENLER",
      "en": "NEW ARRIVALS"
    },
    "tab2Label": {
      "tr": "SEÇTİKLERİMİZ",
      "en": "OUR PICKS"
    },
    "tab3Label": {
      "tr": "ÇOK SATANL
```

## Notlar

- Oluşturuldu: 2026-11-01 — modül envanterinde otomatik tamamlanan README (kaynak dosyalar: index.json, index.html).
- İçerik bu klasördeki gerçek dosyalardan okunarak yazıldı; modül değişikliğinde elden güncellenmelidir.
