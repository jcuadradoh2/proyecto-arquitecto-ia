# D-01 · Microservicios en contenedores con orientación a eventos

**Estado:** Propuesta (v1.0, 2026-09-25)  
**Sección del documento:** 3

## Contexto
Decisión tomada en el diseño de la arquitectura del Sistema de Banca por Internet de BP (modelo C4). El detalle completo, con el análisis de opciones y las consecuencias, se encuentra en la sección 3 del documento `Arquitectura_Banca_Internet_BP_C4.pdf`.

## Opciones evaluadas
- Monolito modular
- microservicios en EKS
- serverless puro

## Decisión
Microservicios en contenedores con orientación a eventos.

## Justificaciones
1. Aislamiento y escalado independiente de consultas vs. transacciones.
2. Reutilización por canales.
3. Madurez operativa y portabilidad de Kubernetes.

## Consecuencias
Ver la sección 3 del documento principal (riesgos asociados en la sección 17).
