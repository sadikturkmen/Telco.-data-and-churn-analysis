# 📊 Müşteri Churn Tahmini – Telco Customer Churn Analysis

Bu proje, bir telekomünikasyon şirketinin müşterilerinin hizmeti bırakıp bırakmayacağını (churn) tahmin etmek amacıyla hazırlanmıştır. Python kullanılarak veri temizleme, özellik mühendisliği, görselleştirme ve makine öğrenmesi uygulamaları yapılmıştır.

## Proje Amacı

Müşteri kaybı (churn) şirketler için büyük maliyetler oluşturabilir. Bu proje, müşteri davranışlarını analiz ederek churn riskini önceden tahmin etmeyi ve şirketin erken aksiyon almasına yardımcı olmayı hedeflemektedir.

## Kullanılan Veri Seti

- Veri kümesi: [Telco Customer Churn Dataset](https://www.kaggle.com/blastchar/telco-customer-churn)
- Gözlem sayısı: 7043
- Özellik sayısı: 20+ (kategorik + sayısal)

## Kullanılan Teknolojiler

- Python
- pandas, numpy
- seaborn, matplotlib
- scikit-learn

## Uygulanan Adımlar

### 1. Veri Ön İşleme
- Eksik değerlerin temizlenmesi
- `TotalCharges` sütununun float’a çevrilmesi
- Gerekli encoding işlemleri (`pd.get_dummies`)

### 2. Özellik Mühendisliği
- `AvgMonthlyCharge = TotalCharges / tenure`
- `TotalServices` → aktif hizmet sayısı
- `class_weight='balanced'` ile model ağırlıklandırması

### 3. Görselleştirme (EDA)
- `Contract`, `InternetService`, `MonthlyCharges` vs `Churn` ilişkileri incelendi
- heatmap, boxplot, histogram kullanıldı

### 4. Modelleme
- Logistic Regression
- K-Nearest Neighbors (KNN)
- Model performansları karşılaştırıldı (accuracy, precision, recall, f1-score)

## 🔍 Model Performans Özeti

| Model               | Accuracy | Recall (Churn=1) | F1-score (Churn=1) |
|---------------------|----------|------------------|--------------------|
| Logistic Regression | 0.73     | **0.79**         | 0.61               |
| KNN (k=5)           | 0.75     | 0.53             | 0.53               |

## 📈 Çıkarımlar

- `Contract`, `InternetService` ve `MonthlyCharges` gibi değişkenler churn üzerinde yüksek etkiye sahiptir.
- Logistic Regression, churn tahmini için daha dengeli bir sonuç vermiştir.
- Özellik mühendisliği ile modelin duyarlılığı artırılmıştır.

## 🧑‍💻 Geliştiren

- [Muhammed Sadık TURKMEN]  
- Üniversite: [Yıldız Teknik Üniversitesi]  
- Bölüm: İstatistik  
- Amaç: Veri analizi ve makine öğrenmesi yeteneklerimi geliştirmek
