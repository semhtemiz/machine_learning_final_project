
# 🚗 Araç Fiyat Tahmini ve Analizi
Bu proje, araçların özelliklerini kullanarak **araç fiyatlarının tahmin edilmesini** amaçlar. Projede kullanılan yöntemlerle, araçların marka, model, üretim yılı, kilometre, yakıt türü, vites türü gibi özelliklere göre fiyatların belirlenmesi sağlanmıştır.

## 📋 İçindekiler
- [Genel Bakış](#genel-bakış)
- [Kullanılan Teknolojiler](#kullanılan-teknolojiler)
- [Veri Seti Hakkında](#veri-seti-hakkında)
- [Proje Aşamaları](#proje-aşamaları)
  - [Veri Ön İşleme](#veri-ön-işleme)
  - [Görselleştirme](#görselleştirme)
  - [Modelleme](#modelleme)
  - [Performans Sonuçları](#performans-sonuçları)
- [Kurulum ve Çalıştırma](#kurulum-ve-çalıştırma)
- [Sonuçlar ve Çıkarımlar](#sonuçlar-ve-çıkarımlar)
- [Videolu Anlatım](#videolu-anlatım)
- [Katkıda Bulunma](#katkıda-bulunma)
- [Lisans](#lisans)

## 🛠 Genel Bakış
Araç piyasasında fiyat tahmini yapmak hem bireyler hem de işletmeler için önemlidir. Bu projede:
- Veri ön işleme adımları gerçekleştirilmiştir (eksik değerlerin silinmesi, veri temizleme, encoding işlemleri).
- Farklı modellerin performansları karşılaştırılarak en iyi model belirlenmiştir.
- Araç fiyatlarına etki eden özellikler analiz edilmiştir.

## 🔧 Kullanılan Teknolojiler
Bu proje, aşağıdaki Python kütüphaneleri ve araçlarını kullanır:
- **Veri Analizi ve Manipülasyon:** pandas, numpy
- **Veri Görselleştirme:** matplotlib, seaborn
- **Makine Öğrenmesi Modelleri:** scikit-learn
- **Modeller:** 
  - Linear Regression
  - Ridge Regression
  - Lasso Regression
  - Random Forest Regressor
  - Gradient Boosting Regressor
  - K-Nearest Neighbors (KNN)

## 📊 Veri Seti Hakkında
Kullanılan veri seti, araçların şu özelliklerini içerir:
- Marka ve Model
- Üretim Yılı
- Kilometre
- Vites Türü
- Yakıt Türü
- Sahiplik Durumu
- Toplam Fiyat

**Veri Seti Boyutu:** 1084 satır, 10 sütun  
**Özellik Özetleri:** 
- Numerical (Sayısal) ve Categorical (Kategorik) değerlerin birlikte bulunduğu bir yapı.
- Eksik değerler içermekte, ancak temizlenmiştir.

## 🛠 Proje Aşamaları

### Veri Ön İşleme
- Sütunlar Türkçeleştirildi ve okunabilir hale getirildi.
- Eksik ve uygunsuz veriler temizlendi.
- Özelliklerin doğru veri tiplerine dönüştürülmesi sağlandı.
- Kategorik değişkenler **get_dummies** ve **Label Encoding** yöntemleri ile sayısallaştırıldı.
- Yeni özellikler çıkarıldı (örneğin, *araba_adi* sütunu üretim yılı ve marka-model olarak ikiye bölündü).

### Görselleştirme
Aşağıdaki grafikler ile veri seti analizi yapılmıştır:
- Histogram ve Boxplot Grafikleri
- Korelasyon Matrisi (Isı Haritası)
- Özelliklere Göre Fiyat Analiz Grafikleri

### Modelleme
Farklı makine öğrenmesi algoritmaları eğitilmiş ve doğruluk oranlarına göre karşılaştırılmıştır. Kullanılan modeller:
- Linear Regression
- Ridge Regression
- Lasso Regression
- Random Forest
- Gradient Boosting
- KNN

### Performans Sonuçları
Performans metrikleri olarak **MSE**, **RMSE** ve **R² Skoru** kullanılmıştır. Modellerin doğruluk oranları:
- **Gradient Boosting:** %85.98
- **Random Forest:** %78.74
- **KNN:** %65.60
- Diğer regresyon modelleri (%42 civarında düşük performans göstermiştir).

Gradient Boosting, bu veri seti için en iyi sonucu veren modeldir.

## 🚀 Kurulum ve Çalıştırma
1. Bu projeyi yerel makinenize klonlayın:
   ```bash
   git clone https://github.com/semhtemiz/machine_learning_final_project.git
   cd arac-fiyat-tahmini
   ```
2. Gerekli Python kütüphanelerini yüklemek için:
   ```bash
   pip install -r requirements.txt
   ```
3. Projeyi çalıştırmak için:
   ```bash
   python cars.py
   ```

## 🎯 Sonuçlar ve Çıkarımlar
- **Gradient Boosting Regressor**, yüksek doğruluk oranı ile fiyat tahmininde kullanılabilecek en uygun model olarak belirlenmiştir.
- Vites türü ve yakıt türü gibi özelliklerin fiyatlar üzerinde önemli etkileri olduğu gözlenmiştir.
- Veri ön işleme adımları, model performansının iyileştirilmesinde kritik bir rol oynamıştır.


## 🎥 Videolu Anlatım

Proje detayları ve adımları için videomu izleyebilirsiniz:

[Araç Fiyat Tahmini ve Analizi](https://youtu.be/hgDkZAUPybg)

## 🤝 Katkıda Bulunma
Katkıda bulunmak isterseniz:
1. Projeyi fork edin.
2. Yeni bir özellik ekleyin veya hata düzeltin.
3. Bir pull request oluşturun.

## Lisans
Bu proje MIT Lisansı ile korunmaktadır. Daha fazla bilgi için `LICENSE` dosyasını inceleyebilirsiniz.
