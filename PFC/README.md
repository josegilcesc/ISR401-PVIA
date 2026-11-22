# ISR401-PVIA — Plataforma de Ventas con Módulo de Recomendación basado en IA para Establecimientos Eléctricos

Repositorio oficial del equipo para la asignatura **Ingeniería de Requerimientos (ISR-401)**, Cuarto Nivel, Paralelo A — Facultad de Ciencias de la Computación, Universidad Técnica Estatal de Quevedo (UTEQ).

**Periodo Académico:** Segundo Periodo Académico Ordinario (SPA) 2026–2027  
**Docente:** Prof. Gleiston C. Guerrero-Ulloa, PhD (`gguerrero@uteq.edu.ec`)  
**Actividad actual:** TA-PFC-E1 — Proyecto Fin de Curso, entrega 1: visión, alcance, partes interesadas, contexto y plan de elicitación.

---

## 👥 Integrantes del Equipo

| N.º | Nombre Completo | Correo Institucional | Usuario GitHub | Rol Principal |
| :---: | :--- | :--- | :--- | :--- |
| 1 | **José Ignacio Gilces Carranza** | `jgilcesc@uteq.edu.ec` | `josegilcesc` | Líder de Proyecto / Visión / Gestión / Release |
| 2 | **Danela Dayana Arteaga Alava** | `darteagaa@uteq.edu.ec` | `danelaarteaga` | Analista de Stakeholders / Ética y Custodia LOPDP |
| 3 | **Winston Damian Cedeño Avila** | `wcedenoa@uteq.edu.ec` | `wcedeno` | Analista de Contexto / Modelado / Gestión de Riesgos |
| 4 | **Allan Jeremy Mendoza Palma** | `amendozap@uteq.edu.ec` | `allanmendoza` | Ingeniero de Elicitación / Diseño de Instrumentos |

---

## 📁 Estructura del Repositorio

El repositorio organiza los entregables de la entrega sumativa **TA-PFC-E1** conforme a la estructura oficial del proyecto:

```text
ISR401-PVIA/
├── .gitignore                                <- Exclusión de archivos auxiliares de compilación (.aux, .log, .out, etc.)
├── README.md                                 <- Instrucciones de compilación reproducible, integrantes y control general
└── PFC/
    └── E1/                                   <- TA-PFC-E1: Planificación y Elicitación de Requisitos
        ├── main.tex                          <- Documento principal integrador en LaTeX
        ├── main.pdf                          <- Documento final compilado (12 a 20 páginas netas de contenido)
        ├── referencias.bib                   <- Bibliografía verificable en formato BibTeX (norma IEEE)
        ├── 01-ficha-vision.tex               <- Sección 1: Declaración de visión y objetivos cuantitativos de negocio
        ├── 02-alcance.tex                    <- Sección 2: Alcance delimitado (in/out) y restricciones técnicas
        ├── 03-partes-interesadas.tex         <- Sección 3: Caracterización de 8+ stakeholders y roles de negocio
        ├── 04-contexto.tex                   <- Sección 4: Descripción del contexto y las 8 perspectivas de Pohl
        ├── 05-elicitacion.tex                <- Sección 5: Plan de elicitación y síntesis de hallazgos de campo
        ├── 06-etica-datos.tex                <- Sección 6: Protocolo ético y de protección de datos (LOPDP Ecuador)
        ├── 07-gestion.tex                    <- Sección 7: Plan de proyecto, cronograma, roles y comunicaciones
        ├── 08-riesgos.tex                    <- Sección 8: Matriz y plan de tratamiento de riesgos
        ├── 09-declaracion-ia.tex             <- Sección 9: Declaración de uso y verificación de herramientas de IA
        ├── 10-conclusiones.tex               <- Sección 10: Integración de conclusiones individuales
        ├── conclusiones/                     <- Conclusiones individuales por integrante (autoría propia)
        │   ├── c-gilces.tex                  <- Conclusión individual: José Ignacio Gilces Carranza
        │   ├── c-arteaga.tex                 <- Conclusión individual: Danela Dayana Arteaga Alava
        │   ├── c-cedeno.tex                  <- Conclusión individual: Winston Damian Cedeño Avila
        │   └── c-mendoza.tex                 <- Conclusión individual: Allan Jeremy Mendoza Palma
        ├── modelos/                          <- Fuentes editables de modelos y matrices
        │   ├── diagrama-contexto.tex         <- Código fuente editable del Diagrama de Contexto
        │   └── matriz-poder-interes.tex      <- Código fuente editable de la Matriz Poder vs. Interés
        ├── instrumentos/                     <- Instrumentos técnicos de elicitación de campo
        │   ├── consentimiento.tex            <- Plantilla anonimizada del consentimiento informado
        │   ├── guion-entrevista.tex          <- Guion estructurado (12 a 15 preguntas temáticas)
        │   ├── cuestionario.tex              <- Encuesta cerrada y escalada (Likert)
        │   └── guia-observacion.tex          <- Protocolo estructurado de observación en mostrador
        ├── figuras/                          <- Diagramas y capturas exportadas en alta resolución
        └── evidencias/                       <- Registro de evidencias de campo
            └── MANIFIESTO.md                 <- Ledger criptográfico con huellas SHA-256 de archivos privados
```

---

## 🛠️ Instrucciones de Compilación Reproducible (Criterio de Piso P2)

El documento principal `PFC/E1/main.tex` ha sido estructurado en **LaTeX puro** para ser completamente reproducible desde cualquier distribución TeX estándar (**TeX Live 2024 / MiKTeX 24+**).

### 1. Dependencias y Paquetes Requeridos
El motor de compilación requiere los siguientes paquetes incluidos en las colecciones estándar de LaTeX:
* **Tipografía y codificación:** `inputenc` (utf8), `fontenc` (T1), `babel` (spanish), `lmodern`.
* **Maquetación y tablas:** `geometry`, `setspace`, `fancyhdr`, `booktabs`, `longtable`, `tabularx`, `array`, `multirow`.
* **Gráficos y modelado:** `graphicx`, `tikz` (librerías `positioning`, `arrows.meta`, `shapes.geometric`, `fit`, `calc`), `xcolor`, `float`, `caption`.
* **Listas y enlaces:** `enumitem`, `hyperref` (con metadatos PDF), `amssymb`.
* **Estilo bibliográfico:** `IEEEtran.bst` con motor `bibtex`.

### 2. Secuencia de Comandos desde la Terminal

Para regenerar de forma limpia y completa el archivo `main.pdf` resolviendo todas las referencias cruzadas y citas bibliográficas, clone el repositorio y ejecute la siguiente secuencia:

```bash
# 1. Clonar el repositorio y posicionarse en la carpeta de la entrega
git clone https://github.com/josegilcesc/ISR401-PVIA.git
cd ISR401-PVIA/PFC/E1

# 2. Primera pasada de compilación (generación de archivos auxiliares)
pdflatex -interaction=nonstopmode main.tex

# 3. Compilación de la bibliografía (BibTeX con estilo IEEE)
bibtex main

# 4. Segunda pasada de compilación (resolución de citas bibliográficas)
pdflatex -interaction=nonstopmode main.tex

# 5. Pasada final de compilación (resolución completa de referencias cruzadas y tabla de contenidos)
pdflatex -interaction=nonstopmode main.tex
```

> **Verificación de calidad (Rúbrica D5):** Al finalizar la secuencia, el documento `main.pdf` compilará con código de salida `0`, sin referencias rotas (`??`) y con todas las figuras y tablas debidamente citadas y maquetadas dentro de los márgenes.


## 🛠️ Instrucciones de Compilación Reproducible (Criterio de Piso P2)

El documento principal `PFC/E1/main.tex` ha sido estructurado en **LaTeX puro** para ser completamente reproducible desde cualquier distribución TeX estándar (**TeX Live 2024 / MiKTeX 24+**).

⚖️ Declaración de Integridad Académica y Uso de IA
Este repositorio opera bajo el Código de Ética de la ACM y las políticas de integridad académica del Encuadre:

Autoría propia: Todo contenido técnico, modelado, redacción y evidencias de campo corresponden a la autoría y análisis del estudiante o del equipo de trabajo.
Uso ético y declarado de IA: La inteligencia artificial generativa no sustituye el trabajo que se evalúa. Cualquier empleo de herramientas como apoyo auxiliar (por ejemplo, depuración de errores de compilación de LaTeX o revisión ortográfica) se detalla de forma explícita en cada informe entregado indicando: herramienta, versión, propósito exacto y método de verificación manual aplicado.
Control de indicios de IA: Se mantiene estricta rigurosidad para descartar referencias artificiales, citas sin respaldo, alucinaciones o textos genéricos desvinculados del caso de estudio real.

---

## 🔒 Custodia de Evidencias y Protección de Datos Personales (LOPDP)

En estricto cumplimiento con la **Ley Orgánica de Protección de Datos Personales del Ecuador (LOPDP)** y la **Norma de Entrega 7** del encuadre académico:
* **Ningún dato personal sensible de terceros se publica en este repositorio:** Se omiten nombres completos, cédulas, números telefónicos, correos electrónicos y firmas de los participantes, así como la identidad comercial del establecimiento.
* **Custodia institucional privada:** Las grabaciones de audio originales y los consentimientos informados firmados en físico se encuentran almacenados bajo un archivo comprimido cifrado mediante el algoritmo **AES-256** (`PFC-E1_evidencias_cifradas.7z`) en la cuenta institucional UTEQ compartida exclusivamente con el docente evaluador (`gguerrero@uteq.edu.ec`).
* **Verificación de integridad:** La integridad inmutable de cada artefacto privado se encuentra registrada en el archivo [`PFC/E1/evidencias/MANIFIESTO.md`](PFC/E1/evidencias/MANIFIESTO.md) mediante sus respectivas huellas digitales criptográficas **SHA-256**.
