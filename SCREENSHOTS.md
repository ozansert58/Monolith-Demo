# 📸 Ekran Görüntüleri ve Mockup'lar

> **Not**: Gerçek ekran görüntüleri telif hakları nedeniyle bu portfolio showcase'de paylaşılamamıştır.  
> Aşağıda, projenin temel ekranlarına dair açıklamalar ve genel yapı bilgileri yer almaktadır.

---

## 🏠 Dashboard (Ana Panel)

### Açıklama
Dashboard, kullanıcının sistemde oturum açtıktan sonra karşılaştığı ilk ekrandır. Üretim süreçlerine dair özet bilgileri ve hızlı erişim butonlarını içerir.

### Bileşenler
- **Header**: Logo, kullanıcı profili, bildirimler
- **KPI Cards**: 
  - Toplam aktif iş emri sayısı
  - Günlük tamamlanan iş sayısı
  - Geciken işler
  - Ortalama tamamlanma süresi
- **Chart Widgets**:
  - Haftalık üretim grafiği (line chart)
  - Durum dağılımı (pie chart)
  - Trend analizi
- **Quick Actions**: Hızlı iş emri oluşturma, rapor alma
- **Recent Activities**: Son işlemler listesi

### Teknik Detaylar
- React functional components
- Real-time data updates via Firebase listeners
- Responsive grid layout
- Chart.js / Recharts for visualizations

---

## 🏭 Üretim Takip Ekranı

### Açıklama
İş emirlerinin oluşturulduğu, düzenlendiği ve takip edildiği ana çalışma ekranıdır.

### Bileşenler
- **Kanban Board**:
  - Sütunlar: Açık, Devam Ediyor, Beklemede, Tamamlandı
  - Sürükle-bırak (drag & drop) özelliği
  - Renk kodlaması (öncelik ve duruma göre)
  
- **İş Emri Kartı**:
  - İş emri numarası
  - Ürün adı ve görseli
  - Sorumlu kişi
  - Termin tarihi
  - İlerleme yüzdesi
  - QR kod (hızlı erişim için)

- **Filtre ve Arama**:
  - Durum filtreleme
  - Tarih aralığı
  - Sorumlu kişi
  - Öncelik seviyesi

- **Detay Modal**:
  - Malzeme listesi
  - İşlem geçmişi
  - Dosyalar ve resimler
  - Notlar ve yorumlar

### Teknik Detaylar
- React DnD (Drag and Drop) library
- Modal components
- Infinite scroll / pagination
- Filter state management

---

## 👥 Kullanıcı Yönetimi

### Açıklama
Sistem yöneticilerinin kullanıcı hesaplarını ve yetkilerini yönettiği ekran.

### Bileşenler
- **Kullanıcı Tablosu**:
  - Kullanıcı adı, email, rol
  - Durum (aktif/pasif)
  - Son giriş tarihi
  - İşlem butonları (düzenle, sil)

- **Rol Yönetimi**:
  - Roller: Admin, Manager, Operator, Viewer
  - Yetki matrisi
  - Modül bazlı erişim kontrolü

- **Kullanıcı Ekleme/Düzenleme Formu**:
  - Temel bilgiler
  - Rol ataması
  - Departman seçimi
  - Şifre yönetimi

- **Aktivite Logları**:
  - Kullanıcı işlemleri
  - Değişiklik geçmişi
  - Filtrelenebilir tablo

### Teknik Detaylar
- Form validation (Formik / React Hook Form)
- Table component with sorting/filtering
- Role-based UI rendering
- Audit trail implementation

---

## 📊 Raporlama Ekranı

### Açıklama
Çeşitli raporların oluşturulduğu ve dışa aktarıldığı ekran.

### Bileşenler
- **Rapor Şablonları**:
  - Üretim raporu
  - Malzeme tüketim raporu
  - Çalışan performans raporu
  - Gecikme analizi

- **Filtre Paneli**:
  - Tarih aralığı seçici (date picker)
  - Departman/takım seçimi
  - Durum filtreleri
  - Özel filtreler

- **Önizleme**:
  - Tablo görünümü
  - Grafik önizleme
  - Özet istatistikler

- **Export Butonları**:
  - Excel (.xlsx)
  - PDF
  - CSV
  - Print

### Teknik Detaylar
- jsPDF for PDF generation
- xlsx library for Excel export
- Date range picker component
- Print-friendly CSS

---

## 📦 Malzeme ve Envanter Ekranı

### Açıklama
Malzeme listesinin ve stok durumlarının görüntülendiği ekran.

### Bileşenler
- **Malzeme Tablosu**:
  - Malzeme kodu ve adı
  - Kategori
  - Mevcut stok
  - Birim fiyat
  - Tedarikçi
  - Durum göstergesi (yetersiz stok uyarısı)

- **Stok Hareketleri**:
  - Giriş/çıkış kayıtları
  - Tarih ve miktar
  - İlgili iş emri

- **Malzeme Detay Paneli**:
  - Teknik özellikler
  - Resimler ve dokümanlar
  - Fiyat geçmişi
  - Tedarikçi bilgileri

- **Sipariş Yönetimi**:
  - Otomatik sipariş önerileri
  - Sipariş oluşturma formu
  - Sipariş takibi

### Teknik Detaylar
- Real-time stock updates
- Low stock alerts
- Barcode scanning integration
- File upload for documents

---

## ⚙️ Ayarlar Ekranı

### Açıklama
Uygulama ayarlarının yapılandırıldığı ekran.

### Bileşenler
- **Genel Ayarlar**:
  - Dil seçimi
  - Tema (açık/koyu mod)
  - Bildirim tercihleri
  - Zaman dilimi

- **Hesap Ayarları**:
  - Profil bilgileri
  - Şifre değiştirme
  - 2FA aktifleştirme
  - Oturum yönetimi

- **Sistem Ayarları** (Admin):
  - Veritabanı yedekleme
  - Log görüntüleme
  - Sistem bilgileri
  - Güncelleme kontrolü

- **Entegrasyon Ayarları**:
  - OneDrive bağlantısı
  - Azure AD yapılandırması
  - API anahtarları
  - Webhook ayarları

### Teknik Detaylar
- Settings persistence (LocalStorage + Firebase)
- Password strength validator
- Two-factor authentication setup
- API key management

---

## 🔐 Login & Authentication Ekranları

### Açıklama
Kullanıcı giriş ve kimlik doğrulama ekranları.

### Ekranlar

#### 1. Login Screen
- Email/password form
- "Beni hatırla" checkbox
- "Şifremi unuttum" linki
- Google / Microsoft SSO butonları
- Kayıt ol linki (eğer kayıt açıksa)

#### 2. Microsoft Login Screen
- Azure AD redirect
- Organization login
- Consent screen
- Success/error handling

#### 3. Password Reset
- Email input
- Reset link gönderimi
- Confirmation message

#### 4. Two-Factor Authentication
- OTP input
- QR code (ilk kurulum için)
- Backup codes

### Teknik Detaylar
- Firebase Authentication
- MSAL (Microsoft Authentication Library)
- JWT token management
- Secure storage

---

## 📱 QR Kod ve Barkod Ekranları

### Açıklama
QR kod üretimi ve okuma işlemlerinin yapıldığı ekranlar.

### Bileşenler
- **QR Kod Üretici**:
  - İçerik girişi (iş emri, ürün, vb.)
  - Boyut ve renk ayarları
  - Logo ekleme
  - İndirme butonları (PNG, SVG)

- **Barkod Okuyucu**:
  - Kamera görünümü
  - Tarama çerçevesi
  - Otomatik odaklama
  - Okuma sonucu gösterimi

- **Tarama Geçmişi**:
  - Son taranan kodlar
  - Tarih ve zaman damgası
  - İlgili iş emri bilgisi
  - Konum (eğer izin verilmişse)

### Teknik Detaylar
- qrcode.js for QR generation
- jsQR or ZXing for scanning
- Camera API access
- Canvas manipulation

---

## 🔔 Bildirim ve Uyarı Sistemleri

### Açıklama
Kullanıcılara gösterilen bildirim ve uyarı mesajları.

### Tipler
- **Toast Notifications**:
  - Başarılı işlem (yeşil)
  - Hata mesajı (kırmızı)
  - Uyarı (sarı)
  - Bilgi (mavi)

- **System Notifications**:
  - Yeni iş emri ataması
  - Termin tarihi yaklaşıyor
  - Stok seviyesi düşük
  - Sistem güncellemesi mevcut

- **Modal Alerts**:
  - Onay gerektiren işlemler
  - Kritik uyarılar
  - Bilgilendirme mesajları

### Teknik Detaylar
- Toast library (react-toastify)
- Electron native notifications
- Firebase Cloud Messaging (planned)
- Priority-based notification queue

---

## 🖼️ Görsel Tasarım Özellikleri

### Renk Paleti
```
Primary: #667eea (Mor-Mavi)
Secondary: #764ba2 (Mor)
Success: #10b981 (Yeşil)
Warning: #f59e0b (Turuncu)
Error: #ef4444 (Kırmızı)
Info: #3b82f6 (Mavi)
Background: #f9fafb (Açık Gri)
Text: #1f2937 (Koyu Gri)
```

### Typography
```
Headings: Inter, sans-serif
Body: -apple-system, BlinkMacSystemFont, "Segoe UI"
Monospace: 'Courier New', monospace
```

### Layout
- Grid-based responsive design
- 8px spacing units
- Consistent padding/margins
- Card-based UI components

---

**Not**: Bu ekranlar, projenin genel yapısını göstermek amacıyla tanımlanmıştır. Gerçek tasarımlar ve ekran görüntüleri telif hakları nedeniyle paylaşılmamıştır.

---

## 📷 Placeholder İmages

Gerçek ekran görüntüleri yerine aşağıdaki placeholder'lar kullanılabilir:

```
/screenshots/
├── dashboard-placeholder.png
├── production-placeholder.png
├── users-placeholder.png
├── reports-placeholder.png
└── materials-placeholder.png
```

*Bu görseller için [Unsplash](https://unsplash.com) veya [UI Design Daily](https://uidesigndaily.com) gibi kaynaklardan benzer arayüz örnekleri kullanılabilir.*

---

*© 2026 Portfolio Showcase - Screenshots & Mockups Documentation*
