# Aplicación de Modelos GLM para la Tarifación de Seguros de Automóviles

Este repositorio contiene el desarrollo en **RMarkdown** para el análisis actuarial y la aplicación de **Modelos Lineales Generalizados (GLM)** en la tarifación técnica de seguros de automóviles en Previsora Seguros.

##  Contenido principal

- **Perfil_de_Variables.Rmd**: código en RMarkdown que implementa:
  - Limpieza, normalización y perfilado de variables (tipos, valores faltantes, duplicados).
  - Construcción de variables actuariales clave: exposición, frecuencia, severidad y costo puro.
  - Tratamiento de outliers y consolidación de categorías con baja exposición.
  - Generación de un reporte descriptivo (EDA) automatizado en HTML.
  - Ajuste de modelos GLM para:
    - **Frecuencia de siniestros**: Poisson, Binomial Negativa y exceso de ceros.
    - **Severidad**: Gamma (log), Inverse Gaussian (log) y Lognormal.
    - **Costo puro**: modelo Tweedie.

##  Objetivos alcanzados

1. **Exploración y depuración de los datos**: garantizando calidad, consistencia y creación de variables estándar para análisis actuarial.  
2. **Selección y justificación de distribuciones y enlaces apropiados**: comparación de Poisson vs. NegBin para frecuencia, Gamma/IG/Lognormal para severidad, y Tweedie para costo puro, apoyados en métricas de ajuste como AIC y devianza .  

Estos avances corresponden al cumplimiento de los dos primeros objetivos específicos planteados en el proyecto .

##  Requisitos

- **R ≥ 4.2**
- Paquetes principales:  
  `tidyverse`, `janitor`, `lubridate`, `skimr`, `DataExplorer`,  
  `MASS`, `pscl`, `statmod`, `tweedie`, `arrow`

##  Ejecución

1. Abrir `Perfil_de_Variables.Rmd` en **RStudio**.  
2. Ajustar la ruta del archivo Feather con la base de datos.  
3. Ejecutar los chunks en orden para:
   - Generar el reporte `reportes/EDA_autos.html`.
   - Ajustar y comparar los modelos GLM.  
4. Verificar en la consola los mensajes de mapeo automático de columnas, que confirman la identificación de fechas, siniestros y pagos.

##  Resultados esperados

- Perfil detallado de la información: estructura, tipos y valores faltantes.  
- Variables actuariales claves para tarifación: exposición, frecuencia, severidad y costo puro.  
- Reporte EDA interactivo para explorar las variables relevantes.  
- Comparación de familias y enlaces GLM con soporte estadístico y actuarial.  

