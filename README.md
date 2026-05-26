# House Prices Prediction 🏠

Makine öğrenmesi kullanarak ev fiyatı tahmini yapan bir regresyon projesi.

## Proje Hakkında

Bu proje, Kaggle'ın House Prices veri seti üzerinde veri analizi ve makine öğrenmesi uygulamalarını kapsamaktadır. 1460 ev ve 81 özellik içeren bu veri setinde, evin çeşitli özelliklerine bakarak satış fiyatını tahmin etmek amaçlanmıştır.

## Kullanılan Teknolojiler

- Python 3
- NumPy
- Pandas
- Scikit-learn

## Proje Adımları

### 1. Veri Analizi
- Veri setinin genel yapısını inceleme: 1460 satır, 81 sütun
- Eksik verileri tespit etme

### 2. Veri Temizleme
- %50'den fazla eksik verisi olan 5 sütunu silme (Alley, PoolQC, Fence vb.)
- Sayısal sütunları ortalama ile doldurma
- Yazısal sütunları en sık geçen değerle doldurma
- One-hot encoding ile yazısal sütunları sayıya çevirme (81 → 273 sütun)

### 3. Model Eğitimi

| Model | Sonuç |
|---|---|
| Random Forest Regressor | Ortalama 18.200$ hata |
| Ortalama ev fiyatına göre hata oranı | **%10** ✅ |

## Sonuç

Model, ortalama ev fiyatı 180.921$ olan bu veri setinde yaklaşık %10 hata ile tahmin yapıyor. Bu, ilk model denemesi için oldukça başarılı bir sonuç.

## Nasıl Çalıştırılır

```bash
pip install numpy pandas scikit-learn jupyter
jupyter notebook
```

Kaggle'dan `train.csv` dosyasını indirip proje klasörüne ekleyin.

## Öğrendiklerim

- Regresyon ile sınıflandırma arasındaki fark
- Çok sayıda eksik sütunu verimli şekilde temizleme
- One-hot encoding nedir ve neden kullanılır
- Mean Absolute Error ile model performansı ölçme
