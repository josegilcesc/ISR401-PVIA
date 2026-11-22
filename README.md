# ISR401-PVIA — Plataforma de Ventas con Módulo de Recomendación basado en IA para Establecimientos Eléctricos

Repositorio oficial del equipo para la asignatura **Ingeniería de Requerimientos (ISR-401)**, Cuarto Nivel, Paralelo A — Facultad de Ciencias de la Computación, Universidad Técnica Estatal de Quevedo (UTEQ).

**Periodo Académico:** Segundo Periodo Académico Ordinario (SPA) 2026–2027  
**Docente:** Prof. Gleiston C. Guerrero-Ulloa, PhD (`gguerrero@uteq.edu.ec`)  
**Actividad actual:** TA-PFC-E1 — Proyecto Fin de Curso, Entrega 1: Visión, alcance, partes interesadas, contexto y plan de elicitación.

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

La organización del repositorio se estructura bajo la carpeta de la entrega sumativa `PFC/E1/` conforme al estándar de modularización y reproducibilidad:

```text
ISR401-PVIA/
├── .gitignore                                <- Exclusión de archivos temporales de compilación (.aux, .log, .out, etc.)
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

El documento principal `PFC/E1/main.tex` ha sido desarrollado en **LaTeX estándar** para garantizar compilación limpia y reproducible desde distribuciones TeX modernas (**TeX Live 2024 / MiKTeX 24+**).

### 1. Dependencias y Paquetes Requeridos
El motor requiere la presencia de los siguientes paquetes estándar:
* **Codificación e idioma:** `inputenc` (utf8), `fontenc` (T1), `babel` (spanish).
* **Maquetación y tablas:** `geometry`, `booktabs`, `longtable`, `array`, `multirow`.
* **Gráficos y modelado:** `graphicx`, `tikz`, `pgfplots`, `xcolor`.
* **Referencias bibliográficas:** `biblatex` (con backend `biber` o `bibtex` estándar en formato IEEE).
* **Hipervínculos:** `hyperref` (configurado para enlaces y metadatos).

### 2. Secuencia de Compilación desde Terminal

Para compilar de forma limpia el informe `main.pdf`, resolver referencias cruzadas (`\ref`) y procesar la bibliografía (`\cite`), clone el repositorio y ejecute:

```bash
# 1. Clonar el repositorio y acceder a la carpeta de la entrega
git clone https://github.com/josegilcesc/ISR401-PVIA.git
cd ISR401-PVIA/PFC/E1

# 2. Primera compilación (generación de índices y archivos auxiliares)
pdflatex -interaction=nonstopmode main.tex

# 3. Compilación de bibliografía
bibtex main

# 4. Segunda compilación (resolución de citas bibliográficas)
pdflatex -interaction=nonstopmode main.tex

# 5. Pasada final de compilación (resolución de referencias cruzadas y numeración)
pdflatex -interaction=nonstopmode main.tex
```

> **Verificación de calidad (Rúbrica D5):** La compilación final debe culminar con código de retorno `0`, sin referencias rotas (`??`) y con todas las tablas y figuras contenidas rigurosamente dentro de los márgenes del documento.

---

## 🔒 Protocolo de Ética, Custodia y Datos Personales (LOPDP)

En cumplimiento de la **Ley Orgánica de Protección de Datos Personales del Ecuador** y la **Norma de Entrega 7** de la asignatura:

* **Repositorio público:** No contiene datos personales identificables de terceros (nombres reales de participantes, números de cédula, correos privados, contactos telefónicos, audios originales ni formularios firmados escaneados).
* **Custodia privada:** Las grabaciones de audio originales y los consentimientos físicos firmados se encuentran empaquetados en un contenedor cifrado con algoritmo **AES-256** (`PFC-E1_evidencias_cifradas.7z`), custodiado en la nube institucional privada de la UTEQ y compartido exclusivamente con el docente evaluador (`gguerrero@uteq.edu.ec`).
* **Verificación de integridad:** La inalterabilidad de cada evidencia privada se audita mediante su respectiva huella digital **SHA-256** registrada en el archivo [`PFC/E1/evidencias/MANIFIESTO.md`](PFC/E1/evidencias/MANIFIESTO.md).

---

## ⚖️ Declaración de Integridad Académica y Uso de IA

Este repositorio opera bajo el **Código de Ética de la ACM** y las políticas de integridad académica del **Encuadre de la Asignatura**:

* **Autoría propia:** Todo contenido técnico, modelado, redacción y evidencias de campo corresponden a la autoría y análisis del estudiante o del equipo de trabajo.
* **Uso ético y declarado de IA:** La inteligencia artificial generativa no sustituye el trabajo que se evalúa. Cualquier empleo de herramientas como apoyo auxiliar (por ejemplo, depuración de errores de compilación de LaTeX o revisión ortográfica) se detalla de forma explícita en cada informe entregado indicando: herramienta, versión, propósito exacto y método de verificación manual aplicado.
* **Control de indicios de IA:** Se mantiene estricta rigurosidad para descartar referencias artificiales, citas sin respaldo, alucinaciones o textos genéricos desvinculados del caso de estudio real.
