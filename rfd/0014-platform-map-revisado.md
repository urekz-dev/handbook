---
rfd: 0014
title: Handbook público en git, Notion como registro
state: published
owner: Alexis Zazueta
created: 2026-09-16
supersedes: 0002, 0011
---

# RFD 0014: Handbook público en git, Notion como registro

## Contexto
Revisamos nuestra estructura contra la de equipos pequeños que admiramos ([inspiraciones](../reference/inspiraciones.md)). Dos ideas pesaron: un handbook abierto al mundo crea accountability y es más difícil de dejar morir que un wiki interno, y un pull request separa a quien propone de quien aprueba. Decidimos tener handbook público y código privado.

## Decisión
El handbook (cómo trabajamos: principios, procesos, políticas) vive en el repositorio público `urekz-dev/handbook`, se publica en handbook.urekz.com y cambia por pull request. Las decisiones organizativas y transversales son RFD en ese repositorio; las sensibles siguen el mismo proceso en nuestro espacio de trabajo. Notion queda como **registro privado**: personas y custodios, herramientas y proveedores, portfolio, procedimientos de recuperación, borradores. Plane sigue con definición y ejecución de producto; GitHub con lo técnico. El mapa completo está en [Platform Map](../reference/platform-map.md).

## Alternativas consideradas
Publicar Notion en la web: público, pero sin historial revisable ni separación entre proponente y aprobador. Plane Pages para el handbook: mezcla documentación de producto y organizacional, y no tiene PR. Mantener Notion privado: sin accountability pública.

## Consecuencias
Migramos unas 25 páginas a Markdown en español. Aprendemos a proponer cambios por PR. El sitio handbook.urekz.com existe por fin. Los datos personales y de proveedores se quedan fuera del repositorio público.

## Seguimiento
Este handbook y su primer índice de RFD.

## Disparador de revisión
Que el handbook deje de recibir PRs durante un ciclo completo, o que necesitemos documentación organizacional privada que no quepa en nuestro registro.
