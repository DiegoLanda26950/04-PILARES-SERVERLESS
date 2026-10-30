# Bloque 02
 
## Resultado
- Qué añadí al proyecto:No he modificado nada Comprobé una ruta y la función de eventos existentes
- Ruta o pantalla comprobada: GET http://localhost:3010/dev/events/EVT-330 mediante curl
- Estado y respuesta observados: id: "EVT-330", 
                                    artist: "Neon Waves", 
                                    space: "Main Stage", 
                                    time: "22:30",
                                    status: "CONFIRMED"
 
## Comprensión
- Recorrido del dato, explicado con mis palabras: La ruta events/{id} de Serverless envía la petición a getEvent.handler. La función obtiene id de event.pathParameters, lo escribe en el log y lo incluye en el JSON de respuesta.

-Cambio guiado y resultado: pedi un tercer identificador sin cambiar la funcións se mostro EVT-330.

- Error encontrado y cómo lo resolví:
 
## Evidencias
- Captura o transcripción breve, sin credenciales:
GET /dev/events/EVT-330 (λ: getEvent)
GET evento: EVT-330
HTTP/1.1 200 OK
{"id":"EVT-330","artist":"Neon Waves","space":"Main Stage","time":"22:30","status":"CONFIRMED"}

- Limitaciones del ejercicio: La comprobación fue local con curl y Serverless Offline. No realicé una petición desde Thunder Client ni comprobé un despliegue en AWS.
 