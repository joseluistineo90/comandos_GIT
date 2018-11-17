# comandos_GIT
Repaso de apuntes de GIT año 2018 . (Fuente https://trello.com/b/tbkg45FJ/git-github )
******************************************************************************************************
GITHUB: es el facebook de los coders, es opensource si veo un ícono de un ojo y el texto NOT WATCHING // indica no seguir el repositorio,
watching// notifica cambios en el proyecto
ignoring // ignora los cambios del repositorio.
la estrella es para añadir a favoritos.

git clone jquery // baja el framework jquery y también podemos pasar un repositorio de local a remoto PUEDO CLONAR COPIANDO EL HTTP o el HSS directamente de github.

Conviene colocar el mismo nombre a la carpeta y al repositorio ademàs de comenzar creando el repositorio primero. Si la carpeta no tiene archivos no se ve nada en github.

git remote add origin (http.....de github) // conecta nuestro proyecto local con el remoto desde cònsola.

git remote -v // muestra el origin y el fetch, osea muestra cómo se encuentra el remote en su conección.

git remote remove origin // quita la conexión del remote.

git push origin master // pasa la rama master a github, luego nos pide el user y la clave para subir los cambios, recargo github y lo veré cargado listo para contribuciones. ojo con la rama en que esté trabajando, si tengo varias abro en github la que corresponde y observo sus commits.

ISSUES : parte de github que permite mejorar o solucionar errores o cosas pendientes del repositorio, lo creo en github, describo lo que harè (es colaborativo) es como comentar opiniones tipo chat.
con staying with markdown is supported tendremos la posibilidad de añadir interactividad al código tipo preview, para marcar y colorear los issues.

MILESTONES: Son grupos de issues que aplican para un proyecto con perìodo de caducidad tipo TRELLO, engloba a todos los issues y los ORGANIZA, aparece en la pestaña de issues y se crean con su nombre.

LABELS: aparece como pestaña en la ventana de issues, organizan con etiquetas de colores los distintos problemas que podamos encontrar en los issues , se pueden editar como en TRELLO.
Tambièn podemos asignar usuarios a los issues.


Crear una carpeta para tu proyecto y colocar archivos
Entonces, estando en una carpeta de tu ordenador donde hemos dicho que vamos a crear todos nuestros repositorios, puedes crear una carpeta específica para tu primer proyecto con Git. La carpeta de tu proyecto la puedes crear con el explorador de archivos o si quieres por línea de comandos, es indiferente.

Una vez creada tu carpeta puedes crear archivos dentro. Como estamos hablando de desarrollo de software, los archivos que meterás dentro de tu carpeta contendrán el código de tu aplicación, página web, etc.

Nota: Para crear los archivos, en el flujo de trabajo común de un desarrollador usarás tu editor de código preferido: Eclipse, Sublime Text, Komodo, Notepad++, Gedit, PhpStorm, etc. Como prefieras. También, por supuesto, puedes crear tu archivo por línea de comandos y editarlo si estás en Linux con el conocido Vim o cualquier otro editor de interfaz solo texto.
Inicializar el repositorio Git
Para crear tu repositorio Git, donde monitorizamos los archivos de un proyecto, tienes que realizar una operación previa. Es la inicialización del repositorio Git que queremos crear en la carpeta de tu proyecto y es una operación que deberás realizar una única vez para este proyecto.

Nota: Cada proyecto lo tendrás en una carpeta distinta y será un repositorio independiente. Esta operación de inicialización de tu repositorio, por tanto, la tendrás que realizar una única vez para cada proyecto que quieras controlar sus versiones por medio de Git.
Así pues, antes que nada (antes de enviar cualquier archivo al repositorio), creo el repositorio Git con el comando "git init".

git init

Una vez has inicializado el repositorio, podrás observar que se ha creado una carpeta en tu proyecto llamada ".git" . Si ves esa carpeta en tu proyecto es que el repositorio se ha inicializado correctamente y que ya tienes convertida esa carpeta en un repositorio de software Git.

Nota: Los archivos o carpetas en Linux / Mac que comienzan por un punto están ocultos en el sistema de archivos. Para verlos tendrás que ejecutar el comando "ls -la".
En la carpeta .git es donde se va a guardar toda la información relativa al repositorio. Resultará obvio, pero conviene decir que nunca se debe borrar esa carpeta y tampoco deberíamos acceder de forma directa a sus contenidos, ya que nos vamos a comunicar siempre con el repositorio por medio de comandos.

Guardar los archivos en el repositorio (commit)
Una vez que crees tus primeros archivos, puedes comenzar a trabajar con Git, enviando esos ficheros al repositorio. Aunque los archivos estén en la carpeta de tu proyecto y hayas iniciado el repositorio Git previamente, el sistema de control de versiones no los está monitorizando, por lo que a nivel de tu repositorio Git todavía es como si no estuvieran.

A esa acción de guardar los archivos en el repositorio se llama, en la jerga de Git, hacer un "commit". En este caso el commit lo estás haciendo en local, porque los archivos los estás enviando a tu repositorio local que tienes en tu máquina.

Un commit en Git se hace mediante dos pasos.

1) Tengo que añadir el fichero a una zona intermedia temporal que se llama "Zona de Index" o "Staging Area" que es una zona que utiliza Git donde se van guardando los ficheros que posteriormente luego se van a hacer un commit.

Cualquier archivo que quieras mandar a la zona de index lo haces con el comando "add".

git add nombre-del-fichero

Una vez añadido podrías ver que realmente tienes ese fichero en el "staging area", mediante el comando "status".

git status

Verás que, entre las cosas que te aparecen como salida de ese comando, te dice que tienes tu fichero añadido como "new file". Además te dice que estos cambios están preparados para hacer commit.

2) Tengo que enviar los archivos de la zona de Index al repositorio, lo que se denomina el commit propiamente dicho. Lo haces con el siguiente comando:

git commit -m "mensaje para el commit"

Con esto ya tenemos nuestro primer archivo dentro del repositorio. A partir de aquí podremos mantener y controlar los cambios que se hagan sobre este archivo (u otros que hayamos incluido por medio del commit).

Si haces de nuevo un comando "git status" podrás comprobar que no hay nada para enviar al repositorio. Eso quiere decir que la zona de Index está limpia y que todos los cambios están enviados a Git.

Hasta este punto hemos podido aprender a crear nuestro repositorio y enviar los primeros cambios por medio de la operación de commit. Ahora puedes probarlo en tu sistema para comenzar a experimentar Git. En las siguientes entregas continuaremos explorando el flujo de trabajo con Git, y mejorando esta primera aproximación con nuevos comandos que te permitan hacer mas cosas y facilitarte el trabajo resumiendo las operaciones ya comentadas en menos pasos.

Editar - Eliminar
jose 6 de mar. de 2016 a las 19:57 (editado)
Antes que nada, inmediatamente después de instalar Git, lo primero que deberías hacer es lanzar un par de comandos de configuración.

git config global user.name "Tu nombre aquí"
git config global user.email "tu_email_aquí@example.com"

Con estos comandos indicas tu nombre de usuario (usas tu nombre y apellidos generalmente) y el email. Esta configuración sirve para que cuando hagas commits en el repositorio local, éstos se almacenen con la referencia a ti mismo, meramente informativa. Gracias a ello, más adelante cuando obtengas información de los cambios realizados en el los archivos del "repo" local, te va a aparecer como responsable de esos cambios a este usuario y correo que has indicado.
Git es la tecnología para hacer el control de versiones y GitHub simplemente es un hosting de repositorios Git, con una interfaz web que nos ofrece algunas utilidades basadas en el propio control de versiones Git.

En GitHub puedo tener repositorios diversos y si quiero trabajar con alguno de ellos, primero debo tenerlo en local. Ojo, no necesitamos tener todos los repositorios que has publicado en GitHub en local, solo aquellos con los que vayamos a trabajar. En el momento que los tenemos en local podremos hacer cambios, almacenarlos en nuestro repositorio local y cuando lo juzguemos oportuno, enviarlo (empujar, push) a tantos servidores o repositorios remotos como queramos
***********************************************************************************************************
ojo no usar acentos. no jugar con la conexión una vez hice un git remove y me costó entrar.
pwd // me permite ver la ruta por default en donde me encuentro.

git config --list //muestra la configuración de GIT en mi PC.

ls // muestra la lista de files de la ruta por defecto.

cd // sirve para cambiar de directorio por ejemplo para ubicarme en Desktop.

mkdir // crea un directorio por ejemplo mkdir pinocho, con las teclas de cursor arriba y abajo me desplazo entre los folders.

touch index.html // con touch agrego un archivo a mi directorio creado, no debo subir a github repositorios con folders vacíos.

ssh // es la llave pública o privada para conectarme a github. suele crear un archivo con extención .pub y el comando es ssh-keygen, copio esa llave de local y crea la llave en github. Con el comando cd~/.ssh verifico si tengo llave.
crear llave desde cónsola puedo hacerlo así:
ssh-keygen -t rsa -C "mi correo fe github" // busco el archivo .pub que me genere, le doy enter y coloco el password, lueo creo una llave desde github.

FORK: en github sirve para proyectos colaborativos me clona pero dentro de Github no en local, para hacerlo en local uso git clone.

PULL REQUEST: me permite compartir los cambios que haya yo hecho a código ajeno y ver si me los aceptan. con ello le decimos AL DUEÑO, Epa tengo Algo, mira a ver si te sirve.

staged : (preparado) // significa que el proyecto tuvo cambios desde que se obtuvo el repositorio y fue añadido al área de preparación .
modified // tuvo cambios desde que se obtuvo del repositorio pero no ha sido preparado.
GLOBAL SETUP // Una vez confiurado no se vuelve a tocar , a menos que deseemos reconfigurarlo con otro user e email.

README: es bueno colocar un README para que quienes vean nuestros repositorios sepan de qué va la cosa., los creamos desde cónsola o directamente desde github, su extensión es readme.md, se veran no en teto plano sino como html.

lo que elimine de mi código se verá en color rojo y con sino menos y lo que agreue con un signo más adelante y en color verde

COMANDO BASICO E IMPORTANTES
rm -rf css //me elimina el archivo css sin dejar ni rastro.
git --version // permite saber si tenemos git instalado y cuál es su versión.
1) Creo primero mis archivos locales o folders
2) git init // desde la cónsola, para marcar el inicio del proyecto, git monitorea los cambios, éste comando se usa 1 sola vez.
3) git status // muestra el estado del proyecto, qué cambios agregamos al mismo.
4) git add -A // Agrega todos los archivos, tambien podemos agregarlos con su nombre de uno en uno ejemplo gitt add -index.html
5) git clear // limpia la pantalla.
6) git exit //sale de la cónsola.
7) git commit -m "nombre del commit" // especifico què cambios hice en el nombre del commit.
8) git log // nos da una lista de todos los commits que hice.
9) git checkout // permite previo a añadir el código cifrado del commit, navegar entre su distintas versiones, tambièn se usa en las branches o ramas. Equivale a viajar en el tiempo del status del commit o la rama.
10) git checkout master // mueve al ùltimo commit que tenga.
11) git reset // borra los commits. CUIDADO con su uso.
git reset --soft// borra el commit sin tocar nuestro código.
git reset --mixed // borra el staging area, no toca nuestro código
git reset --hard. // BORRA TODO.
12) q // permite salir
13) git log > commit.txt // crea un archivo txt de nuestros commits, útil para seleccionar el cifrado de cada commit.
14) git help // ayuda de comando con su documentación, si no se el uso de alguno allí lo detalla.
15) git branch // muestra las ramas le coloca un símbolo *
16 )git branch pinocho // crea la rama pinocho
17) git checkout test // navega y se posiciona en la rama test.
18) git branch -D test // me borrarìa la rama test.
19) git checkout -b Testing // crea la rama testing y se posiciona en ella.
20) git clone jquery // nos baja el framework jquery y también podemos pasar un repositorio de local a remoto.
21)git remote add origin (http.....de github) // conecta nuestro proyecto local con el remoto desde cònsola.
22) git remote -v // muestra el origin y el fetch, osea muestra cómo se encuentra el remote y su estado de conexión.
23)git remote remove origin // quita la conexión del remote.
24) git push origin master // pasa la rama master a github, luego nos pide el user y la clave para subir los cambios, recargo github y lo veré cargado listo para contribuciones.
25)git commit --amend -m "hice un cambio en el h3" // sirve para corregir un commit, en èste caso el título en HTML.
26)git push origin master -f // fuerza a que se suban los cambios del commit si estos fuesen los mismos, así evitamos que github lo rechace por ser un commit repetido. coloco user contraseña y listo.
27)git tag -a v1.0 -m "mensaje" // tipo de tag anotada con su mensaje
28)git tag v1.0 // tipo de tag ligera no lleva inormaciòn como las tags anotadas.
29)git tag -a v1.0 -m "mensaje" (aquí coloco su código SSH, lo copio desde git log) // al agregar el código SSH podemos especificar dónde se va a aplicar una etiqueta
30)git push origin v1.0 // no coloco origin master sólo la versión del tag. luego clave y usuario
31)git push origin --tags // sube todos los tags luego user y clave recargo github y listo.
32) git branch -a // muestra todas las ramas incluidas la origin master espejo que está oculta.
33) git fetch origin // permite pasar el cambio de la rama master remota de Omar al espejo o rama oculta origin master.
34) git merge origin/master // con ello fusionaré el commit de omar con el de Filiberto creando un nuevo commit.
35) git push origin master // para subir
36) git branch gh-pages // Todo lo que esté en ésta rama se ubicará dentro del dominio como nuestro sitio web gratuito
37) git push origin gh-pages // colocamos user y clave para subirlo de local a remoto en github a nuestra nueva rama gh-pages.
para ver nuestro nuevo sitio web escribimos su URL así jose.github.io/mirepositorio
38) git pull origin master // me permite actualizar los cambios que haga en github en mi cónsola local.
39) git clone ~/pinocho pinochoclonado// cre un clon en local de mi repositorio
40)git diff // verifica la diferencia de los commits.
41)cat archivo1.txt // nos da todos los cambios de nuestro proyecto.
42) rm -r carpeta/.git // Borra toda la carpeta.
43) ls -rf // muestra todos los archivos , inclusive los ocultos.
44) git checkout 6123d8 // con los 6 primeros números del commit , me posiciono sobre el de primero para poder decidir que hacer con ese commit, modificarlo borrarlo etc.

