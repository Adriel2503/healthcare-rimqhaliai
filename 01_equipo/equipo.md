# 📋 Entregable 1: Información del equipo y propuesta inicial

> **⚠️ Importante:** Este entregable debe completarse antes del **viernes 21 de noviembre a las 5:30 PM** para continuar en la competencia.

---

## ✅ Cómo entregar este documento

1. **Completa todas las secciones** de este archivo con la información de tu equipo
2. **Guarda los cambios:**
   - Desde GitHub: Presiona "Commit changes" al terminar de editar
   - Localmente: Ejecuta `git add .` y `git commit -m "Entregable 1 completo"`
3. **Sube a GitHub:** 
   - Desde GitHub: Automático al hacer commit
   - Localmente: Ejecuta `git push`
4. **Verifica:** Refresca este repositorio en GitHub y confirma que tus cambios estén visibles

> 💡 **Tip:** No necesitas crear un nuevo repositorio. Solo edita este archivo y guarda los cambios.

---

## Nombre del equipo

**Rimqhali.ai**


---

## ¿Cuéntanos a grandes rasgos qué planean hacer?

> Describe brevemente la idea principal de tu solución. Incluye los componentes clave, la tecnología que planeas usar y cómo esperas que tu solución resuelva el reto planteado.

**Ejemplo:**  
*"Desarrollaremos un buscador inteligente de doctores que utiliza web scraping para extraer información de clínicas públicas (médicos, especialidades, horarios). Implementaremos un sistema ETL con Python y Pandas para normalizar los datos, una API REST con FastAPI para las consultas, y un frontend con Next.js. La búsqueda será potenciada con algoritmos de ML para búsqueda semántica, permitiendo a los usuarios encontrar especialistas por ubicación, disponibilidad o tipo de atención."*

**Tu respuesta:**

El plan principal consiste en desarrollar Rimqhali.ai, un Agente Virtual de Salud con Inteligencia Artificial diseñado como un compañero digital y orquestador proactivo de servicios de bienestar, estructurado en seis módulos clave:

Módulo A: Asistente de Triaje + Gestión de Beneficios
Funcionalidad: Clasificación conversacional de síntomas por nivel de urgencia, con priorización de citas (presencial/virtual) y gestión de beneficios; además, permite priorizar el agendamiento con doctores mejor calificados según la atención previa.

Módulo B: Seguimiento y Adherencia a Tratamientos
Funcionalidad: Registro de tratamientos y envío de recordatorios personalizados (app/WhatsApp/SMS), aplicando gamificación y generando alertas médicas ante un alto riesgo de no adherencia.

Módulo C: Panel para Personal Médico / Call Center
Funcionalidad: Vista única para el personal de salud con el resumen consolidado del historial del paciente y todas las alertas priorizadas generadas por el sistema.

Módulo D: Índice de Bienestar + Sentimiento
Funcionalidad: Análisis continuo del sentimiento del usuario para calcular un Índice de Bienestar (0-100) y ofrecer recomendaciones de salud accionables y contextualizadas.

Módulo E: Modo Emergencia RIMAC
Funcionalidad: Botón o activación por voz que dispara una alerta inmediata a la central con datos del asegurado, ubicación GPS y resumen de síntomas para una respuesta coordinada.

Módulo F: Modo Familia / Cuidador
Funcionalidad: Implementación de una "Vista de Modo Familia" dentro de la app donde el asegurado principal puede conectar y agregar familiares (asegurados o no asegurados, estos últimos solo con credenciales de visor). Este modo permite que los familiares/cuidadores vean un resumen detallado del paciente, incluyendo el progreso de tratamientos, el estado de sus citas, notas clave del doctor y exámenes médicos, facilitando el seguimiento integral.

---

## ¿Qué retos/riesgos visualizan? (¿Con qué te podemos ayudar?)

> Identifica los principales desafíos o riesgos que podrían afectar el desarrollo de tu solución. Estos pueden ser técnicos, operativos o relacionados con la viabilidad de la idea. Además, menciona cualquier apoyo específico que necesites para superar estos obstáculos.

**Ejemplo:**  
*"El principal reto será la variabilidad en la estructura de los sitios web de las clínicas, lo que puede dificultar el scraping. También prevemos desafíos en la normalización de especialidades médicas que tienen diferentes nomenclaturas. Necesitaríamos apoyo con acceso a APIs oficiales si existen, y guía sobre el manejo de datos sensibles de salud."*

**Tu respuesta:**

Los principales riesgos de nuestro asistente virtual de salud para Rímac se concentran en datos, clínica, integración vía MCP y operación.

**1. Gobernanza y privacidad de datos de salud (PHI).** Existe riesgo de uso inadecuado de datos sensibles, falta de consentimiento explícito y almacenamiento inseguro. Nuestro sistema multiagente consultará información del cliente, por lo que debemos limitar estrictamente qué datos se usan para personalizar recomendaciones y cómo se registran las conversaciones en la app.

**2. Riesgos en la capa de integración MCP (API Hub).** MCP será la “puerta de entrada” a los sistemas de Rímac. Publicaremos APIs que la IA consumirá y otras que seguirán usándose de forma tradicional (app, web, call center). Hay riesgo de:

* Sobre-permisos en las APIs que usa la IA.
* Falta de separación clara entre APIs “para IA” y APIs “normales”.
* Inconsistencias de negocio si distintas capas consumen versiones diferentes.

Esto exige una gobernanza de APIs clara: scopes específicos para el agente, control de acceso por cliente, versionado y monitoreo de consumo.

**3. Riesgo médico-legal por exceder el rol asistencial.** El asistente no debe prescribir ni ajustar medicación. Su alcance se limitará a triaje básico (a qué especialidad ir), recomendación de centros cercanos, gestión de citas y recordatorios. Si el modelo comenzara a dar indicaciones clínicas concretas, podría considerarse acto médico y generar responsabilidad legal.

**4. Alucinaciones y sesgos en recomendaciones.** La IA podría inventar coberturas/beneficios o favorecer ciertos centros sin criterios transparentes, afectando confianza y percepción de equidad.

**5. Disponibilidad y observabilidad.** Fallas o latencias altas en horas pico afectarían la experiencia del cliente. Sin métricas en tiempo real (uso, errores, desvíos en triaje, escalamiento a humano) se dificulta detectar incidentes, medir impacto en prevención y mejorar el comportamiento del agente de forma continua.


---

## Tecnologías planificadas

Lista las principales tecnologías, frameworks y herramientas que planean utilizar:

*Frontend:*
- React Nativa

*Backend:*
- Node JS, Express js

*IA/ML:*
- OpenAI, Gemini PRO 3, Claude

*Cloud/DevOps:*
- AWS EC2, Lambda, SageMaker

*Otras:*
- Expo Go, LangChain, RAG, Typescript, SCSS, TaildWindCSS, Docker, N8N

---

## Notas adicionales

Nuestra motivación para participar en esta Hackathon y crear Rimqhali.ai surge de una experiencia personal profunda de una integrante del equipo: la pérdida de un familiar debido a la desinformación en el hogar sobre citas y síntomas, y la minimización de problemas de salud. Buscamos evitar que otras familias pasen por ese dolor, por lo que diseñamos un sistema que garantiza la transparencia y la proactividad. Funcionalidades como el Triaje conversacional y el Modo Familia/Cuidador no son solo tecnología, sino herramientas esenciales para que todos estén plenamente informados, elevando la salud de la gestión individual a una responsabilidad familiar.

*Experiencia del equipo:*
- Benjamin fue a programar a Suiza
- Ariel trabajó en una consulting de España
- Brigitte fundó una startup
- Harold, experto en anáslisis de Datos 
