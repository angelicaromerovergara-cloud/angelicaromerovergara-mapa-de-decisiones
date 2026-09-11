# Mapa de Decisiones

Instrumento de autodiagnóstico estratégico y comercial para pymes y ejecutores de fondos públicos, construido por Angélica Romero Vergara — Consultoría Estratégica y Comercial. Antes llamado "Autodiagnóstico Estratégico".

Es la puerta de entrada gratuita al **Diagnóstico Estratégico Comercial** (Servicio 01) y a la **Consultoría CANVAS** (Servicio 02): el usuario responde sobre su negocio en 8 secciones, eligiendo uno de tres niveles de profundidad (Básico, Medio, Profundo), y las respuestas quedan disponibles para preparar el informe y la reunión de revisión.

## Estado actual

- Archivo fuente: `Main.dc.html` — formato "Design Component" (requiere el runtime de Claude Design para renderizar; no es HTML plano autónomo).
- Incluye la revisión de septiembre 2026: variables nuevas (necesidad del cliente, diferenciación, motor de ventas, cuello de botella operativo, dependencia del dueño, capital de trabajo, endeudamiento, rentabilidad por línea, entre otras), eliminación de preguntas de baja señal diagnóstica, y corrección de un bug en la visibilidad condicional de `f_fijosdet`/`f_vardet`.
- Las respuestas se envían a un proyecto Supabase (tabla `piloto`) configurado en `window.ARV_SUPABASE` dentro del propio archivo.
- **Repositorio dedicado**: este proyecto vive en `angelicaromerovergara-cloud/angelicaromerovergara-autodignostico` (pendiente de renombrar a `mapa-de-decisiones` — requiere hacerlo desde GitHub Settings, no hay API/CLI de GitHub disponible en este entorno).
- **Este repositorio todavía no está conectado con el sitio en producción** (`https://diagnostico.angelicaromero.cl`, publicado en Netlify como proyecto `autodiagnosticoarv`). Ese sitio se desplegó por carga manual de archivo, no desde Git — conectarlos es un paso pendiente y separado.
- Nombres internos (claves de `localStorage`, variable `ARV_SUPABASE`, tabla `piloto`) se mantienen sin cambios por ahora para no romper continuidad de datos del piloto en curso; solo se actualizó el texto visible al usuario ("MAPA DE DECISIONES" en el encabezado) y el nombre del instrumento en esta documentación.

## Renombrado pendiente ("Autodiagnóstico Estratégico" → "Mapa de Decisiones")

- [x] Texto visible en el encabezado del instrumento (`Main.dc.html`)
- [x] Este README
- [ ] Nombre del repositorio en GitHub (`angelicaromerovergara-autodignostico` → `mapa-de-decisiones`) — manual, vía GitHub Settings → Rename
- [ ] Nombre del proyecto en Netlify (`autodiagnosticoarv` → `mapa-de-decisiones`) — pendiente a pedido explícito, no se tocó por ahora
- [ ] Dominio público (`diagnostico.angelicaromero.cl`) — pendiente de decisión, implica cambios de DNS

## Próximos pasos sugeridos

- Renombrar el repositorio en GitHub y actualizar el remoto local.
- Decidir si se conecta este repositorio a Netlify (despliegue continuo) o se sigue publicando por carga manual.
- Revisar visualmente los cambios en el editor de Claude Design antes de reemplazar la versión en producción.
