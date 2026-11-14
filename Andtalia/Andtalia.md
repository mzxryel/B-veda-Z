---
tipo: proyecto
estado: activo
actualizado: 2026-11-14
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
- Backend: Supabase
- Traducción automática ES/EN con Claude Haiku
- Dominio andtalia.com en Namecheap · correo hola@andtalia.com (pasando de Zoho a Google Workspace)

## Decisiones tomadas
- **Pagos:** Bold es el único medio de pago web. El cliente paga primero y solo después ve "pago confirmado".
- **Facturación:** toda compra web lleva factura electrónica con Alegra (con NIT si el cliente lo da, si no a consumidor final).
- El cliente debe poder pedir su factura DIAN desde la compra.

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
