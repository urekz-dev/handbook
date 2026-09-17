---
rfd: 0006
title: La organización urekz-dev en GitHub es el hogar del código
state: published
owner: Alexis Zazueta
created: 2026-09-09
supersedes:
---

# RFD 0006: La organización urekz-dev en GitHub es el hogar del código

## Contexto
El código, los pull requests, la CI y los artefactos técnicos necesitan un lugar con revisión, historial y permisos por equipo. GitHub Free para organizaciones cubre repositorios privados ilimitados, Actions y Dependabot; no cubre protección de rama en repositorios privados.

## Decisión
La organización `urekz-dev` es canónica para código, PRs, CI, ADR y runbooks técnicos, y desde el [RFD 0014](0014-platform-map-revisado.md) también para este handbook. Un repositorio por producto. Issues y Discussions desactivados: el trabajo vive en Plane.

## Alternativas consideradas
GitLab (handbook-first nativo, pero ya usamos GitHub y las herramientas de agentes lo integran mejor). Repositorios personales (sin propiedad organizacional).

## Consecuencias
Doble factor obligatorio, permiso base mínimo, los miembros no crean repositorios. Los repositorios privados no tienen protección de `main`: lo cubrimos con una guardia automática y con la convención, y pasaremos al plan de equipo cuando haya código de producto con más de una persona activa.

## Seguimiento
Esqueleto de repositorio de producto; guardia de `main`; CODEOWNERS; firma de commits.

## Disparador de revisión
Cambio de plan de GitHub o más de una persona activa por repositorio privado.
