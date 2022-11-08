g.     Haga clic en la pestaña Outbound PDU Details

La información que figura en PDU Formatses reflejo de las capas del modelo TCP/IP.

Nota: La información que aparece en la sección Ethernet II de la pestaña Outbound PDU Details proporciona información aún más detallada que la que se muestra en Layer 2 en la pestañaOSI Model. Los Outbound PDU Details proporcionan información más descriptiva y detallada. Los valores bajo DEST MAC y SRC MAC dentro de la sección Ethernet II de PDU Detailsaparecen en la pestaña OSI Model bajo Layer 2, pero no se identifican como tales. Preguntas:

¿Cuál es la información común que figura en la sección IP de los PDU Details en comparación con la información que figura en la pestaña del OSI Model ? ¿Con qué capa está asociado?

¿Cuál es la información común que aparece en la sección TCP de PDU Details, en comparación con la información que aparece en la pestaña delOSI Model , y con qué capa está asociada?

¿Cuál es el host que aparece en la sección HTTP de los PDU Details? ¿Con qué capa se asociaría esta información en la pestaña del MOdelo OSI?

h.     Haga clic sobre la primer caja de color en Event List > bajo la columna Type . Solo Layer 1 está activa (sin atenuar). El dispositivo mueve la trama del búfer y lo coloca en la red.

i.      Avance al siguiente cuadro HTTP Type dentro de Event List y haga clic en la caja de color. Esta ventana contiene tanto en In Layers como Out Layers. Observe la dirección de la flecha directamente debajo de la columnaIn Layers ; apunta hacia arriba, indicando la dirección en la que viajan los datos. Desplácese por estas capas y tome nota de los elementos vistos anteriormente. En la parte superior de la columna, la flecha apunta a la derecha. Esto indica que el servidor ahora está enviando la información al cliente.

Pregunta:
Comparando la información que se muestra en la columnaIn Layers con la de la columna Out Layers, ¿cuáles son las principales diferencias?

j.      Haga clic en la pestaña Inbound and Outbound PDU Details. Revise los detalles PDU.

k.     Haga clic sobre la última caja de color bajo la columna Info.

Pregunta:
¿Cuántas pestañas se muestran con este evento? Explique.


Parte 2: Muestre elementos del conjunto de Protocolos TCP/IP
En la Parte 2 de esta actividad, utilizará el modo Simulación de Packet Tracer para ver y examinar algunos de los otros protocolos que comprenden el conjunto TCP/IP.

Step 1: View Additional Events
a.     Cierre cualquier ventana de información de PDU abierta.

b.     En elEvent List Filters > seccion Visible Events, haga clic en Show All/None.

Pregunta:
¿Qué tipos de eventos adicionales se muestran?

Estas entradas adicionales desempeñan varios roles dentro del conjunto TCP/IP . El Protocolo de resolución de direcciones (ARP) solicita direcciones MAC para hosts de destino. DNS es responsable de convertir un nombre (por ejemplo, www.osi.local) a una dirección IP. Los eventos TCP adicionales son responsables de conectarse, acordar los parámetros de comunicación y desconectar las sesiones de comunicación entre los dispositivos. These protocols have been mentioned previously and will be further discussed as the course progresses. Currently there are over 35 possible protocols (event types) available for capture within Packet Tracer.

c.     Haga clic en el primer evento de DNS en la columna Type. Explore las pestañas OSI Model y PDU Detail y observe el proceso de encapsulación. Al mirar la pestaña OSI Model con Layer 7 resaltada, una descripción de lo que está ocurriendo se encuentra justo debajo de In Layers y Out Layers (“1. El cliente DNS envía una consulta DNS al servidor DNS."). Esta es información muy útil para ayudar a comprender lo que ocurre durante el proceso de comunicación.

d.     Haga clic en la pestaña Outbound PDU Details .

Pregunta:
¿Qué información se indica en el campo NAME :en la sección de DNS QUERY?

e.     Haga clic en la ultima caja de color de Info de DNS en el event list.

Preguntas:
¿En qué dispositivo se capturó la PDU?

¿Cuál es el valor que aparece junto a ADDRESS: en la sección DNS ANSWER de Inbound PDU Details?

f.      Busque el primer evento HTTP en la lista y haga clic en la caja de color del TCP event inmediatamente después de este evento. Resalte Layer 4 en la pestaña OSI Model.

Pregunta:
En la lista numerada directamente debajo de In Layers y Out Layers, ¿cuál es la información que se muestra en los elementos 4 y 5?

TCP gestiona la conexión y desconexión del canal de comunicaciones junto con otras responsabilidades. Este evento en particular muestra que el canal de comunicación ha sido ESTABLECIDO.

g.     Haga clic en el último evento TCP. Resalte Layer 4 en la pestaña OSI Model. Examine los pasos enumerados directamente debajo de In Layers y Out Layers.

Pregunta:
¿Cuál es el propósito de este evento, basado en la información proporcionada en el último elemento de la lista (debe ser el elemento 4)?

