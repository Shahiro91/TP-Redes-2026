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

3. **¿Qué es una SAN?**
   **¿Qué es una red de área de almacenamiento (SAN - Storage Area Network)?**
Una red de área de almacenamiento (SAN) es una red dedicada que se adapta a un entorno específico, que combina servidores, sistemas de almacenamiento, conmutadores de red, software y servicios.

**¿Por qué son importantes las redes SAN?**
Es posible que la memoria de la computadora y los recursos de almacenamiento local no proporcionen suficiente capacidad de almacenamiento, protección de almacenamiento, acceso de múltiples usuarios o velocidad y rendimiento para las aplicaciones empresariales. Por lo tanto, la mayoría de las organizaciones emplean algún tipo de SAN además del almacenamiento adjunto de red (NAS) para mejorar la eficiencia y la gestión de datos.

**¿Cuáles son las ventajas de una red SAN?**
La SAN libera el dispositivo de almacenamiento para que no esté en un bus de servidor en concreto. Conecta el almacenamiento directamente a la red, externalizando y distribuyendo funcionalmente el almacenamiento en toda la organización.

- Disponibilidad mejorada de las aplicaciones
El almacenamiento existe independientemente de las aplicaciones y es accesible a través de múltiples rutas para mayor confiabilidad, disponibilidad y capacidad de servicio.

- Mejor rendimiento de las aplicaciones
Las SAN descargan y mueven el procesamiento de almacenamiento de servidores a redes separadas.

- Centralizado y consolidado
Las SAN permiten una gestión más sencilla, escalabilidad, flexibilidad y alta disponibilidad.

- Transferencia y almacenamiento de datos de sitios remotos
Las SAN protegen los datos contra desastres y ataques maliciosos con una copia remota.

- Gestión centralizada sencilla
Las SAN simplifican la gestión creando imágenes únicas de los medios de almacenamiento.

**¿Cómo funciona una SAN?**
A veces llamada la red detrás de los servidores, una SAN incluye una infraestructura de comunicación que proporciona conexiones físicas y permite que un dispositivo cualquiera se conecte a través de la red mediante elementos interconectados, como conmutadores y ordenadores.

**Las redes SAN actuales crean nuevos métodos para conectar almacenamiento a servidores, lo que permite una alta disponibilidad y mejoras de rendimiento.** Conectan matrices de almacenamiento compartido y bibliotecas de cintas a múltiples servidores utilizados por servidores en clúster para conmutación por error. Y pueden evitar los cuellos de botella tradicionales del tráfico de red, facilitando transferencias de datos directas y de alta velocidad entre servidores y dispositivos de almacenamiento de tres maneras:



- De servidor a almacenamiento
La ventaja de este modelo de interacción tradicional es que varios servidores pueden acceder al mismo dispositivo de almacenamiento en serie o simultáneamente.

- De servidor a servidor
Los servidores pueden usar un SAN para facilitar comunicaciones de alta velocidad, baja latencia y alto volumen.

- De almacenamiento a almacenamiento
La capacidad de mover datos sin la intervención del servidor libera ciclos de procesador del servidor para otras actividades, como el procesamiento de aplicaciones. Los ejemplos incluyen un dispositivo de unidad de disco que realiza copias de seguridad de sus datos en un dispositivo de cinta sin intervención del servidor o un dispositivo remoto que se refleja en la SAN.

**Componentes de una SAN**
Los componentes principales de una SAN son servidores, almacenamiento e infraestructura de red.

- Servidores
La infraestructura de servidor es la razón subyacente de todas las soluciones SAN y esta infraestructura incluye una combinación de plataformas de servidor. Con iniciativas como la consolidación de servidores y el comercio por Internet, aumenta la necesidad de SAN, lo que hace que la importancia del almacenamiento en red sea mayor.

- Almacenamiento
Un sistema de almacenamiento puede constar de sistemas de disco y sistemas de cinta. El sistema de disco puede incluir HDD, SSD o unidades flash. El sistema de cinta puede estar compuesto por unidades de cinta, cargadores automáticos de cintas y bibliotecas de cintas.

- Infraestructura de red
La conectividad SAN consta de componentes de hardware y software que interconectan dispositivos de almacenamiento y servidores, incluido Fibre Channel. El hardware puede incluir concentradores, conmutadores, puertas de enlace, directores y enrutadores. El software incluye software de gestión SAN.

4. **Diferencias entre un Hub, Repetidor, Router y SWITCH. Explicar las diferencias.**
   Los hubs, routers y switches son los dispositivos de red más comunes utilizados en la construcción de redes, pero tienen diferencias en cuanto a funciones, escenarios de aplicación y gestión y configuración.

**¿Qué es un Hub?**
Un hub es un dispositivo de red que opera en la capa física del modelo OSI, diseñado para interconectar múltiples dispositivos dentro de una red local (LAN). Como punto de conexión central de una red, el hub se encarga de enviar paquetes entre dispositivos, pero no puede detectar la dirección de destino, solo puede copiarlos y transmitirlos a todos los dispositivos conectados.

Los hubs funcionan en modo semidúplex, lo que significa que todos los dispositivos conectados comparten un dominio de colisión, lo que puede provocar posibles colisiones de datos y afectar el rendimiento de la red. Por eso, los hubs suelen ser más adecuados para redes pequeñas como las domésticas o las de pequeñas oficinas.

**¿Qué es un Router?**
Un router es un dispositivo de red crucial que opera en la capa de red del modelo OSI y se encarga de enrutar paquetes de datos entre diferentes redes. Su función principal es determinar la mejor ruta para los datos a través de la red mediante tablas de enrutamiento y protocolos como el IP (Internet Protocol). Además de conectar dispositivos dentro de una red local (LAN), los routers también facilitan la conexión a redes externas como Internet.

**Router vs. Hub**
En comparación con el hub, el router es más complejo y tiene funcionalidades más avanzadas. Sus principales ventajas incluyen:

- **Enrutamiento de paquetes:** El router puede dirigir eficientemente los paquetes de datos entre diferentes redes utilizando direcciones IP, optimizando así la transmisión de datos.
- **Segmentación de redes:** Permite dividir la red en subredes más pequeñas (subnetting), lo cual mejora la organización y la gestión del tráfico.
- **Mayor seguridad:** Proporciona funciones de firewall y filtros de paquetes para proteger la red contra accesos no autorizados y ataques externos.
Gestión del ancho de banda: Permite controlar y priorizar el tráfico de datos, garantizando un uso eficiente del ancho de banda disponible.

En resumen, el router no solo facilita la conectividad entre diferentes redes, sino que también proporciona seguridad avanzada, gestión de tráfico optimizada y funciones adicionales que son esenciales para redes modernas y complejas.

**¿Qué es un Switch?**
Un switch es un dispositivo de red utilizado para conectar varios dispositivos dentro de una red de área local (LAN). Funciona en la capa de enlace de datos (Capa 2) del modelo OSI y utiliza direcciones MAC para reenviar tramas de datos al dispositivo de destino apropiado.

Los switches están diseñados para gestionar de forma eficiente e inteligente el tráfico de red creando una vía de comunicación dedicada entre los dispositivos emisor y receptor, optimizando así la transferencia de datos dentro de la red. Se utilizan habitualmente en hogares, empresas y centros de datos para conectar ordenadores, impresoras, servidores y otros dispositivos en red, facilitando una comunicación fluida y el uso compartido de recursos.

**Switch vs. Hub**
La diferencia principal entre un switch y un hub reside en cómo manejan y transmiten los datos dentro de una red. Un switch opera en la capa de enlace de datos del modelo OSI y utiliza direcciones MAC para enviar datos directamente al dispositivo de destino, lo cual optimiza el rendimiento y reduce colisiones en la red. En contraste, un hub opera en la capa física del modelo OSI y transmite datos a todos los dispositivos conectados indiscriminadamente, lo que puede causar congestión y disminuir la eficiencia de la red al generar colisiones de datos.

En resumen, un switch es más eficiente y adecuado para redes modernas que requieren mayor velocidad y gestión del tráfico, mientras que un hub es más básico y se utiliza en configuraciones simples donde no se necesita un rendimiento avanzado.

**Switch vs. Router**
La diferencia principal entre un switch y un router radica en sus funciones y cómo manejan el tráfico dentro de una red.

Un switch opera en la capa de enlace de datos del modelo OSI y se utiliza para conectar dispositivos dentro de una misma red local (LAN), optimizando la transferencia de datos al enviar los paquetes únicamente al dispositivo de destino, lo cual mejora la eficiencia y velocidad de la red local.

En cambio, un router opera en la capa de red del modelo OSI y se encarga de enrutar paquetes de datos entre redes diferentes, utilizando direcciones IP para determinar la mejor ruta de entrega, lo cual es esencial para conectar redes locales entre sí o a internet, gestionando y filtrando el tráfico para asegurar que los datos lleguen al destino correcto de manera segura.

Necesitas un router cuando quieres conectar dos o más redes. Un switch sólo puede conectar dispositivos dentro de una misma red, mientras que un router puede dirigir datos entre redes. Si tienes varias redes, por ejemplo una doméstica y otra de oficina, necesitarás un router para conectarlas.

**Repetidor (Repeater)**
Es un dispositivo electrónico que conecta dos segmentos de una misma red, transfiriendo el tráfico de uno a otro extremo, bien por cable o inalámbrico.
El Repetidor amplifica la señal de la red LAN inalámbrica desde el router al ordenador. Un Receptor, por tanto, actúa sólo en el nivel físico o capa 1 del modelo OSI.

**Diferencias principales entre Repetidor y Hub**
- Número de puertos: El repetidor tradicional tiene solo dos puertos (sirve para conectar y extender dos tramos de cable o zonas de red). El hub tiene múltiples puertos (permite conectar muchos equipos a la vez).
- Alcance vs. Conectividad: El objetivo principal del repetidor es extender la distancia física de una señal de red. El objetivo principal del hub es centralizar y conectar varios equipos en una estrella lógica de red. 
- Relación técnica: Todo hub es, en la práctica, un repetidor de múltiples entradas y salidas, pero un repetidor clásico no actúa como un centro de conexión múltiple de computadoras. 

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







