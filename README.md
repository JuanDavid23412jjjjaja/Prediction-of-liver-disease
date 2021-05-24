# Prediction-of-liver-disease

# Predicción de enfermedades hepáticas.

En este repositorio se compararán algunos clasificadores y la forma en la que estos reciben entrenan y procesan los datos, así con el fin de elegir un buen clasificador para hacer una predicción correcta de sí un paciente posee o no una enfermedad hepática.

Target | # | |
-------|:-----:|:----:|
Blood donor |533 |526
Suspect Blood Donor | 7|7
|Hepatitis |24 |20|
|Fibrosis |21 |12|
|Cirrhosis |30 |24|
|TOTAL |615 |589|


# Files

Este trabajo fue programado en Colab by Google y se utilizó una base de datos de https://www.kaggle.com/fedesoriano/hepatitis-c-dataset?rvi=1 para esto es necesario descargar el archivo CSV.

## Resultados
Este trabajo dio malas predicciones con los métodos tradicionales multiclase, debido a las características de los descriptores, el tamaño de cada clase y algunos datos perdidos. Sin embargo, al trabajarse con esas limitantes, se lograron crear clasificadores que predecían sí la persona estaba enferma o no.

|Classifiers|Accuracy|Precision Blood donor|Precision Suspect blood donor|Precision Hepatitis|Precision Fibrosis|Precision Cirrhosis|
|-----|-----|-----|-----|-----|----|-----|-----|---
|Gaussian Bayes|0.920904|0.974026|0.75|0.142857|0.500000|0.875000
Multinomial Bayes|0.892655|0.968153|0.50|0.166667|0.125000|1.000000
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
