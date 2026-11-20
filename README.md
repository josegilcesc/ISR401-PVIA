# ISR401-PVIA · Ingeniería de Requerimientos (ISR-401)

Repositorio del equipo para el Proyecto Fin de Curso (PFC) de la asignatura
Ingeniería de Requerimientos (ISR-401), Universidad Técnica Estatal de Quevedo,
periodo 2026–2027 SPA.

**Sistema del PFC:** Plataforma de Ventas con Módulo de Recomendación basado en
Inteligencia Artificial para Establecimientos de Suministros Eléctricos en Quevedo.

## Integrantes

| Integrante | Rol |
|---|---|
| Gilces Carranza José Ignacio | Líder del equipo |
| Arteaga Alava Danela Dayana | Integrante |
| Cedeño Avila Winston Damian | Integrante |
| Mendoza Palma Allan Jeremy | Integrante |

## Índice de carpetas

| Carpeta | Actividad | Documento principal |
|---|---|---|
| `PFC/E1/` | TA-PFC-E1: visión, alcance, partes interesadas, contexto y plan de elicitación | `PFC/E1/main.tex` → `PFC/E1/main.pdf` |

Estructura de cada entrega:

```
PFC/E1/
├── main.tex            Documento principal
├── main.pdf            PDF compilado
├── referencias.bib     Referencias en BibTeX (estilo IEEE)
├── secciones/          Una sección del documento por archivo
├── instrumentos/       Guion de entrevista, cuestionario, guía de observación, consentimiento
├── modelos/            Fuentes editables de los modelos (.puml, .drawio)
├── figuras/            Imágenes exportadas de los modelos
└── evidencias/         MANIFIESTO.md de las evidencias privadas
```

## Compilación

**Compilador:** `pdflatex` (MiKTeX o TeX Live) con `bibtex`.

**Archivo principal:** `PFC/E1/main.tex`

**Dependencias (paquetes LaTeX):** `inputenc`, `fontenc`, `babel` (idioma
`spanish`), `lmodern`, `geometry`, `setspace`, `fancyhdr`, `graphicx`,
`booktabs`, `longtable`, `tabularx`, `array`, `multirow`, `xcolor`, `float`,
`caption`, `enumitem`, `hyperref`, `amssymb`, `tikz` (bibliotecas `positioning`,
`arrows.meta`, `shapes.geometric`, `fit`, `calc`). Estilo bibliográfico: `IEEEtran.bst`.
En MiKTeX se instalan automáticamente en la primera compilación si está activada
la opción *Install missing packages on-the-fly*.

**Orden de comandos** (desde la raíz del repositorio):

```
cd PFC/E1
pdflatex main
bibtex main
pdflatex main
pdflatex main
```

La primera ejecución de `pdflatex` genera `main.aux`; `bibtex` resuelve las
referencias; las dos últimas ejecuciones de `pdflatex` actualizan citas, índice
y referencias cruzadas. El resultado es `PFC/E1/main.pdf`.

## Evidencias y datos personales

Ningún dato personal de terceros se publica en este repositorio, y tampoco la
identidad de la organización estudiada. Los formularios firmados y las
grabaciones originales se guardan en un archivo cifrado, cuya contraseña solo
conoce el docente, dentro de la carpeta institucional restringida del equipo.
Cada archivo se registra en `PFC/E1/evidencias/MANIFIESTO.md` con su huella
SHA-256.
