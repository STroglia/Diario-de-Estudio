# Bitácora de Decisiones Técnicas y Aprendizaje (MEMORY)
## Proyecto: Diario de Estudio

### Estado del Proyecto
- **Fase:** Versión 1.0 Finalizada y funcional al 100%.
- **Componentes validados:** Interfaz web lista, consola sin errores, persistencia operativa en el navegador mediante la clave exacta `diario-estudio-v1`, y lógica de rachas consecutivas probada.

### Decisiones de Arquitectura
- **Persistencia Local:** Se optó por utilizar `localStorage` con la clave `'diario-estudio-v1'` para cumplir con los requerimientos de la cátedra, logrando un prototipo ligero y directo sin necesidad de levantar un backend o base de datos externa.
- **Manejo de Fechas sin Desfasaje UTC:** Para evitar discrepancias de zona horaria al guardar y comparar fechas, se utiliza el formato estandarizado `YYYY-MM-DD` generado mediante `toLocaleDateString('en-CA')`.

### Reglas de Negocio Implementadas
1. **Registro de Sesión:** Exige de manera obligatoria la carga de Fecha, Materia, Tema y Minutos.
2. **Cálculo de Racha Consecutiva:**
   - Agrupa y ordena las fechas únicas de estudio.
   - Ignora automáticamente las fechas mayores al día de hoy para evitar saltos temporales futuros.
   - Si no hay registro el día de hoy pero sí ayer, la racha se mantiene activa; si no se estudió ni ayer ni hoy, la racha vuelve a 0.

### Desafíos Superados y Buenas Prácticas
- **Autenticación y Entorno:** Configuración inicial del entorno CLI y resolución de credenciales mediante GitHub Copilot dentro de OpenCode.
- **Depuración:** Validación de la consola del navegador (`No issues`) para garantizar un código limpio y libre de errores en tiempo de ejecución.

### Entorno y Herramientas Utilizadas
- **CLI / Asistencia:** OpenCode configurado con GitHub/Copilot para la generación asistida del prototipo inicial de código.
- **Editor:** Cursor como entorno de desarrollo principal.