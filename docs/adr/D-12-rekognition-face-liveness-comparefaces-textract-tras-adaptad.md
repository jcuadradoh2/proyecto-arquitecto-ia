# D-12 · Rekognition Face Liveness + CompareFaces + Textract tras adaptador; Facephi / Incode como alternativas

**Estado:** Propuesta (v1.0, 2026-09-25)  
**Sección del documento:** 9

## Contexto
Decisión tomada en el diseño de la arquitectura del Sistema de Banca por Internet de BP (modelo C4). El detalle completo, con el análisis de opciones y las consecuencias, se encuentra en la sección 9 del documento `Arquitectura_Banca_Internet_BP_C4.pdf`.

## Opciones evaluadas
- Facephi
- Incode
- Jumio / Onfido / Veriff
- iProov

## Decisión
Rekognition Face Liveness + CompareFaces + Textract tras adaptador; Facephi / Incode como alternativas.

## Justificaciones
1. Integración y soberanía de datos en la misma región.
2. Costo por uso.
3. Riesgo de proveedor mitigado con Strategy / Adapter.

## Consecuencias
Ver la sección 9 del documento principal (riesgos asociados en la sección 17).
