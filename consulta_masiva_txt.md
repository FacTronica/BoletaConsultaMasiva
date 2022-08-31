# BoletaConsultaMasiva

Método 1 : [TXT] Consulta Masiva con Archivo Txt
------------------------------------------------
Este método permite realizar la consulta masiva de boletas por medio de un archivo de texto plano.

Pasos a seguir:
---------------

Paso 1:
-------
Crear un archivo de texto plano con el formato requerido.
<br>En este archivo se deben incluir los datos de todas las boletas que se requiere consultar.
<br>Aquí un ejemplo del formato del archivo plano:

https://github.com/FacTronica/BoletaConsultaMasiva/blob/main/txt_consultarfolio_masivo.php


Paso 2:
-------
Enviar el archivo txt a la url de la api.
<br>El envío del txt se debe realizar vía post upload file.
<br>Para realizar el envío del archivo Txt con la librería curl se utiliza el siguiente comando:

```

LINUX:
curl --form "archivito=@archivo.txt" https://dominio.cl/api/factronica_boleta_consultamasiva/index.php

WINDOWS:
c:\curl\curl.exe --form "archivito=@c:\curl\archivo.txt" https://dominio.cl/api/factronica_boleta_consultamasiva/index.php


```

Paso 3:
-------
Recuperar el archivo de texto plano con el resultado de las boletas consultadas.
<br>Para recuperar el archivo Txt con la librería curl se utiliza el siguiente comando:

```

LINUX:
curl --form -o resultado.txt https://dominio.cl/api/factronica_boleta_consultamasiva/respuestas/resultado.txt

WINDOWS:
c:\curl\curl.exe --form -o c:\curl\resultado.txt https://dominio.cl/api/factronica_boleta_consultamasiva/respuestas/resultado.txt


```

El resultado con la respuesta masiva del archivo resultado.txt tiene el siguiente formato

```

{'ESTADO':'OK','FOLIO':'1163','TIPO':'39'}
{'ESTADO':'OK','FOLIO':'1164','TIPO':'39'}
{'ESTADO':'ERROR','FOLIO':'1165','TIPO':'39'}
{'ESTADO':'ERROR','FOLIO':'1166','TIPO':'39'}
{'ESTADO':'OK','FOLIO':'1167','TIPO':'39'}
{'ESTADO':'OK','FOLIO':'1168','TIPO':'39'}
{'ESTADO':'OK','FOLIO':'1169','TIPO':'39'}
{'ESTADO':'OK','FOLIO':'1170','TIPO':'39'}
{'ESTADO':'OK','FOLIO':'1171','TIPO':'39'}
{'ESTADO':'OK','FOLIO':'1172','TIPO':'39'}
{'ESTADO':'OK','FOLIO':'1173','TIPO':'39'}


```
