# CortexMind

**Experimental Artificial Cognitive Architecture**

CortexMind es un proyecto open source para investigar y construir una arquitectura cognitiva artificial inspirada en funciones del cerebro humano, sin pretender reproducir literalmente su anatomía ni afirmar equivalencia con la cognición biológica.

Su objetivo es desarrollar un sistema capaz de **percibir, escuchar, comprender, recordar, mantener múltiples líneas de pensamiento, reconsiderar respuestas, incubar problemas, aprender de la experiencia y actuar sobre un entorno digital o físico**.

CortexMind está pensado para ejecutarse inicialmente sobre **Linux**, utilizando el sistema operativo y el hardware como su cuerpo digital.

> **Escucha. Percibe. Piensa. Recuerda. Corrige. Aprende. Continúa pensando.**

---

## Visión

CortexMind explora un modelo cognitivo continuo:

```text
percibir
   ↓
atender
   ↓
comprender
   ↓
recordar
   ↓
razonar
   ↓
decidir
   ↓
actuar
   ↓
observar consecuencias
   ↓
aprender
   ↓
reconsiderar
```

El objetivo no es simplemente responder más rápido, sino construir una arquitectura donde diferentes procesos cognitivos puedan colaborar, mantenerse pendientes, recuperar información posteriormente y modificar conclusiones cuando aparezca nueva evidencia.

---

## Modelo funcional

CortexMind se organizará mediante módulos cognitivos especializados y coordinados:

- percepción;
- atención;
- lenguaje;
- memoria;
- planificación;
- evaluación de riesgo;
- razonamiento;
- acción;
- aprendizaje;
- consolidación;
- incubación;
- metacognición.

Estos módulos representan **funciones cognitivas artificiales**, no equivalencias médicas exactas de regiones cerebrales humanas.

---

## Linux como cuerpo digital

Linux actuará como interfaz entre CortexMind y el hardware.

El sistema podrá conocer tanto el mundo exterior como el estado de su propio cuerpo computacional:

- CPU;
- RAM;
- GPU;
- almacenamiento;
- temperatura;
- batería;
- red;
- procesos;
- servicios;
- dispositivos;
- sensores.

Esta información constituye una forma de **propiocepción digital**.

---

## Sentidos digitales plug-and-play

CortexMind no dependerá directamente de marcas o modelos físicos de sensores. Cada dispositivo será abstraído mediante un **Sensory Adapter** y registrado por modalidad.

### Visión

- cámaras USB;
- cámaras IP;
- cámaras integradas;
- infrarrojo;
- cámaras térmicas;
- sensores de profundidad.

### Audición

- micrófonos;
- arreglos de micrófonos;
- fuentes de audio del sistema.

### Percepción ampliada

- LiDAR;
- ultrasonido;
- radar;
- sensores ToF;
- GPS/GNSS;
- acelerómetros;
- giroscopios;
- magnetómetros;
- temperatura;
- humedad;
- presión atmosférica;
- luminosidad;
- sensores de gases;
- humo;
- CO₂;
- presión;
- fuerza;
- vibración;
- proximidad.

Una nueva capacidad sensorial deberá poder añadirse sin rediseñar el cerebro completo.

```text
Dispositivo
    ↓
Linux
    ↓
Sensory Adapter
    ↓
Sensory Bus
    ↓
CortexMind
```

---

## Input Gate

Antes de activar procesos cognitivos costosos, CortexMind dispondrá de una etapa ligera que podrá detectar:

- errores de escritura;
- ambigüedades;
- ruido;
- contradicciones;
- nombres inciertos;
- correcciones del usuario;
- información incompleta.

Si una ambigüedad puede cambiar significativamente la solución, el sistema deberá solicitar aclaración antes de continuar.

---

## Atención

No toda información percibida debe recibir el mismo nivel de procesamiento.

El sistema podrá evaluar:

- relevancia;
- urgencia;
- novedad;
- riesgo;
- relación con el objetivo actual;
- relación con pensamientos pendientes;
- solicitudes explícitas del usuario.

Sólo una parte de los estímulos deberá llegar al procesamiento cognitivo de mayor costo.

---

## Cognitive Threads

CortexMind podrá mantener múltiples líneas de pensamiento simultáneamente.

Estados previstos:

```text
ACTIVE
LISTENING
PENDING
INCUBATING
RETRIEVING
WAITING_DATA
CLARIFICATION
RESOLVED
```

Una nueva entrada podrá modificar el hilo actual, aclararlo, corregirlo, crear otro hilo, despertar un pensamiento pendiente o invalidar una conclusión anterior.

La conversación no se modelará únicamente como turnos aislados, sino como **pensamiento continuo con múltiples hilos cognitivos**.

---

## Respuestas versionadas

Las respuestas podrán evolucionar conforme llegue nueva información:

```text
v1 → respuesta inicial
v2 → nueva información
v3 → corrección
v4 → validación
v5 → respuesta consolidada
```

El usuario verá normalmente la versión vigente. Las revisiones anteriores podrán conservarse para auditoría, trazabilidad y aprendizaje.

---

## Recuperación diferida e incubación

Si durante una conversación falta un nombre, concepto, relación o recuerdo, CortexMind podrá continuar intentando recuperarlo sin detener necesariamente el hilo principal.

Los problemas sin solución inmediata podrán mantenerse como pensamientos pendientes. Durante periodos de menor actividad, procesos internos podrán buscar relaciones, consultar memoria, contrastar hipótesis, detectar contradicciones, simplificar problemas y asociar información nueva.

Un nuevo dato podrá despertar automáticamente un pensamiento incubado.

---

## Arquitectura de memoria

CortexMind utilizará distintos tipos funcionales de memoria:

### Memoria de trabajo
Contexto inmediato y tareas en curso.

### Memoria episódica
Experiencias y acontecimientos.

### Memoria semántica
Conceptos, hechos y relaciones.

### Memoria procedimental
Cómo realizar tareas y procesos.

### Memoria de largo plazo
Conocimiento consolidado y durable.

Cada tipo de memoria podrá disponer de su propio orquestador, comunicándose de forma transparente con los demás.

---

## MCMA / memoria persistente

CortexMind podrá utilizar [MCMA-OpenMemory](https://github.com/jimmybackend/MCMA-OpenMemory) como capa persistente de memoria.

Los procesos cognitivos no necesitarán conocer dónde se encuentra físicamente una memoria. Podrán solicitar operaciones conceptuales como:

```text
recordar X
guardar Y
actualizar Z
relacionar A con B
```

Los orquestadores de memoria resolverán qué tipo de memoria corresponde, dónde se encuentra, qué versión está vigente, qué confianza posee, qué relaciones tiene, qué debe conservarse y qué puede decaer.

---

## Olvido y consolidación

CortexMind no pretende mantener toda la información permanentemente activa.

La información útil podrá convertirse en hitos, relaciones e índices antes de consolidarse en memoria persistente. Los detalles de baja relevancia podrán abandonar la memoria activa, conservando cuando sea necesario una ruta para reconstruir o recuperar el original.

```text
experiencia
   ↓
hito
   ↓
relación
   ↓
índice
   ↓
consolidación
   ↓
memoria persistente
```

---

## Executive Cortex

El sistema ejecutivo coordinará:

- objetivos;
- prioridades;
- decisiones;
- planificación;
- solicitudes de memoria;
- selección de herramientas;
- acciones;
- evaluación de consecuencias.

No deberá confundirse pensamiento con ejecución.

---

## Action Cortex

Toda acción sobre el sistema operativo, servicios o hardware deberá atravesar controles explícitos:

```text
intención
   ↓
permisos
   ↓
política
   ↓
riesgo
   ↓
reversibilidad
   ↓
ejecución
```

Linux proporcionará la interfaz hacia herramientas, servicios, dispositivos y hardware.

---

## Evaluación de riesgo sin emociones obligatorias

CortexMind no necesita reproducir miedo, vergüenza o ansiedad para conservar sus funciones protectoras.

En su lugar podrá evaluar explícitamente:

- riesgo;
- incertidumbre;
- consecuencias;
- permisos;
- seguridad;
- impacto;
- reversibilidad.

La prudencia se modelará como proceso cognitivo y no como sufrimiento emocional.

---

## Modo interno

Cuando no exista una tarea externa prioritaria, CortexMind podrá dedicar recursos disponibles a:

- consolidación;
- asociación;
- incubación;
- revisión;
- compresión;
- recuperación diferida;
- detección de contradicciones;
- reorganización del conocimiento.

Este estado no representa sueño biológico, sino **procesamiento cognitivo interno**.

---

## Plasticidad artificial

Uno de los objetivos experimentales será permitir que ciertas rutas cognitivas se adapten según la experiencia.

El sistema podrá comparar:

```text
predicción
vs.
resultado real
```

y utilizar el error observado para modificar futuras decisiones.

Toda plasticidad deberá estar limitada por políticas, auditoría y mecanismos de versionado.

---

## BrainPilot 3D

CortexMind incluirá una representación tridimensional de su arquitectura cognitiva.

BrainPilot 3D deberá permitir observar:

- módulos activos;
- rutas de información;
- memorias consultadas;
- Cognitive Threads;
- decisiones;
- niveles de confianza;
- riesgos;
- consolidación;
- pensamientos incubados.

También podrá permitir correcciones controladas sobre procesos y memorias.

Las modificaciones deberán ser **trazables, versionadas, auditables y reversibles**.

---

## Ciclo cognitivo

```text
       PERCIBIR
          ↓
       ATENDER
          ↓
      COMPRENDER
          ↓
       RECORDAR
          ↓
       RAZONAR
          ↓
       DECIDIR
          ↓
        ACTUAR
          ↓
       OBSERVAR
          ↓
       APRENDER
          ↓
       RECORDAR
          ↺
```

---

## Arquitectura conceptual

```text
MUNDO / USUARIO
      │
      ▼
SENSORES
      │
      ▼
LINUX
      │
      ▼
SENSORY ADAPTERS
      │
      ▼
INPUT GATE
      │
      ▼
ATENCIÓN
      │
      ▼
COGNITIVE THREADS
      │
      ├─────────────┐
      ▼             ▼
EXECUTIVE       MODO INTERNO
CORTEX              │
      │             │
      └──────┬──────┘
             ▼
       MEMORY CORTEX
             │
   ┌─────────┼──────────┐
   ▼         ▼          ▼
Trabajo   Episódica  Semántica
   │         │          │
   ├─────────┼──────────┤
             ▼
       Procedimental
             │
             ▼
            MCMA
             │
             ▼
       ACTION CORTEX
             │
             ▼
           LINUX
             │
             ▼
      MUNDO / HARDWARE
```

---

## Imágenes

La documentación visual del proyecto se almacenará en:

```text
images/
```

Las imágenes son representaciones conceptuales de la arquitectura y no deben interpretarse como modelos médicos o neuroanatómicos exactos.

---

## Estado actual

**Fase: diseño conceptual inicial.**

Las primeras etapas estarán enfocadas en definir y probar:

1. contratos entre módulos cognitivos;
2. modelo de eventos;
3. Sensory Adapter API;
4. Cognitive Threads;
5. memoria y orquestadores;
6. integración con MCMA;
7. integración Linux;
8. Action Cortex y permisos;
9. BrainPilot 3D;
10. aprendizaje, consolidación y plasticidad.

CortexMind no comenzará como una IA monolítica. Cada capacidad deberá poder desarrollarse, observarse y validarse de forma modular.

---

## Alcance científico

CortexMind está inspirado en funciones de la cognición humana, pero **no afirma ser una simulación médica del cerebro, un modelo de conciencia humana ni una reproducción neurobiológica exacta**.

El proyecto utilizará analogías cognitivas únicamente cuando sean útiles para construir y experimentar con arquitecturas computacionales.

---

## Licencia prevista

CortexMind está previsto para distribuirse bajo **Apache License 2.0**, permitiendo uso, modificación y distribución, incluida utilización comercial, bajo los términos de dicha licencia.
