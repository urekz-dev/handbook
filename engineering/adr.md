---
title: Decisiones técnicas (ADR)
owner: Alexis Zazueta
status: active
last_reviewed: 2026-09-17
review_trigger: Cambio en el proceso de decisiones técnicas.
---

# Decisiones técnicas (ADR)

Una decisión técnica de un producto se registra como un archivo corto en su repositorio: `docs/adr/NNNN-titulo-corto.md`. Una o dos páginas, numeradas, nunca reutilizadas, nunca borradas ([inspiraciones](../reference/inspiraciones.md)).

## Cuándo

Cuando una decisión afecta a la estructura, a las características no funcionales, a las dependencias, a las interfaces o a la forma de construir el producto. Elegir lenguaje, base de datos, hosting, autenticación, o conservar o reescribir un prototipo son ADR. Elegir el nombre de una función no lo es.

## Formato

```markdown
# ADR 0001: <frase corta>

- Estado: proposed | accepted | deprecated | superseded by ADR NNNN
- Fecha: AAAA-MM-DD
- Dueño: <persona>

## Contexto
Las fuerzas en juego: técnicas, de producto, de equipo, de costo. Hechos.

## Decisión
"Usamos X para Y." Presente, voz activa.

## Consecuencias
Qué mejora, qué empeora, qué queda pendiente. También lo malo.
```

## Reglas

- Se propone en un PR; se acepta al mergear.
- Para cambiar una decisión se escribe un ADR nuevo y el viejo pasa a `superseded by`.
- Si la decisión afecta a más de un producto, es un [RFD](../how-we-work/decisiones-rfd.md).
