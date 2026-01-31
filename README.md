# 🏗️ Monolith - Üretim Takip Yönetim Sistemi

> Modern, kullanıcı dostu ve kapsamlı bir üretim takip ve yönetim sistemi

![Project Status](https://img.shields.io/badge/status-active-success)
![Version](https://img.shields.io/badge/version-1.0.6-blue)
![Platform](https://img.shields.io/badge/platform-Windows-lightgrey)
![Tech](https://img.shields.io/badge/tech-Electron%20%7C%20React%20%7C%20Firebase-orange)

---

## 📋 Proje Hakkında

Monolith, üretim süreçlerini dijitalleştirmek ve verimliliği artırmak amacıyla geliştirdiğim **modern bir masaüstü uygulaması**dır. Electron, React ve Firebase teknolojilerini kullanarak, gerçek zamanlı üretim takibi ve yönetimi sağlayan kapsamlı bir çözüm sunuyor.

### 🎯 Amaç

Üretim firmalarının iş süreçlerini dijitalleştirerek:
- Gerçek zamanlı üretim takibi
- Malzeme ve stok yönetimi
- Raporlama ve analiz
- Çoklu kullanıcı desteği ve rol yönetimi
sağlamak.

---

## 🚀 Temel Özellikler

### 📊 Üretim Yönetimi
- **Gerçek zamanlı üretim takibi**
- İş emirleri ve görev yönetimi
- Süreç aşamaları görselleştirmesi
- Performans metrikleri ve raporlama

### ☁️ Bulut Entegrasyonu
- **Firebase Firestore** - Gerçek zamanlı veritabanı
- **Firebase Storage** - Dosya ve görsel yönetimi
- **Firebase Authentication** - Güvenli kimlik doğrulama
- Çoklu cihaz senkronizasyonu

### 🔐 Kimlik Doğrulama ve Güvenlik
- **Azure Active Directory** entegrasyonu
- **Multi-factor Authentication** desteği
- Rol tabanlı erişim kontrolü (RBAC)
- Kullanıcı ve yetki yönetimi

### 📁 Dosya Yönetimi
- **OneDrive** entegrasyonu
- Otomatik dosya senkronizasyonu
- Bulut üzerinde döküman saklama
- Microsoft Graph API kullanımı

### 📄 Raporlama
- **Excel export** (XLSX)
- **PDF oluşturma** (jsPDF)
- Özelleştirilebilir şablonlar
- Otomatik rapor üretimi

### 📲 QR Kod Sistemi
- QR kod üretimi
- Barkod okuma
- Ürün takibi
- Envanter yönetimi

### 🔄 Otomatik Güncelleme
- **electron-updater** ile otomatik update
- Versiyon kontrolü
- Kullanıcıya bildirim sistemi
- Kesintisiz güncelleme

---

## 🛠️ Kullanılan Teknolojiler

### Frontend
```
├── React 18.3.1           # UI Framework
├── TypeScript 5.6.2       # Type Safety
├── Vite 6.0.1            # Build Tool & Dev Server
└── CSS Modules           # Styling
```

### Backend & Services
```
├── Electron 28.0.0       # Desktop Framework
├── Node.js              # Runtime
└── Firebase SDK         # Cloud Services
```

### Veritabanı & Storage
```
├── Firebase Firestore   # NoSQL Database
├── Firebase Storage     # File Storage
└── LocalStorage        # Offline Data
```

### Authentication & Integration
```
├── Firebase Auth                # Email/Password Auth
├── Azure AD (MSAL Browser)     # Enterprise SSO
├── Google Auth Provider        # Social Login
└── Microsoft Graph API         # OneDrive Integration
```

### Kütüphaneler & Tools
```
├── jsPDF                # PDF Generation
├── xlsx                 # Excel Export
├── qrcode               # QR Code Generator
├── electron-builder     # App Packaging
├── electron-updater     # Auto Updates
└── concurrently        # Dev Scripts
```

---

## 🏗️ Mimari Tasarım

### Katmanlı Mimari

```
┌─────────────────────────────────────────┐
│          Presentation Layer             │
│  (React Components, UI/UX)              │
├─────────────────────────────────────────┤
│         Application Layer               │
│  (Business Logic, Services)             │
├─────────────────────────────────────────┤
│         Data Access Layer               │
│  (Firebase, LocalStorage, OneDrive)     │
├─────────────────────────────────────────┤
│       Infrastructure Layer              │
│  (Electron, Node.js, OS APIs)           │
└─────────────────────────────────────────┘
```

### Modüler Yapı

```
src/
├── components/        # Reusable UI Components
├── screens/          # Page Components
├── services/         # Business Logic
├── utils/           # Helper Functions
├── contexts/        # React Context Providers
├── hooks/           # Custom React Hooks
└── shared/          # Types & Constants
```

---

## 💡 Teknik Zorluklar ve Çözümler

### 1. Offline-First Yaklaşım
**Sorun**: İnternet bağlantısı kesintilerinde veri kaybı  
**Çözüm**: 
- LocalStorage cache mekanizması
- Offline queue sistemi
- Otomatik senkronizasyon

### 2. Gerçek Zamanlı Senkronizasyon
**Sorun**: Çoklu kullanıcı veri tutarlılığı  
**Çözüm**:
- Firebase realtime listeners
- Optimistic UI updates
- Conflict resolution stratejileri

### 3. Desktop ve Web Uyumluluğu
**Sorun**: Electron ve web platform farklılıkları  
**Çözüm**:
- Preload script güvenlik katmanı
- IPC (Inter-Process Communication) köprüleri
- Platform-agnostic kod yazımı

### 4. Performans Optimizasyonu
**Sorun**: Büyük veri setlerinde yavaşlama  
**Çözüm**:
- React.memo ve useMemo optimizasyonları
- Lazy loading ve code splitting
- Virtual scrolling (windowing)
- Debouncing ve throttling
### Planlama Dashboard
Proje ilerleme takibi, tarih yönetimi ve genel bakış ekranı.

![Planlama Dashboard](screenshots/dashboard-planlama.png)

*Özellikler:*
- Proje başlangıç ve bitiş tarihleri
- Toplam süre hesaplama
- İlerleme yüzdesi ve durum göstergesi
- Toplam parça sayısı ve üretim durumu
- Gerçek zamanlı istatistikler

Daha fazla ekran görüntüsü için [SCREENSHOTS.md](SCREENSHOTS.md) dosyasına bakın.
### Raporlama Paneli
- Rapor şablonları
- Tarih aralığı seçimi
- Excel ve PDF export
- Özelleştirilebilir filtreler

---

## 🎓 Öğrenilen Beceriler

Bu projede kazandığım temel beceriler:

### Frontend Development
- ✅ Modern React patterns (Hooks, Context, Custom Hooks)
- ✅ TypeScript ile tip güvenli kod
- ✅ Component-based architecture
- ✅ State management strategies
- ✅ Performance optimization

### Backend & Cloud
- ✅ Firebase Firestore queries ve security rules
- ✅ Cloud storage yönetimi
- ✅ Serverless architecture
- ✅ Real-time data synchronization

### Desktop Development
- ✅ Electron framework
- ✅ IPC communication
- ✅ Auto-update mechanisms
- ✅ Cross-platform packaging

### DevOps & Tools
- ✅ Git version control
- ✅ CI/CD pipeline konseptleri
- ✅ Build ve deployment süreçleri
- ✅ Debugging ve profiling

### Integration & APIs
- ✅ RESTful API consumption
- ✅ OAuth 2.0 authentication
- ✅ Microsoft Graph API
- ✅ Third-party service integrations

---

## 📦 Deployment

Proje, aşağıdaki deployment stratejisi ile dağıtılmıştır:

### Build Process
```bash
1. TypeScript compilation
2. Vite production build
3. Electron packaging
4. NSIS installer creation
```

### Distribution
- Windows 64-bit installer (.exe)
- Otomatik güncelleme sunucusu
- Sürüm yönetimi ve release notes

---

## 🔒 Güvenlik

Projede uygulanan güvenlik önlemleri:

- ✅ Environment variables ile hassas bilgi yönetimi
- ✅ Firebase security rules
- ✅ Azure AD enterprise authentication
- ✅ HTTPS only communication
- ✅ XSS ve CSRF koruması
- ✅ Input validation ve sanitization
- ✅ Rol tabanlı erişim kontrolü

---

## 📈 Proje Metrikleri

### Kod İstatistikleri
- **Toplam Satır**: ~60,000+ lines
- **Component Sayısı**: 40+ React components
- **Service Modülleri**: 15+ service modules
- **Utility Functions**: 20+ helper utilities

### Performans
- **İlk Yüklenme**: < 3 saniye
- **Ortalama Sayfa Geçişi**: < 500ms
- **Bundle Size**: ~2.5MB (gzipped)

---

## 🎯 Gelecek Geliştirmeler

Proje kapsamında planlanmış ama tamamlanmamış özellikler:

- [ ] Mobile app (React Native)
- [ ] Dark mode support
- [ ] Advanced analytics dashboard
- [ ] Machine learning predictions
- [ ] REST API backend
- [ ] Multi-language support (i18n)

---

## 📄 Lisans ve Telif Hakkı

**© 2025-2026 [Önceki İşveren Adı]**

Bu proje, önceki çalıştığım kuruluşta geliştirilmiştir. Tüm fikri mülkiyet hakları ilgili kuruluşa aittir.

**Bu repository:**
- Portfolio amaçlı showcase'dir
- Kaynak kod içermez
- Dağıtım veya ticari kullanım için değildir
- Sadece teknik beceri ve deneyim gösterimi içindir

## 📝 Lisans

**© 2026 Ozan Sert**

Bu proje portfolyo amaçlı geliştirilmiştir. Kaynak kod ve uygulamanın ticari kullanımı için iletişime geçiniz.
- Email: [Your Email]
- GitHub: [@ozansert](https://github.com/ozansert)

---

## 🙏 Teşekkürler

Bu projeyi ziyaret ettiğiniz için teşekkür ederim. Gerçek uygulamayı görmek veya benzer bir proje geliştirmek isterseniz, lütfen benimle iletişime geçin.

---

**Portfolio Showcase** | **Teknik Beceri Gösterimi** | **Enterprise Project Experience**

---

**Monolith Production Manager** | **Enterprise-Level Desktop Application** | **Modern Tech Stack**

*Geliştirme: 2025-2026 | Versiyon: 1.0.