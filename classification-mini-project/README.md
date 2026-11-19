# Порівняння класичних моделей класифікації
## Постановка задачі
Задача класифікації на наявність захорювання. Позитивний клас - хворий
## Набір даних
heart_disease, 303 об’єктів, числові та категоріальні ознаки, цільова змінна - target (1 - позитина, 0 - негатина)>
## Методика експерименту
- фіксований train/test split;
- підбір лише на train;
- StratifiedKFold;
- одноразове фінальне оцінювання на test.
## Підготовка даних
- SimpleImputer;
- StandardScaler;
- OneHotEncoder;
- ColumnTransformer;
- Pipeline.
## Досліджені моделі
- Logistic Regression;
- k-NN;
- Gaussian Naive Bayes;
- LDA;
- QDA;
- SVM.
## Порівняння за крос-валідацією
| Модель | CV F1 | CV Recall | CV ROC AUC |
|---|---:|---:|---:|
| Logistic Regression (`C=7, penalty=L1`) | 0.8371 | 0.8103 | 0.9019 |
| k-NN (`k=3, euclidean`) | 0.8042 | 0.8008 | 0.8709 |
| Gaussian Naive Bayes | 0.7495 | 0.8458 | 0.8773 |
| LDA | 0.8128 | 0.7656 | 0.8993 |
| QDA (`reg_param=0.1`) | 0.7962 | 0.7743 | 0.8680 |
| SVM (`C=10, gamma=0.01, RBF`) | 0.8270 | 0.7830 | 0.8968 |
## Фінальна модель і test-результат
| Модель | CV F1 | CV ROC AUC | | CV RECALL |
|---|---:|---:|
|GaussianNB|0.7463|0.8268||0.8929|
Recall був пріоріттом, тому саме ця модель
## Запуск
[Відкрити Notebook](notebooks/PR04_Bachysh_Pavlo.ipynb)
