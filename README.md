# RANSOMWARE FUNDAMENTALS

Bienvenidos a la guía básica, para principiantes, sobre ransomware realizada por Ramon Peinado Ruiz gracias al Curso de Ransomware ofrecido por el CCN

## CONCEPTOS BASICOS E HISTORIA

Al contrario de lo que se suele creer, el primer *ransomware* no apareció con Internet. La historia de estos programas maliciosos comenzó a finales de la década de 1980, con el único propósito de bloquear el funcionamiento de puestos de trabajo. De este modo, afectaban a particulares y empresas con microordenadores. En 1989, el **«troyano AIDS» fue el primer ransomware de la historia de la informática**. En un contexto de preocupación por la aparición del virus del SIDA, el biólogo Joseph L. Popp envió 20 000 disquetes con información sobre la enfermedad a grupos de pacientes, instituciones médicas y particulares de 90 países. Pero, aunque el disquete contenía información sobre este tema, también contenía un virus que cifró los archivos de la máquina infectada después de un cierto número de reinicios. Para recibir el *software* descodificador, las víctimas tuvieron que pagar un rescate de 189 dólares.

La famila del ransomware ha sido la amenaza mas concurrente y dañina con una gran evolución en los ultimos años. 

En un contexto en el que la mayoria de las fuentes relacionadas con la seguridad informática prevén que este tipo de amenazas siga aumentando es importante saber como defenderse.

### VECTORES DE INFECCION

La mejor defensa es conocer el medio de entrada de la amenaza así como sus mecanismos de propagación. En algunos casos el codigo maligno puede mantenerse latente en el sistema durante una cantidad de tiempo y manifestarse tras una accion o acciones en una fecha lo que hace difícil identificar el origen.

Vectores mas tipicos:

<img src="/img/1ºimagenn.PNG"  />

1. *Realizados mediante enlaces web o ficheros maliciosos adjuntados.*
2. *Usan este protocolo para ganar acceso a la infraestructura y propagarse, utilizan herramientas para buscar equipos con el servicio expuesto y luego mediante ataques de fuerza bruta o de diccionario tratan de conseguir acceso al equipo.*
3. *Derivados de otros como troyanos que conceden control total al sistema para descargar mas malware o abrir backdoors para usarlas en futuro. Es muy común en programas destinados al pirateo de software comercial.*
4. *Se aprovechan de vulnerabilidades del navegador o de sus plugins para la ejecución de código malicioso. Se pueden activar con tan solo navegar a una pagina sin necesidad alguna de interactuar.(Conviene recurrir a complementos especificos para bloquear apertura de pop-ups, iframes, ejecución de código JavaScript y ads)*.
5. *Un ejemplo es el uso de exploits en los propios documentos ofimáticos que se ejecutan con simple apertura del mismo, sin necesidad de activar macros. Son muy peligrosos ya que la interaccion es nula y no muestran alerta ninguna*.

### BUENAS PRACTICAS

La primera buena practica para prevenir este tipo de ataques radica en la base, la concienciación formacion y entrenamiento del humano puede reducir en gran medida el riesgo. Ademas:

- Tener copias de respaldo: La extorsion del ransomware solo se da cuando el atacante consigue cifrar recursos que son únicos e irrecuperables. Si disponemos de una copia de seguridad nos respaldaremos.
- Mantener el sistema actualizado.
- Políticas BYOD(Bring Your Own Device): Es habitual que las empresas adopten la política de dejar usar sus dispositivos electrónicos como medio de trabajo, hay que definir unas reglas de seguridad estrictas ante estas politicas.
- Contraseñas seguras: Usar contraseñas robustas y no usar credenciales configuradas por defecto.
- Antivirus: Disponer de antivirus y una buena configuración del cortafuegos(Firewall).
- Antispam: Disponer de un sistema antispam a nivel de correo electronico y establecer un filtrado alto.
- Políticas de seguridad: Establecer politicas de seguridad para impedir ejecución de ficheros en directorios comunmente atacados por ransomware(AppData, LocalAppData...) Herramientas como AppLocker Cryptoprevent permiten realizar estas configuraciones.
- IDS/IPS: Ambos sistemas se encargan de vigilar el tráfico, y para ello examinan la red y los puertos, analizando paquetes de datos, para detectar patrones sospechosos.
- Cuentas: No usar cuentas con altos privilegios.
- Control de acceso: Mantener listas de control de acceso.
- Bloqueadores: Recomendable el uso de bloqueadores de JavaScript.
- Extensiones de ficheros: Activar la visualización de las extensiones de los ficheros para evitar la ejecución de código malicioso.
- Anti-ransom: Herramienta que tratara de bloquear el proceso de cifrado o encontrar la clave de cifrado empleada.
- Maquinas Virtuales: La acción del ransomware no llega a materializarse en maquinas virtuales.

### ASPECTOS A TENER EN CUENTA

- **Tiempo**: Algunas variedades usan el tiempo transcurrido después de la infección como un factor de presión para forzar el pago del rescate. Este tiempo también es crucial para la actuación.
- **Eliminación de codigo dañino**: El objetivo principal no es conseguir persistencia en el equipo por lo que la eliminación suele ser sencilla y se encuentran varias herramientas para la desinfección
- **Recuperación de Ficheros**: Una vez identificado el ransomware que ha infectado el equipo se pueden consultar sitios donde se indica si es posible el descifrado y la recuperación de archivos. Estas herramientas existen gracias a organizaciones como Karpersky McAfee Panda Security, Sophos, compañías antimalware... que liberan las claves maestras de forma publica y altruista.
- **El pago no asegura la recuperacion de los ficheros**: Se han detectado paginas fraudulentas donde se realizan normalmente los pagos, pagar incentiva el uso de ransomware y no asegura la recuperación.

### PROCEDIMIENTO EMPLEADO POR EL CCN-CERT

#### DETERMINACION DEL ALCANCE DEL INCIDENTE:

1. Información de contexto del incidente: 
   - ¿Cuando se produjo la infeccion?
   - ¿Como se produjo la infeccion?
   - ¿Cuantos equipos afectados hay?
   - ¿Se dispone de copia de seguridad de los datos?
   - ¿Se ha realizado alguna acción de mitigación?
2. Información técnica sobre la infección:
   - Nota de rescate del ransomware.
   - Muestra de ficheros cifrados (no mas de 2megas).
   - Muestra del ransomware, del correo de phishing, fichero ofimático o evidencia que permita analizar el codigo.
3. Información de la red en la que se ha producido la infeccion
   - Diagrama de red, con todos los componentes e interacciones entre ellos, routers firewalls servidores...
   - Direccionamiento publico, IP y dominios expuestos.

#### LINEAS DE ACTUACION EN LA GESTION DE INCIDENTES:

1. Contención de la amenaza:
   - *Desconexión de los equipos de la red.*
   - *Segmentación de la red.*
   - *Despliegue de solución EDR y vacuna CCN-CERT. (El CCN-CERT mediante su herramienta MicroClaudia distribuye vacunas específicas para cada caso de ransomware. Mediante MicroClaudia se generan actuaciones que permiten el bloqueo inmediato de cualquier malware relacionado con Emotet, Trickbot, Bitpaymer, Ryuk y Sodinokibi entre otros, de forma que se pueda detener la ejecución de los mismos)*
   - *Despliegue de MicroClaudia para distribuir vacunas.*
   - *Ampliar nivel de vigilancia en antispam.*
   - *Intensificar en análisis del contenido de las comunicaciones.*
2. Detección de la amenaza:
   - *Instalación de sonda del CCN-CERT (SAT). [El CCN-CERT dispone de una sonda, Sistema de Alerta Temprana, que realiza las funciones de IDS (Intrusion Detection System) y que puede ser desplegada en un punto de interconexión de la red donde se tenga visibilidad de todo el tráfico entrante y saliente].*
   - *Caracterización del código dañino. [El CCN-CERT dispone de informes de código dañino (ID) en su portal (https://ccn-cert.cni.es) relacionados con distintas familias de ransomware. En estos informes se recopila toda la caracterización de la amenaza, incluyendo características, funcionalidad, conectividades, persistencia e indicadores que permitan la detección. Existen diversas páginas que pueden ayudar a identificar la familia de ransomware implicada en el incidente. Partiendo de un fichero de muestra, las más efectivas y recomendables son:  nomoreransom.org Enlace: https://www.nomoreransom.or/crypto-sheriff.php IDRansomware Enlace: https://id-ransomware.malwarehunterteam.com].*
   - *Revisión de las reglas de antispam.*
   - *Revisión del filtrado de ficheros comprimidos ejecutables y ficheros ofimaticos con o sin macros*
3. Mitigación de la amenaza:
   - *Rediseñar red y segmentando entornos*
   - *Actualizacion y parcheo de los equipos*
   - *Cambio de credenciales en todo el dominio*
   - *Actualización de reglas en antispam y firewalls*
4. Recuperación de la información y servicios:
   - *Valoración de escenarios.*
   - *Inventario de los activos cifrados o eliminados.*
   - *Reconstrucción y recuperación de los servicios críticos. Mediante herramientas o restauracion del sistema*
5. Prevención:
   - *Establecer políticas de seguridad en el dominio.(Deshabilitar ejecucion de PowerShell asi como Macros en documentos ofimaticos)*
   - *Establecer políticas de seguridad a nivel red.(Registrar actividad del Firewall Proxy DNS...)*
   - *Realizar copias de seguridad.*
   - *Aumentar el análisis de contenido de las comunicaciones.*

A continuación se listan algunas de las herramientas y utilidades online existentes, que permiten el descifrado de ciertos especímenes de ransomware ordenadas por familia:

<img src="/img/3ºimagenn.PNG"  />

Además de estos enlaces, se puede consultar: 

- *Solución de Trendmicro, para combatir un amplio abanico de variedades de ransomware (incluyendo algunas no tan conocidas). Enlace: https://success.trendmicro.com/dcx/s/solution/1114221-downloading-and-using-the-trend-micro-ransomware-file-decryptor?language=en_US*
- *Una herramienta de parte de Emsisoft, que combate la infección de diversas familias de Ransomware, también menos conocidas y algunas no incluidas en las herramientas anteriores listadas. Enlace: https://decrypter.emsisoft.com/* 
- *En caso de que la variante que ha infectado el equipo no se encontrara listada en ninguna de las herramientas anteriores, se puede probar suerte con el buscador que ofrece Barkly. Enlace: https://www.barkly.com/ransomware-recovery-decryptiontools-search*



#### MICROCLAUDIA

<img src="/img/2ºimagenn.PNG"  />

