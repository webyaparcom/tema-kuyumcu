# tema-kuyumcu · e2mn01 — Menü E-Ticaret

## Nedir

tema-kuyumcu sitesinin matrix modülü. `Menü E-Ticaret` şablonu (div kökü,
sınıf `modulex`) render sırasında sitenin sayfa akışına eklenir. Şablon içeriği
`index.html`'deki `{{...}}` soketleriyle, veri/tema değerleri `index.json`'la
beslenir.

## Dosyalar

| Dosya | Rol |
|-------|-----|
| `back.js` | Modül davranışı (vanilla JS) (2 KB) |
| `index.html` | Modül şablonu (render hedefi) (9 KB) |
| `index.jpeg` | Önizleme görseli (14 KB) |
| `index.json` | Veri + tema token'ları (1 KB) |

## Girdiler
| Değişken | Örnek değer |
|--------|-------------|
| `logo` | `logo.png` |
| `color` | `#1e3046` |
| `colorhover` | `#123763` |
| `height` | `50px` |
| `urlsepet` | `sepet` |
| `bgcolor` | `#1e3046` |
| `bgcolorhover` | `#123763` |
| `searchPlaceholder` | `{'tr': 'Aradığınız ürün, kategori veya markalar burada...', 'en': 'Search products, categories or brands...'}` |

- `name`: `Menü E-Ticaret`
- Diğer anahtarlar: `category`, `description`, `version`, `icon`

## Temaya bağımlılık
Tema token'ları `index.json -> desing` üzerinden gelir (önceki tablo): **logo**, **color**, **colorhover**, **height**, **urlsepet**.

## Test

Webmaker render hattında site sayfası üretilir; çıktı HTML'de bu modülün kök bloğu
(`modulex`) yerleşik görünmelidir. Render ucu: mcp/webmaker
render aracı / proje site dizini çıktısı.

## Kullanım örneği

Modül tema-kuyumcu sitesinde `web/matrix/modules/e2mn01/` yolunda tanımlıdır; sayfa
yapılandırması bu yolu referans alır. Veri örneği (`index.json`):
```
{
  "name": "Menü E-Ticaret",
  "desing": {
    "logo": "logo.png",
    "color": "#1e3046",
    "colorhover": "#123763",
    "height": "50px",
    "urlsepet": "sepet",
    "bgcolor": "#1e3046",
    "bgcolorhover": "#123763",
    "searchPlaceholder": {
      "tr": "Aradığınız ürün, kategori veya markalar burada...",
      "en": "Search products, categories or brands..."
    },
    "searchAria": {
      "tr": "Ürün, kategori veya marka ara",
      "en": "Search product, category or brand"
    },
    "cartText": {
      "tr": "Sepetim",
      "en": "My Cart"
    },
    "loginText": {
      "tr": "Üye Girişi",
      "en": "Member Login"
    },
    "welcomeTitle": {
      "tr": "Hoş geldiniz!",
 
```

## Notlar

- Oluşturuldu: 2026-11-01 — modül envanterinde otomatik tamamlanan README (kaynak dosyalar: index.json, index.html).
- İçerik bu klasördeki gerçek dosyalardan okunarak yazıldı; modül değişikliğinde elden güncellenmelidir.
