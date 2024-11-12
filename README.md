# Predicción de la inflación en Argentina

1. Introducción: Presentación del problema
2. Objetivos del proyecto
3. Definición de la fuente de datos
4. Definición del dataset
5. Parametría inicial
6. Data Wrangling
7. Análisis exploratorio de datos o EDA
8. Análisis de series de tiempo
9. Modelos/Algoritmos

# ¿Qué es la inflación? Se puede definir como el alza sostenida y generalizada de los precios de los bienes y servicios existentes en un país en un período de tiempo determinado

#¿Por qué se considera como un problema? 
Pérdida del poder adquisitivo 
Disminución del ahorro, afectando también la inversión en el país
Efectos de índole micro y macroeconómicos en el corto y mediano plazo
Íntimamente vinculado con el desempleo (Curva de Phillips)

# Presentación del problema
Asunto de interes para todos los países, en especial para los países subdesarrollados.
La inflación promedio de estos países suele ser del 40% interanual comparado con el 3% a nivel mundial.
La inflación afecta más a las clases sociales más vulnerables y pobres.

# Objetivos del proyecto
Lograr identificar las variables pertenecientes a un modelo predictivo de inflación en Argentina
Realizar un análisis basado en Series de tiempo Identificar correlaciones entre las variables y detectar cuáles tienen mayor influencia en la inflación
Implementar algoritmo basado en Series de tiempo (AR, MA, ARMA, ARIMA, ARIMAX y SARIMAX)
Generar un modelo predictivo de la inflación con una precisión mayor a 50%

# Definición de la fuente de datos
Dado que la inflación es un fenómeno macroeconómico, con impacto en la microeconomía, hemos utilizado como fuente de información los datos provistos por el Ministerio de Economía de la República Argentina (https://www.economia.gob.ar/datos/).
Dicho organismo provee un acceso mediante APIs para la toma de datos descripto en el siguiente link: https://series-tiempo-ar-api.readthedocs.io/es/latest/python-usage/

# Definición de la fuente de datos
De esta manera pudimos conectarnos a la fuente de datos. Sin embargo, nos encontramos con una gran cantidad de series de datos. Por ende, para trabajar con una serie mas chica, aplicamos el  siguiente criterio:
Determinar la variable target (IPC General)
Determinar potenciales variables que permitan describir el target (a criterio de nuestros conocimientos de economía)
Determinación del período de análisis según variables seleccionadas: se encontraron datos consistentes entre 2003 y 2021. (Tener presente que la inflación durante los períodos 2013 y 2015 no fue medida de forma correcta por el INDEC)

