# BoletaConsultaMasiva

Método 1 : [TXT] Consulta Masiva con Archivo Txt
------------------------------------------------
Este método permite realizar la consulta masiva de boletas por medio de un archivo de texto plano.

Pasos a seguir:
---------------

Paso 1:
-------
Crear un archivo de texto plano con el formato requerido.
En este archivo se deben incluir los datos de todas las boletas que se requiere consultar.
Aquí un ejemplo del formato del archivo plano:
https://github.com/FacTronica/BoletaConsultaMasiva/blob/main/txt_consultarfolio_masivo.php


Paso 2:
-------
Enviar el archivo txt a la url de la api.
El envío del txt se debe realizar vía post upload file.
Para realizar el envío del archivo Txt con la librería curl se utiliza el siguiente comando:

```

LINUX:
curl --form "archivito=@archivo.txt" https://dominio.cl/api/factronica_boleta_consultamasiva/index.php

WINDOWS:
c:\curl\curl.exe --form "archivito=@c:\curl\archivo.txt" https://dominio.cl/api/factronica_boleta_consultamasiva/index.php


```

Paso 3:
-------
Recuperar el archivo de texto plano con el resultado de las boletas consultadas.
Para recuperar el archivo Txt con la librería curl se utiliza el siguiente comando:

```

LINUX:
curl --form -o resultado.txt https://dominio.cl/api/factronica_boleta_consultamasiva/respuestas/resultado.txt

WINDOWS:
c:\curl\curl.exe --form -o c:\curl\resultado.txt https://dominio.cl/api/factronica_boleta_consultamasiva/respuestas/resultado.txt


```

