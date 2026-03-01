# Walkthrough: Arquitectura Lógica y Auditoría del Anteproyecto

Este documento resume el trabajo realizado para modelar y auditar la estructura lógica de tu anteproyecto de maestría.

## 1. Mapeo Semántico y Zettelkasten

Se realizó una lectura profunda de `Plantilla.tex` (y usando `contexto_proyecto.md` como guía) para extraer "Zettels" (ideas atómicas) clave que trascienden las secciones formales del documento. Algunas de estas ideas clave capturadas fueron:
*   La escritura humana fragmenta las ideas en documentos extensos (Problema).
*   Los LLMs sufren de Amnesia Contextual y no razonan estructuralmente (Problema).
*   Los Grafos de Conocimiento aportan un "Ground Truth" para superar esta amnesia (Solución/Tecnología).
*   Los SLMs permiten hacer esta extracción Text-to-Graph a bajo costo computacional (Solución/Tecnología).
*   Los Agentes operan como módulos de verificación sin reemplazar al investigador (Metodología/Tecnología).

## 2. Construcción del Grafo Lógico en Mermaid

Con base en la abstracción del **Marco Lógico**, se construyó un diagrama de flujo en Mermaid dentro del archivo `arquitectura-lógica.md`. La topología se estructuró en 4 capas para evidenciar las conexiones:

1.  **Capa Teleológica (Fin/Propósito):** Conecta el Título $\rightarrow$ Pregunta de Investigación $\rightarrow$ Objetivo General.
2.  **Capa del Problema Central (Justificación):** Detalla las debilidades actuales (amnesia contextual, fisuras lógicas).
3.  **Capa Tecnológica (Transversal):** Muestra cómo los KGs, SLMs y Agentes actúan como el motor que da solución a los problemas planteados. Esta capa cruza transversalmente el grafo, demostrando que la tecnología no es un fin en sí misma, sino el medio articulador.
4.  **Envolvente Metodológico (Actividades y Resultados):** Desglosa la impecable relación 1:1 entre los Objetivos Específicos (O.E. 1 al 4) y sus Fases correspondientes (Fase 1 a 5), finalizando en entregables concretos.

## 3. Análisis Crítico y Auditoría de Coherencia

Tras construir el grafo, evaluamos las conexiones ("Top-Down" y "Bottom-Up"), lo que nos permitió identificar:

*   **Alta Coherencia:** El proyecto tiene una alineación vertical excepcional. La tecnología seleccionada (KG + SLM) justifica y atiende de manera directa el problema central (Amnesia Contextual). La metodología es muy clara.
*   **Áreas de Mejora (Alertas Metodológicas):**
    *   **Vacío 1:** Falta explicar explícitamente en el O.E.2 o Fase 2 cómo el SLM poblará el Grafo de Conocimiento (Text-to-Graph).
    *   **Vacío 2:** La taxonomía de la Fase 1 debe diseñarse pensando en que será ejecutada por consultas `Cypher` en la Fase 5, no puede ser puramente teórica.
    *   **Vacío 3:** No se menciona un mecanismo claro sobre cómo el Grafo de Conocimiento se actualizará (control de versiones / "Ground Truth" dinámico) al interactuar interactivamente con el usuario.

El resultado final es el archivo `arquitectura-lógica.md` en tu directorio de proyecto, que contiene el código Mermaid listo para previsualizar y el reporte completo de las alertas metodológicas.
