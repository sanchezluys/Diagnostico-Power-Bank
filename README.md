# Diagnostico-Power-Bank
Metodología para el diagnostico de dispositivo electrónico, Power Bank

## Datos técnicos

| Item | Descripción | Valor |
| --------- | --------- | --------- |
|  1         | Modelo          |           |
|  2         | Marca          |           |
|  3         | Serial          |           |

```mermaid
graph TD
    A[Inicio] --> B{Power bank no enciende}
    B --> C[Verificar que esté cargado correctamente]
    C --> D[Intentar encender el power bank]
    D --> E{¿Encendió?}
    E -- Sí --> F[Fin]
    E -- No --> G[Inspección visual]
    
    G --> H[Revisar conexiones sueltas o dañadas]
    H --> I{¿Conexiones en buen estado?}
    I -- Sí --> J[Continuar diagnóstico]
    I -- No --> K[Reparar conexiones]
    K --> D
    
    J --> L[Revisar la placa de circuito impreso]
    L --> M[Inspeccionar componentes quemados o dañados visualmente]
    M --> N{¿Componentes dañados?}
    N -- Sí --> O[Reemplazar componentes]
    O --> P[Volver a probar encendido]
    P --> E
    
    N -- No --> Q[Medir el estado de las baterías]
    Q --> R[Verificar voltaje de cada celda con multímetro]
    R --> S{¿Voltaje adecuado?}
    S -- No --> T[Reemplazar baterías]
    T --> P
    S -- Sí --> U[Medir continuidad y resistencia de los circuitos]
    U --> V[Verificar reguladores de voltaje]
    V --> W{¿Reguladores funcionando?}
    W -- No --> X[Reemplazar reguladores]
    X --> P
    
    W -- Sí --> Y[Medir voltaje de entrada y salida de la placa]
    Y --> Z{¿Voltajes correctos?}
    Z -- No --> AA[Reparar o reemplazar circuito de control]
    AA --> P
    Z -- Sí --> AB[Revisar puerto de carga y cables]
    AB --> AC{¿Puerto y cables en buen estado?}
    AC -- No --> AD[Reparar o reemplazar puerto/cables]
    AD --> P
    
    AC -- Sí --> AE[Prueba final del power bank]
    AE --> AF{¿Funciona correctamente?}
    AF -- Sí --> F
    AF -- No --> AG[Consultar a un técnico especializado]
    AG --> F

```
