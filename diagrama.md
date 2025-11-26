# Diagrama Mermaid

```mermaid
flowchart LR

A[Clientes] -->|Pedidos Online| B(E-commerce)
B --> C[CRM]

subgraph IT
    C --> D[ERP]
    D --> E[Base de Datos]
    D --> F[Dashboard Power BI]
end

subgraph OT
    G[Sensores IoT] --> H[PLC]
    H --> I[SCADA]
    I --> D
end

E --> J[IA: Predicción de Demanda]
H --> K[IA: Mantenimiento Predictivo]

J --> D
K --> I
