# comandos_GIT
Repaso de apuntes de GIT año 2015
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

