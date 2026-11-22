Grupo 11

Tema: Brecha de la educación y su impacto en la movilidad laboral y salarios.

El nivel educativo alcanzado por la Población Económicamente Activa (PEA) en Paraguay influye considerablemente en la calidad de su compensación en el mercado laboral; a mayor nivel de educación se registra un aumento significativo en los ingresos promedio.

Pregunta principal:

¿De qué manera el nivel educativo impacta en los ingresos laborales de la Población Económicamente Activa (PEA) en Paraguay durante el año 2025?

Objetivo General:

Realizar un análisis a nivel descriptivo sobre la relación entre el nivel educativo, el ingreso promedio y la distribución de los ingresos laborales de la población en Paraguay durante el año 2025, utilizando los microdatos de la Encuesta Permanente de Hogares Continua (EPHC), para dimensionar el impacto de la brecha educativa en las condiciones socioeconómicas.

Objetivos Específicos:

1. Describir el perfil educativo y laboral de la fuerza de trabajo: Cuantificar a la Población Económicamente Activa (PEA) y ocupada según sus años de estudio, máximo nivel educativo alcanzado y sector económico de empleo.
2. Comparar los ingresos laborales según estrato educativo: Calcular y contrastar el ingreso promedio y la mediana salarial (ingreso principal y total) entre los diferentes grupos de escolaridad (educación básica, media, terciaria/universitaria).
3. Examinar la calidad de la ocupación y la movilidad laboral: Relacionar el nivel educativo con categorías de subocupación, precariedad e informalidad laboral (por ejemplo, acceso a seguridad social/IPS o tenencia de RUC).
4. Identificar disparidades transversales: Analizar cómo se comporta la brecha de retornos educativos (ingresos y ocupación) al segmentar los datos por sexo y área de residencia (urbana vs. rural), para evaluar si el impacto de la educación “en el ingreso promedio” varía según el contexto demográfico.

Datos y Fuente

Se utilizan los microdatos de la Encuesta Permanente de Hogares Continua (EPHC) anual 2025, publicados por el Instituto Nacional de Estadística (INE) de Paraguay.

Archivos utilizados:

- "REG02_EPHC_ANUAL_2025.csv": Información de personas, educación, empleo e ingresos.
- "REG01_EPHC_ANUAL_2025.csv": Información sobre características de vivienda, servicios y equipamiento del hogar.
- "diccionario_EPHC_ANUAL_2025.xls": Descripción y codificación de las variables.

Fuente oficial: https://www.ine.gov.py/

Los resultados inferenciales y predictivos corresponden a la población estudiada y no a la totalidad de la PEA.

Tecnologías Utilizadas

- Python: Lenguaje principal del proyecto.
- Jupyter Notebook y Google Colab: Desarrollo y ejecución de los análisis.
- Pandas y NumPy: Limpieza, transformación y procesamiento de datos.
- Matplotlib y Seaborn: Visualización de resultados.
- SciPy y Statsmodels: Análisis inferencial y pruebas estadísticas.
- Scikit-learn: Modelos predictivos, clustering, validación cruzada y métricas de evaluación.
- Git y GitHub: Control de versiones y publicación del proyecto.

Estructura del Repositorio

- "notebooks/": Notebooks de Jupyter correspondientes a las tres fases del proyecto.
- "Informes/": Informes periódicos generados para presentaciones.
- "requirements.txt": Dependencias necesarias para ejecutar el proyecto.

Guía de Reproducción

1. Clonar el repositorio:

git clone https://github.com/fiomusmeci-rgb/Proyecto_DataScience.git
cd Proyecto_DataScience

2. Instalar dependencias:

pip install -r requirements.txt

3. Preparar los datos:

Los archivos oficiales de la EPHC anual 2025 se descargan automáticamente desde el portal del INE y se ubican en la carpeta "data/".

En los notebooks también se incluyen instrucciones para descargar los archivos necesarios.

4. Ejecutar los notebooks:

Abrir los archivos desde Google Colab y ejecutar sus celdas en orden.

- Fase 1: Selección de variables, limpieza y análisis exploratorio.
- Fase 2: Corrección de datos y análisis inferencial.
- Fase 3: Modelado predictivo, clustering e incorporación de variables de vivienda.

Se recomienda utilizar la opción Restart & Run All para ejecutar las celdas en orden y reproducir los resultados.

5. Consultar los resultados:

Los gráficos, tablas y métricas se presentan en las salidas de los notebooks. Los archivos generados durante la ejecución se almacenan en los directorios de salida establecidos en el código.

Para garantizar la reproducibilidad, deben mantenerse los nombres de los archivos originales, las transformaciones documentadas y las semillas aleatorias definidas en los notebooks.

Síntesis de Resultados

Fase 1 - Análisis exploratorio:

Se seleccionaron las variables educativas, laborales y sociodemográficas relevantes para la investigación. Se realizó la limpieza inicial y se exploraron las distribuciones de escolaridad, ingresos y condiciones de empleo.

Fase 2 - Análisis inferencial:

Se corrigieron inconsistencias detectadas en la fase anterior, principalmente el formato de los ingresos con coma decimal y la clasificación de los estratos educativos.

Los resultados evidenciaron diferencias estadísticamente significativas en los ingresos medios según el nivel educativo. Los promedios aproximados fueron:

- Educación básica: 2,17 millones de guaraníes.
- Educación media: 2,77 millones de guaraníes.
- Educación terciaria/universitaria: 4,16 millones de guaraníes.

El ANOVA obtuvo un valor p aproximado de 1,01 × 10⁻⁸⁰. Sin embargo, el tamaño del efecto fue reducido, con un eta cuadrado de 0,0156, por lo que la educación no explica por sí sola toda la variabilidad de los ingresos.

Fase 3 - Análisis predictivo:

Se evaluaron modelos de regresión para estimar el ingreso habitual de la ocupación principal mediante su logaritmo natural.

La ampliación incorporó el factor de expansión de la encuesta, variables de vivienda del registro REG01 y perfiles identificados mediante K-Means.

El análisis de clustering identificó dos perfiles descriptivos con diferencias en escolaridad e informalidad laboral, aunque con una separación limitada según el índice Silhouette de 0,203.

En la comparación predictiva, agregar variables de vivienda redujo el RMSE ponderado en prueba de aproximadamente 0,594 a 0,566, una mejora relativa del 4,64 %. Incorporar la etiqueta de clúster no produjo una mejora predictiva adicional apreciable.

Conclusión general:

Los resultados muestran una asociación positiva entre el nivel educativo y los ingresos laborales en la población estudiada. Sin embargo, también intervienen características ocupacionales, sociodemográficas y habitacionales.

La inferencia estadística permitió identificar diferencias significativas entre grupos, mientras que los modelos predictivos evaluaron qué variables ayudan a estimar mejor los ingresos.

Los resultados representan asociaciones estadísticas y evidencia predictiva; no permiten establecer relaciones causales definitivas.

Integrantes

- Fiorella Musmeci
- Oscar Román
- Ian Torres

Asignatura: Electiva - Data Science
Profesora: Margarita Ruiz Olazar
Institución: Facultad Politécnica - Universidad Nacional de Asunción