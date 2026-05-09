# Dinim İslâm - Ahlâk Öğrenme Uygulaması

İslâm Ahlâkının Öngördüğü Model İnsan ünitesini (Dinim İslâm 7. Baskı, s. 151-189) kapsayan interaktif öğrenme uygulaması.

## Özellikler
- 📚 Menü tabanlı konu seçimi (İyi & Kötü Ahlâk)
- 💬 Sohbet robotu ile öğrenme
- ✅ Konu bazlı hedef takibi ve tamamlanma yüzdesi
- 📱 Tam mobil uyumlu tasarım

## Deploy

### Vercel (Önerilen)
```bash
npx vercel
```

### Netlify
```bash
npx netlify deploy --dir . --prod
```

### GitHub Pages
Repo ayarlarından `main` branch, `/` (root) klasörünü seçin.

## API Anahtarı

`index.html` dosyasını açıp şu satırı bulun:
```js
const API_KEY = 'YOUR_ANTHROPIC_API_KEY';
```
Kendi Anthropic API anahtarınızla değiştirin.

> **Güvenlik notu:** API anahtarını istemci taraflı kodda tutmak geliştirme/kişisel kullanım için uygundur. Prodüksiyonda bir backend proxy kullanmanız önerilir.

## Dosya Yapısı
```
/
├── index.html   ← Tek sayfa uygulama (tüm kod burada)
└── README.md
```
