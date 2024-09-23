# Red LSTM para Predecir la Bolsa de Valores

<p align="center">
<img src="https://github.com/jrguignan/Proyecto-Predictor_de_Trading/blob/main/images/banner.png"  height=400>
</p>



# Índice


* [Introducción](#Introducción) 
  * [Explicación del Código](#Explicación-del-Código) 
* [Datasets](#Datasets) 
* [Standard & Poor's 500](#Standard-&-Poor's-500) 
* [TESLA, INC.](#TESLA,-INC.) 
* [APPLE COMPUTER INC](#APPLE-COMPUTER-INC) 
* [Autor](#Autor)


# Introducción

En este proyecto se ha desarrollado un modelo de predicción de precios de cierre tres activos financieros, utilizando una red neuronal de tipo LSTM (Long Short-Term Memory). Las LSTM son especialmente efectivas para capturar patrones en datos secuenciales, lo que las hace ideales para tareas como la predicción de series temporales. En este caso, hemos aplicado este modelo para predecir los valores futuros de cierre de un activo del índice S&P 500, basándonos en los precios históricos.

Beneficios de usar LSTM:
Memoria a largo plazo: A diferencia de las redes neuronales simples, las LSTM pueden "recordar" patrones en los datos a lo largo del tiempo. Esto es útil en series temporales, donde los valores pasados pueden influir en los futuros.

Captura de dependencias temporales: Las LSTM son capaces de modelar relaciones complejas a lo largo de períodos largos, lo que les permite reconocer tendencias o comportamientos recurrentes en los datos de mercado.

Evitan el problema de desvanecimiento del gradiente: Gracias a su arquitectura interna, las LSTM pueden mantener información relevante durante largos intervalos de tiempo, superando problemas que otros modelos tradicionales, como las redes neuronales recurrentes simples (RNN), no pueden manejar eficientemente.

En resumen, el uso de una LSTM mejora la precisión del modelo al capturar patrones temporales en los datos históricos, lo que es fundamental para la predicción de valores en mercados financieros, donde los precios pasados influyen en los futuros.

<br>[Volver al Índice](#Índice)

## Explicación del Código
División de Datos: Los datos se dividen en dos conjuntos: uno de entrenamiento y otro de validación, utilizando solo la columna del precio de cierre.

Escalado: Utilizamos MinMaxScaler para escalar los datos entre 0 y 1, lo que mejora la capacidad de aprendizaje del modelo.

Ventana de Tiempo: Se crean secuencias de 60 días como entrada (X_train) y se predice el valor del día siguiente como salida (Y_train).

Red LSTM: Definimos un modelo secuencial con una capa LSTM de 50 neuronas y una capa densa de salida que predice un único valor (el precio de cierre del día siguiente).

Entrenamiento: El modelo es entrenado durante 20 épocas con un tamaño de lote de 32.

Predicción: Después de entrenar, utilizamos el conjunto de validación para realizar las predicciones y desescalamos los valores para obtener los precios originales.

Este enfoque de predicción puede ser una herramienta valiosa para tomar decisiones informadas en el mercado de valores.

<br>[Volver al Índice](#Índice)

# [Datasets](https://github.com/jrguignan/Proyecto-Predictor_de_Trading/tree/main/datasets)

En esta [carpeta](https://github.com/jrguignan/Proyecto-Predictor_de_Trading/tree/main/datasets)
 se encuentran los datasets utilizados en formato csv. Actualizados hasta septiembre 2024. 

Los archivos .ipynb se utiliza la libreria yfinance para tener los datos actualizados de los activos financieros.


# [Standard & Poor's 500](https://github.com/jrguignan/Proyecto-Predictor_de_Trading/blob/main/red_LSTM_sp500.ipynb)

<p align="center">
<img src="https://github.com/jrguignan/Proyecto-Predictor_de_Trading/blob/main/images/sp500_c.png"  height=400>
</p>

<br>[Volver al Índice](#Índice)

# [TESLA, INC.](https://github.com/jrguignan/Proyecto-Predictor_de_Trading/blob/main/red_LSTM_tesla.ipynb)

<p align="center">
<img src="https://github.com/jrguignan/Proyecto-Predictor_de_Trading/blob/main/images/tesla_c.png"  height=400>
</p>

<br>[Volver al Índice](#Índice)

# [APPLE COMPUTER INC](https://github.com/jrguignan/Proyecto-Predictor_de_Trading/blob/main/red_LSTM_apple.ipynb)

<p align="center">
<img src="https://github.com/jrguignan/Proyecto-Predictor_de_Trading/blob/main/images/apple_c.png"  height=400>
</p>




<br>[Volver al Índice](#Índice)

# Autor

- José R. Guignan
- Mail: joserguignan@gmail.com
- Linkedin: [https://www.linkedin.com/in/jrguignan](https://www.linkedin.com/in/jrguignan)
