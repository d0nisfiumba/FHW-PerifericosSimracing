sequenceDiagram
    participant U as Usuario (Piloto)
    participant V as Volante (USB)
    participant PC as PC (CPU/GPU)
    participant M as Monitor (DP)

    Note over U, V: Acción Física
    U->>V: Gira Volante + Presiona Freno
    Note over V, PC: Comunicación Entrada (1000Hz)
    V->>PC: Envía datos posición (X, Y, Z) vía USB
    
    rect rgb(20, 20, 20)
        Note over PC: Procesamiento
        PC->>PC: Simula físicas (Suspensión, Agarre)
        PC->>PC: Renderiza frame gráfico
    end
    
    par Salida Paralela
        PC->>V: Envía datos Force Feedback (USB)
        PC->>M: Envía Frame de Video (DisplayPort)
    end
    
    Note over V: Motor reacciona (Torque)
    Note over M: Panel actualiza píxeles
    
    U->>U: Ojo ve + Mano siente
