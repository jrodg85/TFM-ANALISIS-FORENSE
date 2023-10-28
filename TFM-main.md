# Master Universitario de Ciberseguridad y privacidad.

# M1.881 - TFM - Análisis forense

## Alumno:

José Enrique Rodríguez González.

## Tutora de TFM:

Dña. Elena Botana de Castro.

## Profesor responsable de la asignatura:

D. Jordi Serra Ruiz.

## Fecha de Entrega:

Enero de 2024.


## Índice General.

- [Deuda técnica.](#deuda-técnica)
- [0. Agradecimientos.](#0-agradecimientos)
- [1. Plan de trabajo.](#1-plan-de-trabajo)
  - [Índice del capítulo 1. Plan de trabajo.](#índice-del-capítulo-1-plan-de-trabajo)
  - [1.0. Introducción al capítulo 1. Plan de trabajo.](#10-introducción-al-capítulo-1-plan-de-trabajo)
  - [1.1. Problema a resolver.](#11-problema-a-resolver)
  - [1.2. Objetivos.](#12-objetivos)
  - [1.3. Descripción del entorno de trabajo.](#13-descripción-del-entorno-de-trabajo)
  - [1.4. Listado de tareas.](#14-listado-de-tareas)
  - [1.5. Planificación temporal de las tareas.](#15-planificación-temporal-de-las-tareas)
  - [1.6. Revisión del estado del arte de la informática forense.](#16-revisión-del-estado-del-arte-de-la-informática-forense)
- [2. Extremos del análisis y previsión de pruebas técnicas.]
  - [Índice del capítulo 2. Extremos del análisis y previsión de pruebas técnicas.]
  - [2.0. Introducción al capítulo 2. Extremos del análisis y previsión de pruebas técnicas.]
  - [2.1. Propuesta de extremos.]
  - [2.2. Previsión de pruebas técnicas.]
- [3. Análisis de la memoria RAM.]
  - [Índice del capítulo 3. Análisis de la memoria RAM.]
  - [3.0. Introducción al capítulo 3. Análisis de la memoria RAM.]
  - [3.1. Acciones previas al análisis de la memoria RAM.]
  - [3.2. Sistema Operativo de la memoria RAM analizada.]
  - [3.3. Datos de interés de la captura de la memoria RAM.]
  - [3.4. Búsqueda de procesos en funcionamiento de interés para el análisis.]
  - [3.5. Listado de conexiones de red y conexiones sospechosas.]
- [4. Análisis del disco duro.]
  - [Índice del capítulo 4. Análisis del disco duro.]
  - [4.0. Introducción al capítulo 4. Análisis del disco duro.]
  - [4.1. Acciones previas al análisis del disco duro.]
  - [4.2. Datos de interés del disco duro.]
  - [4.3. Usuarios del sistema.]
  - [4.4. Análisis de evidencias del disco duro.]
- [5. Resumen ejecutivo.]
  - [Índice del capítulo 5. Resumen ejecutivo.]
  - [5.0. Introducción al capítulo 5. Resumen ejecutivo.]
- [6. Informe pericial.]
  - [Índice del capítulo 6. Informe pericial.]
  - [6.0. Introducción al capítulo 6. Informe pericial.]
- [7. Conclusiones.]
  - [Índice del capítulo 7. Conclusiones.]
  - [7.0. Introducción al capítulo 7. Conclusiones.]
- [8. Anexos.]
  - [Índice del capítulo 8. Anexos.]
  - [8.0. Introducción al capítulo 8. Anexos.]
  - [8.1. Creación de perfil para volatility]
  - [8.2. Glosario de términos y abreviaturas.]
  - [8.3. Imágenes.]
- [9. Bibliografía]

---

# Deuda técnica.

Este no es un capitulo al uso del TFM, si no que tratará de llevar un control de las tareas pendientes (Deuda técnica) de todo el TFM.

PEC 1


**DEUDA TÉCNICA: Pendiente de Referenciar!!!, enunciado del TFM**

**DEUDA TÉCNICA: Pendiente de Referenciar!!!, referenciar de la web de los TFM**

**DEUDA TÉCNICA: Buscar presidente de los EE.UU., preguntar a "//4lanoga" LA RESPUESTA ES REAGAN**

**DEUDA TÉCNICA: Listado de aplicaciones a utilizar en la descripción del entorno de trabajo**

**DEUDA TÉCNICA: plantear posible reducción del estado del arte**

**DEUDA TÉCNICA: Referencia a WIKIPEDIA**


PEC 2

**DEUDA TÉCNICA: Indexar indice, indicar paginas**

---


# 0. Agradecimientos.

A mi esposa e hija, acompañantes en todo momento de esta aventura académica.

A mis compañeros de trabajo, Juanma, Luisma y Borja, que saben de que estos tres años que llevo realizando este master y han conocido todos los derroteros que me ha llevado este camino.


[Volver al Índice General.](#índice-general)

---

# 1. Plan de trabajo.


## Índice del capítulo 1. Plan de trabajo.

- [1.0. Introducción al capítulo 1. Plan de trabajo.](#10-introducción-al-capítulo-1-plan-de-trabajo)
- [1.1. Problema a resolver.](#11-problema-a-resolver)
- [1.2. Objetivos.](#12-objetivos)
- [1.3. Descripción del entorno de trabajo.](#13-descripción-del-entorno-de-trabajo)
- [1.4. Listado de tareas.](#14-listado-de-tareas)
- [1.5. Planificación temporal de las tareas.](#15-planificación-temporal-de-las-tareas)
- [1.6. Revisión del estado del arte de la informática forense.](#16-revisión-del-estado-del-arte-de-la-informática-forense)


[Volver al Índice General.](#índice-general)

---

## 1.0. Introducción al capítulo 1. Plan de trabajo.

La situación en la que nos encontramos es un caso práctico laboral, en el que realizamos el papel de CISO.

En este caso, la dirección de la empresa tiene serias sospechas, no probadas, de que han accedido a los sistemas de forma ilícita. Por lo que el gerente de la empresa me solicita, como CISO, que se compruebe si realmente han accedido, así como el método que han utilizado. Por otro lado, solicitan las consecuencias que se derivan del dicho acceso, si ha habido extracción de información alguna.

**DEUDA TÉCNICA: Pendiente de Referenciar!!! ENUNCIADO TFM**

[Volver al Índice del capítulo 1. Plan de trabajo.](#índice-del-capítulo-1-plan-de-trabajo)

[Volver al Índice General.](#índice-general)

---

## 1.1. Problema a resolver.

Por, lo expuesto en la introducción del capítulo, se coliga que el problema a resolver es la resolución de las cuestiones solicitadas por el Gerente de la empresa.

Una definición idónea que se puede adoptar en el presente TFM es lo indicado en su momento en la propuesta del TFM:

Solventar las necesidades del gerente de la empresa mediante el análisis forense del disco duro y la captura de memoria de un ordenador personal, en un caso real con un sistema virtualizado, vinculado a una presunta conducta delictiva real. Para ello, se utilizarán herramientas específicas para la localización de las evidencias digitales sobre los discos duros y la memoria que puedan demostrar el presunto delito (Encase, Autopsy, Volatility, o cualquier otra herramienta, o conjunto de herramientas con prestaciones equivalentes). Finalmente, las evidencias localizadas deberán recogerse en un informe ejecutivo o pericial, el cual, además de los aspectos técnicos, deberá tener en cuenta aquellos requisitos procesales necesarios para que el análisis pueda tener validez en un proceso judicial.

**DEUDA TÉCNICA: Pendiente de Referenciar!!!, referenciar de la web de los TFM**

[Volver al Índice del capítulo 1. Plan de trabajo.](#índice-del-capítulo-1-plan-de-trabajo)

[Volver al Índice General.](#índice-general)

---

## 1.2. Objetivos.

Se describe un el siguiente listado de objetivos que se obtienen al analizar el enunciado del TFM:

  - 1. Elaboración del Análisis forense de Disco Duro y RAM.
    - 1.1. realizar una recuperación parcial o total de la información borrada existente en los dispositivos susceptibles de ser analizados (carving).
    - 1.2. Relativo al análisis de la memoria RAM.
      - 1.2.1. Comprobar la integridad de la memoria RAM.
      - 1.2.2. Comprobar fecha de la captura de la RAM.
      - 1.2.3. Determinar la edición y versión de Windows que tiene instalado el sistema operativo del ordenador sobre el cual se ha efectuado la captura de la memoria RAM.
      - 1.2.4. Buscar los procesos en funcionamiento y localiza aquellos que te parezcan de interés para el análisis forense del ordenador analizado.
      - 1.2.5. Extraer los procesos que consideres sospechosos y analizarlos.
      - 1.2.6. Listar las conexiones de red y analizarlas.
    - 1.3. Relativo al análisis del Disco Duro.
      - 1.3.1. Comprobar la integridad del disco duro.
      - 1.3.2. Determinar la siguiente información del disco duro.
        - 1.3.2.1. Tamaño del disco duro analizado.
        - 1.3.2.2. Sistema y versión del sistema operativo instalado.
        - 1.3.2.3. Nombre del propietario y relación de software instalado.
        - 1.3.2.4. "Product ID" y "Product Key" asociadas al sistema.
        - 1.3.2.5. Fecha y hora de instalación del sistema operativo.
        - 1.3.2.6. Determinar marca y modelo (si es posible) del hardware siguiente: CPU, monitor, tarjeta gráfica, tarjeta Ethernet y Wireless.
      - 1.3.3. Determinar qué usuarios tiene definidos el sistema.
      - 1.3.4.Localizar los documentos (archivos PDF, de texto, hojas de cálculo, etc.) que puedan tener relación con alguna conducta presuntamente delictiva.
      - 1.3.5. Localizar los archivos eliminados y determina si hay alguno relevante para la causa investigada.
      - 1.3.6. Localizar los ficheros comprimidos relevantes analizarlos, reventar contraseña si es necesario y analizar su contenido.
      - 1.3.7. Localizar algún fichero ejecutable que pueda resultar de interés para la investigación, ademas, analizar la relación con alguna evidencia anterior.
      - 1.3.8. Determinar el contenido del fichero log de un conocido programa de comunicación si es necesario y relacionarlo con el caso investigado.
      - 1.3.9. Realizar un análisis de la navegación web.
      - 1.3.10. Estudio de los dispositivos físicos que en algún momento fueron conectados al sistema estudiado: móviles, USBs, impresoras, escáneres, cámaras, tarjetas de memoria.
      - 1.3.11. Estudio de la información contenida en los unallocated cluster o en el file slack.
      - 1.3.12. Información contenida en los archivos de hibernación, paginación, particiones y archivos de intercambio (swap).
      - 1.3.13. Análisis de la cola de impresión.
      - 1.3.14. Visualización de los links de los archivos y de los archivos accedidos recientemente.
      - 1.3.15. Estudio de los metadatos de los archivos, si se considera que pueden ser relevantes para el caso.
      - 1.3.16. Estudio de las aplicaciones de virtualización.
      - 1.3.17 Estudio de las bases de datos instaladas y las aplicaciones que permiten su gestión.
      - 1.3.18. Estudio de los programas de cifrado, particiones cifradas.
      - 1.3.19. Análisis de los clientes de correo electrónico y del webmail.
    - 1.4. Realizar un estudio de la seguridad.
      - 1.4.1. Estudiar si las evidencias analizadas han sido comprometidas.
      - 1.4.2. Identificar cualquier aplicación vulnerable, software malicioso, evaluar el daño sufrido, identificar los archivos que han sido comprometidos, así como determinar la vía de acceso al sistema.
  - 2. Relativo al resumen ejecutivo, elaborarlo teniendo en cuenta los siguientes apartados.
    - 2.1. Claridad en la comunicación, proporcionando información de forma clara y concisa y, por otro lado, utilizar un lenguaje accesible para los no expertos en el área.
    - 2.2. Presentar el contexto u antecedentes, describiendo el motivo y las circunstancias del análisis forense y Proporcionar una breve descripción del incidente o situación bajo investigación.
    - 2.3. Redactar un resumen ejecutivo con los hallazgos clave y las recomendaciones.
    - 2.4. Describir la metodología utilizada durante el análisis forense.
    - 2.5. Explicar las herramientas y técnicas de análisis implementadas.
    - 2.6. Proporcionar una línea de tiempo detallada de los eventos y acciones tomadas.
    - 2.7. Detallar los hallazgos significativos del análisis.
    - 2.8. Incluir evidencia técnica relevante, como registros de logs, archivos, etc
    - 2.9. Evaluar y describir el impacto del incidente en la organización o individuos afectados.
    - 2.10. Proveer conclusiones basadas en los hallazgos del análisis forense.
    - 2.11. Proporcionar recomendaciones para la acción futura, basadas en los hallazgos y conclusiones.
    - 2.12. Sugerir medidas preventivas y correctivas para evitar incidentes similares en el futuro.
  - 3. Elaborar un informe pericial teniendo en cuenta los siguientes apartados.
    - 3.1. Mantener una postura objetiva e imparcial en todo momento.
    - 3.2. Garantizar que el análisis y las conclusiones estén fundamentados en evidencias tangibles y replicables.
    - 3.3. Mantener la cadena de custodia y la integridad de las pruebas durante todo el proceso.
    - 3.4. Redactar el informe de manera clara, precisa y entendible para personas sin conocimientos técnicos específicos.
    - 3.5. Describir detalladamente el caso, partes involucradas, y el objeto del peritaje.
    - 3.6. Detallar las herramientas, técnicas y procedimientos utilizados en el análisis forense.
    - 3.7. Justificar la elección de la metodología y herramientas utilizadas.
    - 3.8. Establecer una línea temporal clara de todas las acciones y procesos llevados a cabo durante la investigación
    - 3.9. Presentar de forma clara y precisa los hallazgos resultantes del análisis forense. Los cuales será
    - 3.10 Incluir elementos visuales como gráficos, imágenes o tablas para facilitar la comprensión de los datos.
    - 3.11. Interpretar las evidencias de manera fundamentada y ligada a las normativas y principios de la ciencia forense digital.
    - 3.12. Derivar conclusiones basadas exclusivamente en las evidencias y hallazgos del análisis.
    - 3.13. Ofrecer una opinión pericial en base a los hallazgos, respetando los límites de la prueba pericial y los datos disponibles.
    - 3.14. Garantizar que toda la información manejada se mantiene confidencial y segura.
    - 3.15. Discutir las implicaciones legales de los hallazgos y su posible impacto en el caso.
    - 3.16. Estar preparado para ratificar el informe en un tribunal y responder a preguntas relacionadas con el análisis y los hallazgos. Este supuesto, el defensor se intuye que se realizará en la defensa síncrona de la defensa de este TFM.
  - 4. Realizar unas conclusiones acordes a todo el TFM realizado.
    - 4.1. Basarse en ideas fuerza que han aparecido durante todo el TFM.
    - 4.2. Tener en cuenta que este apartado es el que finalmente, el gerente de la empresa, como miembro directivo de la misma, usando el método del Presidente Reagan.


**DEUDA TÉCNICA: Pendiente de Referenciar!!! ENUNCIADO TFM**


[Volver al Índice del capítulo 1. Plan de trabajo.](#índice-del-capítulo-1-plan-de-trabajo)

[Volver al Índice General.](#índice-general)

---

## 1.3. Descripción del entorno de trabajo.














[Volver al Índice del capítulo 1. Plan de trabajo.](#índice-del-capítulo-1-plan-de-trabajo)

[Volver al Índice General.](#índice-general)

---

## 1.4. Listado de tareas.











[Volver al Índice del capítulo 1. Plan de trabajo.](#índice-del-capítulo-1-plan-de-trabajo)

[Volver al Índice General.](#índice-general)

---

## 1.5. Planificación temporal de las tareas.










[Volver al Índice del capítulo 1. Plan de trabajo.](#índice-del-capítulo-1-plan-de-trabajo)

[Volver al Índice General.](#índice-general)

---

## 1.6. Revisión del estado del arte de la informática forense.















[Volver al Índice del capítulo 1. Plan de trabajo.](#índice-del-capítulo-1-plan-de-trabajo)

[Volver al Índice General.](#índice-general)

---

## 




















[Volver al Índice del capítulo 1. Plan de trabajo.](#índice-del-capítulo-1-plan-de-trabajo)

[Volver al Índice General.](#índice-general)

---

## 
























[Volver al Índice del capítulo 1. Plan de trabajo.](#índice-del-capítulo-1-plan-de-trabajo)

[Volver al Índice General.](#índice-general)

---

## 





















[Volver al Índice del capítulo 1. Plan de trabajo.](#índice-del-capítulo-1-plan-de-trabajo)

[Volver al Índice General.](#índice-general)

---

## 
























