---
title: Documentación
owner: Alexis Zazueta
status: active
last_reviewed: 2026-09-17
review_trigger: Cambio en los sistemas canónicos o en la estructura del handbook.
---

# Documentación

## Dónde va cada cosa

| Tipo | Dónde |
|---|---|
| Cómo trabajamos: principios, procesos, políticas | Este handbook (público, en git, por PR) |
| Decisiones organizativas y de arquitectura compartida | `rfd/` en este handbook (las sensibles, en nuestro registro interno) |
| Referencia interna: catálogo de etiquetas, estados, plantillas, accesos por sistema, estructura interna de Discord | Nuestro registro interno |
| Definición de un producto (brief de una página) | La página del producto en nuestro gestor de trabajo |
| Decisiones técnicas de un producto | `docs/adr/` en su repositorio |
| Arquitectura, runbooks técnicos, README | El repositorio del producto |
| Trabajo: qué, quién, en qué estado | Los work items |
| Archivos formales y medios | La carpeta de archivos |
| Secretos | El gestor de secretos, y en ningún otro sitio |

Una sola fuente por cosa. Enlazamos, no copiamos.

## Cuatro tipos de documento

Cada página es de un solo tipo. Mezclarlos es la causa de la mayoría de los problemas de documentación ([inspiraciones](../reference/inspiraciones.md)).

| Tipo | Sirve para | Aquí |
|---|---|---|
| **Explicación** | entender el porqué | `company/`, `community/principios` |
| **Guía** | hacer una tarea concreta | `how-we-work/`, `community/ai-coffee` |
| **Referencia** | consultar hechos exactos | `reference/` |
| **Tutorial** | aprender haciendo | ninguno todavía |

## Presente

Escribimos cómo son las cosas: "trabajamos en ciclos", no "deberíamos trabajar en ciclos". El estado de implementación no va en la prosa: va en la cabecera (`implementation_status: documented | partial | operating`) y en el trabajo. Una política escrita no prueba que algo esté funcionando.

## Cabecera

```yaml
title: …
owner: <persona>
status: active | draft | deprecated
last_reviewed: AAAA-MM-DD
review_trigger: <qué cambio obliga a revisar>
implementation_status: documented | partial | operating   # solo si describe un sistema
```

## Idioma

Español. Los identificadores técnicos (etiquetas, slugs, claves, nombres de canales) se quedan en inglés cuando el sistema lo pide. Decisión: [RFD 0013](../rfd/0013-idioma-del-handbook.md).

## Mantenimiento

Cada página tiene un dueño y un disparador de revisión. No revisamos por calendario: revisamos cuando el disparador ocurre. Las páginas `deprecated` se conservan un ciclo y se borran.
