# 🛠️ Comandos: SQL
##### 📚 Módulo: [[00 - Índice]] | 🏷️ Etiquetas: #ASIR #Comandos #[[Módulo]]

---

> [!INFO] 📋 Descripción General
> Breve resumen de la herramienta, lenguaje o servicio (ej. *Linux CLI, MySQL, PowerShell, SSH*) y su función en la gestión de sistemas.

---

### ⚡ Tabla de Referencia Rápida

| Comando / Sintaxis | Parámetros Clave | Descripción | Ejemplo de Uso |
| :--- | :--- | :--- | :--- |
| `comando1` | `-a`, `-l` | Muestra todos los archivos detallados. | `ls -la /var/log` |
| `comando2` | `--help` | Muestra la ayuda y opciones. | `systemctl --help` |
| `comando3` | `-v` | Modo detallado (verbose). | `cp -v orig.txt dest.txt` |

---

### 💻 Casos de Uso & Flujos de Trabajo

#### 1. [Nombre del Proceso 1 - Ej: Comprobación de Estado]
```bash
# Verificar el estado del servicio
sudo systemctl status [nombre_servicio]

# Reiniciar el servicio si ha fallado
sudo systemctl restart [nombre_servicio]
```

#### 2. [Nombre del Proceso 2 - Ej: Edición de Configuración]
```bash
# Hacer copia de seguridad antes de editar
cp /etc/[archivo].conf /etc/[archivo].conf.bak

# Editar archivo
sudo nano /etc/[archivo].conf
```

---

> [!WARNING] ⚠️ Precauciones y Rutas Críticas
> - **Precaución:** Revisa siempre los parámetros antes de ejecutar comandos con `sudo` o modificadores destructivos.
> - **Rutas clave:** `/etc/` (configuración), `/var/log/` (registros de eventos).

---

### 🔗 Enlaces Relacionados
- **Sesión práctica:** [[Sesión XX - Práctica de Comandos]]
- **Hojas de comandos:** [[Comandos Linux]] | [[PowerShell]]