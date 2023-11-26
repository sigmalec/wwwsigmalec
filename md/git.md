---
layout: default
title: referencia rapida de git
fecha: 2023-11-23
---

# git


&nbsp;
## 1 que es github
Software de control de versiones creado en 2005 por Linus Torvalds, para trabajar con varios desarrolladores en el núcleo de Linux.
**git** rastrea el contenido y permite revertir y regresar a una versión anterior del código.

### conceptos
- **rama**, copia independiente del codigo que puede cambiarse y luego integrarse, o no
- **repositorio**, proyecto con multiples archivos, hay 3 de referencia,
    - github, de microsoft
    - gitlab, de gitlab
    - bitbucket, de atlassian

&nbsp;

## 2 instalacion de git
En RockyLinux (RedHat, CentOS),

    yum install -y git
    git --version
    git config --global user.name "nombre_usuarios_defecto_guardar_el_trabajo"
    git config --global user.mail "email_defecto"

&nbsp;

## 3 comenzar cuando el repositorio está en línea
1. Una vez creado el repositorio en línea, obtener la URL para clonarlo localmente

       git clone URL

2. Una vez editados los cambios localmente, revisar estado

       git status

3. Añadir los archivos que están listos para integrarse en el repositorio

       git add NOMBRE_ARCHIVO

4. Integrar los archivos en el repositorio local

       git commit -m "MENSAJE DESCRIPTIVO CAMBIO"

5. Obtener nombre del repositorio en línea (por defecto origin)

       git remote

6. Enviar ficheros a la rama "master" del repositorio en línea "origin"

       git push origin master

7. Descargar ficheros de la rama "master" del repositorio en línea "origin"

       git pull origin master

&nbsp;

## 4 comenzar creando un repositorio local y luego enviándolo a un repo en línea

1. Ubicados en el directorio que contendrá los ficheros, iniciar el repositorio git

       git init

2. Revisar estado del repositorio

       git status

3. Añadir ficheros

       git add .

4. Integrar ficheros en el repositorio local

       git commit -m "MENSAJE"

5. Se crea el repositorio remoto, se obtiene su URL y se añade al proyecto git con el nombre "origin" (por defecto)

       git remote add origin URL

6. Se listan los repositorios remotos vinculados al proyecto (debe aparecer "origin" o el nombre que se haya dado)

       git remote

7. Se envian los ficheros a la rama master

       git push origin master
