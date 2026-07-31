# gestor-inteligente-reclamos-ia
Sistema inteligente de gestión de reclamos para ecommerce utilizando n8n, OpenAI, Gmail y Airtable con Human-in-the-Loop.
# 🚀 Sistema Inteligente de Gestión de Reclamos y Compensaciones con IA

## Trabajo Final – Arquitectura de Flujos con Inteligencia Artificial

Sistema desarrollado para automatizar el proceso de gestión de reclamos de clientes de un ecommerce mediante **n8n**, **OpenAI**, **Airtable** y **Gmail**, incorporando un proceso de **Human-in-the-Loop (HITL)** para garantizar el control humano antes de responder al cliente.

---

# 🎯 Objetivo

Automatizar el ciclo completo de atención de reclamos, desde la recepción del correo electrónico hasta la respuesta final al cliente, utilizando Inteligencia Artificial para analizar el caso, clasificarlo y proponer una compensación acorde a las políticas de la empresa.

---

# 🏗 Arquitectura

```
Cliente
   │
   ▼
Gmail Trigger
   │
   ▼
Normalización del correo
   │
   ▼
Airtable
(Clientes y Reclamos)
   │
   ▼
Carga de Políticas
   │
   ▼
OpenAI GPT-4o Mini
   │
   ▼
Análisis IA
   │
   ▼
Human in the Loop
(Aprobación por Email)
   │
 ┌─┴─────────────┐
 │               │
 ▼               ▼
Aprobado      Rechazado
 │
 ▼
Respuesta Gmail
 │
 ▼
Actualización Airtable
```

---

# ⚙ Tecnologías utilizadas

- n8n Cloud
- OpenAI API (GPT-4o Mini)
- Airtable
- Gmail
- Human-in-the-Loop (HITL)
- GitHub

---

# 📌 Funcionalidades implementadas

- Recepción automática de reclamos desde Gmail.
- Creación automática del cliente.
- Registro automático del reclamo.
- Consulta de políticas de compensación.
- Clasificación mediante Inteligencia Artificial.
- Análisis de sentimiento.
- Priorización automática.
- Selección de política de compensación.
- Generación de respuesta sugerida.
- Aprobación humana antes del envío.
- Respuesta automática en el mismo hilo de Gmail.
- Actualización automática de Airtable.
- Dashboard de monitoreo.

---

# 📂 Estructura del repositorio

```
📦 gestor-inteligente-reclamos-ia
│
├── docs
│   ├── Informe.pdf
│   ├── Manual_Datos.pdf
│   ├── Costos_IA.pdf
│   └── Seguridad_Resiliencia.pdf
│
├── workflow
│   └── gestor-inteligente-reclamos.json
│
├── evidencia
│   ├── Capturas del funcionamiento
│
├── enlaces.md
│
└── README.md
```

---

# 📄 Documentación incluida

- Informe completo del proyecto.
- Manual operativo de datos.
- Matriz de costos del modelo de IA.
- Documento de seguridad y resiliencia.
- Workflow exportado de n8n.
- Evidencias del funcionamiento.
- Dashboard de Airtable.

---

# 🔄 Flujo de funcionamiento

1. El cliente envía un reclamo por Gmail.
2. n8n recibe el correo mediante Gmail Trigger.
3. Se crea o actualiza el cliente en Airtable.
4. Se registra el reclamo.
5. Se cargan las políticas de compensación.
6. OpenAI analiza el caso.
7. La IA clasifica el reclamo y propone una compensación.
8. Se solicita aprobación humana.
9. El operador aprueba o rechaza la propuesta.
10. Se responde al cliente y se actualiza Airtable.

---

# 📊 Recursos

## Workflow n8n

```
workflow/gestor-inteligente-reclamos.json
```

## Dashboard Airtable

Agregar aquí el enlace público de la Interface.

## Base de Datos Airtable

Agregar aquí el enlace público en modo lectura.

---

# 🔒 Seguridad

El sistema incorpora las siguientes medidas:

- Human-in-the-Loop antes de responder al cliente.
- Uso de credenciales seguras de n8n.
- Minimización de datos enviados al modelo de IA.
- Registro completo del ciclo del reclamo.
- Trazabilidad mediante Gmail Message ID y Thread ID.

---

# 💰 Optimización de costos

Se seleccionó **GPT-4o Mini** como modelo principal por ofrecer un excelente equilibrio entre costo, velocidad y precisión para tareas de clasificación, análisis de sentimiento y generación de respuestas.

---

# 👨‍💻 Autor

**Lautaro Agustín Coria**

Trabajo Final – Arquitectura de Flujos con Inteligencia Artificial

Año 2026
