## 📱 Uygulama Hakkında

MyAgentApp, kullanıcıların görevlerini, alışkanlıklarını ve önemli etkinliklerini tek bir yerden yönetmelerini sağlayan kapsamlı bir üretkenlik uygulamasıdır. Modern Android geliştirme pratikleri ve Clean Architecture prensiplerine göre geliştirilmiştir.

### ✨ Temel Özellikler

#### 📋 Görev Yönetimi
- **Öncelik Sistemi**: Düşük, Orta, Yüksek, Acil
- **Tarih Aralığı**: Tek tarih veya başlangıç-bitiş aralığı
- **Alt Görevler**: Görevleri parçalara ayırma
- **Akıllı Hatırlatıcılar**: 1 ay önce, 2 hafta önce, 1 hafta önce, 3 gün önce, 1 gün önce, aynı gün
- **Kategori Sistemi**: Kişisel, İş, Sağlık, vb.
- **Sabitleme & Arşivleme**

#### 💪 Alışkanlık Takibi
- **Frekans Tipleri**: Günlük, Haftalık (X gün), Aylık (X gün), Özel
- **Streak Sistemi**: Kesintisiz gün sayısı takibi
- **Görsel Takvim**: GitHub-style tamamlanma geçmişi
- **Günlük Hatırlatıcılar**: Birden fazla hatırlatıcı desteği
- **İstatistikler**: Başarı oranı, toplam tamamlama, en uzun streak

#### 📅 Etkinlik Yönetimi
- **Etkinlik Tipleri**: Doğum Günü, Yıldönümü, Toplantı, Seyahat, Sınav, Randevu
- **Otomatik Yaş Hesaplama**: Doğum günleri için
- **Geri Sayım**: Etkinliğe kalan gün/saat gösterimi
- **Tekrarlama**: Yıllık, Aylık, Haftalık
- **Hatırlatıcılar**: Özelleştirilebilir bildirim zamanları

#### 📝 Not Defteri
- Hızlı not alma
- Kategori bazlı organizasyon
- Arama özelliği

---

## 🏗️ Mimari

Uygulama **Clean Architecture** ve **MVVM** pattern'leri kullanılarak geliştirilmiştir.
```
app/
├── data/
│   ├── local/
│   │   ├── dao/          # Room DAO'ları
│   │   ├── entities/     # Database Entity'leri
│   │   └── AppDatabase   # Room Database
│   ├── preferences/      # SharedPreferences yönetimi
│   └── repository/       # Repository implementasyonları
│
├── domain/
│   ├── model/            # Domain modelleri
│   └── repository/       # Repository interface'leri
│
├── presentation/
│   ├── task/             # Görev ekranları
│   ├── habit/            # Alışkanlık ekranları
│   ├── event/            # Etkinlik ekranları
│   ├── note/             # Not ekranları
│   └── components/       # Paylaşılan UI bileşenleri
│
├── util/                 # Utility sınıfları
├── worker/               # WorkManager worker'ları
└── di/                   # Hilt modülleri
```

---

## 🛠️ Teknolojiler

### **Core**
- **Kotlin** - %100 Kotlin ile geliştirildi
- **Jetpack Compose** - Modern deklaratif UI framework
- **Material Design 3** - Google'ın en yeni tasarım sistemi
- **Coroutines & Flow** - Asenkron programlama

### **Architecture Components**
- **ViewModel** - UI state yönetimi
- **Room** - Yerel veritabanı
- **Navigation Component** - Ekranlar arası geçiş
- **WorkManager** - Arka plan görevleri ve hatırlatıcılar

### **Dependency Injection**
- **Hilt** - Dagger tabanlı DI

### **Diğer**
- **Gson** - JSON serialization/deserialization
- **Material Icons** - UI ikonları

---
