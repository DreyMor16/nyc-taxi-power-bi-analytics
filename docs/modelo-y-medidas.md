# Modelo de datos y medidas DAX

## Modelo analítico

El informe organiza la información alrededor de la tabla de hechos de viajes y varias dimensiones para facilitar el filtrado y el análisis.

| Componente | Propósito |
|---|---|
| `FactViajes` | Registra cada viaje y sus métricas operativas y económicas. |
| `DimFecha` | Permite análisis por fecha, mes, año y día de la semana. |
| `DimHora` | Permite estudiar patrones horarios y periodos de mayor demanda. |
| `DimMetodoPago` | Clasifica los viajes según el método de pago. |
| `DimTipoTarifa` | Agrupa los viajes por tipo de tarifa. |
| `DimZonaOrigen` | Describe zona, borough y ubicación de recogida. |
| `DimZonaDestino` | Describe zona, borough y ubicación de destino. |
| `MedidasDAX` | Centraliza los indicadores y cálculos utilizados por los visuales. |

## Grupos de medidas

### Ingresos y volumen

- **Ingresos Totales:** suma del importe total de los viajes en el contexto de filtros seleccionado.
- **Total Viajes:** cantidad de viajes del periodo, zona o categoría seleccionada.
- **Total Pasajeros:** suma de pasajeros transportados.
- **Ingreso Promedio por Viaje:** ingresos totales divididos entre el total de viajes.
- **Participación de Ingresos:** peso porcentual de un método de pago o una zona respecto al total.

### Inteligencia de tiempo

- **Ingresos Año Anterior:** compara el periodo seleccionado con su equivalente del año previo.
- **Variación Ingresos YoY:** cambio porcentual interanual de los ingresos.
- **Promedio Móvil 7 Días:** suaviza la serie diaria para identificar tendencias.
- **Hora y Día de Mayor Demanda:** identifica los periodos con mayor volumen de viajes.

### Operación y desplazamiento

- **Duración Promedio Minutos:** tiempo medio de los viajes válidos.
- **Distancia Promedio por Viaje:** millas promedio recorridas.
- **Velocidad Operacional:** relación entre distancia y duración.
- **Minutos por Milla:** indicador de eficiencia del desplazamiento.

### Geografía

- **Zona Origen Mayor Demanda** y **Zona Destino Mayor Demanda:** identifican ubicaciones críticas.
- **Ranking de Zonas:** ordena zonas por viajes o ingresos.
- **Índice Atractivo Zona:** combina demanda, ingresos y comportamiento operacional para apoyar la priorización geográfica.

### Economía y rentabilidad

- **Tarifa Base Total:** suma de tarifas base.
- **Propinas Totales:** suma de propinas registradas.
- **Cargos Asociados Totales:** agrega recargos, impuestos y peajes.
- **Costo Operativo Estimado:** aproximación del costo operativo para fines analíticos.
- **Rentabilidad Estimada:** diferencia entre ingresos y costo estimado.
- **Margen Estimado %:** proporción de rentabilidad respecto a los ingresos.
- **Ingreso por Milla:** ingreso total dividido entre la distancia recorrida.

## Interactividad

Los segmentadores y las interacciones entre visuales permiten analizar los indicadores por periodo, zona, método de pago y tipo de tarifa. Los mapas conectan el desempeño económico con las zonas de origen y destino.
