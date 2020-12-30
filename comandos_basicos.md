# Comandos basicos de Git y Github 

### Comandos especial para mostrar las ramas

~~~

git config --global alias.superlog "log --graph --abbrev-commit --decorate --date=relative --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all"

~~~

### Crear una rama

~~~
$ git checkout -b 'nombre de la rama'
~~~

### Borrar una rama

~~~
$ git branch -d 'nombre de la rama'
~~~

### Borrar la carpeta de git de un proyecto

~~~
$ rm -rf .git
~~~

### Rectificar el último commit realizado

~~~
$ git commit -am "Descripcion del commit" --amend
~~~


____

# Workflow - Proyectos creados pot ti - Repositorios personales

1. Crear usuario 
2. Crear un repositorio
3. Conectar con llave SSH a Github, desde tu área local.

~~~
$ ssh-keygen -t rsa -b 4096 -C "[email de Github]"

Dar enter. Aceptar la localización por defecto

Contraseña

$ cd ~/.ssh

$ cat id_rsa.pub

Copiamos la llave y la pegamos en Settings > SSH, dentro de Github
~~~

4. Iteración básica en tu área local y subir a Github
~~~
$ git init

$ git remote add origin [SSH]

$ git remote -v

$ git commit -am "[Mensaje]"

$ git push origin master
~~~

# Workflow - Proyectos creados por tu organización o equipo

~~~
$ git remote add origin [SSH]

$ git fetch origin 

$ git merge origin/master

*** Desarrollamos ***

$ git fetch origin 

$ git merge origin/master

$ git push origin master
~~~

# Workflow - Proyectos de terceros (Repositorios Forked)

Crear o entrar a la carpeta del proyecto

~~~
$ git remote add origin [HTTPS o SSH del proyecto]

$ git remote add upstream [HTTPS o SSH del proyecto principal]

$ git fetch origin

$ git merge origin/master

$ git fetch upstream

$ git merge upstream master

*** Hacer cambios en local ***

$ git fetch upstream

$ git merge origin upstream

$git push origin master

___

$ git pull request
~~~