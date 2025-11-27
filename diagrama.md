[Volver al Inicio](README.md) | [Empresa](empresa.md) | [Tecnologías](tecnologias.md) | [Digitalización](digitalizacion.md) | [Transformación](transformacion_digital.md) | [Reflexión](reflexion.md)

---

# Arquitectura de la Solución (IT + OT + IA)

Este diagrama representa cómo fluyen los datos desde la planta física hasta el sistema de negocio, pasando por el motor de Inteligencia Artificial.

```mermaid
graph LR
    %% Subgrafo de PLANTA (OT)
    subgraph OT [PLANTA - Operaciones Físicas]
        direction TB
        A[Sensores IoT]
        B[Lectores RFID]
        C[Cámaras Visión]
        D(Concentrador de Datos)
        
        A --> D
        B --> D
        C --> D
    end

    %% Subgrafo de INTELIGENCIA ARTIFICIAL
    subgraph IA [MOTOR DE INTELIGENCIA ARTIFICIAL]
        direction TB
        Motor{Algoritmo ML}
    end

    %% Subgrafo de NEGOCIO (IT)
    subgraph IT [NEGOCIO - Gestión Digital]
        direction TB
        E[ERP Gestión]
        F[CRM Clientes]
        G[App Móvil]
        H(Data Lake / Nube)

        H --> E
        H --> F
        H --> G
    end

    %% Conexiones entre Áreas
    D -->|Datos en tiempo real| Motor
    E -->|Histórico de ventas| Motor
    F -->|Datos de clientes| Motor

    %% Decisiones de la IA (Salidas)
    Motor -->|1. Orden de Compra Auto| E
    Motor -->|2. Oferta Personalizada| G
    Motor -->|3. Alerta Reposición| A
