## Configuración previa

Recuerda configurar las variables antges de hacer push

```
git config --global user.name "Your Name"
git config --global user.email "youremail@yourdomain.com"
git config --list
```

## Iniciando GitFlow

Crear el branch `develop` a partir del branch `master`:

`git branch develop`

Ubicar en la rama develop:

`git checkout develop`

Subir el branch develop al repositorio remoto:

`git push -u origin develop`

## Crear un nuevo Feature

Cargar el Git Bash.en la carpeta donde se descargara el proyecto.

Clonar la rama develop del proyecto

`git clone -b develop https://github.com/ntt-data-microservice/spring-banca.git`

Ubicarme en la carpeta del proyecto

`cd spring-banca`

crear el Feature respectivo (Colocar tu nombre y apellidos)

`git branch feature/NombreYApellidos`

Cambiar al branch creado:

`git checkout feature/NombreYApellidos`

Subir el nuevo branch al repositorio remoto:

`git push -u origin feature/NombreYApellidos`

## Desarrollar codigo y subir cambios al feature

Ejecutar los siguiente comandos
```
git add .
git commit -m "Adding/Change new Entity NombresYApellidos"
git pull
git push -u origin feature/NombresyApellidos
```

## Realizar un Pull Request

Ingresar a la opción de Pull Request en el GitHub y crear un `New pull request`:

Seleccionar:

`base: develop  <--  compare: feature/NombresyApellidos`

y Luego hacer click en `Create pull request`

Colocar el Comentario respectivo y confirmar haciendo click en `Create pull request`

## Descargar desde el develop remoto al feature local

realizar la siguiente secuencia de pasos

```
git checkout develop
git pull
git checkout feature/NombresyApellidos
git pull
git merge develop
```

## Crear un Tag

Crear el tage de la versión 1.0.0

`git tag v1.0.0`

Verificar el tag creado:

`git log --all --decorate --oneline --graph`

Subir el tag creado:

`git push origin v1.0.0`








