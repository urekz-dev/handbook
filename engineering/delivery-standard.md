---
title: Cómo entregamos
owner: Alexis Zazueta
status: active
last_reviewed: 2026-09-17
review_trigger: Cambio en el flujo de trabajo o en las herramientas de CI.
implementation_status: partial
---

# Cómo entregamos

Cómo un cambio va de idea a producción en cualquier producto nuestro.

## El flujo

1. **Intención.** Un work item con objetivo, lo que queda fuera, criterios de aceptación y cómo se verifica. Sin work item no hay rama. Excepción: mantenimiento urgente, marcado como tal en el PR.
2. **Entender.** Quien lo toma lee el brief del producto, las decisiones técnicas relevantes y el work item. Si falta algo, pregunta en el hilo del item; no adivina.
3. **El cambio más pequeño y completo.** Rama corta desde `main`: `<tipo>/<ID>-<descripcion>`. Una rama por story, mergeada a `main` antes del cierre del ciclo.
4. **Revisión.** PR con la plantilla: resumen, por qué, cambios, verificación, riesgos, enlace al work item. Lo revisa alguien distinto de quien lo escribió. Conversaciones resueltas antes de mergear.
5. **Verificación.** CI verde y la verificación que el work item describe, ejecutada: un comando, una captura, un recibo.
6. **Juicio humano.** Lo que toca accesos, datos, dinero o borrados lo aprueba explícitamente una persona en el PR.
7. **Entrega.** Squash merge; el título del PR es el commit. Desplegamos desde `main`.
8. **Aprender.** Si cambió una decisión, un ADR. Si cambió un proceso, un PR a este handbook. Si vale la pena contar, una idea de contenido.

## Agentes

Un agente puede hacer los pasos 2 a 5 de un item marcado `flow:agent-ready`. Trabaja en rama, no toca `main`, deja un recibo en el PR (qué leyó, qué cambió, qué verificó, cuánto costó) y no amplía el alcance. Lo aprueba una persona.

## Reglas de repositorio

- `main` siempre desplegable. Sin push directo.
- Commits firmados por personas.
- Squash only; la rama se borra al mergear.
- Revisión automática por área con `CODEOWNERS`.
- Sin secretos en el repo: escaneo en pre-commit y en CI.

## Dónde estamos

Convención y plantillas activas. La CI de cada producto llega con su primer código.
