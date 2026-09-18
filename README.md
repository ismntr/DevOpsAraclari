# 🚀 AltyapıSim: DevOps Altyapı Analizi & İnteraktif Simülasyonu

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live%20Demo-brightgreen?logo=github&style=for-the-badge)](https://ismntr.github.io/DevOpsAraclari/)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)](LICENSE)

> **Modern yazılım geliştirme ortamları ile canlı üretim ortamı (Production) arasındaki mimari farkları, ağ erişim engellerini ve konteynerizasyonun önemini görselleştiren interaktif DevOps simülasyon aracı ve ders notları platformu.**

---

## 📌 Proje Hakkında

Bir yazılım projesi geliştirmek yalnızca kod yazmaktan ibaret değildir. Kodun çalışacağı **ortamın (environment)** hazırlanması, dış sistemlerle (GitLab Webhook'ları, ödeme sistemleri, API sağlayıcıları) **ağ iletişiminin (network)** kurulması sistemin can damarıdır.

Bu proje;
1. Ev/ofis ağlarındaki **NAT ve Güvenlik Duvarı (Firewall)** kısıtlamalarını ve **Ngrok (Reverse Proxy & Tunneling)** çözümünü,
2. Farklı işletim sistemlerinde yaşanan bağımlılık çakışmalarını (**"Benim bilgisayarımda çalışıyordu!"** sorunu) ve **Docker (Containerization)** mimarisinin getirdiği çözümü,

hem **canlı interaktif simülasyonlar** hem de detaylı **teorik ders notları** ile ele alır.

---

## 🎮 İnteraktif Modüller ve Özellikler

### 1. 🌐 Ağ İletişimi & Ngrok Senaryosu
* **GitLab Webhook Akışı:** Dış dünyadaki bir servisten yerel makineye (Localhost) gönderilen isteklerin ağ üzerindeki yolculuğunu gösteren animasyonlu veri akış çizgileri.
* **Ortam Karşılaştırması:** *Geliştirme (Lokal)* ve *Canlı Sunucu (Prod)* modları arasında tek tıkla geçiş.
* **İnteraktif Ngrok Anahtarı:** Ngrok açıkken paketlerin tünelden geçişi; Ngrok kapatıldığında ise modem güvenlik duvarına (Firewall) çarparak engellenmesi (`Connection Refused`).
* **Ders Notları:** NAT mekanizması, tersine tünelleme, Ngrok'un neden sadece geliştirme aşamasında kullanıldığı ve canlıda neden **asla** kullanılmaması gerektiği.

### 2. 🐳 Altyapı & Docker Senaryosu
* **Docker'sız Kaos (Geleneksel):** Mac (ARM) vs Windows ortamlarında yaşanan PostgreSQL ve Redis sürüm uyuşmazlıkları, port çakışmaları ve ortam konfigürasyon hataları simülasyonu.
* **Docker ile Düzen (Modern):** `docker compose up` tek komutuyla platformdan bağımsız PostgreSQL ve Redis konteynerlerinin saniyeler içinde ayağa kalkması.
* **Ders Notları:** Sanallaştırma (VM) vs Konteynerleştirme farkı, Çevre Eşitliği (%100 Environment Parity), CI/CD pipeline süreçlerinde Docker imajlarının yeri.

### 3. ⚖️ Mimari Karar & Gelecek Stratejisi
* **Ngrok Kararı:** *"Gerekli Bir Kötülük"*. Canlıya çıkıldığı anda kaldırılacak, yerini statik IP ve Nginx/Traefik gibi kurumsal ters vekiller alacaktır.
* **Docker Kararı:** *"Sistemin Temel Taşı"*. Geliştirmeden canlıya kadar tüm DevOps süreçlerinin merkezinde yer almaya devam edecektir.

---

## 🛠️ Kullanılan Teknolojiler

* **HTML5:** Anlamsal etiketleme ve modern sayfa yapısı.
* **Vanilla CSS & Tailwind CSS (CDN):** Glassmorphism tasarım dili, karanlık tema (Dark Mode), yumuşak geçişler ve dinamik animasyonlar.
* **FontAwesome 6:** Zengin vektörel ikon kütüphanesi.
* **Google Fonts (Inter):** Modern ve okunaklı tipografi.
* **Vanilla JavaScript:** Gerçek zamanlı DOM manipülasyonu, durum yönetimi (state management) ve tab navigasyonu.

---

## 🌐 GitHub Pages ile Yayına Alma (Canlıya Çıkış Rehberi)

Bu projeyi GitHub Pages üzerinde yayınlamak için aşağıdaki adımları sırasıyla takip edebilirsiniz:

### 1. Adım: Yerel Git Deposunu Başlatın ve Dosyaları Ekleyin
Bulunduğunuz proje dizininde bir terminal (PowerShell / Git Bash) açın ve şu komutları çalıştırın:

```bash
# Git deposunu başlatın
git init

# Tüm dosyaları takibe alın
git add .

# İlk commit'i oluşturun
git commit -m "feat: DevOps altyapı simülasyonu ve ders notları yayına hazır"

# Ana dal adını 'main' yapın
git branch -M main
```

### 2. Adım: GitHub Üzerinde Yeni Bir Repository Açın
1. [GitHub](https://github.com/new) adresine gidin.
2. Repository adı belirleyin (Örnek: `devops-altyapi-simulasyonu` veya `devops-tools`).
3. Depoyu **Public (Herkese Açık)** seçin.
4. "Initialize this repository with a README" seçeneğini **işaretlemeyin** (zaten yerelde hazırladık).
5. **Create repository** butonuna basın.

### 3. Adım: Uzak Depoya (Remote) Bağlayın ve Yükleyin (Push)
Terminalinize dönün ve GitHub'ın verdiği bağlantıyı ekleyerek dosyalarınızı push edin *(kendi kullanıcı adınızı yazın)*:

```bash
git remote add origin https://github.com/ismntr/DevOpsAraclari.git
git push -u origin main
```

### 4. Adım: GitHub Pages'i Aktif Edin
1. GitHub deponuzun üst menüsünden **Settings** sekmesine tıklayın.
2. Sol taraftaki menüden **Pages** seçeneğini seçin.
3. **Build and deployment** başlığı altındaki **Source** kısmını **Deploy from a branch** olarak bırakın.
4. **Branch** ayarını `main` ve klasörü `/ (root)` seçip **Save** butonuna tıklayın.
5. Yaklaşık 1-2 dakika sonra sayfanın üstünde sitenizin canlı bağlantısı belirecektir:
   ```
   https://ismntr.github.io/DevOpsAraclari/
   ```

> 💡 **İpucu:** Projede varsayılan giriş noktası olarak `index.html` yer aldığı için linke tıkladığınız an doğrudan simülasyon açılacaktır.

---

## 💻 Yerel Ortamda Çalıştırma

Projeyi herhangi bir sunucu kurmadan yerel bilgisayarınızda açmak isterseniz:

1. Bu depoyu klonlayın veya indirin:
   ```bash
   git clone https://github.com/ismntr/DevOpsAraclari.git
   ```
2. Klasör içindeki [index.html](index.html) dosyasını herhangi bir modern web tarayıcısında (Chrome, Firefox, Edge, Safari) çift tıklayarak doğrudan açın.
3. Dilerseniz VS Code'un **Live Server** eklentisiyle veya Python basit HTTP sunucusuyla çalıştırabilirsiniz:
   ```bash
   # Python ile çalıştırmak isterseniz:
   python -m http.server 8000
   # Tarayıcınızdan http://localhost:8000 adresine gidin
   ```

---

## 📁 Dosya Yapısı

```text
├── index.html                     # GitHub Pages ana giriş dosyası (SEO & Favicon optimizasyonlu)
├── devops_altyap_sim_lasyonu.html # Orijinal simülasyon kaynak dosyası
├── README.md                      # Proje tanıtım ve dokümantasyon dosyası
├── LICENSE                        # MIT Açık Kaynak Lisansı
└── .gitignore                     # Git tarafından yok sayılacak gereksiz sistem dosyaları
```

---

## 🤝 Katkıda Bulunma

Geri bildirimleriniz, yeni senaryo önerileriniz (örn: Kubernetes pod simülasyonu, Nginx reverse proxy vb.) veya hata düzeltmeleriniz için:
1. Bu depoyu Fork edin.
2. Yeni bir dal açın (`git checkout -b feature/yeni-senaryo`).
3. Değişikliklerinizi commit edin (`git commit -m 'feat: yeni senaryo eklendi'`).
4. Dalınıza push edin (`git push origin feature/yeni-senaryo`).
5. Bir **Pull Request** açın!

---

## 📄 Lisans

Bu proje [MIT Lisansı](LICENSE) kapsamında açık kaynak olarak yayınlanmıştır.
