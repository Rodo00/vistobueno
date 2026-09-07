# Bitácora Semana 2 — Integrante 2 (Frontend/UX)

- **Nombre**: Integrante 2
- **Rol**: Frontend / Experiencia de usuario
- **Semana**: S2
- **Rama de trabajo**: `semana2-mockups-frontend`

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

## Evidencias producidas

- `mockups/carga.html` — Mockup navegable de la pantalla de carga (drag & drop, formatos DOCX/PDF, mensajes de error).
- `mockups/reporte.html` — Mockup navegable de la pantalla de reporte (semáforo, resumen, filtro por severidad, checklist por categoría, vista simple/detallada, sección "Cómo preguntar a una IA").
- `frontend/src/components/Upload.jsx` — Componente React de carga con interactividad real.
- `frontend/src/components/Report.jsx` — Componente React de reporte con datos reales o mock.
- `frontend/package.json` y configuración Vite — Proyecto listo para desarrollar.
- `docs/semana2_trabajo_retblast.md` — Bitácora semanal actualizada.

## Relación con competencias curriculares

- **Ingeniería de Software II**: arquitectura de componentes, manejo de estados, comunicación cliente-servidor.
- **Interacción Humano Computador**: principios de diseño centrados en el usuario aplicados en ambos mockups y su implementación.
- **Redes de Computadoras I**: consumo de API REST mediante `fetch`, manejo de multipart/form-data, códigos de estado.
- **Estructura de Datos**: mapeo entre `RuleResult` del backend y la representación en frontend.

## Dificultades y aprendizajes

- El reporte del motor no incluye el campo de categoría (`tipo`) en la respuesta; el frontend agrupará por ese campo cuando se implemente (pendiente coordinar con Integrante 1 el contrato final).
- El contrato de la API (`POST /validar`) lo desarrolla el Integrante 1 en la rama `week2-api-contract`; mientras tanto, usamos datos de ejemplo que imitan la forma del JSON del motor.
- Configurar Vite con React requirió entender los scripts y dependencias de desarrollo.

## Plan de la semana siguiente

- Convertir los componentes React a consumir la API real cuando el Integrante 1 tenga el endpoint listo (Act. 3, S6–S8).
- Refinar la experiencia de usuario basada en pruebas de usabilidad.
- Preparar la integración final para el despliegue.