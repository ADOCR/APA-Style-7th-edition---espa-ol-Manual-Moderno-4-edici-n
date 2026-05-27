# Revisión de cumplimiento APA Manual Moderno 4ª edición

Archivo revisado: `apa-español-mm4-actualizado.csl`

Referencia usada: `manual de publicaciones apa 4ta edicion.pdf` y la guía/fe de erratas en español revisada antes.

## Dictamen

El estilo cumple razonablemente con APA 7 / Manual Moderno 4ª edición en todo lo que un archivo CSL puede automatizar. La copia revisada está basada en el `apa.csl` oficial de CSL actualizado el 2026-02-07 y tiene ajustes para español.

No es posible afirmar cumplimiento absoluto de "todo" el manual solo con CSL, porque muchas reglas dependen de los datos cargados por la persona usuaria: mayúsculas de títulos, elección correcta del tipo de fuente, abreviaturas de autores grupales, si una URL debe omitirse, si una fuente es recuperable, y reglas de formato del documento como márgenes, tablas, figuras, encabezados y redacción.

## Cambios aplicados en la copia revisada

- Se fijó el idioma por defecto en español: `default-locale="es-ES"`.
- Se conservó la base oficial APA más reciente disponible del repositorio CSL.
- Se reemplazaron conectores forzados con `&` por conectores de texto para que el estilo use `y`.
- Se agregó la forma española para fechas de recuperación: `Recuperado el [fecha], de [URL]`.
- Se asignó un identificador propio al estilo para no sobrescribir el APA oficial.

## Cumplimiento verificado

| Regla del manual | Estado | Observación |
| --- | --- | --- |
| Sistema autor-fecha | Cumple | La cita usa autor, año y localizador cuando aplica. |
| Citas parentéticas con varias obras separadas por punto y coma | Cumple | El `layout` usa `delimiter="; "`. |
| Tres o más autores como `et al.` desde la primera cita | Cumple | `citation et-al-min="3" et-al-use-first="1"`. |
| Desambiguación por año/letras, nombres e iniciales | Cumple | Tiene reglas de desambiguación activas. |
| Lista de referencias con sangría francesa y doble espacio | Cumple | `hanging-indent="true"` y `line-spacing="2"`. |
| Hasta 20 autores en referencias; desde 21, 19 + puntos suspensivos + último autor | Cumple | `bibliography et-al-min="21" et-al-use-first="19" et-al-use-last="true"`. |
| DOI en formato actual `https://doi.org/...` | Cumple | El macro de DOI antepone `https://doi.org/`. |
| Si hay DOI y URL, usar DOI | Cumple | El macro prioriza DOI antes que URL. |
| No poner punto final después de DOI o URL | Cumple | DOI/URL se emiten fuera del grupo que agrega punto. |
| Fecha de recuperación para obras cambiantes | Cumple tras ajuste | Queda como `Recuperado el ... de ...`. |
| Sin fecha como `s. f.` | Cumple según localidad española | Depende del procesador CSL y de `default-locale="es-ES"`. |
| Editorial sin lugar de publicación | Cumple | El estilo no usa lugar editorial para libros/reportes. |
| Capítulos de libro con `En`, editores, páginas y editorial | Cumple en la base oficial APA | Depende de que el item esté cargado como capítulo y tenga contenedor/editor/páginas. |
| Artículos con revista, volumen, número, páginas/artículo y DOI | Cumple | Sigue la estructura de fuentes periódicas de APA. |
| Obras sin autor usando el título en posición de autor | Cumple | El estilo sustituye autor por título/descripción. |
| Comunicaciones personales no recuperables solo en texto | Cumple parcialmente | CSL puede omitirlas de la bibliografía si no tienen datos recuperables; el usuario debe clasificar bien la fuente. |
| Autores grupales con abreviatura en primera cita y abreviada después | No totalmente automatizable | CSL no puede decidir ni recordar abreviaturas institucionales de forma perfecta. |
| Títulos en sentence case y nombres propios correctos | Depende de datos | CSL no debe corregir automáticamente todos los títulos porque puede dañar nombres propios. |
| Omisión de URLs de bases de datos comunes | Depende de datos | Si el campo URL está lleno, el estilo tiende a imprimirlo; la decisión normativa exige limpieza de metadatos. |

## Punto delicado: `&` frente a `y`

El manual impreso muestra `&` en citas parentéticas y referencias con varios autores. Sin embargo, la guía/fe de erratas en español indica usar `y` en lugar de `&` para textos en español. Por eso esta copia revisada sigue el criterio español actualizado y usa `y`.

Si alguien exige seguir literalmente el manual impreso sin aplicar la fe de erratas, habría que crear otra variante estricta que conserve `&` en citas parentéticas y referencias.

## Conclusión

La versión recomendada es `apa-español-mm4-actualizado.csl`. Cumple con la estructura APA actual y con los ajustes principales del español. Para que el resultado final cumpla en documentos reales, también hay que revisar los metadatos de cada referencia en Zotero/Mendeley/Word.
