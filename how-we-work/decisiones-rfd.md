---
title: Decisiones
owner: Alexis Zazueta
status: active
last_reviewed: 2026-09-17
review_trigger: Cambio en el proceso de decisión.
---

# Decisiones

Una decisión que cuesta deshacer la escribimos antes de ejecutarla. Para las decisiones organizativas y de arquitectura compartida usamos un solo mecanismo: el **RFD**, Request for Discussion ([inspiraciones](../reference/inspiraciones.md)). Las decisiones técnicas de un producto van como [ADR](../engineering/adr.md) en su repositorio. Las decisiones de alcance de un producto son el pitch de su bet y no necesitan otro documento.

## Cuándo escribir un RFD

- Adoptar, cambiar o abandonar una herramienta o un sistema canónico.
- Cambiar un proceso de este handbook de forma que afecte a más de una persona.
- Arquitectura compartida por varios productos.
- Cualquier cosa que costaría más de un día deshacer.

Si cabe en el hilo semanal y es reversible, no es un RFD.

## Formato

Un archivo `rfd/NNNN-titulo-corto.md` con cabecera:

```yaml
rfd: 0017
title: …
state: discussion      # prediscussion | ideation | discussion | published | committed | abandoned
owner: <persona>
created: 2026-09-17
supersedes: 0002       # opcional
```

y cuerpo: **Contexto** (qué fuerzas hay), **Decisión** (en presente, voz activa), **Alternativas consideradas**, **Consecuencias** (también las negativas), **Seguimiento**, **Disparador de revisión**.

## Estados

| Estado | Significa |
|---|---|
| `prediscussion` | placeholder; el autor sigue escribiendo |
| `ideation` | solo hay una descripción del tema, sin propuesta |
| `discussion` | hay un PR abierto y se está discutiendo |
| `published` | el PR se mergeó: es la dirección establecida |
| `committed` | implementado por completo; cambia poco |
| `superseded` | sustituido por un RFD posterior; se conserva como historial |
| `abandoned` | no se implementará |

## Proceso

1. Reservas el siguiente número libre y creas una rama desde `main` llamada `rfd/NNNN-titulo`.
2. Escribes el RFD en esa rama, en estado `discussion`, y abres un pull request **hacia `main`**. El RFD nunca se escribe directamente en `main`: el PR es donde se discute.
3. Plazo de comentarios: cinco días naturales, ajustable por quien lo escribe. Un RFD no se mergea sin que al menos otra persona lo haya leído y comentado.
4. El autor decide cuándo mergear. Al mergear, el estado pasa a `published` y el archivo queda en `main` para siempre.
5. Para cambiar una decisión no se edita el RFD: se escribe uno nuevo que la sustituye. El nuevo lleva `supersedes: NNNN` en su cabecera y el viejo pasa a estado `superseded`. Así el historial cuenta qué decidimos, cuándo y por qué cambiamos de opinión. Ejemplo: el [RFD 0014](../rfd/0014-platform-map-revisado.md) sustituye al 0002 y al 0011.

## Públicos e internos

Los RFD sobre cómo trabajamos son públicos y están en [rfd/](../rfd/index.md). Los que tocan proveedores, dinero, acuerdos entre nosotros o seguridad son internos y siguen el mismo proceso en nuestro registro interno, donde una tabla dice cuáles están vigentes y cuáles fueron sustituidos. El índice público no los lista.
