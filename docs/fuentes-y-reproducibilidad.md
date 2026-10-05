# Fuentes y reproducibilidad

## Datos públicos

Los registros originales provienen de [NYC Taxi & Limousine Commission](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page), que publica archivos mensuales en formato Parquet y tablas de referencia para las zonas de taxi.

El análisis utiliza datos de Yellow Taxi correspondientes a 2015, 2016 y 2017.

## Contenido incluido

- `data/taxi_zone_lookup.csv`: catálogo público de zonas y boroughs.
- `notebooks/importacion_datos.ipynb`: proceso de apoyo para la importación de archivos Parquet hacia SQL Server.
- `dashboard/NYC_Taxi_Analytics.pbix`: modelo, medidas y visualizaciones finales.
- `theme/NYC_Taxi_Profesional.json`: tema visual del informe.

## Contenido no incluido

Los archivos mensuales completos y el respaldo de SQL Server no se incluyen porque exceden el tamaño razonable de un repositorio de portafolio. Para reproducir el proceso, los archivos Parquet deben descargarse desde la fuente oficial y cargarse mediante el notebook.

## Consideraciones de calidad

Antes de construir el modelo se revisan fechas inconsistentes, distancias o importes negativos, viajes con duración inválida, pasajeros en cero y valores atípicos. Las reglas aplicadas buscan mejorar la confiabilidad de los indicadores sin ocultar las limitaciones de la fuente.
