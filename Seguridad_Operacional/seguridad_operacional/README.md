# Seguridad Operacional y Gestión en Operaciones Aéreas — Manual de 7mo año

Manual del módulo **Seguridad Operacional y Gestión en Operaciones Aéreas** (Entorno: **Legislación Aeronáutica**) de 7mo año de la Tecnicatura en Aviónica, según el **Diseño Curricular 2025** de la Provincia de Buenos Aires. Se dicta en la **E.E.S.T. N° 7 "Taller Regional Quilmes" (IMPA)**, Quilmes, Provincia de Buenos Aires.

Está escrito en **LaTeX** y pensado para compilarse en [Overleaf](https://www.overleaf.com) o en cualquier instalación local de TeX. Edición **Ciclo Lectivo 2026**. Carga horaria: 4 horas semanales (144 horas anuales).

**Autor y docente:** Técnico Aviónico Julián Scicolone — scicolonejulian@impatrq.com

---

## Objetivo

El módulo busca que el futuro técnico aviónico entienda que **trabaja dentro de un sistema regulado**, en el que cada firma tiene valor legal y cada error puede costar vidas. Al terminar el año, el estudiante:

- Conoce el marco legal de la aviación: Convenio de Chicago, OACI y sus Anexos, Código Aeronáutico, ANAC, JST, EANA y las RAAC.
- Sabe qué hace a una aeronave aeronavegable y maneja la documentación técnica: certificados, directivas de aeronavegabilidad, manuales, capítulos ATA y normas AN/MS/NAS.
- Conoce los requisitos de la licencia de **Mecánico de Equipos Radioeléctricos de Aeronaves (MERA)**. Según la **Res. ANAC 443/2025**, el título de Técnico en Aviónica permite tramitarla.
- Comprende el rol del **representante técnico** y la organización de un taller aeronáutico (RAAC 145).
- Aplica herramientas de **factores humanos**: el modelo SHELL, la "docena sucia" (*Dirty Dozen*), el MRM y el método MEDA.
- Diseña e implementa un **Sistema de Gestión de la Seguridad Operacional (SMS)** según el Anexo 19 de la OACI.

La **Hoja de ruta del estudiante** (al inicio del manual) lista los 18 logros que cada estudiante tiene que completar durante el año.

---

## Contenido

| Archivo | Sección |
|---|---|
| `caratula.tex` | Carátula |
| `presentacion.tex` | Presentación de la materia: datos, fundamentación, objetivos, organización, metodología y hoja de ruta |
| `u1_derecho.tex` | **Unidad 1 – Derecho aeronáutico:** fuentes, convenios internacionales, OACI y sus 19 Anexos, libertades del aire, FAA, EASA y SRVSOP, Código Aeronáutico y reformas, organismos argentinos, RAAC, rol regulador del Estado |
| `u2_certificacion.tex` | **Unidad 2 – Aeronavegabilidad y certificación:** certificados tipo y de aeronavegabilidad, directivas de aeronavegabilidad (AD), RAAC 43, registros, manuales (AMM, IPC, WDM, MEL), partes y 8130-3, capítulos ATA, normas AN/MS/NAS/MIL, ARINC y RTCA |
| `u3_licencias.tex` | **Unidad 3 – Licencias y responsabilidad técnica:** RAAC 65, licencia MERA, atribuciones y obligaciones, representante técnico, oficina técnica |
| `u4_organizaciones.tex` | **Unidad 4 – Organizaciones aeronáuticas:** operadores y talleres, programa de mantenimiento, abastecimiento, indicadores, economía de la operación, calidad, ambiente y salud laboral |
| `u5_factores.tex` | **Unidad 5 – Actuación humana:** SHELL, factores que afectan el rendimiento, docena sucia, error humano, MRM, cultura justa, MEDA, primeros auxilios |
| `actividad_mrm.tex` | Actividad práctica: simulación de pase de turno (MRM) con planillas |
| `u6_seguridad.tex` | **Unidad 6 – Prevención de accidentes:** riesgo y peligro, enfoques de causalidad (Heinrich, Reason, sistémico), investigación (Anexo 13, JST), matriz de riesgos, SMS (Anexo 19, Doc 9859), costos de los accidentes, casos reales |
| `u7_operaciones.tex` | **Unidad 7 – Operaciones aéreas:** tipos de operación, servicios de tránsito aéreo, clases de espacio aéreo, cartas aeronáuticas, AIP y NOTAM |
| `proyecto_sms.tex` | Proyecto integrador: SMS del taller de aviónica de la escuela |

Recursos:

- `logos/` — logos de la Provincia de Buenos Aires y de IMPA (PDF).
- `logos/organismos/` — logos de los organismos del sistema aeronáutico usados en la tabla 3.2 (Secretaría de Transporte, ANAC, JST, EANA, ORSNA, PSA, Fuerza Aérea Argentina, SMN). Si falta alguno, el manual muestra un recuadro con la sigla. Los nombres de archivo están en `LEEME.txt`.

---

## Cómo compilar

### En Overleaf

1. Descargar el repositorio como `.zip` (botón **Code → Download ZIP**).
2. En Overleaf: **New Project → Upload Project** y elegir el zip.
3. Verificar que el compilador sea **pdfLaTeX** (Menu → Compiler).
4. Compilar `main.tex`.

### En una instalación local

Se necesita una distribución TeX completa (TeX Live o MiKTeX).

```bash
pdflatex main.tex
pdflatex main.tex   # segunda pasada para referencias
```

Paquetes utilizados: `lmodern`, `babel` (spanish), `geometry`, `graphicx`, `tikz`, `xcolor`, `enumitem`, `fancyhdr`, `array`, `titlesec`, `tcolorbox`.

---

## Cómo modificarlo

- Cada unidad está en su propio archivo `.tex`. Para **quitar o reordenar** una unidad, comentá o mové su línea `\input{...}` en `main.tex`.
- Para **agregar** una unidad nueva, creá un archivo `.tex` que empiece con `\clearpage` y `\section*{...}`, y sumá su `\input{...}` en `main.tex`.
- El encabezado y el pie de página se definen en `main.tex` (estilo `materia`). Para cambiar el año, la materia o el mail, editá el bloque `\fancypagestyle{materia}{...}`.
- Los recuadros destacados usan el entorno `recuadro`:

```latex
\begin{recuadro}
Texto destacado.
\end{recuadro}
```

- Las casillas de verificación de la hoja de ruta usan el comando `\casilla`.

---

## Datos que hay que revisar cada año

La normativa aeronáutica argentina está en plena actualización. Antes de cada ciclo lectivo conviene revisar:

- **Código Aeronáutico (Ley 17.285)** y sus modificaciones por DNU (70/2023, 941/2024, 338/2025 y posteriores).
- Enmiendas de las **RAAC**, en particular las Partes 21, 43, 65, 91, 121, 135, 145 y 147, que la ANAC está alineando con las normas de la FAA y la EASA.
- Requisitos vigentes para la **licencia MERA** y el alcance de la Res. ANAC 443/2025.
- Nuevas ediciones de los documentos de la OACI (Anexos 13 y 19, Doc 9859).
- Informes finales de la **JST** y la **NTSB** sobre los casos citados.

El Diseño Curricular menciona una "RAAC 143", que no existe como parte vigente; el manual trabaja con la **Parte 43 (Mantenimiento)**.

---

## Créditos

- Contenidos y edición: **Téc. Aviónico Julián Scicolone**.
- Programa basado en el Diseño Curricular 2025 (IF-2025-41581603-GDEBA-DETECDGCYE).
- Logos de los organismos: propiedad de cada institución, usados con fines educativos.
- E.E.S.T. N° 7 "Taller Regional Quilmes" — Dirección General de Cultura y Educación de la Provincia de Buenos Aires.
