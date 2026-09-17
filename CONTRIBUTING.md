---
title: Cómo proponer cambios
owner: Alexis Zazueta
status: active
last_reviewed: 2026-09-17
review_trigger: Cambio en el proceso de revisión.
---

# Cómo proponer cambios

Este handbook cambia por pull request. La regla es simple: si queremos cambiar cómo trabajamos, cambiamos el handbook; no lo anunciamos en un chat ([de dónde viene](reference/inspiraciones.md)).

## Pasos

1. Rama desde `main`: `docs/<tema-corto>`, o `rfd/NNNN-<tema>` si es una decisión.
2. Edita o crea el archivo. Respeta la cabecera (`title`, `owner`, `status`, `last_reviewed`, `review_trigger`).
3. Abre el PR y cuenta qué cambia, por qué y a quién afecta. Si sustituye una práctica, enlaza la anterior.
4. Lo aprueba alguien distinto de quien lo escribió. Somos cinco: a veces el par se repite, y lo decimos.
5. Squash merge. El título del PR es el mensaje del commit (`docs: …`, `rfd: …`).

## Agentes

Un agente puede abrir un PR si el work item que lo motiva lleva `flow:agent-ready`. El PR enlaza el work item y deja un recibo: qué leyó, qué cambió. Lo aprueba una persona.

## Estilo

Español, en primera persona del plural, en presente: "trabajamos en ciclos", no "se debería trabajar en ciclos". Frases cortas. Una idea por página. Tablas para lo comparable, listas para lo secuencial. Sin adjetivos de relleno.
