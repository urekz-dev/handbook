---
title: Repositorios
owner: Alexis Zazueta
status: active
last_reviewed: 2026-09-17
review_trigger: Al crear un repositorio o cambiar de plan de GitHub.
---

# Repositorios

Nuestro código vive en la organización [`urekz-dev`](https://github.com/urekz-dev) en GitHub. Un repositorio por producto, monorepo por dentro. Un agente solo ve el repositorio en el que trabaja, así que todo lo que un producto necesita (código, brief, decisiones, runbooks) vive en su repo.

## Cómo está organizado un repositorio de producto

```text
README.md                  qué es, estado, cómo correr, cómo desplegar
docs/product-brief.md      el brief de una página, enlazado desde el gestor de trabajo
docs/adr/                  decisiones técnicas numeradas
CHANGELOG.md               una entrada por versión, para personas
CODEOWNERS                 quién revisa qué
.github/workflows/         callers de los workflows compartidos y CI propia
apps/ packages/ infra/     código, según el stack
```

Los repositorios de producto son privados. Este handbook es público. El repositorio `.github` de la organización también lo es, porque GitHub exige que sea público para que sus plantillas (guía de contribución, plantilla de PR, política de seguridad, perfil) apliquen a todos los repositorios; por eso solo contiene plantillas. Los workflows y guardias reutilizables viven en un repositorio privado y cada repo los llama con un archivo de pocas líneas.

## Convenciones

- **Ramas:** `main` más ramas cortas `<tipo>/<ID>-<descripcion>`. Una rama por story; mergeada antes del cierre del ciclo.
- **Commits:** Conventional Commits (`feat`, `fix`, `docs`, `chore`, `refactor`, `test`). Firmados.
- **Merge:** squash only; el título del PR es el commit; la rama se borra al mergear.
- **Versiones:** SemVer y un `CHANGELOG.md` escrito para personas.
- **Secretos:** ninguno en el repo. Las variables se documentan por nombre en el README.
- **Actions:** solo acciones de GitHub o fijadas por SHA; el token de CI es de solo lectura por defecto.

## Un límite que conocemos

En el plan gratuito de GitHub, los repositorios privados no tienen protección de rama. Lo cubrimos con una guardia automática compartida que avisa y falla si alguien hace push directo a `main`, y con la convención. Cuando haya código de producto y más de una persona activa por repo, pasaremos al plan de equipo.
