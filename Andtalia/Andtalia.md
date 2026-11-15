---
tipo: proyecto
estado: activo
actualizado: 2026-11-15
---

# 💎 Andtalia Joyeros

Joyería en oro, negocio de mis papás. Hice toda su presencia digital: tienda online, panel de administración y backend.

## Marca
- **Colores:** ónix `#12100E` · oro champaña `#C8A55C` · oro profundo `#8A6A33` · marfil `#F5F0E6` · gris piedra `#6B655B` · oro brillo `#E2C88A`
- **Tipografías:** Cormorant Garamond (títulos) y Jost (textos)
- **Logo:** diamante facetado + ANDTALIA + JOYEROS (Manual de Identidad, edición 02, oct 2026)
- **Eslogan:** "Brilla contigo, vive Andtalia" · #BrillaConAndtalia
- **Instagram:** @andtaliajoyeros

## Tecnología
- Tienda: Cloudflare Pages, proyecto **andtalia** (andtalia.com y www.andtalia.com)
- Panel de mando: Cloudflare Pages, proyecto **andtalia-mando** (mando.andtalia.com)
- Cuenta de Cloudflare: la de hola@andtalia.com. Antes estaba en Netlify (cambio confirmado el 2026-11-10).
- 2026-11-10: la web vive en **Cloudflare Pages**, proyecto `andtalia`. El proyecto "andtalia" de Netlify es la versión vieja del 30 oct y ya no recibe visitas.
- Código vigente: `Andtalia-2026-11-10-analytics.zip` (reemplaza al zip anterior del mismo día).
- Código de la web en GitHub: https://github.com/mzxryel/andtalia-web (desde 2026-11-14 la versión vigente es main `c7f24d1`)
- Backend: Supabase
- Traducción automática ES/EN con Claude Haiku
- Dominio andtalia.com en Namecheap · correo hola@andtalia.com (pasando de Zoho a Google Workspace)

## Decisiones tomadas
- **Pagos:** Bold es el único medio de pago web. El cliente paga primero y solo después ve "pago confirmado".
- **Facturación:** toda compra web lleva factura electrónica con Alegra (con NIT si el cliente lo da, si no a consumidor final).
- El cliente debe poder pedir su factura DIAN desde la compra.

## Portada con video
*Actualizado por Claude el 2026-11-14.*
- La portada abre en ónix, sin logo; el video se ve **una sola vez** y se detiene con el logo ya formado (11,8 s).
- Al terminar queda una imagen idéntica (`hero-final`) con destello y polvo de oro.
- Si el video no se puede mostrar, aparece directamente el logo final.
- Se quitaron los pósters viejos que tenían el logo.
- Publicado en Cloudflare (despliegue `1a0fdf50`). Código en GitHub: [mzxryel/andtalia-web](https://github.com/mzxryel/andtalia-web), rama main, commit `c7f24d1`.
- Ver la decisión: [[Decisión — Intro de video una vez por visita]].
- **Pregunta abierta:** ¿se borran los videos viejos de Cloudinary (carpeta `andtalia/hero`)?

## Vitrina viva
*Actualizado por Claude el 2026-11-15 (sesión del 2026-11-14).*

- **Estado:** en vista previa, esperando que Zaryel la pruebe en su iPad y su iPhone. Todavía no está unida a main.
- **Vista previa:** https://vitrina-viva.andtalia.pages.dev/
- **Decisión:** la Vitrina viva es lo principal y va primero en el inicio; lo demás va después. Ver [[Decisión — Vitrina viva primero en el inicio]].
- **Aprobado por Zaryel:** la luz al elegir una joya (sin líneas y con buen brillo).
- **Hecho:** paso a la ficha sin nada que vuele. La joya se enciende, nace un círculo de luz marfil de borde suave que llena la pantalla y la ficha entra en foco debajo (unos 1,3 s). Sirve para las fichas con foto individual.
- **Hecho:** ficha más limpia. «Descúbrela en la vitrina» con miniatura y sin caja, acciones en línea y garantías en una sola línea.
- **Al unirla a main, cuidar:** el pie de página sin NIT, los videos de portada y la rama de temporadas.

## Catálogo 2026
*Actualizado por Claude el 2026-11-15.*

- **Estado:** las 200 joyas (**AND-001 a AND-200**) ya están en Supabase (`oezipeuyamyzqrxfupuo`) como productos **ocultos**, marcados «datos incompletos». Todavía no se ven en la web.
- **Por colección:** 38 / 15 / 60 / 46 / 20 / 21 (mismo orden de la tabla de abajo).
- **Valores provisionales:** precio 0 (la casilla no puede ir vacía). Ley 18K y «mujer» son el valor por defecto, **no datos reales**: siguen pendientes. Origen vacío.
- **Candado:** la base no deja mostrar una joya incompleta. Ver [[Decisión — Catálogo 2026 cargado oculto y con candado]].
- **Supabase, hecho:** tabla de colecciones; columnas colección, color del oro, piedras, medida y notas; categoría **collares** (oculta). La próxima referencia nueva es **AND-201**.
- **Fotos grupales:** 54 en borrador con 142 piezas vinculadas. Faltan 4 bandejas por volver a fotografiar y 5 piezas dudosas por vincular.
- **Panel en vista previa** (rama `catalogo-2026`, no está en main): https://catalogo-2026.andtalia-mando.pages.dev/#/catalogo?inc=1
- **Fotos de origen:** 102 en Drive («Andtalia - Fotos Instagram»), 14 de ellas copias exactas. Las mismas, limpias, en Cloudinary (`andtalia/instagram`).
- **Entregado antes:** hoja de productos y presentación vertical.
  - Carpeta: https://drive.google.com/drive/folders/100Fg9EurIxDHbQY3jn3VSPq53QcG9Boz
  - Hoja: https://docs.google.com/spreadsheets/d/1XsRmNaMog29y5p_J2kW1hia7fCqadjCPjhy_r4-_r6I/edit
  - Presentación: https://drive.google.com/file/d/1o4yjwicmGt4hGqWzUuNCKCOj7d2XGis-/view

**Colecciones (ES / EN · número de joyas)**
| Colección | English | Joyas |
|---|---|---|
| Promesa de Brisa | Breeze Vow | 38 |
| Cayena | Hibiscus | 15 |
| Hora Dorada | Golden Hour | 60 |
| Marea | Tide | 46 |
| Bendición | Blessing | 20 |
| Puerta de Oro | Gate of Gold | 21 |

**Decisiones:** nombres propios sin marcas ni formas emblemáticas, códigos AND como referencia en Supabase y fotos limpias de Cloudinary. Ver [[Decisión — Nombres propios y códigos AND del catálogo 2026]].

**Preguntas abiertas**
- ¿AND-124, AND-140 a AND-142, AND-093 y AND-042 son joyas repetidas?
- ¿Qué se hace con las joyas de prueba que dicen «trébol» o «clavo»?
- ¿Qué se hace con las 3 fotos de ejemplo que están publicadas?
- ¿Cuáles joyas serán las destacadas?

## Inauguración del local
Ver [[Inauguración Andtalia]].

## Financiación: Addi y Sistecrédito (Fase 1)
*Actualizado por Claude el 2026-11-14.*

- **Estado:** en trámite de afiliación.
- **Hecho:** revisión de los documentos legales, hoja de afiliación ajustada a los datos reales de la empresa y 7 archivos subidos a Drive.
- **Titular:** ANDALIA JOYEROS BQ S.A.S. · representante legal: Tatiana Africano García. Ver [[Decisión — Titular y nombre en la afiliación a Addi y Sistecrédito]].
  - Nota: la razón social se escribió tal como vino en el resumen ("ANDALIA", sin T). Verificar contra el RUT.
- **Nombre:** la razón social con "JOYEROS" solo en el campo de razón social; en todo lo demás, "Andtalia Joyería".

**Preguntas abiertas**
- ¿Qué tiempo mínimo de funcionamiento exigen Addi y Sistecrédito? (preguntar a los asesores)
- ¿La fecha de los estados financieros sirve y están registrados en la Junta Central? (revisar con el contador)

## Alianzas
- Propuestas con restaurantes de Barranquilla (Don Ernesto, Baltazhar): beneficios para los dueños y servicio de joyería para pedidas de mano.

## Medición
- Google Analytics 4 creado el 2026-11-10 desde la cuenta personal de Zaryel (cuenta "Andtalia Joyeros", flujo "Web Andtalia"). ID de medición: G-CVWCRXZK6Q.
- Pendiente: dar acceso de administrador a hola@andtalia.com.
- **2026-11-10: Analytics instalado y publicado** en andtalia.com y www.andtalia.com. Ver [[Analítica con Google Analytics 4]].
  - Archivo `web/js/analitica.js`, cargado en index.html y confirmacion.html. La política de seguridad (`_headers`) ahora deja pasar a Google.
  - Eventos: `view_item` (abrir joya), `add_to_cart` (agregar o comprar ya), `begin_checkout` (antes de abrir Bold), `purchase` y `click_whatsapp`.
  - `purchase` solo cuenta pedidos ya pagados con Bold, una vez por pedido, con valor en COP, código AND-P y nombre de cada joya.
  - Si Analytics falla, la tienda y el pago siguen funcionando. Bold y Supabase no se tocaron.
  - Mando no lleva Analytics.
  - ⚠️ En Analytics quedaron **dos compras de prueba de $1.500.000** ("AND-W-1", "Cadena prueba"). No son ventas reales y Google no deja borrarlas.

## Pendientes
- [ ] Activar llaves de Bold y conectar pagos
- [ ] Crear cuenta en Alegra y conectar factura electrónica
- [ ] Subir fotos reales de productos desde el panel
- [ ] Crear Instagram y Facebook ligados a hola@andtalia.com
- [ ] Personalizar el correo de verificación de Supabase
- [ ] Plantillas de publicidad para que el dueño publique con el estilo de la marca
- [ ] Confirmar en Analytics → Tiempo real que llegan las visitas (2026-11-10)
- [ ] Borrar la llave de Cloudflare "Andtalia analytics" (2026-11-10)
- [ ] Dar acceso de administrador de Analytics a hola@andtalia.com
- [ ] Addi/Sistecrédito: conseguir el RUT de la empresa (2026-11-14)
- [ ] Addi/Sistecrédito: conseguir el certificado bancario (2026-11-14)
- [ ] Addi/Sistecrédito: conseguir la cédula de Tatiana (2026-11-14)
- [ ] Preguntar a los asesores de Addi y Sistecrédito el tiempo mínimo de funcionamiento (2026-11-14)
- [ ] Revisar con el contador la fecha de los estados financieros y su registro en la Junta Central — **vence el 2026-12-18**
- [ ] Revisar la portada con video en el iPhone y el iPad reales (2026-11-14)
- [ ] Quitar el nombre, el NIT y "JOYEROS" de la remisión del panel admin, cuando Zaryel lo autorice (2026-11-14)
- [ ] Cambiar el link de Instagram cuando exista el usuario nuevo (2026-11-14)
- [ ] Decidir si se borran los videos viejos de Cloudinary `andtalia/hero` (2026-11-14)
- [ ] Catálogo: completar los datos reales de las 200 joyas (precio, ley, género, origen, color del oro, piedras) (2026-11-15)
- [ ] Catálogo: tomar foto propia de 114 joyas (2026-11-15)
- [ ] Catálogo: decidir las joyas destacadas (2026-11-15)
- [ ] Catálogo: confirmar las repetidas: AND-124, AND-140 a 142, AND-093 y AND-042 (2026-11-15)
- [x] Claude: migración de Supabase (colecciones, campos nuevos y categoría collares) — hecho el 2026-11-15
- [x] Claude: cargar las 200 joyas como productos ocultos — hecho el 2026-11-15
- [ ] Catálogo: ajustar los puntos de las joyas en Vitrinas (2026-11-15)
- [ ] Catálogo: volver a fotografiar 4 bandejas y vincular 5 piezas dudosas (2026-11-15)
- [ ] Catálogo: decidir qué hacer con las joyas de prueba «trébol/clavo» y las 3 fotos de ejemplo publicadas (2026-11-15)
- [ ] Claude, con visto bueno: armar las páginas de colección en una rama aparte (2026-11-15)
- [ ] Vitrina viva: Zaryel la prueba en su iPad y su iPhone y la aprueba (2026-11-14)
- [ ] Claude, con visto bueno: unir la Vitrina viva a main cuidando el pie sin NIT, los videos de portada y la rama de temporadas (2026-11-14)
