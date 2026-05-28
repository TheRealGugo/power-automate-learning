# Semana 1 — Anatomía de flujos

## Ejercicio
Flujo de gestión de facturas por correo electrónico.

## QUE HACE
El flujo hace que de enviar factura a un correo.
Recibe el correo, señala si existe la factura
Extrae el documento en una carpeta y clasfica respecto al día y mes entregado
Respecto si es de diferente año, se crea otra carpeta

## TRIGER USADO Y POR QUE
Cada vez que un correo llega, y de existir la condición de subject: factura y un attachment especifico, que solo es pdf, se guarda

## CONVERT TIME ZONE 
convertTimeZone(triggerOutputs()?['body/receivedDateTime'],
'UTC','SA Pacific Standard Time','yyyy-MM-dd')
De acuerdo a las zona de sudamerica, se guarda además el año,mes y día

## TRAMPAS
1 Que no guarde imagen de firma o imagenes añadidas por parte de un correo corporativo 
2 Que se pueda guardar con fecha y nombre correcto
3 Que el correo se cree correctamente en el onedrive

## problemas
Tener en cuenta los permiso de tu cuenta institucional, se recomienda una corporativa.
Asi mismo de tener en cuenta no combinar los archivos en onedrive para empresas y la local