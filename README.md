# 🏎️ Arquitectura de Hardware en Simulación (SimRacing)

![Estado del Proyecto](https://img.shields.io/badge/Estado-Terminado-green) ![Asignatura](https://img.shields.io/badge/Asignatura-Fundamentos_Hardware-blue) ![Plataforma](https://img.shields.io/badge/Plataforma-PC-lightgrey)

## 📖 Descripción del Proyecto
Este repositorio documenta técnicamente el ecosistema de hardware necesario para un simulador de carreras profesional. A diferencia del hardware de oficina o gaming convencional, el *SimRacing* requiere periféricos de **baja latencia**, **alto ancho de banda** y **retroalimentación física (Haptic Feedback)** en tiempo real.

El objetivo es analizar cómo fluyen los datos desde la entrada física (volante) hasta la salida visual (monitor), pasando por el procesamiento de la CPU/GPU.

## 🗂️ Estructura del Documentación

| Módulo | Descripción Técnica |
| :--- | :--- |
| **[1. Sistema Visual (Monitores)](monitores.md)** | Análisis de paneles, ancho de banda (HDMI/DP), sincronización vertical y cálculo de FOV. |
| **[2. Sistema de Control (Volantes)](volantes.md)** | Ingeniería de motores Direct Drive, sensores Hall, Células de Carga y protocolos USB. |
| **[3. Arquitectura y Comunicación](arquitectura.md)** | **Diagramas de flujo**, latencia "End-to-End", Polling Rate y cuellos de botella. |

## 🛠️ Tecnologías Analizadas
* **Protocolos:** USB HID, HDMI 2.1, DisplayPort 1.4.
* **Física:** Torque (Nm), Fuerza G, Presión hidráulica (Load Cell).
* **Renderizado:** Ray Tracing, VRR (G-Sync/FreeSync).

---
**Autor:** Daniel González Hidalgo  
**Curso:** 1º ASIR / DAM / DAW  
**Licencia:** MIT
