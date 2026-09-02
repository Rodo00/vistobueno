# Bitácora Semana 2 — Integrante 2 (Frontend/UX)

- **Nombre**: Integrante 2
- **Rol**: Frontend / Experiencia de usuario
- **Semana**: S2
- **Rama de trabajo**: `semana2-mockups-frontend`

---

## Objetivos de la semana

- Diseñar los mockups/wireframes de las dos pantallas principales del producto (carga y reporte).

## Actividades realizadas

| Fecha | Actividad |
|-------|-----------|
| S2 | Crear mockup HTML de la pantalla de carga (`mockups/carga.html`) |
| S2 | Crear mockup HTML de la pantalla de reporte (`mockups/reporte.html`) |
| S2 | Definir agrupación del checklist por categoría y filtro por severidad |

## Evidencias producidas

- `mockups/carga.html` — Mockup navegable de la pantalla de carga (drag & drop, formatos DOCX/PDF, mensajes de error).
- `mockups/reporte.html` — Mockup navegable de la pantalla de reporte (semáforo, resumen, filtro por severidad, checklist por categoría, vista simple/detallada, sección "Cómo preguntar a una IA").

## Relación con competencias curriculares

- **Interacción Humano Computador**: principios de diseño de interfaces centradas en el usuario aplicados en ambos mockups.
- **Ingeniería de Software I**: estructura de la vista de reporte (agrupación, filtros).

## Dificultades y aprendizajes

- El reporte del motor no incluye el campo de categoría (`tipo`) en la respuesta; el frontend agrupará por ese campo cuando se implemente (pendiente coordinar con Integrante 1 el contrato final).
- El contrato de la API (`POST /validar`) lo desarrolla el Integrante 1 en la rama `week2-api-contract`; los mockups usan datos de ejemplo que imitan la forma del JSON del motor.

## Plan de la semana siguiente

- Convertir los mockups a componentes React (Act. 2, S4–S5): componente de carga de archivo.
