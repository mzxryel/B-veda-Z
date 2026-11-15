---
tipo: decisión
proyecto: Andtalia
fecha: 2026-11-15
---

# Decisión — Catálogo 2026 cargado oculto y con candado

*Registrado por Claude el 2026-11-15.* Proyecto: [[Andtalia]].

## Qué decidí
- Las 200 joyas AND-001 a AND-200 se cargaron en Supabase como **productos ocultos**, marcados «datos incompletos».
- Mientras falten datos, se usan valores de relleno: precio 0, ley 18K y «mujer». Son provisionales, **no datos reales**. Origen queda vacío.
- La base de datos tiene un **candado**: no deja mostrar en la web una joya con datos incompletos.
- La próxima referencia nueva es **AND-201**.

## Por qué
- Tener todo el catálogo ya dentro del panel para completarlo poco a poco.
- La casilla de precio no puede ir vacía, por eso el 0.
- El candado evita que una joya salga a la venta con precio 0 o datos falsos por error.

## Qué descarté
- Esperar a tener todos los datos completos antes de cargar.
- Publicar joyas con datos de relleno.

## Qué cambia a partir de ahora
- Cada joya se publica solo cuando Zaryel complete sus datos reales en el panel.
- Ley 18K y «mujer» se deben revisar joya por joya, aunque ya aparezcan llenos.
