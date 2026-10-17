# Ficha del artículo

Completa esta ficha al crear el repositorio y mantenla al día. Es el único
lugar con datos propios del artículo; el README es igual en todos los
repositorios.

## Identificación

- **Título:** Pesimismo y desconfianza: ¿Cómo afectan a la situación económica y política del país?
- **Descripción del repositorio:** Articulo del Quantificador sobre el actitudes pesimistas en el Ecuador.
- **Autoría:** Romina Estévez
- **Fecha de publicación:** 2023-10-13
- **Artículo publicado:** https://elquantificador.org/post/economia/2023-10-13-pesimismo-y-desconfianza/
- **Categoría:** Economía (el artículo también está en Valores y comportamiento)
- **Edición:** Septiembre 2023 - Marzo 2024

## Estado

Publicado el 2023-10-13. El artículo del sitio no declara `repository_url`; la
vinculación con este repositorio se hizo por título, autora y gráficos.

## Pregunta y alcance

El artículo pregunta cómo se relacionan el pesimismo y la desconfianza de los
ecuatorianos con la situación económica y política del país. Usa las rondas
2004 a 2019 del Barómetro de las Américas de LAPOP para Ecuador y estima, por
año, porcentajes ponderados con diseño muestral (pesimismo sobre la economía
del país y la personal, desaprobación del Presidente, desempleo, desconfianza
en el Presidente, falta de respeto por las instituciones y justificación de un
golpe de Estado frente a mucha corrupción). La unidad de análisis es la
persona encuestada.

## Requisitos

- R: versión no documentada en el repositorio.
- Paquetes de R: dplyr, ggplot2, here, patchwork, survey, tidyverse. El script
  los instala si faltan. Para compilar `report/report.Rmd` también se necesitan
  knitr y rmarkdown.

## Fuentes de datos

| Fuente | Institución | Periodo | Acceso | Script |
|---|---|---|---|---|
| Barómetro de las Américas (AmericasBarometer), base de Ecuador preparada por LIDE | LAPOP, Vanderbilt University | Rondas 2004, 2006, 2008, 2010, 2012, 2014, 2016 y 2019 | Descarga automática desde `laboratoriolide/americas-barometer` en GitHub; copia local en `data/ab_04_19.csv`. Fuente original: www.LapopSurveys.org | `code/pesimismo.R` |

El archivo remoto se llama `ab_04_09.csv`, pero contiene las rondas 2004 a 2019
(verificado: 17 992 filas, las ocho rondas). El script solo lo descarga si falta
`data/ab_04_19.csv`; la copia versionada en `data/` es la que se usa por defecto.

## Salidas

- `figures/grafico_pesimismo_econ.png`: pesimismo sobre la situación económica
  del país y la personal.
- `figures/grafico_desaprobacion_presidente.png`: desaprobación del trabajo del
  Presidente de turno.
- `figures/grafico_conjunto.png`: panel combinado de los dos gráficos
  anteriores.
- `figures/grafico_pesimismo_vs_desempleo.png`: pesimismo económico frente a
  desempleo.
- `figures/grafico_desconfianza_politica.png`: desconfianza política frente a
  justificación de un golpe de Estado.
- `report/report.html`: versión renderizada del texto del artículo.

## Cómo replicar en este repositorio

Este repositorio tiene un único script, sin `MASTER.R`; los pasos salen de su
README anterior y de `code/pesimismo.R`.

1. Clona el repositorio (o descarga el comprimido) y abre
   `influencia-pesimismo-ecu.Rproj` para que las rutas relativas (`data/` y
   `figures/`) apunten a la raíz del proyecto.
2. Ejecuta `code/pesimismo.R` con la raíz del repositorio como directorio de
   trabajo. Lee `data/ab_04_19.csv` (si falta, la descarga desde el repositorio
   de LIDE), calcula las tablas ponderadas con `survey` y guarda las cinco
   figuras en `figures/`.
3. Compila `report/report.Rmd` para reproducir el texto del artículo; usa las
   figuras de `figures/`.

## README anterior

Texto del README de este repositorio antes de adoptar el README estándar,
conservado sin cambios de contenido para no perder información.

### Pesimismo y desconfianza: ¿Cómo afectan a la situación económica y política del país?

Este repositorio almacena todos los archivos necesarios para el análisis de actitudes sobre pesimismo y desconfianza en Ecuador utilizando la encuesta de LAPOP.

#### Estructura del proyecto

- `code/` - Scripts de R para el análisis de datos y generación de gráficos
- `data/` - Datos de la encuesta LAPOP
- `figures/` - Gráficos generados para el reporte
- `report/` - Archivos del reporte (documento principal, bibliografía)
  - `report.Rmd` - Documento principal del reporte en R Markdown
  - `report.html` - Versión HTML del reporte
  - `refs.bib` - Referencias bibliográficas
  - `style.csl` - Estilo de citación

#### Cómo replicar el análisis

Se tienen dos opciones para replicar el análisis:

- Clonar el repositorio utilizando Git y GitHub y ejecutar los scripts.

- Descargar un archivo comprimido desde la página web del repositorio y ejecutar los scripts en la carpeta `code`.

Los scripts en `code/` generarán automáticamente las figuras en `figures/` que son utilizadas por el reporte principal.
