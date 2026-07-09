# Kalp Hastalığı Verisi: Ön İşleme ve Veri Kalitesi Analizi

Bu depo, dört kişilik akademik bir veri madenciliği projesindeki kişisel katkım olan **veri ön işleme ve veri kalitesi çalışmalarını** içermektedir.

Projenin genel amacı, klinik değişkenleri kullanarak kalp hastalığı riskini farklı makine öğrenmesi yöntemleriyle incelemektir. Bu depo yalnızca veri hazırlama sürecine odaklanmaktadır.

## Kişisel Katkılarım

- 1.025 satırlık ham veri setindeki tekrar kayıtları analiz ettim.
- 723 tekrar kaydı kaldırarak 302 benzersiz kayıt elde ettim.
- Veri şeması ve alan kurallarına ilişkin kalite kontrolleri oluşturdum.
- `chol` ve `trestbps` alanlarındaki sıfır değerleri koşullu olarak denetleyen temizleme adımını hazırladım.
- `ca` ve `thal` alanlarındaki eksik/bilinmeyen kodları düzenledim.
- Sınıf dağılımı ve korelasyon analizlerini oluşturdum.
- Modelleme dönüşümlerinin yalnızca eğitim verisine uygulanmasını sağlayan, veri sızıntısını önleyici bir ön işleme örneği hazırladım.
- Teknik raporlama ve proje koordinasyonuna katkı sağladım.

## Veri İşleme Özeti

| Aşama | Sonuç |
|---|---:|
| Ham veri | 1.025 satır |
| Tekrar kayıt | 723 satır |
| Temiz veri | 302 benzersiz satır |
| Değişken sayısı | 14 |

## Yapılan Metodolojik Düzeltmeler

- Ölçeklendirme, veri eğitim/test olarak ayrılmadan önce uygulanmamaktadır.
- Eğitim/test ayrımında hedef sınıf oranlarını korumak için `stratify` kullanılmaktadır.
- Model geliştirme kodları bu depodan çıkarılmıştır; depo yalnızca kişisel veri ön işleme katkısını göstermektedir.
- Ham veride bulunmayan sıfır değerleri yapay olarak oluşturulmamaktadır.
- Temiz veri, modelden bağımsız kullanım için ölçeklenmeden kaydedilmektedir.

## Dosyalar

```text
.
├── heart.csv
├── heart_cleaned.csv
├── veri_on_isleme.ipynb
├── requirements.txt
├── .gitignore
└── README.md
```

- `heart.csv`: Ham veri seti
- `heart_cleaned.csv`: Tekrarları ve alan kodu sorunları düzenlenmiş temiz veri
- `veri_on_isleme.ipynb`: Çalıştırılmış ve doğrulanmış veri ön işleme notebook'u

## Kurulum

```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook
```

Ardından `veri_on_isleme.ipynb` dosyasını açıp hücreleri sırayla çalıştırın.

## Akademik Proje Bağlamı

Projenin tamamında Lojistik Regresyon, Random Forest ve Bayesian Network yöntemleri ekip üyeleri tarafından değerlendirilmiştir. Bu depo yalnızca veri ön işleme ve veri kalitesi çalışmalarıma odaklanmaktadır.

> Bu çalışma eğitim amaçlıdır ve klinik tanı amacıyla kullanılmamalıdır.

**Hazırlayan:** Büşra Demirkıran  
**Bölüm:** Bartın Üniversitesi Bilgisayar Mühendisliği
