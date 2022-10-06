ut2-a1. Ejercicios modelo OSI

   1. ¿Qué niveles OSI son los niveles de soporte de red? 
    
El nivel 1 (Físico)

El nivel 2 (enlace)

El nivel 3 (red)

El nivel 4 (tranporte)

   2. ¿Qué niveles OSI son los niveles de soporte de usuario? 

El nivel 5 (sesión)

El nivel 6 (presentación) 

El nivel 7(aplicación)

   3. ¿Cómo están OSI e ISO relacionadas entre sí? 

Están relacionados porque ISO es la organización de estándares
que creo el modelo de interconexión de sistemas abiertos OSI.

   4. Enumere los niveles del modelo OSI.

Nivel 1: Físico

Nivel 2: Enlace

Nivel 3: Red

Nivel 4: Transporte

Nivel 5: Sesión

Nivel 6: Presentación

Nivel 7: Aplicación

   5. ¿Cómo pasa la información de un nivel OSI al siguiente? 

Pasa del nivel mas alto (7) en la maquina A hasta el nivel mas
bajo (1) de la misma, y se envía en lujo de bits al nivel mas bajo
(1) de la maquina B y sube hasta el nivel mas alto (7) de la
maquina B.

   6. ¿Qué son las cabeceras y cola y cómo se añaden y se quitan? 

Las cabeceras o colas son datos de control que se añaden al
principio o al inal de un paquete de datos.

Las cabeceras se añaden en la maquina emisora en los niveles:
6,5,4,3,2, y en el nivel 2 se añade una cola.

Se quitan en la maquina receptora al pasar nivel por nivel, cada
nivel procesa y elimina los datos que son para el.

   7. ¿Cuáles son las responsabilidades del nivel físico? 

Características físicas de las interfases y el medio

Representación de los bits

Tasa de datos

Sincronización de los bits


   8. ¿Cuáles son las responsabilidades del nivel de enlace? 

Tramado

Direccionamiento físico

Control de lujo

Control de errores


   9. ¿Cuáles son las responsabilidades del nivel de red? 

 Direccionamiento lógico

Encaminamiento

   10. ¿Cuáles son las responsabilidades del nivel de transporte? 


 Direccionamiento en punto de servicio.

Segmentación y reensamblado.

Control de conexión

Control de lujo

Control de errores

   11. El nivel de transporte crea una conexión entre el origen y el destino. ¿Cuáles son los tres eventos involucrados en la conexión? 
   
Establecimiento de la conexión

Transferencia de datos

Liberación de la conexión

   12. ¿Cuál es la diferencia entre una dirección de punto en servicio, una dirección lógica y una dirección fisica? 
  
Direccionamiento lógico: proporcionado por el nivel de enlace de datos gestiona los problemas de direcciones locales si un paquete cruza la frontera
de la red es necesario tener otro tipo de direcciones para
distinguir los sistemas origen de los del destino

Punto de servicio: las computadoras suelen ejecutar a
menudo varios programas al mismo tiempo por esa razón la
entrega desde el origen al destino signiica la entrega no solo de
una pc a otra sino también desde un proceso especiico

Direccionamiento físico: si es necesario distribuir las tramas
por distintos sistemas de la red, el nivel de enlace de datos
añade una cabecera a la trama para deinir la dirección física del
emisor (dirección fuente) y/o receptor (dirección destino) de la
trama.

  13. ¿Cuáles son las responsabilidades del nivel de sesión? 

Control de dialogo

Sincronización

  14. ¿Cuáles son las responsabilidades del nivel de presentación? 

Traducción

Cifrado

Compresión
    
  15. ¿Cuál es el objetivo de la traducción en el nivel de presentación? 

Traducción

Cifrado

Compresión

  16. Indique alguno de los servicios proporcionados por el nivel de aplicación.

Terminal virtual de red

Servicios de correo

  17.  ¿Cómo se relacionan los niveles de la familia del protocolo TCP/IP con los niveles del modelo OSI?

Mediante el nivel de aplicación

  18. El nivel de sesión decide la localización de los puntos de sincronización. 

    transporte
    sesión (escogi esta opción)
    presentación
    aplicación

  19. En el nivel de enlace de datos, la unidad de datos se denomina trama.

    físico
    enlace de datos (escogi esta opcón)
    red
    transporte

 20. Los servicios de correo y de directorio están disponibles a los usuarios de la red a través del nivel:

    enlace de datos
    sesión
    transporte
    aplicación (escogi esta opcón)

 21. A medida que los paquetes de datos se mueven  de los niveles inferiores a los superiores las cabeceras:

    añadidas (escogi esta opción)
    eliminadas
    recolocadas
    modificadas



