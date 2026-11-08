# TA-IND-01 — IEEE 29148 y tipos de requisitos de Temu

**Universidad:** Universidad Técnica Estatal de Quevedo (UTEQ)  
**Carrera:** Software · 4.º nivel · Paralelo B  
**Asignatura:** Ingeniería de Requerimientos (ISR-401)  
**Docente:** Gleiston Cicerón Guerrero Ulloa, PhD  
**Estudiante:** Mendoza Palma Allan Jeremy  
**Sistema analizado:** Temu, aplicación móvil y plataforma web de comercio electrónico  
**Formato:** IEEEtran a una sola columna; referencias IEEE con BibTeX

## Propósito del trabajo

Aplicar los criterios de construcción y calidad de requisitos de **ISO/IEC/IEEE 29148:2018** a funciones y escenarios de compra en Temu. Los enunciados se presentan como **requisitos propuestos para un ejercicio académico**: sus métricas son objetivos de especificación y no estadísticas, pruebas realizadas ni compromisos oficiales de la plataforma.

## Estado de esta versión

**Commit 2 — Especificación y clasificación de requisitos**

Se conserva íntegro el análisis del primer avance y se añaden los requisitos propuestos para Temu con su clasificación y criterios de aceptación.

### Contenido incorporado en este commit

- Todo el contenido del commit 1, sin eliminar el resumen ni el glosario.
- Quince requisitos organizados por categorías: funcionales, interfaz, desempeño, calidad y otras restricciones o necesidades aplicables.
- Cinco requisitos de calidad con característica, subcaracterística, métrica y umbral propuesto según ISO/IEC 25010:2023.
- Tabla consolidada con identificadores, enunciados, tipos y criterios de aceptación.
- Cuatro figuras con referencias cruzadas: todavía se muestran marcadores en lugar de capturas reales.

**Situación de las evidencias:** Los cuadros «Captura pendiente» son intencionales en este avance; no representan imágenes tomadas ni verificaciones ejecutadas.

**Estado del documento:** El PDF del segundo avance es un borrador acumulativo, no una evidencia de funcionamiento medido en Temu.

## Organización del proyecto

```text
ISR401-MendozaAllan/
└── TA-IND-01/
    ├── TA-TAR-01.text       # Código LaTeX editable
    ├── TA-TAR-01.tex        # Copia de compilación del mismo código
    ├── TA-TAR-01.bib        # Fuentes bibliográficas IEEE
    ├── README.md            # Información y reproducción
    └── figuras/
        └── .gitkeep         # Carpeta reservada para capturas
```

El archivo **`TA-TAR-01.text`** contiene código LaTeX; para procesarlo directamente con PDFLaTeX se conserva una copia idéntica llamada **`TA-TAR-01.tex`**. El archivo de salida se denomina **`TA-TAR-01.pdf`**.

> **Nota de nomenclatura:** la guía de TA-IND-01 menciona también `main.tex` y `main.pdf` como nombres esperados en el repositorio. Aquí se utilizan los nombres `TA-TAR-01.*` solicitados para el trabajo; antes de la entrega conviene comprobar si el docente exige adicionalmente aquellos alias. La carpeta del repositorio se mantiene como `TA-IND-01/`, conforme a la guía.

## Requisitos de compilación

Instalar **TeX Live** o **MiKTeX** con PDFLaTeX y BibTeX. El proyecto utiliza la clase `IEEEtran`, el estilo `IEEEtran.bst` y los paquetes `fontenc`, `inputenc`, `babel` (español), `lmodern`, `microtype`, `csquotes`, `amsmath`, `amssymb`, `graphicx`, `booktabs`, `tabularx`, `array`, `longtable`, `float`, `url`, `cite`, `hyperref` y `enumitem`.

Abrir una terminal **dentro de `TA-IND-01/`**, donde se encuentran los archivos `.tex` y `.bib`, y ejecutar:

```bash
pdflatex -interaction=nonstopmode -halt-on-error TA-TAR-01.tex
bibtex TA-TAR-01
pdflatex -interaction=nonstopmode -halt-on-error TA-TAR-01.tex
pdflatex -interaction=nonstopmode -halt-on-error TA-TAR-01.tex
```

**Importante:** el comando correcto es `bibtex TA-TAR-01`, no `bibtex main`, porque PDFLaTeX genera `TA-TAR-01.aux` a partir del archivo principal `TA-TAR-01.tex`.

Al terminar, el archivo generado se llama `TA-TAR-01.pdf`. Si se compila desde Overleaf, seleccionar `TA-TAR-01.tex` como documento principal y usar BibTeX.

## Capturas y trazabilidad de evidencia

Las imágenes deben proceder de la cuenta o sesión personal del estudiante. La macro LaTeX comprueba la existencia de cada PNG: si falta, el PDF muestra un recuadro provisional; si existe, inserta la captura.

| Figura | Archivo esperado | Funcionalidad de Temu |
|---|---|---|
| 1 | `figuras/captura1.png` | Catálogo o búsqueda de productos |
| 2 | `figuras/captura2.png` | Carrito y pantalla del proceso de pago |
| 3 | `figuras/captura3.png` | Seguimiento de un pedido |
| 4 | `figuras/captura4.png` | Configuración de cuenta o privacidad |

Antes de publicar capturas, ocultar datos personales, direcciones, medios de pago, identificadores de pedidos y cualquier información de terceros. Las capturas ilustran elementos observables de la interfaz; **no prueban por sí solas** los tiempos de respuesta, la disponibilidad o el cumplimiento de umbrales de calidad.

## Fuentes y criterios de revisión

- **ISO/IEC/IEEE 29148:2018:** construcción, revisión individual y del conjunto, lenguaje y atributos de los requisitos.
- **ISO/IEC 25010:2023:** características y subcaracterísticas para clasificar los requisitos de calidad.
- **Pohl (2025)** y **SWEBOK Guide v4.0 (2024):** referencias complementarias de fundamentos de ingeniería de requisitos.

Las citas del texto se resuelven desde `TA-TAR-01.bib`. Antes de entregar, comprobar contra los documentos originales la correspondencia entre las cláusulas citadas y cada afirmación; las propuestas del informe no constituyen una evaluación certificada de Temu.

## Continuidad del trabajo

El tercer avance completará la autoevaluación, las correcciones y las secciones de cierre; las capturas reales se insertan cuando estén disponibles.

Las fechas de los commits deben corresponder a los días de trabajo reales. Cada versión de este proyecto es acumulativa: no reemplaza el contenido anterior por un documento parcial.
