# CTRL IS HERS – Assessment 1 (ML)

Xəbər məqalələrinin xüsusiyyətləri əsasında `target` dəyişənini proqnozlaşdıran ikili təsnifat (binary classification) layihəsi.

## Fayllar

- `CTRL_IS_HERS_ASSESSMENT_1.ipynb` – bütün iş (EDA, preprocessing, modellər, submission)
- `requirements.txt` – lazım olan kitabxanalar

`train.csv` və `test.csv` repoya daxil deyil. Onları notebook ilə eyni qovluğa qoyun.

## Nə edilib

1. Data 80% train və 20% test-ə bölündü (əvvəlcə bölünüb, sonra EDA və preprocessing edilib).
2. Train datası üzərində EDA aparıldı.
3. Preprocessing: boş dəyərlərin doldurulması, qeyri-simmetrik sütunlara `log1p`, miqyaslama, kateqoriyalı sütunlara one-hot encoding.
4. 9 model müqayisə edildi: Logistic Regression, kNN, SVM, Decision Tree, Random Forest, Gradient Boosting, XGBoost, LightGBM, CatBoost.
5. Metrikalar: Accuracy, Precision, Recall, F1, ROC-AUC.
6. CatBoost modeli ilə `test.csv` üçün ehtimallar proqnozlaşdırıldı və `submission.csv` faylı yaradıldı.

## Necə işlədilir

```bash
pip install -r requirements.txt
jupyter notebook CTRL_IS_HERS_ASSESSMENT_1.ipynb
```

Qeyd: notebook train faylını `/content/train.csv` yolundan oxuyur (Google Colab). Lokal işlədirsinizsə, yolu `train.csv` ilə əvəz edin.

## Nəticə

`submission.csv` faylı iki sütundan ibarətdir: `id` və `predicted_probability`.
