# ESPECIFICACIÓN DE REQUERIMIENTOS DE SOFTWARE (SRS)

**Proyecto:** Sistema de Gestión de Biblioteca Escolar (SGBE)  


---

## 1. Introducción

### 1.1 Propósito
Este documento define los requerimientos funcionales y no funcionales del Sistema de Gestión de Biblioteca Escolar (SGBE). Su objetivo es servir de guía única para el equipo de desarrollo, los testers, las directivas del Colegio San Antonio y el personal de bibliotecarios, reemplazando el control manual en cuadernos.

### 1.2 Alcance
El sistema automatizará el catálogo de libros, préstamos, devoluciones y reservas mediante una plataforma web y una aplicación móvil. Queda fuera del alcance la gestión de compras de libros, inventario de mobiliario y contabilidad general de la institución.

### 1.3 Definiciones y Acrónimos
* **SGBE:** Sistema de Gestión de Biblioteca Escolar.
* **RF:** Requerimiento Funcional.
* **RNF:** Requerimiento No Funcional.
* **CU:** Caso de Uso.
* **Reserva:** Apartado preventivo de un texto disponible para su posterior retiro.

### 1.4 Referencias
* Reglamento interno de la biblioteca del Colegio San Antonio (2025).
* Estándar IEEE 830-1998 para la estructuración de SRS.
* Ley 1581 de 2012 (Protección de Datos Personales en Colombia).

---

## 2. Descripción General

### 2.1 Perspectiva del Producto
El SGBE es un software independiente que se integrará con el sistema académico central del colegio mediante servicios web para la validación y autenticación de la identidad de la comunidad educativa.

### 2.2 Funciones del Producto
* Control y actualización del catálogo bibliográfico.
* Registro digitalizado de préstamos y devoluciones.
* Módulo de reservas web y móviles para estudiantes y docentes.
* Alertas y notificaciones automáticas de vencimiento.
* Motor de reportes de uso y analítica de textos.

### 2.3 Características de los Usuarios
* **Estudiantes (800):** Acceso a consultas y reservas vía app móvil. Nivel técnico básico.
* **Profesores (40):** Acceso a consultas, reservas y extensiones de tiempo. Nivel técnico medio.
* **Bibliotecarios (3):** Administradores diarios de la plataforma de escritorio. Nivel técnico medio con capacitación previa.

### 2.4 Restricciones
* **Presupuesto:** Límite estricto de 15 millones de pesos colombianos.
* **Tiempo:** Plazo de ejecución e implementación de 4 meses.
* **Cumplimiento legal:** Cifrado y manejo de datos bajo la Ley Estatutaria de Habeas Data.

### 2.5 Suposiciones y Dependencias
* Se asume que la institución garantizará una conectividad a internet estable.
* El sistema académico actual mantendrá activas y estables las API de consulta de usuarios.

---

## 3. Requisitos Específicos

### 3.1 Requerimientos Funcionales (RF)
* **RF-001:** El sistema deberá permitir a los usuarios buscar libros por título, autor o categoría.
* **RF-002:** El sistema deberá permitir reservar un libro disponible por un tiempo máximo de 72 horas.
* **RF-003:** El sistema deberá registrar los préstamos asociando el código del libro, el ID del usuario y las fechas límite.
* **RF-004:** El sistema deberá despachar un correo recordatorio automáticamente 24 horas antes del vencimiento del préstamo.
* **RF-005:** El sistema deberá generar un reporte mensual con los 20 libros más solicitados.

### 3.2 Requerimientos No Funcionales (RNF)
* **RNF-001 (Rendimiento):** El tiempo de respuesta en las búsquedas del catálogo no debe superar los 2 segundos para el 95% de las peticiones.
* **RNF-002 (Disponibilidad):** La plataforma debe asegurar una disponibilidad del 99% en la jornada escolar (7:00 a.m. a 5:00 p.m.).
* **RNF-003 (Seguridad):** Las contraseñas de los usuarios se almacenarán en la base de datos cifradas mediante el algoritmo bcrypt con un factor de trabajo de 12.
* **RNF-004 (Escalabilidad):** El sistema debe soportar una carga concurrente de 100 usuarios activos sin experimentar degradación del servicio.

### 3.3 Interfaces Externas
* **Sistema Académico:** Conexión mediante API REST para verificar el estado de matrícula de los alumnos.
* **Notificaciones:** Integración con servidor SMTP institucional para la salida de correos electrónicos.
* **App Móvil:** Comunicación HTTPS segura basada en tokens JWT para transacciones de datos.

---

## 4. Apéndices
* **Anexo A:** Especificación detallada de Casos de Uso (CU-001 a CU-015).
* **Anexo B:** Diagramas de Casos de Uso en notación UML.
* **Anexo C:** Prototipos y maquetas de interfaz de usuario de las pantallas críticas.