# TP-Redes-2026
Trabajo grupal ifts 18 - 2026 
# Integrantes 
## GRUPO D:
* Lezcano, Sergio.
* Roth Norberto Oscar
* Tassara Daniela
* Quintana, María Florencia

## Preguntas:

## 1. VLAN (Virtual Local Area Network)

Una **VLAN** o *LAN Virtual* permite crear redes lógicamente independientes sobre una misma infraestructura física. Requiere el uso de switches gestionables e idealmente routers compatibles para segmentar y administrar adecuadamente el tráfico.

### Ventajas principales
* **Seguridad:** Aísla el tráfico entre redes por defecto. Para permitir la comunicación entre diferentes VLANs, es necesario implementar un router o switch multicapa (Capas 3) mediante *inter-vlan routing*.
* **Segmentación y flexibilidad:** Permite agrupar equipos en distintas subredes fácilmente, asignando políticas específicas de comunicación y acceso a Internet.
* **Optimización de la red:** Contiene el tráfico de *broadcast* (difusión) en dominios más pequeños. Esto evita que las transmisiones masivas saturen la red global.
* **Reducción de costes:** Maximiza el rendimiento del ancho de banda y elimina la necesidad de adquirir hardware costoso adicional para dividir redes.
* **Gestión eficiente:** Facilita la administración a los equipos de TI al aplicar políticas unificadas a través de los switches, además de adaptar la red a requisitos geográficos o proyectos específicos.

### Desventajas
* **Complejidad de mantenimiento:** Requiere conocimientos avanzados tanto para su configuración como para su posterior administración.
* **Escalabilidad limitada:** Los switches tienen un límite máximo en la cantidad de VLANs que pueden soportar.
* **Carga en los equipos:** Gestionar múltiples VLANs en un mismo dispositivo puede ocasionar sobrecarga de procesamiento.
* **Riesgos de seguridad:** Una mala configuración puede hacer la red vulnerable a ataques como el *VLAN hopping*.
* **Incompatibilidad de hardware:** Todos los dispositivos de red deben admitir el estándar **802.1Q**, lo que puede exigir la renovación de equipos.

### Tipos de VLAN
* VLAN nativa
* Etiquetado VLAN 802.1Q
* VLAN basadas en puerto
* VLAN basadas en MAC
* VLAN etiquetadas
* VXLAN
* VLAN híbrida
* VLAN de gestión
* VLAN de control
* VLAN dedicada

---

## 2. VPN (Virtual Private Network)

Una **VPN** o *Red Privada Virtual* es una tecnología que establece una conexión a Internet segura y cifrada entre el dispositivo del usuario y una red privada o punto de conexión de confianza.

### Características fundamentales
* **Virtual:** No requiere cables o enlaces físicos dedicados.
* **Privada:** Oculta el tráfico y las actividades frente a terceros.
* **En red:** Conecta de forma coordinada múltiples dispositivos (como el cliente y el servidor VPN).

### Pilares tecnológicos
1. **Cifrado:** Transforma los datos en un formato ilegible (texto cifrado) mediante algoritmos criptográficos para proteger credenciales y datos confidenciales.
2. **Tunelización:** Encapsula los paquetes de datos cifrados para que viajen de forma aislada a través de redes públicas no seguras.
3. **Autenticación:** Valida que solo usuarios y dispositivos autorizados puedan conectarse al túnel y acceder a los recursos internos.

### Ventajas principales
* **Privacidad y anonimato:** Enmascara la dirección IP del usuario y evita el rastreo o la interceptación en redes públicas.
* **Acceso remoto seguro:** Permite a empleados, desarrolladores y estudiantes conectarse a sistemas corporativos o educativos desde cualquier lugar.
* **Integración con la nube:** Une de forma segura infraestructuras locales con plataformas en la nube (como Azure) mediante gateways dedicados.
* **Cumplimiento normativo:** Ayuda a cumplir los estándares de seguridad de protección de datos en tránsito.

### Casos de uso comunes
* **Trabajo remoto e híbrido:** Conexión segura a datos y aplicaciones internas sin exporlos a Internet.
* **Conectividad sitio a sitio:** Enlace entre sucursales u oficinas sin depender de líneas privadas dedicadas de alto costo.
* **Entornos multinube e híbridos:** Interconexión de recursos locales con múltiples proveedores de nube.
* **Entornos de desarrollo:** Acceso privado y cifrado a APIs, entornos de pruebas y servicios en la nube.
* **Ámbito educativo:** Acceso remoto de estudiantes a bases de datos, bibliotecas digitales y plataformas académicas.

## 3. SAN (Storage Area Network)

Una **SAN** es una red dedicada y de alta velocidad que conecta servidores con sistemas de almacenamiento compartido (matrices de discos, unidades SSD/HDD o bibliotecas de cintas) mediante hardware y software especializado (como *Fibre Channel*).

### Importancia
A diferencia del almacenamiento adjunto tradicional, permite superar los límites de capacidad local, optimizar la protección de datos, gestionar el acceso multiusuario de gran escala y ofrecer alto rendimiento para aplicaciones empresariales junto a esquemas NAS.

### Ventajas principales
* **Disponibilidad mejorada:** El almacenamiento es independiente de las aplicaciones y accesible a través de múltiples rutas de conexión.
* **Rendimiento optimizado:** Descarga el procesamiento de almacenamiento de los servidores de aplicaciones hacia una red independiente.
* **Gestión centralizada y consolidada:** Simplifica la administración al unificar los medios de almacenamiento, permitiendo mayor escalabilidad y flexibilidad.
* **Recuperación ante desastres:** Facilita la creación de copias remotas de datos para protección contra ataques o fallos graves.

### Formas de interacción en la SAN
* **Servidor a Almacenamiento:** Acceso directo y simultáneo de múltiples servidores a los mismos recursos de almacenamiento.
* **Servidor a Servidor:** Comunicación directa de alta velocidad y baja latencia entre servidores.
* **Almacenamiento a Almacenamiento:** Mapeo, migración y respaldo de datos directamente entre dispositivos de almacenamiento sin saturar la CPU del servidor.

### Componentes principales
* **Servidores:** Plataformas que ejecutan las aplicaciones corporativas.
* **Sistemas de almacenamiento:** Discos (HDD/SSD/Flash) y bibliotecas de cintas.
* **Infraestructura de red:** Componentes de interconexión físicos (conmutadores, directores, enrutadores, Fibre Channel) y software de gestión centralizada.

---

## 4. Comparativa de Dispositivos de Red

### 1. Repetidor (Repeater)
* **Capa OSI:** Capa 1 (Física).
* **Función:** Captura y regenera/amplifica la señal (cableada o inalámbrica) para extender el alcance físico del segmento de red.
* **Características:** Cuenta generalmente con solo dos puertos. No inspecciona ni filtra el tráfico.

### 2. Hub (Concentrador)
* **Capa OSI:** Capa 1 (Física).
* **Función:** Actúa como punto de conexión central multiport para múltiples dispositivos dentro de una LAN.
* **Características:**
  * Reenvía los paquetes entrantes a todos sus puertos indiscriminadamente (difusión general).
  * Trabaja en modo *semidúplex*, compartiendo un único dominio de colisión entre todos los puertos, lo que puede provocar congestión.
  * Funciona internamente como un repetidor multipuerto básico.

### 3. Switch (Conmutador)
* **Capa OSI:** Capa 2 (Enlace de datos).
* **Función:** Conecta múltiples dispositivos en una red local (LAN) de forma inteligente.
* **Características:**
  * Utiliza **direcciones MAC** para enviar datos únicamente al dispositivo de destino específico.
  * Crea canales dedicados para cada conexión, eliminando los dominios de colisión y optimizando el rendimiento del tráfico interno.

### 4. Router (Enrutador)
* **Capa OSI:** Capa 3 (Red).
* **Función:** Interconecta diferentes redes independientes entre sí (por ejemplo, una LAN corporativa con Internet).
* **Características:**
  * Utiliza **direcciones IP** y tablas de enrutamiento para determinar la trayectoria óptima de los datos.
  * Permite la segmentación en subredes (*subnetting*), gestión de ancho de banda y priorización de tráfico.
  * Incorpora funciones avanzadas de seguridad como firewalls e inspección de tráfico.

---

### Resumen comparativo de dispositivos

| Dispositivo | Capa OSI | Identificación utilizada | Ámbito de trabajo | Manejo del tráfico |
| :--- | :--- | :--- | :--- | :--- |
| **Repetidor** | Capa 1 (Física) | Ninguna | Extensión de tramo | Regenera y amplifica la señal |
| **Hub** | Capa 1 (Física) | Ninguna | Red Local (LAN) | Difusión a todos los puertos (*Broadcast*) |
| **Switch** | Capa 2 (Enlace) | Dirección MAC | Red Local (LAN) | Reenvío directo al destino específico |
| **Router** | Capa 3 (Red) | Dirección IP | Entre redes distintas (LAN/WAN) | Enrutamiento estratégico de paquetes |

5. **¿Qué es un protocolo de comunicaciones?**
   Un protocolo de comunicación es un conjunto de normas, pautas o instrucciones que sirven para guiar las acciones durante el intercambio de información.
Tipos de protocolos de comunicación
Existen diferentes tipos de protocolos de comunicación que se ajustan a las necesidades de cada usuario:

  **1.  Protocolos punto a punto**
Son aquellos protocolos más antiguos y tradicionales, y sirven para traspasar información entre dos computadoras.

Este protocolo se encarga de garantizar la comunicación entre dos usuarios y de controlar el envío y la recepción de los datos.

De esta manera, permite reenviar el mensaje original las veces que fueran necesarias hasta recibir un acuse de recibo.

  **2.  Comunicación entre redes**
Además de cumplir con las tareas del protocolo anterior, permite la comunicación de varios usuarios o servidores mediante una red local (LAN).

Para hacerlo de una forma organizada, le asigna un número para identificar cada uno de los terminales que se ven implicados en el intercambio de información o datos.

A su vez, cuenta con un ordenador central que se encarga de preguntar regularmente al resto de los usuarios por su funcionamiento.

  **3.  Protocolos de transmisión de paquetes**
Los paquetes son grupos de información que contienen datos que deben garantizar su llegada satisfactoria a destino.

A diferencia de los dos protocolos anteriores, en este caso la responsabilidad de la transmisión está a cargo de los paquetes y sus datos y no de los equipos u ordenadores.

Se les llama paquetes porque actúan de manera fragmentaria, como si fuese una carta o postal tradicional que pasa por diferentes manos y controles hasta llegar al destinatario.

  **4.  Protocolos TCP/IP**
Sus siglas significan “Transfer Control Protocol / Internet Protocol” y se trata de un protocolo de transmisión de paquetes. Es decir, que cuando una máquina necesita enviar datos a otros usuarios, los fragmenta en diferentes trozos para que estos transiten por separado.

Estos paquetes se dirigen de manera independiente y contienen la información con la Red a la cual debe llegar, su remitente y su correspondiente acuse de recibo.

Al existir múltiples redes posibles, los paquetes tienden a elegir el más apropiado para ese momento. De esta manera, se logra una transferencia estable y veloz.

6. **TCP/IP y NetBios. Diferencias**
   TCP/IP es un protocolo de enlace de datos que se usa en Internet para que los ordenadores y otros dispositivos envíen y reciban datos. TCP/IP son las siglas en inglés de Transmission Control Protocol/Internet Protocol (protocolo de control de transmisión/protocolo de Internet). Posibilita que los dispositivos conectados a Internet se comuniquen entre sí en varias redes.

**¿Qué hace TCP/IP?**
TCP/IP determina cómo los ordenadores transfieren datos de un dispositivo a otro. Estos datos deben ser exactos para que el receptor obtenga la misma información enviada por el emisor.

¿Qué es TCP/IP y cómo funciona? Para garantizar que cada comunicación llegue intacta al destino deseado, el modelo TCP/IP divide los datos en paquetes y luego los vuelve a juntar para formar el mensaje completo en el destino. Enviar los datos en paquetes pequeños hace que sea más fácil mantener la exactitud que enviando todos los datos a la vez.

Después de dividir un mensaje individual en paquetes, estos pueden recorrer diversos caminos en caso de congestión. 

**¿Cómo funciona el modelo TCP/IP?**
Cuando envía algo por Internet, ya sea un mensaje, una foto o un archivo, el modelo TCP/IP divide esos datos en paquetes según un procedimiento de cuatro capas. Los datos primero atraviesan estas capas en un sentido, y luego lo hacen en sentido contrario cuando los datos se vuelven a juntar en el destino.

El modelo TCP/IP funciona porque todo el proceso está estandarizado. Sin la estandarización, la comunicación podría volverse impredecible y ralentizar las operaciones, y un Internet rápido depende de la eficiencia. Como estándar global, el modelo TCP/IP es una de las maneras más eficientes de transferir datos por Internet.

**¿Cuáles son las capas del modelo TCP/IP?**
Hay cuatro capas en el modelo TCP/IP: acceso a la red, Internet, transporte y aplicación. Conjuntamente, estas capas son un conjunto de protocolos. El modelo TCP/IP pasa los datos por estas capas en un orden concreto cuando un usuario envía información y después en el orden inverso cuando se reciben los datos.

- **Capa 1: capa de acceso a la red**
La capa de acceso a la red, también conocida como la capa de enlace a los datos, gestiona la infraestructura física que permite a los ordenadores comunicarse entre sí por Internet. Esto abarca, entre otros elementos, cables Ethernet, redes inalámbricas, tarjetas de interfaz de red y controladores de dispositivos en el ordenador.

La capa de acceso a la red también incluye la infraestructura técnica, como el código que convierte datos digitales en señales transmisibles, que hacen posible una conexión.

- **Capa 2: Capa de Internet**
La capa de Internet, también llamada la capa de red, controla el flujo y el enrutamiento de tráfico para garantizar que los datos se envían de forma rápida y correcta. Esta capa también es responsable de volver a juntar el paquete de datos en el destino. Si hay mucho tráfico en Internet, esta capa puede tardar un poco más en enviar un archivo, pero es menos probable que el archivo se dañe.

- **Capa 3: Capa de transporte**
La capa de transporte es la que proporciona una conexión de datos fiable entre dos dispositivos de comunicación. Es como enviar un paquete asegurado: la capa de transporte divide los datos en paquetes, confirma los paquetes que ha recibido del remitente y se asegura de que el destinatario confirme los paquetes recibidos por su parte.

- **Capa 4: Capa de aplicaciones**
La capa de aplicaciones es el grupo de aplicaciones que permite al usuario acceder a la red. Para la mayoría de nosotros, esto significa el correo electrónico, las aplicaciones de mensajería y los programas de almacenamiento en la nube. Esto es lo que el usuario final ve y con lo que interactúa al recibir y enviar datos.

**Definición de NetBIOS (protocolo de red)**

Protocolo de red creado originalmente para redes locales de computadoras IBM PC.

NetBIOS (Network Basic Input/Output System) es un conjunto de protocolos de nivel de sesión que proporciona tres servicios principales en redes locales:

- Servicio de nombres: permite identificar dispositivos en la red mediante nombres simples y legibles, en lugar de direcciones numéricas.
- Servicio de datagramas o paquetes: facilita el envío de mensajes sin conexión entre dispositivos.
- Servicio de sesión: establece y gestiona conexiones orientadas a sesión para la transferencia fiable de datos.

**Resumen:** NetBIOS es un conjunto de protocolos utilizados en redes locales para identificar dispositivos, enviar mensajes y gestionar sesiones de comunicación. Permite compartir recursos como archivos e impresoras de manera sencilla. Aunque su uso ha disminuido, sigue presente en entornos con equipos antiguos.

**La diferencia principal es que NetBIOS es una interfaz de software para redes locales pequeñas, mientras que TCP/IP es un conjunto de protocolos globales diseñado para internet.**

7. **¿Cómo está formado un paquete de datos en TCP/IP? ¿Qué es un “flag” en un paquete de TCP/IP?**
   
Los paquetes TCP/IP
Cada paquete TCP/IP tiene una estructura básica compuesta por encabezados (headers).

El encabezado IP actúa como la columna vertebral, proporcionando las direcciones de origen y destino, así como información sobre cómo debe ser manejado el paquete en la red. Este encabezado es crucial para los routers, ya que les permite tomar decisiones basadas en la información contenida en él.

Dentro del encabezado IP, encontramos el encabezado TCP, que contiene detalles como los puertos de origen y destino, el número de secuencia y la suma de verificación hash. Esta última es esencial para verificar la integridad del paquete. Por ejemplo, los investigadores de seguridad vigilan estos encabezados en busca de anomalías que podrían indicar ataques como el escaneo de puertos o intentos de inyección de datos.

Consideramos que el encabezado es la columna vertebral, los datos y el payload representan el corazón de los paquetes TCP/IP. Aquí es donde se almacena la información valiosa que se transmite a través de la red. Los ciberdelincuentes a menudo intentan infiltrarse en estos datos para robar información confidencial o llevar a cabo ataques de denegación de servicio.

A continuación, podemos entender en detalle cada uno de los puntos más relevantes de las características de los paquetes TCP/IP.

**Encabezado TCP / IP:**

**Encabezado TCP:**
- Puerto de origen (16 bits): Identifica la aplicación de origen en el equipo emisor.

- Puerto de destino (16 bits): Identifica la aplicación de destino en el equipo receptor.

- Número de secuencia (32 bits): Indica el número de orden del segmento actual dentro del flujo de datos.

- Número de acuse de recibo (32 bits): Indica el número de secuencia del siguiente byte que el emisor espera recibir del receptor.

- Longitud de la cabecera (4 bits): Indica la longitud del encabezado TCP en palabras de 32 bits. El tamaño mínimo es de 5 palabras (20 bytes) y puede aumentar hasta 15 palabras (60 bytes) si se incluyen opciones adicionales.

- **Flags (8 bits): Conjunto de indicadores que controlan el comportamiento del protocolo TCP. Algunos de los flags más importantes son:**

 - URG: Indica que el segmento contiene datos urgentes que deben procesarse de inmediato.

 - ACK: Indica que el campo "Número de acuse de recibo" es válido.

 - PSH: Indica que el receptor debe enviar los datos al usuario tan pronto como los reciba.

 - RST: Indica que se debe reiniciar la conexión TCP.

 - SYN: Indica que se está iniciando una nueva conexión TCP.

 - FIN: Indica que se está finalizando la conexión TCP.

 - Ventana (16 bits): Indica la cantidad de datos que el receptor está dispuesto a recibir sin necesidad de enviar un acuse de recibo.

 - Suma de verificación (16 bits): Se utiliza para detectar errores en la transmisión del encabezado TCP.

**Encabezado IP:**

- Versión: Indica la versión del protocolo IP utilizado. Actualmente, la versión más utilizada es IPv4 (versión 4) y se está implementando gradualmente IPv6 (versión 6).

- Longitud de la cabecera: Especifica la longitud del encabezado en bytes. Esta información es importante para que los routers puedan leer correctamente el encabezado y procesar el paquete.

- Tipo de servicio: Define la prioridad y el tipo de tratamiento del paquete. Permite a los routers dar prioridad a ciertos tipos de paquetes, como los que contienen datos sensibles o urgentes.

- Identificación: Permite la fragmentación y reensamblaje de paquetes grandes. Cuando un paquete es demasiado grande para ser transmitido por una red, se puede fragmentar en varios paquetes más pequeños. El campo de identificación permite reensamblar estos fragmentos en el destino.

- Banderas: Controlan diferentes aspectos del procesamiento del paquete. Por ejemplo, una bandera puede indicar si el paquete debe ser fragmentado o si se requiere un acuse de recibo.

- Tiempo de vida: Limita el tiempo que un paquete puede permanecer en la red. Esto evita que los paquetes circulen indefinidamente en caso de errores en el enrutamiento.

- Protocolo: Identifica el protocolo de la capa de transporte utilizado (TCP o UDP). Esta información permite al dispositivo receptor saber cómo interpretar los datos del payload.

- Suma de comprobación: Garantiza la integridad del encabezado. Si la suma de comprobación no es válida, el paquete se descarta.

- Dirección IP de origen: Indica la dirección del dispositivo que envía el paquete.

- Dirección IP de destino: Indica la dirección del dispositivo que recibe el paquete.
  

8. **Defina la red según su geografía. Explicar distintas variantes.**
   Las redes informáticas se clasifican principalmente en función de la extensión del área física que cubren y los medios de transmisión empleados para interconectar sus nodos:

**Red LAN (Local Area Network)**
La Red de Área Local (LAN) conecta dispositivos en un espacio geográfico limitado y controlado, como una vivienda, una oficina corporativa o un edificio de servidores. Suelen utilizar tecnologías cableadas como Ethernet o estándares inalámbricos de alta fidelidad para facilitar la comunicación a alta velocidad y con baja latencia entre dispositivos cercanos.

En una configuración típica de oficina, los terminales e impresoras se interconectan mediante un conmutador (switch) o un enrutador central (router). Cada dispositivo dispone de una dirección física MAC y una dirección lógica IP única, empleadas para identificar el flujo de paquetes dentro del segmento local. Este entorno resulta idóneo para compartir recursos de forma rápida, implementando medidas de ciberseguridad perimetral como firewalls locales, aislamiento de subredes y políticas de acceso restrictivas.

**Red WAN (Wide Area Network)**
La Red de Área Amplia (WAN) abarca extensiones geográficas masivas, interconectando ciudades, provincias o países enteros. Las WAN enlazan múltiples subredes dispersas combinando tecnologías de transporte públicas y dedicadas, tales como tendidos de fibra óptica transoceánica, enlaces de radio microondas y conexiones satelitales. El ejemplo más representativo y masivo de una red de tipo WAN es la propia red global Internet.

**Red WLAN (Wireless Local Area Network)**
La Red de Área Local Inalámbrica (WLAN) consiste en una variación elástica de la red LAN tradicional que prescinde de los cables físicos para realizar la conexión. Emplea ondas de radio mediante el estándar Wi-Fi y resulta indispensable en entornos donde realizar un cableado estructurado no es viable o práctico, como cafeterías, aeropuertos, almacenes y oficinas dinámicas. Sus ventajas estratégicas incluyen:

- Movilidad completa: Los terminales se desplazan libremente por la zona de cobertura sin interrumpir la persistencia de las sesiones de datos.
- Agilidad de despliegue: La puesta en marcha de los puntos de acceso (APs) inalámbricos reduce los tiempos y costes de instalación física en obra.
- Escalabilidad elástica: Admite la incorporación fluida de nuevos usuarios e instancias sin necesidad de alterar la infraestructura de puertos físicos.
- Versatilidad en el acceso remoto: Facilita la salida segura hacia internet o redes corporativas privadas mediante la integración de pasarelas de autenticación.

Su despliegue exige una monitorización constante para gestionar las interferencias de señal, proteger el perímetro radioeléctrico contra intrusiones no autorizadas y optimizar el ancho de banda para mitigar cuellos de botella.

**Red MAN (Metropolitan Area Network)**
La Red de Área Metropolitana (MAN) posee un alcance geográfico intermedio: cubre áreas metropolitanas densas, como un campus universitario distribuido o un término municipal completo. Conectan de forma eficiente múltiples redes LAN locales entre sí y son utilizadas habitualmente por administraciones públicas o proveedores de telecomunicaciones para desplegar redes de servicios unificados en grandes núcleos urbanos.

**Red VPN (Virtual Private Network)**
Una Red Privada Virtual (VPN) es una arquitectura lógica de red que construye una capa de comunicación cifrada y privada utilizando como canal una infraestructura de transporte pública, como internet. Es la solución estándar del mercado para permitir el teletrabajo seguro, garantizando que el personal acceda a los recursos del servidor corporativo desde ubicaciones remotas de manera hermética. Sus pilares de protección se basan en:

- Cifrado de datos de extremo a extremo: Aplica algoritmos criptográficos robustos para codificar la información en origen, asegurando que si los paquetes son interceptados en tránsito resulten indescifrables para terceros.
- Túnel de comunicación seguro (Tunneling): Encapsula el tráfico legítimo de la red aislándolo por completo del resto del tráfico público de internet, blindándolo contra ataques de manipulación o inyección de datos.
- Autenticación y autorización estricta: Valida minuciosamente las credenciales e identidad de los dispositivos antes de habilitar el acceso al perímetro privado del negocio.
- Privacidad de navegación: Oculta la dirección IP real del cliente y enmascara su localización geográfica, mitigando el rastreo de actividad por parte de operadores externos.

**Red PAN (Personal Area Network)**
La Red de Área Personal (PAN) es un entorno de conectividad de cortísimo alcance (típicamente pocos metros) enfocado en vincular los dispositivos de uso individual de un mismo usuario, tales como teléfonos inteligentes, portátiles, periféricos inalámbricos y sensores biométricos mediante protocolos eficientes de baja potencia como Bluetooth, Zigbee o conexiones físicas de interfaz USB.

**Red GAN (Global Area Network)**
La Red de Área Global (GAN) representa el peldaño definitivo en la escala de conectividad. Es una infraestructura global interconectada que da soporte a las comunicaciones móviles transcontinentales, unificando redes WAN mediante infraestructuras globales de satélite y redes de telecomunicaciones internacionales.

**33. Experiencia en Redes:**
### Sergio Lezcano: 

No tengo experiencia. 

### Norberto Oscar Roth:

Mi experiencia con redes es principalmente práctica, adquirida a lo largo de los años por la necesidad de conectar equipos y resolver problemas de conectividad. Algunos ejemplos:

- En PC antiguas, cuando las placas de red no venían integradas, tuve que averiguar qué placa necesitaba, conseguirla e instalarla. Como vivía en City Bell (La Plata), a veces tenía que buscar componentes específicos en lugares como Galería Jardín o en ferreterias cercanas para evitar viajar.

- Aprendí de manera práctica sobre cables de red, coaxiales, fichas y conectores, consultando también a amigos que se dedicaban a reparación de PC. Según el caso, compraba los componentes necesarios o directamente cables ya armados.

- Realicé configuraciones básicas de routers y redes hogareñas con distintos proveedores, como Fibertel y Telefónica, además de conectar equipos mediante Ethernet y Wi-Fi.

- Trabajé en un "Ciber" con varias PC conectadas en red para juegos. Participaba en la conexión de los equipos y utilizábamos un software centralizado para administrar las PC y controlar el tiempo de uso de cada usuario.

- En el Ministerio de Agricultura, Ganadería y Pesca trabajé dentro de una red privada del Estado Nacional. Para desarrollar y publicar proyectos debía configurar las conexiones necesarias para acceder a los distintos ambientes (desarrollo/test y producción) y ejecutar las aplicaciones en servidores propios del Ministerio.
En ese mismo trabajo, cuando trabajaba de forma remota una vez por semana, accedía a la red privada mediante FortiClient. También, cuando la conexión Wi-Fi de la oficina era muy lenta, utilizaba un adaptador USB-Ethernet (RJ45) para conectar la notebook directamente a la red cableada.

- Actualmente utilizo y configuro principalmente redes Wi-Fi y conexiones Bluetooth entre notebooks, celulares, auriculares, smartwatch, Smart TV, Apple TV y decodificadores de Flow.
Para ampliar la cobertura Wi-Fi de mi casa sin realizar cableado, utilizo un extensor de rango TP-Link TL-WA850RE como repetidor de señal.
También utilizo aplicaciones del celular como controles remotos para distintos dispositivos y realizo casting de contenido hacia Smart TV. Además tengo experiencia vinculando dispositivos como AirTag y otros equipos inteligentes mediante Bluetooth o Wi-Fi.







