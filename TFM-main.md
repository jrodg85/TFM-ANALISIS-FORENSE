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

---

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

**FICHA DEL TRABAJO FINAL DE MASTER**

|  |  |
| --: | :-- |
| Titulo del trabajo: | Análisis forense de un ordenador. |
| Nombre del autor: | José Enrique Rodríguez González. |
| Nombre del Consultor: | Elena Botana de Castro. |
| Área de trabajo final: | Análisis Forense. |
| Título del Master: | Master Universitario de Ciberseguridad y Privacidad (MUCYP). |
| Universidad: | Universitat Oberta de Catalunya. |
||

<br>

**RESUMEN DEL TRABAJO**

|  |
|---|
|El objetivo del presente Trabajo de Fin de Máster es realizar un análisis forense de un ordenador del que se sospecha de que han accedido a los sistemas de forma ilícita. Se comprobará si realmente han accedido, así como el método que han utilizado. Por otro lado, se elaborará un informe con las consecuencias que se derivan del dicho acceso ademas se comprobará si ha habido extracción de información alguna. <br>Por último, y no menos importante, para el presente trabajo se tendrán en cuenta los estándares que existen en la actualidad, como pueden ser la norma ISO 27037, la RFC 3227  o las normas de la Asociación Española de Normalización UNE 71505 y UNE 71506.|
||

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

## Índice General.

- [Deuda técnica.](#deuda-técnica)
- [0. Agradecimientos.](#0-agradecimientos)
- [1. Plan de trabajo.](#1-plan-de-trabajo)
    - [Índice del capítulo 1. Plan de trabajo.](#índice-del-capítulo-1-plan-de-trabajo)
    - [1.0. Introducción al capítulo 1. Plan de trabajo.](#10-introducción-al-capítulo-1-plan-de-trabajo)
    - [1.1. Problema a resolver.](#11-problema-a-resolver)
    - [1.2. Objetivos.](#12-objetivos)
    - [1.3 Metodologías.](#13-metodologías)
    - [1.4. Descripción del entorno de trabajo.](#14-descripción-del-entorno-de-trabajo)
    - [1.5. Listado de tareas.](#15-listado-de-tareas)
    - [1.6. Planificación temporal de las tareas.](#16-planificación-temporal-de-las-tareas)
    - [1.7. Revisión del estado del arte de la informática forense.](#17-revisión-del-estado-del-arte-de-la-informática-forense)
- [2. Extremos del análisis y previsión de pruebas técnicas.](#2-extremos-del-análisis-y-previsión-de-pruebas-técnicas)
    - [Índice del capítulo 2. Extremos del análisis y previsión de pruebas técnicas.](#índice-del-capítulo-2-extremos-del-análisis-y-previsión-de-pruebas-técnicas)
    - [2.0. Introducción al capítulo 2. Extremos del análisis y previsión de pruebas técnicas.](#índice-del-capítulo-2-extremos-del-análisis-y-previsión-de-pruebas-técnicas)
    - [2.1. Propuesta de extremos.](#21-propuesta-de-extremos)
    - [2.2. Previsión de pruebas técnicas.](#22-previsión-de-pruebas-técnicas)
- [3. Análisis de la memoria RAM.](#3-análisis-de-la-memoria-ram)
    - [Índice del capítulo 3. Análisis de la memoria RAM.](#índice-del-capítulo-3-análisis-de-la-memoria-ram)
    - [3.0. Introducción al capítulo 3. Análisis de la memoria RAM.](#30-introducción-al-capítulo-3-análisis-de-la-memoria-ram)
    - [3.1. Acciones previas al análisis de la memoria RAM.](#31-acciones-previas-al-análisis-de-la-memoria-ram)
    - [3.2. Sistema Operativo de la memoria RAM analizada.](#32-sistema-operativo-de-la-memoria-ram-analizada)
    - [3.3. Datos de interés de la captura de la memoria RAM.](#33-datos-de-interés-de-la-captura-de-la-memoria-ram)
    - [3.4. Búsqueda de procesos en funcionamiento de interés para el análisis.](#34-búsqueda-de-procesos-en-funcionamiento-de-interés-para-el-análisis)
    - [3.5. Listado de conexiones de red y conexiones sospechosas.](#35-listado-de-conexiones-de-red-y-conexiones-sospechosas)
- [4. Análisis del disco duro.](#4-análisis-del-disco-duro)
    - [Índice del capítulo 4. Análisis del disco duro.](#índice-del-capítulo-4-análisis-del-disco-duro)
    - [4.0. Introducción al capítulo 4. Análisis del disco duro.](#40-introducción-al-capítulo-4-análisis-del-disco-duro)
    - [4.1. Acciones previas al análisis del disco duro.](#41-acciones-previas-al-análisis-del-disco-duro)
    - [4.2. Datos de interés del disco duro.](#42-datos-de-interés-del-disco-duro)
    - [4.3. Usuarios del sistema.](#43-usuarios-del-sistema)
    - [4.4. Análisis de evidencias del disco duro.](#44-análisis-de-evidencias-del-disco-duro)
- [5. Resumen ejecutivo.](#5-resumen-ejecutivo)
    - [Índice del capítulo 5. Resumen ejecutivo.](#índice-del-capítulo-5-resumen-ejecutivo)
    - [5.0. Introducción al capítulo 5. Resumen ejecutivo.](#50-introducción-al-capítulo-5-resumen-ejecutivo)
    - [5.1. Resumen ejecutivo](#51-resumen-ejecutivo)
- [6. Informe pericial.](#6-informe-pericial)
    - [Índice del capítulo 6. Informe pericial.](#índice-del-capítulo-6-informe-pericial)
    - [6.0. Introducción al capítulo 6. Informe pericial.](#60-introducción-al-capítulo-6-informe-pericial)
    - [6.1. Informe pericial.](#61-informe-pericial)
- [7. Conclusiones.](#7-conclusiones)
    - [Índice del capítulo 7. Conclusiones.](#índice-del-capítulo-7-conclusiones)
    - [7.0. Introducción al capítulo 7. Conclusiones.](#70-introducción-al-capítulo-7-conclusiones)
    - [7.1 Conclusiones.](#71-conclusiones)
- [8. Anexos.](#8-anexos)
    - [Índice del capítulo 8. Anexos.](#índice-del-capítulo-8-anexos)
    - [8.0. Introducción al capítulo 8. Anexos.](#80-introducción-al-capítulo-8-anexos)
    - [8.1. Creación de perfil para volatility.](#81-creación-de-perfil-para-volatility)
    - [8.2. Glosario de términos y abreviaturas.](#82-glosario-de-términos-y-abreviaturas)
    - [8.3. Imágenes.](#83-imágenes)
    - [8.4. Videos.](#84-videos)
    - [8.5. Extracto de comandos utilizados.](#85-extracto-de-comandos-utilizados)
    - [8.5. Referencias.](#86-referencias)
    - [8.6. Linea de tiempo de evidencias.](#87-linea-de-tiempo-de-evidencias)

---

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

# Deuda técnica.

Este no es un capitulo al uso del TFM, si no que tratará de llevar un control de las tareas pendientes (Deuda técnica) de todo el TFM.

PEC 1

**DEUDA TÉCNICA: Listado de aplicaciones a utilizar en la descripción del entorno de trabajo**

**DEUDA TÉCNICA: plantear posible reducción del estado del arte**

**DEUDA TÉCNICA: Referencia a WIKPEDIA**

PEC 2

**DEUDA TÉCNICA: Indexar indice, indicar paginas**

**DEUDA TÉCNICA: ENLAZAR CON INDICE DEL CAPITULO**

**DEUDA TÉCNICA: MOVER COMANDOS UTILIZADOS Y LAS IMÁGENES A LOS ANEXOS DE IMÁGENES.**

COMENTARIOS TUTORA TFM PEC 1.

- Has realizado un buen trabajo con la planificación temporal y actividades.
    - Sin embargo, deben mejorarse los siguientes puntos:
        - 2. Definición de Objetivos: Has definido claramente tus objetivos, lo cual es positivo. Sin embargo, es esencial que logres responder a todos ellos en la entrega final o justifiques cualquier impedimento que impida su cumplimiento.
        - 3. Entorno de Trabajo: Debes proporcionar más detalles sobre el equipo y las herramientas específicas que utilizarás en tu análisis forense. Esto garantizará una comprensión completa de tu enfoque.
        - 5. Comparativa de Herramientas: La comparativa de herramientas es exhaustiva, pero muchas de ellas pueden resultar irrelevantes. Sería más beneficioso seleccionar algunas, analizarlas en detalle y explicar por qué las has elegido y cómo se utilizarán en tu TFM.
        - 6. Glosario: Es positivo que incluyas un glosario de términos y abreviaturas, pero es necesario desarrollarlo, incluyendo el origen de abreviaturas como "CISO".
        - 7. Bibliografía: La ausencia de una bibliografía es una deficiencia significativa. Debes incluir una bibliografía que respalde tus afirmaciones y muestre la base teórica en la que se basa tu TFM.
        - 8. Impacto ético y social: No he podido ver nada relativo a este punto en la entrega realizada.

---

<br><br><br><br>

# 0. Agradecimientos.

A mi esposa e hija, acompañantes en todo momento de esta aventura académica.

A mis compañeros de trabajo, Juanma, Luisma y Borja, que saben de que estos tres años que llevo realizando este master y han conocido todos los derroteros que me ha llevado este camino.

**[Volver al Índice General.](#índice-general)**

---

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

# 1. Plan de trabajo.

## Índice del capítulo 1. Plan de trabajo.

- [1.0. Introducción al capítulo 1. Plan de trabajo.](#10-introducción-al-capítulo-1-plan-de-trabajo)
- [1.1. Problema a resolver.](#11-problema-a-resolver)
- [1.2. Objetivos.](#12-objetivos)
- [1.3. Metodologías.](#13-metodologías)
    - [1.3.1. Introducción.](#131-introducción)
    - [1.3.2. Normas ISO 27037 e ISO 30121.](#132-normas-iso-27037-e-iso-30121)
    - [1.3.3. Norma RFC 3227.](#133-norma-rfc-3227)
    - [1.3.4. Normas UNE 71505 y UNE 71506.](#134-normas-une-71505-y-une-71506)
    - [1.3.5. Conclusiones relativo a las metodologías.](#135-conclusiones-relativo-a-las-metodologías)
- [1.4. Descripción del entorno de trabajo.](#14-descripción-del-entorno-de-trabajo)
- [1.5. Listado de tareas.](#15-listado-de-tareas)
- [1.6. Planificación temporal de las tareas.](#16-planificación-temporal-de-las-tareas)
- [1.7. Revisión del estado del arte de la informática forense.](#17-revisión-del-estado-del-arte-de-la-informática-forense)
    - [1.7.1. Introducción del estado del arte de la informática forense.](#171-introducción-del-estado-del-arte-de-la-informática-forense)
    - [1.7.2. Definiciones.](#172-definiciones)
    - [1.7.3. Objetivos de la informática forense.](#173-objetivos-de-la-informática-forense)
    - [1.7.4. Evidencia digital.](#174-evidencia-digital)
    - [1.7.5. Perspectiva de tres roles.](#175-perspectiva-de-tres-roles)
    - [1.7.6. Retos y riesgos en el análisis forense.](#176-retos-y-riesgos-en-el-cómputo-forense)
    - [1.7.7. Herramientas del análisis forense.](#177-herramientas-de-análisis-forense)

**[Volver al Índice General.](#índice-general)**

---

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

## 1.0. Introducción al capítulo 1. Plan de trabajo.

#### [1.0. Glosario 001: CISO.](#82001000001-ciso)

La situación en la que nos encontramos es un caso práctico laboral, en el que realizamos el papel de [CISO](#82001000001-ciso).

En este caso, la dirección de la empresa tiene serias sospechas, no probadas, de que han accedido a los sistemas de forma ilícita. Por lo que el gerente de la empresa me solicita, como [CISO](#82001000001-ciso), que se compruebe si realmente han accedido, así como el método que han utilizado. Por otro lado, solicitan las consecuencias que se derivan del dicho acceso, si ha habido extracción de información alguna.

#### [1.0. Referencia 001.](#86001-enunciado-tfm)

**[Volver al Índice del capítulo 1. Plan de trabajo.](#índice-del-capítulo-1-plan-de-trabajo) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [Volver al Índice General.](#índice-general)**

---

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

## 1.1. Problema a resolver.

Por, lo expuesto en la introducción del capítulo, se coliga que el problema a resolver es la resolución de las cuestiones solicitadas por el Gerente de la empresa.

Una definición idónea que se puede adoptar en el presente Trabajo de Final de Máster (en adelante TFM) es lo indicado en su momento en la propuesta del TFM:

Solventar las necesidades del gerente de la empresa mediante el análisis forense del disco duro y la captura de memoria de un ordenador personal, en un caso real con un sistema virtualizado, vinculado a una presunta conducta delictiva real. Para ello, se utilizarán herramientas específicas para la localización de las evidencias digitales sobre los discos duros y la memoria que puedan demostrar el presunto delito (Encase, Autopsy, Volatility, o cualquier otra herramienta, o conjunto de herramientas con prestaciones equivalentes). Finalmente, las evidencias localizadas deberán recogerse en un informe ejecutivo o pericial, el cual, además de los aspectos técnicos, deberá tener en cuenta aquellos requisitos procesales necesarios para que el análisis pueda tener validez en un proceso judicial.

#### [1.1. Referencia 002.](#86002-propuestas-de-tfm)

**[Volver al Índice del capítulo 1. Plan de trabajo.](#índice-del-capítulo-1-plan-de-trabajo) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [Volver al Índice General.](#índice-general)**

---

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

## 1.2. Objetivos.

Se describe un el siguiente listado de objetivos que se obtienen al analizar el enunciado del TFM:

1. Elaboración del Análisis forense de Disco Duro y RAM.
    - 1.1. realizar una recuperación parcial o total de la información borrada existente en los dispositivos susceptibles de ser analizados (**<u style='color:red'>carving</u>**).
    - 1.2. Relativo al análisis de la memoria RAM.
        - 1.2.1. Comprobar la **<u style='color:red'>integridad</u>** de la memoria RAM.
        - 1.2.2. Comprobar fecha de la captura de la RAM.
        - 1.2.3. Determinar la edición y versión de Windows que tiene instalado el sistema operativo del ordenador sobre el cual se ha efectuado la captura de la memoria RAM.
        - 1.2.4. Buscar los procesos en funcionamiento y localiza aquellos que te parezcan de interés para el análisis forense del ordenador analizado.
        - 1.2.5. Extraer los procesos que consideres sospechosos y analizarlos.
        - 1.2.6. Listar las conexiones de red y analizarlas.
    - 1.3. Relativo al análisis del Disco Duro.
        - 1.3.1. Comprobar la **<u style='color:red'>integridad</u>** del disco duro.
        - 1.3.2. Determinar la siguiente información del disco duro.
            - 1.3.2.1. Tamaño del disco duro analizado.
            - 1.3.2.2. Sistema y versión del sistema operativo instalado.
            - 1.3.2.3. Nombre del propietario y relación de software instalado.
            - 1.3.2.4. "**<u style='color:red'>Product ID</u>**" y "**<u style='color:red'>Product Key</u>**" asociadas al sistema.
            - 1.3.2.5. Fecha y hora de instalación del sistema operativo.
            - 1.3.2.6. Determinar marca y modelo (si es posible) del hardware siguiente: **<u style='color:red'>CPU</u>**, monitor, tarjeta gráfica, tarjeta **<u style='color:red'>Ethernet</u>** y **<u style='color:red'>Wireless</u>**.
        - 1.3.3. Determinar qué usuarios tiene definidos el sistema.
        - 1.3.4.Localizar los documentos (archivos PDF, de texto, hojas de cálculo, etc.) que puedan tener relación con alguna conducta presuntamente delictiva.
        - 1.3.5. Localizar los archivos eliminados y determina si hay alguno relevante para la causa investigada.
        - 1.3.6. Localizar los ficheros comprimidos relevantes analizarlos, reventar contraseña si es necesario y analizar su contenido.
        - 1.3.7. Localizar algún fichero ejecutable que pueda resultar de interés para la investigación, ademas, analizar la relación con alguna evidencia anterior.
        - 1.3.8. Determinar el contenido del fichero log de un conocido programa de comunicación si es necesario y relacionarlo con el caso investigado.
        - 1.3.9. Realizar un análisis de la navegación web.
        - 1.3.10. Estudio de los dispositivos físicos que en algún momento fueron conectados al sistema estudiado: móviles, **<u style='color:red'>USB's</u>**, impresoras, escáneres, cámaras, tarjetas de memoria.
        - 1.3.11. Estudio de la información contenida en los unallocated cluster o en el file slack.
        - 1.3.12. Información contenida en los archivos de hibernación, paginación, particiones y archivos de intercambio (**<u style='color:red'>swap</u>**).
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
2. Relativo al resumen ejecutivo, elaborarlo teniendo en cuenta los siguientes apartados.
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
3. Elaborar un informe pericial teniendo en cuenta los siguientes apartados.
    - 3.1. Mantener una postura objetiva e imparcial en todo momento.
    - 3.2. Garantizar que el análisis y las conclusiones estén fundamentados en evidencias tangibles y replicables.
    - 3.3. Mantener la **<u style='color:red'>cadena de custodia</u>** y la **<u style='color:red'>integridad</u>** de las pruebas durante todo el proceso.
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
4. Realizar unas conclusiones acordes a todo el TFM realizado.
    - 4.1. Basarse en ideas fuerza que han aparecido durante todo el TFM.
    - 4.2. Tener en cuenta que este apartado es el que finalmente, el gerente de la empresa, como miembro directivo de la misma, usando el método del Presidente Reagan.

#### [1.2. Referencia 001.](#86001-enunciado-tfm) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [1.2. Referencia 003.](#86003-el-método-reagan)

**[Volver al Índice del capítulo 1. Plan de trabajo.](#índice-del-capítulo-1-plan-de-trabajo) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [Volver al Índice General.](#índice-general)**

---

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

## 1.3. Metodologías.

### **1.3.1. Introducción.**

En esta sección se procederá a realizar un repaso general de algunas de las normativas y estándares.

Primero abordaremos un pequeño estudio relativo a las normas ISO 27037 e ISO 30131, posteriormente abordaremos la normativa RFC 3227 para finalmente comentar un resumen de las normas UNE 71505 y UNE 71506.

Por ultimo, pero no menos importante, trataré unas conclusiones sobre esta sección.

**[Volver al Índice del capítulo 1. Plan de trabajo.](#índice-del-capítulo-1-plan-de-trabajo)**

---

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

### **1.3.2. Normas ISO 27037 e ISO 30121.**

Dentro de la seguridad informática cabe destacar una normativa ampliamente conocida, es la familia ISO 27000. Esta serie de normas son estándares de seguridad publicados por la Organización Internacional para la Estandarización (ISO) y la Comisión Electrotécnica Internacional (IEC).

Esta serie contiene diversas normas todas relacionadas con las mejores prácticas recomendadas en Seguridad de la Información para desarrollar, implementar y mantener especificaciones para los Sistemas de Gestión de la Seguridad de la Información (SGSI).

Concretamente, existe una norma dedicada en exclusiva al análisis forense, se trata de la ISO 27037 Directrices para la identificación, recolección, adquisición y preservación de la prueba digital.

Esta norma ofrece orientación para tratar situaciones frecuentes durante todo el proceso de tratamiento de las pruebas digitales. Además define dos roles especialistas:

- **<u style='color:red'>DEFR</u>** **(Digital Evidence First Responders)**: Expertos en primera intervención de evidencias electrónicas.
- **<u style='color:red'>DES</u>** **(Digital Evidence Specialists)**: Experto en gestión de evidencias electrónicas.

ISO 27037 proporciona orientación para los siguientes dispositivos y circunstancias:

- Medios de almacenamiento digitales utilizados en equipos varios como por ejemplo discos duros, disquetes, discos magneto-ópticos y ópticos y otros similares.
- Teléfonos móviles, **<u style='color:red'>PDA's</u>**, tarjetas de memoria.
- Sistemas de navegación móvil (**<u style='color:red'>GPS</u>**).
- Cámaras de video y cámaras digitales (incluyendo circuitos cerrados de televisión).
- Ordenadores estándares con conexiones a redes.
- Redes basadas en protocolos **<u style='color:red'>TCP/IP</u>** y otros protocolos digitales.
- Otros dispositivos con funcionalidades similares a las descritas anteriormente.

Resumiendo, se puede destacar que esta norma ofrece orientación sobre el manejo de las pruebas digitales. Siguiendo las directrices de esta norma se asegura que la evidencia digital potencial se recoge de manera válida a efectos legales para facilitar su aportación en juicios y procesos legales. Además cabe destacar que cubre una amplia gama de tipos de dispositivos y situaciones, por lo que la orientación dentro de la norma es ampliamente aplicable.

Se dispone de una copia de la ISO 27037 en ingles.

#### [1.3.2. Referencia 004](#86004-norma-iso-27037)

La ISO/IEC 30121 es la norma internacional para el análisis forense digital. Define los requisitos mínimos que todas las organizaciones deben cumplir para estar preparados ante un análisis forense digital. La primera edición de la norma se publicó en 2015. Desde entonces, se han realizado varias actualizaciones importantes para reflejar las
nuevas tecnologías y la evolución de los procedimientos de investigación criminal. Ha sido adoptada por muchas organizaciones de todo el mundo como base de las mejores prácticas para el manejo de las pruebas digitales, maximizando la disponibilidad y acceso a esta.

La ISO/IEC 30121 se creó para garantizar que las pruebas digitales se traten de forma coherente en las distintas organizaciones y para ayudar a garantizar que las pruebas digitales puedan utilizarse como prueba en los procedimientos judiciales.

#### [1.3.2. Referencia 005](#86005-implementación-de-herramientas-para-la-extracción-de-evidencia-digital)

**[Volver al Índice del capítulo 1. Plan de trabajo.](#índice-del-capítulo-1-plan-de-trabajo)**

---

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

### **1.3.3. Norma RFC 3227.**

Otra norma destacable para mencionar es la RFC 3227. Este documento publicado por la **<u style='color:red'>Internet Engineering Task Force (IETF)</u>** recoge directrices para recopilar y almacenar evidencias sin ponerlas en riesgo.

En cuanto a los principios para la recolección de evidencias destacan básicamente tres, el orden de volatilidad de los datos, las acciones que deben evitarse y las consideraciones sobre la privacidad.

Sobre el procedimiento de almacenamiento tiene en cuenta la **<u style='color:red'>cadena de custodia</u>** de las pruebas recogidas anteriormente y dónde y cómo se deben almacenar estas para que estén a buen recaudo.

Para acabar detalla qué tipo de herramientas son las más útiles y qué características deben tener para evitar conflictos, haciendo hincapié en que las herramientas deben alterar lo menos posible el escenario. Según este documento el kit de análisis debe incluir las siguientes herramientas:

- Programas para listar y examinar procesos.
- Programas para examinar el estado del sistema.
- Programas para realizar copias bit a bit.

Todas estas recomendaciones tienen como epicentro el principio de intercambio de Locard, que señala que: "siempre que dos objetos entran en contacto transfieren parte del material que incorporan al otro objeto".

Se dispone de una copia de la RFC 3227 en español.

#### [1.3.3. Referencia 006.](#86006-norma-rfc-3227)

**[Volver al Índice del capítulo 1. Plan de trabajo.](#índice-del-capítulo-1-plan-de-trabajo)**

---

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

### **1.3.4. Normas UNE 71505 y UNE 71506.**

Las normas UNE son normas técnicas desarrolladas por el organismo español de normalización, la Asociación Española de Normalización (UNE). "UNE" es el acrónimo de "Una Norma Española". Estas normas establecen especificaciones técnicas, criterios y directrices que deben seguirse en la fabricación, diseño, instalación, uso o mantenimiento de productos, sistemas o servicios en España.

#### [1.3.4. Referencia 007.](#86007-que-son-las-normas-une)

Estas normas que tratamos en el presente trabajo tienen como finalidad dar una metodología para la preservación, adquisición, documentación, análisis y presentación de pruebas digitales.

Según la asociación esta norma debe dar respuesta a las infracciones legales e incidentes informáticos en las distintas empresas y entidades. Con la obtención de dichas pruebas digitales, que serán más robustas y fiables siguiendo la normativa, se podrá discernir si su causa tiene como origen un carácter intencional o negligente.

Estas normativas son de aplicación a cualquier organización con independencia de su actividad o tamaño, así como a cualquier profesional competente en este ámbito. Se dirige especialmente a incidentes y seguridad, así como al personal técnico que trabaje en laboratorios o entornos de análisis forense de evidencias electrónicas.

Se dispone de una copia de la norma UNE 71505.

#### [1.3.4. Referencia 008.](#86005-implementación-de-herramientas-para-la-extracción-de-evidencia-digital)

**[Volver al Índice del capítulo 1. Plan de trabajo.](#índice-del-capítulo-1-plan-de-trabajo)**

---

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

### **1.3.5. Conclusiones relativo a las metodologías.**

Tras analizar los distintos apartados de esta sección y otras fuentes que se indicarán al final de la sección, se puede llegar a la conclusión de que el análisis forense informático recoge de la misma manera la metodología forense per sé, siguiendo la siguiente estructura.

Aunque no existe una metodología que sea única y universal en el análisis forense, a tenor de la documentación consultada y tomando en consideración la normativa legal y los estándares vigentes a nivel internacional, sí que se puede decir que existen una serie de fases o puntos importantes que se tienen que tomar en consideración para que el análisis forense sea adecuado y sirva como elemento probatorio ante un incidente.

Todas estas recomendaciones, recogidas en distintas documentaciones (ver bibliografía), establecen una estructura lógica que permiten garantizar el proceso y que, en el ámbito civil, se compone básicamente de las siguientes fases:

#### [1.3.5. Imagen 001.](#83001003005001-diagrama-de-metodología-del-análisis-forense)

En cada una de las fases indicadas en la imagen anterior podemos destacar las siguientes tareas.

#### [1.3.5. Imagen 002.](#83001003005002-fases-1-2-y-3-de-la-metodología-del-análisis-forense) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [1.3.5. Imagen 003.](#83001003005003-fases-4-5-y-6-de-la-metodología-del-análisis-forense) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [1.3.5. Imagen 004.](#83001003005004-fase-7-de-la-metodología-del-análisis-forense)

**PLANTEAMIENTO DEL PROBLEMA.**

En el caso de que nos trata el presente TFM, estas acciones de planteamiento del problema, nos viene dado en el enunciado, ya que el enunciado, se expresa claramente que el jefe de la empresa tiene serias sospechas, no probadas, de que se ha accedido de forma licita al sistema, y por tanto, en primera instancia se requieren nuestras acciones relativo al asunto.

Entrando en el trasfondo de la legalidad y posible contaminación de pruebas, ante un presunto delito que este tipificado en el código penal, suelen ser las Fuerzas y Cuerpos de Seguridad del estado los que, bajo la orden de un juzgado de instrucción, las competentes en realizar este análisis forense por un presunto hecho

**IDENTIFICACIÓN.**

En el caso del presente TFM, en el enunciado hemos recibido y el material didáctico que se adjunta, se han realizado previamente y satisfactoriamente todos los pasos de esta metodología.

Cabe destacar en uno de las tareas dedicadas a la identificación, nos encontramos con la tarea de asegurar la escena, es recomendable realizar las siguientes acciones:

1. Realizar fotografías del entorno del equipo para evidenciar el estado original de la escena, identificando así el perímetro de la escena a analizar y protegiéndolo de accesos de personal no autorizado.

2. Proteger las huellas dactilares que pueda haber en los equipos para que los demás cuerpos y unidades de policía e investigadores puedan realizar su tarea. Es por lo tanto recomendable el uso de guantes de látex o similar para esta finalidad. En este punto se recuerda el principio de intercambio de Locard ya citado en el [apartado 1.3.3](#133-norma-rfc-3227).

3. Anotar la hora y fecha de los equipos implicados que no tiene por qué coincidir con la real, esto es importante para la investigación posterior y para la realización de una línea temporal con todos los sucesos que han ocurrido. En caso de haber desfase entre la hora del equipo y la real, este desfase se tiene que documentar para tenerlo en cuenta posteriormente. La captura de la hora y fecha se puede realizar fotografiando la pantalla o grabando un vídeo de la misma, siempre y cuando no haya que manipular el equipo para ello.

4. Ver si en pantalla hay algún proceso que nos aporte información útil sobre lo que esté pasando en directo, en ese caso, grabar todo lo que ocurre. Es importante valorar las entradas y salidas de los equipos, pues nos pueden aportar pistas importantes. De igual modo con otros periféricos de entrada/salida, tales como impresoras, teléfonos IP, escáneres, etcétera.

**ADQUISICIÓN.**

Llegados a esta fase, la cual ya ha sido previamente realizada a la elaboración del TFM, cabe destacar la tarea de establecer el orden de prioridad de la recolección de las evidencias. Para ello, hay que tener en cuenta una serie de principios acerca de la identificación de las evidencias y más específicamente sobre la volatilidad de las mismas. Es vital conocer qué datos son más o menos volátiles, identificarlos correctamente y posteriormente proceder a su recolección.

Entendemos por volatilidad de los datos el período de tiempo en el que estarán accesibles en el equipo. Por lo tanto, se deberán recolectar previamente aquellas pruebas más volátiles. Según la RFC 3227, el que se presenta a continuación, es un posible orden de volatilidad de mayor a menor:

#### [1.3.5. Imagen 005.](#83001003005005-orden-de-volatilidad-análisis-forense)

Como ya se ha indicado previamente, si se quiere realizar una depuración de responsabilidades de manera penal, es necesario establecer una autoridad legal que presente la recogida de evidencias, ya sea un secretario judicial o un notario.

La ultima tarea de esta fase es la recogida de evidencias, para ello se realiza una copia bit a bit de los discos que se quieran analizar, es decir, se requiere una copia exacta del contenido de los discos incautados. Esto incluye todos los archivos del disco, por ejemplo los temporales, los ocultos, los de configuración, los eliminados y no sobrescritos y la información relativa a la parte del disco no asignada, es lo que se conoce como copia a bajo nivel.

Esta copia se llevará a cabo sobre un soporte limpio mediante un borrado seguro de los datos que pudiera contener anteriormente para evitar así contaminaciones con otros casos.

**PRESERVACIÓN.**

Esta accion, se ha realizado al igual que las anteriores, ha sido realizada de manera previa a la elaboración del TFM, para ello se tienen que tener en cuenta las siguientes consideraciones.

Una vez realizada la copia se debe verificar la **<u style='color:red'>integridad</u>** de la misma. Para ello se calcula el **<u style='color:red'>hash</u>** o **<u style='color:red'>CRC</u>** de la copia, normalmente los equipos destinados al clonado de discos ya incorporan esa característica. Así con el **<u style='color:red'>hash</u>** del disco original y el de la copia se puede certificar que ambos son idénticos a todos los niveles y ante un juez, por ejemplo, quedará probado que no se ha manipulado de ningún modo. Con este procedimiento también nos aseguraremos que no se han producido errores en la copia.

Con la primera copia realizada y comprobada procedemos a realizar una segunda copia sobre la primera. En este caso también se comprobará que el contenido es idéntico mediante el mismo proceso descrito anteriormente. Teniendo ambas copias entregaremos la primera al secretario judicial o notario responsable del caso y nos quedaremos con la segunda para poder trabajar. La segunda copia será nuestra copia de respaldo en todo momento en el laboratorio y no será para trabajar directamente con ella en ningún caso. Para realizar el análisis se deberá realizar una tercera copia, comprobar su **<u style='color:red'>integridad</u>** y trabajar sobre ella, de tal modo que en caso de cualquier desastre o alteración de los datos siempre tengamos la segunda copia exacta al original de donde poder volver a realizar otra copia para analizar.

Una mala preservación de las evidencias, un mal uso o una mala manipulación pueden invalidar toda la investigación que se lleva a cabo delante de un tribunal, este es un factor muy importante que se va repitiendo a lo largo de toda la metodología.

La **<u style='color:red'>cadena de custodia</u>** es el procedimiento controlado aplicable a las evidencias relacionadas con el suceso, desde el momento en que se encuentran en la escena hasta su análisis en el laboratorio. La finalidad de la **<u style='color:red'>cadena de custodia</u>** es evitar cualquier tipo de manipulación y tener un control absoluto sobre todos los elementos incautados, quién los ha manipulado, cómo lo ha realizado, porqué los ha manipulado, para qué lo ha hecho y cuándo ha tenido lugar dicha manipulación.

Es importante realizar todas las anotaciones descritas en la fase de identificación de las evidencias para que esta fase sea aún más sólida. Con todos los elementos documentados será mucho más fácil tener un control de todas las evidencias que disponemos y poder realizar una traza de todas las pruebas adquiridas.

Además se tendrá en cuenta de proteger los bienes para el transporte desde el lugar de los hechos hasta el laboratorio con los medios necesarios para evitar golpes o proteger de caídas fortuitas.

La documentación de la **<u style='color:red'>cadena de custodia</u>** deberá contener también todos los lugares por donde ha pasado la evidencia y quién ha realizado su transporte y su acceso.

En nuestro caso, cabe destacar que una vez iniciado el análisis de la memoria, esta no debe de modificarse ni contaminarse, en caso de ello el **<u style='color:red'>Hash</u>** de las evidencias cambiaría, por lo que la evidencia ha quedado contaminada. Hay que hacer estas acciones teniendo presente al secretario judicial, para que esa copia quede registrada si es necesario y que no ha habido mas alteraciones al respecto, ese cambio de **<u style='color:red'>hash</u>** será notificado y adjuntado en el proceso de instrucción, haciéndose también nuevas copias de este nuevo "snapshot" de la prueba.

**ANÁLISIS.**

La fase de análisis, ***en la cual iniciamos la elaboración del presente TFM,*** no termina hasta que no se puede determinar qué o quién causó el incidente, cómo lo hizo, qué afectación ha tenido en el sistema, etc. Es decir, es el núcleo duro de la investigación y tiene que concluir con el máximo de información posible para poder proceder a elaborar unos informes con todo el suceso bien documentado.

Antes de empezar el análisis, es importante recordar unas premisas básicas que todo investigador debe tener presente en el momento de enfrontarse al incidente. Como ya se ha explicado nunca se debe trabajar con datos originales y se debe respetar cada una de las leyes vigentes en la jurisdicción donde se lleve a cabo la investigación. Los resultados que se obtengan de todo el proceso han de ser verificables y reproducibles, así que en cualquier momento debemos poder montar un entorno donde reproducir la investigación y mostrarlo a quién lo requiera. Es importante también disponer de una documentación adicional con información de diversa índole, por ejemplo:

- Sistema operativo del sistema.
- Programas instalados en el equipo.
- Hardware, accesorios y periféricos que forman parte del sistema.
- Datos relativos a la conectividad del equipo:
    - Si dispone de **<u style='color:red'>firewall</u>**, ya sea físico o lógico.
    - Si el equipo se encuentra en zonas de red especiales, por ejemplo, **<u style='color:red'>DMZ</u>**.
    - Si tiene conexión a Internet o utiliza **<u style='color:red'>proxies</u>**.
- Datos generales de configuración que puedan ser de interés para el investigador
para ayudar en la tarea.

Para ayudar al desarrollo de esta fase del análisis forense podemos centrarnos en varias subfases o puntos importantes que generalmente siempre deben realizarse. Cabe recordar que no existe ningún proceso estándar que ayude a la investigación y habrá que estudiar cada caso por separado teniendo en cuentas las diversas particularidades que nos podamos encontrar. No será lo mismo analizar un equipo con sistema operativo Windows o con Linux. Tampoco será lo mismo un caso de intrusión en el correo electrónico de alguien o un ataque de denegación de servicio a una institución. De igual forma no actuaremos con los mismos pasos en un caso de instalación de un malware que destruya información de una ubicación de disco o un malware que envíe todo lo que se teclea en un equipo.

En todo caso, se pueden destacar varios pasos, que habrá que adaptar en cada caso:

- Preparar un entorno de trabajo adaptado a las necesidades del incidente.
- Reconstruir una línea temporal con los hechos sucedidos.
- Determinar qué procedimiento se llevó a cabo por parte del atacante.
- Identificar el autor o autores de los hechos.
- Evaluar el impacto causado y si es posible la recuperación del sistema.

Antes de empezar el análisis propiamente, se debe preparar un entorno para dicho análisis. Es el momento de decidir si se va a hacer un análisis en caliente o en frío.

En caso de un análisis en caliente se hará la investigación sobre los discos originales, lo que conlleva ciertos riesgos. Hay que tomar la precaución de poner el disco en modo sólo lectura, esta opción sólo está disponible en sistemas operativos Linux pero no en Windows. Si se opta por esta opción hay que operar con sumo cuidado pues cualquier error puede ser fatal y dar al traste con todo el proceso, invalidando las pruebas.

Si se opta por un análisis en frío, lo más sencillo es preparar una máquina virtual con el mismo sistema operativo del equipo afectado y montar una imagen del disco. Para ello, previamente habremos creado la imagen a partir de las copias que se hicieron para el análisis. En este caso podremos trabajar con la imagen, ejecutar archivos y realizar otras tareas sin tanto cuidado, pues siempre cabe la opción de volver a montar la imagen desde cero en caso de problemas.

La opción del análisis en frío, ***La cual será el caso que nos atañe el presente TFM, ya que der este modo es como se realizará el análisis***, resulta muy atractiva pues en caso de malwares se podrán ejecutar sin miedo, reproducir lo que ocurre y desmontar la imagen sin que la copia original resulte afectada. De este modo tal vez se pueda ir un poco más allá en la investigación y ser
un poco más agresivo.

Existen varios programas gratuitos para crear y gestionar máquinas virtuales, por ejemplo,
Oracle VM VirtualBox, que ofrecen muy buenas prestaciones.

Para la tarea de construir una cadena de acontecimientos y hacer una linea temporal cabe destacar lo siguiente.

Para crear la línea temporal, lo más sencillo es referirnos a los tiempos MACD de los archivos, es decir, las fechas de modificación, acceso, cambio y borrado, en los casos que aplique. Es importante, como ya se ha indicado en alguna ocasión tener en cuenta los husos horarios y que la fecha y hora del sistema no tienen por qué coincidir con los reales. Este dato es muy importante para poder dar crédito a las pruebas y a la investigación en general.

Para empezar, lo mejor es determinar la fecha de instalación del sistema operativo, para ello se puede buscar en los datos de registro. Además la mayoría de ficheros del sistema compartirán esa fecha. A partir de aquí puede ser interesante ver qué usuarios se crearon al principio, para ver si hay discrepancias o usuarios fuera de lo común en últimos instantes del equipo. Para ver esta información también es útil acudir al registro del sistema operativo.

Teniendo ya los datos iniciales del sistema, ahora se puede proceder a buscar más información en los ficheros que se ven "a simple vista". Lo importante es localizar que programas fueron los últimos en ser instalados y qué cambios repercutieron en el sistema. Lo más habitual es que estos programas no se instalen en los lugares habituales, sino que se localicen en rutas poco habituales, por ejemplo en archivos temporales o mezclados con los archivos y librerías del sistema operativo. Aquí se puede ir creando la línea temporal con esos datos.

Alternativamente es útil pensar que no todos los archivos están a la vista. Se puede encontrar información en archivos normales, pero también en temporales, ocultos, borrados o usando técnicas como la esteganografía, no se puede obviar ninguna posibilidad.

Habitualmente los sistemas operativos ofrecen la opción de visualizar los archivos ocultos y también las extensiones. Es útil activar estas opciones para detectar posibles elementos ocultos y extensiones poco habituales que nos resulten extrañas.

Para los archivos borrados se utilizaran programas especiales capaces de recuperar aquellos datos que se hayan eliminado del disco pero sobre los cuales aún no se haya sobrescrito nada. Es posible que el atacante elimine archivos o registros varios en afán de esconder lo que ha ocurrido, si estos no han sido sobrescritos se podrán recuperar y se podrán situar en la línea temporal relacionándolos con el conjunto de sucesos. Para recuperar información oculta mediante esteganografía también se deberán usar programas concretos. Es posible que el atacante ocultara información sobre otros archivos, tales como imágenes o audio para enviarlos posteriormente o tenerlos almacenados sin llamar la atención. Habitualmente hallaremos más información en ubicaciones ocultas que en los lugares más habituales.

Con todos estos datos se debería poder crear un esbozo de los puntos clave en el tiempo tales como la instalación del sistema, el borrado de determinados archivos, la instalación de los últimos programas, etcétera.

El siguiente paso del análisis es determinar el ***como se actuó***. Para determinar cómo se actuó es importante llevar a cabo una investigación sobre la memoria del equipo. Es interesante realizar un volcado de memoria para la obtención de cierta información. Con programas destinados a tal fin podremos ver que procesos se están ejecutando en el momento concreto y también aquellos que hayan sido ocultados para no levantar sospechas. Con esta información podremos saber qué ejecutables inician los procesos en ejecución y qué librerías se ven involucradas. Llegados aquí se puede proceder a realizar volcados de los ejecutables y de dichas librerías para poder analizar si contienen cadenas sospechosas o si, por lo contrario, son archivos legítimos. Sabiendo los procesos que se ejecutan y su naturaleza podemos obtener pistas de cómo se actuó para comprometer el equipo.

A menudo nos deberemos fijar en procesos en ejecución aparentemente inofensivos, habituales y legítimos en los sistemas operativos. No es extraño que determinados procesos con fines malintencionados se camuflen con procesos legítimos. Para ello deberemos observar que muchas veces estos se encuentran sin un proceso padre, cuando lo más habitual es que dependan de otros. En otras ocasiones simplemente se camuflan con nombres muy parecidos a otros para pasar desapercibidos.

Ciertos programas también nos darán información sobre las cadenas del ejecutable en cuestión. Con ellas podremos ver si mutan su contenido cuando se ejecutan en memoria y cuál es su contenido. En ocasiones, cierta información de las cadenas nos puede dar pistas muy valiosas, como por ejemplo, cadenas dónde encontrar logs, o enlaces a direcciones de Internet. También nos puede dar pistas sobre el tipo de malware al que nos enfrentamos. Si por ejemplo encontramos cadenas con alfabetos o teclas concretas del teclado, es probable que nos encontremos ante un keylogger.

Finalmente, otra práctica interesante para determinar cómo se actuó es leer la secuencia de comandos escrita por consola. Para ello procederemos con el volcado de memoria y podremos obtener dicha información. De este modo podremos leer que comandos se hicieron por consola y sabremos si se ejecutó algún proceso de este modo. Debemos excluir nuestras propias instrucciones pues seguramente aparecerán los comandos del volcado de memoria que se hicieron en su momento. Relativo a esta práctica, personalmente es la primera que se debería de realizar en un análisis forense, de ahi también poder corroborar que es lo que pueda decir el usuario en una posible entrevista, que en este caso no va a ser posible.

Para la tarea de identificación de autores, cabe destacar que para poder realizar una identificación del autor o autores del incidente, otra información importante que nos puede dar el volcado de memoria son las conexiones de red abiertas y las que están preparadas para enviar o recibir datos. Con esto podremos relacionar el posible origen del ataque buscando datos como la dirección **<u style='color:red'>IP</u>** en Internet.

Hay que actuar con prudencia puesto que en ocasiones se utilizan técnicas para distribuir los ataques o falsear la dirección **<u style='color:red'>IP</u>**. Hay que ser crítico con la información que se obtiene y contrastarla correctamente. No siempre se obtendrá la respuesta al primer intento y posiblemente en ocasiones sea muy difícil averiguar el origen de un incidente.

Es interesante recapacitar en los distintos perfiles de atacantes que se pueden dar hoy día en este ámbito para intentar mimetizarse y entender quién pudo ser el autor.

Por un lado podemos encontrar organizaciones y criminales que actúan por motivaciones económicas. Su finalidad es robar cierta información, ya sea empresarial o personal, para una vez obtenida venderla o sacar un rendimiento oneroso de la información.

Por otro lado está quién sólo busca acceder a sistemas por mero prestigio y reconocimiento en su ambiente cibernético. Accediendo a sistemas mal configurados y publicando datos que prueben su fechoría incrementará su notoriedad y se dará a conocer más en las redes.

En este punto es importante analizar dos vertientes. En caso que se esté realizando un peritaje con fines inculpatorios, o sea, judiciales, se deberá intentar resolver quién es el autor o al menos aportar pistas fiables para que otros investigadores puedan llevar a cabo otras investigaciones de otros ámbitos.

En cambio, si es con fines correctivos lo más interesante seguramente será obviar esta fase y proceder con el estudio del impacto causado y estudiar las mejoras que se pueden implantar para evitar episodios similares.

Para establecer el impacto causado, cabe destacar que se puede calcular en base a distintos factores y no hay un método único para su cálculo, ni una fórmula que nos dé un importe económico. Aun así para estos cálculos puede servir ayudarse de métodos como BIA (Business Impact Analysis) que determinan el impacto de ciertos eventos ayudando a valorar los daños económicamente.

A la larga cualquier incidente ocurrido devengará en unos gastos económicos que habrá que cuantificar en función de los ítems afectados tras el suceso. En ocasiones el coste económico resultará de tener que reemplazar una máquina o dispositivo que ha quedado inservible tras un ataque o bien las horas de empleado de tener que reinstalar el sistema. En este caso, el cálculo no supone mayor dificultad y se resuelve fácilmente.

En otras ocasiones, por ejemplo, los daños pueden deberse al robo de una información de secreto industrial en el que habrá que cuantificar no sólo qué supone reponer el sistema sino, a la larga, en qué se verá afectada la empresa. Los datos robados pueden ser para publicar cierta información sobre la empresa y poner en la opinión pública datos con intenciones de crear mala imagen, lo cual supone un daño incalculable y muy elevado para la empresa.

El impacto no sólo se puede calcular en base económica. Como ya se ha comentado al inicio de esta sección también existen otros factores, es el caso del tiempo de inactividad. Si el incidente ha supuesto paralizar la producción de una planta automatizada de fabricación esto supone muchas horas en que la producción es nula, por lo tanto no se trabajará. Evidentemente, a la larga también supondrá un problema económico pues no se podrán servir los pedidos pendientes de los clientes. Si la paralización afecta a una oficina, tal vez no se pare la producción de bienes pero sí el trabajo de los empleados que verán retrasado todo su trabajo.

**PRESENTACIÓN.**

La última fase de un análisis forense queda para redactar los informes que documenten los antecedentes del evento, todo el trabajo realizado, el método seguido y las conclusiones e impacto que se ha derivado de todo el incidente.

Para ello se redactarán dos informes, a saber, el informe técnico y el ejecutivo. En esencia en ambos informes se explican los mismos hechos pero varía su enfoque y el grado de detalle con que se expone el asunto.

- En el informe ejecutivo se usará un lenguaje claro y sin tecnicismos, se debe evitar usar terminología propia de la ciencia e ingeniería y expresiones confusas para gente no ducha en el tema. Hay que pensar que el público lector de estos informes serán jueces y gerentes que seguramente estén poco relacionados con el tema y además tengan poco tiempo para dedicarle. Se les debe facilitar la tarea al máximo.

- En el informe técnico, por el contrario, el público final será técnico y con conocimientos de la materia que se expone. Aquí se detallarán todos los procesos, los programas utilizados, las técnicas, etcétera. Debemos crear un documento que pueda servir de guía para repetir todo el proceso que se ha realizado en caso necesario.

Relativo al informe ejecutivo, cabe destacar que será un resumen de toda la tarea que se ha llevado a cabo con las evidencias digitales. Aunque será un documento de poca extensión, al menos comparado con el informe técnico, éste deberá contener al menos los siguientes apartados:
- Motivos de la intrusión.
    - ¿Por qué se ha producido el incidente?
    - ¿Qué finalidad tenía el atacante?
- Desarrollo de la intrusión.
    - ¿Cómo lo ha logrado?
    - ¿Qué ha realizado en los sistemas?
- Resultados del análisis.
    - ¿Qué ha pasado?
    - ¿Qué daños se han producido o se prevén que se producirán?
    - ¿Es denunciable?
    - ¿Quién es el autor o autores?
- Recomendaciones.
    - ¿Qué pasos dar a continuación?
    - ¿Cómo protegerse para no repetir los hechos?

El informe técnico será más largo que el anterior y contendrá mucho más detalle. Se hará una exposición muy detallada de todo el análisis con profundidad en la tecnología usada y los hallazgos. En este caso se deberá redactar, al menos:

- Antecedentes del incidente.
    - Puesta en situación de cómo se encontraba la situación anteriormente al incidente.
- Recolección de datos.
    - ¿Cómo se ha llevado a cabo el proceso?
    - ¿Qué se ha recolectado?
- Descripción de la evidencia.
    - Detalles técnicos de las evidencias recolectadas, su estado, su contenido,
etc.
- Entorno de trabajo del análisis.
    - ¿Qué herramientas se han usado?
    - ¿Cómo se han usado?
- Análisis de las evidencias.
    - Se deberá informar del sistema analizado aportando datos como las características del sistema operativo, las aplicaciones instaladas en el equipo, los servicios en ejecución, las vulnerabilidades que se han detectado y la metodología usada.
- Descripción de los resultados.
    - ¿Qué herramientas ha usado el atacante?
    - ¿Qué alcance ha tenido el incidente?
    - Determinar el origen del mismo y como se ha encontrado.
- Dar la línea temporal de los hechos ocurridos con todo detalle.
- Redactar unas conclusiones con las valoraciones que se crean oportunas a la vista de todo el análisis realizado.
- Dar unas recomendaciones sobre cómo proteger los equipos para no repetir el incidente o sobre cómo actuar legalmente contra el autor.

#### [1.3.5. Referencia 008.](#86008-metodología-para-un-análisis-forense) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [1.3.5. Referencia 009.](#86009-ninjas-de-la-web-metodología-para-un-análisis-forense)

**[Volver al Índice del capítulo 1. Plan de trabajo.](#índice-del-capítulo-1-plan-de-trabajo) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [Volver al Índice General.](#índice-general)**

---

<br>

## 1.4. Descripción del entorno de trabajo.

El entorno de trabajo para un análisis forense enfocado en la exploración de memoria RAM y disco duro exige una meticulosa preparación y adecuación de las herramientas y espacios de trabajo. Las evidencias, provenientes tanto de la RAM como del almacenamiento persistente del ordenador en cuestión, se convierten en el pilar fundamental del análisis, permitiendo la evaluación de procesos en ejecución, archivos almacenados, registros de actividad y cualquier otro elemento que pueda arrojar luz sobre las acciones realizadas en la máquina.

En un segundo plano, pero no menos esencial, se encuentra el portátil personal, que se configura como la estación de trabajo principal para la realización del análisis forense. Este debe estar equipado con un sistema operativo que, comúnmente en el ámbito forense, suele ser alguna distribución de Linux, junto con una serie de herramientas específicas para el análisis forense (como Autopsy o Sleuth Kit). No obstante, la selección y configuración de estas herramientas incurren en una deuda técnica que debe ser minuciosamente administrada, asegurando la pertinencia, licencia y compatibilidad de las mismas.

Relativo al ordenador personal destacar las siguientes aplicaciones que se van a utilizar para la realización del análisis.

- VirtualBox
- Volatility

**DEUDA TÉCNICA: Listado de aplicaciones a utilizar en la descripción del entorno de trabajo**

Por otro lado, la documentación y redacción del TFM se consolida mediante el uso del repositorio en GitHub TFM-ANÁLISIS-FORENSE (https://github.com/jrodg85/TFM-ANALISIS-FORENSE). Este repositorio no solo sirve como medio para documentar y presentar los hallazgos y metodologías empleadas, sino que también se erige como una herramienta para gestionar versiones y cambios a lo largo del desarrollo del trabajo, facilitando la trazabilidad y coherencia del mismo. Se deben establecer estrategias robustas para garantizar la **<u style='color:red'>integridad</u>** y confidencialidad de la información almacenada, considerando la naturaleza sensible de los datos manejados en la investigación forense.

Finalmente, Internet emerge como un recurso invaluable para la investigación, actualización y comunicación a lo largo del proyecto. Navegar por la red debe ser realizado de forma segura y consciente, protegiendo las comunicaciones y asegurando la **<u style='color:red'>integridad</u>** de las herramientas y datos descargados.

**[Volver al Índice del capítulo 1. Plan de trabajo.](#índice-del-capítulo-1-plan-de-trabajo) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [Volver al Índice General.](#índice-general)**

---

<br><br><br><br><br><br><br><br><br><br>

## 1.5. Listado de tareas.

En esta sección se ha elaborado después de una planificación del trabajo, el cual se han designado el siguiente listado de tareas a realizar. Gracias a este listado, podemos organizar el cómo vamos a realizar el TFM

Destacar que durante el listado de las tareas, cabe mencionar que habrán tareas de grooming o refinamiento, ellas no son utilizadas para reducción de deuda técnica, el objetivo estas jornadas es reflexionar sobre el contenido del mismo y valorar posibilidad de mejorar la organización del mismo. Estas variaciones, gracias a que se está realizando un control de versiones con git, se podrán ver las evoluciones o cambios del TFM en el mismo.

Durante la elaboración del reto 1 (PEC 1), se realizarán las siguientes tareas:

1. Lectura enunciado actividad 1.
2. Decision de formato de TFM.
3. Maquetación de TFM en LaTeX.
4. Elaboración de índice.
5. Refinamiento de TFM 1.
6. Diagrama de Gantt.
7. Problema a resolver.
8. Objetivos.
9. Revisión del estado del arte de la informática forense.
10. Refinamiento de TFM 2.

Durante la elaboración del reto 2 (PEC 2), se realizarán las siguientes tareas:

1. Lectura enunciado actividad 2.
2. Extremos de análisis y previsión de pruebas: Introducción.
3. Extremos de análisis.
4. Previsión de pruebas.
5. Análisis de la memoria RAM: Introducción.
6. Acciones previas al análisis de RAM.
7. Búsqueda de procesos en funcionamiento.
8. Análisis y extracción de procesos sospechosos.
9. Listado de conexiones de red y conexiones sospechosas.
10. Refinamiento TFM 3.
11. Feedback de la PEC 01.
12. Análisis de disco duro: Introducción.
13. Acciones previas al análisis de disco duro.
14. Datos de interés y usuarios del sistema del disco duro analizado.
15. Análisis de las evidencias del disco duro.
16. Planning relativo al resumen ejecutivo.
17. Planning relativo al informe pericial.
18. Adaptación al indice a los nuevos cambios en los capítulos 6 y 7.
19. Refinamiento TFM 4.

Durante la elaboración del reto 3  (PEC 3), se realizarán las siguientes tareas:

1. Lectura enunciado actividad 3.
2. Introducción Resumen ejecutivo.
3. Análisis Ejecutivo.
4. Conclusión de análisis ejecutivo.
5. Refinamiento TFM 5.
6. Feedback de la PEC 02.
7. Introducción del informe pericial.
8. Cuerpo del informe pericial.
9. Conclusiones del informe pericial.
10. Conclusiones TFM.
11. Revision de términos abreviaturas y acrónimos.
12. Revisión de imágenes.
13. Revision de referencias.
14. Refinamiento TFM 6.

Durante la elaboración del reto 4  (PEC 4), se realizarán las siguientes tareas.

1. Revisión de las anotaciones y consejos de la tutora de TFM 1.
2. Ultimas correcciones Feedback TFM 1.
3. Revisión de las anotaciones y consejos de la tutora de TFM 2.
4. Ultimas correcciones Feedback TFM 2.

La Entrega de videos, presentación y realización de la defensa del TFM, se consideran que están fuera de este TFM, ya que a partir de la fecha se considera entregado el presente documento.

**[Volver al Índice del capítulo 1. Plan de trabajo.](#índice-del-capítulo-1-plan-de-trabajo) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [Volver al Índice General.](#índice-general)**

---

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

## 1.6. Planificación temporal de las tareas.

Para esta sección, se han elaborado los siguientes diagramas de Gantt relativos a cada uno de los retos a entregar.

Relativo al reto/PEC 1 se establece el siguiente diagrama:

#### [1.6. Imagen 001.](#83001006001-diagrama-de-gantt-retopec-1)

Relativo al reto/PEC 2 se establece el siguiente diagrama.

#### [1.6. Imagen 002.](#83001006002-diagrama-de-gantt-retopec-2)

Relativo al reto/PEC 3 se establece el siguiente diagrama.

#### [1.6. Imagen 003.](#83001006003-diagrama-de-gantt-retopec-3)

Relativo al reto/PEC 4 se establece el siguiente diagrama.

#### [1.6. Imagen 004.](#83001006004-diagrama-de-gantt-retopec-4)

**[Volver al Índice del capítulo 1. Plan de trabajo.](#índice-del-capítulo-1-plan-de-trabajo) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [Volver al Índice General.](#índice-general)**

---

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

## 1.7. Revisión del estado del arte de la informática forense.

### **1.7.1. Introducción del estado del arte de la informática forense.**

El análisis forense, también llamado informática forense, computación forense, análisis forense digital o examen forense digital es la aplicación de técnicas científicas y analíticas especializadas a infraestructuras tecnológicas que permiten identificar, preservar, analizar y presentar datos válidos dentro de un proceso legal.

Dichas técnicas incluyen reconstruir elementos informáticos, examinar datos residuales, autenticar datos y explicar las características técnicas del uso de datos y bienes informáticos.

Esta disciplina no sólo hace uso de tecnologías de punta para mantener la **<u style='color:red'>integridad</u>** de los datos y del procesamiento de los mismos; sino que también requiere de una especialización y conocimientos avanzados de informática y sistemas para identificar lo que ha ocurrido dentro de cualquier dispositivo electrónico. La formación de un informático forense abarca no sólo el conocimiento del software, sino también de hardware, redes, seguridad, piratería, hackeo y recuperación de información.

La informática forense ayuda a detectar pistas sobre ataques informáticos, robos de información, conversaciones o para recolectar evidencias en correos electrónicos y chats.

La evidencia digital o electrónica es sumamente frágil, de ahí la importancia de mantener su integridad; por ejemplo, el simple hecho de pulsar dos veces en un archivo modificaría la última fecha de acceso del mismo.

Dentro del proceso del análisis forense, un examinador forense digital puede llegar a recuperar información que haya sido borrada desde el sistema operativo. El informático forense debe tener muy presente el principio de intercambio de Locard por su importancia en el análisis criminalístico, así como el estándar de Daubert para hacer admisibles en juicio las pruebas presentadas por el experto forense.

Es muy importante mencionar que la informática o el análisis forense no tiene como objetivo prevenir delitos, por lo que resulta imprescindible tener claros los distintos marcos de actuación de la informática forense, la seguridad informática y la auditoría informática.

**[Volver al Índice del capítulo 1. Plan de trabajo.](#índice-del-capítulo-1-plan-de-trabajo)**

---

<br><br><br><br><br><br><br><br><br><br><br><br><br><br>

### **1.7.2. Definiciones.**

Existen diferentes términos referentes a la ciencia forense en informática. Cada uno de estos términos trata de manera particular o general temas que son de interés para las ciencias forenses.

**Computación forense (computer forensics).**

1. Disciplina de la ciencia forense que considera los procedimientos en relación con las evidencias para descubrir e interpretar la información en los medios informáticos con el fin de establecer hipótesis o hechos relacionados con un caso. (Centrada en las consideraciones forenses).

2. Disciplina científica que ofrece un análisis de la información que contienen las tecnologías y de los equipos de computación a partir de su compresión.(Centrada en la tecnología).

**Ciencia forense en las redes (network forensics).**

1. Trata las operaciones de redes de computadores, estableciendo rastros e identificando movimientos y acciones. Es necesario entender los protocolos, configuraciones y la infraestructura de las comunicaciones. A diferencia de la computación forense, es necesario poder establecer relaciones entre eventos diferentes e incluso aleatorios.

**Ciencia forense digital (digital forensics).**

1. Es una forma de aplicar los conceptos y procedimientos de la criminalística a los medios informáticos o digitales. Su objetivo es apoyar al poder judicial en el contexto de la inseguridad informática es decir, la perpetración de posibles delitos aclarando temas relacionados con incidentes o fraudes.

**[Volver al Índice del capítulo 1. Plan de trabajo.](#índice-del-capítulo-1-plan-de-trabajo)**

---

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

### **1.7.3. Objetivos de la informática forense.**

La informática forense tiene tres objetivos:

1. La compensación de los daños causados por los intrusos o criminales.
2. La persecución y procesamiento judicial de los criminales.
3. La creación y aplicación de medidas para prevenir casos similares.


Estos objetivos se alcanzan de varias formas, siendo la principal la recopilación de evidencias.

Es importante mencionar que quienes se dedican a la informática forense deben ser profesionales con altos niveles de ética, pues gracias a su trabajo se toman decisiones sobre los hechos y casos analizados.

**[Volver al Índice del capítulo 1. Plan de trabajo.](#índice-del-capítulo-1-plan-de-trabajo)**

---

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

### **1.7.4. Evidencia digital.**

Los discos duros, las memorias **<u style='color:red'>USB</u>** y las impresoras (entre otros elementos) se pueden considerar evidencias en un proceso legal, al igual que las huellas digitales o las armas. Las evidencias digitales son las que se extraen de un medio informático.

**Características.**

Estas evidencias comparten una serie de características que dificultan el ejercicio de la computación forense:

1. Volatilidad.
2. Anonimato.
3. Facilidad de duplicación.
4. Alterabilidad.
5. Facilidad de eliminación.

**Categorías.**

Estas evidencias se pueden dividir en tres categorías:

- Registros almacenados en el equipo de tecnología informática (ej. imágenes y correos).
- Registros generados por equipos de tecnología informática (ej. transacciones, registros en eventos).
- Registros parcialmente generados y almacenados en los equipos de tecnología informática (ej. consultas en bases de datos).

**Dispositivos a analizar.**

Cualquier infraestructura informática que tenga una memoria (almacenamiento) es susceptible a los análisis:

- Disco duro de una Computadora o Servidor.
- Documentación referente al caso.
- Tipo de sistema de telecomunicaciones.
- Dirección **<u style='color:red'>MAC</u>**.
- Inicios de sesiones.
- Información de los cortafuegos.
- **<u style='color:red'>IP</u>**, redes **<u style='color:red'>Proxy</u>**. **<u style='color:red'>LMhost</u>**, host, conexiones cruzadas, pasarelas.
- Software de supervisión y seguridad.
- Credenciales de autentificación.
- Rastreo de paquetes de red.
- Teléfonos móviles o celulares (telefonía móvil)
- Agendas electrónicas (**<u style='color:red'>PDA</u>**).
- Dispositivos de **<u style='color:red'>GPS</u>**.
- Impresoras.
- Memorias **<u style='color:red'>USB</u>**.
- **<u style='color:red'>BIOS</u>**.

**[Volver al Índice del capítulo 1. Plan de trabajo.](#índice-del-capítulo-1-plan-de-trabajo)**

---

<br><br>

### **1.7.5. Perspectiva de tres roles.**

En el análisis de un caso en el que sea necesario el cómputo forense, hay tres roles principales que son importantes y se deben tener en cuenta: el intruso, el administrador y la infraestructura de la seguridad informática, al igual que el investigador.

**Intrusos.**

El intruso es aquel que ataca un sistema, hace cambios no autorizados, manipula contraseñas o cambia configuraciones, entre otras actividades que ponen a prueba la seguridad de un sistema. La intención de los intrusos es un punto clave para poder analizar el caso, ya que no se puede comparar un intruso cuya motivación es el dinero con otro cuya motivación es la demostración de sus habilidades. Jeimy J. Cano hace una comparación entre las motivaciones de diferentes tipos de atacantes en la siguiente tabla, basada en el artículo de Steven Furnell Cybercrime.

| Motivaciones | **<u style='color:red'>Ciberterroristas</u>** | **<u style='color:red'>Phreakers</u>** | **<u style='color:red'>Script kiddies</u>** | **<u style='color:red'>Crackers</u>** | Desarrollo de virus	 | Atacante interno |
| :------------: | :----------------: | :---------: | :--------------: | :--------: | :------------------: | :----------------: |
| Reto |  | X |  |  | X	| X |
| Ego |  | X | X |  | X	|  |
| Espionaje |  |  |  | X | X | X |
| Ideología | X |  |  |  |  |  |
| Dinero |  | X |  | X | X | X |
| Venganza | X |  | X |  | X | X |
|  |  |  |  |  |  |  |

En la primera fase (reconocimiento), se busca reconocer y recolectar información. De esta manera, el atacante puede saber cómo puede actuar y los riesgos posibles, para así poder avanzar. En la segunda fase (ataque) se compromete el sistema, avanzando hasta el nivel más alto, teniendo el control del sistema atacado. Esta etapa usualmente se maneja de manera discreta, lo que dificulta la identificación del intruso. Usualmente, la vanidad del intruso y la falta de discreción ayudan al investigador a resolver el caso con mayor facilidad. Finalmente, (en la fase de eliminación) se altera, elimina o desaparece toda la evidencia que pueda comprometer al intruso en algún caso judicial. Del cuidado con el que el atacante proceda en esta fase depende el proceso del informático forense y del caso.

**Administradores y la infraestructura de la seguridad informática.**

El administrador del sistema es el experto encargado de la configuración de este, de la infraestructura informática y de la seguridad del sistema. Estos administradores son los primeros en estar en contacto con la inseguridad de la información, ya sea por un atacante o por una falla interna de los equipos. Al ser los arquitectos de la infraestructura y de la seguridad de la información del sistema, son quienes primero deberían reaccionar ante un ataque. Además, ellos deben proporcionar su conocimiento de la infraestructura del sistema para apoyar el caso y poder resolverlo con mayor facilidad.

Las infraestructuras de seguridad informática (realizadas por el administrador) han avanzado a medida que avanzan las tecnologías. Inicialmente, se utilizaba una infraestructura centralizada en la cual la información se encontraba en un equipo. Por lo tanto, en este caso la seguridad informática se concentraba en el control del acceso a los equipos con la información, al control del lugar en donde se encontraban y en el entrenamiento de quienes estaban encargados de manejar los equipos. Pero con la tecnología fueron cambiando las infraestructuras y las inseguridades cambiaron. Así es como se crearon los **<u style='color:red'>proxies</u>**, **<u style='color:red'>firewall</u>**, el sistema de detección de intrusos (**<u style='color:red'>IDS</u>**) , el sistema de prevención de intrusos (**<u style='color:red'>IPS</u>**) entre muchas otras herramientas para proveer una mejor seguridad a los sistemas, ya que ahora el acceso no ocurría solo a través de la máquina, sino a través de otras y de la Web.

Por otro lado, es importante hablar de la auditabilidad y trazabilidad, que son propiedades del sistema, relacionados con la infraestructura que son útiles como evidencia para el investigador. La auditabilidad es la capacidad del sistema para registrar los eventos de una acción en particular con el fin de mantener la historia de estos y de realizar un control con mayor facilidad. En cambio, la trazabilidad es la propiedad que tiene un sistema para rastrear o reconstruir relaciones entre diferentes objetos monitorizados.

Es importante resaltar que el administrador debe conocer lo suficiente sobre la infraestructura del sistema para poder colaborar con el caso, ya que su análisis puede facilitar el proceso del investigador forense. Adicionalmente, contar con los rastros y registro de eventos (Auditoría informática) en los sistemas es crucial para el administrador y su infraestructura, no solo porque genera confianza en sus clientes, sino también porque es una buena práctica en términos de seguridad para toda la empresa.

**Investigador.**

Es un nuevo profesional que actúa como experto, criminalista digital, o informático. Comprende y conoce las nuevas tecnologías de la información. Además, el investigador analiza la inseguridad informática emergente en los sistemas. El perfil del investigador es nuevo y necesario en el contexto abierto informático en el que vivimos. Por lo tanto, es necesario formar personas que puedan trabajar como investigadores en la disciplina emergente de la criminalística digital y el cómputo forense. Estas prácticas emergentes buscan articular las prácticas generales de la criminalística con las evidencias digitales disponibles en una escena del crimen. El trabajo del informático es indagar en las evidencias, analizarlas y evaluarlas para poder decidir cómo estas evidencias pueden ayudar a resolver el caso. Por lo tanto, es ideal que un investigador tenga conocimientos (al menos) sobre las siguientes áreas: justicia criminal, auditoría, administración y operación de tecnologías de Información.

En una investigación informática forense, hay ocho roles principales en un caso: el líder del caso, el propietario del sistema, el asesor legal, el auditor/ingeniero especialista en seguridad de la información, el administrador del sistema, el especialista en informática forense, el analista en informática forense y el fiscal. Usualmente, entre todos estos roles, los informáticos forenses pueden tomar los siguientes cuatro roles:

1. Líder del caso.

Es aquel que planea y organiza todo el proceso de investigación digital. Debe identificar el lugar en donde se realizará la investigación, quienes serán los participantes y el tiempo necesario para esta.

2. Auditor/ingeniero especialista en seguridad de la información.

Conoce el escenario en donde se desarrolla la investigación. Tiene el conocimiento del modelo de seguridad, los usuarios y las acciones que pueden realizar en el respectivo sistema. A partir de sus conocimientos debe entregar información crítica a la investigación.

3. Especialista en informática forense:

Es un criminalista digital que debe identificar los diferentes elementos probatorios informáticos vinculados al caso, determinando la relación entre los elementos y los hechos para descubrir el autor del delito.

4. Analista en informática forense:

Examina en detalle los datos, los elementos informáticos recogidos en la escena del crimen con el fin de extraer toda la información posible y relevante para resolver el caso.

**[Volver al Índice del capítulo 1. Plan de trabajo.](#índice-del-capítulo-1-plan-de-trabajo)**

---

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

### **1.7.6. Retos y riesgos en el análisis forense.**

Al estar en un escenario que evoluciona constantemente, cada vez surgen más retos y riesgos en el área de la informática forense. Entre ellos la formación de informáticos forenses, la confiabilidad de las herramientas, la facilidad de la destrucción de las evidencias, las amenazas estratégicas y tácticas que plantea el ciberterrorismo; y las tecnologías emergentes como la nube, las tecnologías móviles, y las redes sociales. Algunos de estos temas se abordarán a continuación:

**Formación de informáticos forenses.**

Los criminales informáticos son una nueva generación de delincuentes, en este contexto, es necesario desarrollar un nuevo tipo de investigadores: los informáticos forenses. En este momento es un desafío encontrar personas que tengan este perfil, ya que no existen suficientes programas que realicen este tipo de formación. Adicionalmente, en este momento, la mayoría de las personas ignoran la importancia de los informáticos forenses porque no son conscientes de la dimensión del cibercrimen. Usualmente se cree que no es algo tan grave y se le da mayor importancia a otro tipo de crímenes.

Por lo tanto, se deben plantear programas e iniciativas para poder realizar esta formación. Según investigaciones e iniciativas ya realizadas, hay cuatro componentes principales que deben estar presentes en un programa de computación forense o forensia digital: contenido multidisciplinario, ejercicios prácticos, profesores de calidad y ejemplos del mundo real (investigación de Taylor Endicott-Popovsky y Phillips, 2007).

- **Contenido multidisciplinario.**
    - Técnico en informática, conocimiento de criminalística, seguridad y delitos informáticos, entre otros.
- **Ejercicios prácticos en el laboratorio.**
    - Con herramientas tecnológicas forenses, en diferentes niveles de dificultad y variedad de componentes a analizar.
- **Profesores calificados.**
    - Con alto conocimiento en el tema.
- **Ejemplos del mundo real.**
    - Con el fin de dar mayor profundidad al aprendizaje.

**Confiabilidad de las herramientas.**

Las herramientas existentes disponibles para el cómputo forense presentan otro reto. Las herramientas licenciadas exigen a los investigadores inversiones altas (tanto en hardware, como en software), al adquirirlas y para mantenerlas. Adicionalmente, como las herramientas están avanzando constantemente requieren técnicos y usuarios que estén constantemente aprendiendo las actualizaciones, las modificaciones y los posibles errores. Por otro lado, las herramientas de código abierto son cuestionadas en muchos tribunales por su confiabilidad. Por lo tanto, no se recomiendan a la hora de usarse en una audiencia.

Es por esto que el **<u style='color:red'>NIST</u>** (National Institute of Standards and Technology de Estados Unidos) ha planteado importantes investigaciones para probar y poner reglas para las herramientas del cómputo forense, en su proyecto **<u style='color:red'>NIST</u>** Computer Forensic Tool Testing Program. Las pruebas realizadas serán útiles para cumplir las exigencias del test de Daubert standard, prueba que establece la confiabilidad de las herramientas en computación forense.

**[Volver al Índice del capítulo 1. Plan de trabajo.](#índice-del-capítulo-1-plan-de-trabajo)**

---

### **1.7.7. Herramientas de Análisis Forense.**

La siguiente tabla compara cuatro herramientas reconocidas internacionalmente al ser muy completas. Luego, se encuentra una lista más completa de herramientas útiles para la labor del investigador.

----------------------------------------------------------
| **Herramienta** | **Licencia** | **Imagen** | **Control de Integridad**  | **Administración del caso**  |
| :-----------: |  :-------: | :------: | :----------------------: | :------------------------: |
| Encase |  SI | SI | SI | SI |
| Forensic Toolkit | SI | SI | SI | SI |
| Winhex | SI | SI | SI | SI |
| Sleuth Kit | NO | SI | SI | SI |
|  |   |  |  |  |

- Air (Forensics Imaging GUI).
- Autopsy (Forensics Browser for Sleuth Kit)Cryptcat (Command Line)Deep Freeze.
- Dcfldd (DD Imaging Tool command line tool and also works with AIR).
- Dumpzilla (Forensics Browser: Firefox, Iceweasel and Seamonkey).
- Encase: \url{https://www.guidancesoftware.com/encase-forensic?cmpid=nav_r}.
- Exif Viewer (Visor de metadatos en imágenes).
- Faces.
- Foremost (Data Carver command line tool).
- Forensik Toolkit: \url{https://accessdata.com/products-services/forensic-toolkit-ftk}.
- Helix.
- Hetman software (Recuperador de datos borrados por los criminales).
- Hiren´s boot.
- Md5deep (MD5 Hashing Program).
- Metashield Analyser Online (Analizador de metadatos online).
- Mini XP.
- NTFS-Tools.
- Netcat (Command Line).
- Net resident.
- NetFlow.
- Py-Flag (Forensics Browser).
- Qtparted (GUI Partitioning Tool).
- R-Studio Emergency (Bootable Recovery media Maker).
- R-Studio Network Edtion.
- R-Studio RS Agent.
- Regviewer (Windows Registry).
- Sleuth Kit (Forensics Kit. Command Line): \url{https://www.sleuthkit.org/}.
- Snort.
- Viewer.
- Volatility (Reconstrucción y análisis de memoria RAM).
- X-Ways Forensics.
- X-Ways WinHex \url{https://www.x-ways.net/winhex/}.
- X-Ways WinTrace.

**Herramientas para el análisis de discos duros:**

- AccessData Forensic ToolKit (FTK).
- Guidance Software EnCase.
- Kit Electrónico de Transferencia de datos.

**Herramientas para el análisis de correos electrónicos:**

- Paraben.
- AccessData Forensic ToolKit (FTK).

**Herramientas para el análisis de dispositivos móviles:**

- Cellebrite UFED Touch 2, Physical Analyzer.
- AccessData Mobile Phone Examiner Plus (MPE+).

**Herramientas para el análisis de redes:**

- E-Detective - Decision Computer Group.
- SilentRunner - AccessData.
- NetworkMiner.
- Nerviness Investigator.

**Herramientas para filtrar y monitorear el tráfico de una red tanto interna como a internet:**

- Tcpdump.
- USBDeview.
- SilentRunner - AccessData.
- WireShark.

#### [1.3.5. Referencia 010.](#86010-cómputo-forense-de-wikipedia)

**[Volver al Índice del capítulo 1. Plan de trabajo.](#índice-del-capítulo-1-plan-de-trabajo) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [Volver al Índice General.](#índice-general)**

---

<br><br><br><br><br><br><br><br><br><br><br><br><br><br>

# 2. Extremos del análisis y previsión de pruebas técnicas.

## Índice del capítulo 2. Extremos del análisis y previsión de pruebas técnicas.

  - [2.0. Introducción al capítulo 2. Extremos del análisis y previsión de pruebas técnicas.](#índice-del-capítulo-2-extremos-del-análisis-y-previsión-de-pruebas-técnicas)
  - [2.1. Propuesta de extremos.](#21-propuesta-de-extremos)
  - [2.2. Previsión de pruebas técnicas.](#22-previsión-de-pruebas-técnicas)

**[Volver al Índice General.](#índice-general)**

---

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

## 2.0. Introducción al capítulo 2. Extremos del análisis y previsión de pruebas técnicas.

En la era digital actual, la capacidad de llevar a cabo análisis forenses en ordenadores se ha convertido en una competencia crítica dentro del ámbito de la investigación criminal. El análisis forense informático permite a los investigadores descubrir, preservar y analizar datos en dispositivos electrónicos que pueden ser críticos para resolver delitos. Este capítulo se dedica al estudio meticuloso de los métodos y prácticas estándar en la computación forense, con un enfoque específico en la adquisición y análisis de datos de la memoria RAM y discos duros. Se expondrá la metodología utilizada para garantizar la **<u style='color:red'>integridad</u>** de la evidencia y se ilustrarán los desafíos asociados a la recolección y el análisis de datos digitales.

Con el avance de la tecnología, los investigadores forenses enfrentan la dualidad de oportunidades y desafíos. Por un lado, las herramientas modernas ofrecen capacidades sin precedentes para recuperar y analizar datos; por otro lado, la creciente sofisticación del software y hardware supone nuevos niveles de complejidad y la necesidad de constante actualización en conocimientos y técnicas. Este capítulo también contempla la noción de deuda técnica asociada a la utilización de herramientas y sistemas operativos en la investigación forense, reconociendo la importancia de mantener un enfoque crítico hacia las herramientas utilizadas.

La documentación y control de versiones son aspectos cruciales en cualquier proyecto de investigación y desarrollo, más aún en el ámbito forense digital, donde la transparencia y reproducibilidad son fundamentales. Se detallará el uso del repositorio de **<u style='color:red'>Github</u>** (https://github.com/jrodg85/TFM-ANALISIS-FORENSE) para la documentación del TFM y el control de versiones aplicado al proceso de análisis forense. Se discutirá la relevancia de la colaboración y el seguimiento preciso de cambios en el código y documentos relacionados con el proyecto.

Finalmente, no se puede ignorar el papel fundamental que juega el acceso a recursos online en la actualización constante y el acceso a información relevante y actualizada en el campo de la forense digital. La Internet es una fuente inagotable de conocimiento, pero también presenta riesgos que deben ser gestionados con prudencia. En resumen, este capítulo traza el panorama del análisis forense en ordenadores, describiendo las herramientas y metodologías utilizadas, así como las mejores prácticas en la documentación y gestión de la información digital en investigaciones forenses.

Esta introducción proporciona una vista general y establece las expectativas para el contenido que seguirá, preparando al lector para los detalles técnicos y metodológicos que se presentarán en el capítulo.

**[Volver al Índice del capítulo 2. Extremos del análisis...](#índice-del-capítulo-2-extremos-del-análisis-y-previsión-de-pruebas-técnicas) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [Volver al Índice General.](#índice-general)**

---

<br><br><br><br><br><br><br><br><br>

## 2.1. Propuesta de extremos.

La presente investigación tiene como propósito fundamental el establecimiento de un marco metodológico para el análisis forense de ordenadores, específicamente orientado hacia la identificación, recolección y análisis de evidencias digitales que puedan ser presentadas en un entorno judicial. A continuación, se delinean los extremos de esta propuesta:

**Objeto de Estudio:**

- La investigación se centrará exclusivamente en el análisis forense del material facilitado para el desarrollo de la asignatura por parte del profesorado de la asignatura.
- Se realizará una breve indicación sobre la aplicación utilizada con cada uno de los objetivos del presente TFM.

**Alcance metodológico:**

- La validación de la **<u style='color:red'>integridad</u>** de la evidencia se hará mediante el uso de funciones **<u style='color:red'>hash</u>** estándar.
- Se examinarán las metodologías para el análisis de la memoria volátil y no volátil.

**Limitaciones:**

- La validación de la **<u style='color:red'>integridad</u>** de la evidencia se hará mediante el uso de funciones **<u style='color:red'>hash</u>** estándar.
- Se examinarán las metodologías para el análisis de la memoria volátil y no volátil.

**Exclusiones:**

- No se utilizará material de análisis que no sea el proporcionado por la asignatura.

**[Volver al Índice del capítulo 2. Extremos del análisis...](#índice-del-capítulo-2-extremos-del-análisis-y-previsión-de-pruebas-técnicas) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [Volver al Índice General.](#índice-general)**

---

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

## 2.2. Previsión de pruebas técnicas.

**Pruebas técnicas:**

- El propósito de estas pruebas técnicas es lo indicado en el apartado de problema a resolver del presente Trabajo de fin de master
  - Solventar las necesidades del gerente de la empresa mediante el análisis forense del disco duro y la captura de memoria de un ordenador personal, en un caso real con un sistema virtualizado.
  - Posible vinculación con una presunta conducta delictiva real.
- Importancia de las pruebas para validar la hipótesis y objetivos de investigación.
  - La posible imputación de los hechos ocurridos y tomar posibles medidas legales contra el autor univoco de la acción detectada.

**Marco metodológico de las pruebas:**

- Las pruebas que se realizarán serán una investigación y un estudio temporal de los hechos ocurridos dentro del pc.
- Se emplearán herramientas de análisis forense en sus distintos sistemas operativos (Linux/Windows) para su detección.
- se tratará de arrancar el sistema virtualizado para posible **<u style='color:red'>carving</u>** de la información del disco duro por posible eliminación de pruebas por parte del posible infractor.
- La planificación de las pruebas ha quedado detallado en la sección "planificación temporal de las tareas".

**Criterios de éxito de las pruebas:**

- Análisis de los incidentes ocurridos con una justificación probatoria del mismo.
- Realización de un análisis de seguridad de las vulnerabilidades detectadas y una via de mitigación de los mismos.

**Cronograma de pruebas:**

- El cronograma de las pruebas ha quedado detallado en la sección "planificación temporal de las tareas".
- Hitos importante, fechas de entrega de las PEC.

**[Volver al Índice del capítulo 2. Extremos del análisis...](#índice-del-capítulo-2-extremos-del-análisis-y-previsión-de-pruebas-técnicas) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [Volver al Índice General.](#índice-general)**

---

<br><br><br><br><br><br><br><br><br><br><br>

# 3. Análisis de la memoria RAM.

## Índice del capítulo 3. Análisis de la memoria RAM.


[Volver al Índice General.](#índice-general)

---

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

## 3.0. Introducción al capítulo 3. Análisis de la memoria RAM.

El análisis forense de la memoria RAM es un componente crítico en la investigación digital, pues permite a los analistas extraer información valiosa que no persiste una vez que el dispositivo se apaga. Esta volatilidad hace que la memoria RAM sea una fuente de evidencia esencial, especialmente en casos donde los procesos activos y la información en tránsito son relevantes para el caso. El presente capítulo detalla un enfoque metodológico estructurado para examinar de manera exhaustiva el contenido de la memoria RAM capturada de un sistema informático, con el objetivo de identificar y analizar aspectos críticos que contribuyan a la investigación.

Las acciones específicas que se abordarán son las siguientes:

1. **Comprobación del MD5:**

- Iniciaremos con la verificación de la **<u style='color:red'>integridad</u>** del volcado de la memoria RAM mediante el cálculo de su suma de verificación MD5. Este paso es fundamental para asegurar que los datos analizados no han sido alterados desde el momento de su adquisición, garantizando así la **<u style='color:red'>cadena de custodia</u>** digital.

2. **Identificación del Sistema Operativo:**

- Aunque ya intuyamos, por el apartado anterior datos básicos del Sistema operativo, es vital determinar la versión y configuración del sistema operativo en uso, ya que esto influirá en la interpretación de los datos y en la selección de las herramientas de análisis adecuadas.

3. **Búsqueda de Datos de Interés:**

- Seguiremos con la inspección minuciosa del contenido de la memoria para identificar información potencialmente relevante para el caso. Esto incluye, pero no se limita a, datos residuales de aplicaciones, fragmentos de comunicaciones y elementos que puedan ser reconstruidos para obtener evidencia. Servirá para tener una previsión de por donde dirigir el estudio de todo el análisis forense.

4. **Búsqueda de Procesos en Funcionamiento de Interés:**

- Un punto focal de nuestra investigación será el examen de los procesos activos en el momento de la captura de la memoria. Esta inspección nos permitirá comprender mejor el estado del sistema antes del apagado o la hibernación.

5. **Análisis y Extracción de Procesos Sospechosos:**

- Finalmente, nos concentraremos en reconstruir y examinar las conexiones de red activas y pasivas. El objetivo es identificar patrones de tráfico inusuales o conexiones que puedan indicar comunicación con servidores de comando y control, exfiltración de datos o cualquier otra actividad que se considere sospechosa.


El resultado de este análisis exhaustivo proporcionará una comprensión detallada de lo que estaba ocurriendo en el sistema en el momento de la captura de la memoria. Esta información es invaluable para formar una imagen completa de los eventos bajo investigación y para establecer hechos concretos que puedan ser presentados como evidencia en un entorno judicial.

**[Volver al Índice del capítulo 3. Análisis de la memoria RAM.](#índice-del-capítulo-3-análisis-de-la-memoria-ram) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [Volver al Índice General.](#índice-general)**

---

## 3.1. Acciones previas al análisis de la memoria RAM.

En el presente TFM, se nos ha proporcionado a los alumnos un archivo de captura de memoria RAM .mem. Por otro lado, se nos ha proporcionado los resúmenes o **<u style='color:red'>hash</u>** en MD5 y en SHA1 de los archivos tal y como se muestra en la siguiente imagen.

#### [3.1 Imagen 001](#83003001001-imagen-hash-archivos)

Como Podemos ver, los **<u style='color:red'>hash</u>** resúmenes del archivo de la ram, tememos los siguientes hashes en MD5 y en SHA1:

- **MD5:** 75a99b57032aa34ba19042ed85db273f
- **SHA1:** cc1fad2af321b8c2ddf0103986e3b344eb8f2cc8

El **<u style='color:red'>hash</u>** tal y como se indica en los apuntes de la asignatura, en el módulo de Fases y metodología del análisis forense, durante la adquisición de evidencias digitales dice  lo siguiente:

Una vez generada la copia o clon del soporte original, el programa o el dispositivo hardware empleado en este proceso realiza el cálculo del **<u style='color:red'>CRC</u>** o del valor **<u style='color:red'>hash</u>** del soporte original y del destino, con la finalidad de garantizar que los dos son idénticos y que la copia se ha producido sin ningún error. Este cálculo puede realizarse sobre todo el conjunto de información contenida en el soporte original, o bien emplear solamente un conjunto de ficheros del total.

A su vez, en el glosario de términos la definición de **<u style='color:red'>hash</u>** es la siguiente:

Es una función matemática unidireccional que resume un mensaje de tamaño variable (por ejemplo, un archivo), en una representación de tamaño fijo. Es poco probable que dos ficheros distintos tengan la misma representación **<u style='color:red'>hash</u>**, lo cual significa que este valor puede utilizarse a efectos de comprobación de la **<u style='color:red'>integridad</u>** de un archivo (o de un sistema entero). Las funciones **<u style='color:red'>hash</u>** más conocidas son MD5 y SHA-1.

Una vez descargado el archivo de captura de la memoria RAM, procedemos a usar PowerShell para determinar el **<u style='color:red'>hash</u>** del archivo. Para ello usamos el comando  "Get-FileHash [Argumento] -Algorithm MD5". En nuestro caso hemos usado los siguientes comandos:

#### [3.1 Comando 001.](#85003001001-comando-hash-md5) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [3.1 Comando 002.](#85003001002-comando-hash-sha1)

Se puede observar en la siguiente imagen la respuesta de PowerShell de los hashes de MD5 y SHA1.

#### [3.1. Imagen 002](#83003001002-imagen-hash-PowerShell)

Como conclusión podemos verificar que la **<u style='color:red'>integridad</u>** de la copia facilitada para realizar el TFM no ha sido vulnerada.

**[Volver al Índice del capítulo 3. Análisis de la memoria RAM.](#índice-del-capítulo-3-análisis-de-la-memoria-ram) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [Volver al Índice General.](#índice-general)**

---

<br><br><br><br>

## 3.2. Sistema Operativo de la memoria RAM analizada.

Procedemos a preparar una máquina virtual con Ubuntu 22.04, el cual le instalamos el volatility según en el siguiente enlace. Haga click en la imagen para acceder al enlace:

#### [3.2. Video 001](#84003002001-video-de-instalación-de-volatility-en-ubuntu)

A continuación procedemos a buscar el perfil con volatility con el comando `imageinfo`.

#### [3.2 Imagen 001](#83003002001-imagen-de-imageinfo)

Como se puede observar en la imagen anterior, no hemos llegado a encontrar un perfil concreto con `imageinfo`, eso se debe a que el perfil creado no es el que se encuentra dentro de las conocidas en la base de datos de volatility. Por ello procedemos a buscar dentro de la memoria RAM un string que tenga la cadena de texto "linux version". para ello ejecutamos el comando `strings Server_{RAM}.mem \mid grep -Ei linux version \mid uniq`.

#### [3.2 Imagen 002](#83003002002-imagen-de-búsqueda-de-string-linux-version)

Podemos observar en la imagen anterior que el sistema operativo que utiliza en nuestro caso es un sistema operativo Linux para Amazon Web Service, concretamente el sistema operativo es el **4.15.0-1021.21-aws 4.15.18**. Esta version de Linux, es muy usada para las instancias de Amazon Web Services.

Como no tenemos el perfil cargado dentro de volatility, nos va a tocar hacer la tarea de cargar un perfil de este Sistema operativo para poder seguir ejecutando la aplicación volatility.

Buscando en google **linux version 4.15.0-1021.21-aws volatility**, nos encontramos solo un enlace en internet, el cual es https://lists.ubuntu.com/archives/bionic-changes/2018-August/016183.html, con ello nos encontrábamos con algo que ya se intuía previamente, y es que la versión del server de AWS, es basada en un ubuntu 18.04, ya que la fecha que indica 4.15.18 es una fecha en tipo "d.mm.aa".

**[Volver al Índice del capítulo 3. Análisis de la memoria RAM.](#índice-del-capítulo-3-análisis-de-la-memoria-ram) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [Volver al Índice General.](#índice-general)**

---

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

## 3.3. Datos de interés de la captura de la memoria RAM.

En el anexo Creación perfil ubuntu AWS, hemos realizado una guía para crear el perfil de Linux AWS que detectado durante el análisis del sistema operativo.

Una vez creado el perfil de linuxUbuntu_4.15.0-1021-aws procederemos a hacer un pslist para listar todas las aplicaciones que estaban ejecutándose en el momento de la captura.

Para comprobar que el perfil funciona, vamos a comenzar a comprobar cual es el **<u style='color:red'>CPU</u>** que usa el sistema.

Para ello ejecutaremos `sudo python2.7 vol.py --profile=LinuxlinuxUbuntu_4_15_0-1021-awsx64 -f '/home/jrodg85/Server_RAM.mem' linux_cpuinfo`.

Al comprobar que el perfil funciona, obtenemos que solo hay un procesador de marca GenuineIntel modelo Intel(R) Xeon(R) **<u style='color:red'>CPU</u>** E5-2676 v3 que tiene una frecuencia de 2.4Ghz.

Otro comando de interés es obtener el history del la terminal, con ello podemos observar los pasos realizados y los que ha ejecutado. Para ello ejecutaremos el comando `sudo python2.7 vol.py --profile=LinuxlinuxUbuntu_4_15_0-1021-awsx64 -f '/home/jrodg85/Server_RAM.mem' linux_bash`. Los comandos usados son los siguientes:

#### [3.3 Comando 001.](#85003003001-comando-linux-bash)


Analizando los comandos realizados se pueden destacar los siguientes:

- **exit**: Sale de la sesión actual, ya sea una sesión de terminal o una conexión SSH.
- **sudo apt update**: Actualiza la lista de paquetes disponibles y sus versiones. Es un paso previo común antes de instalar o actualizar paquetes.
- **sudo systemctl restart postfix**: Reinicia el servicio Postfix, un agente de transferencia de correo (MTA).
- **ls -l**: Lista los archivos en el directorio actual en un formato detallado.
- **mysql -uroot -p**: Inicia sesión en el servidor MySQL como usuario 'root', pidiendo la contraseña.
- **cd apache2/ y movimientos similares**: Cambia el directorio actual a uno especificado.
- **sudo vi /etc/mysql/debian.cnf**: Edita el archivo de configuración de MySQL usando el editor vi.
- **ps -ef| grep mysql**: Muestra los procesos actuales relacionados con MySQL.
- **sudo kill -9 4539**: Mata de manera forzosa el proceso con el ID 4539.
- **sudo mysqld_safe --skip-grant-tables**: Inicia MySQL en un modo especial que omite ciertas comprobaciones de seguridad.
- **sudo apt install python-certbot-apache**: Instala Certbot para Apache, una herramienta para obtener certificados SSL/TLS de Let's Encrypt.
- **sudo service apache2 restart**: Reinicia el servidor web Apache.
- **sudo mysql_secure_installation**: Ejecuta un script para mejorar la seguridad de MySQL.
- **sudo apt-get install mysql-server**: Instala el servidor MySQL.
- **sudo chmod 777 /var/run/mysqld**: Cambia los permisos del directorio /var/run/mysqld para que todos los usuarios puedan leer, escribir y ejecutar archivos en él.
- **sudo chown -R www-data:www-data html**: Cambia la propiedad del directorio html al usuario y grupo www-data, comúnmente usado para servidores web.
- **find . -name functions.php -exec grep -H add_filer {} \;**: Busca en archivos functions.php y ejecuta grep en ellos.
- **tail access.log y variantes**: Muestra las últimas líneas de los archivos de registro especificados.
- **sudo vi /etc/apache2/sites-enabled/000-default.conf**: Edita la configuración predeterminada del sitio de Apache.
- **sudo apt upgrade**: Actualiza todos los paquetes instalados a sus últimas versiones.
- **sudo systemctl reload apache2**: Recarga la configuración de Apache sin reiniciar el servicio.
- **sudo service mysql stop**: Detiene el servicio MySQL.
- **sudo dpkg-reconfigure mysql-server-5.7**: Reconfigura la versión especificada del servidor MySQL.
- **sudo apachectl configtest**: Verifica la sintaxis de los archivos de configuración de Apache.
- **sudo add-apt-repository ppa:certbot/certbot**: Añade el repositorio PPA para Certbot.
- **sudo apt install php-mysql**: Instala el módulo PHP para interactuar con MySQL.
- **sudo insmod lime-4.15.0-42-generic.ko "path=captura.mem format=lime"**: Carga un módulo del kernel para la captura de memoria.

Relativo a la seguridad del servidor, siguiente listado de documentos son notables para la seguridad, ya que pueden tener un impacto significativo en la seguridad del servidor. Aquí hay algunos ejemplos notables:

**1. sudo mysqld_safe --skip-grant-tables.**

  - Este comando inicia el servidor MySQL sin respetar el sistema de permisos. Cualquiera podría acceder a todas las bases de datos sin necesidad de una contraseña. Es extremadamente peligroso en un entorno de producción y debería usarse solo en situaciones de recuperación de emergencia.

**2. sudo chmod 777 /var/run/mysqld.**

  - Este comando establece los permisos de lectura, escritura y ejecución para todos los usuarios en el directorio /var/run/mysqld. Otorgar estos permisos tan amplios puede ser un riesgo de seguridad significativo, ya que permite a cualquier usuario en el sistema modificar o eliminar archivos críticos para el funcionamiento de MySQL.

**3. sudo kill -9 (con varios números de proceso).**

- Si bien no es inherentemente inseguro, el uso imprudente de kill -9 puede terminar procesos cruciales y causar inestabilidad o pérdida de datos si se aplica a procesos críticos del sistema o de la base de datos.

**4. sudo rm -r /run/mysqld.**

- Eliminar directorios críticos del sistema puede afectar la estabilidad y funcionamiento de los servicios asociados, en este caso, MySQL.

**5. sudo service mysql stop y sudo service apache2 stop.**

- Detener servicios como MySQL y Apache puede afectar la disponibilidad de aplicaciones dependientes. Si se hace sin precaución, podría provocar tiempos de inactividad no planificados.

**6. vi /etc/mysql/debian.cnf y sudo vi /etc/apache2/sites-enabled/000-default.conf.**

- Editar archivos de configuración es una tarea común, pero si se hacen cambios incorrectos o inseguros, pueden surgir problemas de seguridad y funcionamiento.

**7.sudo insmod lime-4.15.0-42-generic.ko "path=captura.mem format=lime".**

- Cargar módulos del kernel personalizados o desconocidos puede ser una accion de riesgo si no se comprenden completamente sus funciones y orígenes.

**8. sudo apt install php-mysql.**

- La instalación de software debe hacerse con cuidado, asegurándose de que las fuentes sean confiables y que no se introduzcan vulnerabilidades.

**9. Errores tipográficos y comandos incompletos.**

- Podrían resultar en acciones no intencionadas que afectan la seguridad o estabilidad del sistema.

Es fundamental que cualquier administrador de sistemas ejecute estos comandos con conocimiento completo de sus implicaciones y en el contexto adecuado. Además, las buenas prácticas de seguridad, como la mínima exposición de servicios, el uso restringido de permisos y la monitorización constante, son esenciales para mantener la **<u style='color:red'>integridad</u>** y seguridad del sistema.

[Volver al Índice del capítulo 3. Análisis de la memoria RAM.](#índice-del-capítulo-3-análisis-de-la-memoria-ram)

[Volver al Índice General.](#índice-general)

---



## 3.4. Búsqueda de procesos en funcionamiento de interés para el análisis.








[Volver al Índice del capítulo 3. Análisis de la memoria RAM.](#índice-del-capítulo-3-análisis-de-la-memoria-ram)

[Volver al Índice General.](#índice-general)

---



## 3.5. Listado de conexiones de red y conexiones sospechosas.








[Volver al Índice del capítulo 3. Análisis de la memoria RAM.](#índice-del-capítulo-3-análisis-de-la-memoria-ram)

[Volver al Índice General.](#índice-general)

---



# 4. Análisis del disco duro.


## Índice del capítulo 4. Análisis del disco duro.












[Volver al Índice General.](#índice-general)

---



## 4.0. Introducción al capítulo 4. Análisis del disco duro.











[Volver al Índice del capítulo 4. Análisis del disco duro.](#índice-del-capítulo-4-análisis-del-disco-duro)

[Volver al Índice General.](#índice-general)

---



## 4.1. Acciones previas al análisis del disco duro.










[Volver al Índice del capítulo 4. Análisis del disco duro.](#índice-del-capítulo-4-análisis-del-disco-duro)

[Volver al Índice General.](#índice-general)

---



## 4.2. Datos de interés del disco duro.










[Volver al Índice del capítulo 4. Análisis del disco duro.](#índice-del-capítulo-4-análisis-del-disco-duro)

[Volver al Índice General.](#índice-general)

---



## 4.3. Usuarios del sistema.







[Volver al Índice del capítulo 4. Análisis del disco duro.](#índice-del-capítulo-4-análisis-del-disco-duro)

[Volver al Índice General.](#índice-general)

---



## 4.4. Análisis de evidencias del disco duro.






[Volver al Índice del capítulo 4. Análisis del disco duro.](#índice-del-capítulo-4-análisis-del-disco-duro)

[Volver al Índice General.](#índice-general)

---



# 5. Resumen ejecutivo.

## Índice del capítulo 5. Resumen ejecutivo.








[Volver al Índice General.](#índice-general)

---



## 5.0. Introducción al capítulo 5. Resumen ejecutivo.






[Volver al Índice del capítulo 5. Resumen ejecutivo.](#índice-del-capítulo-5-resumen-ejecutivo)

[Volver al Índice General.](#índice-general)

---



## 5.1. Resumen ejecutivo.











[Volver al Índice del capítulo 5. Resumen ejecutivo.](#índice-del-capítulo-5-resumen-ejecutivo)

[Volver al Índice General.](#índice-general)

---



# 6. Informe pericial.

## Índice del capítulo 6. Informe pericial.

[Volver al Índice General.](#índice-general)

---



## 6.0. Introducción al capítulo 6. Informe pericial.

[Volver al Índice del capítulo 6. Informe pericial.](#índice-del-capítulo-6-informe-pericial)

[Volver al Índice General.](#índice-general)

---



## 6.1. Informe pericial.

[Volver al Índice del capítulo 6. Informe pericial.](#índice-del-capítulo-6-informe-pericial)

[Volver al Índice General.](#índice-general)

---



# 7. Conclusiones.

## Índice del capítulo 7. Conclusiones.

[Volver al Índice General.](#índice-general)

---



## 7.0. Introducción al capítulo 7. Conclusiones.





[Volver al Índice del capítulo 7. Conclusiones.](#índice-del-capítulo-7-conclusiones)

[Volver al Índice General.](#índice-general)

---



## 7.1. Conclusiones.








[Volver al Índice del capítulo 7. Conclusiones.](#índice-del-capítulo-7-conclusiones)

[Volver al Índice General.](#índice-general)

---



# 8. Anexos.

## Índice del capítulo 8. Anexos.






[Volver al Índice General.](#índice-general)

---




## 8.0. Introducción al capítulo 8. Anexos.




[Volver al Índice del capítulo 8. Anexos.](#índice-del-capítulo-8-anexos)

[Volver al Índice General.](#índice-general)

---



## 8.1. Creación de perfil para volatility.

### 8.1.0. Introducción de creación de perfil de volatility.

Crear un perfil de volatility es fundamental para poder extraer la información de los datos de la ram.

En el repositorio de github de volatility podemos observar perfiles relativos a windows, pero ninguno relativo al sistema operativo linux. Si ejecutamos el comando `sudo python2.7 vol.py --info` tenemos la siguiente respuesta relativo a perfiles:

~~~Shell
Profiles
--------
VistaSP0x64                         - A Profile for Windows Vista SP0 x64
VistaSP0x86                         - A Profile for Windows Vista SP0 x86
VistaSP1x64                         - A Profile for Windows Vista SP1 x64
VistaSP1x86                         - A Profile for Windows Vista SP1 x86
VistaSP2x64                         - A Profile for Windows Vista SP2 x64
VistaSP2x86                         - A Profile for Windows Vista SP2 x86
Win10x64                            - A Profile for Windows 10 x64
Win10x64_10240_17770                - A Profile for Windows 10 x64 (10.0.10240.17770 / 2018-02-10)
Win10x64_10586                      - A Profile for Windows 10 x64 (10.0.10586.306 / 2016-04-23)
Win10x64_14393                      - A Profile for Windows 10 x64 (10.0.14393.0 / 2016-07-16)
Win10x64_15063                      - A Profile for Windows 10 x64 (10.0.15063.0 / 2017-04-04)
Win10x64_16299                      - A Profile for Windows 10 x64 (10.0.16299.0 / 2017-09-22)
Win10x64_17134                      - A Profile for Windows 10 x64 (10.0.17134.1 / 2018-04-11)
Win10x64_17763                      - A Profile for Windows 10 x64 (10.0.17763.0 / 2018-10-12)
Win10x64_18362                      - A Profile for Windows 10 x64 (10.0.18362.0 / 2019-04-23)
Win10x64_19041                      - A Profile for Windows 10 x64 (10.0.19041.0 / 2020-04-17)
Win10x86                            - A Profile for Windows 10 x86
Win10x86_10240_17770                - A Profile for Windows 10 x86 (10.0.10240.17770 / 2018-02-10)
Win10x86_10586                      - A Profile for Windows 10 x86 (10.0.10586.420 / 2016-05-28)
Win10x86_14393                      - A Profile for Windows 10 x86 (10.0.14393.0 / 2016-07-16)
Win10x86_15063                      - A Profile for Windows 10 x86 (10.0.15063.0 / 2017-04-04)
Win10x86_16299                      - A Profile for Windows 10 x86 (10.0.16299.15 / 2017-09-29)
Win10x86_17134                      - A Profile for Windows 10 x86 (10.0.17134.1 / 2018-04-11)
Win10x86_17763                      - A Profile for Windows 10 x86 (10.0.17763.0 / 2018-10-12)
Win10x86_18362                      - A Profile for Windows 10 x86 (10.0.18362.0 / 2019-04-23)
Win10x86_19041                      - A Profile for Windows 10 x86 (10.0.19041.0 / 2020-04-17)
Win2003SP0x86                       - A Profile for Windows 2003 SP0 x86
Win2003SP1x64                       - A Profile for Windows 2003 SP1 x64
Win2003SP1x86                       - A Profile for Windows 2003 SP1 x86
Win2003SP2x64                       - A Profile for Windows 2003 SP2 x64
Win2003SP2x86                       - A Profile for Windows 2003 SP2 x86
Win2008R2SP0x64                     - A Profile for Windows 2008 R2 SP0 x64
Win2008R2SP1x64                     - A Profile for Windows 2008 R2 SP1 x64
Win2008R2SP1x64_23418               - A Profile for Windows 2008 R2 SP1 x64 (6.1.7601.23418 / 2016-04-09)
Win2008R2SP1x64_24000               - A Profile for Windows 2008 R2 SP1 x64 (6.1.7601.24000 / 2016-04-09)
Win2008SP1x64                       - A Profile for Windows 2008 SP1 x64
Win2008SP1x86                       - A Profile for Windows 2008 SP1 x86
Win2008SP2x64                       - A Profile for Windows 2008 SP2 x64
Win2008SP2x86                       - A Profile for Windows 2008 SP2 x86
Win2012R2x64                        - A Profile for Windows Server 2012 R2 x64
Win2012R2x64_18340                  - A Profile for Windows Server 2012 R2 x64 (6.3.9600.18340 / 2016-05-13)
Win2012x64                          - A Profile for Windows Server 2012 x64
Win2016x64_14393                    - A Profile for Windows Server 2016 x64 (10.0.14393.0 / 2016-07-16)
Win7SP0x64                          - A Profile for Windows 7 SP0 x64
Win7SP0x86                          - A Profile for Windows 7 SP0 x86
Win7SP1x64                          - A Profile for Windows 7 SP1 x64
Win7SP1x64_23418                    - A Profile for Windows 7 SP1 x64 (6.1.7601.23418 / 2016-04-09)
Win7SP1x64_24000                    - A Profile for Windows 7 SP1 x64 (6.1.7601.24000 / 2018-01-09)
Win7SP1x86                          - A Profile for Windows 7 SP1 x86
Win7SP1x86_23418                    - A Profile for Windows 7 SP1 x86 (6.1.7601.23418 / 2016-04-09)
Win7SP1x86_24000                    - A Profile for Windows 7 SP1 x86 (6.1.7601.24000 / 2018-01-09)
Win81U1x64                          - A Profile for Windows 8.1 Update 1 x64
Win81U1x86                          - A Profile for Windows 8.1 Update 1 x86
Win8SP0x64                          - A Profile for Windows 8 x64
Win8SP0x86                          - A Profile for Windows 8 x86
Win8SP1x64                          - A Profile for Windows 8.1 x64
Win8SP1x64_18340                    - A Profile for Windows 8.1 x64 (6.3.9600.18340 / 2016-05-13)
Win8SP1x86                          - A Profile for Windows 8.1 x86
WinXPSP1x64                         - A Profile for Windows XP SP1 x64
WinXPSP2x64                         - A Profile for Windows XP SP2 x64
WinXPSP2x86                         - A Profile for Windows XP SP2 x86
WinXPSP3x86                         - A Profile for Windows XP SP3 x86
~~~

[Volver al Índice del capítulo 8. Anexos.](#índice-del-capítulo-8-anexos)

### 8.1.1. Creación de la máquina virtual.

Vamos crear una máquina virtual para generar una máquina virtual base con el mismo kernel que el servidor auditado.

![025-detalles-servidor-perfil-volatility](./images/025-detalles-servidor-perfil-volatility.png)

[Volver al Índice del capítulo 8. Anexos.](#índice-del-capítulo-8-anexos)

### 8.1.2. Búsqueda en cache del kernel relativo al perfil a crear.

Procedemos a arrancar la máquina virtual (en adelante VM), una vez realizado el login, procedemos a ejecutar el comando `sudo apt-cache search linux-image | grep 4.15.0-1021`.

Este comando realiza dos acciones, por un lado `sudo apt-cache search linux-image`, y por otro `grep 4.15.0-1021`. Gracias al  "pipe" o "|", pasaremos la respuesta del primera acción como entrada de la segunda acción.. Es una parte fundamental de la filosofía de Unix que permite a los usuarios combinar múltiples comandos sencillos para realizar tareas más complejas. En nuestro caso:

**sudo apt-cache search linux-image.**

  - Esta parte del comando busca en la caché de APT (Advanced Package Tool) todos los paquetes cuyos nombres o descripciones contienen la cadena "linux-image". Los paquetes "linux-image" generalmente se refieren a imágenes del kernel de Linux para diferentes versiones y configuraciones.

**| grep 4.15.0-1021.**

  - La salida del primer comando se canaliza (|) al comando grep, que filtra y muestra solo las líneas que contienen la cadena "4.15.0-1021". En este contexto, "4.15.0-1021" probablemente se refiere a una versión específica del kernel de Linux.

Al combinar estos dos comandos, `sudo apt-cache search linux-image | grep 4.15.0-1021` efectivamente busca y lista todas las versiones de las imágenes del kernel de Linux disponibles en los repositorios que coincidan con la versión específica "4.15.0-1021". Este comando es útil para identificar si una versión específica del kernel está disponible para la instalación o actualización en el sistema.

Se adjunta pantallazo de la respuesta por parte de la consola.

##### [Imagen 009](#83009)

[Volver al Índice del capítulo 8. Anexos.](#índice-del-capítulo-8-anexos)

### 8.1.3. Instalación del kernel relativo al perfil a crear.

Una vez encontrado la imagen del kernel que buscamos, procedemos a instalarla en el sistema, para ello ejecutamos el comando `sudo apt-get install linux-image-4.15.0-2021-aws`.

El comando `sudo apt-get install linux-image-4.15.0-2021-aws` en Ubuntu o sistemas basados en Debian, se utiliza para instalar una versión específica del kernel de Linux, diseñada para ambientes Amazon Web Services (AWS). Al usar `sudo`, el comando se ejecuta con privilegios de superusuario, necesarios para instalar software a nivel de sistema. `apt-get install` es parte del sistema de gestión de paquetes APT, y se usa aquí para instalar el paquete `linux-image-4.15.0-2021-aws`. Este paquete contiene una imagen del kernel de Linux, la cual está optimizada para correr en servidores AWS, indicando que este kernel podría tener configuraciones o parches específicos para un rendimiento mejorado o características adicionales en esa plataforma. **Al instalar un nuevo kernel, es importante reiniciar el sistema para que empiece a usar esta nueva versión.**

Se adjunta pantallazo de la instalación del kernel de AWS:

##### [Imagen 010](#83010)

Como hemos indicado anteriormente, es necesario reiniciar el sistema para que el kernel instalado se utilice en el Sistema operativo, procederemos a ejecutar el comando `sudo reboot now` para realizar esta acción.

##### [Imagen 011](#83011)

Una vez reiniciado el sistema, procedemos a ejecutar el comando `uname - r` para comprobar que el comando se ha ejecutado correctamente.

##### [Imagen 012](#83012)

[Volver al Índice del capítulo 8. Anexos.](#índice-del-capítulo-8-anexos)

### 8.1.4. Instalación de volatility.

Una vez comprobado, procederemos a la instalación de volatility en el servidor de ubuntu.

Primero de todo instalaremos los paquetes relativos a `dwarfdum`, `gcc`, `linux-headers` y `git`, ya que el servidor no los tiene instalado por defecto.

 Seguiremos los pasos ya indicados en el [Apartado 3.2](#32-sistema-operativo-de-la-memoria-ram-analizada):

[![Miniatura video Volatility](./images/024-miniatura-instalacion-volatility.png)](https://youtu.be/z_SWIIa3AnY)

> https://www.youtube.com/watch?v=z_SWIIa3AnY

Una vez instalado, procedemos a realizar los pasos para la creación del perfil de volatility.

[Volver al Índice del capítulo 8. Anexos.](#índice-del-capítulo-8-anexos)

### 8.1.5. Creación del perfil de volatility.

Una vez hemos realizado la instalación procedemos a crear el perfil de volatility.

Para ello entraremos en la carpeta `home/jrodg85/volatility/tools/linux`, una vez allí dentro ejecutaremos el comando `make`. En la siguiente imagen, se puede ver un pantallazo del comando, en caso de tener error del mismo, lo mas recomendable es hacer un `make clean` y después volver a ejecutar `make`. Lo mas importante es que se tiene que crear el archivo **`modules.dwarf`**

##### [Imagen 013](#83013)

Ahora procederemos a nombrar el perfil de volatility para ello vamos a generar un archivo zip, este archivo, como norma general, usaremos los valores de `lsb_release -si` y `uname -r`. De esta manera nombraremos de manera correcta el perfil de volatility para después no tengamos problemas al importarlo dentro de la máquina donde estamos realizando la investigación.

![017-lsb-release-y-uname-r.png](./images/017-lsb-release-y-uname-r.png)

Este archivo zip, debe de contener los dos archivos necesarios de perfil:

**modules.dwarf**

- Este archivo se genera a partir de los módulos del kernel de Linux y contiene información sobre las estructuras de datos del kernel. Es creado usando, en nuestro caso, la herramienta dwarfdump sobre módulos del kernel compilados con símbolos de depuración (debugging symbols). El archivo module.dwarf es crucial porque contiene los offsets y las definiciones de las estructuras de datos internas del kernel, lo que permite a Volatility entender cómo están organizados los datos en el volcado de memoria.

**/boot/System.map-4.15.0-1021-aws**

- Este archivo es un mapa de símbolos del kernel. Proporciona una lista de todas las funciones y variables en el kernel, junto con sus direcciones de memoria. Cada versión del kernel de Linux tiene su propio archivo System.map, y el archivo específico para una versión dada del kernel (en tu caso, 4.15.0-1021-aws) es necesario para analizar un volcado de memoria tomado de un sistema que ejecuta esa versión del kernel. Este archivo es esencial para que Volatility pueda mapear las direcciones de memoria en el volcado a nombres de funciones y variables específicas en el kernel.

Para la generación del perfil, procederemos a ejecutar el comando `sudo zip /home/jrodg85/volatility/volatility/plugins/overlays/linux$(lsb_release -si)_$(uname -r)_profiles.zip /home/jrodg85/volatility/tools/linux/module.dwarf /boot/System.map-4.15.0-1021-aws`

![018-perfil-generado.png](./images/018-perfil-generado.png)

Una vez creado el perfil, tenemos que sacar el perfil del servidor para después pegarlo dentro de la máquina una donde realizaremos el análisis. para ello procederemos a montar un usb dentro del servidor del ubuntu, posteriormente copiamos el archivo, `/home/jrodg85/volatility/volatility/plugins/overlays/linuxUbuntu_4.15.0-1021-aws_profile.zip`, y lo pegamos en el **<u style='color:red'>USB</u>**, posteriormente, procedemos a insertar en la VM de análisis en la carpeta en la carpeta `/home/jrodg85/volatility/volatility/plugins/overlays/linux` tal y como se muestra en la siguiente imagen.

![021-copiado-en-entorno-volatility.png](./images/021-copiado-en-entorno-volatility.png)

para comprobar que esta correctamente creado el perfil procedemos a ejecutar el comando `sudo python2.7 col.py --info`, donde se podrá observar que se ha creado correctamente el perfil.

![022-perfil-creado.png](./images/022-perfil-creado.png)

[Volver al Índice del capítulo 8. Anexos.](#índice-del-capítulo-8-anexos)

[Volver al Índice General.](#índice-general)

---

## 8.2. Glosario de términos y abreviaturas.

---

#### 8.2.001.000.001. CISO.

1. La persona responsable de velar por la ciberseguridad de una empresa, es el acrónimo de (Chief Information Security Officer). También podemos conocerlo como director de seguridad de la información. Esta persona es la que se encarga de proteger la información ante posibles ciberataques y fugas de datos. De esta manera, garantiza la seguridad dentro de las posibilidades tanto humanas, técnicas como económicas que tenga cada empresa.

[Volver al texto del término en la Sección 1.0.](#10-glosario-001-ciso)

---

#### 8.2..


#### **Análisis de archivo.**

- Examina cada archivo digital descubierto y crea una base de datos de información relacionada al archivo (metadatos, etc.), consistente entre otras cosas en la firma del archivo o **<u style='color:red'>hash</u>** (indica la **<u style='color:red'>integridad</u>** del archivo).

---

#### **Cadena de custodia.**

- La identidad de personas que manejan la evidencia en el tiempo del suceso y la última revisión del caso. Es la responsabilidad de la persona que maneja la evidencia asegurar que los artículos son registrados y contabilizados durante el tiempo en el cual están en su poder, y que son protegidos, así mismo llevando un registro de los nombres de las personas que manejaron la evidencia o artículos durante el lapso de tiempo y fechas de entrega y recepción.VCX

----

[Volver al Índice del capítulo 8. Anexos.](#índice-del-capítulo-8-anexos)

[Volver al Índice General.](#índice-general)

---

## 8.3. Imágenes.

---

#### 8.3.001.003.005.001. Diagrama de metodología del análisis forense.

![001-003-005-001](./images/001-003-005-001-FASES-METODOLOGIA-ANALISIS-FORENSE.png)

[Volver al texto de la imagen en la Sección 1.3.5.](#135-imagen-001)

---

#### 8.3.001.003.005.002. Fases 1 2 y 3 de la metodología del análisis forense.

![001-003-005-002](./images/001-003-005-002-FASES-1-2-3-METODOLOGIA-ANALISIS-FORENSE.png)

[Volver al texto de la imagen en la Sección 1.3.5.](#135-imagen-002-135-imagen-003-135-imagen-004)

---

#### 8.3.001.003.005.003. Fases 4 5 y 6 de la metodología del análisis forense.

![001-003-005-003](./images/001-003-005-003-FASES-4-5-6-METODOLOGIA-ANALISIS-FORENSE.png)

[Volver al texto de la imagen en la Sección 1.3.5.](#135-imagen-002-135-imagen-003-135-imagen-004)

---

#### 8.3.001.003.005.004. Fase 7 de la metodología del análisis forense.

![001-003-005-004](./images/001-003-005-004-FASE-7-METODOLOGIA-ANALISIS-FORENSE.png)

[Volver al texto de la imagen en la Sección 1.3.5.](#135-imagen-002-135-imagen-003-135-imagen-004)

---

#### 8.3.001.003.005.005. Orden de volatilidad análisis forense.

![001-003-005-005](./images/001-003-005-005-ORDEN-VOLATILIDAD-RFC-3227.png)

[Volver al texto de la imagen en la Sección 1.3.5.](#135-Imagen-005)

---

#### 8.3.001.006.001. Diagrama de Gantt reto/PEC 1.

![001-006-001](./images/001-006-001-diagrama-de-gantt-pec-01.png)

[Volver al texto de la imagen en la Sección 1.6.](#16-Imagen-001)

---

---

#### 8.3.001.006.002. Diagrama de Gantt reto/PEC 2.

![001-006-002](./images/001-006-002-diagrama-de-gantt-pec-02.png)

[Volver al texto de la imagen en la Sección 1.6.](#16-Imagen-001)

---

---

#### 8.3.001.006.003. Diagrama de Gantt reto/PEC 3.
![001-006-003](./images/001-006-003-diagrama-de-gantt-pec-03.png)

[Volver al texto de la imagen en la Sección 1.6.](#16-Imagen-003)

---

---

#### 8.3.001.006.004. Diagrama de Gantt reto/PEC 4.

![001-006-004](./images/001-006-004-diagrama-de-gantt-pec-04.png)

[Volver al texto de la imagen en la Sección 1.6.](#16-imagen-004)

---

#### 8.3.003.001.001. Imagen Hash archivos.

![005-imagen-hash-archivos.png](./images/003-001-001-imagen-hash-archivos.png)

[Volver al texto de la imagen en la Sección 3.1.](#31-imagen-001)

---

#### 8.3.003.001.002. Imagen Hash PowerShell.

![003-001-002](./images/003-001-002-captura-hash-PowerShell.png)

[Volver al texto de la imagen en la Sección 006.](#31-imagen-002)

---

#### 8.3.003.002.001. Imagen de imageinfo.

![003-002-001](./images/003-002-001-captura-imageinfo.png)

[Volver al texto de la imagen en la Sección 3.2.](#32-imagen-001)

---

#### 8.3.003.002.002. Imagen de búsqueda de string linux version.

![003-002-002](./images/003-002-002-buscar-strings-linux-version.png)

[Volver al texto de la imagen en la Sección 3.2.](#32-imagen-002)

---

#### 8.3.010. Imagen de buscando caché de AWS.

![009-buscando-cache-aws.png](./images/009-buscando-cache-aws.png)

[Volver al texto de la imagen en la Sección 009.](#imagen-009)

---

#### 8.3.011. Imagen de instalación de kernel de AWS.

![010-instalación-kernel-aws.png](./images/010-instalacion-kernel-aws.png)

[Volver al texto de la imagen en la Sección 010.](#imagen-010)

---

#### 8.3.012. Imagen de reinicio del servidor de AWS.

![011-reinicio-server-aws.png](./images/011-reinicio-server-aws.png)

[Volver al texto de la imagen en la Sección 011.](#imagen-011)

---

#### 8.3.013. Imagen de reinicio del servidor con kernel de AWS.

![012-inicio-con-server-aws.png](./images/012-inicio-con-server-aws.png)

[Volver al texto de la imagen en la Sección 012.](#imagen-012)

---

#### 8.3.013. .

![013-make-clean-clear-make.png](./images/013-make-clean-clear-make.png)

[Volver al texto de la imagen en la Sección 013.](#imagen-013)

---













[Volver al Índice del capítulo 8. Anexos.](#índice-del-capítulo-8-anexos)

[Volver al Índice General.](#índice-general)

---

## 8.4. Videos.

---

#### 8.4.003.002.001. Video de instalación de Volatility en Ubuntu.

[![Miniatura video Volatility](./images/024-miniatura-instalacion-volatility.png)](https://youtu.be/z_SWIIa3AnY)

> [https://www.youtube.com/watch?v=z_SWIIa3AnY](https://www.youtube.com/watch?v=z_SWIIa3AnY)

[Volver al texto del video en la Sección 3.2.](#32-video-001)

---















[Volver al Índice del capítulo 8. Anexos.](#índice-del-capítulo-8-anexos)

[Volver al Índice General.](#índice-general)

---

## 8.5. Extracto de comandos utilizados.

---

#### 8.5.003.001.001. Comando **<u style='color:red'>Hash</u>** MD5.

~~~PowerShell
Get-FileHash .\Server_RAM.mem -Algorithm MD5
~~~

La respuesta de PowerShell es el siguiente:

~~~PowerShell
Algorithm       Hash                                                                   Path
---------       ----                                                                   ----
MD5             75A99B57032AA34BA19042ED85DB273F                                       D:\TFM\RAM\...
~~~

[Volver al texto del comando en la Sección 3.1](#31-comando-001-31-comando-002)


---

#### 8.5.003.001.002. Comando **<u style='color:red'>Hash</u>** SHA1.

~~~PowerShell
Get-FileHash .\Server_RAM.mem -Algorithm SHA1
~~~

La respuesta de PowerShell es el siguiente:

~~~PowerShell
Algorithm       Hash                                                                   Path
---------       ----                                                                   ----
SHA1            CC1FAD2AF321B8C2DDF0103986E3B344EB8F2CC8                               D:\TFM\RAM\...
~~~

[Volver al texto del comando en la Sección 3.1](#31-comando-001-31-comando-002)

---

#### 8.5.003.003.001. Comando linux bash.

~~~
exit

sudo apt update

sudo systemctl restart postfix

ls -l

mysql -uroot -p

cd apache2/

ls -l

sudo vi /etc/mysql/debian.cnf

ps -ef| grep mysql

tail access.log.1

cd /var/www/html

sudo kill -9 4539

ls -als

cd /

ps -ef| grep mysql

sudo mysqld_safe --skip-grant-tables

H?=? &

qls -l tmp

qls -l tmp

cd

exit

vi functions.php

ps -ef| grep mysql

ls -l /var/run/mysqld

ls -l /run

ls -lt

ls -lt| more

vi access.log.1

sudo mysql_secure_installation

ls -l

p?JU

su mysql

tail access.log

cat /var/log/mysql/error.log

cd /var/log

find . -name functions.php

sudo apt install python-certbot-apache

sudo service apache2 restart

ps -ef| grep mysql

mysql -uroot -p

sudo apt-get install apache2

apt-cache search mysql-server

apt-cache search php

mysql -u root -p

ls -l

#1546501785

tail error.log

sudo vi functions.php

sudo mysql

ls -l /var/run

exit

ls -l

apt-cache search php| grep apache

sudo vi /etc/mysql/debian

tail syslog

sudo apt-get install mysql-server

_service

apt-cache search mysql | grep php

sudo cp /home/ubuntu/wordpress-4.9.8.tar.gz  .

cd /var/log

cd

U

H???Nt??nu??6

sudo mysqld_safe --skip-grant-tables &

apt-cache search mysql

pwd

ls -l

ls -l

`uSU

sudo mv * ..

?,YU

sudo mysqld_safe --skip-grant-tables

r="$c_clear$r"

ls -l /run

ls -l

COMPREPLY=($(compgen -W "--help --local" -- $cur_word))

ls -l

sudo tar xzf wordpress-4.9.8.tar.gz

sudo apt-get install aapche2

tail -100 kern.log

mysql -u root -p

cd ..

cd /var/www/html/

ps -ef| grep mysql

apt-cache search php

cd wordpress/

cd hhtml

sudo rm -r wordpress/

ls -l

ls -l

sudo chmod 777 /var/run/mysqld

sudo apt upgrade

ls -l

sudo vi /etc/apache2/sites-enabled/000-default.conf

cd htmlls -l

mysql -uroot -p

ls -l

ls -l

ls -l

sudo chown -R www-data:www-data html

sudo mysqld_safe --skip-grant-tables

cd /var/www/html

find . -name functions.php -exec grep -H add_filer {} \;

sudo apt install libapache2-mod-php

exit

cd /var/lg

suudo mysqld_safe --skip-grant-tables &

ls -l

cd /var/log/apache2/sites-e

mysql -u root -p

cd

sudo service mysql restart

find . -name functions.php -exec grep -H add_filter {} \;

apt-cache search apache2

sudo apt-get update

cat debian

?2JU

echo "Test 1" | mail -s "Test 1" test12312321@mailinator.com

sudo chmod 777 /run/mysqld/

dpkg -l | grep mysql-server

sudo certbot --apache -d ganga.site -d www.ganga.site

ps -ef| grep mysql

cd /var/log/apache2/

sudo mkdir /run/mysqld

cd /etc/mysql/

sudo grep root *

mysql -u root -p

ps -ef| grep mysql

sudo mysqld_safe --skip-grant-tables

mysql -u root

ls -l /run

cd /var/log

cd

sudo dpkg-reconfigure mysql-server-5.7

sudo service mysql stop

cd apache2/

sudo service mysql stop

cat /var/log/mysql/error.log

sudo kill -9 3181

ls -l

mysql -u root

more access.log.1

dpkg -l | grep mysql

chmod 777 /run/mysqld/

g|MP?(E)G|wm[av]|WM[AV]|avi|AVI|asf|vob|VOB|bin|dat|divx|DIVX|vcd|ps|pes|fli|flv|FLV|fxm|FXM|viv|)4[av]|M?(P)4[AV]|mkv|MKV|og[agmvx]|OG[AGMVX]|t[ps]|T[PS]|m2t?(s)|M2T?(S)|mts|MTS|wav|WAV|flac||XM)|+([0-9]).@(vdr|VDR))?(.part)'

sudo kill -9 3182 3542

sudo kill -9 4179

ls

ls -l

sudo service mysql stop

?

ls -l

sudo service apache2 rewtart

ls

sudo apt install mailutils

ls -lt| more

sudo cat debian.cnf

exit

pwd

mysql -u root -p

cat /etc/issue

cd wordpress/

tail error.log

tail error.log

vi access.log

cd ..

cd wp-content/themes/twentyseventeen/

sudo systemctl restart psotfix

ls -l

exit

mysql_secure_installation

mysql -uroot -p

sudo cat /etc/mysql/debian

ls -l tmp

mysql -u root -p

tail syslog

cd /tmp

exit

cd html

find . -name functions.php -exec grep -H add_filter {} \;

cat debian.cnf

mysql -u root

suudo mysql_secure_installation

sudo cat /etc/mysql/debian.cnf

sudo service apache2 retart

sudo rm index.html

sudo rm -r /run/mysqld

sudo vi wp-config.php

sudo systemctl reload apache2

sudo service mysql start

sudo vi /etc/postfix/main.cf

tail access.log

tail -100 syslog

ps -ef| grep mysql

cd /var/log/apache2/

ls- l

pwd

vi index.html

sudo apachectl configtest

ps -ef| grep mysql

sudo mkdir /var/run/mysqld

tail access.log

exit

sudo add-apt-repository ppa:certbot/certbot

tail access.log

ls -l

tail -100 access.log

tail -100 access.log

execute-command

sudo mysqld_safe --skip-grant-tables &

sudo kill 3181

exit

!

sudo service apache2 restart

sudo apt install php-mysql

date

cd ap

ls -l

grep POST access.log

ls -l

vi access.log

ls -l

cd home

cd /var/log

sudo apchectl configtest

sudo service mysql start

sudo vi /etc/php/7.2/apache2/php.ini

sudo kill -9 4178

tail -100 syslog

ps -ef| grep mysql

tail -100 syslog

sudo rm wordpress-4.9.8.tar.gz

ls -l /run

??OU

ls -l /etc/cron.d

ls -l

cd /tmp

sudo insmod lime-4.15.0-42-generic.ko "path=captura.mem format=lime"

cat /etc/issue

uname -a

ls -l

rm lime-4.15.0-42-generic.ko

ls -l

sudo insmod lime-4.15.0-1021-aws.ko "path=captura.mem format=lime"
~~~





[Volver al texto del comando en la Sección 3.1](#33-comando-001)


---


[Volver al Índice del capítulo 8. Anexos.](#índice-del-capítulo-8-anexos)

[Volver al Índice General.](#índice-general)

---

## 8.6. Referencias.

---

#### 8.6.001. Enunciado TFM:

- Autor: Universitat Oberta de Catalunya.
- Título del trabajo: Enunciado TFM - Análisis forense.
- Título del Contenedor: Descripción del caso.
- URL: [https://drive.google.com/file/d/1TOKWOF_akO6IKVvXJ9ovPxMMhd9kafy1/view](https://drive.google.com/file/d/1TOKWOF_akO6IKVvXJ9ovPxMMhd9kafy1/view)
- URL repositorio Github: [ENUNCIADO-M1.881-TFM-ANÁLISIS-FORENSE-SISTEMAS-INFORMÁTICOS.pdf](https://github.com/jrodg85/TFM-ANALISIS-FORENSE/blob/main/referencias/001-ENUNCIADO-M1.881-TFM-ANALISIS-FORENSE-SISTEMAS-INFORMATICOS.pdf)

[Volver at texto de la referencia en la Sección 1.0.](#10-referencia-001)

[Volver at texto de la referencia en la Sección 1.2.](#12-referencia-001-12-referencia-003)

---

#### 8.6.002. Propuestas de TFM:

- Autor: Universitat Oberta de Catalunya.
- Título del trabajo: M1.881 - AnálisiS forense.
- Título del Contenedor: Descripción.
- URL: [https://docs.google.com/spreadsheets/d/16JGkkrY4fiPN32RAfdpVuLJBZrnewscpmuTelbe3X_o/edit#gid=0](https://docs.google.com/spreadsheets/d/16JGkkrY4fiPN32RAfdpVuLJBZrnewscpmuTelbe3X_o/edit#gid=0)
- URL repositorio Github: [002-PROPUESTA-TFM-EXCEL.pdf](https://github.com/jrodg85/TFM-ANALISIS-FORENSE/blob/main/referencias/002-PROPUESTA-TFM-EXCEL.pdf)

[Volver at texto de la referencia en la Sección 1.1.](#11-referencia-002)

---
#### 8.6.003. El método Reagan:

- Autor: GEFIRA.
- Título del trabajo: El método Reagan.
- URL: [https://www.xn--elespaoldigital-3qb.com/el-metodo-reagan/](https://www.xn--elespaoldigital-3qb.com/el-metodo-reagan/)

[Volver at texto de la referencia en la Sección 1.2.](#12-referencia-001-12-referencia-003)

---

#### 8.6.004. Norma ISO 27037:

- Autor: International Organization for Standardization.
- Título del trabajo: Information technology — Security techniques — Guidelines for identification, collection, acquisition, and preservation of digital evidence.
- URL: [https://www.amnafzar.net/files/1/ISO%2027000/ISO%20IEC%2027037-2012.pdf](https://www.amnafzar.net/files/1/ISO%2027000/ISO%20IEC%2027037-2012.pdf)
- URL repositorio Github: [003-ISOIEC-27037-2012.pdf](https://github.com/jrodg85/TFM-ANALISIS-FORENSE/blob/main/referencias/003-ISOIEC-27037-2012.pdf)

[Volver at texto de la referencia en la Sección 1.3.2.](#132-referencia-004)

---

#### 8.6.005. IMPLEMENTACIÓN DE HERRAMIENTAS PARA LA EXTRACCIÓN DE EVIDENCIA DIGITAL:

- Autor: ANTHONY ALEXANDER GUZMÁN MOLINA.
- Título del trabajo: IMPLEMENTACIÓN DE HERRAMIENTAS PARA LA EXTRACCIÓN DE EVIDENCIA DIGITAL .
- Título del Contenedor: ISO/IEC 30121.
- URL: [https://bibdigital.epn.edu.ec/bitstream/15000/23797/1/CD%2013084.pdf](https://bibdigital.epn.edu.ec/bitstream/15000/23797/1/CD%2013084.pdf)
- URL repositorio Github: [004-IMPLEMENTACIÓN-HERRAMIENTAS-PARA-LA-EXTRACCIÓN-DE-EVIDENCIA-DIGITAL.pdf](https://github.com/jrodg85/TFM-ANALISIS-FORENSE/blob/main/referencias/004-IMPLEMENTACION-HERRAMIENTAS-PARA-LA-EXTRACCION-DE-EVIDENCIA-DIGITAL.pdf)

[Volver at texto de la referencia en la Sección 1.3.2.](#132-referencia-005)

---

#### 8.6.006. Norma RFC 3227:

- Autores:  Dominique Brezinski & Tom Killalea.
- Título del trabajo: RFC 3227.
- URL Español: [https://www.rfc-es.org/pendientes/rfc3227-es.nroff](https://www.rfc-es.org/pendientes/rfc3227-es.nroff)
- URL Inglés: [https://datatracker.ietf.org/doc/html/rfc3227](https://datatracker.ietf.org/doc/html/rfc3227)
- URL repositorio Github: [005-RFC-3227-ESP.pdf](https://github.com/jrodg85/TFM-ANALISIS-FORENSE/blob/main/referencias/005-RFC-3227-ESP.pdf)

[Volver at texto de la referencia en la Sección 1.3.3.](#133-referencia-006)

---

#### 8.6.007. Que son las normas UNE:

- Autor:  Grupo ACMS Consultores.
- Título del trabajo: Norma UNE: Significado y Estructura.
- URL Español: [https://www.grupoacms.com/consultora/norma-une-significado](https://www.grupoacms.com/consultora/norma-une-significado)

[Volver at texto de la referencia en la Sección 1.3.4.](#134-referencia-007)

---

#### 8.6.008. Metodología para un análisis forense:

- Autores: Carles Gervilla Rivas.
- Título del trabajo: Metodología para un Análisis Forense.
- Título del Contenedor: DESARROLLO DE UNA METODOLOGÍA PARA EL ANÁLISIS FORENSE.
- URL: [https://openaccess.uoc.edu/bitstream/10609/39681/6/cgervillarTFM1214memoria.pdf](https://openaccess.uoc.edu/bitstream/10609/39681/6/cgervillarTFM1214memoria.pdf)
- URL repositorio Github: [007-METODOLOGÍA-PARA-UN-ANÁLISIS-FORENSE.pdf](https://github.com/jrodg85/TFM-ANALISIS-FORENSE/blob/main/referencias/007-METODOLOGÍA-PARA-UN-ANÁLISIS-FORENSE.pdf)

[Volver at texto de la referencia en la Sección 1.3.5.](#135-referencia-008-135-referencia-009)

---

#### 8.6.009. Ninjas de la web. Metodología para un análisis forense:

- Autor: Miguel Angel Olivares.
- Título del trabajo: Metodología de Análisis Forense (Ninjas de la Web).
- URL: [https://ninjasdelaweb.com/metodologia-de-analisis-forense/](https://ninjasdelaweb.com/metodologia-de-analisis-forense/)

[Volver at texto de la referencia en la Sección 1.3.5.](#135-referencia-008-135-referencia-009)

---

#### 8.6.010. Cómputo Forense de Wikipedia

- Autor: Avelaz
- Ultimo editor: Sabbut
- Título visualizado: Cómputo forense
- Criterio de ordenación predeterminado: Cómputo forense
- URL: [https://es.wikipedia.org/wiki/C%C3%B3mputo_forense](https://es.wikipedia.org/wiki/C%C3%B3mputo_forense)

[Volver at texto de la referencia en la Sección 1.7.](#17-referencia-010)


[Volver al Índice del capítulo 8. Anexos.](#índice-del-capítulo-8-anexos)

[Volver al Índice General.](#índice-general)

---

## 8.7. Linea de tiempo de evidencias.




[Volver al Índice del capítulo 8. Anexos.](#índice-del-capítulo-8-anexos)

[Volver al Índice General.](#índice-general)

---