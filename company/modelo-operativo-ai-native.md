---
title: Cómo trabajamos con IA
owner: Alexis Zazueta
status: active
last_reviewed: 2026-09-17
review_trigger: Cambio en la política de autonomía de agentes.
implementation_status: partial
---

# Cómo trabajamos con IA

Decimos que somos AI-native, y no nos referimos a usar un chat de IA ni a añadir funciones generativas a los productos. Nos referimos a diseñar procesos, herramientas y documentación asumiendo que los agentes participan en el trabajo. Un documento, un repositorio o un proceso no debería entenderse solo por quien lo creó: un agente tiene que poder entrar con poco contexto y reconstruir el estado de las cosas.

## Las personas dirigen, la IA amplifica

Conservamos el juicio y la responsabilidad. Los agentes investigan, proponen, implementan, revisan, verifican, documentan y automatizan. Evitamos dos extremos: usar la IA como autocompletado sofisticado, y darle autonomía sin límites.

## Qué puede hacer un agente

| Tipo de acción | Quién | Cómo se marca |
|---|---|---|
| Leer, analizar, proponer, redactar borradores | Un agente, sin pedir permiso | cualquier work item |
| Cambios reversibles con recibo (un PR, una página, un work item, una etiqueta, una carpeta) | Un agente, si el work item lo dice | `flow:agent-ready` |
| Accesos, roles, invitaciones, dinero, dominios, secretos, borrados, publicaciones | Una persona | `flow:human-required` |
| Lo que depende de alguien de fuera | Esperar | `flow:blocked-external` |

La autonomía se fija por riesgo, reversibilidad y permisos concedidos. Un agente no cambia políticas, permisos ni gobernanza por su cuenta. Y siempre deja rastro: qué leyó, qué cambió, qué verificó, cuánto costó.

## Recibos

Toda ejecución automatizada produce un recibo: estado encontrado, diferencia detectada, cambio propuesto, cambio realizado, verificación. Para sistemas con API seguimos `audit → plan → dry-run → apply → verify`. Un agente no hace clics hasta que "parezca correcto".

## Modelos y proveedores

Usamos distintos modelos para distintas funciones: uno puede planificar, otro implementar, otro revisar. Diseñamos alrededor de roles y contratos, no de un proveedor.

## Dónde estamos

Las etiquetas `flow:*` existen y las usamos; los recibos se exigen en los work items. Un harness de agentes propio, hoy en el taller, es la apuesta que convierte este modelo en herramienta. Ningún agente tiene hoy permisos de escritura permanentes en producción.
