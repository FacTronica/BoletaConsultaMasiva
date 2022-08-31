# BoletaConsultaMasiva

Consultar Estado de Boletas de forma Masiva
===========================================

Introducción
------------
Esta función permite realizar la consulta masiva de un rango de boletas de venta por Emisor.
En tan solo segundos puede obtener el resultado del estado de cientos de boletas.

Métodos para realizar la Integración
------------------------------------
La integración de esta función se puede realizar por 2 mecanismos

1. [TXT] Consulta Masiva con Archivo Txt

2. [JSON] Consulta Masiva con Datos JSON


Para realizar el envío del archivo Txt a la Api se debe utilizar el siguiente comando curl:
```
curl --form "archivito=@archivo.txt" https://dominio.cl/api/factronica_boleta_consultamasiva/index.php

```
