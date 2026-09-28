# D-11 · Vista materializada por eventos para clientes frecuentes (DynamoDB + Redis)

**Estado:** Propuesta (v1.0, 2026-09-25)  
**Sección del documento:** 6.5

## Contexto
Decisión tomada en el diseño de la arquitectura del Sistema de Banca por Internet de BP (modelo C4). El detalle completo, con el análisis de opciones y las consecuencias, se encuentra en la sección 6.5 del documento `Arquitectura_Banca_Internet_BP_C4.pdf`.

## Opciones evaluadas
- Solo caché TTL
- réplica completa del Core

## Decisión
Vista materializada por eventos para clientes frecuentes (DynamoDB + Redis).

## Justificaciones
1. Rendimiento con consistencia acotada.
2. Menor carga y costo en el Core.
3. Minimización de datos.

## Consecuencias
Ver la sección 6.5 del documento principal (riesgos asociados en la sección 17).
