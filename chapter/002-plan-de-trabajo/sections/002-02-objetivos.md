Se describe un el siguiente listado de objetivos que se obtienen al analizar el enunciado del TFM:

\begin{enumerate}
    \item Elaboración del Análisis forense de Disco Duro y RAM.
    \begin{enumerate}
        \item realizar una recuperación parcial o total de la información borrada existente en los dispositivos susceptibles de ser analizados (carving).
        \item Relativo al análisis de la memoria RAM.
        \begin{enumerate}
            \item Comprobar la integridad de la memoria RAM.
            \item Comprobar fecha de la captura de la RAM.
            \item Determinar la edición y versión de Windows que tiene instalado el sistema operativo del ordenador sobre el cual se ha efectuado la captura de la memoria RAM.
            \item Buscar los procesos en funcionamiento y localiza aquellos que te parezcan de interés para el análisis forense del ordenador analizado.
            \item Extraer los procesos que consideres sospechosos y analizarlos.
            \item Listar las conexiones de red y analizarlas.
        \end{enumerate}
        \item Relativo al análisis del Disco Duro.
        \begin{enumerate}
            \item Comprobar la integridad del disco duro.
            \item Determinar la siguiente información del disco duro.
            \begin{enumerate}
                \item Tamaño del disco duro analizado.
                \item Sistema y versión del sistema operativo instalado.
                \item Nombre del propietario y relación de software instalado.
                \item "Product ID" y "Product Key" asociadas al sistema.
                \item Fecha y hora de instalación del sistema operativo.
                \item Determinar marca y modelo (si es posible) del hardware siguiente: CPU, monitor, tarjeta gráfica, tarjeta Ethernet y Wireless.
            \end{enumerate}
            \item Determinar qué usuarios tiene definidos el sistema.
            \item Localizar los documentos (archivos PDF, de texto, hojas de cálculo, etc.) que puedan tener relación con alguna conducta presuntamente delictiva.
            \item Localizar los archivos eliminados y determina si hay alguno relevante para la causa investigada.
            \item Localizar los ficheros comprimidos relevantes analizarlos, reventar contraseña si es necesario y analizar su contenido.
            \item Localizar algún fichero ejecutable que pueda resultar de interés para la investigación, ademas, analizar la relación con alguna evidencia anterior.
            \item Determinar el contenido del fichero log de un conocido programa de comunicación si es necesario y relacionarlo con el caso investigado.
            \item Realizar un análisis de la navegación web.
            \item Estudio de los dispositivos físicos que en algún momento fueron conectados al sistema estudiado: móviles, USBs, impresoras, escáneres, cámaras, tarjetas de memoria.
            \item Estudio de la información contenida en los unallocated cluster o en el file slack.
            \item Información contenida en los archivos de hibernación, paginación, particiones y archivos de intercambio (swap).
            \item Análisis de la cola de impresión.
            \item Visualización de los links de los archivos y de los archivos accedidos recientemente.
            \item Estudio de los metadatos de los archivos, si se considera que pueden ser relevantes para el caso.
            \item Estudio de las aplicaciones de virtualización.
            \item Estudio de las bases de datos instaladas y las aplicaciones que permiten su gestión.
            \item Estudio de los programas de cifrado, particiones cifradas.
            \item Análisis de los clientes de correo electrónico y del webmail.
        \end{enumerate}
        \item Realizar un estudio de la seguridad.
            \begin{enumerate}
                \item Estudiar si las evidencias analizadas han sido comprometidas.
                \item Identificar cualquier aplicación vulnerable, software malicioso, evaluar el daño sufrido, identificar los archivos que han sido comprometidos, así como determinar la vía de acceso al sistema.
            \end{enumerate}
        \end{enumerate}
    \item Relativo al resumen ejecutivo, elaborarlo teniendo en cuenta los siguientes apartados.
    \begin{enumerate}
        \item Claridad en la comunicación, proporcionando información de forma clara y concisa y, por otro lado, utilizar un lenguaje accesible para los no expertos en el área.
        \item Presentar el contexto u antecedentes, describiendo el motivo y las circunstancias del análisis forense y Proporcionar una breve descripción del incidente o situación bajo investigación.
        \item Redactar un resumen ejecutivo con los hallazgos clave y las recomendaciones.
        \item Describir la metodología utilizada durante el análisis forense.
        \item Explicar las herramientas y técnicas de análisis implementadas.
        \item Proporcionar una línea de tiempo detallada de los eventos y acciones tomadas.
        \item Detallar los hallazgos significativos del análisis.
        \item Incluir evidencia técnica relevante, como registros de logs, archivos, etc
        \item Evaluar y describir el impacto del incidente en la organización o individuos afectados.
        \item Proveer conclusiones basadas en los hallazgos del análisis forense.
        \item Proporcionar recomendaciones para la acción futura, basadas en los hallazgos y conclusiones.
        \item Sugerir medidas preventivas y correctivas para evitar incidentes similares en el futuro.
    \end{enumerate}
    \item Elaborar un informe pericial teniendo en cuenta los siguientes apartados.
    \begin{enumerate}
        \item Mantener una postura objetiva e imparcial en todo momento.
        \item Garantizar que el análisis y las conclusiones estén fundamentados en evidencias tangibles y replicables.
        \item Mantener la cadena de custodia y la integridad de las pruebas durante todo el proceso.
        \item Redactar el informe de manera clara, precisa y entendible para personas sin conocimientos técnicos específicos.
        \item Describir detalladamente el caso, partes involucradas, y el objeto del peritaje.
        \item Detallar las herramientas, técnicas y procedimientos utilizados en el análisis forense.
        \item Justificar la elección de la metodología y herramientas utilizadas.
        \item Establecer una línea temporal clara de todas las acciones y procesos llevados a cabo durante la investigación
        \item Presentar de forma clara y precisa los hallazgos resultantes del análisis forense. Los cuales será
        \item Incluir elementos visuales como gráficos, imágenes o tablas para facilitar la comprensión de los datos.
        \item Interpretar las evidencias de manera fundamentada y ligada a las normativas y principios de la ciencia forense digital.
        \item Derivar conclusiones basadas exclusivamente en las evidencias y hallazgos del análisis.
        \item Ofrecer una opinión pericial en base a los hallazgos, respetando los límites de la prueba pericial y los datos disponibles.
        \item Garantizar que toda la información manejada se mantiene confidencial y segura.
        \item Discutir las implicaciones legales de los hallazgos y su posible impacto en el caso.
        \item Estar preparado para ratificar el informe en un tribunal y responder a preguntas relacionadas con el análisis y los hallazgos. Este supuesto, el defensor se intuye que se realizará en la defensa síncrona de la defensa de este TFM.
    \end{enumerate}
    \item Realizar unas conclusiones acordes a todo el TFM realizado.
    \begin{enumerate}
        \item Basarse en ideas fuerza que han aparecido durante todo el TFM.
        \item Tener en cuenta que este apartado es el que finalmente, el gerente de la empresa, como miembro directivo de la misma, usando el método del Presidente {\color{red}\textbf{DEUDA TÉCNICA: Buscar presidente de los EE.UU., preguntar a "//4lanoga"}}.
    \end{enumerate}
\end{enumerate}


{\color{red}\textbf{DEUDA TÉCNICA: Pendiente de Referenciar!!! ENUNCIADO TFM}}
