---
rfd: 0010
title: La documentación técnica vive con el código
state: published
owner: Alexis Zazueta
created: 2026-09-13
supersedes:
---

# RFD 0010: La documentación técnica vive con el código

## Contexto
La documentación que cambia con la implementación (ADR, arquitectura, runbooks) se desactualiza si vive lejos del código. Un agente solo ve el repositorio en el que trabaja.

## Decisión
Los ADR, la arquitectura, los runbooks técnicos y el brief enlazado de cada producto viven en su repositorio, en `docs/`. Este handbook enlaza al código; no lo describe. Plane guarda el brief canónico de una página; el repositorio guarda una copia enlazada y todo lo técnico.

## Alternativas consideradas
Documentación técnica en Notion o en Plane Pages: se desactualiza y es invisible para los agentes que trabajan en el repositorio.

## Consecuencias
Cada repositorio de producto tiene el esqueleto `docs/product-brief.md`, `docs/adr/` y `CHANGELOG.md`. Quien cambia el código cambia la documentación en el mismo PR.

## Seguimiento
Esqueleto de repositorios; [Decisiones técnicas (ADR)](../engineering/adr.md).

## Disparador de revisión
Que un repositorio activo necesite otra frontera para su documentación.
