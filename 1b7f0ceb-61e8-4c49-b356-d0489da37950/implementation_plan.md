# Plan de Implementación: Arquitectura Lógica de Alta Densidad Extrema (V4)

## Objetivo
Generar un diagrama de arquitectura lógica masivo (mínimo 150 nodos) extraído desde cero. La extracción documentará cada idea, concepto, autor, metodología y tecnología, agrupándolos estrictamente bajo su respectiva sección en el documento fuente (Introducción, Planteamiento del Problema, Objetivos, etc.).

## Estrategia de Extracción "Ciega" e Iterativa (Clean Slate)
No me basaré en versiones previas del grafo. Trataré `Plantilla.tex` como un documento virgen.

1. **Partición Rigurosa (Map):**
   Leeré el documento `Plantilla.tex` rigurosamente en bloques de 250 líneas.
   - Bloque 1: Líneas 1 a 250 (Preámbulo, Resumen, Primera parte).
   - Bloque 2: Líneas 251 a 500 (Introducción, Problema, Objetivos, Justificación, Antecedentes inicio).
   - Bloque 3: Líneas 501 a 750 (Antecedentes fin, Marco Teórico, Metodología).
   - Bloque 4: Líneas 751 a 874 (Metodología fin, Presupuesto, Referencias).

2. **Extracción Atómica por Bloque:**
   Por cada bloque leído, generaré un archivo temporal (ej. `temp_v4_chunk1.json`, etc.). 
   En estos volcados, las ideas atómicas estarán obligatoriamente taggeadas con su **Sección de Origen**.
   Se extraerá una granularidad extrema: cada afirmación clave, cada autor referenciado y cada paso metodológico será un nodo independiente.

3. **Síntesis y Ontología Estructural (Reduce):**
   Leeré todos los archivos temporales consolidados.
   Agruparé los grafos de Mermaid utilizando `subgraphs` que correspondan a las macro-secciones del documento.
   Las conexiones cruzarán de sección a sección para demostrar cómo se hila argumentativamente el documento.

4. **El Entregable (Artifact):**
   Generaré el archivo `arquitectura_logica_v4.md` con un código de Mermaid que albergará la totalidad de las ideas extraídas organizadas bajo un enfoque de Marco Lógico Extendido (incluyendo las secciones formales del documento).
