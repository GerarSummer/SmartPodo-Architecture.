# SmartPodo: Plataforma SaaS de Gestión Clínica y Expedientes Electrónicos (AI-Driven)

## 1. Título del Proyecto y Descripción High-Level

**SmartPodo** es un sistema integral SaaS (Software as a Service) diseñado como proyecto de tesis de ingeniería para revolucionar la administración clínica y el control de expedientes médicos. La plataforma digitaliza y asegura el ciclo de vida del paciente, resolviendo la fragmentación de historiales clínicos y optimizando el flujo de trabajo del personal médico mediante automatización con Inteligencia Artificial.

Arquitectónicamente, el sistema opera bajo un modelo robusto que prioriza la confidencialidad, integridad y disponibilidad (Tríada CIA) de la información médica, utilizando una infraestructura sin servidor (Serverless) acoplada a un backend reactivo en tiempo real y motores de IA generativa para el soporte a la toma de decisiones clínicas.

---

## 2. Stack Tecnológico y Dependencias Críticas

El núcleo de la aplicación fue construido con un enfoque en seguridad, escalabilidad y procesamiento cognitivo:

### **Frontend & UI/UX**
* **JavaScript (ES6+) / Entorno Web:** Construcción de interfaces dinámicas y responsivas enfocadas en la usabilidad clínica.
* **Manejo del DOM y Estado:** Lógica de cliente optimizada para renderizar historiales médicos complejos sin degradación de rendimiento.

### **Backend, Base de Datos & Inteligencia Artificial**
* **Node.js & Express:** Capa de lógica de negocio y enrutamiento backend para el procesamiento seguro de peticiones.
* **Firebase Firestore & Authentication:** Base de datos NoSQL en tiempo real para colecciones jerárquicas y proveedor de identidad seguro con hashing avanzado y tokens JWT.
* **Integración LLM (Gemini Pro API):** Implementación nativa del modelo Gemini Pro como motor cognitivo del sistema, encargado del procesamiento de lenguaje natural (NLP) y análisis de visión artificial sobre datos clínicos no estructurados.

---

## 3. Arquitectura de Software y Flujo de Datos

El sistema implementa una arquitectura orientada a servicios, optimizada para entornos clínicos:

1.  **Capa de Presentación (Frontend):** Interfaz limpia y enfocada en la productividad médica. Consume directamente los servicios del backend manteniendo un estado sincronizado con la base de datos.
2.  **Autenticación y Control de Acceso (Identity and Access Management):** Mecanismo de validación estricta mediante Firebase Auth. Solo el personal autenticado y autorizado puede realizar consultas de lectura/escritura sobre las colecciones de Firestore.
3.  **Persistencia y Modelo de Datos:** Los registros médicos están desnormalizados estratégicamente en Firestore para permitir lecturas rápidas de los perfiles de pacientes, mientras que los historiales de consultas se mantienen en subcolecciones aisladas para prevenir la sobrecarga de datos.

---

## 4. Funcionalidades Técnicas Clave

* **Procesamiento Óptico y Diagnóstico Asistido (Computer Vision):** Módulo impulsado por Gemini Pro que analiza fotografías médicas subidas al sistema (ej. casos de onicocriptosis/uña encarnada). La IA identifica la anomalía visual, detalla el estado del tejido y sugiere protocolos de intervención y curación basados en la evidencia clínica.
* **Síntesis Inteligente de Historiales (NLP):** Motor de procesamiento cognitivo que analiza longitudinalmente múltiples consultas (ej. 5 meses de evolución, observaciones y tratamientos) para generar un resumen ejecutivo automático del progreso del paciente, agilizando la revisión de expedientes extensos.
* **Asistente Virtual Clínico ("Piecito"):** Chatbot conversacional especializado integrado nativamente en la plataforma para interactuar de forma natural, resolver dudas operativas y guiar los flujos de trabajo del consultorio.
* **Gestión Centralizada de Expedientes Clínicos:** Módulo principal para el alta, edición y consulta de historiales médicos, alergias y antecedentes patológicos.
* **Trazabilidad de Consultas y Auditoría (Logs):** Registro inmutable de la evolución clínica del paciente, con sellos de tiempo (timestamps) de servidor para garantizar la auditoría de los datos y el control de inventario.
* **Control de Identidades y Seguridad:** Sistema de login protegido contra ataques, garantizando que el acceso a la plataforma sea exclusivo del personal autorizado bajo un modelo de control de acceso basado en roles (RBAC).

---

## 5. Cláusula Crítica de Privacidad, Cumplimiento y Gobernanza de Datos (Normativas Clínicas)

> [!WARNING]
> **CLÁUSULA DE SEGURIDAD Y PRIVACIDAD DE DATOS (MOCK DATA POLICY)**
> 
> Hago constar de manera explícita que todos los expedientes clínicos, fotografías de diagnósticos, nombres, recetas y datos demográficos visualizados en esta documentación y capturas de pantalla, consisten única y exclusivamente en **"Mock Data" (Datos sintéticos y simulados de prueba generados para el entorno de desarrollo)**.
> 
> - **CERO EXPOSICIÓN DE DATOS SENSIBLES:** No se expone Información de Identificación Personal (PII) ni Registros de Salud Protegidos (PHI) de pacientes reales.
> - **CUMPLIMIENTO NORMATIVO:** El diseño arquitectónico de este SaaS contempla los principios rectores de confidencialidad médica alineados a estándares normativos (como los fundamentos de la NOM y criterios COFEPRIS para la gestión de expedientes clínicos electrónicos). La integración con la API de IA maneja los flujos de inferencia bajo estrictos controles de sesión para evitar fugas de información.

---

## 6. Galería de Interfaz y Capturas de Pantalla

A continuación, se presentan los módulos principales del sistema. *(Nota: Todas las métricas y perfiles mostrados son datos de simulación).*

## 6. Galería de Interfaz y Capturas de Pantalla

A continuación, se presentan los módulos principales del sistema. *(Nota: Todas las métricas, nombres y perfiles mostrados son datos de simulación controlada).*

### Tabla de Gestión de Expedientes
<img width="1918" height="911" alt="eXPEDIENTES" src="https://github.com/user-attachments/assets/8f1d8e67-63b6-455a-a988-8704e63c86bd" />



### Detalle del Expediente y Perfil del Paciente
<img width="1912" height="911" alt="EXPEDIENTE ADENTRO" src="https://github.com/user-attachments/assets/00f4c3d5-46e7-487e-97b0-f18a09df6741" />




### Registro de Nueva Cita y Consulta
<img width="1917" height="911" alt="Nueva cita" src="https://github.com/user-attachments/assets/bfbdc565-3ef0-4dd9-b6d9-78dff080e87b" />



### Catálogo de Servicios Clínicos
<img width="1916" height="913" alt="catalogo de servicio" src="https://github.com/user-attachments/assets/2d3f8ad7-9299-46d5-9f72-7e7982aeb8a0" />



### Gestión de Usuarios, Accesos y Licencias
<img width="1917" height="908" alt="Gestion de usuarios y nombre de clinica contratada con licencia" src="https://github.com/user-attachments/assets/8504a67e-35a4-495a-b11a-ad038104a3a2" />



### Control de Inventario Clínico
<img width="1917" height="910" alt="Inventario" src="https://github.com/user-attachments/assets/af4c5eaa-9a31-4640-b532-0970d46a9824" />



### Dashboard Clínico y Panel de Control
<img width="1916" height="908" alt="DASH" src="https://github.com/user-attachments/assets/3bb1f8ca-9b5a-4d80-878c-b8521fe3a742" />



### Cumplimiento Normativo (Módulo COFEPRIS)
<img width="1915" height="910" alt="COFEPRIS" src="https://github.com/user-attachments/assets/a0a9d9dc-2f22-4ca1-b05e-ffe297c699e1" />



### Bitácora de Auditoría y Trazabilidad (Logs)
<img width="1920" height="910" alt="bitacora" src="https://github.com/user-attachments/assets/67a7171f-6d2c-475c-8e74-134db95aac77" />



---
*Diseño, desarrollo y arquitectura por Gerardo Gabriel Verano Martínez como proyecto de tesis en Ingeniería en Sistemas Computacionales.*
