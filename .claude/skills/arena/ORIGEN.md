# Origen de la skill Arena

- **Fuente:** https://github.com/Jakeschincariol/arena-skill (licencia MIT)
- **Carpeta copiada:** `skills/arena/` → `.claude/skills/arena/`
- **Commit exacto:** `df07b8e518e10cdecd8cd7712d9958b6f396250e` (2026-09-26, "The Arena skill: 100 sub-agents, one task, one survivor")
- **Fecha de la copia:** 2026-11-11
- **Archivos copiados sin modificar:** `SKILL.md`, `bracket.py`, `rubric.md`, `strategies.json`
- **Revisión:** `bracket.py` solo usa la librería estándar de Python y no se conecta a internet. La prueba original (`tests/test_bracket.py`, 27 pruebas) pasó completa el 2026-11-11.

## Cómo actualizarla

1. Ver el último commit de la fuente oficial (solo esa, no copias de terceros).
2. Copiar de nuevo los cuatro archivos de `skills/arena/` sin modificarlos.
3. Correr `tests/test_bracket.py` del repositorio original.
4. Actualizar en este archivo el commit y la fecha.
