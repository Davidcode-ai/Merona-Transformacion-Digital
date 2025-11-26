graph TD
    %% Planta (OT)
    PlantaOT[Planta OT] --> IoT[IoT y Sensores]
    PlantaOT --> RFID[RFID y Códigos de Barras]
    IoT --> Plataforma[Plataforma de Datos]
    RFID --> Plataforma
    Plataforma --> MotorIA[Motor de Inteligencia Artificial]
    MotorIA --> OptPlanta[Optimización y Decisiones en Planta]

    %% Negocio (IT)
    NegocioIT[Negocio IT] --> ERP[ERP Conectado]
    NegocioIT --> CRM[CRM con IA]
    NegocioIT --> Chatbot[Chatbot con IA]
    ERP --> Plataforma
    CRM --> Plataforma
    Chatbot --> Plataforma
    Plataforma --> OptNegocio[Optimización y Decisiones en Negocio]

    %% Colores para diferenciar
    classDef planta fill:#f9f,stroke:#333,stroke-width:1px;
    classDef negocio fill:#9ff,stroke:#333,stroke-width:1px;
    class PlantaOT,IoT,RFID,OptPlanta planta;
    class NegocioIT,ERP,CRM,Chatbot,OptNegocio negocio;
