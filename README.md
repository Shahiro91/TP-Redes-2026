# TP-Redes-2026
Trabajo grupal ifts 18 - 2026 
# Integrantes 
## GRUPO D:
* Lezcano, Sergio.
* Roth Oscar
* Tassara Daniela
* Quintana, María Florencia

## Preguntas:
1. ¿Qué es una VLAN?
   Las VLAN o también conocidas como «Virtual LAN» nos permite crear redes lógicamente independientes dentro de la misma red física, haciendo uso de switches gestionables que soportan VLANs para segmentar adecuadamente la red. También es muy importante que los routers que utilicemos soportan VLAN, de lo contrario, no podremos gestionarlas todas ni permitir o denegar la comunicación entre ellas. 

Las principales ventajas de las VLANs son:

- **Seguridad**. Las VLAN nos permite crear redes lógicamente independientes, por tanto, podemos aislarlas para que solamente tengan conexión a Internet, y denegar el tráfico de una VLAN a otra. Por defecto no se permite a las VLANs intercambiar tráfico con otra VLAN, es totalmente necesario ascender a nivel de red (L3) con un router o un switch multicapa, con el objetivo de activar el inter-vlan routing, es decir, el enrutamiento entre VLANs para sí permitir la comunicación entre ellas siempre que lo necesitemos.
- **Segmentación**. Las VLAN nos permite segmentar todos los equipos en diferentes subredes, a cada subred le asignaremos una VLAN diferente. 
- **Flexibilidad**. Gracias a las VLAN podremos colocar a los diferentes equipos en una subred o en otra, de manera fácil y rápida, y tener unas políticas de comunicación donde permitimos o denegamos el tráfico hacia otras VLANs o hacia Internet. 
- **Optimización de la red**. Al tener subredes más pequeñas, en entornos donde tengamos cientos o miles de equipos conectados, contendremos el broadcast en dominios más pequeños, por tanto, el rendimiento de la red será óptimo, sin tener que transmitir los mensajes de broadcast a todos los equipos conectados, lo que haría que el rendimiento de la red baje radicalmente e incluso podría llegar a colapsar. Al usar VLAN, tendremos varios dominios de difusión en el mismo switch. En redes donde el tráfico consiste en un alto porcentaje de transmisiones y multidifusiones, las VLAN pueden reducir la necesidad de enviar dicho tráfico a destinos innecesarios. 
- **Reducción de costes**. Debido a la poca necesidad de actualizaciones de red que son demasiado costosas, y gracias a un uso más eficaz de los enlaces y del ancho de banda disponible, es posible reducir costes al realizar este tipo de redes. Las VLAN se pueden usar para crear dominios de transmisión que eliminan la necesidad de costosos routers, lo cual ayuda aún más a reducir dichos costes.
- **Mejor eficiencia del personal de TI**. Nos facilitarán el manejo de la red, debido a que diferentes usuarios pueden compartir una misma VLAN. Cuando implementamos un nuevo switch, este implantará todas las políticas y procedimientos que tiene prestablecidos la VLAN. 
- **Administración de aplicaciones y proyectos simples**. Estas redes pueden agregar dispositivos y usuarios para admitir ciertos requisitos geográficos o de tipo comercial. Como tienen características diferentes, se facilita mucho la administración de una aplicación concreta, o albergando proyectos diferentes.

**¿Tienen desventajas las VLAN?**

Pese a que las VLAN ofrecen ventajas como segmentación de redes, seguridad y gestión eficiente del tráfico, también tienen una serie de desventajas que deberíamos conocer antes de su configuración:

**- Complejidad en el mantenimiento:** No solo la configuración e instalación requieren de conocimientos, sino también el mantenimiento, por lo que, pese a que contratemos a alguien para la puesta a punto, tendremos que tener nociones posteriores, o contratar a alguien siempre, algo que puede ser muy costosos o requerir de aprendizaje avanzado si no lo tenemos.

**- Escalabilidad limitada:** Algunos switches tienen límites en la cantidad de VLANs que pueden soportar, por lo que si hablamos de gestionar muchas VLANs en grandes infraestructuras, puede ser engorroso y poco eficiente.

**- Problemas de rendimiento:** Si se manejan muchas VLANs en el mismo equipo (como un switch o router), podría haber sobrecarga de procesamiento, por lo que si hablamos de algo simple, puede ir muy bien, pero a nivel de escalabilidad, como comentábamos ahora, se puede poner complicado todo.

**- Seguridad:** Si no se implementan bien las políticas de seguridad (como el uso adecuado de VLAN hopping o storm control), una VLAN puede ser vulnerable a ataques (por ejemplo, ataques de VLAN hopping). 

**- Compatibilidad:** Todos los dispositivos en la red deben ser compatibles con VLANs y el estándar 802.1Q. Esto podría limitar mucho las opciones de hardware, obligándonos a adquirir nuevos sustitutos, lo que se vería reflejado en un incremento de gasto.

**Tipos de VLAN**
- VLAN nativa
- Etiquetado VLAN 802.1Q
- VLAN basadas en puerto
- VLAN basadas en MAC
- VLAN etiquetadas
- VXLAN
- VLAN híbrida
- VLAN de gestión
- VLAN de control
- VLAN dedicada


2. **¿Qué es una VPN?**
   Una VPN es una tecnología de red y seguridad fundamental en un mundo en el que las aplicaciones abarcan la infraestructura local y los servicios en la nube pública. A menudo se usan junto con Confianza cero y otros enfoques de seguridad modernos, las VPN encapsulan los datos en cifrado y los envían a través de un túnel protegido al que solo pueden conectarse usuarios y dispositivos autorizados.
Una VPN (Virtual Private Network) ayuda a proteger las experiencias en línea mediante la creación de conexiones a Internet seguras y cifradas entre dispositivos de usuario y una red privada.

Una VPN es una tecnología de red y seguridad fundamental en un mundo en el que las aplicaciones abarcan la infraestructura local y los servicios en la nube pública. A menudo se usan junto con Confianza cero y otros enfoques de seguridad modernos, las VPN encapsulan los datos en cifrado y los envían a través de un túnel protegido al que solo pueden conectarse usuarios y dispositivos autorizados.

**¿Cómo funciona una VPN?**

En lugar de enviar datos directamente a través de Internet, una red privada virtual canaliza los datos cifrados entre el dispositivo y un punto de conexión de confianza, como una red corporativa o un entorno en la nube. Un servidor VPN intermedio autentica al usuario y a su dispositivo, enmascara la dirección IP y le permite omitir los firewalls y los bloques de sitios web en Internet. Este enfoque ayuda a evitar el acceso no autorizado, la interceptación y la manipulación de datos.

Por definición, una conexión VPN es:

- Virtual porque no hay cables físicos implicados en el proceso de conexión.
- Privada porque a través de esta conexión, nadie más puede ver los datos ni la actividad de exploración.
- En red porque varios dispositivos (su ordenador y el servidor VPN) funcionan de manera conjunta para mantener el vínculo establecido.

Una VPN depende de tres tecnologías clave:

**Cifrado**
El cifrado convierte los datos legibles en un formato ilegible conocido como texto cifrado. Las VPN se basan en algoritmos criptográficos sólidos para que, incluso si se interceptan datos, no se puedan entender sin las claves adecuadas. Esto protege la información confidencial, como las credenciales, la propiedad intelectual y las comunicaciones internas mientras están en tránsito.

**Tunelización**
La tunelización es el proceso de encapsular datos cifrados dentro de otro paquete de red para que puedan viajar de forma segura a través de Internet. El túnel actúa como un camino privado entre el usuario y la red de destino. La tunelización VPN ayuda a proteger el tráfico de la interceptación, especialmente en redes no seguras, como una red inalámbrica pública, donde el tráfico sin cifrar se puede observar o interceptar de otro modo.

**Autenticación**
Antes de establecer un túnel, las VPN autentican usuarios o dispositivos para confirmar que pueden conectarse. Este paso garantiza que solo los puntos de conexión aprobados obtengan acceso a los sistemas internos o a los recursos en la nube. Juntos, el cifrado, la tunelización y la autenticación forman la base de cómo funciona una red privada virtual.

Las VPN suelen funcionar junto con otras tecnologías como macrodatos, inteligencia artificial y aprendizaje automático para admitir sistemas digitales seguros y escalables.

**¿Cuáles son las principales ventajas de una VPN?**

Las redes privadas virtuales ofrecen varias ventajas para individuos y organizaciones, especialmente a medida que los recursos y las aplicaciones se distribuyen más. Estas son algunas de las principales ventajas:

- **Privacidad y seguridad mejoradas:** al cifrar el tráfico y enmascarar las direcciones IP, las VPN ayudan a proteger la privacidad del usuario y reducen la exposición en redes públicas o compartidas. Esto es especialmente importante cuando se accede a sistemas confidenciales fuera de un entorno corporativo de confianza.
- **Mayor protección para trabajadores remotos e híbridos:** los modelos de trabajo flexibles dependen de proporcionar a los usuarios acceso seguro a los sistemas internos. Las VPN permiten a los empleados, desarrolladores y estudiantes conectarse de forma segura a redes privadas desde casi cualquier lugar sin exponer esos recursos directamente a Internet.
- **Experiencias de cliente fluidas:** los usuarios se sienten como si sus dispositivos estuvieran conectados directamente a una red privada, aunque estén trabajando desde casa, una cafetería o un aeropuerto.
- **Acceso más seguro a los recursos en la nube:** a medida que las organizaciones adoptan cada vez más plataformas en la nube, como Microsoft Azure, las VPN ayudan a unir los entornos locales con los servicios en la nube. Servicios seguros y basados en la nube, como VPN Gateway proporcionan conectividad cifrada entre centros de datos locales y redes virtuales de Azure.
- **Cumplimiento mejorado y menor riesgo:** muchos marcos normativos y del sector requieren medidas de seguridad para los datos en tránsito. Las VPN admiten estos requisitos al ayudar a proteger la información confidencial a medida que se mueve entre usuarios, redes y servicios en la nube. También admiten equipos distribuidos al tiempo que permiten a las organizaciones mantener controles centralizados.

**¿Cuáles son algunos tipos de VPN?**

Las VPN se usan en sectores y entornos, incluidos los siguientes escenarios:

- **Trabajo remoto:** las organizaciones usan VPN para proporcionar a los empleados y contratistas acceso remotos a aplicaciones internas, entornos de desarrollo y datos sin hacer que esos sistemas sean accesibles públicamente. Los empleados pueden conectarse de forma segura a las redes corporativas desde casa o mientras se desplazan, manteniendo la productividad sin poner en peligro la seguridad.
- **Conectividad de sitio a sitio:** una VPN de sitio a sitio conecta varias ubicaciones de oficinas, como sucursales o centros de datos, a través de Internet. Esto permite a las organizaciones vincular ubicaciones de forma segura sin depender de circuitos privados costosos.
- **Entornos híbridos y multinube:** al habilitar conexiones seguras entre la infraestructura local y los servicios en la nube, las VPN pueden admitir cargas de trabajo híbridas y multinube y una migración gradual a la nube.
- **Entornos de desarrollador:** los desarrolladores suelen usar VPN para compilar, probar y mantener aplicaciones basadas en la nube y otras soluciones. Esto incluye soluciones con servicios cognitivos que requieren acceso seguro, cifrado y privado a las API de IA.
- **Entornos de aprendizaje y estudiantes:** muchas universidades y escuelas se basan en VPN para proporcionar a los alumnos fuera del campus acceso a sistemas internos, como plataformas de administración del aprendizaje, bibliotecas digitales, bases de datos de investigación y entornos de laboratorio.

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
- Sergio Lezcano: No tengo experiencia. 







