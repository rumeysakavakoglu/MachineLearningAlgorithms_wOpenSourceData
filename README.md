# HepsiEmlak ML Pipeline

Data cleaning and machine learning experiments on Turkish real estate listings collected from **HepsiEmlak**.  
This project was developed by a **10-person team** with a strong emphasis on **data preprocessing**, feature engineering, and predictive modeling for property type and price estimation.

Contributors: Esma Kara, Dilara Top, Hayrunnisa Yılmaz,Rumeysa Kavakoğlu, Esra Özden, Ebrar Mert
---

## 📊 Project Overview
- **Dataset size:** 2,180 rows × 135 columns  
- **Final cleaned dataset:** 57 columns (up to **87 features** after encoding)  
- **Teamwork:** Each member worked on a subset of columns, with weekly meetings for sharing insights and aligning methodologies.  
- **Main focus:** Data preparation, feature engineering, and applying multiple ML models for classification and regression tasks.  

---

## 🧹 Data Preparation
The most time-consuming and critical phase of the project was **data cleaning**. Steps included:

- **Column elimination:**  
  - Removed columns with >95% missing values  
  - Removed columns containing only `0`/`1`  
  - Removed columns with a single constant string value  

- **Distributed feature analysis:**  
  Each member handled ~7 columns to ensure thorough cleaning and preprocessing.  

- **Data cleaning & transformation:**  
  - Filled missing values using:
    - Information extracted from the `description` field  
    - Derived values from correlated columns  
    - Custom prediction functions for specific attributes  
  - Split multi-valued columns into multiple features  
  - Extracted meaningful data from HTML tags  
  - Created new engineered features, e.g.:
    - Distance to city center  
    - Distance to sea  
    - Numerical floor ranking system
    - ...
  - Corrected contradictory or incorrect entries  
  - Outlier detection and adjustments  

- **Encoding:**  
  Since most ML algorithms require numerical input, categorical variables were encoded, raising the total number of features to **87**.  

- **Overfitting prevention:**  
  Columns that led to overfitting during model training were **excluded from the final feature set** to improve generalization.  

---

## 🤖 Modeling Scenarios
We implemented ML models in **three main scenarios**:

1. **Property Type Prediction (Classification)**  
   - Algorithms: Random Forest, Logistic Regression  
   - Techniques: SMOTE, GridSearchCV, SelectKBest, PCA, Cross-Validation  
   - Evaluation: Performance metrics & learning curves  

2. **Price Prediction – Categorical (Classification by price ranges)**  
   - Algorithms: Random Forest, XGBoost, LightGBM, Decision Tree  
   - Techniques: GridSearchCV, RandomizedSearchCV  
   - Evaluation: Metrics & learning curves  

3. **Price Prediction – Numerical (Regression)**  
   - Algorithms: Linear Regression, CART, Random Forest, LightGBM  
   - Techniques: Feature Selection (SelectKBest, RFE), Correlation Analysis, Log Transformation, GridSearchCV, RandomizedSearchCV, Cross-Validation  
   - Evaluation: Metrics & learning curves  

---

## 🛠️ Technologies Used
- **Languages & Libraries:** Python, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, XGBoost, LightGBM  
- **Collaboration:** Version control & teamwork (10 members)  
- **Approach:** Iterative cleaning, feature engineering, and ML experiments  

---

# What we are asked for?
[Veri Madenciliği Dönem Proje İsterleri.docx](https://github.com/user-attachments/files/22122002/Veri.Madenciligi.Donem.Proje.Isterleri.docx) (in Turkish)

## Project Report 
[Rapor.docx](https://github.com/user-attachments/files/22122039/Rapor.docx) (in Turkish)



---

## 🇹🇷 Türkçe Versiyon

# HepsiEmlak ML Pipeline

**HepsiEmlak** üzerinden toplanan Türkçe emlak ilanları üzerinde veri temizleme ve makine öğrenmesi çalışmaları.  
Bu proje, **10 kişilik bir ekip** tarafından geliştirilmiş olup, özellikle **veri ön işleme**, özellik mühendisliği ve konut tipi ile fiyat tahmini için makine öğrenmesi modellerine odaklanmaktadır.

---

## 📊 Proje Özeti
- **Veri seti boyutu:** 2.180 satır × 135 sütun  
- **Temizlenmiş nihai veri seti:** 57 sütun (**encoding sonrası 87 özellik**)  
- **Ekip çalışması:** Her üye belirli sütunları üstlenerek üzerinde çalıştı, haftalık toplantılar ile fikir paylaşımı ve yöntem birliği sağlandı.  
- **Ana odak:** Veri hazırlığı, özellik mühendisliği ve sınıflandırma/regresyon görevleri için ML modellerinin uygulanması.  

---

## 🧹 Veri Hazırlama
Projenin en zaman alıcı ve kritik aşaması **veri temizleme** olmuştur. Adımlar şunlardır:

- **Sütun elemesi:**  
  - %95’ten fazla eksik değer içeren sütunlar kaldırıldı  
  - Sadece `0` veya `1` değerinden oluşan sütunlar kaldırıldı  
  - Sadece tek bir sabit string değeri içeren sütunlar kaldırıldı  

- **Dağıtılmış özellik analizi:**  
  Her ekip üyesi yaklaşık 7 sütun üzerinde çalışarak detaylı temizlik yaptı.  

- **Veri temizleme & dönüştürme:**  
  - Eksik veriler dolduruldu:
    - `description` sütunundan çıkarılan bilgilerle
    - İlişkili sütunlardan elde edilen verilerle
    - Özel tahmin fonksiyonları kullanılarak
    - Birden fazla veri içeren sütunlar ayrılarak yeni sütunlar oluşturuldu  
  - HTML tag’leri içerisindeki faydalı veriler çıkarıldı  
  - Yeni özellikler oluşturuldu, örn.:
    - Merkeze uzaklık
    - Denize uzaklık
    - Kat bilgisi sayısal derecelendirme
    - ...
  - Çelişkili ve hatalı bilgiler düzeltildi  
  - Aykırı değerler tespit edilerek düzenlendi  

- **Encoding:**  
  Çoğu ML algoritması sayısal veri gerektirdiğinden kategorik değişkenler encode edilerek toplam özellik sayısı **87’ye** çıktı.  

- **Overfitting önleme:**  
  Model eğitiminde aşırı uyuma yol açan sütunlar **kullanılmayarak** genelleme başarısı artırıldı.  

---

## 🤖 Modelleme Senaryoları
Projede **üç temel senaryo** uygulanmıştır:

1. **Konut Tipi Tahmini (Sınıflandırma)**  
   - Algoritmalar: Random Forest, Lojistik Regresyon  
   - Teknikler: SMOTE, GridSearchCV, SelectKBest, PCA, Cross-Validation  
   - Değerlendirme: Performans metrikleri & öğrenme eğrileri  

2. **Fiyat Tahmini – Kategorik (Fiyat aralıklarına göre sınıflandırma)**  
   - Algoritmalar: Random Forest, XGBoost, LightGBM, Decision Tree  
   - Teknikler: GridSearchCV, RandomizedSearchCV  
   - Değerlendirme: Metrikler & öğrenme eğrileri  

3. **Fiyat Tahmini – Sayısal (Regresyon)**  
   - Algoritmalar: Linear Regression, CART, Random Forest, LightGBM  
   - Teknikler: Özellik seçimi (SelectKBest, RFE), Korelasyon Analizi, Logaritmik Dönüşüm, GridSearchCV, RandomizedSearchCV, Cross-Validation  
   - Değerlendirme: Metrikler & öğrenme eğrileri  

---

## 🛠️ Kullanılan Teknolojiler
- **Diller & Kütüphaneler:** Python, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, XGBoost, LightGBM  
- **Ekip çalışması:** Versiyon kontrolü & ortak çalışma (10 kişi)  
- **Yaklaşım:** Tekrarlamalı temizlik, özellik mühendisliği ve ML deneyleri  
