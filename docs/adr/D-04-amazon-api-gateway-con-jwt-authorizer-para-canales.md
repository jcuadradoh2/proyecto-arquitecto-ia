# D-04 · Amazon API Gateway con JWT Authorizer para canales

**Estado:** Propuesta (v1.0, 2026-09-25)  
**Sección del documento:** 5.2

## Contexto
Decisión tomada en el diseño de la arquitectura del Sistema de Banca por Internet de BP (modelo C4). El detalle completo, con el análisis de opciones y las consecuencias, se encuentra en la sección 5.2 del documento `Arquitectura_Banca_Internet_BP_C4.pdf`.

## Opciones evaluadas
- Kong / Apigee / NGINX autogestionado

## Decisión
Amazon API Gateway con JWT Authorizer para canales.

## Justificaciones
1. Gestionado y elástico con WAF.
2. Autorización estándar en el borde.
3. Separación norte-sur / este-oeste.

## Consecuencias
Ver la sección 5.2 del documento principal (riesgos asociados en la sección 17).
