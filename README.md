# TELEMÁTICA PROYECTO FINAL 2020

# Datos del autor
Nombre: Manuela Hernández Ríos
ID: 000196974
# Nombre de la aplicación:
COVIMAPS

# Descripción:
Es un servidor de página web basada en contenedores el cual ofrecerá información en tiempo real acerca de los casos locales de covid-19 (dependiendo de la ubicación del usuario en la localidad especificada) y mediante métodos algorítmicos le informa al usuario el número de casos que hay en una zona de Medellín. Los lenguajes que se usarán para la app web serán python, html y SQL (la interfaz gráfica es una página web con html)

# Arquitectura
 # readme.md: 
 contiene la información general del funcionamiento de la página.
 # Dockerfile
 Este archivo directamente relacionado con el contenedor se encargará de ejecutar las instrucciones necesarias al momento de montar al servidor. Levantará los servicios necesarios y ejecutará el .py por debajo de memoria (Este archivo no se implementó en la entrega final)
 # index.html
 Este archivo de hipertexto (estará en un directorio llamado templates)contendrá la interfaz de entrada que verá el usuario. Acá se obtendrán los datos del usuario como el nombre y la edad, incluyendo su localización actual y si ha tenido covid-19; y se redireccionará al archivo bdtesting.py
 # bdtesting.py
 Acá se contendrá el cuerpo del proyecto (se utilizará la librería flask de python y dash para la graficación). En este archivo se obtendrán los datos enviados por el index.html mediante el método POST y a partir de estos se buscará en las bases de datos la información de los casos covid-19 de la localidad para realizar el gráfico y el análisis por zonas. Si según los datos ingresados, el usuario tiene covid-19 o sospecha de ello, entonces su información se añadirá a la base de datos. (Se implementaron dos bases de datos: la primera es una base de datos basada en una hoja de cálculo dada por el municipio y la otra es una base de datos en sqlite3 que almacena las localizaciones de las personas con covid-19 que ingresan a la página)
 # BaseDatos2.db
  Esta base de datos tendrá la información de los casos confirmados de covid-19 dadas por los usuarios que ingresen a la página.
 # BaseDeDatosValleDeAburra100%realNoFake.xlss
  Esta hoja de cálculo contiene las ubicaciones de los casos confirmados de covid-19 dados por el municipio (un dummy data)
 # Contenedor en docker
  En el contenedor se almacenarán los archivos ya mencionados en el ubuntu que se usará para el servicio (se tendrá ya instalados el flask, dash para graficar el mapa, el pip y la versión python que se necesitan para soportar el servicio). Así al momento de levantar una imagen en memoria lo único que se hará es levantar el servicio (No fue implementado en el proyecto final)
 # Tipo de servidor y Firewall
  La página web funcionará en un servidor web http (Se usará la librería flask de python para soportar la página). Se usará el ufw como el firewall del sistema habilitando el puerto 80. Como el servicio se va a montar en una red de servidores en la nube(como AWS), se activa el puerto 22 y se harán las configuraciones de los grupos de seguridad respectivos. El SO que se va a usar es un Ubuntu Server 18.04
