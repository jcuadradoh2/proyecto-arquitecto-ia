# D-14 · Aurora PostgreSQL + DynamoDB + ElastiCache Redis

**Estado:** Propuesta (v1.0, 2026-09-25)  
**Sección del documento:** 10

## Contexto
Decisión tomada en el diseño de la arquitectura del Sistema de Banca por Internet de BP (modelo C4). El detalle completo, con el análisis de opciones y las consecuencias, se encuentra en la sección 10 del documento `Arquitectura_Banca_Internet_BP_C4.pdf`.

## Opciones evaluadas
- RDS MySQL / Oracle
- Cassandra / DocumentDB
- Memcached

## Decisión
Aurora PostgreSQL + DynamoDB + ElastiCache Redis.

## Justificaciones
1. Ajuste al patrón de acceso (polyglot persistence).
2. HA y DR gestionadas multi-región.
3. Estándares abiertos sin licencias.

## Consecuencias
Ver la sección 10 del documento principal (riesgos asociados en la sección 17).
