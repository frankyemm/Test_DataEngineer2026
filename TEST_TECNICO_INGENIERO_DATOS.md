# Test Técnico - Ingeniero de Datos
## Sun Valley Investment - 2026

---

## Contexto del Proyecto

Sun Valley Investment necesita procesar y estructurar información de reportes técnicos mineros (NI 43-101) para facilitar la toma de decisiones de inversión. Los reportes están en formato PDF y contienen información valiosa sobre proyectos mineros, recursos, reservas, metadata de proyectos, etc.

## Objetivo del Test

Evaluar la capacidad del candidato para:
1. Extraer información no estructurada de documentos PDF
2. Implementar un script/pipeline de procesamiento de datos
3. Estructurar datos en formatos utilizables
4. Documentar su solución de manera clara

---

## Tiempo de Entrega: 2 días

---

## Tarea Principal: Extracción y Estructuración de Datos

Desarrollar un script/pipeline que extraiga información estructurada de **al menos 2-3 reportes técnicos** de la carpeta `/data`.

### Información a Extraer

**Debes intentar extraer las siguientes 4 categorías. Si alguna información no está disponible en el reporte, déjala vacía/null pero intenta obtener lo que puedas de cada categoría:**

1. **Metadata del Proyecto:**
   - Nombre del proyecto
   - Nombre de la compañía
   - Ubicación geográfica (país, región)
   - Fecha del reporte

2. **Recursos Minerales:**
   - Categoría (Measured, Indicated, Inferred)
   - Toneladas
   - Ley (grade) principal (Au, Ag, Cu, etc.)
   - Contenido metálico estimado

3. **Reservas Minerales:**
   - Categoría (Proven, Probable)
   - Toneladas
   - Ley (grade)
   - Contenido metálico

4. **Información Económica:**
   - CAPEX estimado
   - OPEX estimado
   - NPV (Valor Presente Neto)
   - IRR (Tasa Interna de Retorno)

### Entregables Requeridos

1. **Código fuente** (Python preferido, pero puedes usar otro lenguaje)
2. **Datos extraídos** en JSON o CSV
3. **README.md** con:
   - Cómo ejecutar tu código
   - Qué tecnología/APIs usaste y por qué
   - Principales desafíos encontrados
   - Limitaciones de tu solución
   - **Propuesta de producción:** Cómo llevarías esto a producción y lo automatizarías para procesar 1000+ o 10,000+ PDFs
4. **Presentación breve** (5-7 slides en PowerPoint/PDF):
   - Qué hiciste
   - Cómo lo hiciste
   - Resultados obtenidos
   - **Arquitectura para producción:** Propuesta de cómo escalar esto (arquitectura, automatización, costos a escala)

---

## Tecnología - Usa lo que quieras

**Eres libre de usar cualquier herramienta o tecnología que tengas disponible.** 

Los siguientes enfoques son **sugerencias**, no requisitos. Usa lo que mejor conozcas o lo que tengas a tu disposición:

### Enfoque 1: Extracción Tradicional
- **Parsing de PDFs:** PyPDF2, pdfplumber, PyMuPDF, pdfminer.six
- **Procesamiento:** Regex, Pandas, spaCy, NLTK
- **Tablas:** Tabula-py, Camelot
- ✅ Gratis, control total

### Enfoque 2: LLMs y APIs
- **APIs Comerciales:** 
  - OpenAI (GPT-4, GPT-4o)
  - Anthropic (Claude 3.5 Sonnet, Claude 3 Opus)
  - Google (Gemini Pro, Gemini Flash)
  - DeepSeek (modelos R1, V3)
  - Mistral AI
  - Cohere
- **APIs Cloud para Documentos:**
  - Azure Document Intelligence
  - AWS Textract
  - Google Document AI
- **Frameworks:** LangChain, LlamaIndex, Haystack
- ⚠️ Requiere API keys, tiene costo

### Enfoque 3: Modelos Open Source (Local)
- **Modelos locales:** Llama 3, Mistral, Qwen, Phi
- **Herramientas:** Ollama, LM Studio, vLLM
- ✅ Gratis, sin límites, privado
- ⚠️ Requiere buenos recursos (GPU recomendada)

### Enfoque 4: Híbrido
- Combina parsing tradicional + LLMs para partes complejas
- ✅ Balance entre costo y precisión

**Lo importante es que funcione y puedas explicar por qué elegiste ese enfoque.**

---

## Criterios de Evaluación

| Criterio | Descripción |
|----------|-------------|
| **Funcionalidad** | ¿Funciona? ¿Extrae datos correctamente? |
| **Código** | Código limpio, organizado, comentado |
| **Documentación** | README claro con instrucciones |
| **Visión de producción** | ¿Cómo llevarías esto a producción? ¿Cómo escalarías a miles de PDFs? |
| **Presentación** | Comunicación clara de tu solución |

---

## Formato de Entrega

Envía un repositorio Git (GitHub preferido) o ZIP con:

```
proyecto/
├── data/              # PDFs (ya incluidos)
├── src/               # Tu código
├── output/            # Datos extraídos (JSON/CSV)
├── README.md          # Documentación
├── presentacion.pdf   # Slides
└── requirements.txt   # Dependencias
```

---

## Preguntas Frecuentes

**P: ¿Debo procesar los 5 PDFs?**  
R: Con 2-3 está bien. Si logras los 5, mejor.

**P: ¿Puedo usar APIs de pago (OpenAI, Claude)?**  
R: Sí, solo menciona el costo aproximado en tu README.

**P: ¿Qué pasa si no logro extraer todo perfectamente?**  
R: Está bien. Documenta las limitaciones y explica cómo lo mejorarías.

**P: ¿Necesito tests unitarios?**  
R: No es obligatorio, pero suma puntos.

**P: ¿Debo proponer una arquitectura de producción?**  
R: Sí, es importante. Explica cómo automatizarías esto y lo escalarías para procesar 1,000 o 10,000 PDFs. Piensa en:
   - ¿Cómo orquestarías el proceso?
   - ¿Qué servicios de cloud usarías?
   - ¿Cómo manejarías errores y reintentos?
   - ¿Cómo monitorearías el sistema?
   - ¿Cuál sería el costo a esa escala?

---

## Notas Finales

- No esperamos perfección en 2 días
- Muestra tu proceso de pensamiento
- La documentación es tan importante como el código
- **La propuesta de producción/escalabilidad es clave** - muestra que piensas en sistemas reales
- Prepara tu presentación para explicar tu trabajo

---

**¡Buena suerte! Esperamos ver tu solución.**

**Contacto para preguntas:**  
ogaspar@oceloteminerals.com

**Fecha límite de entrega:**  
2 días desde que recibes este test
