# RANSOMWARE FUNDAMENTALS

Bienvenidos a la guía básica, para principiantes, sobre ransomware realizada por Ramon Peinado Ruiz gracias al Curso de Ransomware ofrecido por el CCN

## CONCEPTOS BASICOS E HISTORIA

Al contrario de lo que se suele creer, el primer *ransomware* no apareció con Internet. La (triste) historia de estos programas maliciosos comenzó a finales de la década de 1980, con el único propósito de bloquear el funcionamiento de puestos de trabajo. De este modo, afectaban a particulares y empresas con microordenadores. En 1989, el **«troyano AIDS» fue el primer ransomware de la historia de la informática**. En un contexto de preocupación por la aparición del virus del SIDA, el biólogo Joseph L. Popp envió 20 000 disquetes con información sobre la enfermedad a grupos de pacientes, instituciones médicas y particulares de 90 países. Pero, aunque el disquete contenía información sobre este tema, también contenía un virus que cifró los archivos de la máquina infectada después de un cierto número de reinicios. Para recibir el *software* descodificador, las víctimas tuvieron que pagar un rescate de 189 dólares.

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
- Politicas BYOD(Bring Your Own Device): Es habitual que las empresas adopten la política de dejar usar sus dispositivos electrónicos como medio de trabajo, hay que definir unas reglas de seguridad estrictas ante estas politicas.
- Contraseñas seguras: Usar contraseñas robustas y no usar credenciales configuradas por defecto.
- Antivirus: Disponer de antivirus y una buena configuración del cortafuegos(Firewall).
- Antispam: Disponer de un sistema antispam a nivel de correo electronico y establecer un filtrado alto.
- Politicas de seguridad: Establecer politicas de seguridad para impedir ejecución de ficheros en directorios comunmente atacados por ransomware(AppData, LocalAppData...) Herramientas como AppLocker Cryptoprevent permiten realizar estas configuraciones.
- IDS/IPS: Ambos sistemas se encargan de vigilar el tráfico, y para ello examinan la red y los puertos, analizando paquetes de datos, para detectar patrones sospechosos.
- Cuentas: No usar cuentas con altos privilegios.
- Control de acceso: Mantener listas de control de acceso.
- Bloqueadores: Recomendable el uso de bloqueadores de JavaScript.
- Extensiones de ficheros: Activar la visualización de las extensiones de los ficheros para evitar la ejecución de código malicioso.
- Anti-ransom: Herramienta que tratara de bloquear el proceso de cifrado o encontrar la clave de cifrado empleada.
- Maquinas Virtuales: La acción del ransomware no llega a materializarse en maquinas virtuales.