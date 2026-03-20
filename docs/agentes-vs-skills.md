# Agentes vs Skills en Claude Code

## Qué es cada uno

### Skill
Una **inyección de conocimiento e instrucciones** en el contexto principal de Claude. Se activa por trigger (descripción) o por invocación (`/skill-name`) y carga instrucciones progresivamente.

- Claude principal absorbe las instrucciones y actúa según ellas
- Comparte el contexto de la conversación — ve todo lo anterior
- Progressive disclosure: descripción → SKILL.md → references/
- Es Claude "potenciado" con conocimiento extra

### Agente
Un **subproceso aislado** que se lanza desde la conversación principal. Tiene su propio contexto, tools, y opcionalmente su propio modelo.

- Arranca limpio — no ve la conversación anterior (solo el prompt que le pasas)
- Devuelve un resultado al Claude principal
- Tiene sus propios tools configurados
- Es "otro Claude" especializado que trabaja por encargo

---

## Cuándo usar cada uno

### Usa una SKILL cuando:

| Señal | Por qué |
|-------|---------|
| Claude necesita **conocimiento de dominio** para hacer su trabajo | La skill inyecta ese conocimiento en contexto |
| El trabajo requiere **ver el contexto de la conversación** | La skill comparte el contexto principal |
| Es una **forma de trabajar** (método, proceso, checklist) | Claude sigue las instrucciones como propias |
| Necesitas que Claude **aplique criterios** mientras hace otra cosa | La skill guía sin interrumpir el flujo |
| El trigger es **implícito** — Claude debería activarlo solo | La descripción permite auto-activación |
| El output es **parte de la conversación** con el usuario | No hay handoff, Claude responde directamente |

**Ejemplos típicos de skill:**
- Lean delivery: mientras Claude ayuda a definir una feature, aplica los principios de slicing
- User research: cuando Claude analiza feedback, sigue la estructura de síntesis
- Métricas: cuando Claude ve datos de SaaS, razona con el framework de Lean Analytics

### Usa un AGENTE cuando:

| Señal | Por qué |
|-------|---------|
| La tarea es **autónoma y acotada** — "analiza esto y vuelve con un resultado" | El agente trabaja solo y devuelve un entregable |
| Necesitas **proteger el contexto** principal de mucho output | El agente consume su propio contexto |
| Quieres **paralelizar** trabajo (varios análisis a la vez) | Los agentes corren en paralelo |
| El proceso es **conversacional paso a paso** con el usuario | El agente gestiona su propio flujo |
| Necesitas un **modelo diferente** (ej: opus para razonamiento complejo) | Los agentes pueden tener model override |
| La tarea necesita **tools específicos** (WebSearch, Bash) sin abrir permisos globales | Los agentes tienen su propia lista de tools |
| Quieres **memoria persistente** entre sesiones para ese rol | Los agentes pueden tener su propio directorio de memoria |

**Ejemplos típicos de agente:**
- Business strategist: guía paso a paso (Diagnóstico → Guiding Policy → Actions), conversación larga
- Engineer review: analiza un PRD y devuelve un informe de feasibility
- Executive: toma un update técnico y produce un resumen ejecutivo

---

## La zona gris — criterio para decidir

Muchas veces un mismo rol podría ser skill o agente. La clave es preguntarte:

### 1. ¿Enriquece o reemplaza?
- **Enriquece** lo que Claude ya hace → **Skill** (añade criterio, conocimiento, método)
- **Reemplaza** a Claude con un especialista → **Agente** (otro punto de vista, otro flujo)

### 2. ¿Necesita el contexto previo?
- **Sí**, necesita ver lo que se ha hablado → **Skill**
- **No**, trabaja con un input específico → **Agente**

### 3. ¿Cuánto output genera?
- **Poco** (guía, criterios, estructura) → **Skill**
- **Mucho** (informes, análisis largos) → **Agente** (protege el contexto)

### 4. ¿Es un flujo de varios pasos con el usuario?
- **No**, es aplicar conocimiento → **Skill**
- **Sí**, tiene su propia conversación → **Agente**

### 5. ¿Debería activarse solo?
- **Sí**, cuando Claude detecte el contexto → **Skill** (auto-trigger por descripción)
- **No**, solo cuando el usuario lo pida → **Agente** o skill con `disable-model-invocation: true`

---

## Patrón combinado: Skill + Agente

No son excluyentes. Un patrón potente es:

- **Skill** que inyecta el conocimiento y criterios base
- **Agente** que ejecuta tareas pesadas usando ese conocimiento

Ejemplo: una skill de "lean-analytics" que hace que Claude siempre razone con métricas SaaS, y un agente "metrics-analyst" que puede lanzarse a analizar datos concretos en profundidad.

---

## Aplicado a tus agentes actuales

| Agente actual | Recomendación | Razón |
|---------------|---------------|-------|
| **lean-delivery** | **Skill** | Es una forma de trabajar (slicing, hamburger method) que Claude debería aplicar siempre que se hable de features. Auto-trigger ideal. |
| **lean-analytics** | **Skill** | Conocimiento de dominio (métricas SaaS) que Claude debería usar cuando ve datos o métricas. |
| **impact-growth** | **Skill** o **ambos** | El framework IDG es conocimiento que Claude puede aplicar, pero las 4 fases de coaching son un flujo conversacional que se beneficia de un agente. |
| **user-researcher** | **Skill** | Estructura de síntesis y criterios de research que Claude aplica cuando analiza feedback/entrevistas. |
| **business-strategist** | **Agente** | Flujo paso a paso (Diagnosis → Policy → Actions) que requiere conversación guiada. El agente gestiona el progreso. |
| **executive** | **Skill** | Criterios de comunicación ejecutiva que Claude aplica al escribir updates o business cases. |
| **engineer** | **Skill** | Criterios de review técnica que Claude aplica al evaluar specs o PRDs. |
| **lean-product-manager** | **Skill** | Principios lean que Claude debería aplicar en cualquier decisión de producto. Overlap con lean-delivery y lean-analytics — candidato a fusionar. |
