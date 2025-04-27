# Pg2-practica2

Pge2.pracica22

# Uso de Django

Repositorio de ejemplo para el uso de Django en un proyecto de desarrollo web.

### Crear entorno virtual

```
python -m venv venv
```

### Activar entorno virtual

`````
# Windows

.\env\Scripts\activate

# Linux

````python
 source env/bin/activate
`````

### Instalar dependencias

```
pip install -r requirements.txt
```

### Crear proyecto Django

```
django-admin startproject practica2
```

### Aplicar migraciones

```
python manage.py migrate
```

### Iniciar servidor

```
python manage.py runserver
```

### Crear superusuario

```
python manage.py createsuperuser
```

### Crear aplicación

```
python manage.py startapp libros
```

### Agregar aplicación a settings.py

```
INSTALLED_APPS = [
...
'libros',
]
```

### Crear modelo

Escribe el modelo en `libros/models.py:`

```
from django.db import models

class Autor(models.Model):
nombre = models.CharField(max_length=100)
fecha_nacimiento = models.DateField()

    def __str__(self):
        return self.nombre

class Libro(models.Model):
titulo = models.CharField(max_length=100)
autor = models.ForeignKey(Autor, on_delete=models.CASCADE, related_name="libros")
fecha_publicacion = models.DateField()

    def __str__(self):
        return self.titulo
```

### Crear migraciones

```
python manage.py makemigrations
```

### Aplicar migraciones

```
python manage.py migrate
```

### Configurar admin.py

Escribe el siguiente código en `libros/admin.py:`

```
from django.contrib import admin
from .models import Autor, Libro

admin.site.register(Autor)
admin.site.register(Libro)
```

### Iniciar servidorf

```
python manage.py runserver
```

### Acceder al panel de administración

<p>Abre tu navegador y ve a  [http://localhost:8000/admin/.]  Inicia sesión con el superusuario que creaste anteriormente. Deberías ver las opciones para agregar autores 
y libros.

# practica

despues de activar el entorno virtual descargamos XAMMP y abrimos de apache e entorno virtual Djiango y creamos usuario y libros

https://github.com/jhon-escobar/Pg2-practica2/blob/fb998c76012ccef5ded4855bf8cd63bc26606773/imagen/djiango.png
![imagen](https://github.com/jhon-escobar/Pg2-practica2/blob/fb998c76012ccef5ded4855bf8cd63bc26606773/imagen/djiango.png)
