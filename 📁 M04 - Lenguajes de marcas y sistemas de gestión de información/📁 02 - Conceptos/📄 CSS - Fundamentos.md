
# 🧠 Concepto: {{title}}

 📌 DEFINICIÓN RÁPIDA
 **¿Qué es?** Escribe aquí una definición clara y concisa en 1-2 frases.
**¿Para qué sirve?** Explicación del caso de uso principal en administración de sistemas o desarrollo web.

---
## 📐 Contexto y Arquitectura

Explicación detallada del concepto. Puedes estructurarlo en los siguientes apartados:

### 1. Principios Fundamentales
- Punto clave 1.
- Punto clave 2.

### 2. Estructura y Funcionamiento
&gt; [!note] Explicación técnica
&gt; Describe el funcionamiento interno, reglas de sintaxis o flujo de datos.

---

## 📊 Comparativa / Reglas Teóricas

| Aspecto | Opción / Estándar A | Opción / Estándar B |
| :--- | :--- | :--- |
| **Definición** | | |
| **Ventajas** | | |
| **Casos de uso** | | |

---

## 🔗 Relaciones dentro de la Bóveda

- **Sesión asociada:** [[S01 - XML]]
- **Guía práctica / Sintaxis:** [[XML]] (en `03 - Comandos y sintaxis`)
- **Conceptos relacionados:**
  - [[XML Schema]]
  - [[XPATH]]
  - [[XSLT]]

---

## ❓ Preguntas de Autoevaluación (Active Recall)

&gt; [!question] Test rápido de repaso
&gt; 1. **¿Diferencia principal entre...?**
&gt;    - *Respuesta:*
&gt; 2. **¿Cuándo se debe utilizar...?**
&gt;    - *Respuesta:*

```

---

### **📝 Ejemplo de Aplicación Práctica: `📁 02 - Conceptos/Validación y almacenamiento XML.md`**

Así quedaría una ficha completa sobre **Validación y almacenamiento XML** (uno de los temas teóricos de la asignatura)[2][3]:

```
---
modulo: M04 - Lenguajes de marcas y sistemas de gestión de información
concepto: Validación y almacenamiento XML
categoria: Estándar / Arquitectura
relacion_sesiones:
  - "[[S01 - XML]]"
tags:
  - ASIR
  - M04
  - XML
  - Schema
  - XSD
---

# 🧠 Concepto: Validación y almacenamiento XML

&gt; [!info] 📌 DEFINICIÓN RÁPIDA
&gt; **¿Qué es?** Mecanismo para comprobar que un documento XML cumple con una estructura y tipos de datos prefijados (XML Schema/XSD), permitiendo además su persistencia en bases de datos relacionales o nativas XML [3].
&gt; **¿Para qué sirve?** Garantiza la integridad de los datos intercambiados entre sistemas informáticos antes de ser procesados o almacenados.

---

## 📐 Contexto y Arquitectura

### 1. Documento Bien Formado vs. Documento Válido
- **Bien formado:** Cumple las reglas sintácticas universales de XML (etiqueta raíz única, etiquetas de cierre correctas, atributos entre comillas).
- **Válido:** Además de estar bien formado, cumple con las reglas de estructura, elementos requeridos y tipos de datos definidos en un **DTD** o **XML Schema (XSD)**.

### 2. XML Schema (XSD)
&gt; [!note] Estándar W3C
&gt; XSD es el estándar moderno basado en propia sintaxis XML que permite definir restricciones estrictas (tipos enteros, cadenas, expresiones regulares, ocurrencias `minOccurs` / `maxOccurs`).

---

## 📊 Comparativa: Formas de Almacenamiento

| Criterio | Almacenamiento Relacional (SQL) | Base de Datos Nativa XML |
| :--- | :--- | :--- |
| **Estructura** | Tablas, filas y columnas (mapeo ORM). | Documentos jerárquicos en árbol. |
| **Tecnología** | MySQL, PostgreSQL (`CLOB` / columna `XML`). | BaseX, ExistDB. |
| **Consulta** | SQL / SQL con extensiones XML. | XPATH / XQUERY. |

---

## 🔗 Relaciones dentro de la Bóveda

- **Sesión asociada:** [[S01 - XML]]
- **Guía de Sintaxis:** [[XML]] *(en `📁 03 - Comandos y sintaxis/`)*
- **Conceptos relacionados:** [[XML]], [[XPATH]], [[XSLT]]

---

## ❓ Preguntas de Autoevaluación (Active Recall)

&gt; [!question] Test rápido de repaso
&gt; 1. **¿Qué ocurre si un XML no tiene etiqueta raíz única?**
&gt;    - *Respuesta:* No estará bien formado y cualquier analizador (parser) devolverá un error fatal.
&gt; 2. **¿Por qué se prefiere XSD frente a DTD?**
&gt;    - *Respuesta:* Porque XSD usa sintaxis XML, soporta tipos de datos avanzados y admite espacios de nombres (*namespaces*).

```

---

### **💡 Características clave de esta plantilla**

1. **Metadatos Frontmatter:** Permiten organizar las notas por etiquetas (`tags`) y relaciones de sesiones dentro de Obsidian[1].
2. **Llamadas tipo Callout de Obsidian:** Estilos como `&gt; [!info]`, `&gt; [!note]` y `&gt; [!question]` destacan visualmente tanto en la aplicación de escritorio como al renderizarse en GitHub[4].
3. **Sección de Active Recall:** Integra preguntas de repaso para afianzar el aprendizaje activo durante el estudio[4].