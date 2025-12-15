# Volantes y Pedales (Sim Racing Setup)

## 1. Definición
El sistema de control de simulación es un conjunto de **dispositivos mixtos (E/S)**:
* **El Volante:** Actúa como **entrada** (enviando el giro y botones) y como **salida**, recibiendo información física del ordenador a través del sistema **Force Feedback (FFB)**.
* **Los Pedales:** Son dispositivos de **entrada** puros que controlan aceleración y frenada.

![Esquema de un volante Direct Drive](https://mozaracing.com/wp-content/uploads/2022/08/R5-Bundle-1.png)
*(Nota: Puedes cambiar esta imagen por una subida a tu repo)*

## 2. Características Principales
* **Force Feedback (FFB) / Par Motor:** Es la fuerza que ejerce el motor para simular físicas (baches, derrapes). Se mide en **Newton-metro (Nm)**.
* **Tecnología de Pedales (Load Cell):** A diferencia de los pedales básicos que miden distancia (potenciómetros), los pedales de gama alta usan **Célula de Carga**, midiendo la **presión (kg)** ejercida, igual que un coche real.
* **Resolución:** La precisión en bits con la que el volante detecta el ángulo de giro.

## 3. Tipos de Tecnologías (Base del Volante)
Existen tres arquitecturas principales:

| Tipo | Descripción | Ventajas/Desventajas |
| :--- | :--- | :--- |
| **Engranajes (Gear)** | Un motor mueve engranajes dentados. | ❌ Ruidoso y con holgura. ✅ Barato. |
| **Correa (Belt)** | Correas de goma transmiten la fuerza. | ✅ Suave y silencioso. ❌ Pierde detalle fino. |
| **Direct Drive (DD)** | El volante va conectado al eje del motor. | ✅ Respuesta inmediata (1:1), máxima potencia. ❌ Precio más alto. |

## 4. Ejemplo Comercial: Moza R5 Bundle
Analizamos este modelo por ser el referente actual en calidad/precio:

* **Tecnología:** Direct Drive (DD).
* **Potencia:** 5.5 Nm de par motor (suficiente para sentir pérdida de tracción sin fatiga extrema).
* **Construcción:** Aleación de aluminio de aviación para disipación pasiva (sin ventiladores).
* **Pedales (SR-P Lite):** Acero de alta resistencia con sensor Hall (magnético) para evitar desgaste.
* **Software:** *Moza Pit House*, permite ajustar las curvas de fuerza y ecualizar las sensaciones del asfalto.

---
[⬅️ Volver al Índice Principal](./README.md)
