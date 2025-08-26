# 🌐 Sentiric Web Portal - Geliştirme Yol Haritası

Bu belge, ana web portalının geliştirme görevlerini projenin genel fazlarına uygun olarak listeler.

---

### **FAZ 1: Pazarlama Vitrini ve Müşteri Kazanımı**

**Amaç:** Potansiyel müşterilere Sentiric'in ne olduğunu anlatan, onları kaydolmaya teşvik eden ve kurumsal satış için bir iletişim kanalı sunan temel bir pazarlama sitesi oluşturmak.

-   [ ] **Görev ID: WEB-001 - Next.js Proje Kurulumu**
    -   **Açıklama:** TypeScript, Tailwind CSS ve `sentiric-governance`'daki standartlarla uyumlu bir Next.js projesi oluştur.
    -   **Kabul Kriterleri:**
        -   [ ] Proje `create-next-app` ile oluşturulmalı.
        -   [ ] Temel sayfa yapısı (`/pages`) ve layout bileşenleri oluşturulmalı.

-   [ ] **Görev ID: WEB-002 - Pazarlama Sayfalarının Oluşturulması (Statik)**
    -   **Açıklama:** `governance/docs/marketing/pages` altındaki Markdown dosyalarını içerik kaynağı olarak kullanarak ana pazarlama sayfalarını oluştur.
    -   **Kabul Kriterleri:**
        -   [ ] Ana Sayfa (`/`)
        -   [ ] Fiyatlandırma Sayfası (`/pricing`) - Cloud ve Self-Hosted planlarını göstermeli.
        -   [ ] Kurumsal İletişim Sayfası (`/contact-enterprise`) - Form içermeli.
        -   [ ] ROI Raporu İndirme Sayfası (`/report-roi`) - Form içermeli.
        -   [ ] Bu sayfalar, `getStaticProps` kullanılarak build zamanında statik olarak üretilmelidir.

-   [ ] **Görev ID: WEB-003 - Kullanıcı Kayıt (`Sign Up`) Akışı**
    -   **Açıklama:** Kullanıcıların platforma kaydolmasını sağlayan `/signup` sayfasını ve `api-gateway` entegrasyonunu yap.
    -   **Kabul Kriterleri:**
        -   [ ] `/signup` sayfasında isim, e-posta, şifre alanları olan bir form bulunmalı.
        -   [ ] Form gönderildiğinde, `POST /api/v1/auth/register` endpoint'ine istek atılmalı.
        -   [ ] Başarılı kayıt sonrası, kullanıcı bilgilendirilmeli ve `dashboard.sentiric.ai` adresine yönlendirilmelidir.
        -   [ ] E-posta zaten kayıtlı gibi hatalar kullanıcıya net bir şekilde gösterilmelidir.

-   [ ] **Görev ID: WEB-004 - Kullanıcı Giriş (`Login`) Akışı**
    -   **Açıklama:** Mevcut kullanıcıların platforma giriş yapmasını sağlayan `/login` sayfasını oluştur.
    -   **Kabul Kriterleri:**
        -   [ ] `/login` sayfasında e-posta ve şifre alanları olan bir form bulunmalı.
        -   [ ] Form gönderildiğinde, `POST /api/v1/auth/login` endpoint'ine istek atılmalı.
        -   [ ] Başarılı girişte, dönen JWT token saklanmalı ve kullanıcı `dashboard.sentiric.ai`'ye yönlendirilmeli.

---

### **FAZ 2: Geliştirici Portalı ve İçerik Entegrasyonu**

**Amaç:** Web sitesini, geliştiriciler için de değerli bir kaynak haline getirmek.

-   [ ] **Görev ID: WEB-005 - Dokümantasyon Portalı (`/docs`)**
    -   **Açıklama:** `sentiric-governance` reposundaki tüm Markdown dosyalarını otomatik olarak çekip sunan, arama ve navigasyon özellikli bir dokümantasyon bölümü oluştur.
    -   **Kabul Kriterleri:**
        -   [ ] `governance` reposu bir `git submodule` olarak projeye dahil edilmeli veya bir CI script'i ile build zamanında çekilmelidir.
        -   [ ] `/docs` altındaki tüm sayfalar, `governance`'daki dosya yapısını yansıtacak şekilde dinamik olarak (`getStaticPaths` ile) oluşturulmalıdır.
        -   [ ] Sayfalar arası linkler ve `mermaid` diyagramları doğru bir şekilde render edilmelidir.

-   [ ] **Görev ID: WEB-006 - Blog Altyapısı**
    -   **Açıklama:** Teknik makaleler, vaka analizleri ve duyurular için bir blog altyapısı kur.
    -   **Durum:** ⬜ Planlandı.
