# Analisis de Desempeño de Reckit

***Objectivo: ***
<br>Detectar puntos débiles en el mercado para la marca Reckit y mejoras que se
pueden implementar para obtener más presencia en el mercado donde Cloros y Blanqueadores de ropa son una de las categorías más importantes para la
empresa Reckitt

***Herramientas Utilizadas:***
<br>SQL, Python con las librerías numpy, pandas, matplotlib, Scikit Learn, Statsmodels,
Seaborn, PowerBI, etc.

***Carga, limpieza, union y transformacion de los datos con pandas***
<br>Importamos la librería de pandas para cargar los datos y realizar la limpieza y organización de datos de ser necesario
<br>![image](https://github.com/user-attachments/assets/3c3a3938-2c8a-43e8-8431-ded142a041cf)

Utilizamos los metodos .info() y .describe() para obtener información general del DataFrame creado seguido de .isnull().any() y .duplicated().any() para revisar la existencia de valores vacíos o duplicados
<br>![image](https://github.com/user-attachments/assets/db6795b6-ae79-4cb9-b47a-b244140bd58a)
![image](https://github.com/user-attachments/assets/ac6c5a53-0441-481e-97a5-a3b706487569)
![image](https://github.com/user-attachments/assets/327cf89f-5e6f-4407-bdfd-883131043c42)

En caso de tener campos vacíos podemos visualizarlos para determinar como tratarlos
<br>![image](https://github.com/user-attachments/assets/4004a8c7-cdbf-4a45-bd00-bc0038746465)
<br>![image](https://github.com/user-attachments/assets/fb961f8f-c87e-45df-a7e5-39f60d84964e)

Para este caso buscamos un valor similar para determinar si rellenar o dropear el valor
<br>![image](https://github.com/user-attachments/assets/449c0eff-a29b-4fc8-8dd0-65f46f555877)
<br>![image](https://github.com/user-attachments/assets/092907e5-7eb3-4c1e-8760-08d1af362b5d)

Con ayuda de Seaborn podemos visualizar gráficamente la
existencia de valores nulos y saber si es necesario realizar algún
otro proceso.
<br>![image](https://github.com/user-attachments/assets/fd8e0ef9-d96a-4b63-bf07-37622c5cad5c)

Al haber insertado todos los datos necesarios, renombramos columnas para mejor 6
identificación y facilitar la unión de los diferentes DataFrames
<br>![image](https://github.com/user-attachments/assets/a4c63647-3012-4159-ac78-1e0274b57744)
![image](https://github.com/user-attachments/assets/89a75110-7cff-4d91-a0d3-5b7b2e3e9018)

Reordenar columnas de ser necesario
<br>![image](https://github.com/user-attachments/assets/506b3ab1-7834-4bae-a309-2e27b9a66a90)

Al final exportamos la información, habiendo limpiado, organizado y combinado los campos
<br>![image](https://github.com/user-attachments/assets/d9d6eb16-edb7-4bf0-ac33-59e49cbbccf8)

***Análisis exploratorio de datos (EDA) y visualizaciones***
<br>Separamos los años para poder analizar los datos independientemente
<br>![image](https://github.com/user-attachments/assets/1d7e7469-791b-4228-b04f-78028b3e9502)

Realizamos una visualización entre el mes y el promedio de ventas para observar cómo se
comportan las diversas marcas
<br>![image](https://github.com/user-attachments/assets/b8dafe9d-0330-4fd6-80df-fe809e1203a5)
![image](https://github.com/user-attachments/assets/0aae2b73-93f0-42df-889d-26b827fa5dcf)
![image](https://github.com/user-attachments/assets/8018d261-6be9-4497-9b83-4de0ead150b5)

Filtrando las ventas totales por marca y mes para identificar las marcas líderes
<br>![image](https://github.com/user-attachments/assets/f8f1ea80-78eb-43e1-a41c-e70f77a6880a)

Nuevamente se puede apreciar que las ventas por marca a lo largo del año se mantienen relativamente y que las marcas líderes son Cloralex, Vanish y Clorox, siendo Cloralex quien supera a todas por mucho.
<br>![image](https://github.com/user-attachments/assets/94db5844-f10c-4f95-b0d8-6bc39b4868ed)

Comparamos graficando las marcas por región y ventas acumuladas
<br>![image](https://github.com/user-attachments/assets/a2fd23d2-7de2-41ed-968d-2c32f3af2594)

Según las gráficas anteriores se puede observar que la media de ventas por marca se mantienen en cantidades bastante similaresa través de las distintas regiones
<br>![image](https://github.com/user-attachments/assets/f785796a-2972-42e6-8e30-f9e27ec89137)

Realizamos la graficación de la suma acumulada de ventas, agrupando por mes y región
<br>![image](https://github.com/user-attachments/assets/c31704b0-a69a-4f15-a4b5-8d4655b3fcac)
<br>![image](https://github.com/user-attachments/assets/9016a469-381f-4a08-9af2-c9b063cd1487)
<br>![image](https://github.com/user-attachments/assets/410a155e-e41f-4100-b108-e6029186d13d)
![image](https://github.com/user-attachments/assets/edf2a9fb-9fc1-438b-a320-c72e14c78281)

Existen meses donde se realizan más ventas como lo son los meses 1 y 6 del año 2022 y los meses 5 y 6 del 2023.
<br>A si mismo se observa que hay otros meses donde caen las ventas como los meses 2, 3 y 4 de ambos años y el mes 12 del 2022

Podemos realizar visualizaciones para conocer mejor la relación entre ventas y regiones
<br>![image](https://github.com/user-attachments/assets/02448596-bf39-4a37-ba58-c3c6ed441989)
<br>![image](https://github.com/user-attachments/assets/2ca3ba52-0aca-4c27-8cf1-adf6839e6af0)
<br>![image](https://github.com/user-attachments/assets/14461df8-ad36-493e-a8fd-237a7418133d)
![image](https://github.com/user-attachments/assets/04d548fc-5a85-46d8-994b-d9c2bd1aa77f)
<br>En base al mapa anterior se pueden observar las áreas con mayor y con menor rendimiento

Podemos realizar visualizaciones para conocer mejor la relación entre ventas y regiones
<br>![image](https://github.com/user-attachments/assets/fdea25b9-8594-483b-93db-b7d532e2a203)

En estas últimas gráficas de forma más completa la relación de las ventas totales por región, donde a simple vista se puede ver la relación con los meses con más ventas que se observó en otras gráficas anteriores y también se observa que casos requerirían una mayor atención debido a la dispersión de sus datos y casos especiales (outliers)
<br>![image](https://github.com/user-attachments/assets/83f89616-89d5-485e-bbdb-07126d66f285)

***Segmentación de productos/regiones con clustering***
<br>Realizamos una filtración para solo enfocarnos en productos VANISH
<br>![image](https://github.com/user-attachments/assets/16efe696-a176-439b-bf38-da703f309336)

Reorganizamos la información para enfocarnos en las características clave
<br>![image](https://github.com/user-attachments/assets/875169dc-8884-4286-bb2b-9cf26e09b40c)

Convertimos los datos en valores numéricos para poder procesarlos y los filtramos
<br>![image](https://github.com/user-attachments/assets/cdf4ecda-1f6c-403a-8a94-68a698ccc6e4)
<br>![image](https://github.com/user-attachments/assets/e92b7b02-e9df-47b8-a9c8-0678a0221dac)

Finalmente escalamos los datos
<br>![image](https://github.com/user-attachments/assets/53681d23-31dd-46f5-883c-d363c2216312)

Para obtener los mejores resultados, calculamos el wcss para poder graficar el Codo de Jambu y obtener el número óptimo de clusters a utilizar
<br>![image](https://github.com/user-attachments/assets/bd191b01-340a-491f-a43c-b43333edb319)
<br>![image](https://github.com/user-attachments/assets/53ab330a-c477-4de2-b18f-7554e656e57c)

Gracias a esta gráfica podemos determinar que el número óptimo de clusters es el de 4
<br>![image](https://github.com/user-attachments/assets/295ce20d-7073-46d8-8a01-53a85a864973)

Utilizamos el método de K-means para realizar la graficación de clusters
<br>![image](https://github.com/user-attachments/assets/34a845b7-c213-44e8-bdde-6bbc2e6bbb0f)
<br>![image](https://github.com/user-attachments/assets/2ea92be6-e434-44ee-9628-3c76f5e481c0)

Los resultados obtenidos en este punto no son fáciles de interpretar debido a la falta de dimensionalidad, por lo que podemos realizar el método de PCA (Principal Component Analysis) para mejorar los resultados.
<br>![image](https://github.com/user-attachments/assets/de68fee5-d389-4f29-bbe5-c301387293bb)

Después de utilizar PCA realizamos una descomposición para volver a correr el modelo
<br>![image](https://github.com/user-attachments/assets/6c4792a5-5d42-4203-91e2-5b51d852d0b6)
![image](https://github.com/user-attachments/assets/c315057b-40eb-4d43-8f92-80298a9f9127)
<br>![image](https://github.com/user-attachments/assets/e6827a9b-ff31-4917-a272-f7b00b81e1dd)

Volvemos a graficar el codo de Jambu para verificar el número óptimo de clusters, en este caso sigue siendo 4
<br>![image](https://github.com/user-attachments/assets/60251d7f-628d-4749-bc73-df6ca2b2c3e6)

Volvemos a correr el modelo de K-means
<br>![image](https://github.com/user-attachments/assets/2d40451c-02f0-404b-9d16-cd63809968d6)
<br>![image](https://github.com/user-attachments/assets/66e49cbe-7a96-45db-a5b3-338b6ff7c256)

Podemos observar que existe una alta relación entre las ventas totales de cada producto con los atributos que los definen, esto nos ayudará para sacar provecho de un atributo de los productos o para reestructurar la estrategia utilizada con algún atributo que no se esté desempeñando de la manera adecuada
<br>![image](https://github.com/user-attachments/assets/a4d604da-8b01-4c0f-81b0-a9af75e1e090)

***Análisis de Datos con SQL***
<br>Creamos la base de datos y las tablas con los datos a utilizar dentro de SSMS
<br>![image](https://github.com/user-attachments/assets/ea45c4be-95b7-4191-abca-4f95ef672d3a)
<br>![image](https://github.com/user-attachments/assets/91bfbb3c-afec-4e0f-96f3-da81e2219afe)
![image](https://github.com/user-attachments/assets/e356cd09-a054-41d8-b5d4-a0456b1dffa5)

Importamos los datos y confirmamos que se añadieran correctamente para cada tabla
<br>![image](https://github.com/user-attachments/assets/f5c4141e-7902-44ca-abc7-c6d1afdb0711)
![image](https://github.com/user-attachments/assets/42baec2f-3a18-4fe1-aa86-2a1ba7a27e69)
![image](https://github.com/user-attachments/assets/b7742a90-8354-4528-b14c-a3e7124be3d5)
![image](https://github.com/user-attachments/assets/a75e0fd1-25b7-4d7e-97d1-c05d0217f66c)
![image](https://github.com/user-attachments/assets/0bb47fe3-7d78-4dff-a8fe-ea99b43a8570)

Ejecutamos uniones entre tablas paras combinar la información y obtener insights clave sobre las ventas por categoría, región y periodo de tiempo.
<br>![image](https://github.com/user-attachments/assets/ba0f3b07-1bc7-446c-8f8a-e012f237bfa5)
<br>![image](https://github.com/user-attachments/assets/0cf546ff-326c-4d56-96df-b425c335cd56)
<br>![image](https://github.com/user-attachments/assets/45c8fd28-022b-4c16-92c7-2efacd038859)

***Prediccion de Ventas con Machine Learning***
<br>Se desarrollará un modelo predictivo para prever las ventas futuras de productos clave como Vanish y Lysol. Cargamos librerías principales y los datos a utilizar
<br>![image](https://github.com/user-attachments/assets/5a4896e8-a650-4400-9db1-50db2873f2d2)

Realizamos una filtración para trabajar solo sobre las marcas Vanish y Lysol
<br>![image](https://github.com/user-attachments/assets/fbdc43a7-13db-4da7-86b0-7b0faf9f6c2d)

Para realizar las predicciones de ventas futuras, organizamos el data frame en el valor de las ventas totales en los intervalos semanales proveídos
<br>![image](https://github.com/user-attachments/assets/d62499c7-aa23-4eaa-a903-cb5636107919)

Realizando una visualización simple de los datos podemos identificar que existe una tendencia aunque no es muy fácil de identificar
<br>![image](https://github.com/user-attachments/assets/bee77742-118d-405a-9047-75c079cfc772)

Dividimos los datos en conjunto de entrenamiento y prueba, Podemos dividir simplemente el tamaño del data frame debido a que se utilizara un modelo de series de tiempo
<br>![image](https://github.com/user-attachments/assets/9b7e00dc-cc3d-4537-9b1c-d25cf9681e00)
<br>![image](https://github.com/user-attachments/assets/c500c0fc-e07d-475c-b49c-13d82451fc8f)
![image](https://github.com/user-attachments/assets/424a1a41-9c68-416e-8ca2-d01ea410c242)

Debido a que no se puede observar una estacionalidad regular se utilizará el modelo ARIMA
sobre SARIMA

Realización de la prueba Dickey-Fuller para conocer si los datos son estacionarios 
<br>H0: La serie es NO ESTACIONARIA
<br>Ha: La serie SI ES ESTACIONARIA
<br>![image](https://github.com/user-attachments/assets/bb5becb4-b1bb-4647-8af2-ae994cf85c1f)

Aplicar diferencias para remover la tendencia
<br>![image](https://github.com/user-attachments/assets/bb8139aa-3f16-42db-ad1c-03856101b28d)

Con un valor p de 0.513085 no podemos rechazar la hipótesis nula, no podemos decir que es no estacionaria
<br>![image](https://github.com/user-attachments/assets/5d259a76-a9a2-4d53-8329-0975cd2d96c2)
<br>![image](https://github.com/user-attachments/assets/64263ac4-c7f5-4c91-93a2-b3278a2a5d3c)
<br>Con un valor p de 0.078 no podemos rechazar la H0 por lo que no podemos decir que la serie es estacionaria

Aplicar diferencias doble para remover la tendencia
<br>![image](https://github.com/user-attachments/assets/f0f5c738-e559-4be0-8245-b47e9f151455)
![image](https://github.com/user-attachments/assets/8e32c127-f024-4f7c-be7b-218843237225)

Realizar Dickey-Fuller en las diferencias
<br>![image](https://github.com/user-attachments/assets/31abb881-76cd-4881-90eb-52f38d1b5abd)

Al tener un valor p menor a 0.05, podemos decir que la serie es estacional 
<br>Al haber realizado dos diferencias, en ARIMA, el valor a utilizar en d sería de 2
<br>Evaluamos para encontrar el valor p con los índices AIC y BIC
<br>![image](https://github.com/user-attachments/assets/03b65524-fbbd-4282-88f9-205fbc7033f4)

Debido a que el AIC y BIC dejaron de disminuir significativamente, podemos tomar p = 5
<br>![image](https://github.com/user-attachments/assets/361f062f-94da-4177-bd67-f6ccf2b24f66)

Evaluamos para encontrar el valor q
<br>![image](https://github.com/user-attachments/assets/f2a1d886-0ec8-49e3-8d47-54aab676c29d)

Volvemos a calcular las bases de prueba y entrenamiento para que incluyan los valores dropeados con al realizar las diferencias
<br>![image](https://github.com/user-attachments/assets/4a61654c-0835-4b0c-b58b-e8af0c6652ee)

Debido a que el AIC y BIC dejaron de disminuir significativamente, podemos tomar q = 1 
<br>Realizadas estas pruebas podemos determinar que el mejor modelo sería ARIMA(5,2,1)
<br>![image](https://github.com/user-attachments/assets/139b835f-ee83-4144-b6c3-0c887cb7a1f0)

Pronóstico puntual de la base de prueba tomando en cuenta Base de entrenamiento: 72 Base 38 de prueba: 8
<br>![image](https://github.com/user-attachments/assets/8fb0c290-61ce-4a5a-b9d2-dab61bbdca29)
![image](https://github.com/user-attachments/assets/ad29fec2-dbbe-4fe9-91ea-b5309e41f957)

Pronóstico por intervalo de las 8 semanas restantes
<br>![image](https://github.com/user-attachments/assets/13cede71-0cf4-4e3b-a1a6-3fafbf0e185c)
![image](https://github.com/user-attachments/assets/8e677a5e-65e0-40b0-a25d-806f4b510750)

***Con este pronóstico graficamos y evaluamos los resultados***
![image](https://github.com/user-attachments/assets/04807db3-fcf4-4bdc-961f-19b361419e5e)

![image](https://github.com/user-attachments/assets/6785d77e-8e43-459c-b8ea-7525a5c558e8)
<br>***Conclusión:*** Los pronósticos son confiables debido a que el error es solo de 7.37%

***
Se puede apreciar que las ventas por marca a lo largo del año se mantienen relativamente a lo largo del año y que las marcas líderes son Cloralex, Vanish y Clorox

Existe una alta relación entre las ventas totales de cada
producto con los atributos que los definen.

Este análisis nos ayuda a conocer las marcas y sectores con un buen desempeño, lo que nos puede ayudar a saber en qué productos enfocarnos o dejar de manejar, al igual de los sectores que requieren una mejor estrategia para priorizarlos.

Existen meses donde se realizan más ventas como lo son los meses 1 y 6 del año 2022 y los meses 5 y 6 del 2023; A si mismo se observa que hay otros meses donde caen las ventas como los meses 2, 3 y 4 de ambos años y el mes 12 del 2022. Al tener el conocimiento de que sectores, productos y fechas específicas, podemos realizar análisis enfocados donde existe un mejor desempeño y compararlos donde las ventas no tienen un buen rendimiento y conocer las estrategias que funcionan y las que no.

Debido al crecimiento constante que se ha encontrado a lo largo del tiempo podría haber algún otro factor que no se esté tomando en cuenta como la aplicación de alguna promoción, el crecimiento de la población o podría existir una estacionalidad que no se esté aprovechando y sea lo que hace un poco confusa los resultados de las pruebas de autocorrelación y autocorrelación parcial
***
