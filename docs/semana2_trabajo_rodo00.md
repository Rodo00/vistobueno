# Bitácora Semana 2 — Trabajo realizado

**Integrante**: Rodo00
**Rol**: Integrante 2 — Frontend / Experiencia de usuario
**Semana**: 2 de 14 (01/09/2026 – 05/09/2026)
**Proyecto**: VistoBueno — Validador automático de formato de tesis (UNT FECyC)

---

## Objetivos de la semana

- Diseñar los mockups/wireframes de las dos pantallas principales del producto (carga y reporte).
- Implementar los componentes React que consumen la API.
- Validar la experiencia de usuario con pruebas de usabilidad.

## Actividades realizadas

| Fecha | Actividad |
|-------|-----------|
| S2 | Crear mockup HTML de la pantalla de carga (`mockups/carga.html`) |
| S2 | Crear mockup HTML de la pantalla de reporte (`mockups/reporte.html`) |
| S2 | Definir agrupación del checklist por categoría y filtro por severidad |
| S4 | Configurar proyecto React con Vite (`frontend/package.json`, `vite.config.js`, etc.) |
| S4 | Implementar componente de carga (`Upload.jsx`) con drag & drop, validación y llamada a API |
| S4 | Implementar componente de reporte (`Report.jsx`) con semáforo, resumen, filtro por severidad, checklist por categoría, prompts IA |
| S5 | Estilizar componentes para coincidir exactamente con los mockups |
| S5 | Probar funcionalidad con datos mock mientras el Integrante 1 desarrolla el endpoint |
| S6 | Refinar UI/UX: agregar responsividad mobile-first con media queries |
| S6 | Implementar modo oscuro con auto-detección (prefers-color-scheme) y toggle manual |
| S7 | Refactorizar estilos inline del reporte a clases CSS semánticas |
| S7 | Mejorar accesibilidad con focus states visibles (outline) |
| S8 | Mover `index.html` a la raíz del frontend (corrección de error 404 de Vite) |
| S8 | Verificar build de producción con `vite build` (34 módulos, sin errores) |

## Evidencias producidas

### Actividad 1: Mockups/Wireframes
- `mockups/carga.html` — Mockup navegable de la pantalla de carga (drag & drop, formatos DOCX/PDF, mensajes de error).
- `mockups/reporte.html` — Mockup navegable de la pantalla de reporte (semáforo, resumen, filtro por severidad, checklist por categoría, vista simple/detallada, sección "Cómo preguntar a una IA").

### Actividad 2: Componentes React base
- `frontend/package.json` y `vite.config.js` — Configuración del proyecto Vite con React 18.
- `frontend/src/main.jsx` — Punto de entrada de React.
- `frontend/src/components/Upload.jsx` — Componente de carga con drag & drop, validación de tipo (DOCX/PDF) y tamaño (≤ 25 MB).
- `frontend/src/components/Report.jsx` — Componente de reporte con semáforo, filtro por severidad, checklist agrupado por categoría (mapeo local de 43 reglas), prompts IA con botón copiar.
- `frontend/src/App.jsx` — Componente raíz con datos mock y alternancia Upload/Report.
- `frontend/src/index.css` — Estilos base del sistema (colores, header, tarjetas, semáforos, filtros).

### Actividad 3: Refinamiento visual y accesibilidad
- `frontend/index.css` — Refactorizado: variables CSS, mobile-first, media queries para tablet (≥600px) y desktop (≥900px), focus states accesibles.
- `frontend/src/App.jsx` — Agregado `DarkModeToggle` con auto-detección de preferencia del sistema.
- `frontend/src/components/Report.jsx` — Refactorizado: eliminación de estilos inline, uso de clases CSS semánticas.
- `frontend/index.html` — Movido a la raíz del proyecto (corrección del 404 de Vite).

## Relación con competencias curriculares

- **Ingeniería de Software II**: arquitectura de componentes, manejo de estados, comunicación cliente-servidor.
- **Interacción Humano Computador**: principios de diseño centrados en el usuario aplicados en mockups e implementación; responsividad y modo oscuro.
- **Redes de Computadoras I**: consumo de API REST mediante `fetch`, manejo de `multipart/form-data`, códigos de estado.
- **Estructura de Datos**: mapeo entre `RuleResult` del backend y la representación en frontend; agrupación de reglas con `Map` y `useMemo`.
- **Ingeniería de Software I**: refactorización de estilos, separación de responsabilidades, documentación de componentes.

## Dificultades y aprendizajes

- El reporte del motor no incluye el campo de categoría (`tipo`) en la respuesta JSON; el frontend agrupa por `rule_id` localmente (mapeo en `CATEGORIA_POR_ID`).
- El contrato de la API (`POST /validar`) lo desarrolla el Integrante 1 en la rama `week2-api-contract`; mientras tanto, se usan datos mock que imitan la forma del JSON del motor.
- Configurar Vite requirió entender los scripts y dependencias de desarrollo, y la importancia de tener `index.html` en la raíz del proyecto.
- El modo oscuro requirió decidir entre auto-detección del sistema vs toggle manual; se implementaron ambos para dar control al usuario.

## Plan de la semana siguiente

- Conectar el frontend con la API real del Integrante 1 (sustituir `MOCK_REPORT` por la respuesta del endpoint `POST /validar`).
- Verificar el contrato final de la API para ajustar el mapeo de campos si es necesario.
- Continuar refinando la UI/UX según los primeros tests de integración.
