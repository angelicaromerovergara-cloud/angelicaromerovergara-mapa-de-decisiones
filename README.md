# Autodiagnóstico Estratégico

Instrumento de autodiagnóstico estratégico y comercial para pymes y ejecutores de fondos públicos, construido por Angélica Romero Vergara — Consultoría Estratégica y Comercial.

Es la puerta de entrada gratuita al **Diagnóstico Estratégico Comercial** (Servicio 01) y a la **Consultoría CANVAS** (Servicio 02): el usuario responde sobre su negocio en 8 secciones, eligiendo uno de tres niveles de profundidad (Básico, Medio, Profundo), y las respuestas quedan disponibles para preparar el informe y la reunión de revisión.

## Estado actual

- Archivo fuente: `Main.dc.html` — formato "Design Component" (requiere el runtime de Claude Design para renderizar; no es HTML plano autónomo).
- Incluye la revisión de septiembre 2026: variables nuevas (necesidad del cliente, diferenciación, motor de ventas, cuello de botella operativo, dependencia del dueño, capital de trabajo, endeudamiento, rentabilidad por línea, entre otras), eliminación de preguntas de baja señal diagnóstica, y corrección de un bug en la visibilidad condicional de `f_fijosdet`/`f_vardet`.
- Las respuestas se envían a un proyecto Supabase (tabla `piloto`) configurado en `window.ARV_SUPABASE` dentro del propio archivo.
- **Este repositorio todavía no está conectado con el sitio en producción** (`https://diagnostico.angelicaromero.cl`, publicado en Netlify). Ese sitio se desplegó por carga manual de archivo, no desde Git — conectarlos es un paso pendiente y separado.

## Próximos pasos sugeridos

- Decidir si se conecta este repositorio a Netlify (despliegue continuo) o se sigue publicando por carga manual.
- Revisar visualmente los cambios en el editor de Claude Design antes de reemplazar la versión en producción.
