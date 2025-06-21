# Wind Turbine

## 📌 Proje Özeti

**Wind Turbine**, Bu proje, hava durumu verilerini kullanarak gelecekteki hava sıcaklığını tahmin etmek için bir LSTM (Long Short-Term Memory) derin öğrenme modeli geliştirmeyi amaçlamaktadır.

## 🌟 Amaç
Meteorolojik istasyonlardan alınan gerçek zamanlı verileri kullanarak:
* Kısa vadeli hava sıcaklığı tahminleri yapmak (5-30 dakika sonrası)
* Hava sıcaklığındaki değişimleri önceden tahmin ederek enerji yönetimi sistemlerine destek sağlamak
* Tarım, ulaşım ve acil durum yönetimi gibi alanlarda karar destek sistemi olarak kullanılabilecek bir model geliştirmek

## 🧠 Kullanılan Teknolojiler

* **Python** – 3.10+
* **TensorFlow/Keras** – Derin öğrenme modeli geliştirme
* **Pandas/NumPy** – Veri işleme ve analiz
* **Scikit-learn** – Veri ön işleme ve metrikler
* **Joblib** – Model ve scaler kaydetme


## 📁 Veri Hazırlığı

* **Eksik veri analizi** - Her sütundaki NaN oranlarının hesaplanması
* Yüksek NaN oranlı sütunların çıkarılması
* **Zaman serisi interpolasyonu** - Eksik değerlerin zaman ekseninde lineer interpolasyonla doldurulması
* **Medyan doldurma** - Kalan eksik değerlerin sütun medyanlarıyla doldurulması
* Etiket koordinatları görselleştirilerek kontrol sağlandı.
* **Z-Score analizi** - Sürekli değişkenlerde aykırı değerlerin tespiti
* **3 standart sapma eşiği** - |Z-Score| > 3 olan değerlerin veri setinden çıkarılması

## 📸 Çalışma Mantığı

1. **Zaman serisi formatı** - 6 zaman adımlı (30 dakikalık) geçmiş veriler
2. **Sıralı öğrenme** - LSTM katmanları zaman içindeki bağımlılıkları öğrenir
3. **Özellik ilişkileri** - Sıcaklık, nem, rüzgar gibi değişkenler arasındaki karmaşık ilişkilerin modellenmesi
4. **Tahmin** - Bir sonraki zaman adımındaki (5 dakika sonraki) hava sıcaklığının tahmini

## 📊 Örnek Çıktı

* **R² Skoru** - 0.9870



