# Estación meteorológica básica IoT
Estación meteorológica IoT básica basada en ESP8266. Pensada para poder prevenir heladas en cultivos.

La idea de ésta estación proviene de la necesidad en zonas rurales de controlar la temperatura para intentar combatir las heladas. Cuando un agricultor prevee una helada, éste pone en marcha varios sistemas que intentan combatirla encendiendo lumbres y usando sumideros(ventiladores) invertidos para mezclar el aire. La estación provee información al agricultor en su teléfono móvil, incluso usando alarmas, que le permiten conocer las condiciones meteorológicas exactas en sus cultivos de manera que puedan actuar si es preciso o quedarse tranquilos en casa si no lo es.

El proyecto está pensado para ser efectivo y barato(su coste de base es de aproximadamente 10€), siendo para ello modular, por lo que está montado sobre el microcontrolador de una placa ESP8266, que hace la función de un Arduino con antena WiFi. Ésta placa se puede intercambiar por alguna otra con SIM integrada, yo he elegido ésta placa porque en mi caso los agricultores que he consultado prefieren usar un smartphone antiguo para generar la red WiFi o usarla en zonas donde se dispone de internet. El sensor básico es un DHT11, que recoge temperatura y humedad, al que le pueden añadir varios más dependiendo de las necesidades del agricultor. La placa puede estar alimentada por la red eléctrica o, más interesante para zonas rurales, por batería o pilas, ya que el consumo de base es muy pequeño.

La estación manda los datos al servicio de código abierto ThingSpeak. A partir de aquí cualquier interesado en los datos de la estación tan sólo deberá de conectarse al canal correspondiente, en mi caso mediante las aplicaciones IoT ThingSpeak Monitor Widget y PocketIOT(tienen la capacidad de mostrar los datos de un canal y realizar avisos bajo circuntancias a elegir), ambas gratuitas, y con la posibilidad también de usar los servicios de ThingSpeak para enviar un tweet bajo ciertas circunstancias.
