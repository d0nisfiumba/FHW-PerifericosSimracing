[⬅️ Volver al Inicio](README.md)

# ⚙️ Arquitectura del Sistema y Flujo de Datos

En hardware de alto rendimiento, el enemigo es la **Latencia**. Analizamos el ciclo completo desde la acción física hasta la respuesta visual ("Motion-to-Photon").

## 🔄 Diagrama de Flujo de Datos (Mermaid)

```mermaid
sequenceDiagram
    participant U as Usuario (Piloto)
    participant V as Volante (USB HID)
    participant PC as PC (CPU/GPU)
    participant M as Monitor (DisplayPort)

    Note over U, V: Acción Mecánica
    U->>V: Gira Volante / Pisa Freno (Presión)
    
    rect rgb(20, 20, 20)
        Note over V, PC: Comunicación USB (Input)
        V->>V: Conversión ADC (Analógico a Digital 16-bit)
        V->>PC: Envío Paquete HID (Polling Rate 1000Hz)
    end
    
    rect rgb(40, 0, 0)
        Note over PC: Procesamiento (Game Loop)
        PC->>PC: Motor de Físicas calcula la tracción
        PC->>PC: GPU renderiza el frame
    end
    
    par Salida Simultánea
        PC->>V: Envío datos FFB (Output Telemetría)
        PC->>M: Envío Frame (Scanout por DisplayPort)
    end
    
    Note over V: Motor Direct Drive aplica Torque
    Note over M: Pixel cambia de color (GtG)
    
    U->>U: El ojo ve + La mano siente
