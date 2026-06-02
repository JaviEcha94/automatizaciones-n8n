# 🤖 Automatizaciones N8N — Javier Echalecu

Colección de workflows de N8N construidos como parte
de mi formación en IA & Automatización.

---

## Flujo 5 — Lead Intelligence + Audit Trail

**Problema que resuelve:**
Los leads que entran por formulario web necesitan
ser clasificados por prioridad, notificar al ejecutivo
y dejar registro de cada operación para trazabilidad.

**Solución:**
Workflow de N8N que procesa leads de punta a punta:
- PII masking antes de enviar datos a la IA
- Clasificación automática con Gemini 2.5 Flash
- Deduplicación por idempotency key
- Notificación por email al ejecutivo con prioridad y razón
- Error branching en nodos críticos (Gemini + Email)
- Audit trail completo en Google Sheets

**Stack:**
N8N · Gemini 2.5 Flash · Google Sheets · Gmail SMTP

**Resultado:**
Todo lead procesado queda registrado en el audit log
con timestamp, acción, resultado y detalle —
sin importar si fue exitoso, duplicado o falló.
