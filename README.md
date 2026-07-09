# Kalp Hastalığı Verisi - Ön İşleme ve Veri Kalitesi Analizi

Bu depo, dört kişilik bir akademik veri madenciliği projesindeki **kişisel katkım olan veri ön işleme ve veri kalitesi çalışmalarını** içermektedir. Projenin genel amacı, klinik değişkenlerden yararlanarak kalp hastalığı riskini farklı makine öğrenmesi yaklaşımlarıyla incelemektir.

## Projedeki Katkım

- 1.025 satırlık ham veri setindeki kopya kayıtları analiz ettim.
- 723 kopya kaydı kaldırarak analizlerin 302 benzersiz kayıt üzerinde yürütülmesini sağladım.
- Kolesterol (`chol`) ve dinlenme kan basıncı (`trestbps`) alanlarındaki tıbben anlamsız sıfır değerlerini inceledim ve medyan ile doldurma yaklaşımını uyguladım.
- Kategorik değişkenler için one-hot encoding, sayısal değişkenler için ölçeklendirme adımlarını hazırladım.
- Sınıf dağılımı, korelasyon ve keşifsel veri analizi görsellerini oluşturdum.
- Ekipte geliştirilen modellerin aynı temizlenmiş veri üzerinde değerlendirilebilmesi için ortak veri dosyasını hazırladım.
- Teknik raporlama ve proje koordinasyonu süreçlerine katkı sağladım.

## Veri İşleme Özeti

| Aşama | Sonuç |
|---|---:|
| Ham veri | 1.025 satır |
| Kopya kayıt | 723 satır |
| Temizlenmiş veri | 302 benzersiz satır |
| Ham değişken sayısı | 14 |
| İşlenmiş değişken sayısı | 19 |

## Kullanılan Teknolojiler

Python, pandas, NumPy, Matplotlib, Seaborn, scikit-learn ve Jupyter Notebook.

## Proje Yapısı

```text
.
├── data/
│   ├── heart.csv
│   └── heart_FINAL_VERSION.csv
├── notebooks/
│   └── veri_on_isleme.ipynb
├── requirements.txt
├── .gitignore
└── README.md
```

## Çalıştırma

Sanal ortam oluşturun ve etkinleştirin:

```bash
python -m venv .venv
.venv\Scripts\activate
```

Gerekli paketleri yükleyin:

```bash
pip install -r requirements.txt
```

Ardından Jupyter Notebook'u başlatın:

```bash
jupyter notebook
```

`notebooks/veri_on_isleme.ipynb` dosyasını açıp hücreleri sırayla çalıştırın.

## Akademik Proje Bağlamı

Projenin tamamında Lojistik Regresyon, Random Forest ve Bayesian Network yöntemleri ekip üyeleri tarafından değerlendirilmiştir. Bu depo yalnızca benim sorumluluğum olan veri ön işleme ve veri kalitesi çalışmalarına odaklanmaktadır.

**Hazırlayan:** Büşra Demirkıran  
**Bölüm:** Bartın Üniversitesi Bilgisayar Mühendisliği
