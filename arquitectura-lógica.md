# Arquitectura Lógica del Anteproyecto

Este documento visualiza y audita la coherencia lógica interna de tu anteproyecto de maestría, utilizando una abstracción basada en el **Marco Lógico** y mapeada mediante extracción de ideas tipo **Zettelkasten**. 

El objetivo es evidenciar cómo se conectan las dimensiones ontológicas del problema con las teleológicas (objetivos), metodológicas y, de manera transversal, con el componente tecnológico (Grafos de Conocimiento, SLMs, Sistemas Agénticos).

---

## 1. Topología Lógica (Grafo Mermaid)

El siguiente diagrama ilustra cómo las entidades conceptuales fluyen y se integran.
*   **Líneas sólidas fuertes:** Flujo metodológico y derivaciones causales.
*   **Líneas punteadas:** Influencia transversal de la capa tecnológica.
*   **Nodos redondeados:** Ideas atómicas (Zettels) clave extraídas del texto.

```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'primaryColor': '#ffffff', 'edgeLabelBackground':'#f4f4f4', 'tertiaryColor': '#f4f4f4', 'fontFamily': 'Inter, sans-serif'}}}%%
flowchart TD
    %%------------------------------------%%
    %% DEFINICIÓN DE CLASES Y ESTILOS     %%
    %%------------------------------------%%
    classDef fin fill:#e0f2fe,stroke:#0284c7,stroke-width:2px,color:#0c4a6e;
    classDef problema fill:#fee2e2,stroke:#dc2626,stroke-width:2px,color:#7f1d1d;
    classDef objetivo fill:#dcfce7,stroke:#16a34a,stroke-width:2px,color:#14532d;
    classDef metodo fill:#fef9c3,stroke:#ca8a04,stroke-width:2px,color:#713f12;
    classDef tecnologia fill:#f3e8ff,stroke:#9333ea,stroke-width:2px,color:#581c87,stroke-dasharray: 5 5;
    classDef output fill:#f1f5f9,stroke:#64748b,stroke-width:1px,color:#0f172a;
    classDef zettel fill:#ffffff,stroke:#94a3b8,stroke-width:1px,stroke-dasharray: 3 3;

    %%------------------------------------%%
    %% CAPA 1: FIN Y PROPÓSITO GENERAL     %%
    %%------------------------------------%%
    subgraph CapaTeleologica ["1. FIN / PROPÓSITO GENERAL (Marco Lógico)"]
        direccion(TB)
        T[Título: Sistema Agéntico (KG + SLM) para \nVerificación Estructural]:::fin
        Q[Pregunta: ¿Cómo la Ing. de Contexto (KG+SLM) en \nsistema agéntico reduce inconsistencias?]:::fin
        OG[Obj. General: Desarrollar prototipo copiloto para \nevaluar coherencia y consistencia]:::fin
        T --> Q --> OG
    end

    %%------------------------------------%%
    %% CAPA 2: SITUACIÓN PROBLEMA          %%
    %%------------------------------------%%
    subgraph CapaProblema ["2. EL PROBLEMA CENTRAL (Justificación)"]
        direccion(TB)
        P1[Inconsistencia y fisuras lógicas en doc. extensos]:::problema
        P2[Amnesia Contextual en LLMs]:::problema
        P3[Falta de memoria estructurada (Groud Truth)]:::problema
        OG -. "Resuelve" .-> P1
        P1 --- Z1(((ZETTEL: \nEscritura humana \nfragmentada))):::zettel
        P2 --- Z2(((ZETTEL: \nLLM predice\nsin razonar))):::zettel
    end

    %%------------------------------------%%
    %% CAPA 3: TECNOLOGÍA ENVOLVENTE       %%
    %%------------------------------------%%
    subgraph CapaTecnologica ["3. CAPA TECNOLÓGICA (Transversal)"]
        KG[Grafos de Conocimiento: Memoria Estructurada]:::tecnologia
        SLM[SLMs: Extractores Eficientes (Text2Graph)]:::tecnologia
        AGENTES[Sist. Agéntico: Módulos Cognitivos \ny Orquestación]:::tecnologia
        
        KG --- Z3(((ZETTEL: \nSupera Amnesia. \nRazonamiento Multihop))):::zettel
        SLM --- Z4(((ZETTEL: \nBajo costo \ncomputacional))):::zettel
        AGENTES --- Z5(((ZETTEL: \nVerifican coherencia, \nsin sustituir al investigador))):::zettel

        %% Vínculos tecnológicos transversales
        KG -. "Soluciona" .-> P2
        KG -. "Aporta Ground Truth" .-> P3
        SLM -. "Alimenta eficiente" .-> KG
        AGENTES -. "Usa" .-> KG
    end

    %%------------------------------------%%
    %% CAPA 4: COMPONENTES METODOLÓGICOS (El Envolvente) %%
    %%------------------------------------%%
    subgraph CapaMetodologia ["4. ENVOLVENTE METODOLÓGICO (Fases y Resultados)"]
        direccion(TB)
        O1[O.E.1: Analizar estructuras documentales]:::objetivo
        O2[O.E.2: Diseñar modelo semántico (Grafo)]:::objetivo
        O3[O.E.3: Implementar arquitectura copiloto]:::objetivo
        O4[O.E.4: Validar coherencia y desempeño]:::objetivo

        F1[Fase 1: Revisión y Taxonomía]:::metodo
        F2[Fase 2: Modelado Ontológico OWL/RDF]:::metodo
        F3[Fase 3: Diseño Agentes y Flujos]:::metodo
        F4[Fase 4: Desarrollo Funcional]:::metodo
        F5[Fase 5: Pruebas y Validación Híbrida]:::metodo
        
        R1(Entregable 1: Ontología y Mapa Semántico):::output
        R2(Entregable 2: Grafo Neo4J/RDF operativo):::output
        R3(Entregable 3: Arquitectura UML/BPMN):::output
        R4(Entregable 4: Prototipo y Documentación):::output
        R5(Entregable 5: Informe experimental controlado):::output

        %% Relación Objetivos -> Fases -> Resultados
        O1 --> F1 --> R1
        O2 --> F2 --> R2
        O3 --> F3 --> R3
        O3 --> F4 --> R4
        O4 --> F5 --> R5
    end

    %%------------------------------------%%
    %% CONEXIONES GLOBALES CASCADA         %%
    %%------------------------------------%%
    OG --> CapaMetodologia
    
    %% La tecnología habilita los objetivos
    KG -. "Instrumentaliza" .-> O2
    SLM -. "Integra" .-> O3
    AGENTES -. "Ejecuta Validación" .-> O4
    
    %% Fases afectan problema
    F5 -. "Mide mitigación" .-> P1
```

---

## 2. Auditoría de Coherencia Estructural (Marco Lógico)

A partir de la topología anterior, se realizó una evaluación crítica top-down (desde el propósito hasta las tareas) y bottom-up (desde las herramientas hasta el propósito) para identificar fortalezas, vacíos y "nodos huérfanos".

### ✅ 2.1 Puntos de Alta Coherencia
1. **Alineación Vertical (Fin $\leftrightarrow$ Medios):** Hay un hilo conductor matemático entre la "Amnesia Contextual" (Problema P2) y el uso de "Grafos de Conocimiento" (Tecnología KG). La tecnología no está puesta por moda, sino que justifica *exactamente* la falla de las soluciones estrictamente LLM.
2. **Trazabilidad de Objetivos a Metodología:** La estructura `Objetivo Específico -> Fase -> Entregable` es inusualmente limpia. El O.E.1 mapea a la Fase 1 / R1, el O.E.2 mapea a la Fase 2 / R2, etc. (Notablemente visible en la Capa 4 del grafo).
3. **Escalaridad de la Propuesta de Valor:** El límite está claro: "Prototipo", "Escenario Controlado", "No sustituye el criterio". Esto hace que la Fase 5 (Evaluación híbrida) sea altamente factible en 8 meses.

### ⚠️ 2.2 Vacíos Identificados y Áreas de Mejora (Alertas Metodológicas)

> [!WARNING] Vacío 1: El rol del "SLM" en el Objetivo Específico 2
> **Observación:** El O.E.2 habla de "Diseñar un modelo semántico-ontológico". Sin embargo, el O.E.3 dice que integrarás el grafo y los SLM. **Falta en el O.E.2 o en la Fase 2 especificar cómo el SLM (Text-To-Graph) va a poblar / instanciar el grafo.**
> **Recomendación:** Asegurar que la Fase 2 ("Modelado semántico") contenga explícitamente la estrategia de cómo las "Small Language Models" realizarán la Extracción de Relaciones (Relation Extraction) hacia el KG de manera eficiente.

> [!TIP] Vacío 2: Instrumentos de Validación Multihop vs. "Fase 1"
> **Observación:** La Fase 1 propone hacer una taxonomía de coherencia. La Fase 5 propone evaluarla con "LLM-as-a-judge" y "Razonamiento Multihop". 
> **Recomendación:** La taxonomía de la Fase 1 debe estar pre-formateada pensando en cómo se traducirá a consultas `Cypher`/Grafos. Si la taxonomía es puramente teórica, la Fase 5 fracasará en las métricas. Añadir en Fase 1: *"Definición de heurísticas de evaluación de coherencia traducibles a reglas de grafo"*.

> [!IMPORTANT] Vacío 3: El "Ground Truth" dinámico
> **Observación:** En el documento se menciona el KG como un "Ground Truth dinámico" (Zettel 3 / Capa 3). Pero no hay una actividad en la metodología sobre **cómo el sistema actualiza ese grafo si el usuario cambia de opinión a mitad del documento.**
> **Recomendación:** En la Fase 3, añadir una sub-tarea sobre "Mecanismos de actualización o control de versiones en el Grafo de Conocimiento al interactuar con el investigador". 

### 💡 Conclusión del Evaluador
El anteproyecto presenta una arquitectura **excepcionalmente robusta**, con una sólida articulación causal. El modelo de Marco Lógico demuestra que las Tecnologías seleccionadas (Capa 3) actúan perfectamente como un "envolvente" resolutivo del Problema central (Capa 2), permitiendo estructurar los Componentes Metodológicos (Capa 4) de manera lógica. Salvar los tres vacíos metodológicos menores listados consolidará el documento a prueba de revisiones estrictas.
