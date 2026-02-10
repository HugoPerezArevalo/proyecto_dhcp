# 🌐 Proyecto Aula Invertida: Servidor DHCP en Linux

![Linux](https://img.shields.io/badge/OS-Linux-black?logo=linux)
![Service](https://img.shields.io/badge/Service-ISC--DHCP--SERVER-blue)
![Status](https://img.shields.io/badge/Status-Completed-success)

**Módulo:** Servicios de Red e Internet (SRI)  
**Curso:** 2025/2026  
**Autores:** * 👤 **Hugo Pérez Arévalo** * 👤 **Alejandro Álvarez Romero**

---

## 📖 1. Descripción del Proyecto
Este repositorio contiene todo el material didáctico y técnico necesario para impartir una sesión de **Aula Invertida (Flipped Classroom)** sobre el protocolo **DHCP (Dynamic Host Configuration Protocol)**.

El objetivo es enseñar a los compañeros cómo automatizar la asignación de direcciones IP en una red corporativa utilizando **Ubuntu Server / Kali Linux**.

---

## 📂 2. Índice del Material (Estructura del Repositorio)

A continuación se detalla el contenido de cada carpeta para facilitar la corrección:

### 🔹 `/presentacion`
* **`diapositivas_dhcp.pdf`**: Presentación visual para la clase (Teoría + Práctica).
* **`/img`**: Capturas de pantalla originales del proceso de instalación y configuración.

### 🔹 `/material_aula_invertida`
* 📄 **`cheatsheet_dhcp.md`**: Hoja de trucos (Chuleta) con comandos y sintaxis para los alumnos.
* 🎬 **`GUION_VIDEO.md`**: Guion técnico utilizado para grabar el vídeo tutorial previo a la clase.

### 🔹 `/actividades`
* 🛠️ **`solucion_actividad_1.conf`**: Archivo de configuración real (`dhcpd.conf`) probado en clase.
* 📝 **Enunciados**: Prácticas propuestas (Básica: Configuración de ámbito; Avanzada: Reserva de IP por MAC).

### 🔹 `/kahoot`
* 🦁 **`preguntas_kahoot.md`**: Banco de 50 preguntas técnicas con respuestas justificadas.
* 📊 **`kahoot_import.xlsx`**: Archivo Excel listo para importar a la plataforma Kahoot.
* 🎮 **[Jugar al Kahoot ahora](https://create.kahoot.it/share/proyecto-dhcp/225e2179-fd4d-43eb-b739-31503a34952a)**: Enlace directo al cuestionario interactivo de 50 preguntas.

### 🔹 `/examen`
* 📝 **`examen_dhcp.md`**: Prueba objetiva de evaluación con 30 preguntas (Test + Casos Prácticos).

### 🔹 `/guia_profesor`
* 👨‍🏫 **`GUIA_DIDACTICA.md`**: Documento con la temporalización, objetivos y solución de errores típicos.

---

## 🚀 3. Instalación y Despliegue Rápido

Para replicar este proyecto en tu máquina local:

1.  **Clonar el repositorio:**
    ```bash
    git clone [https://github.com/HugoPerezArevalo/proyecto_dhcp.git](https://github.com/TU_USUARIO/proyecto_dhcp.git)
    ```
2.  **Instalar el servicio:**
    ```bash
    sudo apt update && sudo apt install isc-dhcp-server -y
    ```
3.  **Aplicar configuración (Ejemplo):**
    ```bash
    sudo cp proyecto_dhcp/actividades/solucion_actividad_1.conf /etc/dhcp/dhcpd.conf
    sudo systemctl restart isc-dhcp-server
    ```

---

## 💡 4. Reflexión Final del Grupo

Realizar este proyecto nos ha permitido profundizar en el funcionamiento interno de las redes, yendo más allá de la teoría:

1.  **Dificultades Técnicas:** Lo más complejo fue entender la lógica de los archivos de configuración en Linux. Tuvimos problemas iniciales con el error *"Not configured to listen on any interfaces"*, que solucionamos editando el archivo `/etc/default/isc-dhcp-server`. También aprendimos la importancia de que la IP estática del servidor coincida con la `subnet` declarada.
2.  **Aprendizaje:** Hemos aprendido a diagnosticar errores reales leyendo los logs del sistema (`journalctl`), algo fundamental para un administrador de sistemas.
3.  **Metodología:** Preparar el material para enseñar a otros nos ha obligado a dominar el tema mucho mejor que si solo hubiéramos estudiado para un examen. "Enseñar es aprender dos veces".

---
*Proyecto realizado bajo licencia académica para Albor Croft.*
