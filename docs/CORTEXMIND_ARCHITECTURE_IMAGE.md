# CortexMind — Documentación de la imagen de arquitectura

Imagen asociada:

`images/cortexmind-architecture.png`

## Propósito

Esta imagen representa la arquitectura general de CortexMind como sistema cognitivo artificial. Su función es mostrar cómo entra la información desde el usuario o el entorno, cómo se filtra antes del procesamiento costoso, cómo se distribuye entre los distintos procesos cognitivos, cómo se consulta y consolida la memoria, y cómo una respuesta puede evolucionar antes de considerarse final.

No representa una anatomía biológica literal. Es un mapa funcional del flujo cognitivo de CortexMind.

## 1. Usuario / Mundo

El sistema recibe información desde el exterior mediante modalidades digitales.

En la primera versión las entradas principales son:

- visión;
- audición;
- habla;
- texto.

Posteriormente pueden incorporarse sensores adicionales mediante adaptadores plug-and-play sobre Linux.

El usuario aporta intención, objetivos, correcciones y contexto. El mundo aporta señales y cambios que CortexMind puede observar.

## 2. Input Gate

El Input Gate constituye la primera barrera cognitiva.

Su objetivo es evitar que una entrada incorrecta, ambigua o ruidosa active innecesariamente procesos de razonamiento costosos.

Puede detectar:

- errores de escritura;
- términos ambiguos;
- contradicciones;
- ruido;
- nombres dudosos;
- correcciones del usuario;
- información incompleta.

Cuando una diferencia de interpretación puede cambiar significativamente la solución, CortexMind debe solicitar aclaración antes de continuar.

## 3. Cerebro Digital

El Cerebro Digital es el núcleo coordinador de CortexMind.

Integra:

- percepción;
- atención;
- memoria;
- contexto;
- objetivos;
- razonamiento;
- decisiones;
- evaluación de riesgo;
- acciones.

No es un único modelo monolítico. La intención es que diferentes módulos especializados cooperen mediante eventos, estados y contratos bien definidos.

## 4. Modo Ejecutivo

El Modo Ejecutivo corresponde al procesamiento orientado a una tarea activa.

Sus funciones incluyen:

- planificar;
- decidir;
- responder;
- programar;
- coordinar herramientas;
- solicitar memoria;
- mantener objetivos;
- evaluar consecuencias.

Es el equivalente funcional del control ejecutivo dentro de la arquitectura.

## 5. Modo Interno

El Modo Interno trabaja sobre información que no necesita una respuesta inmediata.

Puede:

- asociar ideas;
- reconsiderar conclusiones;
- extraer hitos;
- buscar contradicciones;
- consolidar memoria;
- incubar problemas pendientes;
- reorganizar conocimiento.

No representa sueño biológico. Es procesamiento cognitivo interno durante periodos de menor prioridad externa.

## 6. Cognitive Threads

CortexMind no trata toda la conversación como una secuencia rígida de pregunta y respuesta.

Puede mantener múltiples hilos cognitivos simultáneos.

Estados conceptuales principales:

- `ACTIVE`;
- `PENDING`;
- `INCUBATING`;
- `CLARIFICATION`;
- `LISTENING`;
- `RETRIEVING`;
- `WAITING_DATA`;
- `RESOLVED`.

Una nueva intervención del usuario puede modificar un hilo activo, abrir otro, corregir uno anterior o despertar un pensamiento que estaba incubándose.

## 7. Orquestador de Memoria

La memoria no se modela como un único bloque.

CortexMind separa funciones de memoria:

- memoria de trabajo;
- memoria episódica;
- memoria semántica;
- memoria procedimental;
- memoria de largo plazo.

Cada una puede contar con su propio orquestador, pero todas deben comunicarse de forma transparente.

La cognición solicita conceptos como:

```text
recordar X
guardar Y
actualizar Z
relacionar A con B
```

y la capa de memoria decide dónde buscar, qué versión utilizar y qué información merece consolidarse.

## 8. MCMA / Nube

MCMA-OpenMemory actúa como memoria persistente.

Su función dentro de CortexMind es conservar información más allá del contexto inmediato sin obligar al resto de la arquitectura a conocer detalles físicos de almacenamiento.

MCMA puede conservar:

- experiencias;
- conocimiento;
- relaciones;
- procedimientos;
- versiones;
- referencias;
- contexto histórico.

El objetivo es que CortexMind conserve lo importante y pueda reconstruir detalles cuando los necesite, en lugar de mantener todo permanentemente en memoria activa.

## 9. Respuestas versionadas

Una respuesta puede evolucionar.

Ejemplo:

```text
v1 → interpretación inicial
v2 → nueva información
v3 → corrección del usuario
v4 → validación
v5 → respuesta consolidada
```

El usuario ve normalmente la versión vigente.

Las revisiones anteriores pueden conservarse para:

- auditoría;
- trazabilidad;
- aprendizaje;
- explicación de cambios.

## 10. BrainPilot 3D

BrainPilot 3D es la interfaz de observación del cerebro artificial.

Debe permitir visualizar:

- qué módulos están activos;
- qué hilos están pendientes;
- qué memoria se consulta;
- qué riesgo se evalúa;
- qué decisiones se están formando;
- qué procesos están incubándose.

También puede convertirse en una interfaz de corrección controlada, donde cada modificación sea versionada, auditable y reversible.

## Flujo resumido

```text
Usuario / Mundo
      ↓
Input Gate
      ↓
Atención
      ↓
Cognitive Threads
      ↓
Modo Ejecutivo ↔ Modo Interno
      ↓
Orquestadores de Memoria
      ↓
MCMA
      ↓
Respuesta versionada
      ↓
Usuario
```

## Principio representado

La imagen resume una idea central de CortexMind:

> La inteligencia no debe limitarse a producir una respuesta inmediata. Debe poder escuchar, mantener contexto, recordar, reconsiderar, corregir y continuar pensando.
