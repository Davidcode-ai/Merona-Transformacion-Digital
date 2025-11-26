🏠 [Volver al Inicio](README.md) | 🏢 [Empresa](empresa.md) | ⚙️ [Tecnologías](tecnologias.md) | 🚀 [Transformación](transformacion_digital.md) | 🧠 [Reflexión](reflexion.md)

---

# 📊 Arquitectura de la Solución (IT + OT + IA)

Este diagrama muestra el flujo de datos desde la captura física hasta la toma de decisiones inteligente.

```mermaid
graph TD
    %% Definición de Estilos
    classDef planta fill:#e1f5fe,stroke:#01579b,stroke-width:2px;
    classDef negocio fill:#f3e5f5,stroke:#4a148c,stroke-width:2px;
    classDef ai fill:#fff3e0,stroke:#e65100,stroke-width:4px;

    subgraph OT [" 🏭 PLANTA (Operaciones Físicas) "]
        direction TB
        A(📡 Sensores IoT Estanterías):::planta
        B(🏷️ Lectores RFID):::planta
        C(📹 Cámaras Visión Artificial):::planta
        D[Concentrador OT]:::planta
    end

    subgraph IT [" 💻 NEGOCIO (Gestión Digital) "]
        direction TB
        E(🖥️ ERP Conectado):::negocio
        F(👥 CRM Clientes):::negocio
        G(📱 App / Chatbot):::negocio
        H[Data Lake Cloud]:::negocio
    end

    %% Conexiones
    A --> D
    B --> D
    C --> D
    D -->|Datos en tiempo real| H
    E -->|Histórico Ventas| H
    F -->|Datos Clientes| H
    G -->|Consultas| H

    subgraph BRAIN [" 🧠 MOTOR DE INTELIGENCIA ARTIFICIAL "]
        I{Algoritmo ML}:::ai
    end

    H --> I
    I -->|Predicción de Demanda| E
    I -->|Oferta Personalizada| F
    I -->|Alerta de Reposición| A
