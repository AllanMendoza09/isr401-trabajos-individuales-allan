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

**Commit 3 — Autoevaluación y documento de entrega**

Se conserva el informe de los dos avances anteriores y se agregan las correcciones de redacción, el análisis de dificultades y la declaración de apoyo de IA.

### Contenido incorporado en este commit

- Todo el contenido de los commits 1 y 2.
- Autoevaluación de los quince requisitos con referencia a las nueve propiedades de calidad y a las reglas de lenguaje.
- Tabla comparativa de versiones iniciales defectuosas y enunciados corregidos.
- Reflexión sobre la dificultad de cuantificar requisitos de calidad, redactada como borrador revisable.
- Declaración de asistencia de IA y referencias en formato IEEE.
- Espacios automáticos para cuatro capturas propias de Temu; se sustituyen al añadir los archivos PNG.

**Situación de las evidencias:** Esta versión compila sin las imágenes, pero no debe darse por terminada hasta incorporar capturas auténticas y revisar personalmente la reflexión, el uso declarado de IA y las cláusulas normativas.

**Estado del documento:** El PDF final se debe regenerar después de colocar las cuatro capturas y verificar que no aparezca «Captura pendiente».

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



