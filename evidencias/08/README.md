# Bloque 08

## Resultado
- Qué añadí al proyecto: No añadí código. No pude realizar la comprobación de la Lambda desplegada en AWS.
- Ruta o pantalla comprobada: No se consultó ningún endpoint cloud ni se ejecutó `npx serverless logs -f getEvent --stage dev --region "$AWS_REGION"`.
- Estado y respuesta observados: No se obtuvieron respuestas HTTP cloud para `EVT-101` ni `NO-EXISTE`, y no se consultaron logs. Por tanto, no comprobé los resultados esperados `200` y `404`.

## Comprensión
- Recorrido del dato, explicado con mis palabras: La ruta configurada `events/{id}` envía el id de la URL a `getEvent.handler`. Se escribe en el log como `GET evento: <id>` y busca el evento en el catálogo.
- Cambio guiado y resultado: No hice cambios ni ejecuté la prueba cloud porque no tenía una sesión AWS CLI autenticada ni un URL de API Gateway confirmado.
- Error encontrado y cómo lo resolví:

## Evidencias
- Captura o transcripción breve, sin credenciales:
- Limitaciones del ejercicio: