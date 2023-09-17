# Bienvenida al curso básico de Git y Github
Bienvenido al curso básico de Git y Github, En esta sección del curso crearemos una cuenta en Github para
luego configurar nuestro Git en el equipo. Posterior a estas acciones se realizaran todas las
configuraciones básicas necesarias para poder trabajar y mantener actualizado nuestro proyecto. Finalmente
veremos aspectos de *Markdown* que mejoran y facilitan la lectura de la documentación. 

# Crear cuenta en Github.
Para crear una cuenta en Github debemos dirigirnos a la siguiente url.

[https://github.com/](https://github.com/)

Una vez nos encontramos en la página debemos dar clic en *sign up*

![Home-de-Github.com](/Curso_Básico/Presetación/images/Github1.png)

Luego deberemos llenar los siguientes campos:
- E-mail
- Contraseña
- Username

![Imagen-Registro](/Curso_Básico/Presetación/images/Github2.png)

Posteriormente nos solicitara datos adicionales los cuales debemos rellenar por preferencia.

Señalar que Github hoy en día funciona como una red social en la cual se pueden editar campos como:

- Foto de perfil
- Biografía
- Añadir url personal
- Redes sociales

![Imagen-de-mi-perfil](/Curso_Básico/Presetación/images/PerfilGithub.png "Foto de mi perfil")

# Configuración de e-mail y nombre en Git.
Primero que todo debemos instalar git en nuestro equipo, esto dependerá de que sistema operativo contemos.
Una vez identificado nuestro sistema operativo nos dirigiremos a la siguiente web:

[https://git-scm.com/](https://git-scm.com/)

ya en la web nos dirigimos a descargar el software que corresponda a nuestro sistema operativo.
Tenemos dos formas de hacerlo haciendo clic en *download* o haciendo clic en la pantalla que
debería reconocer nuestro sistema operativo.

![imagen-web-github](/Curso_Básico/Presetación/images/Git1.png)

![imagen-de-download](/Curso_Básico/Presetación/images/Git2.png)

Una vez finalizada la instalación se nos abrirá la terminal y los parámetros básicos a configurar
son el nombre y el correo electrónico.

Para añadir tu nombre a git debemos escribir el siguiente comando y este debe ser reemplazado por tu nombre

`$ git config --global user.name "Carlos Carrasco"`

![imagen-git-nombre](/Curso_Básico/Presetación/images/Git-Nombre.png)

Una vez agregado el nombre debemos agregar nuestro correo electrónico que es el mismo con el que 
creamos nuestra cuenta en Github.
 
`$ git config --global user.email carlos.carrasco@example.com`

![imagen-git-email](/Curso_Básico/Presetación/images/Git-Email.png)

finalizado este proceso estamos en condiciones de generar nuestra Key SSH

# Generar Key para actualizar mediante SSH.

Este proceso es muy importante ya que nos brindara mayor seguridad a la hora de actualizar nuestro repositorio.
La documentación oficial es bastante clara. Si estas en Linux o Mac es sencillo solo debes seguir los pasos que dejo a continuación. En el caso que te encuentres trabajando con sistema operativo de Windows te sugiero que habras la aplicación de git para realizar este proceso.

1. Abrir la terminal
```
$ ssh-keygen -t ed25519 -C "your_email@example.com"
```
Si el proceso a finalizado con éxito la terminal debería arrojarnos lo siguiente:
```
$ Generating public/private ALGORITHM key pair.
```
Luego nos consultará el lugar donde queremos almacenar nuestro archivo por lo que en mi caso fue la ruta establecida:
```
Enter a file in which to save the key (/home/YOU/.ssh/ALGORITHM):[Press enter]
```
2. Ingresar contraseña
Es importante darle una contraseña ya que esta la solicitará cuando querramos pushear un cambio a github.
En la terminal debería aparecer lo siguiente:
```
> Enter passphrase (empty for no passphrase): [Type a passphrase]
> Enter same passphrase again: [Type passphrase again]
```
3. Evaluar si esta corriendo el proceso
Para ejecutar el siguiente paso tenemos que evaluar que este corriendo el proceso
```
$ eval "$(ssh-agent -s)"
> Agent pid 59566
```
Si el proceso arroja **Agent pid XXXXX** cualquier número, eso quiere decir que vamos por buen camino.

4. Agregar la contraseña al archivo
En esta parte debemos agregar la contraseña que previamente habíamos creado
```
ssh-add ~/.ssh/id_ed25519
```
Si el proceso a funcionado correctamente ya estamos listos para agregar nuestra *Key Ssh* en Github.



[Documentación oficial](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

# Crear tu primer repositorio con Git.

# Subir repositorio a Github.

# Sincronizar tu repositorio desde Github.

# Introducción a Markdown
