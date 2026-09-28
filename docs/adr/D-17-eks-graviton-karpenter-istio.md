# D-17 · EKS + Graviton + Karpenter + Istio

**Estado:** Propuesta (v1.0, 2026-09-25)  
**Sección del documento:** 12

## Contexto
Decisión tomada en el diseño de la arquitectura del Sistema de Banca por Internet de BP (modelo C4). El detalle completo, con el análisis de opciones y las consecuencias, se encuentra en la sección 12 del documento `Arquitectura_Banca_Internet_BP_C4.pdf`.

## Opciones evaluadas
- ECS / Fargate
- Linkerd
- App Mesh

## Decisión
EKS + Graviton + Karpenter + Istio.

## Justificaciones
1. Ecosistema abierto para auto-healing y GitOps.
2. Costo-rendimiento.
3. Malla madura con políticas L7.

## Consecuencias
Ver la sección 12 del documento principal (riesgos asociados en la sección 17).
