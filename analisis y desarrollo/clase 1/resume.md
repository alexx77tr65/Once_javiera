# Pilares del Análisis y Diseño de Software

## 1. La Importancia del Análisis y el Diseño
* **El problema:** El **66% de los proyectos fracasan** o fallan gravemente, principalmente por **requerimientos mal definidos**, no por errores de programación.
* **Análisis vs. Diseño:**
    * **Análisis:** Define el **QUÉ** se va a construir (problema, necesidades, restricciones).
    * **Diseño:** Define el **CÓMO** se va a construir (arquitectura, tecnologías, UX).
* **Regla del 1-10-100:** Corregir un error en *Análisis* cuesta $1, en *Diseño* $10, en *Programación* $100 y en *Producción* más de $1000.
* **Caso histórico:** En 1999, la NASA perdió la sonda *Mars Climate Orbiter* ($327M) por una incompatibilidad de unidades no detectada a tiempo.

---

## 2. El Ciclo de Vida del Software (SDLC)
El proceso actual es **cíclico** (el mantenimiento reactiva el análisis) y consta de 6 fases:
1. **Análisis de Requerimientos:** Documenta las necesidades del cliente.
2. **Diseño:** Crea los planos, bases de datos y arquitectura.
3. **Implementación:** Traducción del diseño a código (Java, Python, etc.).
4. **Pruebas:** Verificación de errores, seguridad e integridad.
5. **Despliegue:** Entrega y puesta en marcha en servidores reales.
6. **Mantenimiento:** Corrección de fallos diarios y nuevas funciones.

---

## 3. Metodologías Estructuradas (Tradicionales)
Son metodologías "pesadas", basadas en una planificación inicial exhaustiva. Ideales para **sistemas críticos** (hospitales, banca, aviación) con requerimientos estables.
* **Cascada:** Secuencial y lineal. No se avanza sin terminar la fase anterior. Rigió pero documenta todo.
* **Modelo en V:** Une cada fase de desarrollo con su respectiva fase de pruebas desde el inicio.
* **Modelo Espiral:** Enfocado en el análisis de riesgos a través de vueltas iterativas y evolutivas.

---

## 4. Metodologías Ágiles
Nacen del **Manifiesto Ágil (2001)**. Priorizan la flexibilidad, las personas y el software funcional sobre la burocracia. Trabajan en **iteraciones de 1 a 4 semanas**.
* **Scrum:** Trabaja en *Sprints*. Roles: *Product Owner* (QUÉ), *Scrum Master* (facilitador) y *Equipo Dev*. Eventos: Daily (15 min), Demo y Retrospectiva.
* **Kanban:** Tablero visual por columnas (Por hacer ➔ Haciendo ➔ Hecho). Su clave es **limitar el WIP** (Trabajo en Curso) para evitar cuellos de botella.
* **XP (Extreme Programming):** Foco en la excelencia técnica mediante programación en pares, **TDD** (testear antes de codificar) y refactorización.

---

### Tabla Comparativa de Enfoques

| Criterio | Metodologías Estructuradas | Metodologías Ágiles |
| :--- | :--- | :--- |
| **Planificación** | Inicial y total | Continua por iteraciones |
| **Cambios** | Difíciles y costosos | Bienvenidos en cualquier momento |
| **Documentación** | Extensa y formal | Mínima y necesaria |
| **Cliente** | Participa al inicio y al final | Participación constante |
| **Riesgo** | Alto si se detectan fallas tarde | Bajo, se detectan rápido |

---

## 5. Ingeniería de Requerimientos
Un requerimiento es una condición o restricción que el sistema debe cumplir.

### Tipos de Requerimientos
* **Funcionales (QUÉ):** Acciones concretas (ej. *Registrar usuario*, *Generar reporte*).
* **No Funcionales (CÓMO):** Atributos de calidad o restricciones (ej. *Cifrado de datos*, *Carga en < 3 segundos*).

### Cualidades SMART
Los requerimientos deben ser **S**pecific (Específicos), **M**easurable (Medibles), **A**chievable (Alcanzables), **R**elevant (Relevantes) y **T**ime-bound (Con plazo).
> **Mal ejemplo:** *"El sistema debe ser rápido y fácil de usar".*
> 
> **Buen ejemplo (SMART):** *"Un usuario nuevo debe poder registrarse en menos de 3 minutos sin cometer más de un error".*

* **Elicitación:** Técnicas para descubrir requerimientos (entrevistas, encuestas, observación, talleres y prototipos).
* **Gestión del Cambio:** Los requerimientos cambian casi siempre. El ingeniero no los rechaza, sino que evalúa su impacto en costo y tiempo para el cliente.