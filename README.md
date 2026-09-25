# Taller de Optimización GraphQL: Patrón DataLoader y Problema N+1

**Asignatura:** Patrones de Diseño de APIs  
**Carrera:** Maestría de Software - Universidad Politécnica Salesiana  
**Periodo Lectivo:** 2026  

---

## Descripción del Proyecto

Este laboratorio demuestra la identificación y mitigación del problema de rendimiento **Consulta N+1** en entornos GraphQL mediante la implementación del patrón arquitectónico **DataLoader** (agrupamiento por lotes y almacenamiento en caché por petición).

El proyecto cuenta con dos servidores independientes ejecutándose en paralelo para comparar el rendimiento en tiempo real:
- **Puerto 4000:** Solución naive/ingenua que genera el problema $N+1$.
- **Puerto 4001:** Solución optimizada implementando DataLoader[cite: 1].

---

## Estructura del Repositorio

```text
├── database.js          # Base de datos simulada y funciones de consulta
├── schema.graphql       # Definición del esquema SDL
├── dataloaders.js       # Implementación de la función Batch con DataLoader
├── resolvers-naive.js   # Resolutores ingenuos (N+1)
├── resolvers.js         # Resolutores optimizados
├── server-naive.js      # Servidor en puerto 4000 (Problema N+1)
├── server-optimized.js  # Servidor en puerto 4001 (Optimizado)
├── package.json         # Configuración de scripts y dependencias
└── README.md            # Documentación del proyecto