# 🏢 Cerebro Agente de Rentas — Arquitectura Multi-Agente Optimizada en Tokens

Sistema modular de atención al cliente inmobiliaria diseñado con un **Agente Principal (Router)**, **Subagentes especializados por tipo de inmueble** y un módulo de **Skills operativos** para optimizar el consumo de contexto y acelerar la calificación de prospectos.

---

## 🎯 Problema que resuelve
Los asistentes tradicionales cargan todo el catálogo y reglas en cada consulta, consumiendo demasiados tokens y generando respuestas largas o imprecisas. Esta arquitectura divide el conocimiento en archivos ligeros en Markdown (`.md`) para que la IA lea **únicamente** la información que el cliente necesita.

---

## 🧠 Estructura del Cerebro

| Archivo | Rol en el sistema | Función principal |
| :--- | :--- | :--- |
| `agente_principal.md` | **Coordinador / Router** | Filtra la intención inicial del cliente y enruta al subagente exacto sin leer el resto. |
| `subagente_casa.md` | **Especialista en Vivienda** | Gestiona renta/venta de casa habitación, características y requisitos. |
| `subagente_depa.md` | **Especialista en Departamentos** | Atiende renta de espacios individuales exclusivos para oficinas y consultorios. |
| `subagente_edificio.md` | **Especialista Corporativo** | Maneja renta de edificios completos, superficies por nivel y accesorias comerciales. |
| `skill_rentas.md` | **Operaciones y Handoff** | Valida disponibilidad, presupuesto y aplica reglas de derivación inteligente de Bot a Asesor Humano. |

---

## ⚙️ Flujo de Funcionamiento
1. **Clasificación rápida:** El Agente Principal identifica si el prospecto busca casa, departamento u edificio.
2. **Carga selectiva:** Consulta solo el subagente correspondiente (reduciendo el uso de contexto a ~1% por sesión).
3. **Calificación y Handoff:** Si el cliente cumple requisitos, solicita visita o requiere negociación, activa `skill_rentas.md` para transferir la atención a un asesor humano.

---

## 🛠️ Tecnologías y Metodología
* **Arquitectura:** Prompt Engineering modular + Context Engineering en Markdown.
* **Entorno:** Claude Projects & Visual Studio Code.
* **Control de versiones:** GitHub.

---

*Desarrollado por **Lilia Rojas Rojas** — Proyectos de Automatización e Inteligencia Artificial Aplicada.*
