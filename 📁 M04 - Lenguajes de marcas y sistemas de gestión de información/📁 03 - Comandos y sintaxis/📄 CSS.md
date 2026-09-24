
# 💻 Guía de Sintaxis y Comandos: {{title}}

&gt; [!example] 📌 PROPÓSITO DE LA GUÍA
&gt; **Tecnología / Herramienta:** {{title}}
&gt; **Uso principal:** Referencia rápida de reglas de código, estructuras válidas, fragmentos (*snippets*) y comandos de validación o ejecución.

---

## 🚀 Índice de Referencia Rápida
1. [[#1. Reglas Estructurales y Sintaxis Básica]]
2. [[#2. Tipos de Datos y Validaciones]]
3. [[#3. Consultas y Expresiones]]
4. [[#4. Transformación y Procesamiento]]
5. [[#5. Errores Comunes y Buenas Prácticas]]

---

## 1. Reglas Estructurales y Sintaxis Básica

&gt; [!tip] Reglas indispensables
&gt; Resumen de los requisitos sintácticos universales para evitar errores de sintaxis o ejecución.

```{{title_lowercase}}


````

---

## **2. Tipos de Datos y Validaciones**

Explicación de reglas de validación o parámetros principales.

|Elemento / Estructura|Sintaxis / Parámetro|Descripción / Valor permitido|
|---|---|---|
|**Elemento A**|`sintaxis_a`|Descripción corta|
|**Elemento B**|`sintaxis_b`|Descripción corta|

---

## **3. Consultas y Expresiones**

```
// Expresiones de búsqueda o comandos de consulta

```

---

## **4. Transformación y Procesamiento**

---

## **⚠️ 5. Errores Comunes y Buenas Prácticas**

> [!warning] Errores sintácticos típicos

- ❌ **Incorrecto:**
- ✅ **Correcto:**

---

## **🔗 Enlaces de la Bóveda**

- **Sesión principal:** [[S01 - XML]]
- **Conceptos teóricos:**
    - [[XML]]
    - [[XML Schema]]
    - [[XPATH]]
    - [[XSLT]]

````

---

### 📝 Ejemplo Completo Aplicado: `📁 03 - Comandos y sintaxis/XML.md`

Aquí tienes la guía lista para usar con todo el contenido técnico de **XML, Schema (XSD), XPATH y XSLT** correspondiente a la primera sesión del módulo:

```markdown
---
modulo: M04 - Lenguajes de marcas y sistemas de gestión de información
tecnologia: XML
categoria: Sintaxis y Comandos
relacion_sesiones:
  - "[[S01 - XML]]"
tags:
  - ASIR
  - M04
  - XML
  - XSD
  - XPATH
  - XSLT
---

# 💻 Guía de Sintaxis y Comandos: XML, XSD, XPATH y XSLT

&gt; [!example] 📌 PROPÓSITO DE LA GUÍA
&gt; **Tecnología:** XML y herramientas asociadas (XSD, XPATH, XSLT).
&gt; **Uso principal:** Hoja de consulta rápida con ejemplos prácticos reutilizables para ejercicios de clase, validación de documentos y evaluaciones.

---

## 1. Sintaxis Básica de XML

```xml




````

---

## **2. Esquemas de Validación (XML Schema / XSD)**

### **📄 Ejemplo de Archivo `.xsd`**

---

## **3. Expresiones XPATH**

|Operador / Expresión|Descripción|Ejemplo de Sintaxis|
|---|---|---|
|`/`|Selección desde el nodo raíz|`/modulo/nombre`|
|`//`|Selección en cualquier nivel del documento|`//unidad`|
|`@`|Selección de atributos|`//unidad/@id`|
|`[]`|Predicado / Filtro condicional|`//unidad[@estado='activa']`|
|`text()`|Extrae el valor de texto del nodo|`//titulo/text()`|
|`count()`|Cuenta el número de nodos seleccionados|`count(//unidad)`|
|`contains()`|Comprueba si un texto contiene una cadena|`//unidad[contains(titulo, 'XML')]`|

### **🛠️ Ejemplos Prácticos de XPATH**

```
# Obtener los títulos de las unidades cuya ID sea mayor que 1
/modulo/unidad[@id &gt; 1]/titulo

# Seleccionar el último elemento unidad del documento
/modulo/unidad[last()]

```

---

## **4. Plantilla de Transformación XSLT**

---

## **⚠️ 5. Errores Comunes y Buenas Prácticas**

> [!warning] Puntos clave a revisar en exámenes y ejercicios

- ❌ **Sensibilidad a mayúsculas:** `` dará error. Las etiquetas deben coincidir exactamente.
- ❌ **Atributos sin comillas:** `