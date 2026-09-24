---
modulo: M04 - Lenguajes de marcas y sistemas de gestión de información
tecnologia: XML
categoria: Sintaxis y Comandos
relacion_sesiones:
  - "[[📄 S01 - XML]]"
tags:
  - ASIR
  - M04
  - Sintaxis
  - XML
---

# 💻 Guía de Sintaxis y Comandos: XML

> [!example] 📌 PROPÓSITO
> Hoja de consulta rápida con la sintaxis exacta de elementos, atributos, entidades reservadas y bloques CDATA.

---

## 1. Estructura Básica con Atributos

```xml
<?xml version="1.0" encoding="UTF-8"?>
<!-- Documento de ejemplo con elementos y atributos -->
<estudiantes>
    <student nif="3636542X">
        <nombre>Juan Pablo</nombre>
        <telefono>670253697</telefono>
    </student>
    <student nif="48572199Y">
        <nombre>Leonor Andres Sanahuja</nombre>
    </student>
</estudiantes>
```

---

## 2. Tabla de Caracteres Especiales (Entidades)

```xml
<!-- Ejemplo de uso de entidades dentro de un elemento -->
<notacion>
    Si 5 &lt; 10 y 10 &gt; 3, entonces "A &amp; B" es correcto.
</notacion>
```

| Código | Resultado | Uso |
| :--- | :---: | :--- |
| `&lt;` | `<` | Reemplaza al símbolo menor que. |
| `&gt;` | `>` | Reemplaza al símbolo mayor que. |
| `&amp;` | `&` | Reemplaza al ampersand. |
| `&apos;` | `'` | Reemplaza al apóstrofe. |
| `&quot;` | `"` | Reemplaza a las comillas dobles. |

---

## 3. Comentarios y Secciones CDATA

```xml
<!-- Sintaxis de Comentarios -->
<!-- Este es un comentario en XML y no es procesado por el parser -->

<!-- Sintaxis de CDATA -->
<codigo>
    <![CDATA[<html><body><h3>Titulo</h3></body></html>]]>
</codigo>
```

---

## ⚠️ 4. Errores Comunes de Sintaxis

> [!warning] Lista de Verificación Rápida
> - ❌ **Error en nombres:** `<xml_nodo>` o `<1nodo>` (No pueden empezar por "xml" ni por número).
> - ❌ **Sensible a mayúsculas:** `<Student>Juan</student>` (Error: Las etiquetas de inicio y cierre deben coincidir exactas).
> - ❌ **Atributos no entrecomillados:** `<student nif=3636542X>` (Error: Los atributos deben ir entre comillas dobles o simples).
> - ❌ **Símbolo `<` sin escapar:** `<formula>5 < 10</formula>` (Error: Debe escribirse `5 &lt; 10`).

---

## 🔗 Enlaces de la Bóveda
- **Sesión principal:** [[📄 S01 - XML]]
- **Concepto teórico:** [[📁 ASIR/📁 M04 - Lenguajes de marcas y sistemas de gestión de información/📁 02 - Conceptos/📄 XML|📄 XML]]
