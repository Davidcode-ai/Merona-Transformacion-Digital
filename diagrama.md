# Diagrama Mermaid de IT + OT + IA

```mermaid
graph TD
A[Planta - Almacén OT] --> B[IoT y Sensores Inteligentes]
A --> C[RFID y Lectura de Códigos de Barras]
A --> D[Machine Learning - Previsión de Demanda]
B --> H[Plataforma de Datos]
C --> H
D --> H

E[Negocio IT] --> F[ERP Conectado]
E --> G[CRM con IA]
E --> I[Chatbot con IA]
E --> J[Base de Datos]
F --> H
G --> H
I --> H
J --> H

H --> K[Motor de Inteligencia Artificial]
K --> L[Decisiones Automáticas y Optimización]
