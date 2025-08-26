# 🌐 Sentiric Web Portal

[![Status](https://img.shields.io/badge/status-in_development-yellow.svg)]()
[![Framework](https://img.shields.io/badge/framework-Next.js-black.svg)](https://nextjs.org/)
[![Styling](https://img.shields.io/badge/styling-Tailwind_CSS-blue.svg)](https://tailwindcss.com/)

Bu depo, [Sentiric Platformu](https://sentiric.ai)'nun resmi web portalının kaynak kodunu içerir. Bu portal, projenin halka açık yüzü olup; pazarlama, dokümantasyon ve kullanıcı katılımı (kayıt/giriş) için merkezi bir merkez olarak hizmet verir.

## ✨ Felsefe ve Teknoloji

Bu proje, modern web geliştirme standartları kullanılarak oluşturulmuştur:

*   **Framework:** Hızlı, SEO dostu ve hem statik hem de dinamik sayfalar oluşturabilen **Next.js**.
*   **Dil:** Tip güvenliği ve ölçeklenebilirlik için **TypeScript**.
*   **Stil:** Hızlı ve tutarlı arayüzler için **Tailwind CSS**.
*   **İçerik Kaynağı:** Pazarlama sayfalarının içeriği, projenin ana anayasası olan [`sentiric-governance`](https://github.com/sentiric/sentiric-governance) reposundaki Markdown dosyalarından dinamik olarak çekilir. Bu, içerik ve sunum katmanlarını birbirinden ayırır.

## 🚀 Yerel Geliştirme Ortamını Kurma

### Önkoşullar
*   Node.js v18+
*   Yarn (veya npm)

### Kurulum Adımları

1.  **Repoyu Klonlayın:**
    ```bash
    git clone https://github.com/sentiric/sentiric-website.git
    cd sentiric-website
    ```

2.  **Bağımlılıkları Yükleyin:**
    ```bash
    yarn install
    ```

3.  **Ortam Değişkenlerini Ayarlayın:**
    `.env.local.example` dosyasını kopyalayarak `.env.local` adında yeni bir dosya oluşturun ve içindeki `API_GATEWAY_URL` gibi değişkenleri kendi yerel geliştirme ortamınıza göre düzenleyin.
    ```bash
    cp .env.local.example .env.local
    ```

4.  **Geliştirme Sunucusunu Başlatın:**
    ```bash
    yarn dev
    ```

5.  **Tarayıcıda Açın:**
    [http://localhost:3000](http://localhost:3000) adresini ziyaret ederek çalışan siteyi görebilirsiniz.

## 📂 Dizin Yapısı

*   `/pages`: Next.js'in dosya tabanlı yönlendirme (routing) sistemi. Her `.tsx` dosyası bir sayfaya karşılık gelir.
*   `/components`: Sayfalar arasında paylaşılan React bileşenleri (Navbar, Footer, Button vb.).
*   `/styles`: Global CSS ve Tailwind CSS yapılandırması.
*   `/lib`: Harici API'lerle konuşan veya `governance` reposundan veri çeken yardımcı fonksiyonlar.
*   `/public`: Statik varlıklar (resimler, fontlar vb.).

## 🤝 Katkıda Bulunma

Bu projeye katkıda bulunmak için lütfen `sentiric-governance` reposundaki [kodlama standartlarına](https://github.com/sentiric/sentiric-governance/blob/main/docs/engineering/Coding-Standards.md) ve genel katkı rehberine göz atın.

1.  Yeni bir özellik için `feature/özellik-adi` adında bir branch oluşturun.
2.  Değişikliklerinizi yapın.
3.  Değişikliklerinizi `main` branch'ine birleştirmek için bir Pull Request (PR) açın.

---
## 🏛️ Anayasal Konum
Bu web portalı, [Sentiric Anayasası'nın (v11.0)](https://github.com/sentiric/sentiric-governance/blob/main/docs/blueprint/Architecture-Overview.md) **Yönetim, Altyapı ve Geliştirici Ekosistemi** katmanının son kullanıcıya dokunan yüzüdür.
