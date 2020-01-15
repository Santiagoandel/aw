# Instalar apache 2 
Para ello usaremos el comando apt-get install apache 2
Si no funciona usaremos este comando "fuser -vki /var/lib/dpkg/lock" y volveremos a intentar descargarlo

# Configurar apache 2
Una vez descargado iremos a este directorio "cd /var/www" y crearemos dentro las carpetas example.com y test.com, dentro de cada una crearemos una carpeta que se llame public_html y dentro editaremos con el comando "nano index.html" un html (en este caso un html que se llama index)

Despues, iremos a "/" y con el comando "cp /etc/apache2/sites-available/000-default.conf /etc/apache2/sites-available/example.com.conf" copiaremos el fichero 000-default.conf en la carpeta de example.com  y despues en la carpeta test.com.conf

Ir a la carpeta /etc/apache2/sites-available y alli editar el fichero con "nano  example.com.conf" y añadir estos parametros;
    	Servername example.com
    	ServerAlias www.example.com
    	DocumentRoot /var/www/example.com/public_html
y lo mismo con el fichero test.com.conf en el que añadiremos los mismos parámetros pero sustituyendo example por test.


