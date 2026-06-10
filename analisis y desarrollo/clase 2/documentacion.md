# Resumen Rapido: Ingenieria de Requerimientos

## 1. Definicion Formal (IEEE 830)
Un requerimiento es una propiedad documentada y una declaracion verificable que un sistema debe poseer para resolver un problema o lograr un objetivo.
* **Regla de oro:** Si no se puede escribir ni comprobar, NO es un requerimiento.

## 2. Niveles de Abstraccion
* **Nivel 3 (Especificacion Tecnica):** Orientado al programador (Ej: "La API /menu debe retornar un JSON en < 300ms").
* **Nivel 2 (Requerimiento del Sistema):** Orientado al analista (Ej: "El sistema mostrara el menu a usuarios autenticados").
* **Nivel 1 (Necesidad del Usuario):** Orientado al cliente (Ej: "Quiero ver que hay de comida para no perder el viaje").
* **Rol del analista:** Traducir hacia arriba (convertir el Nivel 1 en los Niveles 2 y 3).

## 3. Fuentes de Requerimientos (Stakeholders)
* **Usuarios finales:** Operan el sistema dia a dia.
* **Clientes / Patrocinadores:** Financian y definen los objetivos de negocio.
* **Leyes y normas:** Regulaciones obligatorias (proteccion de datos, accesibilidad).
* **Sistemas externos:** Software con el que se debe integrar (pasarelas de pago, correos).

## 4. Las 7 Cualidades de un Buen Requerimiento
1. **Necesario:** Esencial para el proposito del sistema.
2. **No ambiguo:** Una sola interpretacion posible.
3. **Verificable:** Se puede probar objetivamente si se cumple o no.
4. **Consistente:** No contradice a otros requerimientos.
5. **Completo:** Contiene toda la informacion necesaria.
6. **Atomico:** Una sola idea por enunciado.
7. **Trazable:** Se conoce su origen y su impacto.

## 5. Requerimientos Funcionales (RF) vs No Funcionales (RNF)

### Requerimientos Funcionales (El QUÉ hace)
Definen acciones concretas, tareas, calculos y flujos ante entradas especificas.
* **Identificacion:** Verbos de accion (registrar, mostrar, calcular), roles, entradas y salidas.
* **Plantilla:** El sistema debera [verbo] + [objeto] + [condicion].
* **Categorias:** Autenticacion, calculo, persistencia (CRUD), comunicacion, reportes y validacion.

### Requerimientos No Funcionales (El CÓMO lo hace)
Definen caracteristicas de calidad, restricciones globales y propiedades del sistema.
* **Regla de oro:** Deben ser medibles cuantitativamente (definir metrica, umbral y validacion).
* **Categorias:** Rendimiento, seguridad, usabilidad, confiabilidad, escalabilidad, mantenibilidad, portabilidad y legales.

## 6. Atributos de Calidad (ISO/IEC 25010)
Son los conceptos abstractos generales que definen la excelencia del software. Los RNF son la bajada medible de estos atributos.

Los 8 atributos principales son:
1. Adecuacion funcional
2. Eficiencia de desempeno
3. Compatibilidad
4. Usabilidad
5. Confiabilidad
6. Seguridad
7. Mantenibilidad
8. Portabilidad

---

## 7. Resolucion de Caso: "SchoolEats"

### Paso 1: Stakeholders
Estudiantes, cocineros, rector/administracion y padres de familia.

### Paso 2: Elicitacion
* Estudiantes y Padres: Encuesta digital (poblaciones masivas/dispersas).
* Cocineros: Observacion directa + Entrevista (flujo operativo, grupo pequeno).
* Rector: Entrevista estructurada uno a uno (tomador de decisiones).

### Paso 3: Necesidades principales
Visualizacion de menu, reserva de platos, pagos digitales, control de porciones para cocina, reportes mensuales y alta disponibilidad.

### Paso 4: Clasificacion de Requerimientos
* "Mostrar el menu a estudiantes autenticados" -> **Funcional**
* "Permitir reservar y pagar con saldo" -> **Funcional**
* "Disponibilidad minima del 99.5% en horario escolar" -> **No Funcional**
* "Funcionar en iOS, Android y web" -> **No Funcional**
* "Generar reportes mensuales en PDF" -> **Funcional**
* "Tiempo de respuesta menor a 2 segundos" -> **No Funcional**

### Paso 5: Atributos de Calidad Criticos
1. **Usabilidad:** Clave para agilizar las filas en periodos cortos de tiempo.
2. **Confiabilidad:** El sistema no puede caerse en la hora pico del almuerzo.
3. **Seguridad:** Manejo de dinero real (saldos), transacciones y datos de menores.