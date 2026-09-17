---
title: Ciclos de seis semanas
owner: Alexis Zazueta
status: active
last_reviewed: 2026-09-17
review_trigger: Al cierre de cada ciclo, en la retro.
implementation_status: documented
---

# Ciclos de seis semanas

Trabajamos en ciclos de seis semanas con *bets* de tiempo fijo y alcance variable, y una semana de *cool-down* entre ciclos. Usamos el vocabulario de Shape Up en su idioma original. Seis semanas a cinco o diez horas semanales son lo que un equipo a tiempo completo hace en una o dos; por eso el ciclo es largo y el apetito, fijo ([inspiraciones](../reference/inspiraciones.md)).

## Vocabulario

- **Bet:** una o dos personas se comprometen con un resultado durante un ciclo, sin interrupciones, con la expectativa de terminar.
- **Appetite:** las horas por persona que estamos dispuestos a gastar. Se fija antes de diseñar la solución. Si el trabajo no cabe, recortamos el alcance.
- **Pitch:** la descripción de un bet: problema, appetite, solución esbozada, *rabbit holes* (agujeros donde no meterse), *no-gos* (lo que no se hace), criterios de cierre.
- **Cool-down:** la semana entre ciclos. Cosas sueltas, bugs, retro y la *betting table*.

## El ciclo

| Semana | Qué pasa |
|---|---|
| 0 (cool-down anterior) | Cada quien propone como máximo un pitch. Betting table por escrito: elegimos los bets del ciclo, máximo uno por persona y al menos dos de producto. |
| 1–6 | Ejecución. Check-in semanal escrito. El alcance solo cambia para recortarse. |
| 6 | Cierre: demo asíncrona (un video corto o un hilo con capturas) y retro escrita de tres preguntas: qué funcionó, qué no, qué aprendimos que valga la pena contar. |
| 7 (cool-down) | Bugs, pendientes, siguiente betting table. |

## Reglas

1. **Sin backlog acumulado.** Lo que no entra como bet no se guarda en una lista infinita. La respuesta por defecto a una idea nueva es "interesante, quizá algún día". Las ideas importantes vuelven solas.
2. **Sin prórrogas por defecto.** Si un bet no termina al cierre, no se extiende. Se vuelve a proponer con lo aprendido, o se abandona.
3. **Los bugs esperan.** Salvo los que rompen producción, van al cool-down.
4. **Productos nuevos: explorar, no lanzar.** El primer bet de una idea es validar el problema, sin código.
5. **Nadie en más de un bet.** Con cinco personas caben dos productos activos por ciclo, no más.
