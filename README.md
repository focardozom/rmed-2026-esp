# Promover la Equidad Científica: Introducción a R

Materiales del taller **R-Med en Español** para [R/Medicine 2026](https://rconsortium.github.io/RMedicine_website/workshops.html#equidad).

🌐 **Sitio web del taller:** https://focardozom.github.io/rmed-2026-esp/

> Este taller ofrece una introducción práctica al uso de **R** para el análisis de datos en investigación médica y en salud. Está dirigido a profesionales de la salud, investigadores clínicos y estudiantes **sin experiencia previa en programación**.

## Objetivos de aprendizaje

Al final del taller los participantes podrán:

1. Crear y organizar un proyecto en RStudio.
2. Escribir un reporte reproducible con **Quarto**.
3. Importar datos desde distintas fuentes (Excel, CSV, SPSS, paquetes de R).
4. Explorar e identificar tipos de variables en un conjunto de datos.
5. Manipular datos con `tidyverse`.
6. Generar **tablas descriptivas listas para publicación** con `gtsummary`.

## Estructura del taller (3 horas)

| Tiempo | Bloque | Material |
|---|---|---|
| 15 min | Bienvenida y rompehielos | `inicio.qmd` |
| 20 min | R, RStudio y proyectos | `sesion_1.qmd` |
| 40 min | Introducción a Quarto (YAML, chunks, markdown) | `sesion_1.qmd` |
| *5 min* | *Pausa* | |
| 25 min | Importar datos (`rio`, paquetes) | `sesion_1.qmd` |
| 25 min | Explorar datos (`glimpse`, `skim`, tipos de variables) | `sesion_1.qmd` |
| *5 min* | *Pausa* | |
| 30 min | Manipulación con `tidyverse` y el pipe | `sesion_1.qmd` |
| 25 min | Análisis descriptivo con `gtsummary` | `sesion_1.qmd` |
| 10 min | Cierre y recursos | `sesion_1.qmd` |

## Archivos

```
.
├── inicio.qmd          # Slides de rompehielos para abrir el taller
├── sesion_1.qmd        # Sesión principal (R + Quarto + tidyverse + gtsummary)
├── data/               # Datos para la sección de importación
│   ├── yrbs_2021.csv
│   ├── yrbs_2021.xlsx
│   └── yrbs_2021.sav
├── img/                # Imágenes y diagramas
├── ref.bib             # Bibliografía
└── style-copy.css      # Estilos para las slides
```

## Requisitos previos

- **R** (4.0 o superior)
- **RStudio** (recomendado) o **Positron**
- **Quarto** (incluido con RStudio reciente)

### Paquetes de R

```r
install.packages(c(
  "tidyverse",      # Manipulación y visualización
  "rio",            # Importar datos
  "skimr",          # Resumen exploratorio
  "gtsummary",      # Tablas descriptivas para publicación
  "table1",         # Tablas descriptivas alternativas
  "palmerpenguins", # Dataset de ejemplo
  "medicaldata",    # Datasets clínicos reales
  "countdown"       # Cronómetro para las pausas
))
```

## Cómo usar este repositorio

1. Clona el repositorio:
   ```bash
   git clone https://github.com/focardozom/rmed-2026-esp.git
   ```
2. Instala los paquetes listados arriba.
3. Renderiza el sitio completo:
   ```bash
   quarto render
   ```
   o publica a GitHub Pages localmente:
   ```bash
   quarto publish gh-pages
   ```

> Cada push a `main` dispara automáticamente la GitHub Action que renderiza el sitio y lo publica en la rama `gh-pages` (ver `.github/workflows/publish.yml`).

## Datos

Los ejemplos prácticos utilizan:

- **YRBS 2021** (`data/yrbs_2021.*`) — Youth Risk Behavior Survey, para demostrar importación desde múltiples formatos.
- **`covid_testing`** del paquete [`medicaldata`](https://higgi13425.github.io/medicaldata/) — datos de pruebas de COVID-19 en un hospital pediátrico, usados para exploración y análisis descriptivo con `gtsummary`.
- **`palmerpenguins`** y **`starwars`** — datasets clásicos para introducir tidyverse.

## Instructores

**Catalina Cañizares, Ph.D.** — [ccani007.github.io](https://ccani007.github.io/ccani_website/)
**Francisco Cardozo, Ph.D.** — [focardozom.github.io](https://focardozom.github.io/)

## Licencia

> *Promover la Equidad Científica: Introducción a R* © 2026 por Catalina Cañizares y Francisco Cardozo está licenciado bajo [Creative Commons Atribución–NoComercial–SinDerivadas 4.0 Internacional](https://creativecommons.org/licenses/by-nc-nd/4.0/).
