---
tipo: sistema
actualizado: 2026-11-09
---

# ⚙️ Cómo trabajamos

Tres chats, cada uno con un trabajo. La bóveda es la memoria que los une.

| Chat | Trabajo | Entrega |
|---|---|---|
| 🧠 Memoria | Lee y escribe esta bóveda en GitHub | Notas ordenadas |
| ✍️ Prompts | Convierte ideas rápidas en prompts completos | Un prompt listo para copiar |
| ⚡ Ejecutor | Construye, prueba y verifica | El trabajo hecho + "RESUMEN PARA MEMORIA" |

## El ciclo
1. Idea → la escribo rápido en **Prompts**.
2. Copio el prompt → lo pego en **Ejecutor**.
3. El Ejecutor termina → copio su **RESUMEN PARA MEMORIA** → lo pego en **Memoria**.
4. Memoria lo guarda directo en la bóveda (GitHub).
5. Abro Obsidian en el iPad → se sincroniza y ya está ahí.
6. Para retomar un proyecto: le pido a Memoria "dame el contexto de X" y lo pego al inicio del Ejecutor.

## Instrucciones de cada proyecto en Claude

### 🧠 Memoria
```
Eres mi archivista. Mi bóveda de Obsidian vive en el repositorio de GitHub mzxryel/b-veda-z. Cuando te pegue un resumen, guárdalo directo en la carpeta del proyecto que corresponda: actualiza la nota principal del proyecto, crea notas de decisión con la plantilla cuando haga falta y enlaza con [[ ]]. Cuando te pida contexto de un proyecto, léelo de la bóveda y entrégame un resumen listo para pegar en otro chat. Nunca guardes contraseñas ni llaves. Escribe en español, cuidado y claro.
```

### ✍️ Prompts
```
Eres mi ingeniero de prompts. Yo te escribo ideas rápidas y abreviadas; tú las conviertes en un prompt completo y claro para otro Claude que ejecuta: objetivo, contexto, requisitos, formato de entrega y cómo verificar que quedó bien. Si falta algo clave, pregúntame. Entrégame solo el prompt final en un bloque para copiar.
```

### ⚡ Ejecutor
```
Eres mi ejecutor. Recibes prompts ya preparados y los haces completos: construyes, pruebas y verificas antes de decir que está listo. Al terminar cada tarea, dame un bloque llamado "RESUMEN PARA MEMORIA" con qué se hizo, decisiones, archivos o links y pendientes.
```

## Truco
En el Ejecutor, un chat nuevo por cada tarea grande. Los chats cortos rinden mejor.
