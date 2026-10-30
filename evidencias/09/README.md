# Bloque 09

## Resultado
- Qué añadí al proyecto:Revisé la configuración de la URL base de la API y cambie la url de la api
- Ruta o pantalla comprobada: Revisé el api.ts; ahora contiene `https://ttsyiz3ekh.execute-api.us-east-1.amazonaws.com/dev`.
- Estado y respuesta observados: Ejecute el endpoint de get y devolvio lossss conciertos con exito

## Comprensión
- Recorrido del dato, explicado con mis palabras: Las funciones de API construyen las rutas añadiéndolas a `API_URL`, por ejemplo `'/events'` para listar eventos. La URL base debe apuntar al API Gateway desplegado y terminar en el stage correcto.
- Cambio guiado y resultado: Sustituí la URL de ejemplo por la de AWS. La api me devolvio los datoss con exito
- Error encontrado y cómo lo resolví: 

## Evidencias
- Captura o transcripción breve, sin credenciales:
  
  API_URL = https://ttsyiz3ekh.execute-api.us-east-1.amazonaws.com/dev
 
- Limitaciones del ejercicio: Confirmé la URL de API Gateway y ejecuté peticiones cloud
