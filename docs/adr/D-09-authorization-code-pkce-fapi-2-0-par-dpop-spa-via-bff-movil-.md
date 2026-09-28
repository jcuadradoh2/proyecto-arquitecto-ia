# D-09 · Authorization Code + PKCE (FAPI 2.0, PAR, DPoP); SPA vía BFF; móvil con AppAuth

**Estado:** Propuesta (v1.0, 2026-09-25)  
**Sección del documento:** 8

## Contexto
Decisión tomada en el diseño de la arquitectura del Sistema de Banca por Internet de BP (modelo C4). El detalle completo, con el análisis de opciones y las consecuencias, se encuentra en la sección 8 del documento `Arquitectura_Banca_Internet_BP_C4.pdf`.

## Opciones evaluadas
- Implicit
- ROPC
- Code sin PKCE
- Hybrid

## Decisión
Authorization Code + PKCE (FAPI 2.0, PAR, DPoP); SPA vía BFF; móvil con AppAuth.

## Justificaciones
1. Alineación con RFC 9700 / 8252 / OAuth 2.1.
2. Tokens fuera del navegador y ligados al dispositivo.
3. Exigencias del sector financiero (FAPI).

## Consecuencias
Ver la sección 8 del documento principal (riesgos asociados en la sección 17).
