

## 1. Revisión Inicial del Código HTML
- Verificamos errores en `index.html` usando herramientas de validación.
- Confirmamos que el HTML está correctamente enlazado con `styles.css` mediante `<link rel="stylesheet" href="styles.css">` en el `<head>`.
- Aseguramos que no hay errores de sintaxis que impidan la comunicación entre HTML y CSS.

## 2. Agregado de Campo de Edad (Primera Versión)
- Insertamos un nuevo campo `<input type="number">` para Edad entre los bloques "Asunto" y "Mensaje".
- Atributos: `min="15"`, `max="99"`, con etiqueta y ayuda.
- Ubicación: Después de `<!-- Asunto -->` y antes de `<!-- Mensaje -->`.

## 3. Modificación del Box-Shadow del Botón Principal
- Intensificamos el `box-shadow` de `.btn-primario` en `styles.css` para sombras negras expandidas
- Base: Múltiples capas de sombra negra con opacidad alta.
- Hover: Sombras aún más grandes y brutales para impacto visual.
- Propósito: Dar dramatismo y profundidad al botón.

## 4. Eliminación del Campo de Edad
- Removimos el campo de Edad agregado en el paso 2 para simplificar el formulario.

## 5. Agregado de Campo de Edad (Segunda Versión)
- Insertamos el campo de Edad en la fila doble (`fila-doble`) junto a Nombre y Correo Electrónico.
- Atributos: `type="number"`, `min="15"`, `max="99"`, con mensaje de ayuda.
- Ubicación: En la sección de Nombre y Email.


## 6. Documentación en README
- Agregamos explicaciones y procedimientos en este archivo `readme.md`.
- Incluimos ayuda sobre `box-shadow` y sintaxis CSS.

