# D-05 · Patrón BFF por canal

**Estado:** Propuesta (v1.0, 2026-09-25)  
**Sección del documento:** 5.2

## Contexto
Decisión tomada en el diseño de la arquitectura del Sistema de Banca por Internet de BP (modelo C4). El detalle completo, con el análisis de opciones y las consecuencias, se encuentra en la sección 5.2 del documento `Arquitectura_Banca_Internet_BP_C4.pdf`.

## Opciones evaluadas
- API única genérica
- gateway con lógica

## Decisión
Patrón BFF por canal.

## Justificaciones
1. Composición por canal sin contaminar dominios.
2. Seguridad diferenciada (Token Handler vs. DPoP).
3. Evolución independiente.

## Consecuencias
Ver la sección 5.2 del documento principal (riesgos asociados en la sección 17).
