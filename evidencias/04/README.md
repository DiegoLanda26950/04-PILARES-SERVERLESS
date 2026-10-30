# Bloque 04

## Resultado
- Qué añadí al proyecto: Comprobé las rutas PUT y PATCH ya configuradas para los eventos
- Ruta o pantalla comprobada: PUT, PATCH y "GET http://localhost:3014/dev/events/EVT-101", con Serverless Offline
- Estado y respuesta observados: PUT con `{"status":"CANCELLED"}` devolvió `400`. PATCH con el mismo body devolvió `operation: "UPDATED"`. El GET siguiente devolvió `200` y `status: "CONFIRMED"`.

## Comprensión
- Recorrido del dato, explicado con mis palabras: Serverless dirige PUT y PATCH a handlers distintos para el evento indicado. PUT valida el body como un reemplazo completo, por eso rechaza un body que sólo contiene `status`. PATCH acepta ese único campo y responde con el cambio solicitado.
- Cambio guiado y resultado: Envié `{"status":"CANCELLED"}` mediante PUT y PATCH a EVT-101. PUT respondió `400`; PATCH respondió `200` con `operation: "UPDATED"`. Al consultar el evento de nuevo, el estado seguía siendo `CONFIRMED`.
- Error encontrado y cómo lo resolví: PUT respondió `400` porque faltaban los campos obligatorios para reemplazar el evento completo. Para probar una actualización parcial, envié el mismo body mediante PATCH, que respondió `200`.

## Evidencias
- Captura o transcripción breve, sin credenciales:
  
  PUT /dev/events/EVT-101 {"status":"CANCELLED"} -> 400
  PATCH /dev/events/EVT-101 {"status":"CANCELLED"} -> 200 {"id":"EVT-101","changes":{"status":"CANCELLED"},"operation":"UPDATED"}
  GET /dev/events/EVT-101 -> 200 {"id":"EVT-101","artist":"Neon Waves","space":"Main Stage","time":"22:30","status":"CONFIRMED"}
 
- Limitaciones del ejercicio: La comprobación fue local con Serverless Offline. El handler PATCH informa el cambio, pero GET sigue devolviendo `CONFIRMED`. 
