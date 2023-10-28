\subsection{Introducción}

El análisis forense, también llamado informática forense, computación forense, análisis forense digital o examen forense digital es la aplicación de técnicas científicas y analíticas especializadas a infraestructuras tecnológicas que permiten identificar, preservar, analizar y presentar datos válidos dentro de un proceso legal.

Dichas técnicas incluyen reconstruir elementos informáticos, examinar datos residuales, autenticar datos y explicar las características técnicas del uso de datos y bienes informáticos.

Esta disciplina no sólo hace uso de tecnologías de punta para mantener la integridad de los datos y del procesamiento de los mismos; sino que también requiere de una especialización y conocimientos avanzados de informática y sistemas para identificar lo que ha ocurrido dentro de cualquier dispositivo electrónico. La formación de un informático forense abarca no sólo el conocimiento del software, sino también de hardware, redes, seguridad, piratería, hackeo y recuperación de información.

La informática forense ayuda a detectar pistas sobre ataques informáticos, robos de información, conversaciones o para recolectar evidencias en correos electrónicos y chats.

La evidencia digital o electrónica es sumamente frágil, de ahí la importancia de mantener su integridad; por ejemplo, el simple hecho de pulsar dos veces en un archivo modificaría la última fecha de acceso del mismo.

Dentro del proceso del análisis forense, un examinador forense digital puede llegar a recuperar información que haya sido borrada desde el sistema operativo. El informático forense debe tener muy presente el principio de intercambio de Locard por su importancia en el análisis criminalístico, así como el estándar de Daubert para hacer admisibles en juicio las pruebas presentadas por el experto forense.

Es muy importante mencionar que la informática o el análisis forense no tiene como objetivo prevenir delitos, por lo que resulta imprescindible tener claros los distintos marcos de actuación de la informática forense, la seguridad informática y la auditoría informática.

\subsection{Definiciones.}

Existen diferentes términos referentes a la ciencia forense en informática. Cada uno de estos términos trata de manera particular o general temas que son de interés para las ciencias forenses.

\begin{itemize}
    \item \textbf{Computación forense (computer forensics):}
    \begin{itemize}
        \item Disciplina de la ciencia forense que considera los procedimientos en relación con las evidencias para descubrir e interpretar la información en los medios informáticos con el fin de establecer hipótesis o hechos relacionados con un caso. (Centrada en las consideraciones forenses).
        \item Disciplina científica que ofrece un análisis de la información que contienen las tecnologías y de los equipos de computación a partir de su compresión.(Centrada en la tecnología).
    \end{itemize}
    \item \textbf{Ciencia forense en las redes (network forensics):}
    \begin{itemize}
        \item Trata las operaciones de redes de computadores, estableciendo rastros e identificando movimientos y acciones. Es necesario entender los protocolos, configuraciones y la infraestructura de las comunicaciones. A diferencia de la computación forense, es necesario poder establecer relaciones entre eventos diferentes e incluso aleatorios.
    \end{itemize}
    \item \textbf{Ciencia forense digital (digital forensics):}
    \begin{itemize}
        \item Es una forma de aplicar los conceptos y procedimientos de la criminalística a los medios informáticos o digitales. Su objetivo es apoyar al poder judicial en el contexto de la inseguridad informática es decir, la perpetración de posibles delitos aclarando temas relacionados con incidentes o fraudes.
    \end{itemize}
\end{itemize}

\subsection{Objetivos de la informática forense.}

La informática forense tiene tres objetivos:

\begin{enumerate}
    \item La compensación de los daños causados por los intrusos o criminales.
    \item La persecución y procesamiento judicial de los criminales.
    \item La creación y aplicación de medidas para prevenir casos similares.
\end{enumerate}

Estos objetivos se alcanzan de varias formas, siendo la principal la recopilación de evidencias.

Es importante mencionar que quienes se dedican a la informática forense deben ser profesionales con altos niveles de ética, pues gracias a su trabajo se toman decisiones sobre los hechos y casos analizados.

\subsection{Evidencia digital.}

Los discos duros, las memorias USB y las impresoras (entre otros elementos) se pueden considerar evidencias en un proceso legal, al igual que las huellas digitales o las armas. Las evidencias digitales son las que se extraen de un medio informático.

\textbf{Características.}

Estas evidencias comparten una serie de características que dificultan el ejercicio de la computación forense:

\begin{enumerate}
    \item Volatilidad.
    \item Anonimato.
    \item Facilidad de duplicación.
    \item Alterabilidad.
    \item Facilidad de eliminación.
\end{enumerate}

\textbf{Categorías.}

Estas evidencias se pueden dividir en tres categorías:

\begin{enumerate}
    \item Registros almacenados en el equipo de tecnología informática (ej. imágenes y correos).
    \item Registros generados por equipos de tecnología informática (ej. transacciones, registros en eventos).
    \item Registros parcialmente generados y almacenados en los equipos de tecnología informática (ej. consultas en bases de datos).
\end{enumerate}


\textbf{Dispositivos a analizar.}

Cualquier infraestructura informática que tenga una memoria (almacenamiento) es susceptible a los análisis:

\begin{itemize}
    \item Disco duro de una Computadora o Servidor.
    \item Documentación referente al caso.
    \item Tipo de sistema de telecomunicaciones.
    \item Dirección MAC.
    \item Inicios de sesiones.
    \item Información de los cortafuegos.
    \item IP, redes Proxy. LMhost, host, conexiones cruzadas, pasarelas.
    \item Software de supervisión y seguridad.
    \item Credenciales de autentificación.
    \item Rastreo de paquetes de red.
    \item Teléfonos móviles o celulares (telefonía móvil)
    \item Agendas electrónicas (PDA).
    \item Dispositivos de GPS.
    \item Impresoras.
    \item Memorias USB.
    \item BIOS.
\end{itemize}

\subsection{Perspectiva de tres roles.}

En el análisis de un caso en el que sea necesario el cómputo forense, hay tres roles principales que son importantes y se deben tener en cuenta: el intruso, el administrador y la infraestructura de la seguridad informática, al igual que el investigador.

\textbf{Intrusos}

El intruso es aquel que ataca un sistema, hace cambios no autorizados, manipula contraseñas o cambia configuraciones, entre otras actividades que ponen a prueba la seguridad de un sistema. La intención de los intrusos es un punto clave para poder analizar el caso, ya que no se puede comparar un intruso cuya motivación es el dinero con otro cuya motivación es la demostración de sus habilidades. Jeimy J. Cano hace una comparación entre las motivaciones de diferentes tipos de atacantes, basada en el artículo de Steven Furnell, Cybercrime.

En la primera fase (reconocimiento), se busca reconocer y recolectar información. De esta manera, el atacante puede saber cómo puede actuar y los riesgos posibles, para así poder avanzar. En la segunda fase (ataque) se compromete el sistema, avanzando hasta el nivel más alto, teniendo el control del sistema atacado. Esta etapa usualmente se maneja de manera discreta, lo que dificulta la identificación del intruso. Usualmente, la vanidad del intruso y la falta de discreción ayudan al investigador a resolver el caso con mayor facilidad. Finalmente, (en la fase de eliminación) se altera, elimina o desaparece toda la evidencia que pueda comprometer al intruso en algún caso judicial. Del cuidado con el que el atacante proceda en esta fase depende el proceso del informático forense y del caso.

\textbf{Administradores y la infraestructura de la seguridad informática}

El administrador del sistema es el experto encargado de la configuración de este, de la infraestructura informática y de la seguridad del sistema. Estos administradores son los primeros en estar en contacto con la inseguridad de la información, ya sea por un atacante o por una falla interna de los equipos. Al ser los arquitectos de la infraestructura y de la seguridad de la información del sistema, son quienes primero deberían reaccionar ante un ataque. Además, ellos deben proporcionar su conocimiento de la infraestructura del sistema para apoyar el caso y poder resolverlo con mayor facilidad.

Las infraestructuras de seguridad informática (realizadas por el administrador) han avanzado a medida que avanzan las tecnologías. Inicialmente, se utilizaba una infraestructura centralizada en la cual la información se encontraba en un equipo. Por lo tanto, en este caso la seguridad informática se concentraba en el control del acceso a los equipos con la información, al control del lugar en donde se encontraban y en el entrenamiento de quienes estaban encargados de manejar los equipos. Pero con la tecnología fueron cambiando las infraestructuras y las inseguridades cambiaron. Así es como se crearon los proxies, firewall, el sistema de detección de intrusos (IDS) , el sistema de prevención de intrusos (IPS) entre muchas otras herramientas para proveer una mejor seguridad a los sistemas, ya que ahora el acceso no ocurría solo a través de la máquina, sino a través de otras y de la Web.

Por otro lado, es importante hablar de la auditabilidad y trazabilidad, que son propiedades del sistema, relacionados con la infraestructura que son útiles como evidencia para el investigador. La auditabilidad es la capacidad del sistema para registrar los eventos de una acción en particular con el fin de mantener la historia de estos y de realizar un control con mayor facilidad. En cambio, la trazabilidad es la propiedad que tiene un sistema para rastrear o reconstruir relaciones entre diferentes objetos monitorizados.

Es importante resaltar que el administrador debe conocer lo suficiente sobre la infraestructura del sistema para poder colaborar con el caso, ya que su análisis puede facilitar el proceso del investigador forense. Adicionalmente, contar con los rastros y registro de eventos (Auditoría informática) en los sistemas es crucial para el administrador y su infraestructura, no solo porque genera confianza en sus clientes, sino también porque es una buena práctica en términos de seguridad para toda la empresa.

\textbf{Investigador}

Es un nuevo profesional que actúa como experto, criminalista digital, o informático. Comprende y conoce las nuevas tecnologías de la información. Además, el investigador analiza la inseguridad informática emergente en los sistemas. El perfil del investigador es nuevo y necesario en el contexto abierto informático en el que vivimos. Por lo tanto, es necesario formar personas que puedan trabajar como investigadores en la disciplina emergente de la criminalística digital y el cómputo forense. Estas prácticas emergentes buscan articular las prácticas generales de la criminalística con las evidencias digitales disponibles en una escena del crimen. El trabajo del informático es indagar en las evidencias, analizarlas y evaluarlas para poder decidir cómo estas evidencias pueden ayudar a resolver el caso. Por lo tanto, es ideal que un investigador tenga conocimientos (al menos) sobre las siguientes áreas: justicia criminal, auditoría, administración y operación de tecnologías de Información.

En una investigación informática forense, hay ocho roles principales en un caso: el líder del caso, el propietario del sistema, el asesor legal, el auditor/ingeniero especialista en seguridad de la información, el administrador del sistema, el especialista en informática forense, el analista en informática forense y el fiscal. Usualmente, entre todos estos roles, los informáticos forenses pueden tomar los siguientes cuatro roles:


\begin{enumerate}
    \item - Líder del caso:

    Es aquel que planea y organiza todo el proceso de investigación digital. Debe identificar el lugar en donde se realizará la investigación, quienes serán los participantes y el tiempo necesario para esta.

    \item Auditor/ingeniero especialista en seguridad de la información:

    Conoce el escenario en donde se desarrolla la investigación. Tiene el conocimiento del modelo de seguridad, los usuarios y las acciones que pueden realizar en el respectivo sistema. A partir de sus conocimientos debe entregar información crítica a la investigación.

    \item Especialista en informática forense:

    Es un criminalista digital que debe identificar los diferentes elementos probatorios informáticos vinculados al caso, determinando la relación entre los elementos y los hechos para descubrir el autor del delito.

    \item Analista en informática forense:

    Examina en detalle los datos, los elementos informáticos recogidos en la escena del crimen con el fin de extraer toda la información posible y relevante para resolver el caso.

\end{enumerate}

\subsection{Pasos del proceso del cómputo forense.}

A continuación se describe el proceso de análisis forense:

\textbf{Identificación}

Es muy importante conocer los antecedentes a la investigación "HotFix", la situación actual y el proceso que se quiere seguir para poder tomar la mejor decisión con respecto a las búsquedas y las estrategias (debes estar bien programado y sincronizado con las actividades a realizar, herramientas de extracción de los registros de información a localizar). Incluye muchas veces (en un momento específico observar, analizar e interpretar y aplicar la certeza, esto se llama criterio profesional que origina la investigación) la identificación del bien informático, su uso dentro de la red, el inicio de la cadena de custodia (proceso que verifica la integridad y manejo adecuado de la evidencia), la revisión del entorno legal que protege el bien y del apoyo para la toma de decisión con respecto al siguiente paso una vez revisados los resultados.

\textbf{Preservación}

Este paso incluye la revisión y generación de las imágenes forenses de la evidencia para poder realizar el análisis. Esta duplicación se realiza utilizando tecnología punta para poder mantener la integridad de la evidencia y la cadena de custodia requerida (soportes). Al realizar una imagen forense, nos referimos al proceso que se requiere para generar una copia "bit-a-bit" (copia binaria) de todo el disco duro, el cual permitirá recuperar (en el siguiente paso) toda la información contenida y borrada del disco duro. Para evitar la contaminación del disco duro, normalmente se ocupan bloqueadores de escritura de hardware, los cuales evitan el contacto de lectura con el disco, lo que provocaría una alteración no deseada en los medios.

\textbf{Análisis}

Proceso de aplicar técnicas científicas y analíticas a los medios duplicados por medio del proceso forense para poder encontrar pruebas de ciertas conductas. Se pueden realizar búsquedas de cadenas de caracteres, acciones específicas del o de los usuarios de la máquina como son el uso de dispositivos de USB (marca, modelo), búsqueda de archivos específicos, recuperación e identificación de correos electrónicos, recuperación de los últimos sitios visitados, recuperación de la caché del navegador de Internet, etc.

\textbf{Presentación}

Es la recopilación de toda la información que se obtuvo a partir del análisis para realizar el reporte y la presentación a los abogados, jueces o instancias que soliciten este informe, la generación (si es el caso) de una pericial y de su correcta interpretación sin hacer uso de tecnicismos; se deberá presentar de manera cauta, prudente y discreta al solicitante la documentación, ya que siempre existirán puertas traseras dentro del sistema en observación. Debe ser muy específica la investigación dentro del sistema que se documenta porque se compara y vincula una plataforma de telecomunicación y cómputo forense que están muy estrechamente enlazadas, sin olvidar los medios de almacenamiento magnéticos portables basados en software libre y privativo. La información que se transmite debe manejarse con cuidado, porque el prestigio técnico depende de las plataformas y los sistemas

Para poder realizar con éxito su trabajo, el investigador nunca debe olvidar:

\begin{itemize}
    \item Ser imparcial. Solamente analizar y reportar lo encontrado.
    \item Realizar una investigación formal sin conocimiento y experiencia.
    \item Mantener la cadena de custodia (proceso que verifica la integridad y manejo adecuado de la evidencia).
    \item Documentar toda actividad realizada.
\end{itemize}

El especialista debe conocer también sobre:

\begin{itemize}
    \item Desarrollo de los exploit (vulnerabilidades), esto le permite al informático forense saber qué tipo de programas se pondrán de moda, para generar una base de estudio que le permita observar patrones de comportamiento.
\end{itemize}



\subsection{Retos y riesgos en el cómputo forense.}

Al estar en un escenario que evoluciona constantemente, cada vez surgen más retos y riesgos en el área de la informática forense. Entre ellos la formación de informáticos forenses, la confiabilidad de las herramientas, la facilidad de la destrucción de las evidencias, las amenazas estratégicas y tácticas que plantea el ciberterrorismo; y las tecnologías emergentes como la nube, las tecnologías móviles, y las redes sociales. Algunos de estos temas se abordarán a continuación:

\textbf{Formación de informáticos forenses.}

Los criminales informáticos son una nueva generación de delincuentes, en este contexto, es necesario desarrollar un nuevo tipo de investigadores: los informáticos forenses. En este momento es un desafío encontrar personas que tengan este perfil, ya que no existen suficientes programas que realicen este tipo de formación. Adicionalmente, en este momento, la mayoría de las personas ignoran la importancia de los informáticos forenses porque no son conscientes de la dimensión del cibercrimen. Usualmente se cree que no es algo tan grave y se le da mayor importancia a otro tipo de crímenes.

Por lo tanto, se deben plantear programas e iniciativas para poder realizar esta formación. Según investigaciones e iniciativas ya realizadas, hay cuatro componentes principales que deben estar presentes en un programa de computación forense o forensia digital: contenido multidisciplinario, ejercicios prácticos, profesores de calidad y ejemplos del mundo real (investigación de Taylor Endicott-Popovsky y Phillips, 2007).

\begin{itemize}
    \item \emph{Contenido multidisciplinario:} técnico en informática, conocimiento de criminalística, seguridad y delitos informáticos, entre otros.
    \item \emph{Ejercicios prácticos en el laboratorio:} con herramientas tecnológicas forenses, en diferentes niveles de dificultad y variedad de componentes a analizar.
    \item \emph{Profesores calificados:} con alto conocimiento en el tema.
    \item \emph{Ejemplos del mundo real:} con el fin de dar mayor profundidad al aprendizaje.
\end{itemize}



\textbf{Confiabilidad de las herramientas.}

Las herramientas existentes disponibles para el cómputo forense presentan otro reto. Las herramientas licenciadas exigen a los investigadores inversiones altas (tanto en hardware, como en software), al adquirirlas y para mantenerlas. Adicionalmente, como las herramientas están avanzando constantemente requieren técnicos y usuarios que estén constantemente aprendiendo las actualizaciones, las modificaciones y los posibles errores. Por otro lado, las herramientas de código abierto son cuestionadas en muchos tribunales por su confiabilidad. Por lo tanto, no se recomiendan a la hora de usarse en una audiencia.

Es por esto que el NIST (National Institute of Standards and Technology de Estados Unidos) ha planteado importantes investigaciones para probar y poner reglas para las herramientas del cómputo forense, en su proyecto NIST Computer Forensic Tool Testing Program. Las pruebas realizadas serán útiles para cumplir las exigencias del test de Daubert standard, prueba que establece la confiabilidad de las herramientas en computación forense.

\subsection{Herramientas de Análisis Forense.}

La siguiente tabla compara cuatro herramientas reconocidas internacionalmente al ser muy completas. Luego, se encuentra una lista más completa de herramientas útiles para la labor del investigador.


\begin{table}[h!]
    \centering
    \caption{Comparativa de herramientas forenses:}
    \begin{tabular}{|l|c|c|c|c|}
        \hline
        Herramienta & Licencia & Imagen & Control de Integridad & Administración del caso \\
        \hline
        Encase & SÍ & SÍ & SÍ & SÍ \\
        \hline
        Forensic Toolkit & SÍ & SÍ & SÍ & SÍ \\
        \hline
        Winhex & SÍ & SÍ & SÍ & SÍ \\
        \hline
        Sleuth Kit & NO & SÍ & SÍ & SÍ \\
        \hline
    \end{tabular}
    \label{table:comparativa_herramientas}
\end{table}

\begin{itemize}
    \item Air (Forensics Imaging GUI).
    \item Autopsy (Forensics Browser for Sleuth Kit)Cryptcat (Command Line)Deep Freeze.
    \item Dcfldd (DD Imaging Tool command line tool and also works with AIR).
    \item Dumpzilla (Forensics Browser: Firefox, Iceweasel and Seamonkey).
    \item Encase: \url{https://www.guidancesoftware.com/encase-forensic?cmpid=nav_r}.
    \item Exif Viewer (Visor de metadatos en imágenes).
    \item Faces.
    \item Foremost (Data Carver command line tool).
    \item Forensik Toolkit: \url{https://accessdata.com/products-services/forensic-toolkit-ftk}.
    \item Helix.
    \item Hetman software (Recuperador de datos borrados por los criminales).
    \item Hiren´s boot.
    \item Md5deep (MD5 Hashing Program).
    \item Metashield Analyser Online (Analizador de metadatos online).
    \item Mini XP.
    \item NTFS-Tools.
    \item Netcat (Command Line).
    \item Net resident.
    \item NetFlow.
    \item Py-Flag (Forensics Browser).
    \item Qtparted (GUI Partitioning Tool).
    \item R-Studio Emergency (Bootable Recovery media Maker).
    \item R-Studio Network Edtion.
    \item R-Studio RS Agent.
    \item Regviewer (Windows Registry).
    \item Sleuth Kit (Forensics Kit. Command Line): \url{https://www.sleuthkit.org/}.
    \item Snort.
    \item Viewer.
    \item Volatility (Reconstrucción y análisis de memoria RAM).
    \item X-Ways Forensics.
    \item X-Ways WinHex \url{https://www.x-ways.net/winhex/}.
    \item X-Ways WinTrace.
\end{itemize}


\noindent \textbf{Herramientas para el análisis de discos duros:}

\begin{itemize}
    \item AccessData Forensic ToolKit (FTK).
    \item Guidance Software EnCase.
    \item Kit Electrónico de Transferencia de datos.
\end{itemize}

\noindent \textbf{Herramientas para el análisis de correos electrónicos:}

\begin{itemize}
    \item Paraben.
    \item AccessData Forensic ToolKit (FTK).
\end{itemize}

\noindent \textbf{Herramientas para el análisis de dispositivos móviles:}

\begin{itemize}
    \item Cellebrite UFED Touch 2, Physical Analyzer.
    \item AccessData Mobile Phone Examiner Plus (MPE+).
\end{itemize}

\noindent \textbf{Herramientas para el análisis de redes:}

\begin{itemize}
    \item E-Detective - Decision Computer Group.
    \item SilentRunner - AccessData.
    \item NetworkMiner.
    \item Nerviness Investigator.
\end{itemize}

\noindent \textbf{Herramientas para filtrar y monitorear el tráfico de una red tanto interna como a internet:}

\begin{itemize}
    \item Tcpdump.
    \item USBDeview.
    \item SilentRunner - AccessData.
    \item WireShark.
\end{itemize}

\noindent \textbf{Términos importantes:}

\begin{itemize}
    \item \emph{Cadena de custodia:} la identidad de personas que manejan la evidencia en el tiempo del suceso y la última revisión del caso. Es la responsabilidad de la persona que maneja la evidencia asegurar que los artículos son registrados y contabilizados durante el tiempo en el cual están en su poder, y que son protegidos, así mismo llevando un registro de los nombres de las personas que manejaron la evidencia o artículos durante el lapso de tiempo y fechas de entrega y recepción.
    \item \emph{Imagen forense:} técnica llamada también "espejeo" (en inglés "Mirroring"), la cual es una copia binaria de un medio electrónico de almacenamiento. En la imagen quedan grabados los espacios que ocupan los archivos y las áreas borradas incluyendo particiones escondidas.
    \item \emph{Análisis de archivo:} examina cada archivo digital descubierto y crea una base de datos de información relacionada al archivo (metadatos, etc.), consistente entre otras cosas en la firma del archivo o hash (indica la integridad del archivo).
\end{itemize}

{\color{red}\textbf{DEUDA TÉCNICA: plantear posible reducción del estado del arte}}
{\color{red}\textbf{DEUDA TÉCNICA: Referencia a WIKIPEDIA}}