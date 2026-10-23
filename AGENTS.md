# Guía de Contexto para Agentes de IA - Diario de Estudio

## Propósito del Proyecto
Este proyecto es un prototipo funcional de un "Diario de Estudio" orientado a estudiantes de nivel terciario. Permite registrar sesiones de estudio, mantener un historial persistente y calcular la racha de días consecutivos de estudio de forma automatizada.

## Arquitectura y Stack Tecnológico
- **Frontend:** HTML5, CSS3 y JavaScript vanilla (ES6+).
- **Sin Dependencias:** No se utilizan frameworks (React, Vue, etc.) ni paquetes de Node/npm.
- **Persistencia:** Datos almacenados localmente mediante `localStorage` utilizando exactamente la clave `diario-estudio-v1`.

## Estructura de Archivos
- **index.html:** Estructura semántica de la interfaz (formulario de registro, tarjeta de racha e historial).
- **styles.css:** Diseños y estilos responsivos estructurados con CSS Grid/Flexbox.
- **app.js:** Lógica de interacción, manipulación del DOM, cálculo de rachas y gestión del `localStorage`.
- **AGENTS.md:** Guía de contexto técnico para desarrolladores y agentes de IA.
- **MEMORY.md:** Bitácora de decisiones técnicas, estado del proyecto y reglas de negocio.

## Reglas Principales para Modificaciones
1. **Independencia Tecnológica:** Mantener la solución en JavaScript puro, evitando incorporar librerías externas o gestores de paquetes.
2. **Formato de Fechas:** Las fechas almacenadas en `localStorage` deben mantenerse en formato `YYYY-MM-DD`, alineadas estrictamente a la zona horaria local mediante `toLocaleDateString('en-CA')`.
3. **Validación Temporal:** El cálculo de la racha debe omitir y filtrar de forma automática cualquier registro con fechas futuras.

## Instrucciones de Verificación
- **Consola del Navegador:** Al inspeccionar la aplicación (F12), la consola debe mantenerse limpia y libre de errores en tiempo de ejecución (`No issues`).
- **Persistencia:** Recargar la página (F5) no debe alterar ni eliminar los registros previos del historial ni el contador de rachas.
