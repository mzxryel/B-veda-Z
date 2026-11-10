---
tipo: plan
proyecto: "[[Plataforma de negocios]]"
estado: propuesta
actualizado: 2026-11-10
---

# Plan Maestro — Plataforma de negocios

Versión del 2026-11-10. Original editable: [Claude Docs](https://claude.ai/artifact/Jwt7peaWsdWRSKrkoz3sGt). Volver a [[Plataforma de negocios]].

## Resumen ejecutivo

La Plataforma será **Mostrador** (nombre recomendado): una sola aplicación web donde cada negocio vive en su propio espacio cerrado, con su marca, su inventario y sus clientes, y donde la tienda online, la caja y el WhatsApp venden del mismo inventario y facturan ante la DIAN sin doble trabajo.

**La promesa:** «Todo tu negocio en un solo mostrador: vendes en la tienda, en la caja y por WhatsApp, con un solo inventario y la DIAN al día».

**Por qué puede ganar en Colombia:** los competidores fuertes venden piezas sueltas (Alegra y Siigo facturan y llevan contabilidad; Treinta registra ventas; Tiendanube vende online). Nadie une tienda, caja, agente de WhatsApp con inteligencia artificial y un equipo humano que monta y opera el negocio. Esa última pieza es tu Agencia «mano silenciosa», y es la más difícil de copiar.

**Cómo se construye sin capital:** todo corre en planes gratis o casi gratis (Supabase, Cloudflare, Netlify, Cloudinary, Make) y se programa desde el iPad con Claude, guardando el código en GitHub. Se usa como aplicación web instalable (PWA: una página que se agrega a la pantalla de inicio y se comporta como app), así que no depende de la App Store ni de una Mac.

**Números clave (detalle en la hoja de cálculo):**

| Concepto | Valor |
| --- | --- |
| Costo fijo de operar al lanzar | ≈ $530.000 COP/mes (herramientas + contador) |
| Plan Esquina (pequeño) | $119.900 COP/mes + IVA |
| Plan Avenida (mediano) | $349.900 COP/mes + IVA |
| Plan Torre (grande) | desde $890.000 COP/mes + IVA |
| Punto de equilibrio de la operación | 5 clientes |
| Clientes para un ingreso personal de $4 millones | ≈ 41 clientes |
| Caja rápida | Montaje llave en mano de la Agencia: $390.000 a $2.900.000 por negocio |

**Ruta:** 5 fases entre el 17 de noviembre de 2026 y el 31 de mayo de 2027, con lanzamiento comercial el 1 de junio de 2027. Andtalia no se toca hasta después de su inauguración (12 y 13 de noviembre); su prueba real de 30 días va en marzo de 2027.

**Lo que la hace defendible:** red de fidelización compartida entre negocios, datos de ventas por sector en Barranquilla, plantillas por tipo de negocio hechas con experiencia real, y la Agencia como canal de venta y de operación.

**Próximo paso:** mañana, 20 minutos para escoger el nombre y revisar en la Superintendencia de Industria y Comercio que nadie lo tenga registrado (sección 10).

**Entregables de apoyo:** [modelo de precios y punto de equilibrio en Google Sheets](https://docs.google.com/spreadsheets/d/1k4Dk8wy3Bzl_7OgeP9WrNdVRHQIgK16zBfhGIeWwVQY/edit) · [hoja de ruta en Trello](https://trello.com/b/aQoUkL54/plataforma-de-negocios-hoja-de-ruta) · copia en Markdown en tu bóveda, carpeta Plataforma.

## Índice

1. Visión y nombre
2. Funciones y módulos
3. Cómo se adapta a cada tipo de negocio
4. Diseño y experiencia
5. Ventajas difíciles de copiar
6. [Negocio y precios](#6-negocio-y-precios)
7. [Hoja de ruta](#7-hoja-de-ruta)
8. [Las 10 automatizaciones clave](#8-las-10-automatizaciones-clave)
9. Riesgos y cómo evitarlos
10. Próximo paso inmediato
11. [Anexos: herramientas, obligaciones legales y fuentes](#anexos-herramientas-obligaciones-legales-y-fuentes)

Las ideas que no estaban en tu encargo aparecen marcadas como **Idea nueva**.

## 1. Visión y nombre

**Visión:** ser el sistema donde los negocios de Colombia venden, cobran, facturan y fidelizan, empezando por Barranquilla y por negocios que ya facturan, no solo emprendedores. Primero es el motor de tus negocios y de la Agencia; después, un producto que se vende solo porque los dueños ven a otros dueños usándolo.

**A quién sirve:** negocios con local físico que también venden por WhatsApp e Instagram (joyerías, cafés, licoreras, perfumerías, boutiques, salones de belleza, restaurantes pequeños), de 1 a 20 sedes, y a agencias u operadores que manejan varios negocios a la vez.

**Promesa en una frase:** «Todo tu negocio en un solo mostrador: vendes en la tienda, en la caja y por WhatsApp, con un solo inventario y la DIAN al día».

### Nombres propuestos

| Nombre | Por qué funciona | Riesgo |
| --- | --- | --- |
| **Mostrador** (recomendado) | Es el lugar donde pasa todo en un negocio colombiano: se vende, se cobra, se atiende. Se entiende sin explicar y suena cercano. | Palabra común: puede haber marcas parecidas. Registrarla con un diseño y una clase precisa (software, clase 9 y 42). |
| **Cuadre** | «Cuadrar la caja» es lo que todo dueño hace cada noche. Comunica control y tranquilidad. | Suena más contable que comercial. |
| **Manito** | «Una manito» es la ayuda que se pide en Colombia, y conecta con tu Agencia «mano silenciosa». Cálido y memorable. | Puede sonar informal para empresas grandes. |
| **Tendal** | En la Costa, «un tendal» es «un montón»: un montón de ventas, de clientes. Orgullo costeño. | Fuera de la Costa no todos lo entienden. |

Antes de decidir, revisa que el nombre esté libre en el buscador de marcas de la SIC: <https://sipi.sic.gov.co/>, y que el dominio esté disponible en Cloudflare: <https://domains.cloudflare.com/>. No pude confirmar disponibilidad desde aquí; es lo primero de la sección 10.

## 2. Funciones y módulos

Son 26 módulos sobre un mismo núcleo. **Adentro** significa que se construye en la Plataforma y es propio (diferenciador); **Conecta** significa que se apoya en una herramienta externa para lanzar rápido y sin costo. Prioridad: **I** = imprescindible, **D** = después, **F** = futuro. La fase dice cuándo entra (sección 7).

### El núcleo (lo que todo módulo usa)

Cada dato lleva la etiqueta del negocio al que pertenece, y la base de datos tiene un «candado por fila» (en Supabase se llama RLS: reglas que impiden que un negocio vea filas de otro, aunque haya un error en la pantalla). Así, Andtalia y KAFIT viven en la misma base pero nunca se cruzan.

| Módulo | Qué hace | Para quién | Adentro / Conecta | Prioridad | Fase |
| --- | --- | --- | --- | --- | --- |
| Negocios (inquilinos) y sedes | Crea cada negocio con su marca, sedes, horarios y datos legales (NIT, régimen) | Dueño, Agencia | Adentro (Supabase) | I | 1 |
| Usuarios, roles y permisos | Dueño, administrador, cajero, bodega, domiciliario, contador y «operador de Agencia», cada uno ve solo lo suyo | Todos | Adentro (Supabase Auth) | I | 1 |
| Productos y catálogo | Productos con variantes (talla, quilates, ml, sabor), fotos, precios por sede y por canal | Dueño, admin | Adentro + Cloudinary para fotos | I | 1–2 |
| Inventario multi-sede | Existencias por sede en tiempo real, traslados, conteos, lotes y números de serie | Bodega, admin | Adentro | I | 1–2 |
| Proveedores y compras | Proveedores, órdenes de compra, costos y recepción de mercancía | Admin | Adentro (borradores de correo por Gmail) | D | 2 |
| Caja / POS | Vende en el iPad o el celular, con efectivo, datáfono Bold, Nequi o transferencia; funciona sin internet y sincroniza después | Cajero | Adentro + datáfono Bold | I | 2 |
| Cierre de caja | Cuadre diario con diferencias, gastos menores y resumen al dueño | Cajero, dueño | Adentro | I | 2 |
| Tienda online por negocio | Tienda con la marca de cada negocio, en su dominio o subdominio, vendiendo del mismo inventario | Clientes finales | Adentro, publicada en Netlify con dominio en Cloudflare | I | 2 |
| Pagos | Link de pago y botón Bold; confirmación automática del pago | Dueño, clientes | Conecta (Bold) con capa propia para sumar Wompi o Mercado Pago después | I | 2 |
| Pedidos | Todos los pedidos (tienda, WhatsApp, caja, Instagram) en un solo tablero con estados | Admin, bodega | Adentro | I | 2 |
| Facturación electrónica DIAN | Factura electrónica, documento equivalente POS electrónico y notas crédito | Dueño, contador | Conecta con un proveedor tecnológico autorizado por la DIAN (no se construye el motor) | I | 2 |
| Clientes / CRM | Ficha única del cliente: compras, canal, cumpleaños, autorización de datos, notas | Dueño, vendedores | Adentro (HubSpot solo para la venta de la Plataforma) | I | 2 |
| Reportes «Hoy» | Ventas, margen, productos estrella, inventario muerto, por sede y canal | Dueño | Adentro + exportar a Google Sheets | I | 2 |
| Agente de WhatsApp para clientes | Responde, muestra catálogo con existencias reales, toma pedidos y envía link Bold; pasa a humano cuando hace falta | Clientes finales | Adentro (Claude) + WhatsApp Cloud API de Meta | I | 3 |
| **Idea nueva:** Agente del dueño | El dueño pregunta por WhatsApp o voz «¿cuánto vendí hoy?», «¿qué se está agotando?» y recibe la respuesta con datos reales | Dueño | Adentro (Claude) | I | 3 |
| Domicilios | Zonas y tarifas por barrio, asignación a domiciliario, seguimiento y cobro contra entrega | Admin, domiciliario | Adentro (luego conexión a apps de mensajería) | D | 3 |
| Fidelización | Puntos, sellos (10 cafés = 1 gratis), niveles, cupones y cumpleaños | Clientes finales | Adentro | D | 3 |
| Reservas y citas | Citas para asesoría de joyas, pruebas de perfume, reservas de mesa | Clientes finales | Calendly al inicio; agenda propia en fase 5 | D | 3 / 5 |
| Encargos y órdenes de servicio | Pedidos a la medida con abono, reparaciones con estado y fecha de entrega | Joyería, perfumería | Adentro | D | 4 |
| Contratos y firmas | Contratos de la Plataforma y de la Agencia; luego, contratos de encargos para los negocios | Dueño, Agencia | Conecta (Signeasy) | D | 5 |
| Marketing y redes | Plantillas de publicaciones por negocio, borradores programados, campañas por temporada | Dueño, Agencia | Conecta (Canva, Metricool, Abency) | D | 5 |
| Reseñas y Google Business | Pide reseña después de la compra y vigila reseñas negativas | Dueño | Conecta (Abency) | D | 5 |
| Panel de la Agencia | Ver y operar varios negocios a la vez, con permisos y reporte al dueño | Agencia | Adentro | I | 1 y 5 |
| Suscripciones y cobro de la Plataforma | Planes, cobro mensual, límites por plan, factura a cada cliente | Tú | Adentro + Bold (link de pago mensual) | I | 5 |
| Centro de ayuda y soporte | Guías cortas en video, chat de soporte por WhatsApp, estado del servicio | Clientes de la Plataforma | Adentro + Tally para encuestas | D | 5 |
| Nómina electrónica y contabilidad | Turnos, comisiones y exportación al software del contador | Contador | Conecta (exportar a Alegra o Siigo) | F | Después de la fase 5 |

**Idea nueva — Tienda que se arma sola:** el dueño manda por WhatsApp la foto de un producto y su precio; la Plataforma le quita el fondo (Cloudinary), escribe la descripción y lo publica como borrador en la tienda. Un catálogo de 50 productos queda listo en una tarde.

## 3. Cómo se adapta a cada tipo de negocio

El 80 % es igual para todos y el 20 % se activa con una **plantilla de negocio**: un paquete que trae los módulos, campos, reportes y mensajes de WhatsApp de cada sector. Abrir un negocio nuevo es escoger su plantilla y poner su marca.

**Común a todos:** negocio y sedes, usuarios y roles, catálogo, inventario, caja, tienda, pagos Bold, pedidos, facturación DIAN, clientes, reportes, agente de WhatsApp y fidelización.

| Negocio | Lo específico que se activa | Momento estrella |
| --- | --- | --- |
| **Andtalia Joyeros** (joyería) | Piezas únicas con número de serie; variantes por material, quilates y talla; encargos a la medida con abono; reparaciones con orden de servicio; citas de asesoría; separado de piezas (apartados) | **Idea nueva — Certificado digital con QR:** cada joya sale con un QR que abre su certificado, su garantía y el historial de mantenimiento; a los 6 meses llega un recordatorio de limpieza gratis que trae al cliente de vuelta |
| **KAFIT Café & Fit Bar** | Menú con modificadores (leche, proteína, tamaño); armador de smoothies; recetas que descuentan insumos del inventario; pantalla de barra para preparar pedidos; pedido para recoger en el C.C. Villa Carolina; sellos de fidelidad | **Idea nueva — Pedir desde la mesa del centro comercial:** un QR en las mesas de la plazoleta; el cliente pide y paga, y la barra recibe el pedido con su nombre |
| **ZK Licores** (licorera) | Verificación de edad en tienda y domicilio (venta a menores prohibida); zonas de domicilio por barrio con tiempos; combos y cajas; precios por volumen; lotes; crédito a clientes conocidos; bloqueo automático en ley seca | **Idea nueva — Ley seca automática:** la tienda y el agente dejan de vender solos en las fechas y horas de ley seca que decrete la autoridad, para no arriesgar multas |
| **Perfumería** (perfumes árabes) | Inventario en mililitros para decants (frascos pequeños fraccionados); costos en dólares con la tasa del día; muestras; lotes con fecha | **Idea nueva — Encuentra tu aroma:** un test de 6 preguntas en la tienda y en WhatsApp que recomienda 3 perfumes; más un sello QR de autenticidad, clave en un mercado lleno de imitaciones |
| **La Agencia «mano silenciosa»** | Panel multi-negocio; rol «operador de Agencia» que trabaja dentro del negocio sin aparecer; reporte semanal al dueño; marca blanca (la Plataforma se muestra con la marca del cliente, no con la tuya) | **Idea nueva — Operación en la sombra como servicio:** la Agencia vende «tu negocio digital operado por nosotros»; la Plataforma registra todo lo que hizo el operador para que el dueño confíe |
| **Negocios futuros** | Plantillas listas para restaurante (mesas y comandas), salón de belleza (citas y comisiones), boutique (tallas y colores), servicios (agenda y cotizaciones) | **Idea nueva — Negocio en una caja:** una plantilla trae todo para abrir en un día: tienda, menú, mensajes, publicaciones de lanzamiento y lista de chequeo legal |

KAFIT funciona como «laboratorio»: es tuyo, vende todos los días y no tiene la presión de la inauguración de Andtalia, así que allí se prueban primero la caja y la tienda (fase 2).

## 4. Diseño y experiencia

Se diseña primero para el iPad, porque es donde se vende en el mostrador, y desde ahí se adapta al celular y al computador. Todo es una sola aplicación web instalable: se abre en Safari, se toca «Agregar a pantalla de inicio» y queda como una app, sin App Store.

| Pantalla | Cómo se ve y para qué sirve |
| --- | --- |
| **iPad (mostrador)** | Dos columnas: catálogo con fotos grandes a la izquierda y el ticket a la derecha. Cobro en 3 toques. Modo «Vitrina» para girar el iPad hacia el cliente y mostrarle productos. |
| **Celular (dueño y vendedor)** | Pantalla «Hoy»: ventas del día, pedidos pendientes y alertas. Vender rápido desde el celular cuando no hay iPad. Aprobar descuentos y gastos con un toque. |
| **Computador (administración y contador)** | Tablas completas, importar productos desde Excel, reportes, facturación y exportaciones. |

**Estilo visual:** base neutra cálida (crema, grafito y blancos), tipografía clara de alta legibilidad, esquinas suaves y mucho aire. El color de acento cambia con la marca de cada negocio, así KAFIT se ve azul y verde, y Andtalia dorada, sin rediseñar nada. Modo oscuro para la noche y para locales con poca luz.

**Navegación:** cinco pestañas fijas abajo: Hoy, Vender, Productos, Clientes y Más. Arriba, una barra donde se escribe o se dicta lo que se quiere hacer («agrega 10 anillos de plata talla 7») y la Plataforma lo hace.

**Cómo cada negocio pone su marca:** sube su logo, escoge su color y su tipografía entre opciones curadas, y la Plataforma aplica todo a la tienda, los recibos, los mensajes de WhatsApp, los correos y los certificados. Puede usar su propio dominio (andtalia.com) o un subdominio gratis.

**Momentos «wow»:**

1. El primer producto aparece en la tienda 10 segundos después de mandar su foto por WhatsApp.
2. **Idea nueva — Cierre de caja que se celebra:** al cuadrar sin diferencias, la pantalla muestra el resumen del día con una animación breve y el agente le manda al dueño un audio de 20 segundos con cómo le fue.
3. El cliente recibe por WhatsApp un recibo hermoso con la marca del negocio, su factura DIAN y sus puntos.
4. El dueño abre la app y lo primero que ve es una frase útil: «Hoy vendiste 18 % más que el martes pasado; el Cacao Flow se agota mañana».

**Accesibilidad:** contraste suficiente para leer bajo la luz fuerte de un local (norma WCAG 2.2 nivel AA), botones de mínimo 44 puntos para dedos rápidos, texto que crece con el ajuste del teléfono, uso con voz, estados que no dependen solo del color y una caja que sigue vendiendo aunque se caiga el internet del centro comercial.

## 5. Ventajas difíciles de copiar

Un programa se copia en meses; una red de negocios, unos datos acumulados y un equipo que opera no se copian. Estas son las siete defensas, de la más fuerte a la más rápida de construir:

| Ventaja | Por qué cuesta copiarla | Cuándo empieza |
| --- | --- | --- |
| **Idea nueva — Red de fidelización compartida** («Puntos Mostrador») | Los puntos que gana un cliente en KAFIT sirven en Andtalia o en la perfumería y en cualquier negocio de la red. Cada negocio nuevo hace la red más valiosa para todos (efecto red). | Fase 5 |
| **La Agencia como canal y operación** | Los competidores venden software; tú vendes software más personas que lo montan y lo operan. Eso exige equipo, confianza y relaciones locales. | Desde ya |
| **Idea nueva — Termómetro del sector** | Con datos anónimos de todos los negocios, cada dueño ve cómo va contra su sector en Barranquilla («los cafés venden 22 % más en quincena»). Solo lo tiene quien ya tiene muchos negocios adentro. | Desde 20 negocios |
| **Plantillas hechas con experiencia real** | Las plantillas de joyería, café, licorera y perfumería salen de operar esos negocios, no de suposiciones. | Fases 2 a 4 |
| **Idea nueva — Calendario comercial colombiano** | Prepara solas las campañas de quincenas, primas de junio y diciembre, Día de la Madre, Amor y Amistad, Carnaval de Barranquilla y temporada navideña, por tipo de negocio. | Fase 5 |
| **Costo de cambio alto** | Historial de clientes, puntos acumulados, certificados QR en manos de los compradores y facturas: irse duele. | Crece solo con el uso |
| **Integraciones colombianas profundas** | Bold, Nequi, DIAN, ley seca, verificación de edad, Ley 2300 de cobranza: detalles que un competidor extranjero ignora. | Fases 2 y 3 |

Para proteger lo que sí se puede proteger: registrar la marca en la SIC, guardar el código en un repositorio privado y firmar acuerdos de confidencialidad (con Signeasy) con cualquier persona que entre al equipo.

## 6. Negocio y precios

Con tres planes mensuales y un cobro de montaje, la operación se paga con 5 clientes y deja un sueldo de $4.000.000 con unos 41. Todos los cálculos están en la hoja de Google Sheets, con fórmulas que puedes cambiar. Precios en pesos colombianos, sin IVA (se suma el 19 % cuando factures como responsable de IVA).

### Planes

|  | **Esquina** (pequeño) | **Avenida** (mediano) | **Torre** (grande) |
| --- | --- | --- | --- |
| Precio mensual | $119.900 | $349.900 | desde $890.000 |
| Pago anual | 10 meses (2 gratis) | 10 meses (2 gratis) | Negociado |
| Sedes | 1 | Hasta 3 | Ilimitadas |
| Usuarios | 3 | 10 | Ilimitados |
| Tienda, caja, inventario, pedidos, clientes, reportes | Sí | Sí | Sí |
| Documentos DIAN incluidos al mes | 200 | 600 | 2.000 |
| Conversaciones del agente de WhatsApp al mes | 300 | 800 | 2.500 |
| Mensajes de campaña por WhatsApp al mes | — | 300 | 1.000 |
| Fidelización, domicilios y citas | Básico | Completo | Completo |
| Agente del dueño | Sí | Sí | Sí |
| Panel multi-sede, permisos avanzados, marca blanca y conexión con otros sistemas | — | Multi-sede | Todo |
| Soporte | WhatsApp en horario laboral | WhatsApp prioritario | Asesor asignado |
| Montaje llave en mano (pago único, lo hace la Agencia) | $390.000 | $990.000 | desde $2.900.000 |
| Margen estimado por cliente al mes | ≈ $65.500 (55 %) | ≈ $187.200 (53 %) | ≈ $370.600 (42 %) |

Extras: documento DIAN adicional a $200; 100 conversaciones extra a $15.000; fotos profesionales con IA y gestión de redes como servicios de la Agencia. Referencia de mercado: Alegra cobra $74.900 al mes solo por contabilidad y facturación en su plan más básico, y Treinta entre 9,99 y 19,99 dólares; ninguno trae tienda, caja y agente de WhatsApp juntos.

### Costos de operar

| Herramienta | Plan para empezar | Cuándo pagar | Costo mensual estimado |
| --- | --- | --- | --- |
| Supabase (base de datos y usuarios) | Gratis | Con el primer cliente real: el plan gratis se pausa tras 7 días sin uso | 25 USD + 10 USD por dominio propio |
| Cloudflare (dominios, seguridad, funciones, respaldos) | Gratis | Al superar el límite gratis de funciones | 5 USD |
| Netlify (publicar panel y tiendas) | Gratis | Cuando el tráfico lo exija (verificar precio entonces) | 0 USD al inicio |
| Make (automatizaciones) | Gratis: 1.000 créditos y 2 escenarios | Desde la fase 2 | ≈ 10,59 USD (plan Core) |
| Claude (cerebro del agente de WhatsApp) | Pago por uso | Desde la fase 3 | ≈ 20 USD base (estimado, verificar) |
| WhatsApp Cloud API (Meta) | Pago por mensaje | Desde la fase 3 | 0,0008 USD por aviso de servicio; 0,0125 USD por mensaje de campaña |
| Proveedor de facturación DIAN | Por documento | Desde la fase 2 | ≈ $120 por documento (supuesto a confirmar con cotización) |
| Dominio .co | Pago anual | Fase 1 | ≈ 3 USD al mes |
| Cloudinary, Canva, Trello, Tally, Calendly, HubSpot, Metricool, Signeasy, Google | Planes gratis o los que ya tienes | Al crecer | 0 USD al inicio |
| Contador | Por horas | Desde la fase 5 | $250.000 |

Con una tasa de $3.800 por dólar (supuesto conservador, editable en la hoja), el costo fijo es de ≈ $529.600 al mes.

### Punto de equilibrio

Con una mezcla de 70 % Esquina, 25 % Avenida y 5 % Torre, cada cliente deja en promedio ≈ $111.200 al mes. La operación se paga con 5 clientes; un ingreso personal de $4.000.000 al mes exige 41 clientes. El montaje llave en mano no entra en ese cálculo: es caja extra desde el primer día.

### Cómo conseguir los primeros clientes y capital sin inversión

1. **La Agencia vende primero el montaje, no el software.** Ofrece «tu negocio vendiendo por WhatsApp y tienda online en 7 días» a negocios de Barranquilla. El montaje se cobra por adelantado (50 % al firmar) y paga el desarrollo.
2. **Vecinos del C.C. Villa Carolina.** Los locales y kioscos de tu mismo centro comercial ven KAFIT funcionando; son los 10 primeros prospectos naturales.
3. **Idea nueva — Socios Fundadores.** Los primeros 15 negocios pagan un año por adelantado con 40 % de descuento y precio congelado de por vida. Con 15 planes Esquina son ≈ $10.800.000 de caja antes del lanzamiento.
4. **Idea nueva — Contadores como vendedores.** Cada contador maneja decenas de negocios. Se les da 20 % de comisión mensual por cliente referido y un acceso gratis para revisar la facturación de sus clientes.
5. **Casos reales como prueba.** Andtalia y KAFIT con sus números (con permiso) son la mejor publicidad.
6. **Programas públicos sin devolver dinero.** Revisar convocatorias vigentes de iNNpulsa (<https://www.innpulsacolombia.com/>), Fondo Emprender del SENA (<https://www.fondoemprender.com/>) y la Cámara de Comercio de Barranquilla (<https://www.camarabaq.org.co/>). No confirmé fechas de convocatoria abiertas hoy.

## 7. Hoja de ruta

Son 28 semanas, del 17 de noviembre de 2026 al 31 de mayo de 2027, calculadas para una persona sola con unas 20 horas a la semana, trabajando desde el iPad con Claude (proyecto «⚡ Ejecutor») y guardando todo en GitHub. Cada fase termina con una condición clara para pasar a la siguiente. Las mismas tareas están como tarjetas en Trello.

**Cómo se programa desde el iPad:** Claude escribe el código y lo sube a tu repositorio de GitHub; Netlify publica solo cada cambio; tú revisas en Safari y apruebas. No necesitas Mac, ni terminal, ni instalar nada en el iPhone.

| Fase | Fechas | Qué queda funcionando | Condición para pasar |
| --- | --- | --- | --- |
| 1. Datos para varios negocios | 17 nov – 13 dic 2026 (4 semanas) | Base de datos con negocios, sedes, roles, productos, inventario y clientes, con candados por negocio | Prueba automática: un negocio no puede ver datos de otro |
| 2. Panel + tienda + caja | 14 dic 2026 – 7 feb 2027 (8 semanas, con pausa de fin de año) | Panel en el iPad, caja, tienda online, pagos Bold y facturación DIAN, probados en KAFIT | KAFIT vende una semana completa sin volver al sistema anterior |
| 3. Agente de WhatsApp | 8 feb – 7 mar 2027 (4 semanas) | Agente que atiende, muestra existencias reales, toma pedidos y cobra; agente del dueño | 50 conversaciones de prueba con 90 % bien resueltas |
| 4. Prueba real de 30 días en Andtalia | 8 mar – 11 abr 2027 (5 semanas) | Andtalia operando en la Plataforma, con medición diaria | Cero pérdidas de inventario y tus papás quieren quedarse |
| 5. Producto + 3 pilotos | 12 abr – 31 may 2027 (7 semanas) | Planes, cobro, contratos, ayuda y 3 negocios pagando | 3 pilotos activos y lanzamiento el 1 de junio de 2027 |

### Fase 1 — Datos para varios negocios

1. Escoger el nombre, revisar la marca en la SIC y comprar el dominio.
2. Dibujar con Claude el mapa de datos (qué tablas hay y cómo se conectan) y guardarlo en la bóveda.
3. Crear las tablas en el proyecto «plataforma-negocios», todas con la etiqueta del negocio.
4. Activar los candados por fila (RLS) en cada tabla.
5. Crear los roles: dueño, administrador, cajero, bodega, domiciliario, contador y operador de Agencia.
6. Cargar datos de prueba de KAFIT y de Andtalia (copias, sin tocar la Andtalia real).
7. Prueba automática de aislamiento entre negocios.
8. Respaldo diario automático a Cloudflare R2 (almacenamiento de archivos).
9. Borrador de política de tratamiento de datos y términos de uso.

### Fase 2 — Panel + tienda + caja

1. Sistema de diseño con la marca de cada negocio (colores, logo, tipografía).
2. Panel instalable en el iPad: productos, inventario y clientes.
3. Fotos de productos con Cloudinary (carpeta por negocio).
4. Caja con modo sin internet y cierre de caja.
5. Tienda online por negocio, publicada en Netlify con subdominio en Cloudflare.
6. Link y botón de pago Bold con confirmación automática.
7. Escoger proveedor de facturación DIAN, cotizar y conectar en modo de pruebas.
8. Tablero de pedidos y reportes «Hoy».
9. Piloto interno en KAFIT durante una semana.

### Fase 3 — Agente de WhatsApp

1. Número dedicado y verificación del negocio en Meta (WhatsApp Cloud API).
2. Agente que responde preguntas con el catálogo y las existencias reales.
3. Toma de pedidos y envío del link Bold.
4. Paso a una persona cuando el cliente lo pide o el agente duda.
5. Plantillas aprobadas por Meta: confirmación, envío y recordatorio.
6. Registro de la autorización del cliente para recibir mensajes.
7. Agente del dueño.
8. 50 conversaciones de prueba y ajustes.

### Fase 4 — Prueba real de 30 días en Andtalia

1. Acordar con tus papás qué se prueba, quién decide y cómo se vuelve atrás si algo falla.
2. Pasar el catálogo de Andtalia a la Plataforma y operar en paralelo la primera semana.
3. Capacitación de una hora al equipo.
4. Medir cada día: tiempo por venta, diferencias de inventario, ventas por WhatsApp, facturas rechazadas y errores.
5. Bitácora de fallos en Trello y arreglos semanales.
6. Activar encargos, reparaciones y certificado QR.
7. Revisión final y decisión de seguir.

### Fase 5 — Producto + 3 pilotos

1. Página de venta y lista de espera (Tally).
2. Planes, límites y cobro mensual con Bold.
3. Contrato de servicio y de tratamiento de datos (Signeasy).
4. Escoger 3 pilotos: KAFIT y dos negocios externos de la Agencia.
5. Montaje de cada piloto en un día con lista de chequeo.
6. Centro de ayuda con videos cortos y soporte por WhatsApp.
7. Formalizar la empresa y la facturación de la Plataforma con un contador.
8. Casos de éxito con permiso y lanzamiento el 1 de junio de 2027.

## 8. Las 10 automatizaciones clave

Make es el «pegamento» entre herramientas: cuando pasa algo en una, hace algo en otra, sin que nadie toque nada. Se activan solo con tu «hazlo», y las que mandan mensajes a clientes o publican quedan como borrador hasta que tú las apruebes. Con el tiempo, las más usadas se pasan adentro de la Plataforma para depender menos de Make.

| # | Cuando pasa esto… | …ocurre esto | Herramientas | Fase |
| --- | --- | --- | --- | --- |
| 1 | Bold confirma un pago | El pedido queda pagado, se emite la factura DIAN y el cliente recibe recibo y factura por WhatsApp | Bold, Plataforma, proveedor DIAN, WhatsApp | 2 |
| 2 | Entra un pedido online | Se crea la tarjeta de preparación, se avisa al cliente y se anota en la hoja de ventas | Plataforma, Trello, WhatsApp, Google Sheets | 2 |
| 3 | Un producto baja del mínimo | Alerta al dueño y borrador de pedido al proveedor en Gmail, sin enviarlo | Plataforma, WhatsApp, Gmail | 2 |
| 4 | Se cierra la caja | Resumen del día al dueño y fila nueva en la hoja de control | Plataforma, WhatsApp, Google Sheets | 2 |
| 5 | Se sube la foto de un producto nuevo | Cloudinary limpia la foto, Canva arma la publicación y Metricool la deja como borrador para revisión | Cloudinary, Canva, Metricool | 2 |
| 6 | Un negocio se inscribe en la lista de espera | Se crea el contacto en HubSpot, se le envía el link de Calendly y aparece una tarjeta «Prospecto» en Trello | Tally, HubSpot, Calendly, Trello | 5 |
| 7 | Alguien agenda una demostración | El negocio avanza en HubSpot, se bloquea el espacio en Google Calendar y llega un recordatorio 24 horas antes | Calendly, HubSpot, Google Calendar | 5 |
| 8 | Un cliente firma el contrato | Se crea su negocio en la Plataforma con su plantilla, una carpeta en Drive y la lista de montaje en Trello | Signeasy, Plataforma, Google Drive, Trello | 5 |
| 9 | Pasan 2 días desde una compra | Se pide la reseña en Google; si llega una reseña negativa, alerta inmediata al dueño | Plataforma, Abency (Google Business) | 5 |
| 10 | Es lunes a las 7 a. m. | Reporte semanal de ventas y anuncios: Windsor.ai junta Meta y Google, lo pone en Sheets y el dueño recibe el resumen | Windsor.ai, Google Sheets, Gmail | 5 |

El plan gratis de Make (1.000 créditos y 2 escenarios activos) alcanza para probar; desde la fase 2 se necesita el plan Core.

## 9. Riesgos y cómo evitarlos

| Riesgo | Tipo | Qué puede pasar | Cómo se evita |
| --- | --- | --- | --- |
| Un negocio ve datos de otro | Técnico | Fuga de información y pérdida de confianza | Candados por fila en todas las tablas y prueba automática antes de cada publicación |
| El plan gratis de Supabase se pausa | Técnico | La tienda se cae tras 7 días sin uso | Pasar a Pro (25 USD) con el primer cliente real; respaldo diario en Cloudflare R2 |
| Se cae el internet del local | Técnico | No se puede vender | Caja que funciona sin conexión y sincroniza después |
| Dependes solo de ti | Operativo | Si te enfermas o te saturas, todo se detiene | Código y decisiones en GitHub y en la bóveda; manual de operación; no sumar más de 3 pilotos a la vez |
| Saturación con Andtalia y KAFIT | Operativo | La Plataforma se retrasa o los negocios se descuidan | Bloques fijos de trabajo a la semana; fases con condiciones claras, no con fechas a la fuerza |
| Meta bloquea el número de WhatsApp | Dependencia | El agente deja de funcionar | Solo la API oficial, mensajes con autorización previa, nada de envíos masivos sin permiso, número de respaldo |
| Suben los precios de Meta, Supabase o Claude | Dependencia | Baja el margen | Los límites de cada plan absorben el cambio; precios revisados cada 6 meses; la hoja recalcula sola |
| Bold cambia condiciones o falla | Dependencia | No entran pagos | Capa propia de pagos para sumar Wompi o Mercado Pago sin rehacer nada |
| Make se vuelve caro o cambia | Dependencia | Automatizaciones detenidas | Pasar las más usadas a funciones propias en Cloudflare o Supabase |
| La DIAN cambia reglas | Legal | Facturas rechazadas | Usar un proveedor autorizado que se actualiza por obligación; no construir el motor DIAN |
| Tratamiento de datos sin autorización | Legal | Sanciones de la SIC | Autorización registrada por cliente, política publicada, contrato de transmisión de datos con cada negocio |
| Cobros de cartera mal hechos | Legal | Quejas y multas por la Ley 2300 de 2023 | Recordatorios de pago solo en los horarios y con la frecuencia que permite la ley |
| Venta de licor a menores o en ley seca | Legal | Sanciones y cierre | Verificación de edad y bloqueo automático en ley seca |
| Alegra, Siigo, Treinta o Tiendanube copian | Comercial | Guerra de precios | Competir por red, Agencia y plantillas, no por precio (sección 5) |
| Los pilotos no pagan después de la prueba | Comercial | No hay ingresos | Montaje cobrado por adelantado y contrato firmado desde el inicio |
| La prueba en Andtalia afecta sus ventas | Comercial | Problema familiar y comercial | Operar en paralelo la primera semana y plan para volver atrás en una hora |

## 10. Próximo paso inmediato

Mañana, miércoles 11 de noviembre, dedica 20 minutos a escoger el nombre. Andtalia inaugura el 12 y 13, así que la construcción arranca el lunes 17.

- [ ] Lee el resumen ejecutivo y la sección 1, y escoge entre Mostrador, Cuadre, Manito y Tendal.
- [ ] Busca el nombre escogido en la SIC: <https://sipi.sic.gov.co/>
- [ ] Revisa si el dominio está libre en Cloudflare: <https://domains.cloudflare.com/>
- [ ] El lunes 17, dile al proyecto «⚡ Ejecutor»: «Arranca la Fase 1, tarea 2: el mapa de datos de la Plataforma».

No compres el dominio ni pases Supabase a pago todavía: eso se hace cuando el nombre esté confirmado y haya un cliente real.

## Anexos: herramientas, obligaciones legales y fuentes

### A. Cada herramienta conectada y su uso

| Herramienta | Uso en tu operación interna | Se ofrece a los clientes de la Plataforma |
| --- | --- | --- |
| Supabase | Base de datos, usuarios y candados por negocio (proyecto «plataforma-negocios») | Sí, por dentro: es el motor de todo |
| Cloudflare | Dominios, seguridad, funciones que reciben avisos de Bold y WhatsApp, respaldos en R2 | Sí: dominio o subdominio propio para cada negocio |
| Netlify | Publica el panel y las tiendas cada vez que hay un cambio | Sí, por dentro: cada tienda vive allí |
| GitHub | Código de la Plataforma y bóveda de Obsidian | No |
| Canva | Plantillas de marca y publicaciones por negocio | Sí, como servicio de la Agencia |
| Adobe | Retoque de fotos, catálogos y contratos en PDF | Sí, como servicio de la Agencia |
| Cloudinary | Fotos y videos de productos, carpeta por negocio, fondo blanco automático | Sí, por dentro |
| Metricool | Programar publicaciones de tus negocios y de clientes de la Agencia | Sí, como servicio de la Agencia |
| Windsor.ai | Juntar datos de anuncios y redes en reportes | Sí, en el reporte semanal (plan Avenida y Torre) |
| Abency | Google Business, reseñas, SEO y anuncios | Sí, como servicio de la Agencia |
| Tally | Lista de espera, montaje de clientes, encuestas de satisfacción | Sí: formularios de pedidos especiales para los negocios |
| Calendly | Demostraciones de venta de la Plataforma | Al inicio, para citas de joyería; luego se reemplaza por la agenda propia |
| HubSpot | CRM para vender la Plataforma y la Agencia | No: los clientes usan el CRM propio de la Plataforma |
| Signeasy | Contratos con clientes y acuerdos de confidencialidad | Más adelante: contratos de encargos para los negocios |
| Trello | Hoja de ruta, montaje de clientes, bitácora de fallos | No |
| Make | Automatizaciones entre herramientas (sección 8) | Indirecto: las automatizaciones trabajan para ellos |
| Gmail, Google Calendar, Drive y Sheets | Correo, agenda, carpetas por cliente, modelo financiero | Sí: exportar reportes a Sheets |

### B. Obligaciones legales colombianas que aplican

No soy abogado ni contador: esta lista sirve para preparar la conversación con ellos, no la reemplaza.

1. **Facturación electrónica (DIAN, Resolución 000165 de 2023):** cada negocio factura con su propio NIT y su habilitación; las ventas en caja requieren factura o documento equivalente POS electrónico. La Plataforma usa un proveedor tecnológico autorizado y factura a sus propios clientes la suscripción con IVA del 19 %.
2. **Protección de datos (Ley 1581 de 2012 y Decreto 1377 de 2013, hoy en el Decreto 1074 de 2015):** cada negocio es el responsable de los datos de sus clientes y la Plataforma es la encargada. Hace falta política de tratamiento publicada, autorización previa de cada cliente, contrato de transmisión de datos con cada negocio (los servidores están en Estados Unidos) y revisar si aplica el Registro Nacional de Bases de Datos de la SIC.
3. **Estatuto del Consumidor (Ley 1480 de 2011):** precio total visible con impuestos, información clara del producto, derecho de retracto de 5 días hábiles y reversión del pago en ventas a distancia, y garantías.
4. **Comercio electrónico y firmas (Ley 527 de 1999):** da validez a contratos y firmas electrónicas como las de Signeasy.
5. **Cobranza (Ley 2300 de 2023):** limita horarios, días y frecuencia de los recordatorios de pago; se programa en la Plataforma.
6. **Licores:** prohibida la venta a menores de edad (Ley 124 de 1994 y Código de Policía, Ley 1801 de 2016) y obligatorio respetar la ley seca que decreten las autoridades.
7. **Mensajes de marketing:** solo a quien autorizó recibirlos, con opción fácil de darse de baja.
8. **Marca y software:** registrar el nombre en la SIC; el código puede registrarse como derecho de autor ante la Dirección Nacional de Derecho de Autor.
9. **Tu empresa:** RUT con la actividad de software, régimen tributario (evaluar el Régimen Simple con el contador) y nómina electrónica cuando contrates.

### C. Fuentes consultadas (10 de noviembre de 2026)

- Precios de WhatsApp Business por mensaje: [Leadsales](https://leadsales.io/blog/whatsapp-business-api-cuanto-cuesta/) y [documentación de Meta](https://developers.facebook.com/docs/whatsapp/pricing)
- Planes de Supabase: [Toolradar, verificado noviembre de 2026](https://toolradar.com/tools/supabase/pricing) y [Makerkit](https://makerkit.dev/blog/saas/supabase-pricing)
- Planes de Make: [Latenode](https://latenode.com/blog/make-com-pricing) y [Jetadmin](https://www.jetadmin.io/blog/make-pricing/)
- Comisiones de pasarelas en Colombia: [Guía de Software](https://www.guiadesoftware.com/blog/mejor-pasarela-pago-colombia)
- Precios de Alegra y Siigo: [Blog de Alegra](https://blog.alegra.com/colombia/alegra-vs-loggro-colombia/)
- Precios de Treinta: [App Store](https://apps.apple.com/app/id1644703591)
- Costo por documento de facturación electrónica: [portafolio de Sofisis](https://sofisis.com/static/sofisis_site/site/pdf/portafolio_facturacion_electronica_colombia.pdf)

Por confirmar con cotización: la comisión exacta de Bold para link y botón de pago, el precio del proveedor DIAN escogido y el costo real por conversación del agente con Claude.
