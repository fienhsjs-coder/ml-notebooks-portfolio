# ML Notebooks Portfolio

مجموعه‌ای از پروژه‌های یادگیری ماشین که در طول یادگیری Machine Learning و Deep Learning انجام داده‌ام.

## نوت‌بوک‌ها

### 1. [ml_course_overview.ipynb](notebooks/ml_course_overview.ipynb)
مرور جامع الگوریتم‌های یادگیری ماشین روی دیتاست Breast Cancer:
- الگوریتم‌های کلاسیک: Logistic Regression, KNN, Decision Tree, SVM
- یادگیری بدون ناظر: KMeans, DBSCAN, PCA
- روش‌های Ensemble: Random Forest, AdaBoost
- شبکه عصبی مقدماتی و پیشرفته (Keras/TensorFlow) روی MNIST
- مقایسه چند الگوریتم clustering روی سه دیتاست مختلف (Iris, Wine, Breast Cancer) با معیارهای Silhouette و Davies-Bouldin

### 2. [breast_cancer_classifier_api.ipynb](notebooks/breast_cancer_classifier_api.ipynb)
پایپلاین کامل یک مدل طبقه‌بندی سرطان پستان با Random Forest:
- پیش‌پردازش و استانداردسازی داده
- آموزش و ارزیابی مدل (accuracy, classification report, confusion matrix)
- ذخیره مدل با `joblib`
- سرو کردن مدل با یک API ساده مبتنی بر **FastAPI**
- تحلیل بصری (histogram, boxplot, heatmap, PCA 3D)

### 3. [pca_mnist_exploration.ipynb](notebooks/pca_mnist_exploration.ipynb)
کاوش کامل روی PCA با دیتاست MNIST:
- کاهش بعد و بصری‌سازی سه‌بعدی
- نمودار واریانس تجمعی (explained variance)
- بازسازی تصویر (reconstruction) و تشخیص ناهنجاری (anomaly detection) با خطای بازسازی
- خوشه‌بندی روی فضای کاهش‌یافته
- `IncrementalPCA` برای داده‌های بزرگ
- مقایسه دقت چند مدل classification با و بدون PCA

### 4. [optimizer_comparison_nn.ipynb](notebooks/optimizer_comparison_nn.ipynb)
مقایسه‌ی الگوریتم‌های بهینه‌سازی شبکه عصبی روی دیتاست California Housing:
- مقایسه SGD, Momentum, RMSProp, Adam با Keras
- پیاده‌سازی دستی (from scratch) هر الگوریتم بهینه‌سازی برای درک عمیق‌تر
- بصری‌سازی مسیر بهینه‌سازی روی سطح تابع loss

## نصب و اجرا

```bash
pip install -r requirements.txt
jupyter notebook
```

> نکته: نوت‌بوک `breast_cancer_classifier_api.ipynb` به فایل `data/breast-cancer.csv` نیاز داره (دیتاست عمومی Breast Cancer Wisconsin — از [Kaggle](https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data) قابل دانلوده).

## ساختار پروژه

```
.
├── notebooks/
│   ├── ml_course_overview.ipynb
│   ├── breast_cancer_classifier_api.ipynb
│   ├── pca_mnist_exploration.ipynb
│   └── optimizer_comparison_nn.ipynb
├── data/              # دیتاست‌ها اینجا قرار می‌گیرن (در گیت‌هاب آپلود نشده)
├── requirements.txt
└── README.md
```
