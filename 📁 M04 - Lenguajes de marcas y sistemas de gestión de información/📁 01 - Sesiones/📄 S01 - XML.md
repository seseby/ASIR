---
modulo: M04 - Lenguajes de marcas y sistemas de gestión de información
sesion: S01 - XML
fecha: 2026-09-24
estado: 🟢 Completado
tags:
  - ASIR
  - M04
  - XML
  - XPATH
  - XSLT
---

# 📚 S01 - XML: Definición, Estructura y Validación

> [!abstract] 📌 INFORMACIÓN DE LA SESIÓN
> - **Módulo:** M04 - Lenguajes de marcas y sistemas de gestión de información
> - **Unidad / Bloque:** S01 XML (Empezando y Profundizando en XML)
> - **Objetivo:** Comprender la sintaxis de XML, reglas de nomenclatura, manejo de caracteres especiales, validación con XML Schema, transformaciones XSLT y consultas XPATH.

---

## 🎯 ¿Qué debería saber al terminar esta sesión?
- [ ] Definir qué es un metalenguaje de marcas y la función principal de XML.
- [ ] Diferenciar entre etiqueta (*tag*), elemento y atributo.
- [ ] Aplicar correctamente las reglas de nomenclatura para elementos XML.
- [ ] Utilizar caracteres de escape (entidades) y bloques CDATA.
- [ ] Estructurar y validar documentos mediante XML Schema (XSD).
- [ ] Realizar consultas jerárquicas con XPATH y transformaciones con XSLT.

---

## 🗺️ Hoja de Ruta de la Sesión

### 🔹 S01-C01: Empezando con XML
- [x] **V01:** Definición y Clasificación de XML
- [ ] **V02:** Mi primer XML (Estructura y sintaxis)
- [ ] **V03:** Verificación de Documentos XML
- [ ] **V04:** Cómo Estructurar Documentos XML
- [ ] **V05:** XML Schema (Parte I)
- [ ] **V06:** XML Schema (Parte II)
- [ ] **V07:** XML Schema (Parte III)
- [ ] **V08:** Introducción a XSLT
- [ ] **V09:** Utilizando XSLT
- [ ] **S01-C01 Ejercicios**

### 🔹 S01-C02: Profundizando en XML
- [ ] **V01:** Introducción Almacenamiento e Integración de XML
- [ ] **V02:** XPATH Primeros Pasos
- [ ] **V03:** Expresiones XPATH Parte I
- [ ] **V04:** Expresiones XPATH Parte II
- [ ] **V05:** Expresiones XPATH Parte III
- [ ] **S01-C02 Ejercicios**
- [ ] **Actividad de evaluación continua S01**

---

## 🧠 Resumen de la Sesión

> [!note] Puntos clave aprendidos
> 1. **Definición:** XML es un metalenguaje de etiquetas desarrollado por el W3C para almacenar e intercambiar información, separando la estructura de los datos [11, 12].
> 2. **Sintaxis estricta:** Requiere etiquetas de inicio/cierre, sensibilidad a mayúsculas/minúsculas y el uso de entidades de escape para caracteres reservados (`&lt;`, `&gt;`, `&amp;`) [11, 12].
> 3. **Estructuras avanzadas:** Se emplean secciones CDATA para incluir texto no procesable por el *parser* y esquemas XSD / XPATH para validación y consulta de datos [12, 13].

---

## 🔑 Conceptos Clave (Conexión con `📁 02 - Conceptos`)

| Concepto | Enlace en Bóveda | ¿Qué es? / Descripción | Aplicación práctica |
| :--- | :--- | :--- | :--- |
| **Metalenguaje XML** | [[XML - Fundamentos]] | Lenguaje de marcas del W3C para estructuración de datos. | Almacenamiento e intercambio de información. |
| **Etiquetas y Atributos** | [[XML - Fundamentos]] | Componentes para definir marcas y propiedades pares nombre-valor. | Organización de nodos en el documento. |
| **Secciones CDATA** | [[XML - Fundamentos]] | Bloque de texto omitido por el *parser* XML. | Inserción de código HTML u otros lenguajes. |
| **XML Schema (XSD)** | [[Validación y almacenamiento XML]] | Esquema de validación estricta de estructura y tipos. | Control de calidad e integridad de datos. |

---

## 💻 Sintaxis y Comandos (Conexión con `📁 03 - Comandos y sintaxis`)

> [!example] Ficha de Referencia
> Ver la guía completa de sintaxis en `📁 03 - Comandos y sintaxis/XML.md`.

```xml
<?xml version="1.0" encoding="UTF-8"?>
<student nif="3636542X">
    <nombre>Juan Pablo</nombre>
    <!-- Comentario en XML -->
    <codigo><![CDATA[<html><body><h3>Titulo</h3></body></html>]]></codigo>
</student>
```

---

## 📝 Notas de Trabajo y Ejercicios
- **Ejercicio S01-C01:** Creación de un XML bien formado con atributos `nif` y nodos anidados.
- **Ejercicio S01-C02:** Consultas de nodos mediante XPATH.
