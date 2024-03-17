# Aprende a usar Django

Aprende todos los comandos necesarios para usar django.

## Comandos consola
Recordar que primero debemos tener nuestra carpeta de origen, donde se guardara tanto nuestro proyecto, como nuestra maquina virtual (La cual es necesaria)

### 1. Instalar nuestra maquina virtual
```
py -m pip install virtualenv
```
o
```
pip install virtualenv
```

### 2. Ahora crearemos nuestra maquina virtual
Estar ubicado correctamente en el directorio donde crearemos la maquina virtual y posteriormente nuestro proyecto.
```
py -m virtualenv venv
```
Se recomienda llamarla 'venv', aunque le puedes poner otro nombre.

### 3. Activar nuestra maquina virtual
Para activarla necesitaremos hacerlo en dos pasos.
Debemos ir a la ubicacion donde se encuentra el activador de la maquina virtual, normalmente el codigo sera.
```
cd .\venv\Scripts
```
Y luego escribiremos el codigo.
```
.\activate
```
Nos aparecera el nombre de la carpeta de la maquina virtual en nuestro directorio de la terminal, con eso sabremos que se encuentra activada la maquina virtual.

### 3.1 Para desactivar nuestra maquina virtual escribiremos en la consola
```
deactivate
```

### 4. Instalar Django
```
pip install django
```

### 5. Crear la carpeta donde se guardara la configuracion del proyecto
RECORDAR ESTAR EN EL DIRECTORIO CORRECTO A LA HORA DE CREAR EL PROJECTO.
```
django-admin startproject mysite
```
La mejor forma de nombrar esta carpeta es como "Base", "Main", el mismo nombre que usamos para la carpeta donde esta guardado el proyecto, o ponerle un nombre mas especifico de lo que sera el proyecto.

### 6. Ahora crearemos la carpeta donde se alojara nuestro proyecto
```
python manage.py startapp proyecto
```
Ponerle el nombre adecuado segun los archivos que estaran en dicha carpeta.

### 7. Generar las tablas de nuestra base de datos (No se recomienda hacerlo, hasta no tener todo el proyecto configurado, mas abajo se muestra como configurarlo)
```
python manage.py makemigrations
```
```
python manage.py migrate
```

### 8. Crear el usuario administrador del proyecto
Es llamado super user, ya que tiene la ventaja de entrar al entorno de administracion de Django, el cual se entra escribiendo al lado de la url del server local "/admin"
```
python manage.py createsuperuser
```

## Configurar nuestro proyecto
Se recomienda configurarlo antes de crear las migraciones de los modulos.

### 1. Gestionar las carpetas donde se alojara nuestro proyecto, en las configuraciones
Iremos al archivo "settings.py" que se encuentra en la carpetadonde iniciamos nuestro proyecto (Punto 5 de los comandos), una vez alli, iremos al apartado de "INSTALLED_APP", alli siguiendo el formato escribiremos el nombre de las carpetas donde se alojaran nuestro proyecto (Punto 6 de los comandos), recordar poner el nombre exacto de la carpeta.









