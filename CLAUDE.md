# Reglas para Claude en esta bóveda

Lee esto antes de tocar cualquier nota.

1. **Mapa:** empieza por `Inicio.md`. Cada proyecto tiene una nota principal con el mismo nombre de su carpeta; esa nota es la puerta de entrada.
2. **Rutas fijas:** cada proyecto tiene su nota principal; las decisiones van en notas aparte con la plantilla `Plantillas/Decisión.md`. No inventes carpetas nuevas sin avisar.
3. **Lo crudo se respeta:** nunca reescribas ni borres lo que Zaryel escribió a mano. Lo tuyo va al lado, con fecha.
4. **Todo con fecha:** cada actualización lleva fecha (AAAA-MM-DD) en el campo `actualizado` y en el texto cuando sea una decisión.
5. **Bandeja:** lo que no tenga lugar claro va a `00 Inbox/Bandeja.md`.
6. **Nada secreto:** jamás guardes contraseñas, tokens, llaves ni números de cuenta. Si hace falta, escribe solo dónde están guardados.
7. **Antes de escribir, trae lo último** (pull) para no pisar lo que Zaryel editó en el iPad.
8. **Si no sabes, dilo:** no inventes datos, precios ni fechas; márcalos como "por confirmar".
9. **Idioma y estilo:** español, cuidado y claro.

## Arena

*Agregado por Claude el 2026-11-11.*

La skill `/arena` (en `.claude/skills/arena/`) pone a competir varios subagentes con la misma tarea hasta que sobrevive la mejor solución. Gasta bastante límite del plan, así que:

- Usa `/arena` solo cuando Zaryel lo pida, o cuando una respuesta importante salió mal dos veces.
- Por defecto usa el modo `--quick` (16 agentes, 91 llamadas).
- Antes de lanzar 100 agentes, avisa el número de llamadas (595) y espera la confirmación de Zaryel.
- Si el resultado cambia archivos, muestra la propuesta y pregunta antes de aplicarla.
- Los borradores del torneo quedan en `.arena/`, que está en `.gitignore` y no se sube.
- La fuente y el commit exacto de la skill están en `.claude/skills/arena/ORIGEN.md`.
