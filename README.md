# TELEMÁTICA PROYECTO FINAL

# Datos del autor
Nombre: Manuela Hernández Ríos
ID: 000196974
# Nombre de la aplicación:
COVIMAPS
# Descripción:
Permite a los usuarios de la red poner información sobre su experiencia con la enfermedad Covid-19 (si la ha tenido o no) junto con su ubicación geográfica, así como visualizar la información de personas contagiadas. De esta manera se podrá documentar si la zona en donde se encuentra el dispositivo puede ser considerada una zona de riesgo y decir qué probabilidad estimada hay de contagio. Además, cuenta con la función de graficar un mapa de la ciudad con número de casos confirmados. 
# Distribución:
Está compuesta por 3 pantallas. La primera tiene un menú donde el usuario puede elegir qué operación desea realizar: registrar su información, ver el mapa o salir. En la segunda, el usuario puede escribir su información personal (consta de 8 campos e incluye la localización gps del dispositivo), la cual es llevada al servidor web y se registra en la base de datos destinada. Finalmente, en la tercera pantalla se grafica el mapa de la zona, el cual estará en la página del sitio web alojado en el servidor. 
# Arquitectura
App móvil con una interfaz gráfica interactiva con el usuario, para recopilar y mostrar los datos.
Sitio web: archivos en python u otros, con acceso a base de datos.
Contenedores. 
# Árbol de carpetas del sitio
/send_data: recibe la información ingresada por los usuarios desde la app.
/visor_mapa: grafica y muestra el mapa de la zona.
# Conclusiones
Están pendientes de acuerdo con la evolución y la finalización del proyecto.
