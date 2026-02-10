# 👨‍🏫 Guía Didáctica: Despliegue de DHCP en Linux

## 1. Datos Generales
* **Módulo:** Servicios de Red e Internet.
* **Duración:** 50 minutos.
* **Nivel:** Medio / Administración de Sistemas.
* **Metodología:** Aula Invertida (Flipped Classroom).

## 2. Objetivos de Aprendizaje
Al finalizar la sesión, el alumno será capaz de:
1.  Entender el flujo DORA (Discover, Offer, Request, Acknowledge).
2.  Instalar y configurar `isc-dhcp-server` en Ubuntu/Debian.
3.  Diagnosticar errores comunes mediante logs (`journalctl`).
4.  Configurar reservas de IP estáticas mediante dirección MAC.

## 3. Cronograma de la Sesión (50 min)

| Tiempo | Actividad | Descripción |
| :--- | :--- | :--- |
| **00-05'** | **Bienvenida** | Presentación de objetivos y revisión rápida de dudas del vídeo (visto en casa). |
| **05-15'** | **Repaso Teórico** | Explicación breve de los archivos `/etc/dhcp/dhcpd.conf` y `/etc/default/isc-dhcp-server`. |
| **15-35'** | **Práctica Guiada** | Los alumnos realizan la **Actividad 1** (Configuración básica) y **Actividad 2** (Reserva). |
| **35-45'** | **Gamificación** | Realización del **Kahoot** (50 preguntas) para evaluar conocimientos. |
| **45-50'** | **Cierre y Dudas** | Resolución de problemas surgidos durante la práctica. |

## 4. Solucionario de Errores Típicos (Troubleshooting)

### A. El servicio no arranca (`failed`)
* **Causa:** Error de sintaxis (falta un punto y coma `;`).
* **Solución:** Ejecutar `dhcpd -t` para ver la línea exacta del error.

### B. Error "Not configured to listen on any interfaces"
* **Causa:** No se ha definido la tarjeta de red en el archivo por defecto.
* **Solución:** Editar `/etc/default/isc-dhcp-server` y añadir `INTERFACESv4="eth0"`.

### C. Error "No subnet declaration for eth0"
* **Causa:** La IP estática del servidor no coincide con la `subnet` declarada en `dhcpd.conf`.
* **Solución:** Cambiar la IP del servidor con `ip addr add` para que esté dentro del rango.

## 5. Recursos Necesarios
* Máquina Virtual con Ubuntu Server / Kali Linux.
* Cliente (Windows/Linux) en red interna para probar.
* Acceso a Internet para instalar paquetes (`apt`).
