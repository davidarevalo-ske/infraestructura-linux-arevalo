# Infraestructura de Servicios de Red en Linux (`arevalo.lab`)

**Autor:** David Alejandro Arevalo Zeas  
**Modalidad:** Individual  
**Plataforma Servidor:** CentOS Stream 10 (`srv-arevalo`)  
**Dirección IP:** `192.168.18.248`  
**Dominio Local:** `arevalo.lab`  

---

## Descripción General

Este repositorio contiene las evidencias y la documentación técnica de la implementación, endurecimiento (*hardening*) y validación funcional de una infraestructura de servicios esenciales de red en Linux, operando bajo políticas activas de **SELinux (`Enforcing`)** y control perimetral mediante **Firewalld**.

### Resumen de Servicios Desplegados

| Servicio | Software / Demonio | Puerto / Protocolo | Registro DNS | Estado |
| :--- | :--- | :--- | :--- | :--- |
| **DNS (Resolución de Nombres)** | BIND (`named`) | `53/TCP`, `53/UDP` | `ns1.arevalo.lab` | Operativo |
| **Web (Servidor HTTP)** | Apache (`httpd`) | `80/TCP` | `www.arevalo.lab` | Operativo |
| **Administración Remota** | OpenSSH (`sshd`) | `2222/TCP` | `ssh.arevalo.lab` | Operativo |

---

## Documentación Técnica y Entregables

* 👉 **[Ir a la Wiki Oficial del Proyecto](https://github.com/davidarevalo-ske/infraestructura-linux-arevalo/wiki)**
* 📄 **[Leer el Informe Técnico Completo](INFORME_TECNICO.md)**

### Índice de la Wiki
* **[Home](https://github.com/davidarevalo-ske/infraestructura-linux-arevalo/wiki):** Arquitectura general y tabla de parámetros de red.
* **[01 - Servicio DNS](https://github.com/davidarevalo-ske/infraestructura-linux-arevalo/wiki/01-Servicio-DNS):** Configuración autoritativa de BIND y validación directa/cliente.
* **[02 - Servicio Web](https://github.com/davidarevalo-ske/infraestructura-linux-arevalo/wiki/02-Servicio-Web):** Despliegue de Apache, interfaz interactiva, contextos SELinux y pruebas por navegador.
* **[03 - Servicio SSH](https://github.com/davidarevalo-ske/infraestructura-linux-arevalo/wiki/03-Servicio-SSH):** Migración al puerto personalizado `2222/TCP` y acceso remoto sin privilegios directos de `root`.
* **[04 - Seguridad y Troubleshooting](https://github.com/davidarevalo-ske/infraestructura-linux-arevalo/wiki/04-Seguridad-y-Troubleshooting):** Auditoría de `firewalld`, SELinux, respaldos en `/root/backups_interciclo/` e incidentes resueltos.

---

## Estructura del Repositorio

* `01_red_dns.png` — Configuración base de red y hostname (`srv-arevalo`)
* `02a_bind_servidor.png` — Validación de zona `arevalo.lab` y estado de `named`
* `02b_nslookup_cliente.png` — Resolución DNS desde cliente Windows
* `03a_apache_servidor.png` — Estado de Apache (`httpd`) y contexto SELinux
* `03b_web_navegador.png` — Interfaz web interactiva (`www.arevalo.lab`)
* `04_ssh_2222.png` — Sesión SSH segura en puerto `2222/TCP`
* `05_seguridad_backups.png` — Respaldos en `/root/backups_interciclo/`, SELinux `Enforcing` y Firewalld
* `INFORME_TECNICO.md` — Informe técnico completo con evidencias integradas
* `README.md` — Portada e índice general del proyecto
