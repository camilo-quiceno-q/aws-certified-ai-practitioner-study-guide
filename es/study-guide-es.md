# AWS Certified AI Practitioner AIF-C01

# Exam

## Perfil y requisitos del candidato

- **Nivel Inicial:** Esta es una certificación de nivel **Foundational** , lo que significa que está diseñada para personas que desean demostrar un conocimiento básico de IA y las herramientas de AWS, sin necesidad de experiencia profunda.
- **Experiencia recomendada:** Se sugiere tener hasta 6 meses de exposición a las tecnologías de IA y ML en AWS. Aunque no es obligatorio, se recomienda obtener primero la certificación Cloud Practitioner, ya que muchos de esos conceptos de infraestructura se dan por sentados.
- **Lo que NO necesitas:** El examen no requiere que sepas programar algoritmos, realizar análisis matemáticos complejos, ingeniería de datos avanzada o diagramación técnica. El enfoque es el uso de servicios administrados, no el desarrollo de código desde cero.

## Estructura y logística del examen

- **Formato:** Consta de 65 preguntas en total, 50 tienen puntaje y 15 son experimentales.
- **Tipos de preguntas:** Incluye opción múltiple, respuesta múltiple, ordenación, emparejamiento y estudios de caso.
- **Tiempo y costo:** Tendrás 90 minutos para completar el examen, el cual tiene un costo de $100 USD.
- **Puntaje de aprobación:** Debes obtener al menos 700 de un máximo de 1.000 puntos.

## Dominios de contenido

El examen se divide en cinco áreas principales, destacando que **más de la mitad del examen se centra en IA generativa.**

1. **Fundamentos de IA y ML (20%):** Conceptos básicos, tipos de aprendizaje (supervisado, no supervisado, por refuerzo) y ciclo de vida de ML
2. **Fundamentos de IA Generativa (24%):** Conceptos de GenAI, transformadores y modelos multimodales.
3. **Aplicaciones de Modelos Fundacionales (28%):** Ingeniería de peticiones, entrenamiento continuo y RAG
4. **Pautas para una IA responsable (14%):** Sesgo, equidad, explicabilidad y transparencia
5. **Seguridad, cumplimiento y gobernanza (14%):** Protección de sistemas de IA y normativas de AWS.

## Herramientas clave de AWS

Debes familiarizarte con los casos de uso de los siguientes servicios principales:

- **Amazon SageMaker:** Para construir, entrenar y desplegar modelos
- **Amazon Bedrock:** Para trabajar con modelos fundacionales e IA generativa.
- **Servicios de IA específicos:** Comprehend, Rekognition, Transcribe, Polly y Lex

## Consejos de estudios

- **Tiempo de preparación:** Se estima que un principiante necesita unas 20 horas de estudio mientras que alguien con experiencia podría requerir solo 5 horas.
- **Estrategia de asociación:** Una técnica efectiva es crear tarjetas de memoria para asociar cada servicio de AWS con su función principal.

# Study Book

## **Aspectos básicos de la IA y el ML**

### **Terminología y conceptos básicos de la IA**

#### Definiciones Fundamentales

- **Inteligencia Artificial (IA):** Es un campo amplio que busca crear sistemas informáticos con capacidades de resolución de problemas similares a las humanas. Su objetivo es **simular** la inteligencia humana para realizar tareas como reconocer imágenes, escribir poemas o tomar decisiones.
- **Machine Learning (ML):** Es un subconjunto de la IA que otorga a las computadoras la capacidad de aprender a partir de datos sin ser programadas explícitamente para cada paso. Los algoritmos de ML identifican patrones en los datos para realizar predicciones o clasificaciones.
- **Aprendizaje Profundo (Deep Learning):** Es una evolución avanzada del ML que utiliza redes neuronales artificiales con múltiples capas para procesar datos complejos como audio, imágenes y lenguaje natural.

#### Componentes y Tecnologías Específicas

- **Redes Neuronales:** Son modelos computacionales inspirados en la estructura del cerebro humano, compuestos por nodos interconectados y organizados por capas: entrada, oculta y salida. Las conexiones entre estas neuronas tienen pesos numéricos que el modelo ajusta para aprender patrones.
- **Visión Artificial:** Es el campo de la IA que permite a las máquinas **ver** e interpretar información visual del mundo real. El servicio clave en AWS para esto es **Amazon Rekognition,** que identifica objetos, personas, escenas y actividades en imágenes y videos.
- **Procesamiento de lenguaje natural (NLP):** Tecnología que permite a las computadoras entender, interpretar y generar lenguaje humano, ya sea texto o voz. Se utiliza en chatbots, traducción y análisis de sentimientos. AWS ofrece servicios como:
    - **Amazon Comprehend:** Extracción de información
    - **Amazon Translate:** Traducción
    - **Amazon Lex:** Chatbots

#### Training y Inferencia

- **Entrenamiento:** Es la fase en la se alimenta al algoritmo con datos históricos para que aprenda a detectar patrones. Una buena práctica es dividir los datos en grupos de entrenamiento, validación y prueba
- **Inferencia:** Es el acto de utilizar el modelo ya entrenado para solicitar y obtener una predicción basada en datos nuevos. Existen dos tipos principales:
    - **En tiempo real:** Respuestas instantáneas, como un chatbot
    - **Por lotes:** Procesa grandes grupos de datos de una sola vez, ideal para reportes.

#### Sesgo y Equidad

- **Sesgos (Bias):** Ocurre cuando un sistema de IA favorece injustamente a un grupo o individuo, generalmente debido a que los datos de entrenamiento estaban desequilibrados o eran incompletos.
- **Equidad (Fairness):** Es el principio ético de garantizar que los sistemas de IA tomen decisiones imparciales y no discriminen por atributos como raza, género o nivel socioeconómico.
- **Herramientas de AWS: Amazon SageMaker Clarify** es el servicio diseñado para detectar sesgos en los datos y modelos, además de proporcionar explicabilidad sobre cómo el modelo toma sus decisiones.

### Tipos de Aprendizaje

#### Aprendizaje Supervisado

Es el tipo de aprendizaje donde el modelo se entrena utilizando **datos etiquetados,** lo que significa que cada entrada de datos viene acompañada de la respuesta correcta. Se puede comparar con un estudiante que aprende bajo la guía de un profesor.

Este se divide en dos tareas principales:

- **Clasificación:** El objetivo es asignar datos a **categorías o clases predefinidas**. El modelo identifica patrones para etiquetar nuevos ejemplos en grupos discretos.
    - Ejemplos: Detección de correos spam (si/no), diagnóstico médico, reconocimiento de imágenes y evaluación de riesgo crediticio (bajo/alto)
- **Regresión:** Se utiliza para **predecir valores numéricos continuos** en lugar de categorías. Analiza la relación entre variables para realizar pronósticos.
    - Ejemplos: Predicción de precios de viviendas, tendencias del mercado de valores, cálculo de la esperanza de vida o pronósticos de temperatura.

#### Aprendizaje No Supervisado

En este método, el modelo se entrena con **datos sin etiquetar**. No hay “respuesta correcta” previa; el algoritmo debe descubrir por sí solo patrones, estructuras o relaciones ocultas dentro de los datos.

Sus enfoques principales son:

- **Clustering:** Agrupa puntos de datos basados en sus similitudes utilizando técnicas de medición de distancia.
    - Ejemplo: Segmentación de clientes por hábitos de compra para marketing personalizado.
- **Reducción de dimensionalidad:** Es el proceso de reducir el número de variables de entrada en un conjunto de datos, manteniendo la información esencial. Esto ayuda a combatir la maldición de la dimensionalidad y previene el sobreajuste.
- **Asociación:** Busca reglas que describen grandes porciones de datos, como las relaciones entre variables.
    - Ejemplo: Si un cliente compra pan, es probable que compre mantequilla

#### Aprendizaje por Refuerzo

Este tipo de aprendizaje no se basa en datos estáticos, sino en un agente que interactúa con un entorno. El agente aprende mediante un proceso de ensayo y error, recibiendo recompensas por acciones correctas y castigos por las incorrectas.

- **Mecanismos:** El objetivo del agente es maximizar la recompensa total acumulada a lo largo del tiempo. Es similar a cómo un humano aprende a montar bicicleta.
- **Casos de Uso:** Videojuegos, navegación de robots y vehículos autónomos que deben decidir en tiempo real cómo girar o frenar.
- **AWS Highlight:** El servicio **AWS DeepRacer** utiliza aprendizaje por refuerzo para entrenar coches de carreras autónomos en un simulador 3D.

| **Tipo de Aprendizaje** | **Datos** | **Objetivo Principal** | **Concepto Clave** |
| --- | --- | --- | --- |
| **Supervised** | Etiquetados | Predecir categorías o números | Guía/Profesor |
| **Unsupervised** | Sin etiquetar | Hallar estructuras o reducir datos | Explorador/Independiente |
| **Por Refuerzo** | Sin datos previos | Aprender decisiones óptimas | Recompensa/Castigo |

### Tipos de datos en IA

#### Datos etiquetados vs Datos sin etiquetar

- **Datos etiquetados:** Son muestras de datos que ya incluyen la respuesta correcta o una descripción (ejemplo: correos marcados como “spam” o “no spam”). Estos datos son el requisito previo para el aprendizaje supervisado. In AWS, el servicio diseñado para que humanos identifiquen datos brutos y añadan etiquetas informativas es **Amazon SageMaker Ground Truth.**
- **Datos sin etiquetar:** Consisten en datos brutos que carecen de etiquetas, categorías o etiquetas predefinidas. Se utilizan en el aprendizaje no supervisado para que el modelo descubra estructuras, patrones o agrupaciones por su cuenta.

#### Datos estructurados vs Datos no estructurados

- **Datos estructurados:** Es información organizada en un formato predefinido, típicamente filas y columnas dentro de una hoja de cálculo o base de datos. Para el examen, asocia mentalmente el concepto de tablas y datos estructurados con el servicio de **Amazon Redshift**
- **Datos no estructurados:** Son datos que no tienen formato o estructura fija, lo que dificulta su análisis con métodos tradicionales. Ejemplos claves incluyen imágenes, texto, audio y video. Para procesarlos de manera efectiva, se requieren técnicas avanzadas de IA como el NLP o Visión Artificial.

#### Tipos de datos específicos y sus servicios de AWS

- **Texto:** Se clasifica como dato no estructurado. El servicio de AWS para analizar texto, extraer idea y detectar sentimientos es **Amazon Comprehend**
- **Imágenes:** Son datos no estructurados que requiere visión por computadora para ser interpretados. Debes asociar imágenes y video con el servicio **Amazon Rekognition,** que identifica objetos, personas y escenas.
- **Series temporales:** Son valores recogidos de forma continua a lo largo del tiempo, como los precios de las acciones o la temperatura por hora. La nota mental crítica para el examen es asociar la predicción de tendencias en series temporales con **Amazon Forecast.**
- **Documentos escaneados:** Aunque contiene texto e imágenes, su extracción de datos se realiza con **Amazon Textract**

### **Ciclo de vida de desarrollo del ML**

#### Recopilación de datos

- **Propósito:** Reunir datos relevantes y de alta calidad desde diversas fuentes para que el modelo pueda aprender patrones.
- **Servicios Clave:** Se utilizan servicios de almacenamiento como **Amazon S3** para centralizar la información, **AWS Glue** para la integración y **AWS Data Lake** para gestionar grandes volúmenes de datos provenientes de múltiples fuentes.
- **Etiquetado:** Si los datos no tienen etiquetas, se utiliza **SageMaker Ground Truth** para que humanos añadan descripciones informativas necesarias para el aprendizaje supervisado.

#### Análisis Exploratorios de Datos

- **Propósitos:** Investigar el conjunto de datos para descubrir estructuras, detectar anomalías y visualizar patrones mediante estadísticas y gráficos.
- **Herramientas:** Se emplean **SageMaker Notebook Instances o SageMaker Studio** que vienen con librería de python preinstaladas como Pandas y Matplotlib para análisis.

#### Procesamiento de datos

- **Propósito:** Limpiar los datos brutos que suelen ser “sucios” (valores faltantes, duplicados, errores o inconsistencias) y normalizarlos para que sean valiosos para el modelo.
- **Asociación rápida**: El servicio principal es **Amazon SageMaker Data Wrangler**, que ofrece más de 300 transformaciones integradas para automatizar este proceso sin necesidad de escribir código complejo.

#### Ingeniería de características

- **Propósito:** Seleccionar, crear o transformar variables de entrada para mejorar significativamente el rendimiento y la capacidad predictiva del modelo.
- **Almacenamiento:** Se utiliza el **SageMaker Feature Store,** un repositorio centralizado para almacenar, compartir y reutilizar características en diferentes proyectos de ML.

#### Entrenamiento y Ajuste de hiperparámetros

- **Entrenamiento:** Consiste en alimentar al algoritmo con datos históricos (usualmente el 70-80% del conjunto total) para que aprenda patrones.
- **Ajuste de hiperparámetros:** Los hiperparámetros son configuraciones externas (como la **tasa de aprendizaje, el tamaño del lote o las épocas)** que deben definirse antes del entrenamiento para controlar cómo aprende el modelo.
- **Optimización: SageMaker Automatic Model Tuning** ejecuta múltiples trabajos de entrenamiento probando diferentes rangos de hiperparámetros para encontrar la versión que mejor rinda.

#### Evaluación

- **Propósito:** Determinar la precisión del modelo utilizando datos que no vio durante el entrenamiento para asegurar que generalice bien en el mundo real
- **Métricas críticas:**
    - **Clasificación:**
        - Exactitud
        - Precisión
        - Sensibilidad
        - F1 Score
    - **Regresión:**
        - Error Cuadrático Medio
        - Raíz del Error Cuadrático Medio
    - **Generative:**
        - ROUGE
        - BLEU
        - BERTScore

#### Implementación

- **Propósito:** Publicar el modelo entrenado como un endpoint para que las aplicaciones puedan consultarlo
- **Modos de Inferencia:**
    - Tiempo real: Para respuestas instantáneas
    - Por lotes: Procesa grandes grupos de datos de forma asíncrona cuando la respuesta inmediata no es crítica

#### Monitoreo

- **Propósito:** Vigilar el rendimiento del modelo en prod para detectar **Drift** que ocurre cuando el modelo pierde precisión debido a cambios en los datos del mundo real con el tiempo
- **Servicio Clave: Amazon SageMaker Model Monitor** detecta automáticamente la deriva de datos, deriva de calidad y sesgos, emitiendo alertas para decidir si el modelo necesita ser reentrenado.

### Métricas de Rendimiento y Negocio

#### Métricas de Rendimiento del Modelo

**Clasificación (Métricas Críticas)**

- **Accuracy (Exactitud):** Se calcula como el número de predicciones correctas dividido por el número total de predicciones.
    - **Nota:** Puede ser engañosa si el conjunto de datos está desequilibrado. Un modelo podría tener alta exactitud simplemente prediciendo siempre la clase más frecuente, ignorando la minoritaria.
- **Precisión (Precision):** Mide la calidad de las predicciones positivas. Responde a: *"De todos los casos que el modelo marcó como positivos, ¿cuántos lo eran realmente?"* Es vital cuando el costo de un **falso positivo** es alto (ej. marcar un correo legítimo como spam).
- **Sensibilidad (Recall):** Mide la cantidad de casos positivos que el modelo es capaz de identificar. Responde a: *"De todos los casos positivos reales, ¿cuántos logró atrapar el modelo?"* Es crítica cuando no podemos permitirnos **falsos negativos** (ej. detectar una enfermedad).
- **F1 Score:** Es la media armónica entre la precisión y la sensibilidad.
    - **Uso:** Se utiliza principalmente cuando existe una distribución de clases desigual o cuando se busca un equilibrio saludable entre evitar falsos positivos y falsos negativos.
- **AUC (Área bajo la curva):** Representa la probabilidad de que el modelo clasifique un ejemplo positivo aleatorio por encima de uno negativo aleatorio.
    - **Interpretación:** Un valor de **1.0** indica un rendimiento perfecto, mientras que un **0.5** significa que el modelo no es mejor que el azar.

**Regresión (Métricas Críticas)**

- **Error Cuadrático Medio (MSE):** Promedio de los cuadrados de los errores (diferencia entre el valor real y el predicho).
    - **Características:** Al elevar al cuadrado, penaliza mucho más los errores grandes (outliers) que los pequeños.
- **Raíz del Error Cuadrático Medio (RMSE):** Es la raíz cuadrada del MSE.
    - **Ventaja:** Expresa el error en las mismas unidades que la variable que estamos prediciendo (ej. dólares, metros, grados), lo que facilita mucho su interpretación por parte del negocio.

#### Métricas del Negocio

- **ROI (Retorno de Inversión):** Mide la rentabilidad económica del proyecto. Compara los beneficios financieros generados (ahorros o ganancias extras) frente a la inversión total en desarrollo, infraestructura y despliegue del modelo.
- **Satisfacción del Cliente:** Evalúa el impacto directo de la solución de IA en la experiencia del usuario final:
    - **NPS (Net Promoter Score):** Escala de 0 a 10 que mide la lealtad del cliente basándose en qué tan probable es que recomiende el producto.
    - **Análisis de Sentimiento:** AWS sugiere utilizar **Amazon Comprehend** para categorizar automáticamente comentarios como positivos, negativos, neutros o mixtos. Sirve como un termómetro en tiempo real de la satisfacción del usuario.
- **Métricas Operativas y de Costo:**
    - **Costos de desarrollo:** Inversión inicial en talento humano y adquisición de datos.
    - **Costo por usuario:** Gasto de infraestructura (nube/inferencia) que genera cada usuario activo al interactuar con el modelo.
    - **Opinión general:** Feedback cualitativo recolectado de entrevistas o encuestas directas para entender el valor percibido.

## **Aspectos básicos de la IA generativa**

### **Fundamentos técnicos de GenAI**

#### Tokens

- **Definición:** Es la **unidad básica** de datos que procesan los modelos de procesamiento de lenguaje natural e IA generativa.
- **Escala:** Un token puede representar una palabra completa, una parte de una palabra, un signo de puntuación o incluso un solo carácter.
- **Vocabulario interno:** Durante su entrenamiento, los modelos crean un vocabulario interno de tokens; los modelos más grandes suelen manejar entre 30k and 100k tokens.
- **Capacidad y Costo:** Cada token consume memoria y capacidad de cómputo. En servicios como Amazon Bedrock, el costo se basa frecuentemente en el número de tokens procesados (entrada) y generados (salida).

#### Fragmentación (Chunking)

- **Definición:** Es el proceso de dividir grandes volúmenes de texto o datos en partes más pequeñas y manejables.
- **Propósito:** Es esencial porque los modelos tienen un límite de información que pueden procesar a la vez, conocido como **ventana de contexto**.
- **Aplicación en RAG:** Antes de convertir los datos en representaciones numéricas, el conjunto de datos se fragmenta para que el modelo pueda recuperar información relevante de forma eficiente.
- **Riesgos:** Una fragmentación inadecuada puede causar que el modelo pierda el contexto o la relación entre partes del texto.

#### Embeddings

- **Definición:** Son representaciones vectoriales que capturan el significado semántico y las relaciones entre los datos.
- **Funcionamiento:** Permiten que el modelo analice patrones matemáticamente; por ejemplo, palabras con significados similares tendrán representaciones numéricas cercanas en el espacio vectorial.
- **Creation:** Se generan mediante modelos de ML especializados y sirven como una especie de memoria externa para el sistema

#### Vectores

- **Definición:** En este contexto, un vector es una cadena de números donde cada posición representa una característica o dirección en un espacio matemático.
- **Espacio Vectorial:** Es la estructura matemática multidimensional donde existen estos vectores.
- **Relación:** La distancia entre vectores dentro de este espacio correlaciona la relación entre los datos que representan.

#### Latent Space

- **Concepto:** Es una representación matemática comprimida de los datos donde el modelo captura las características y patrones esenciales.
\n**Resumen de comparación para el examen:**

| **Técnica** | **¿Cambia los pesos del modelo?** | **Tipo de datos** | **Caso de uso principal** |
| --- | --- | --- | --- |
| **Fine-tuning** | Sí | Etiquetados | Cambio de estilo, tono o comportamiento. |
| **RAG** | No | Externos | Datos privados que cambian frecuentemente. |
| **Pre-training continuo** | Sí | No etiquetados | Especialización profunda en un dominio. |
| **Destilación** | Sí (en el estudiante) | Probabilidades | Inferencia rápida en dispositivos móviles. |

### **Bases de datos vectoriales en AWS**

Las bases de datos vectoriales son componentes especializados diseñados para almacenar, gestionar y buscar embeddings vectoriales de alta dimensión de manera eficiente. Estas bases de datos son fundamentales para los sistemas de Generación Aumentada por Recuperación (RAG), ya que permite encontrar elementos similares comparando vectores numéricos en lugar de depender únicamente de coincidencias de palabras clave exactas.

#### Amazon OpenSearch Service

- **Propósito principal:** Es la opción preferida para búsquedas vectoriales a escala masiva
- **Capacidades técnicas:** Basado en la biblioteca **Apache Lucene**, ofrece funcionalidades de búsqueda de texto completo, pero destaca como almacén vectorial por su capacidad de manejar millones de documentos con **Alta concurrencia y baja latencia.**
- **Tipos de búsqueda:** Admite búsqueda de similitud vectorial, K-vecinos más cercanos, búsqueda semántica, búsqueda multimodal, búsqueda híbrida.
- **Variante Serverless:** Existe una oferta de **Amazon OpenSearch Serverless** que se utiliza frecuentemente en flujos de RAG para simplificar la gestión de la infraestructura.

#### Amazon Aurora y Amazon RDS para PostgreSQL

- **Extensión Clave:** Ambos utilizan la **extensión PGvector** para habilitar el soporte de datos vectoriales directamente en una base de datos relacional.
- **Criterio de elección:** Debes elegirlos cuando la aplicación ya reside en un entorno SQL y no se desea agregar complejidad operativa migrando datos a un sistema separado.
- **Ventajas empresariales:** Permite realizar consultas complejas y mantener características de grado empresarial como la conformidad ACID, recuperación de un punto en el tiempo y aislamiento de datos, todo mientras se consultan vectores de alta dimensión.
- **Integración con Bedrock:** Las bases de conocimiento de Amazon Bedrock suelen esperar el uso de RDS o Aurora PostgreSQL como almacén de vectores cuando se requiere una estructura relacional.

#### Amazon Neptune

- **Naturaleza:** Es una base de datos de grafos
- **Diferenciador para RAG:** A diferencia de otros almacenes vectoriales, Neptune puede modelar relaciones complejas entre entidades, no solo similitud semántica simple
- **Casos de uso:** Es ideal para sistemas de conocimiento corporativo donde los documentos están profundamente interconectados y las conexiones entre ellos son tan importantes como el contenido mismo.

#### Amazon Kendra

- **Función:** Aunque se define como motor de búsqueda empresarial inteligente proporciona capacidades de bases de datos vectoriales integradas para soluciones RAG.
- **Ventaja:** Utiliza un sistema RAG avanzado para ofrecer resultados altamente precisos rastreando múltiples fuentes de datos en una organización (como Sharepoint, S3, Slack y Github) de forma nativa.

**Resumen de "Match" rápido para el examen:**

- Si el escenario menciona **escala masiva y alta concurrencia**: Elige **Amazon OpenSearch Service**.
- Si se busca **simplicidad y ya se usa SQL**: Elige **Amazon Aurora o RDS con pgvector**.
- Si se necesita **modelar relaciones entre documentos**: Elige **Amazon Neptune**.
- Si los datos están en **formato JSON** y se quiere compatibilidad con MongoDB: Elige **Amazon DocumentDB** (que también soporta búsqueda vectorial).

### **Ingeniería de peticiones**

Representa una de las formas más eficientes de guiar las respuestas de un modelo sin modificar sus pesos internos.

#### La Anatomía de una Petición

Aunque una petición puede tener cualquier longitud, se divide en cuatro componentes esenciales para maximizar su efectividad:

- **Instrucciones:** Es el componenten obligatorio. Sin una instrucción clara de qué debe hacer, el modelo no podrá procesar la tarea.
- **Contexto:** Información de fondo que ayuda al modelo a entender su rol
- **Datos de entrada:** El contenido específico que quieres que el modelo analice o procese
- **Indicador de salida:** Especifica el formato o estructura deseada para la respuesta.

#### Técnicas Principales de Petición

Debes saber diferenciar estas tres técnicas fundamentales según el nivel de guía que ofrecen al modelo.

- **Zero-shot (Sin ejemplos):** Se proporciona una instrucción directa sin ejemplos adicionales. El modelo confía únicamente en si entrenamiento previo para interpretar la tarea.
- **Few-shot (Con pocos ejemplos):** Se incluyen de a 2 a 5 ejemplos de pares “entrada-salida” antes de la tarea real. Esto ayuda al modelo a identificar patrones específicos, formatos de respuesta o matices técnicos que el modelo base podría omitir.
- **Chain-of-Thought (CoT - Cadena de pensamiento):** Se utiliza para que el modelo descompone problemas complejos en pasos intermedios. Se activa con instrucciones como “Piensa paso a paso”, lo que permite al modelos externalizar su razonamiento, reducir errores y mejorar transparencia.

#### Uso de Plantillas de Peticiones

Las plantillas (Prompt Templates) son estructuras predefinidas y parametrizadas que estandarizan cómo se construye una petición para tareas recurrentes.

- **Beneficios:** Aportan consistencia, eficiencia al reutilizar estructuras y claridad tanto para el usuario como para el modelo.
- **Amazon Bedrock Prompt Management:** Es el servicio de AWS diseñado específicamente para crear, probar y almacenar estas plantillas reutilizables con inyección de variables.

#### Conceptos Técnicos y Riesgos Asociados

Riesgos de seguridad en las peticiones:

- **Espacio Latente (Latent Space):** Es el espacio matemático donde el modelo comprime el conocimiento; una petición bien redactada le indica la dirección correcta para navegar hacia la respuesta precisa:
- **Prompt Injection:** Un ataque donde el usuario intenta sobreescribir las instrucciones originales del sistema.
- **Jailbreaking:** El uso de peticiones creativas o hipotéticas para intentar que el modelo evada sus restricciones éticas o de seguridad.
- **Prompt Leaking:** Ocurre cuando el modelo revela accidentalmente sus instrucciones internas o “system prompts” confidenciales.
- **Model Poisoning:** Inyectar datos maliciosos en la base de conocimientos o en el entrenamiento para corromper las respuestas del modelo.

### **Evaluación del rendimiento**

Es el proceso complejo que busca medir la precisión, la veracidad y la utilidad de las respuestas del modelo para construir confianza con los usuarios.

#### Métricas de Evaluación Estándar

Estas métricas comparan el texto generado por la IA con referencias escritas por humanos.

- **ROUGE (Recall-Oriented Understudy for Gisting Evaluation)**
    - **Uso principal:** Ideal para tareas de resumen de texto
    - **Funcionamiento:** Mide la sensibilidad (recall) basándose en la superposición de n-gramas (secuencias de palabras) entre el contenido generado y los resúmenes de referencia.
    - **Variantes:**
        - **ROUGE N:** Se enfoca en palabras individuales o frases cortas
        - **ROUGE L:** Mide la subsecuencia común más larga, útil para evaluar estructura y coherencia en narrativas largas
    - **Puntuación:** Varía de 0 a 1, donde 1 representa una coincidencia perfecta con la referencia.
- **BLEU (Bilingual Evaluation Understudy):**
    - **Uso Principal:** Estándar para evaluar la calidad de la traducción automática.
    - **Funcionamiento:** Mide la precisión, calculando cuántos n-gramas generados aparecen en la referencia humana y promediándolos.
    - **Penalización por brevedad:** BLEU penaliza las salidas demasiado cortas para asegurar que el modelo no sacrifique contenido esencial solo para coincidir con términos clave.
    - **Puntuación:** Varía de 0 a 1, donde 1 representa una coincidencia perfecta con la referencia.
- **BERTScore:**
    - **Diferencia clave:** A diferencia de ROUGE y BLEU, que se basan en coincidencias de palabras exactas, BERTScore evalúa la similitud semántica.
    - **Mecanismo:** Utiliza incorporaciones vectoriales y un modelo de lenguaje para comparar tokens; así reconoce que frases con palabras diferentes pero el mismo significado son equivalentes.
    - **Ventaja:** Ofrece una visión más matizada de la calidad del texto al no depender de la coincidencia literal de palabras.

#### Evaluación Humana

Es indispensable porque evalúa aspectos subjetivos que las métricas no pueden captar, como la experiencia del usuario, la creatividad y el comportamiento ético.

- **Áreas de enfoque:**
    - **Satisfacción del usuario:** Se utiliza frecuentemente el Net Promoter Score una escala del 0 al 10.
    - **Adecuación contextual:** Determina si el modelo entiende la pregunta y se mantiene en el tema.
    - **Inteligencia emocional:** Juzga si el FM detecta y responde apropiadamente a tonos de frustración o tristeza.
- **Métodos:** Se realiza mediante paneles de expertos, grupos focales o retroalimentación pasiva integrada en el chat

#### Conjuntos de Datos de Referencia

Permiten realizar una evaluación cuantitativa del rendimiento del FM frente a estándares acordados de la industria.

- **Factores que miden:** Exactitud, velocidad/eficiencia, escalabilidad, robustez y generalización.
- **Benchmarks comunes mencionados:**
    - **MMLU**: Para conocimiento general en múltiples dominios.
    - **HumanEval**: Específicamente para capacidades de programación.
    - **TruthfulQA**: Evalúa qué tan honesto es el modelo.
- **Proceso de creación:** Expertos en la materia crean preguntas desafiantes y respuestas de referencia de alta calidad; luego, un modelo juez compara las respuestas contra estas referencias

#### Herramientas de AWS para la Evaluación

- **Amazon Bedrock Model Evaluation:** Servicio integrado que permite ejecutar evaluaciones automáticas (precisión, robustez y toxicidad) o evaluaciones con revisores directamente en consola.
- **FMEval:** Biblioteca de código abierto de AWS para evaluar LLMs y ayudar a seleccionar el mejor modelo según el caso de uso. Contiene algoritmos para medir precisión, toxicidad y robustez semántica.

### **Agentes de IA**

Los agentes de la IA representan una evolución crucial dentro de las aplicaciones de modelos fundacionales, **permitiendo pasar de simples respuestas de texto a la ejecución de acciones.**

#### Concepto de la IA Agéntica

La IA agéntica se refiere a modelos de IA de próxima generación que pueden adoptar un enfoque de múltiples pasos para resolver problemas, actuando de forma autónoma o casi autónoma mediante el uso de herramientas. Al contrario de un modelo de lenguaje estándar que solo genera texto, un agente tiene la capacidad de **planificar, decidir y ejecutar** acciones para completar una tarea compleja. Un agente posee su propia agencia, lo que significa que puede determinar contextualmente qué herramientas o bases de conocimientos necesita consultar sin que se le indique explícitamente cada paso.

#### Agents for Amazon Bedrock

Este servicio proporciona una experiencia de bajo código o sin código para crear flujos de trabajo agénticos que automatizan tareas empresariales. Los agentes orquestan las interacciones entre los modelos fundacionales, las APIs y las fuentes de datos de la organización.

#### Componentes y Flujo de Trabajo

- **Selección del Modelo:** Se elige un FM apropiado que servirá como el “cerebro” del agente.
- **Instrucciones:** Se define el rol y el objetivo del agente utilizando lenguaje natural.
- **Grupos de Acción:** Son las manos del agente. Permiten que el sistema invoque funciones lambda de AWS o realice llamadas a APIs externas mediante esquemas OpenAPI para ejecutar lógica de negocio, como procesar un pedido o consultar el clima.
- **Bases de Conocimiento:** El agente puede integrarse con RAG para consultar documentos privados y dar respuestas precisas basadas en datos reales.
- **Trazabilidad:** Una característica clave es la capacidad de obtener trazas, que permiten el razonamiento paso a paso del agente y entender por qué decidió realizar una acción específica

#### Colaboración Multiagente y Memoria

Amazon Bedrock permite colaboración multiagente, donde varios agentes especializados colaboran para resolver un problema complejo. Por Ejemplo, un “Agente de Intención” puede clasificar una duda, un agente de recuperación buscar la información y un agente de análisis de sentimiento decidir si escalar el caso a un humano. Además, los agentes pueden utilizar la memoria para retener el contexto de las interacciones anteriores dentro de una misma sesión, mejorar la coherencia y el razonamiento a lo largo de la conversación.

#### Model Context Protocol (MCP)

El MCP es un estándar abierto mencionado como el enchufe universal para la IA. Su propósito es facilitar la integración entre agentes y herramientas externas sin necesidad de escribir código de integración personalizado para cada herramienta, reduciendo drásticamente el esfuerzo técnico.

**Nota:** Los agentes se diferencian de herramientas como LangChain o LlamaIndex en que los agentes deciden autónomamente la ruta a seguir, mientras que en los otros marcos el desarrollador suele definir explícitamente las tuberías y rutas de lógica.

## **Pautas para una IA responsable**

### **Características de la IA responsable**

La IA responsable es un marco diseñado para desarrollar y desplegar sistemas de IA de manera segura, confiable y ética.

#### Equidad (Fairness)

- **Definición:** Los sistemas de IA deben tomar **decisiones imparciales** y no discriminar individuos o grupos por atributos sensibles como raza, género, edad o nivel socioeconómico.
    
    **Nota:** Incluso si no se utilizan datos específicos (como el género), un modelo puede ser injusto si utiliza datos relacionados que lleven al mismo resultado sesgado. La equidad ayuda a fomentar la inclusión y la confianza del usuario.
    

#### **Inclusividad (Inclusivity)**

- **Definición:** Esta característica va un paso más allá de la equidad; el sistema debe estar diseñado para ser accesible y funcionar correctamente para todos los usuarios.
- **Alcance:** Esto incluye a personas con discapacidades, diferentes idiomas o diversos contextos culturales. En el diseño centrado en el ser humano, esto significa crear herramientas que sean inclusivas desde su origen.

#### Solidez (Robustness)

- **Definición:** Es la capacidad de un sistema de IA para mantener un **rendimiento constante y fiable** frente a variaciones de los datos de entrada o condiciones inesperadas.
- **Resiliencia:** Un sistema robusto debe ser capaz de manejar datos incompletos, anomalías o incluso ataques adversarios deliberados sin comprometer la calidad de su salida.

#### Seguridad (Safety)

- **Definición:** Implica operar sistemas de IA que realicen sus funciones previstas sin causar daño a los seres humanos o al medio ambiente.
- **Prevención:** Se centra en mitigar comportamientos no deseados, sesgos algorítmicos peligrosos y el uso indebido del sistema. Requiere pruebas rigurosas y mecanismos de supervisión para evitar fallos de funcionamiento.

#### Veracidad (Veracity)

- **Definición:** Se refiere a la veracidad y exactitud de las salidas generadas por la IA.
- **Mitigación de riesgos**: El sistema debe evitar fabricar información (Alucinaciones) y ser honesto sobre lo que sabe. En campos críticos como la salud o las finanzas, la veracidad es esencial para la fiabilidad del modelo.

#### Sostenibilidad (Sustainability)

- **Definición:** Se refiere al desarrollo de la tecnología de IA que sea viable a largo plazo, minimizando activamente el daño ecológico.
- **Eficiencia energética:** Un enfoque responsable implica optimizar las arquitecturas de los modelos para reducir el consumo de energía durante el entrenamiento y la inferencia.
    
    **TIP:** Al comparar modelos con rendimiento similar, elegir el más pequeño y eficiente es una práctica de IA responsable por su menor huella ambiental
    

#### Otras características

- **Transparencia:** Compartir información abierta sobre el diseño del sistema, las fuentes de datos y su funcionamiento general.
- **Explicabilidad (Explainability):** La capacidad de proporcionar razones comprensibles para decisiones o predicciones específicas, “abriendo” la caja negra de los modelos complejos.
- **Privacidad:** Garantizar que los datos de los individuos estén protegidos y que estos mantengan el control sobre cómo se utiliza su información.

### Riesgos Legales y Éticos

Dentro del dominio de IA responsable, es fundamental que comprendas que el desarrollo de sistemas éticos no es solo una cuestión técnica, sino una estrategia integral para mitigar riesgos legales, sociales y de reputación.

#### Infracción de propiedad intelectual (IP)

Este es uno de los riesgos legales más críticos desde el lanzamiento de modelos masivos.

- **El Riesgo:** Los modelos se entrenan con datos masivos de internet y pueden generar contenido que se parezcan demasiado a obras protegidas por derechos de autor sin proporcionar atribución o compensación justa.
- **Consecuencias:** Demandas legales por el uso de artículos o creaciones sin permiso.
- **Mitigación:** Las empresas están abordando esto mediante acuerdos de licencias con proveedores de contenido y ofreciendo protección de indemnización.
\n#### Toxicidad

- **Definición:** Instancias donde un modelo generativo produce una respuesta falsa, engañosa o sin sentido, pero que suena convincente y profesional.
- **Causa:** Se deben principalmente a las limitaciones de los datos de entrenamiento y a que los modelos operan basándose en predicciones probabilísticas en lugar de en hechos reales.
- **Mitigación:** Para el examen recuerdas las mejores formas de reducir alucinaciones es con la Generación Aumentada de Recuperación (RAG), el ajuste fino y una ingeniería de peticiones cuidadosa.

#### Plagio y Trampas

- **Impacto Educativo:** El uso de IA para escribir ensayos, completar tareas o responder exámenes sin esfuerzo genuino plantea serios problemas de integridad académica y equidad.
- **Dificultad de Detección:** Es extremadamente difícil detectar el contenido generado por IA de forma fiable, ya que las herramientas suelen dar falsos positivos y los usuarios pueden reescribir el contenido para evadir filtros.
- **Enfoque Responsable:** AWS sugiere que la IA responsable debe fomentar la transparencia y el uso de pautas éticas que desalienten el uso indebido en entornos de aprendizaje.

#### Pérdida de confianza

- **El Riesgo:** Si los clientes descubren que la IA de una empresa genera información falsa, sesgada o discriminatoria, el daño reputacional puede ser enorme y difícil de recuperar.
- **Impacto en el negocio:** La confianza es un motor de adopción; cuando los usuarios creen que un sistema es justo y seguro, se sienten más inclinados a utilizarlo.
- **Mitigación:** Mantener una transparencia total sobre el diseño del sistema, sus limitaciones y los datos que utiliza.

| **Riesgo** | **Concepto Clave** | **Mitigación Principal** |
| --- | --- | --- |
| **Propiedad Intelectual** | Uso de datos con copyright sin permiso. | Acuerdos de licencia e indemnización. |
| **Toxicidad** | Contenido ofensivo o dañino. | Amazon Bedrock Guardrails. |
| **Alucinaciones** | Información falsa que parece real. | RAG y Fine-tuning. |
| **Plagio** | Bypass de esfuerzo académico genuino. | Fomentar la integridad académica. |
| **Pérdida de confianza** | Daño a la marca por errores o sesgos. | Transparencia (Model Cards). |

### Transparencia y explicabilidad

El reconocimiento de la importancia de los modelos transparentes y explicables es un pilar fundamental para construir sistemas éticos y confiables.

#### Transparencia vs Explicabilidad

Aunque están relacionados, estos conceptos sirven para propósitos distintos.

- **Transparencia:** Se refiere a la apertura general sobre el diseño del sistema, las fuentes de datos utilizadas para el entrenamiento, los objetivos del modelo y sus limitaciones.
- **Explicabilidad:** Se centra en proporcionar razones comprensibles para decisiones o predicciones individuales específicas tomadas por la IA

#### Diferencias entre Modelos Transparentes y Opacos

- **Modelos Transparentes e Interpretables:** Son modelos más simples, como la regresión lineal o los árboles de decisión, donde las reglas con claras y permiten una auditoría directa del razonamiento lógico.
- **Modelos Opacos (Caja Negra):** Son sistemas altamente complejos como las redes neuronales profundas. Aunque ofrecen un rendimiento y precisión superiores, su lógica interna es extremadamente difícil de descifrar incluso para sus creadores
- **Compensación (Trade-off):** Existe una relación de compromiso donde los modelos más potentes suelen ser menos interpretables, mientras que los modelos más explicables pueden no ser tan precisos en tareas complejas.

#### Herramientas de AWS para Transparencia

- **SageMaker Model Cards:** Es la herramienta principal para documentar los detalles del modelo, métricas de entrenamiento, evaluaciones de rendimiento y limitaciones, actuando como una ficha técnica que fomenta la transparencia.
- **Modelos de Código Abierto:** Favorecen la transparencia ya que su arquitectura y, a menudo, sus datos de entrenamientos son públicos y auditables.
- **SageMaker Clarify:** Proporciona detalles sobre la toma de decisiones, identificando qué características influyen más en las respuestas del modelo.

#### Principios de Diseño Centrado en el Ser Humano (HCD)

El HCD busca que la tecnología se cree pensando en el usuario final, priorizando la usabilidad y la justicia. Sus principios clave son:

- **Claridad:** Presentar la información de forma sencilla, sin jerga técnica innecesaria.
- **Simplicidad:** Eliminar puntos de datos innecesarios y resaltar solo lo más relevante para la decisión
- **Usabilidad:** Crear interfaces intuitivas que puedan ser navegadas tanto por usuarios técnicos como no técnicos.
- **Reflexividad:** Diseñar herramientas que inciten al usuario a pensar críticamente sobre la decisión de la IA
- **Responsabilidad:** Debe haber una propiedad humana clara sobre las decisiones asistidas por IA; el profesional humano sigue siendo el responsable al final.
- **Personalización:** Adaptar la experiencia y el tono a las necesidades o el estilo de interacción del usuario.
- **Aprendizaje Cognitivo:** Los sistemas deben aprender de los usuarios expertos a través de ejemplos y correcciones.
- **Herramientas centradas en el usuario:** Garantizar que los sistemas sean inclusivos y accesibles para personas con discapacidades o conocimientos limitados de IA.

### Herramientas de AWS para responsabilidad

#### Amazon Bedrock Guardrails

Esta herramienta actúa como una **capa de moderación de contenido** que analiza tanto los prompts enviados por los usuarios como las respuestas generadas por los FM

- **Funciones Principales:** Permite filtrar contenido dañino, redactar o bloquear información de identificación personal como nombres o números de seguridad social, y aplicar políticas de privacidad personalizadas utilizando lenguaje natural.
- **Contexto de uso:** Es ideal para asegurar que los agentes de IA y los chatbots mantengan dentro de los límites éticos y de marca de la organización.
- **Evaluación y pruebas:** Incluye un entorno de prueba para simular entradas y ajustar los filtros antes de desplegarlos en producción

#### Amazon SageMaker Clarify

Es la herramienta principal para la IA explicable y la detección de desigualdades.

- **Detección de sesgos:** Analiza los datos y los modelos para identificar sesgos o prejuicios tanto antes como después del entrenamiento.
- **Explicabilidad:** Proporciona informes detallados que explican qué características o variables tuvieron más influencia de la decisión final del modelo, utilizando algoritmos avanzados como SHAP
- **Gobernanza:** Ayuda a cumplir con regulaciones que exigen transparencia sobre por qué un sistema de IA tomó una decisión específica

#### Amazon SageMaker Model Monitor

Esta herramienta está diseñada para la fase de monitoreo continuo una vez que el modelo ya está en producción

- **Detección de deriva (Drift):** Identifica automáticamente cuándo la precisión de un modelo comienza a degradarse debido a cambios en los datos del mundo real.
- **Tipos de monitoreo:** Detecta deriva en la calidad de los datos, deriva en la calidad del modelo, y deriva en el sesgo o atribución de características
- **Automatización:** Emite alertas basadas en umbrales de rendimiento definidos para que los equipos decidan cuando es necesario reentrenar el modelo.

#### Amazon Augmented AI (Amazon A2I)

Representa el concepto de “humano en el bucle”, permitiendo la supervisión humana en procesos de decisión automatizados.

- **Activación por confianza:** Se puede configurar para que, cuando el modelo tenga una predicción de baja confianza, la respuesta sea enviada automáticamente a un revisor humano para garantizar precisión.
- **Casos de uso:** Es crítico en tareas donde los errores son inaceptables, como la moderación de contenido sensible, extracción de datos de documentos legales o traducciones complejas.
- **Fuerza de trabajo:** Soporta equipos privados de revisores, proveedores externos de AWS Marketplace o el acceso a una fuerza laboral global mediante Amazon Mechanical Turk
- **Diferencia clave:** A diferencia de SageMaker Ground Truth (que es para etiquetar datos iniciales), **A2I es para revisar la calidad de las predicciones** de un modelo ya entrenado.

### Gobernanza y documentación

#### Amazon SageMaker Model Cards

Las **Tarjetas de modelos** son el marco de documentación estándar de AWS diseñado para gestionar y gobernar modelos de ML de forma ética y transparente.

- **¿Qué son?:** Actúan como una ficha técnica que centraliza toda la información crítica sobre el diseño, entrenamiento y limitaciones de un modelo.
- **¿Qué incluye?**
    - **Detalles del modelo:** Propósito y objetivos
    - **Casos de uso previstos:** Para qué tareas es apropiado el modelo y para cuáles no.
    - **Métricas de entrenamiento y evaluaciones:** Detalles técnicos del rendimiento y resultados de benchmarks
    - **Evaluaciones de riesgos y sesgos:** Documentación de riesgos conocidos o limitaciones éticas identificadas durante el desarrollo
    - **Historial de implementación:** Dónde y cómo se ha desplegado el modelo.
- **Beneficio Principal:** Facilitan la transparencia y auditoría tanto para equipos internos como para reguladores externos, ayudando a generar confianza en los usuarios finales.

**Nota:** Los modelos entrenados directamente en Amazon SageMaker pueden autopoblar automáticamente gran parte de la información de estas tarjetas, facilitando el cumplimiento de la gobernanza

#### Linaje de Datos

El linaje de datos es el registro histórico completo que rastrea el origen, el movimiento, las transformaciones y el uso de la información a lo largo de todo su ciclo de vida.

- **Importancia en IA Responsable:** Es fundamental la trazabilidad. Si un modelo toma una decisión incorrecta o muestra un sesgo, el linaje permite investigar exactamente con qué datos fue entrenado y de dónde vinieron esos datos.
- **Componentes de la documentación del origen:** Según AWS para una gobernanza robusta se debe documentar:
    - **Citación de fuentes:** Acreditar adecuadamente de dónde provienen los datos y capturar las licencias o términos de uso asociados.
    - **Origen de datos:** Registrar cómo y dónde se recolectaron, y cómo fueron curados, limpiados y transformados antes de llegar al modelo.
- **Catalogación de datos:** Este proceso organiza los conjuntos de datos, modelos y recursos de forma sistemática (como una biblioteca), facilitando su auditoría y gestión interna.

# **Seguridad, cumplimiento y gobernanza**

---

### Protección de sistema de IA

#### Modelo de Responsabilidad Compartida

Este marco define la división de tareas de seguridad entre AWS y tú:

- **AWS es responsable de la seguridad de la nube:** Esto incluye la protección de la infraestructura global, el hardware y el software básico.
- **Tú eres responsable de la seguridad en la nube:** Debes asegurar tus datos, gestionar las identidades IAM, configurar el cifrado y proteger tus aplicaciones.

#### IAM (Roles y Políticas)

AWS Identity and Access Management es el servicio central para controlar el acceso a los recursos de IA.

- **Principio de mínimo privilegio:** Solo debes otorgar los permisos estrictamente necesarios para realizar una tarea, reduciendo el riesgo de uso indebido accidental o malicioso.
- **Roles IAM:** Son identidades que no tienen credenciales permanentes. Debes crear roles distintos para las cargas de trabajo de entrenamiento, inferencia y monitoreo.
- **Políticas:** Documentos en formato JSON que definen permisos, Pueden estar basadas en la identidad (asignadas a usuarios o roles) o basadas en recursos

#### Cifrado y AWS KMS

- **Datos en reposo:** Debes usar KMS para cifrar los conjuntos de datos de entrenamiento en S3, los artefactos de los modelos y los registros de los modelos
- **Datos en tránsito:** Se utiliza junto con protocolos TLS 1.2 o superior para proteger la información mientras se mueve por la red.
- **Control:** KMS permite la rotación automática de claves y el control estricto sobre quién puede utilizarlas para cifrar o descifrar información sensible de IA.

#### Amazon Macie

Es un servicio de seguridad que utiliza ML para descubrir y clasificar automáticamente datos sensibles en AWS.

- **Uso en IA:** Es crítico para escanear los buckets de S3 antes de entrenar un modelo, Macie detecta Información de Identificación Personal (PII), Información de salud (PHI) o registros financieros que deben ser eliminados o protegidos adicionalmente para evitar el riesgo de exposición.

#### AWS PrivateLink

Este servicio proporciona conectividad privada y segura entre tu VPC (nube privada virtual) y los servicios de AWS como amazon bedrock

- **Propósito:** Permite que el tráfico de tus aplicaciones de IA se mantenga dentro de la red de Amazon sin exponerse a la internet pública
- **Seguridad:** Reduce drásticamente la superficie de ataque, lo cual es vital en industrias altamente reguladas como las finanzas o la salud.

### Ingeniería de datos segura

#### Evaluación de la calidad de los datos (Assessing Data Quality)

La premisa central es que si entra basura, sale basura; si los datos son de baja calidad, el rendimiento del modelo será deficiente. Se deben establecer métricas claras.

- **Integridad (Completeness):** Asegurar que los datos cubran un rango representativo de escenarios sin sesgos o vacíos importantes
- **Exactitud (Accuracy):** Los datos deben ser correctos, estar actualizados y reflejar situaciones reales.
- **Puntualidad:** Mide qué tan actuales son los datos; la información obsoleta puede degradar rápidamente el modelo
- **Consistencia:** Garantizar que la información sea coherente y lógica durante todo el desarrollo y despliegue.

#### Tecnologías de mejora de la privacidad

Estas tecnologías protegen tanto los datos de entrenamiento como los del usuario para evitar exposición de información sensible o PII

- **Anonimización y Seudonimización:** Técnicas esenciales para ocultar información confidencial cuando se aplican personalizaciones como RAG o fine-tuning
- **Privacidad diferencial:** Ayuda a evitar que se expongan puntos de datos individuales dentro de un conjunto masivo
- **Enmascaramiento y Ofuscación:** Métodos para reducir el riesgo de exposición incluso en caso de una brecha de seguridad.
- **Cifrado y Tokenización:** Protegen la información mientras se procesa o almacena, trabajando junto con computación segura multipartita

#### Control de acceso a los datos

Es el pilar para mantener la seguridad, determinando quién puede acceder a la información bajo qué circunstancias.

- Principio del mínimo privilegio
- Control de acceso basado en roles (RBAC)
- Monitoreo: Se deben registrar todas las actividades de acceso para detectar usos no autorizados de forma temprana

#### Integridad de los datos

Asegura que los modelos de IA se construyan sobre bases sólidas y confiables, libres de errores o manipulaciones maliciosas.

- **Controles de validación:** Implementar validaciones de esquema, integridad referencial y reglas de negocio en toda la canalización
- **Estrategia de respaldo y recuperación:** Contar con un plan robusto para restaurar datos rápidamente tras fallos del sistema o desastres
- **Trazabilidad y Linaje:** Mantener un registro completo del historial de los datos y pistas de auditoría para rastrear cada cambio realizado

### Amenazas específicas de IA

#### Inyección de peticiones

Es considerada una de las vulnerabilidades más críticas en la IA generativa.

- **Definición:** Ocurre cuando un atacante manipula un modelo de lenguaje mediante entradas diseñadas para que el modelo ejecute acciones no deseadas o revele información confidencial.
- **Tipos principales:**
    - **Directa:** El usuario escribe instrucciones para sobrescribir o revelar el “system prompt” (ej. “olvida todas las instrucciones anteriores”)
    - **Indirecta:** El modelo procesa contenido de fuentes externas (como una página web o un currículum cargado) que contiene instrucciones maliciosas ocultas por el atacante.
- **Mitigación:** Se debe sanitizar y validar cada petición entrante, y utilizar herramientas como Amazon Bedrock Guardrails para filtrar ataques de este tipo en tiempo real.

#### Envenenamiento de datos (Data Poisoning)

A diferencia de la inyección, este ataque ocurre antes de la interacción con el usuario final.

- **Definición:** Un atacante introduce datos maliciosos o sesgados en el conjunto de entrenamiento del modelo o en la base de conocimientos utilizadas para RAG.
- **Impacto:** El modelo “aprende” patrones incorrectos, lo que resulta en respuestas poco éticas, dañinas o que favorecen los intereses del atacante.
- **Riesgo:** Los modelos de código abierto son más susceptibles debido a la disponibilidad pública de su código y recursos limitados de seguridad.

#### Secuestro

Este término se utiliza de forma intercambiable con la inyección de instrucciones en contextos específicos.

- **Concepto:** El atacante inyecta instrucciones dentro del contenido legítimo que el modelo debe procesar.
- **Falla técnica:** Ocurre cuando el sistema no puede distinguir entre los datos a procesar (ej, un correo electrónico para resumir) y las instrucciones a seguir (ej una orden de reenviar datos a una dirección externa).
- **Consecuencia:** El modelo abandona su tarea original para ejecutar la instrucción maliciosa insertada, sirviendo como un “plano” para realizar actos dañinos.

#### Jailbreak (Evasión de restricciones)

Es un intento deliberado de eludir los filtros de seguridad y ética del modelo.

- **Mecanismos:** Se utilizan técnicas creativas, como pedirle al modelo que adopte un personaje o que responda dentro de un escenario hipotético (ej. "Imagina que escribes una novela sobre un hacker…”) para que realice acciones prohibidas.

### Estrategias de gobernanza de datos

La gobernanza de datos se centra en cómo se recopila, almacena y utiliza información para garantizar su calidad, integridad y privacidad.

- **Ciclos de vida del dato:** Describe el viaje de los datos desde su creación hasta su eliminación o archivo. En cargas de trabajo de IA, esto incluye la recolección de datos brutos, procesamiento, almacenamiento, uso en entrenamiento/inferencia y su retiro final. Una falta de planificación en el retiro de datos puede aumentar los riesgos de cumplimiento y los costos de almacenamiento. S3 permite automatizar este ciclo mediante políticas de ciclo de vida.
- **Registro (Logging):** Consiste en mantener un registro detallado de lo que el sistema de IA hace con los datos, incluyendo entradas, salidas, métricas de rendimiento y eventos del sistema. Es una herramienta fundamental para la transparencia y rendición de cuentas, permitiendo rastrear errores o entender por qué un modelo tomó una decisión específica. AWS utiliza servicios como CloudTrail y CloudWatch para estos registros. En Bedrock, el registro de invocación de los modelos captura el uso de tokens y el texto exacto de procesado.
- **Residencia de datos:** Se refiere a la ubicación física o geográfica donde se almacenan y procesan los datos. Es vital para cumplir con la soberanía de los datos.
- **Retención de datos:** Es la decisión de cuánto tiempo se conservan los datos y por qué. En IA las políticas de retención sirven para cumplir leyes, preservar datos históricos para reentrenar modelos o gestionar costos. Mantener datos por demasiado tiempo aumenta los riesgos de privacidad, mientras que eliminarlos muy pronto puede quitar contexto valioso al modelo.

#### Matriz de Ámbito de Seguridad de la IA Generativa

Este marco de trabajo ayuda a las organizaciones a evaluar y aplicar controles de seguridad clasificando las implementaciones de IA en cinco ámbitos, según el nivel de control y responsabilidad sobre el modelo y los datos.

1. **Aplicaciones de consumo:** Uso de herramientas públicas sin personalización (ej. ChatGPT). Operas totalmente en el entorno del proveedor y este controla los datos de entrenamiento.
2. **Aplicaciones empresariales:** Software de terceros con IA integrada y relaciones formales con el el proveedor.
3. **Modelos preentrenados:** Construcción de aplicaciones propias utilizando modelos existentes a través de APIs. Tú controlas cómo se integra y qué datos alimentas, pero el modelo reside con el tercero.
4. **Modelos refinados:** Ajuste de un modelo existente con tus propios datos propietarios para necesidades específicas. Aquí el cliente controla los datos de refinamiento, pero el proveedor sigue controlando los datos de entrenamiento iniciales.
5. **Modelos entrenados por cuenta propia:** Construcción y entrenamiento de modelos desde cero. El cliente tiene control total y la responsabilidad absoluta sobre el rendimiento, la ética, el cumplimiento y los datos de entrenamiento.

**Tip de examen:** Si una pregunta menciona un marco para clasificar el nivel de riesgo de las aplicaciones de IA generativa basándose en la personalización y el procesamiento de datos, la respuesta correcta es la **Generative AI Security Scoping Matrix**

# **Servicios**

## Inteligencia Artificial Generativa y Asistentes

- **Amazon Bedrock:** La vía rápida para usar IA Generativa y modelos fundacionales ya listos (como Claude o Llama) mediante una API unificada. Incluye herramientas como Bases de Conocimiento (RAG).
- **Amazon Bedrock Prompt Management:** Servicio especializado para crear, probar y almacenar plantillas de prompts reutilizables con soporte para inyección dinámica de variables.
- **Amazon Bedrock Model Evaluation:** Servicio integrado que permite ejecutar evaluaciones automáticas (precisión, robustez y toxicidad) o con revisores directamente en consola.
- **Amazon Bedrock Guardrails:** Capa de moderación que filtra contenido dañino y protege información sensible mediante políticas personalizadas en prompts y respuestas.
- **Amazon Q Business:** Asistente inteligente que ayuda a empleados a resumir documentos y generar contenido conectándose a datos internos de la empresa (Slack, Salesforce, etc.).
- **Amazon Q Developer:** Asistente especializado para desarrolladores que ayuda a escribir código, depurar y optimizar recursos dentro de IDEs y la consola de AWS.
- **PartyRock:** Entorno interactivo no-code basado en Bedrock para crear y experimentar con aplicaciones de IA rápidamente sin necesidad de una cuenta de AWS.

## Ecosistema Amazon SageMaker (Desarrollo y Ciclo de Vida del ML)

- **Amazon SageMaker:** El taller completo para que tú mismo construyas, entrenes y lances modelos de ML personalizados.
- **Amazon SageMaker JumpStart:** Catálogo dentro de SageMaker con modelos pre-entrenados para usuarios técnicos que necesitan control total sobre el fine-tuning e infraestructura.
- **SageMaker Studio y Notebook Instances:** Entorno de desarrollo integrado (IDE) e instancias con Python preinstalado para investigar datos, detectar anomalías, realizar análisis estadísticos y visualizar estructuras.
- **Amazon SageMaker Data Wrangler:** Limpia, normaliza y transforma datos brutos automáticamente con más de 300 opciones sin usar código complejo.
- **SageMaker Feature Store:** Repositorio central para almacenar, compartir y reutilizar características (variables) en distintos proyectos de ML.
- **SageMaker Automatic Model Tuning:** Optimiza el modelo encontrando la mejor combinación de hiperparámetros automáticamente.
- **Amazon SageMaker Ground Truth:** Facilita el etiquetado de datos mediante intervención humana para crear descripciones necesarias en el aprendizaje supervisado.
- **Amazon Augmented AI (A2I):** Implementa la supervisión humana en el flujo de trabajo para revisar predicciones de baja confianza y garantizar precisión.
- **Amazon SageMaker Clarify:** Proporciona herramientas de IA explicable para detectar sesgos en los datos y modelos, justificando mediante informes qué variables influyen más en las decisiones.
- **Amazon SageMaker Model Monitor:** Supervisa modelos en producción de forma continua para detectar derivas de datos (drift) o degradación del rendimiento en el mundo real.
- **SageMaker Model Cards:** Herramienta principal para documentar detalles del modelo, métricas de entrenamiento, evaluaciones y limitaciones, actuando como una ficha técnica de transparencia.

## Servicios de IA Pre-entrenados (Visión, Voz, Texto y Predicción)

- **Amazon Comprehend:** Analiza textos para extraer información, sentimientos, temas y entidades clave.
- **Amazon Rekognition:** Identifica objetos, personas, texto, escenas y actividades en imágenes y videos.
- **Amazon Transcribe:** Utiliza reconocimiento de voz automático para convertir audio en texto de manera rápida.
- **Amazon Polly:** Convierte texto escrito en voz humana realista con una amplia variedad de idiomas y acentos.
- **Amazon Lex:** Proporciona las herramientas para construir interfaces de conversación (chatbots) mediante voz y texto.
- **Amazon Forecast:** Predice tendencias futuras analizando datos históricos de series temporales, como inventarios o precios.
- **Amazon Textract:** Extrae de forma precisa texto y datos estructurados de documentos escaneados o formularios.

## Datos, Búsqueda y RAG (Generación Aumentada por Recuperación)

- **AWS Data Lake:** Permite gestionar y centralizar grandes volúmenes de información masiva de forma eficiente.
- **Amazon Redshift:** Almacén de datos masivo (data warehouse) para analizar petabytes de información mediante SQL.
- **Amazon Aurora y RDS:** Permiten almacenar y consultar vectores en entornos SQL mediante la extensión pgvector, manteniendo la robustez y conformidad ACID.
- **Amazon OpenSearch Service:** Solución escalable diseñada para búsquedas vectoriales masivas, semánticas e híbridas con alta concurrencia y baja latencia.
- **Amazon Neptune:** Base de datos de grafos que optimiza el RAG al modelar relaciones y conexiones complejas entre entidades que la similitud semántica simple no logra captar.
- **Amazon Kendra:** Motor de búsqueda empresarial inteligente que conecta nativamente múltiples fuentes de datos organizacionales para ofrecer respuestas precisas mediante RAG.

## Seguridad, Auditoría y Cumplimiento

- **Cifrado y AWS KMS:** Protege la información de los modelos mediante el cifrado de datos en reposo y en tránsito, permitiendo control total sobre las claves.
- **AWS PrivateLink:** Garantiza que el tráfico entre tu red y los servicios de IA (como Bedrock) se mantenga privado, sin exponerse a la internet pública.
- **Amazon Macie:** Utiliza aprendizaje automático para descubrir y clasificar automáticamente datos sensibles en S3, evitando usos indebidos.
- **AWS CloudTrail:** Registra y monitorea todas las llamadas a la API y la actividad de las cuentas (quién realizó una acción, cuándo y desde dónde).
- **AWS Config:** Rastrea y registra continuamente los cambios de configuración en tus recursos para evaluar si cumplen con las normativas.
- **Amazon Inspector:** Servicio de gestión de vulnerabilidades que escanea automáticamente tus cargas de trabajo para detectar exposiciones de red y fallos.
- **AWS Audit Manager:** Automatiza la recopilación de evidencia para auditorías, facilitando la evaluación del cumplimiento con marcos como GDPR o HIPAA.
- **AWS Artifact:** Portal de autoservicio para acceder bajo demanda a informes de cumplimiento de terceros y certificaciones globales (ISO, SOC).
- **AWS Trusted Advisor:** Evalúa tu entorno frente a las mejores prácticas en áreas como seguridad, rendimiento y optimización de costos.

## Aprendizaje por Refuerzo

- **AWS DeepRacer:** Utiliza aprendizaje por refuerzo para entrenar coches de carreras autónomos en un simulador 3D.
