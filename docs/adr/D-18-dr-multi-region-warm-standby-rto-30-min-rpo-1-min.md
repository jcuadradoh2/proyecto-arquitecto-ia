# D-18 · DR multi-región warm standby (RTO ≤ 30 min, RPO ≤ 1 min)

**Estado:** Propuesta (v1.0, 2026-09-25)  
**Sección del documento:** 12

## Contexto
Decisión tomada en el diseño de la arquitectura del Sistema de Banca por Internet de BP (modelo C4). El detalle completo, con el análisis de opciones y las consecuencias, se encuentra en la sección 12 del documento `Arquitectura_Banca_Internet_BP_C4.pdf`.

## Opciones evaluadas
- Backup & restore
- pilot light
- activo-activo

## Decisión
DR multi-región warm standby (RTO ≤ 30 min, RPO ≤ 1 min).

## Justificaciones
1. Objetivos alineados con la norma.
2. Costo proporcionado (15–20 %).
3. Verificable con IaC y pruebas trimestrales.

## Consecuencias
Ver la sección 12 del documento principal (riesgos asociados en la sección 17).
