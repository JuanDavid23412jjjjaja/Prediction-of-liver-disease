
# Predicción de enfermedades hepáticas.

In this repository, some classifiers will be compared and the way in which they receive, train and process the data, thus in order to choose a good classifier to make a correct prediction of whether or not a patient has liver disease.

Target | # | |
-------|:-----:|:----:|
Blood donor |533 |526
Suspect Blood Donor | 7|7
|Hepatitis |24 |20|
|Fibrosis |21 |12|
|Cirrhosis |30 |24|
|TOTAL |615 |589|


# Files

This work was programmed in Colab by Google and a database of https://www.kaggle.com/fedesoriano/hepatitis-c-dataset?rvi=1 was used for this it is necessary to download the CSV file.

## Results
This work gave poor predictions with traditional multiclass methods, due to the characteristics of the descriptors, the size of each class and some missing data. However, when working with these limitations, it was possible to create classifiers that predicted whether the person was ill or not.

|Classifiers|Accuracy|Precision Blood donor|Precision Suspect blood donor|Precision Hepatitis|Precision Fibrosis|Precision Cirrhosis|
|-----|-----|-----|-----|-----|----|-----
|Gaussian Bayes|0.920904|0.974026|0.75|0.142857|0.500000|0.875000
|Multinomial Bayes|0.892655|0.968153|0.50|0.166667|0.125000|1.000000
|Complement Bayes|0.903955|0.962264|0.00|0.000000|0.000000|0.437500
|Bernoulli Bayes|0.870056|0.870056|0.00|0.000000|0.000000|0.000000
|Desicion tree|0.903955|0.974359|0.00|0.166667|0.333333|0.833333
|Random forest|0.926554|0.939024|1.00|0.400000|0.000000|1.000000

Al montarse los clasificadores binarios, las predicciones mejoraron demasiado.

|Classifiers|Accuracy|Sano|Enfermo|
|-----------|------------|------|---|
Gaussian Bayes|0.949066|0.969697|0.770492
Multinomial Bayes|0.945671|0.966038|0.762712
Complement Bayes|0.945671|0.967803|0.754098
Bernoulli Bayes|0.893039|0.893039|0.000000
Desicion tree|0.988115|0.992410|0.951613
Random forest|0.998302|0.998102|1.000000
