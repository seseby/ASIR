# Laboratorio de redes en Linux: subnetting, router y captura de tráfico

Laboratorio práctico con máquinas virtuales Ubuntu en el que se configura una red desde cero por terminal: direccionamiento estático con Netplan, división de un bloque `/23` en dos subredes, un router Linux que conecta ambas y verificación del resultado con `ping`, `tcpdump` y `mtr`.

Hecho durante el ciclo de ASIR. Todo está documentado con capturas reales del laboratorio.

## Qué se ha construido

Tres máquinas Ubuntu repartidas en dos redes internas. PC2 hace de router entre ellas y solo PC3 tiene salida a Internet.

```
   Internet
      │ (NAT, DHCP)
┌─────┴──────────────────────────┐
│ PC3  ens37: 10.16.209.2/24     │
│      ruta: 10.16.208.0/24      │
│            vía 10.16.209.1     │
└─────┬──────────────────────────┘
      │  Red interna 2 · 10.16.209.0/24
┌─────┴──────────────────────────┐
│ PC2 (router, ip_forward = 1)   │
│     ens35: 10.16.209.1/24      │
│     ens33: 10.16.208.2/24      │
└─────┬──────────────────────────┘
      │  Red interna 1 · 10.16.208.0/24
┌─────┴──────────────────────────┐
│ PC1  ens33: 10.16.208.1/24     │
│      gateway: 10.16.208.2      │
└────────────────────────────────┘
```

## Contenido del laboratorio

| Bloque | Qué se hace | Herramientas |
|---|---|---|
| **1. Linux por terminal** | Crear, copiar, mover y borrar ficheros y carpetas combinando rutas relativas y absolutas | `touch`, `nano`, `mkdir`, `cp`, `mv`, `rm`, `pwd`, `ls` |
| **2. Dos VMs sin Internet** | IP estática en cada máquina sin entorno gráfico y análisis del tráfico ICMP y ARP | Netplan, `ip a`, `ifconfig`, `ping`, `tcpdump` |
| **3. Subnetting y router Linux** | Dividir `10.16.208.0/23` en dos `/24`, configurar PC2 como router, rutas estáticas y verificación del camino | Netplan, `sysctl`, `ping`, `mtr` |

## Resultados clave

**Subnetting.** `10.16.208.0/23` (510 hosts utilizables) → dos redes `/24` de 254 hosts cada una, 508 en total. Se pierden 2 direcciones utilizables porque cada subred reserva su propia dirección de red y de broadcast.

| Red | Rango | Broadcast |
|---|---|---|
| Red interna 1 | `10.16.208.0/24` | `10.16.208.255` |
| Red interna 2 | `10.16.209.0/24` | `10.16.209.255` |

**Enrutamiento.** PC1 usa a PC2 como gateway, PC3 tiene una ruta estática hacia la Red interna 1 a través de PC2, y PC2 reenvía paquetes con `net.ipv4.ip_forward=1`.

**Verificación.** Desde PC1, `mtr -rn -c 10 10.16.209.2` muestra 2 saltos (`10.16.208.2` y `10.16.209.2`) con 0 % de pérdida, lo que confirma que el tráfico pasa por PC2.

## Qué demuestra

- Configurar IP estática con Netplan y resolver los problemas habituales: permisos del `.yaml` (`600`) y elegir entre los renderers `networkd` y `NetworkManager`.
- Calcular subredes, máscaras, broadcast y número de hosts a mano.
- Convertir un equipo Linux en router (`ip_forward`, de forma temporal y persistente) y diseñar las rutas de los extremos.
- Leer una captura de `tcpdump` (ICMP echo request/reply, ARP) y comprobar rutas con `mtr` y el `ttl`.

## Documentación

El procedimiento completo, con los comandos, ficheros de configuración y todas las capturas, está en [DOCUMENTACION.md](linux-redes-subnetting-routing.md).

## Estructura del repositorio

```
.
├── README.md
├── linux-redes-subnetting-routing.md   # procedimiento paso a paso con capturas
```

## Entorno

- Ubuntu Server y Ubuntu Desktop en máquinas virtuales (VMware).
- Redes internas mediante *LAN segments*, sin Internet salvo el adaptador NAT de PC3.
- Configuración de red con Netplan.

## Limitaciones

- Es un laboratorio de fundamentos: no incluye cortafuegos, NAT en el router ni reenvío de Internet a las redes internas. PC1 y PC2 no tienen salida a Internet a propósito.
- Las rutas se configuraron a mano, sin protocolos de enrutamiento dinámico.
