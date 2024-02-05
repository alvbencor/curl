![Logo Curl](img/curlLogo.png)

---
### Index

- Que es curl
- [Sintaxis básica](#comandosBasicos)
- [Funciones comunes](#comandosComunes)
---
  
## ¿Que es curl? ##
**curl** es una herramienta de línea de comandos utilizada para realizar transferencias de datos a través de diferentes protocolos de red. Su nombre proviene de la frase "Client for URLs" (Cliente para URLs). Curl es compatible con una amplia variedad de protocolos, incluyendo HTTP, HTTPS, FTP, FTPS, SCP, LDAP, y más.

Con curl, los usuarios pueden realizar solicitudes a servidores web y descargar o enviar datos desde y hacia ellos. Es muy versátil y puede ser utilizado para probar conexiones, automatizar tareas relacionadas con la web, y realizar diversas operaciones de red directamente desde la línea de comandos. 

Además, curl es de **código abierto** y está disponible en varios sistemas operativos, incluyendo **Linux**, **macOS** y **Windows**.

Puedes consultar el manual directamente en la consola con las siguientes opciones: 

### Obtener el manual de curl en consola:

        man curl

### Descargar el manual de curl en un archivo desde la consola:

        man curl >> manualCurl.txt


---

<a name="comandosBasicos"></a>

### Sintaxis básica

        curl <URL>
        
Donde <URL> es la dirección del recurso al que deseas realizar la solicitud. Esto podría ser una página web, una API, o cualquier otro recurso accesible a través de HTTP.

### Descargar un archivo desde la web

        curl -o nombre_archivo.extension https://www.ejemplo.com/archivo.extension
        
Esto descargará el archivo desde la URL proporcionada y lo guardará con el nombre especificado.

### Especificar URLs en las solicitudes

Puedes especificar la URL directamente en el comando curl para realizar solicitudes a recursos específicos. Por ejemplo:

        curl https://api.ejemplo.com/datos
        
Uso de banderas para configurar la URL

Puedes utilizar diferentes banderas con curl para configurar la URL y la solicitud. Algunas banderas comunes incluyen:

**-X** para especificar el **método HTTP (GET, POST, etc.)**.

**-H** para **agregar encabezados** a la solicitud.

**-d** para enviar datos en una solicitud **POST**.


---
<a name="comandosComunes"></a>

## Comandos básicos

### Solicitud GET
        curl https://www.ejemplo.com

### Solicitud GET y guardarla en un archivo
        curl -o archivo_salida.html https://www.ejemplo.com
### Realizar una solicitud POST con datos
        curl -X POST -d "parametro1=valor1&parametro2=valor2" https://www.ejemplo.com/recursos
### Incluir encabezados en una solicitud
        curl -H "Encabezado1: Valor1" -H "Encabezado2: Valor2" https://www.ejemplo.com

### Realizar una solicitud con autenticación básica
        curl -u usuario:contraseña https://www.ejemplo.com/recursos

### Seguir redirecciones
        curl -L https://www.ejemplo.com
### Mostrar solo las cabeceras de la respuesta
        curl -I https://www.ejemplo.com

### Establecer un límite de tiempo para la solicitud
        curl --max-time 10 https://www.ejemplo.com
### Enviar un archivo en una solicitud post 
        curl -X POST -F "archivo=@ruta/del/archivo.txt" https://www.ejemplo.com/subir

### Ver detalles de la solicitud y respuesta
        curl -v https://www.ejemplo.com
