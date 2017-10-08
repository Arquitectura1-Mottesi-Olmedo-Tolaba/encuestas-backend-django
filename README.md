# ENCUESTAS BACKEND DJANGO

#PREPARACION DEL ENTORNO

Asumiendo Python 2.7.1x, instalar 

Entorno virtual

Vamos a crear un entorno virtual (también llamado un virtualenv) que aislará la configuración Python/Django con base en cada proyecto.

Asi que primero abrimos la terminal e instalamos VirtualEnv (para más info: https://gist.github.com/FarhadurFahim/73c0fad6350332cef7a653bcd762f08d)
-> sudo apt-get install python-pip
-> sudo pip install virtualenv 

Dentro del directorio .../encuestas-backend-django vamos a crear el entorno virtual con la siguiente sintaxis:
virtualenv nombreParaTuEscritorio
-> virtualenv env

Eso crea un al entorno virtual y deberias ver caomo en la terminal aparece algo similar a esto:
(env) nombreUsuario:~/.../encuestas-backend-django
Ahora queda instalar la dependencias del proyecto:
-> pip install -r requirements.txt

Y lanzar el proyecto:
-> python manage.py runserver





 



