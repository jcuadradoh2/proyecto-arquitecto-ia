# D-13 · Kong + conectores ACL para integración

**Estado:** Propuesta (v1.0, 2026-09-25)  
**Sección del documento:** 10

## Contexto
Decisión tomada en el diseño de la arquitectura del Sistema de Banca por Internet de BP (modelo C4). El detalle completo, con el análisis de opciones y las consecuencias, se encuentra en la sección 10 del documento `Arquitectura_Banca_Internet_BP_C4.pdf`.

## Opciones evaluadas
- Amazon API Gateway privado
- MuleSoft / WSO2
- llamadas directas

## Decisión
Kong + conectores ACL para integración.

## Justificaciones
1. ACL protege el dominio del legado.
2. Capacidades este-oeste (mTLS, SOAP, caché).
3. Costo y apertura frente a un ESB.

## Consecuencias
Ver la sección 10 del documento principal (riesgos asociados en la sección 17).
