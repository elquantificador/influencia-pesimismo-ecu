# Ficha del artículo

Completa esta ficha al crear el repositorio y mantenla al día. Es el único
lugar con datos propios del artículo; el README es igual en todos los
repositorios.

## Identificación

- **Título:** Pesimismo y desconfianza: ¿Cómo afectan a la situación económica y política del país?
- **Descripción del repositorio:** Articulo del Quantificador sobre el actitudes pesimistas en el Ecuador.
- **Autoría:** [COMPLETAR: nombres, igual que en el sitio]
- **Fecha de publicación:** [COMPLETAR: AAAA-MM-DD]
- **Artículo publicado:** [COMPLETAR: enlace a elquantificador.org]
- **Categoría:** [COMPLETAR: Economía, Política, Salud, Educación o Valores y
  comportamiento]
- **Edición:** [COMPLETAR: por ejemplo, Julio-Diciembre 2026]

## Estado

[COMPLETAR: en preparación, en revisión editorial o publicado. Anota qué falta
para cerrar el artículo.]

## Pregunta y alcance

[COMPLETAR: dos o tres oraciones con la pregunta, el periodo, la cobertura
geográfica y la unidad de análisis.]

## Requisitos

- R [COMPLETAR: versión, por ejemplo 4.5.x].
- Paquetes de R: [COMPLETAR: lista en orden alfabético].

## Fuentes de datos

| Fuente | Institución | Periodo | Acceso | Script |
|---|---|---|---|---|
| [COMPLETAR] | [COMPLETAR] | [COMPLETAR] | [COMPLETAR: descarga automática o manual] | `code/cleaning/00_download_fuente.R` |

Si alguna fuente no permite descarga automática, explica aquí cómo obtenerla y
dónde colocarla en `data/raw/`.

## Salidas

- `outputs/tables/[COMPLETAR].csv`: [COMPLETAR: qué contiene].
- `outputs/graphs/[COMPLETAR].png`: [COMPLETAR: qué muestra].
- `article/images/graficoN.png`: copias numeradas según el orden del texto.

## Cómo replicar en este repositorio

Este repositorio conserva sus instrucciones originales en la sección
"README anterior". Si todavía no tiene `MASTER.R`, sigue esas instrucciones.
Cuando se migre a la estructura estándar, reemplaza esta sección por los pasos
de `MASTER.R`.

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
