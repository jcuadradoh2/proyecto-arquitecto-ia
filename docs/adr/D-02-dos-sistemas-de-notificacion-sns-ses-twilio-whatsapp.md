# D-02 · Dos sistemas de notificación: SNS/SES + Twilio/WhatsApp

**Estado:** Propuesta (v1.0, 2026-09-25)  
**Sección del documento:** 4

## Contexto
Decisión tomada en el diseño de la arquitectura del Sistema de Banca por Internet de BP (modelo C4). El detalle completo, con el análisis de opciones y las consecuencias, se encuentra en la sección 4 del documento `Arquitectura_Banca_Internet_BP_C4.pdf`.

## Opciones evaluadas
- Solo AWS
- solo Twilio + SendGrid
- Pinpoint
- pasarela local + SMTP

## Decisión
Dos sistemas de notificación: SNS/SES + Twilio/WhatsApp.

## Justificaciones
1. Independencia de proveedores (mandato normativo).
2. Cobertura de canales y evidencia de entrega.
3. Alternativas con menor foco transaccional.

## Consecuencias
Ver la sección 4 del documento principal (riesgos asociados en la sección 17).
