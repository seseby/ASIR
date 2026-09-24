---
modulo: M04 - Lenguajes de marcas y sistemas de gestión de información
concepto: XML - Fundamentos
categoria: Teoría / Estándar
relacion_sesiones:
  - "[[📄 S01 - XML]]"
tags:
  - ASIR
  - M04
  - Conceptos
  - XML
---

# 🧠 Concepto: XML - Fundamentos y Sintaxis

> [!info] 📌 DEFINICIÓN RÁPIDA
> **¿Qué es?** XML (*Extensible Markup Language*) es un metalenguaje de etiquetas desarrollado por el W3C que permite separar la información de estructura de los datos reales [11].
> **¿Para qué sirve?** Facilita el almacenamiento, transporte e intercambio de datos estructurados entre aplicaciones heterogéneas [11].

---

## 📐 Estructura y Componentes del Documento

### 1. Elementos y Etiquetas (TAGs)
- **Etiqueta (TAG):** Texto delimitado por los símbolos menor que (`<`) y mayor que (`>`). Existen etiquetas de inicio y etiquetas de fin [11].
- **Elemento:** Estructura completa formada por la etiqueta de inicio, la etiqueta de cierre y el contenido entre ambas [11].
- **Atributo:** Par `nombre="valor"` situado dentro de la etiqueta de inicio para especificar propiedades asociadas a los elementos [11].

### 2. Reglas de Nomenclatura para Elementos
1. Pueden contener letras, números y otros caracteres [12].
2. **No** pueden comenzar con números, caracteres de puntuación ni con la cadena `xml` / `XML` [12].
3. **No** pueden contener espacios [12].
4. Las etiquetas XML son **sensibles a mayúsculas y minúsculas** (*case-sensitive*) [12].

---

## 🔣 Caracteres Especiales y Secciones Especiales

### 1. Entidades Reservadas
En XML algunos símbolos son reservados del lenguaje. Para representarlos como texto dentro de un nodo se emplean códigos que inician con `&` y terminan con `;` [11, 12]:

| Carácter | Código de Escape | Nombre |
| :---: | :---: | :--- |
| `<` | `&lt;` | Less Than |
| `>` | `&gt;` | Greater Than |
| `&` | `&amp;` | Ampersand |
| `'` | `&apos;` | Apostrophe |
| `"` | `&quot;` | Quote |

### 2. Secciones CDATA y Comentarios
- **Secciones CDATA (`<![CDATA[ ... ]]>`):** Permiten marcar un texto para que no sea procesado por el *parser* (útil para incluir fragmentos de HTML u otro código) [13].
- **Comentarios:** Tienen la sintaxis `<!-- Comentario -->` y no son procesados por el *parser* [13].
- **Instrucciones de procesamiento:** Proporcionan órdenes específicas a las aplicaciones que procesan el XML [13].

---

## ❓ Preguntas de Autoevaluación (Active Recall)

> [!question] Test de Repaso
> 1. **¿Puede un elemento XML llamarse `<1er_estudiante>`?**
>    - *Respuesta:* No, porque los nombres de elementos no pueden empezar por un número.
> 2. **¿Para qué sirve una sección CDATA?**
>    - *Respuesta:* Para insertar texto con caracteres especiales (como etiquetas HTML) evitando que el *parser* XML devuelva un error.
> 3. **¿Cuál es la diferencia entre un elemento y un atributo?**
>    - *Respuesta:* El elemento define la estructura jerárquica con etiquetas de inicio y fin, mientras que el atributo es una propiedad par nombre-valor dentro de la etiqueta de inicio.
