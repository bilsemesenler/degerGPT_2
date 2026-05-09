# 📖 Dinim İslâm – Ahlâk Öğrenme Uygulaması

Dinim İslâm kitabının (7. Baskı) **İslâm Ahlâkının Öngördüğü Model İnsan** ünitesini (s.151–189) kapsayan interaktif mobil öğrenme uygulaması.

## Özellikler

- 26 konu başlığı (13 iyi ahlâk + 13 kötü ahlâk)
- Her konuda Claude AI destekli sohbet robotu
- Konu bazlı tamamlanma takibi + genel ilerleme çubuğu
- Tam mobil uyumlu, dark mode destekli

---

## 📁 Dosya Yapısı

```
/
├── index.html          ← Tek sayfa uygulama
├── vercel.json         ← Vercel yapılandırması
├── api/
│   └── chat.js         ← Anthropic API proxy (API anahtarı burada güvende)
└── README.md
```

---

## 🚀 Deploy (Vercel – Önerilen)

### 1. GitHub'a yükle

```bash
git init
git add .
git commit -m "ilk commit"
git branch -M main
git remote add origin https://github.com/KULLANICI_ADI/REPO_ADI.git
git push -u origin main
```

### 2. Vercel'e bağla

1. [vercel.com](https://vercel.com) → **New Project** → GitHub reponuzu seçin
2. Framework: **Other** (Next.js değil)
3. **Deploy** butonuna basın

### 3. API anahtarını ekle

Vercel Dashboard → Projeniz → **Settings** → **Environment Variables**

| Key | Value |
|-----|-------|
| `ANTHROPIC_API_KEY` | `sk-ant-...` |

Ekledikten sonra **Redeploy** yapın. ✅

---

## 🔧 Netlify ile Deploy

```bash
# Netlify CLI ile
npm i -g netlify-cli
netlify login
netlify deploy --dir . --prod
```

Ardından Netlify Dashboard → **Site settings** → **Environment variables** bölümünden
`ANTHROPIC_API_KEY` değişkenini ekleyin.

> **Not:** Netlify'da `api/chat.js` otomatik Serverless Function olarak çalışır.
> `netlify.toml` dosyası eklemeniz gerekebilir:
> ```toml
> [functions]
>   directory = "api"
> ```

---

## 🔒 Güvenlik

API anahtarı `api/chat.js` içinde `process.env.ANTHROPIC_API_KEY` olarak sunucuda okunur.
Tarayıcıya hiç gönderilmez — güvenlidir.

---

## 📚 Konu Listesi

### İyi Ahlâk (Övülen)
Doğruluk · İnfak · İffet · Emanete Riayet · Âdil Olmak · Kardeşlik ·
Hoşgörü ve Bağışlama · Sabır · Alçakgönüllülük · Sözünde Durmak ·
Görgülü Olmak · İyi Davranmak ve Güzel Söz · Yardımlaşmak

### Kötü Ahlâk (Yerilen)
Cimrilik · İftira · İyiliği Başa Kakmak · Gıybet · Kibir · Bozgunculuk ·
Haset · Savurganlık · Yalan · Hırsızlık · İnsanları Küçük Düşürmek ·
Riyâ/Gösteriş · Zina · Sarhoşluk ve Kumar · Büyücülük · Rüşvet
