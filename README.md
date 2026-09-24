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

## 5. Protocolos de Comunicación

Un **protocolo de comunicación** es un conjunto estandarizado de reglas, pautas e instrucciones que rigen el intercambio de información entre sistemas informáticos.

### Tipos de protocolos
1. **Punto a punto:** Diseñados para transferir información directamente entre dos equipos. Gestionan el envío, recepción y retransmisión de mensajes hasta recibir un acuse de recibo (*ACK*).
2. **Comunicación entre redes:** Permiten la interacción de múltiples usuarios en una red local (LAN). Utilizan identificadores para cada terminal y coordinan el tráfico de forma organizada.
3. **De transmisión de paquetes:** Centran el control de la transmisión en los propios paquetes de datos y sus metadatos (en lugar de en los nodos). La información se fragmenta y viaja de manera independiente hasta el destino.
4. **TCP/IP:** Protocolo basado en la transmisión de paquetes. Divide la información en fragmentos independientes que eligen la ruta más eficiente según el estado de la red, garantizando estabilidad y velocidad.

---

## 6. TCP/IP vs. NetBIOS

### Modelo TCP/IP
Es la suite de protocolos estandarizada sobre la que se estructura Internet y la mayoría de las redes modernas. Divide los datos en paquetes, los transmite por rutas óptimas y los reensambla en el destino.

#### Capas del modelo TCP/IP
1. **Acceso a la Red (Enlace):** Administra la infraestructura física y los controladores de red (cables Ethernet, Wi-Fi, tarjetas NIC) transformando los datos digitales en señales físicas.
2. **Internet (Red):** Gestiona la direccionamiento, el enrutamiento y el flujo del tráfico entre distintas redes, asegurando la entrega eficiente de los paquetes.
3. **Transporte:** Proporciona una conexión de datos fiable de extremo a extremo (mediante la fragmentación, verificación y acuse de recibo de los paquetes).
4. **Aplicación:** Conjunto de protocolos que ofrecen servicios de red directos al usuario o a los programas (correo electrónico, la web, almacenamiento en la nube).

### NetBIOS
Es una interfaz de software y conjunto de servicios de nivel de sesión desarrollado originalmente para pequeñas redes locales (LAN). Proporciona:
* **Servicio de nombres:** Identifica dispositivos con nombres legibles en lugar de direcciones numéricas.
* **Servicio de datagramas:** Permite el envío de mensajes simples sin conexión.
* **Servicio de sesión:** Establece y mantiene conexiones orientadas a sesión para compartir archivos e impresoras.

### Diferencia clave

| Característica | NetBIOS | TCP/IP |
| :--- | :--- | :--- |
| **Alcance** | Redes locales pequeñas (LAN) o entornos heredados. | Estándar global (LAN, WAN e Internet). |
| **Nivel** | Interfaz de software / Capa de sesión. | Conjunto de protocolos multicapa completo. |
| **Escalabilidad** | Limitada; dependiente de difusión local. | Alta; diseñado para enrutamiento entre redes masivas. |

---

## 7. Estructura de un Paquete TCP/IP y "Flags"

Un paquete de datos en la pila TCP/IP se compone de un **encabezado IP**, un **encabezado TCP** (o UDP) y la carga útil de datos (**Payload**).

+-------------------------------------------------------------+
|                       Encabezado IP                         |
+-------------------------------------------------------------+
|                       Encabezado TCP                        |
+-------------------------------------------------------------+
|                       Payload (Datos)                       |
+-------------------------------------------------------------+

### Componentes del Encabezado IP
* **Versión:** IPv4 o IPv6.
* **Longitud de cabecera:** Tamaño del encabezado para su correcta lectura.
* **Tipo de servicio (ToS/QoS):** Define la prioridad del paquete.
* **Identificación y Banderas:** Controlan la fragmentación y reensamblado de paquetes grandes.
* **Tiempo de Vida (TTL):** Límite de saltos para evitar que los paquetes circulen indefinidamente.
* **Protocolo:** Especifica el protocolo de la capa superior (ej. TCP o UDP).
* **Suma de comprobación:** Valida la integridad del encabezado IP.
* **Direcciones IP:** Especifican el origen y el destino.

### Componentes del Encabezado TCP
* **Puertos de Origen y Destino:** Identifican las aplicaciones emisoras y receptoras.
* **Número de secuencia y Acuse de recibo (ACK):** Mantienen el orden de los datos y confirman la recepción.
* **Longitud de la cabecera y Ventana:** Especifican el tamaño del encabezado y el control de flujo de datos.
* **Suma de verificación:** Comprueba la integridad del segmento TCP.
* **Flags (6 bits de control):** Indicadores que gestionan el estado y comportamiento de la conexión TCP:
  * **SYN:** Inicia una nueva conexión (*Handshake*).
  * **ACK:** Confirma la recepción válida de un paquete o número de secuencia.
  * **FIN:** Solicita la finalización ordenada de la conexión.
  * **RST:** Reinicia la conexión de manera abrupta ante un fallo o error.
  * **PSH:** Solicita la entrega inmediata de los datos a la aplicación sin esperar a llenar el búfer.
  * **URG:** Indica que el segmento contiene información urgente que debe procesarse prioritariamente.

---

## 8. Clasificación de Redes según su Geografía

| Red | Denominación | Alcance y Descripción |
| :--- | :--- | :--- |
| **PAN** | *Personal Area Network* | **Corto alcance (pocos metros):** Conecta dispositivos de uso personal (smartphones, periféricos) mediante Bluetooth, USB o Zigbee. |
| **LAN** | *Local Area Network* | **Espacio limitado (oficinas, casas, edificios):** Ofrece alta velocidad y baja latencia mediante conexiones cableadas (Ethernet) o locales. |
| **WLAN** | *Wireless LAN* | **Variante inalámbrica de la LAN:** Utiliza ondas de radio (Wi-Fi), proporcionando movilidad, agilidad de despliegue y escalabilidad. |
| **MAN** | *Metropolitan Area Network* | **Área metropolitana (ciudades, campus universitarios):** Interconecta múltiples LANs dentro de una misma zona geográfica densa. |
| **WAN** | *Wide Area Network* | **Extensiones masivas (países, continentes):** Une subredes dispersas a través de fibra óptica, satélites y microondas. El ejemplo principal es **Internet**. |
| **GAN** | *Global Area Network* | **Cobertura global:** Infraestructura transcontinental que combina satélites y redes internacionales para dar soporte a la conectividad móvil mundial. |
| **VPN** | *Virtual Private Network* | **Red Lógica / Arquitectura Cifrada:** No definida por distancia física, sino por construir un túnel privado, autenticado y cifrado sobre una red pública (como Internet). |

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







