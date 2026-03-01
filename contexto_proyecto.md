# Contexto del Proyecto de Investigación — Anteproyecto de Maestría UAO

> Este archivo es un levantamiento estructurado del contenido del anteproyecto, construido a partir de `Plantilla.tex`.
> Sirve como memoria de contexto para asistencia en redacción, revisión y evolución del documento.

---

## 1. Datos Generales

| Campo | Valor |
|---|---|
| **Estudiante** | Jorge Andrés Jaramillo Neme |
| **Cédula** | 1.144.084.317 |
| **Código Estudiantil** | 22505049 |
| **Correo** | Jorge_and.jaramillo@uao.edu.co |
| **Programa** | Maestría en Inteligencia Artificial y Ciencia de Datos |
| **Universidad** | Universidad Autónoma de Occidente (UAO), Santiago de Cali |
| **Director** | Javier Ferney Castillo García |
| **Correo Director** | jfcastillo@uao.edu.co |
| **Año** | 2025 |

**Perfil del Director:**
- Ph.D. en Ingeniería Eléctrica y Electrónica, 2015, Universidad del Valle
- Magíster en Ingeniería Eléctrica, 2014, Universidade Federal do Espírito Santo, Brasil
- Magíster en Automática, 2009, Universidad del Valle
- Ingeniero Electrónico, 2004, Universidad del Valle

---

## 2. Título del Proyecto

**Desarrollo de un sistema agéntico basado en grafos de conocimiento y modelos de lenguaje pequeños para la verificación estructural automatizada de propuestas de investigación**

---

## 3. Palabras Clave

- **Español:** Sistemas Agénticos, modelos pequeños de lenguaje, ingeniería de contexto, grafos de conocimiento
- **Inglés:** Agentic AI, Small Language Models, Context Engineering, Knowledge Graphs

---

## 4. Resumen

El proyecto aborda la problemática de la **coherencia y consistencia estructural** en documentos de investigación académica (anteproyectos, proyectos y artículos científicos).

**Problema central:** A pesar de los avances en LLMs, persiste la dificultad de garantizar alineación rigurosa entre problema, objetivos, metodología y sustento teórico. Los LLMs sufren "amnesia contextual" y limitan la preservación de relaciones causales en textos extensos.

**Objetivo general:** Diseñar e implementar un prototipo de **sistema agéntico copiloto** basado en ingeniería de contexto, que integre **grafos de conocimiento (KG)** y **modelos de lenguaje pequeños (SLM)**, para asistir en la evaluación de coherencia y consistencia de proyectos de investigación.

**Enfoque metodológico:** Aplicado–experimental, predominio cuantitativo con componente cualitativo.

**Fases del proyecto:**
1. Análisis conceptual y documental de estructuras metodológicas y criterios de coherencia
2. Modelado semántico mediante ontología e implementación en grafo de conocimiento
3. Diseño de arquitectura agéntica y módulos cognitivos (lectura, verificación, razonamiento, navegación, memoria contextual)
4. Implementación del prototipo (KG + SLM + flujos multi-agente)
5. Evaluación híbrida: métricas automáticas + valoración experta en entorno controlado

**Resultado esperado:** Un copiloto cognitivo capaz de representar las relaciones entre problema, objetivos, metodología y literatura; detectar desalineaciones; y ofrecer retroalimentación accionable.

---

## 5. Introducción

La introducción contextualiza el proyecto a través de una narrativa histórica:

1. **Contexto histórico:** La ciencia evolucionó desde la intuición hacia el método científico y la formulación de proyectos de investigación como arquitectura intelectual.
2. **Era digital:** Las herramientas colaborativas facilitaron la escritura pero no resolvieron el desafío estructural de mantener alineación lógica entre problema, objetivos y metodología.
3. **Paradoja de los LLMs:** GPT/BERT son excelentes redactores pero deficientes metodólogos — sufren "amnesia contextual" y generan propuestas con fisuras lógicas.
4. **Pertinencia actual:** En la competitividad académica global (publicaciones Q1/Q2, financiación), la solidez estructural de los documentos es factor diferenciador.
5. **Respuesta propuesta:** Ingeniería de Contexto + Sistemas Agénticos + Grafos de Conocimiento + SLMs = nueva generación de asistentes que validan la estructura profunda de una propuesta.

**Propuesta de valor:** No solo uso de sistemas agénticos, sino una estrategia de ingeniería de contexto más elaborada y personalizada que garantice coordinación, planeación y visibilidad, mitigando alucinaciones y asegurando rigor crítico.

---

## 6. Planteamiento del Problema

### 6.1 Descripción del problema

- Los documentos metodológicos exigen integrar grandes volúmenes de información con consistencia entre objetivos, metodología y resultados.
- Las IAs generativas actuales operan en el plano lingüístico (predicción estadística), sin comprender relaciones causales/jerárquicas → **amnesia contextual/estructural**.
- Las soluciones RAG abordan factualidad pero no consistencia lógica interna.
- La **Ingeniería de Contexto** emerge para resolver esta brecha mediante arquitecturas que superan la amnesia contextual.
- Los **Grafos de Conocimiento** ofrecen representación explícita como "Ground Truth" dinámico para trazabilidad estructural.
- Los **Sistemas Agénticos** permiten orquestar flujos documentales complejos (ej. Verify-Agent, MMA-RAG).
- Los **SLMs** son la vía técnica para extracción semántica eficiente (Text-to-Graph) con bajo costo operacional.

### 6.2 Vacío identificado

> Inexistencia de una arquitectura de Ingeniería de Contexto que utilice el KG como **motor de estado** y los SLMs como **extractores eficientes** para habilitar la Verificación Estructural Automatizada de documentos de investigación.

### 6.3 Pregunta de Investigación

> ¿Cómo una estrategia de ingeniería de contexto basada en grafos de conocimiento, apoyada en modelos de lenguaje pequeños (SLMs), mejora la capacidad de un sistema agéntico para **reducir las inconsistencias lógicas** y fortalecer la coherencia y consistencia de propuestas de investigación?

---

## 7. Objetivos

### 7.1 Objetivo General

Desarrollar un prototipo de sistema agéntico copiloto que incorpore una arquitectura de ingeniería de contexto basada en grafos de conocimiento y Small Language Models (SLMs), para asistir la **evaluación automatizada de la coherencia y consistencia** de proyectos de investigación.

### 7.2 Objetivos Específicos

1. **Analizar** las estructuras y componentes de los proyectos de investigación, identificando los criterios de coherencia y consistencia relevantes para su evaluación automatizada.

2. **Diseñar** un modelo semántico-ontológico, implementado como grafo de conocimiento, que represente las relaciones y dependencias lógicas entre los componentes estructurales de los proyectos de investigación.

3. **Implementar** la arquitectura de ingeniería de contexto del sistema agéntico copiloto, integrando el grafo de conocimiento y los SLMs para apoyar el procesamiento y estructuración del contenido textual.

4. **Validar** el desempeño sistémico y la efectividad del prototipo agéntico para diagnosticar y fortalecer la coherencia y consistencia metodológica, mediante técnicas especializadas de evaluación de LLM y sistemas agénticos en un entorno controlado.

---

## 8. Justificación y Alcance

### Justificación

- Los sistemas actuales basados en LLMs operan sobre texto plano y carecen de mecanismos para preservar conocimiento estructurado → no validan coherencia interna ni consistencia lógica.
- La estrategia propuesta (KG + SLMs + arquitectura agéntica) permite **distribuir tareas cognitivas**: verificación de coherencia entre secciones, evaluación de consistencia terminológica, comprobación de soporte bibliográfico.
- El **grafo de conocimiento actúa como memoria contextual y soporte de razonamiento**.

### Alcance

El sistema tendrá **dos capacidades principales:**
1. Evaluar la coherencia y consistencia interna entre los componentes estructurales del proyecto
2. Contrastar dichos componentes con artículos y referencias aportadas por el usuario, valorando relevancia y alineación temática

**Límites del alcance:**
- Escenario controlado de proyectos de investigación académica
- Conjunto acotado de componentes y referencias
- **No** cubre todo el ciclo de vida de la investigación
- **No** sustituye el criterio del investigador
- Es un **prototipo**, no un sistema de producción

---

## 9. Antecedentes y Estado del Arte

Los antecedentes cubren cuatro grandes bloques temáticos:

### 9.1 Transformers y LLMs
- Arquitectura Transformer (Vaswani, 2017) → mecanismos de atención en paralelo → capacidad de capturar dependencias a largo plazo
- Emergió el comportamiento emergente en LLMs (GPT, BERT, T5): razonamiento, planificación, adaptación contextual
- Surgimiento de **AI Agents**: entidades que usan LLM como núcleo cognitivo para interactuar con entorno, tomar decisiones y cumplir objetivos

### 9.2 Sistemas Agénticos (Agentic AI)
- Evolución de AI Agent a **Agentic AI Systems**: múltiples agentes especializados con módulos de razonamiento, memoria y planificación
- Incluyen: memoria semántica/episódica/procedimental, mecanismos de handoff y cueing
- Marcos de evaluación: razonamiento multietapa, uso de herramientas, reflexión, persistencia de memoria

### 9.3 RAG y sus evoluciones
- **RAG clásico (Lewis, 2021):** recuperador externo + generador interno. Limitaciones: fragmentación de contexto, no maneja consistencia lógica interna
- **GraphRAG:** recuperación estructurada sobre grafos → consultas semánticas, razonamiento multihop, trazabilidad
- **Agentic RAG:** agentes especializados (recuperar, verificar, sintetizar) con memoria compartida y reflexión distribuida

### 9.4 Razonamiento Multihop y Grafos de Conocimiento
- Razonamiento multihop: combinar información de múltiples fuentes/pasos para responder consultas complejas (SMORE)
- KGs: tripletas (sujeto, predicado, objeto) → representación formal, navegable y razonable
- En documentos: permite vincular secciones y evaluar si objetivos derivan del problema, o si metodología responde a hipótesis
- KGs como memoria a largo plazo para agentes

### 9.5 Sistemas Copiloto Documentales
- Docpilot (Adobe Research, Mathur 2024): planificación → verificación → autocorrección → ejecución — agencia dentro del procesamiento documental

---

## 10. Marco Teórico

Tres ejes conceptuales principales:

### 10.1 Sistemas Agénticos vs. Agentes de AI

- **AI Agent tradicional:** entidad individual, tareas específicas, reglas preestablecidas
- **Agentic AI System:** conjunto coordinado de agentes especializados, memoria compartida, razonamiento iterativo, autoevaluación

**Componentes de un sistema agéntico (según Khamis, 2025):**
- Modelo base / núcleo cognitivo (LLM o LRM)
- Módulos cognitivos especializados (lectura, análisis, evaluación, verificación)
- Sistema de memoria: semántica (conocimiento estable), episódica (experiencias previas), procedimental (estrategias)
- Mecanismos de coordinación: handoff (transferencia de tareas), cueing (activación contextual)
- Entorno de acción: bases de datos, grafos, interfaces de usuario

### 10.2 Grafos de Conocimiento

- Estructura: nodos y aristas dirigidas → tripletas (sujeto, predicado, objeto)
- Se apoyan en **ontologías**: clases, relaciones jerárquicas, restricciones lógicas (OWL, RDF)
- Relevantes en ML y razonamiento simbólico; base para modelos de incrustación (Knowledge Graph Embedding)
- Propiedades estructurales del grafo (grado de nodos, frecuencia de relaciones) impactan la calidad del aprendizaje
- El diseño ontológico cuidadoso es esencial en dominios donde la consistencia semántica es crítica

### 10.3 Retrieval-Augmented Generation (RAG)

- RAG básico → RAG con rerankers → **GraphRAG** (KG como base de recuperación) → **Agentic RAG** (agentes especializados)
- Tendencia: de simple recuperación de texto hacia sistemas estructurados, conectados y autónomos

### 10.4 Mecanismos de Evaluación de Sistemas Agénticos

Cuatro categorías de evaluación:

| Categoría | Qué mide |
|---|---|
| Razonamiento y planificación multi-etapa | Corrección del plan, recuperación ante errores, coherencia lógica |
| Uso de herramientas y funciones externas | Selección de herramienta, eficiencia en parámetros, tasa de éxito |
| Autorreflexión y mejora adaptativa | Actualización de creencias, revisión de hipótesis, metacognición |
| Memoria y persistencia contextual | Precisión de recuperación, persistencia, integración semántica/episódica |

**LLM-as-a-Judge:** modelo de lenguaje como evaluador — escalable pero con riesgo de sesgo estilístico.

---

## 11. Diseño Metodológico

### Enfoque
- **Mixto:** predominio cuantitativo + validación cualitativa experta
- **Experimental–aplicado:** desarrollo tecnológico + validación empírica controlada + análisis cualitativo experto

### Hipótesis Principal
> La integración de un sistema agéntico copiloto con un grafo de conocimiento **mejora significativamente** la coherencia y consistencia contextual en la generación asistida de documentos metodológicos.

### Variables

| Tipo | Descripción |
|---|---|
| Independiente | Implementación del sistema agéntico con soporte de grafo de conocimiento |
| Dependientes | Nivel de coherencia semántica, consistencia estructural y utilidad percibida |
| De control | Tipo de documento, nivel de complejidad conceptual, extensión del texto |

### Diseño Experimental
- **Cuasi-experimental**, grupo único, mediciones **pretest y postest**
- **Pretest:** coherencia documental en textos sin asistencia del sistema
- **Postest:** mismo tipo de producción textual con apoyo del sistema agéntico
- **Validación cruzada:** revisión experta

### Instrumentos de Evaluación

| Instrumento | Aplicación |
|---|---|
| Métricas automáticas | Coherencia semántica, completitud estructural y razonamiento multi-hop (LLM as Judge, entorno MLOps) |
| Evaluación experta | Escala Likert (1–5) para coherencia, pertinencia y utilidad |
| Análisis estadístico | Análisis descriptivo y correlacional entre pretest y postest |

### Fases del Proyecto (5 fases)

1. **Fase I – Análisis conceptual y documental** *(M1-M2)*
   - Revisión de estructuras metodológicas y modelos de coherencia
   - Identificación de patrones semánticos y dependencias conceptuales
   - Construcción de taxonomía base y ontología preliminar

2. **Fase II – Modelado semántico y grafo de conocimiento** *(M2-M4)*
   - Diseño del modelo ontológico (OWL/RDF)
   - Implementación del grafo en base de datos especializada (Neo4j o RDF/OWL)
   - Validación estructural y semántica del modelo

3. **Fase III – Arquitectura agéntica y módulos cognitivos** *(M3-M5)*
   - Diseño modular de agentes (lectura, verificación, razonamiento)
   - Definición de flujos de interacción entre agentes y grafo
   - Documentación técnica y diagramas UML

4. **Fase IV – Implementación del prototipo funcional** *(M4-M8)*
   - Desarrollo del sistema agéntico copiloto
   - Integración con el grafo de conocimiento

5. **Fase V – Evaluación y validación experimental híbrida** *(M6-M8)*
   - Pruebas técnicas de coherencia y consistencia narrativa
   - Pruebas multi-hop y validación contextual automática
   - Evaluación experta (encuestas y observación controlada)
   - Análisis comparativo de desempeño y utilidad
   - Consolidación de resultados e informe final

---

## 12. Resultados Esperados

| Fase | Entregable / Resultado |
|---|---|
| **Fase I** | Mapa conceptual y semántico de estructuras de documentos de investigación; taxonomía de coherencia documental |
| **Fase II** | Modelo semántico-ontológico formalizado + grafo de conocimiento funcional (Neo4j/RDF) con consultas Cypher |
| **Fase III** | Arquitectura agéntica documentada (diagramas UML + BPMN) con módulos de lectura, análisis, verificación y navegación |
| **Fase IV** | Prototipo operativo con documentación técnica, guías de instalación, datasets de prueba y reportes de desempeño |
| **Fase V** | Informe de evaluación integral (métricas automáticas + percepciones expertas) sobre coherencia, consistencia y utilidad |

> **Nota:** El proyecto adopta prácticas de MLOps/AgentOps de forma iterativa. No pretende llegar a un nivel de evaluación de producción — es un prototipo.

---

## 13. Recursos y Aspectos Económicos

| Concepto | Descripción | Costo Total (COP) |
|---|---|---|
| Personal | Director (5 h/semana) | 32.000.000 |
| Personal | Investigador (15 h/semana) | 48.000.000 |
| Tecnológico | Servicios nube (Azure) | 960.000 |
| Tecnológico | Modelos de lenguaje (tokens/API) | 500.000 |
| Tecnológico | Licencia Neo4j | 1.560.000 |
| Tecnológico | Office 365 | 400.000 |
| Tecnológico | Documentación digital | 300.000 |
| Equipos | Almacenamiento y cómputo | 2.000.000 |
| Equipos | Impresión (encuestas) | 250.000 |
| Materiales | Papelería | 100.000 |
| Imprevistos | 1% | 860.700 |
| **TOTAL** | | **86.930.700** |

---

## 14. Referencias Clave Citadas en el Documento

| Clave | Descripción |
|---|---|
| Vaswani2017 | Arquitectura Transformer original |
| Lewis2021 | RAG original (Retrieval-Augmented Generation) |
| Khamis2025 | Estructura y componentes de sistemas agénticos |
| Singh2025 | Limitaciones y avances de RAG |
| Edge2025 | GraphRAG (documentación técnica) |
| Acharya2025 | Agentes basados en LLMs y Agentic RAG |
| Sardina2024 | Grafos de conocimiento y modelos de incrustación |
| Mathur2024 | Docpilot (Adobe Research) — sistemas copiloto documentales |
| Ren2022 | SMORE — razonamiento multihop en grafos |
| Chu2024 | Verify-Agent — agentes para validación |
| Krayem2025 | MMA-RAG — agentes con datos estructurados/no estructurados |
| Huang2025 | Amnesia contextual en LLMs |
| Zhuang2025 | Ingeniería de Contexto |
| Ibrahim2024 | Grafos de conocimiento en sistemas agénticos |
| Bonifazi2025 | Combinación de agentes y razonamiento simbólico |
| Asaf2025 | Marcos de evaluación de sistemas agénticos |
| Nan2020 | Razonamiento en relaciones inter-oracionales |
| Li2022 | Redes de grafos heterogéneos y atención |
| Long2022 | Comportamiento emergente en LLMs |
| Colombo2024 | GraphRAG e interpretabilidad |
| Mohamed2025 | KG como solución para consistencia documental |
| Bandi2025 | Evaluación interna en sistemas agénticos |
| Dess2025 | KG de dominio informático (25M+ entidades) |

---

## 15. Estado del Documento (al momento del levantamiento)

- **Fecha del levantamiento:** Febrero 2026
- **Secciones completas:** Portada, Resumen, Introducción, Planteamiento del Problema, Objetivos, Justificación y Alcance, Antecedentes y Estado del Arte, Marco Teórico, Diseño Metodológico (incluyendo cronograma y resultados esperados), Recursos Económicos
- **Secciones de plantilla (sin contenido del proyecto):** Anexos (solo instrucciones de plantilla), últimas páginas con ejemplos de tablas y figuras de la plantilla UAO
- **Bibliografía:** Gestionada mediante archivo `TuArchivo.bib` con `natbib` (estilo `plainnat`, citas autor-año)
- **Figuras del proyecto:** `foto1_anteproyecto.png` (arquitectura agéntica, tomada de Sapkota2025), `foto2_anteproyecto.png` (grafo de conocimiento, SDA Research Group)
