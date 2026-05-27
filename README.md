# APA español Manual Moderno 4ª edición CSL

Estilo CSL para generar citas y referencias en formato APA 7 en español, siguiendo como referencia el **Manual de publicaciones de la American Psychological Association, 4ª edición en español, Editorial El Manual Moderno**, junto con la corrección de uso de `y` en lugar de `&` para textos en español.

Este repositorio no es oficial de APA, Zotero ni Editorial El Manual Moderno. Es una adaptación práctica basada en el estilo oficial `apa.csl` del proyecto Citation Style Language.

## Archivo principal

- `apa-español-mm4-actualizado.csl`: estilo recomendado para instalar en Zotero, Mendeley u otro gestor compatible con CSL.
- `revision-cumplimiento-apa-mm4.md`: nota técnica con el resumen de revisión contra el manual.

## Qué incluye

- Base oficial APA CSL actualizada.
- Localización por defecto en español (`es-ES`).
- Uso de `y` como conector entre autores.
- DOI en formato `https://doi.org/...`.
- Citas autor-fecha.
- `et al.` desde tres autores en citas en texto.
- Lista de referencias con sangría francesa y doble espacio.
- Hasta 20 autores en referencias; desde 21 autores, 19 autores + puntos suspensivos + autor final.
- Fechas de recuperación en forma española: `Recuperado el [fecha], de [URL]`.

## Limitaciones

Un archivo CSL no puede garantizar por sí solo el cumplimiento completo del manual. El resultado final también depende de que los metadatos estén bien cargados en el gestor bibliográfico.

Revise especialmente:

- Mayúsculas y minúsculas de títulos.
- Tipo correcto de fuente: artículo, libro, capítulo, tesis, página web, etc.
- Nombres de autores grupales y abreviaturas.
- URLs que deben omitirse en bases de datos comunes.
- Fuentes no recuperables o comunicaciones personales.
- Formato general del documento: márgenes, tablas, figuras, encabezados y redacción.

## Cómo instalar en Zotero

1. Descargue el archivo `apa-español-mm4-actualizado.csl`.
2. Abra Zotero.
3. Vaya a `Editar > Ajustes > Citar > Estilos`.
4. Seleccione el botón `+`.
5. Elija el archivo `.csl`.
6. Busque el estilo como `APA Style 7th edition - español Manual Moderno 4ª edición`.


## Licencia

El estilo deriva del repositorio oficial de Citation Style Language y conserva la licencia **Creative Commons Attribution-ShareAlike 3.0** indicada en el archivo CSL original.

Fuente base: https://github.com/citation-style-language/styles/blob/master/apa.csl
