# DevDocs — GitHub Pages Kurulum Rehberi

## 1. GitHub'da repo aç

1. https://github.com adresine git, giriş yap
2. Sağ üstte **+** → **New repository**
3. Repository name: `devdocs` (ya da istediğin isim)
4. **Public** seç (GitHub Pages ücretsiz için zorunlu)
5. **Create repository** tıkla

---

## 2. Dosyaları yükle

**Yöntem A — Tarayıcıdan (kod bilgisi gerekmez):**
1. Repo sayfasında **Add file** → **Upload files**
2. `index.html` dosyasını sürükle-bırak
3. `docs/` klasörünü sürükle-bırak
4. **Commit changes** tıkla

**Yöntem B — Git ile (terminal):**
```bash
git clone https://github.com/KULLANICI_ADIN/devdocs.git
# İndirdiğin dosyaları klasöre kopyala
cd devdocs
git add .
git commit -m "İlk yükleme"
git push
```

---

## 3. GitHub Pages'i aç

1. Repo sayfasında **Settings** sekmesine tıkla
2. Sol menüde **Pages**'e tıkla
3. **Source** → **Deploy from a branch**
4. **Branch** → `main` seç, klasör `/root` seç
5. **Save** tıkla

⏳ 1-2 dakika bekle, ardından siteniz şu adreste yayında:

```
https://KULLANICI_ADIN.github.io/devdocs/
```

---

## 4. Yeni döküman eklemek

1. `docs/` klasörüne yeni bir `.html` dosyası ekle
2. `index.html` içinde yeni bir kart ekle (mevcut kartları kopyalayıp düzenle)
3. GitHub'a yükle → otomatik yayınlanır

---

## Klasör yapısı

```
devdocs/
├── index.html          ← Ana sayfa
├── docs/
│   ├── git-flow.html   ← Git Flow dökümanı
│   └── ...             ← Yeni dökümanlar buraya
└── README.md
```

---

## Kendi domain bağlamak (isteğe bağlı)

Domain aldıysan (örn. `docs.sirket.com`):
1. Domain sağlayıcında DNS → CNAME kaydı ekle: `KULLANICI_ADIN.github.io`
2. GitHub Pages ayarlarında **Custom domain** alanına domain'ini yaz
3. **Enforce HTTPS** kutusunu işaretle
