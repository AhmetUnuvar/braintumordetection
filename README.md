# 🧠 Brain Tumor Detection and Segmentation using Deep Learning

Bu proje, beyin MR görüntülerini kullanarak tümör tespiti ve segmentasyonu yapan bir derin öğrenme sistemini içermektedir. Model, sınıflandırma için **ResNet50**, segmentasyon için **ResUNet** mimarilerini kullanmaktadır. 

## 🚀 Projenin Amacı

- Beyin MR görüntülerinde **tümörün varlığını tespit etmek**.
- Tümör pozitif olan MR'larda **tümör bölgesini segment (ayırmak)**.
- Görselleştirme ile modelin tahminlerini kullanıcıya sunmak.

## 🧰 Kullanılan Teknolojiler

| Teknoloji | Açıklama |
|----------|----------|
| Python | Ana programlama dili |
| TensorFlow / Keras | Derin öğrenme modelleri |
| OpenCV & skimage | Görüntü işleme |
| Matplotlib & Seaborn | Görselleştirme |
| ResNet50 | Transfer öğrenme tabanlı sınıflandırma |
| ResUNet | Tümör segmentasyonu |
| Focal Tversky Loss | Segmentasyon için özel loss fonksiyonu |
| Google Colab | Geliştirme ortamı |

## 📂 Proje Yapısı

├── data_mask.csv # Görüntü ve maskelerin yolları
├── classifier-resnet-model.json
├── classifier-resnet-weights.keras
├── ResUNet-model.json
├── ResUNet-weights.keras
├── brain_tumor_guncel_model.keras
├── utilities.py # Kendi yazdığımız yardımcı fonksiyonlar (loss, generator vb.)
├── healthcare_ai_(1).py # Proje kodlarının tamamı


## 📊 Model Performansı

- **Sınıflandırma Modeli (ResNet50)**
  - Accuracy: ~`%X` *(test set üzerinden hesaplandı)*
  - Confusion Matrix ve Classification Report detayları projede mevcuttur.

- **Segmentasyon Modeli (ResUNet)**
  - Custom loss: `Focal Tversky`
  - Metric: `Tversky Index`
  - Model başarıyla maskeleri tahmin edip görselleştirmektedir.

## 📸 Örnek Tahminler

Model, aşağıdaki gibi görseller üretmektedir:

- MRI
- Gerçek Maske (Ground Truth)
- Tahmin Edilen Maske
- Gerçek Maskeli MRI
- Yapay Zeka ile Maskelenmiş MRI


## 🛠️ Nasıl Kullanılır?

1. `data_mask.csv` ile görüntü ve mask yollarını belirleyin.
2. `utilities.py` dosyasında bulunan fonksiyonlar destekleyici olarak kullanılır.
3. Aşağıdaki dosyaları Google Colab veya Jupyter Notebook üzerinde çalıştırabilirsiniz:
   - `healthcare_ai_(1).py`

4. Model eğitildikten sonra `.keras` ve `.json` formatında kaydedilir.

5. Test etmek için kullanıcıdan `.jpg` dosyası alınır ve sınıflandırma sonucu gösterilir.

## 👩‍⚕️ Uygulama Alanları

- Radyolojik görüntü analizi
- Sağlık teknolojileri projeleri
- Klinik karar destek sistemleri
- Medikal yapay zeka çözümleri

