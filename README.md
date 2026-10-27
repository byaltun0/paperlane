# Paperlane — Tanıtım Sitesi

Paperlane PDF uygulaması için statik, bağımsız (framework'süz) tanıtım sitesi. Saf HTML/CSS/JS olduğu için Netlify, Vercel, Cloudflare Pages veya **GitHub Pages** dahil her statik barındırma servisine olduğu gibi yüklenip çalışır.

## İçerik
- `index.html` — Ana sayfa (özellikler, ekran görüntüleri, SEO + yapılandırılmış veri)
- `privacy.html` — Gizlilik Politikası (Play Store / App Store başvurusu için gerekli)
- `terms.html` — Kullanım Koşulları
- `support.html` — Destek, SSS ve iletişim (Play Store "Destek e-postası / URL" alanı için kullanılabilir)
- `404.html` — Özel 404 sayfası
- `robots.txt`, `sitemap.xml` — arama motoru taraması için
- `site.webmanifest` — ikon/tema meta verisi
- `assets/style.css`, `assets/script.js` — ortak stil ve menü betiği
- `assets/img/` — ekran görüntüleri ve ikonlar (sıkıştırılmış)

## GitHub Pages ile yayınlama
1. Bu klasörün içeriğini bir GitHub reposuna yükleyin (kök dizine).
2. Repo → **Settings → Pages** → Source: `Deploy from a branch` → Branch: `main` / `/ (root)` seçin.
3. Birkaç dakika içinde siteniz `https://kullaniciadi.github.io/repo-adi/` adresinde yayında olur.
4. Kendi alan adınızı bağlayacaksanız (ör. `paperlaneapp.com`), **Settings → Pages → Custom domain** alanına yazın ve DNS sağlayıcınızda bir `CNAME` kaydı oluşturun.

Tüm bağlantılar göreli (relative) yazıldığı için site, kök dizinde veya bir alt klasörde (`/repo-adi/` gibi) barındırılsa da otomatik olarak doğru çalışır — ekstra ayar gerekmez.

## Yayına almadan önce güncellemeniz gerekenler
- [ ] `index.html`, `privacy.html`, `terms.html`, `support.html` içindeki `https://www.paperlaneapp.com` canonical/OG adreslerini gerçek alan adınızla değiştirin (bulmak için dosyalarda "paperlaneapp.com" arayın).
- [ ] `sitemap.xml` ve `robots.txt` içindeki alan adını güncelleyin.
- [ ] iOS uygulamanız App Store'da yayına girince, `index.html` içindeki "App Store · Yakında" rozetini gerçek App Store bağlantınızla değiştirin (ilgili `<span class="store-btn secondary">` bloğunu bir `<a>` etiketine çevirin).
- [ ] Google Search Console ve (varsa) Bing Webmaster Tools'a siteyi ekleyip `sitemap.xml` adresini gönderin.

## SEO notları
- Sayfa başlıkları ve açıklamaları "profesyonel PDF uygulaması", "PDF tarama", "PDF birleştirme" gibi aranma hacmi yüksek anahtar kelimeler etrafında kuruldu.
- Ana sayfada `MobileApplication` yapılandırılmış verisi (JSON-LD), destek sayfasında `FAQPage` yapılandırılmış verisi bulunur — Google'ın zengin sonuçlarında (rich results) görünme ihtimalini artırır.
- Görseller sıkıştırılmış, açıklayıcı `alt` metinleri ve `loading="lazy"` ile eklendi.
- Tüm sayfalarda `canonical`, Open Graph ve Twitter Card etiketleri mevcuttur.

## Geliştirici
By Altun · byaltun4@gmail.com
Google Play geliştirici sayfası: https://play.google.com/store/apps/developer?id=By+Altun
