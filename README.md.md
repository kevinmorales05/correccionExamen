**Examen del Primer Bimestre**

**Nombre:** Kevin Morales

**Fecha:** 2021/07/30

**Parte 1**

-   **Script Ejercicio 1 ORLANDO**

**#Orlando Juegos Olimpicos**

import couchdb

from tweepy import Stream

from tweepy import OAuthHandler

from tweepy.streaming import StreamListener

import json

###API ########################

ckey = \"C8gYxcJRD2ZuuQ2hnBKJvZzZm\"

csecret = \"I7RuUZi6VSKLZsLV0qwPjQK1Xmwf95FQPTdiMua6I21aCVfrwV\"

atoken = \"3550065256-xxGrQDuYC4YrDNtFNchfSyetoFmnhz4mjIhdnMh\"

asecret = \"99Wxr7Y4S5zpM4DRmnAYMiyd5qoWbypgypgXXc9bLx0LN\"

####################################\#

class listener(StreamListener):

def on_data(self, data):

dictTweet = json.loads(data)

try:

dictTweet\[\"\_id\"\] = str(dictTweet\[\'id\'\])

doc = db.save(dictTweet)

print (\"SAVED\" + str(doc) +\"=>\" + str(data))

except:

print (\"Already exists\")

pass

return True

def on_error(self, status):

print (status)

auth = OAuthHandler(ckey, csecret)

auth.set_access_token(atoken, asecret)

twitterStream = Stream(auth, listener())

\'\'\'========couchdb\'==========\'\'\'

server = couchdb.Server(\'http://kevin:12345\@localhost:5984/\')
#(\'http://115.146.93.184:5984/\')

try:

db = server.create(\'juegosolimpicos2\')

except:

db = server\[\'juegosolimpicos2\'\]

\'\'\'===============LOCATIONS==============\'\'\'

twitterStream.filter(locations=\[-81.409221,28.510477,-81.324077,28.561631\])

twitterStream.filter(track=\[\'juegosolimpicos\',\'carapaz\'\])

-   **Script Ejercicio 1 QUITO**

> #Quito Juegos Olimpicos
>
> import couchdb
>
> from tweepy import Stream
>
> from tweepy import OAuthHandler
>
> from tweepy.streaming import StreamListener
>
> import json
>
> ###API ########################
>
> ckey = \"C8gYxcJRD2ZuuQ2hnBKJvZzZm\"
>
> csecret = \"I7RuUZi6VSKLZsLV0qwPjQK1Xmwf95FQPTdiMua6I21aCVfrwV\"
>
> atoken = \"3550065256-xxGrQDuYC4YrDNtFNchfSyetoFmnhz4mjIhdnMh\"
>
> asecret = \"99Wxr7Y4S5zpM4DRmnAYMiyd5qoWbypgypgXXc9bLx0LN\"
>
> ####################################\#
>
> class listener(StreamListener):
>
> def on_data(self, data):
>
> dictTweet = json.loads(data)
>
> try:
>
> dictTweet\[\"\_id\"\] = str(dictTweet\[\'id\'\])
>
> doc = db.save(dictTweet)
>
> print (\"SAVED\" + str(doc) +\"=>\" + str(data))
>
> except:
>
> print (\"Already exists\")
>
> pass
>
> return True
>
> def on_error(self, status):
>
> print (status)
>
> auth = OAuthHandler(ckey, csecret)
>
> auth.set_access_token(atoken, asecret)
>
> twitterStream = Stream(auth, listener())
>
> \'\'\'========couchdb\'==========\'\'\'
>
> server = couchdb.Server(\'http://kevin:12345\@localhost:5984/\')
> #(\'http://115.146.93.184:5984/\')
>
> try:
>
> db = server.create(\'juegosolimpicos3\')
>
> except:
>
> db = server\[\'juegosolimpicos3\'\]
>
> \'\'\'===============LOCATIONS==============\'\'\'
>
> twitterStream.filter(locations=\[-78.527042,-0.264936,-78.486942,-0.199842\])
>
> twitterStream.filter(track=\[\'juegosolimpicos\',\'carapaz\'\])

-   **Script Ejercicio 1 GUAYAQUIL**

#Guayaquil Juegos Olimpicos

import couchdb

from tweepy import Stream

from tweepy import OAuthHandler

from tweepy.streaming import StreamListener

import json

###API ########################

ckey = \"C8gYxcJRD2ZuuQ2hnBKJvZzZm\"

csecret = \"I7RuUZi6VSKLZsLV0qwPjQK1Xmwf95FQPTdiMua6I21aCVfrwV\"

atoken = \"3550065256-xxGrQDuYC4YrDNtFNchfSyetoFmnhz4mjIhdnMh\"

asecret = \"99Wxr7Y4S5zpM4DRmnAYMiyd5qoWbypgypgXXc9bLx0LN\"

####################################\#

class listener(StreamListener):

def on_data(self, data):

dictTweet = json.loads(data)

try:

dictTweet\[\"\_id\"\] = str(dictTweet\[\'id\'\])

doc = db.save(dictTweet)

print (\"SAVED\" + str(doc) +\"=>\" + str(data))

except:

print (\"Already exists\")

pass

return True

def on_error(self, status):

print (status)

auth = OAuthHandler(ckey, csecret)

auth.set_access_token(atoken, asecret)

twitterStream = Stream(auth, listener())

\'\'\'========couchdb\'==========\'\'\'

server = couchdb.Server(\'http://kevin:12345\@localhost:5984/\')
#(\'http://115.146.93.184:5984/\')

try:

db = server.create(\'juegosolimpicos5\')

except:

db = server\[\'juegosolimpicos5\'\]

\'\'\'===============LOCATIONS==============\'\'\'

#twitterStream.filter(locations=\[-79.933971,-2.207867,-79.852672,-2.110707\])

twitterStream.filter(track=\[\'juegosolimpicos\',\'carapaz\'\])

![](media/image1.png){width="6.5in" height="3.65625in"}

**Parte 2**

-   **Script Ejercicio 2**

import couchdb

from tweepy import Stream

from tweepy import OAuthHandler

from tweepy.streaming import StreamListener

import json

###API ########################

ckey = \"C8gYxcJRD2ZuuQ2hnBKJvZzZm\"

csecret = \"I7RuUZi6VSKLZsLV0qwPjQK1Xmwf95FQPTdiMua6I21aCVfrwV\"

atoken = \"3550065256-xxGrQDuYC4YrDNtFNchfSyetoFmnhz4mjIhdnMh\"

asecret = \"99Wxr7Y4S5zpM4DRmnAYMiyd5qoWbypgypgXXc9bLx0LN\"

####################################\#

class listener(StreamListener):

def on_data(self, data):

dictTweet = json.loads(data)

try:

dictTweet\[\"\_id\"\] = str(dictTweet\[\'id\'\])

doc = db.save(dictTweet)

print (\"SAVED\" + str(doc) +\"=>\" + str(data))

except:

print (\"Already exists\")

pass

return True

def on_error(self, status):

print (status)

auth = OAuthHandler(ckey, csecret)

auth.set_access_token(atoken, asecret)

twitterStream = Stream(auth, listener())

\'\'\'========couchdb\'==========\'\'\'

server = couchdb.Server(\'http://kevin:12345\@localhost:5984/\')
#(\'http://115.146.93.184:5984/\')

try:

db = server.create(\'juegosolimpicos\')

except:

db = server\[\'juegosolimpicos\'\]

\'\'\'===============LOCATIONS==============\'\'\'

#twitterStream.filter(locations=\[11.4037,41.7901,13.9414,43.568\])

twitterStream.filter(track=\[\'juegosolimpicos\',\'carapaz\'\])

![](media/image2.png){width="6.5in" height="3.65625in"}

**Parte 3**

**Datos de Web Scraping(Python) a MongoDB Compass** 

Pasos: 

Ejecutamos el script de
Python, su funcionamiento consta de realizar una mineria de datos dentro
de un sitio web,
para conseguir ciertos datos se deben especificar ciertos criterios en la estructura que identifican las etiquetas contenedoras de esos datos y posteriormente su traslado a
una lista.  

![](media/image3.jpeg){width="6.5in" height="3.6222222222222222in"} 

![](media/image4.jpeg){width="6.5in" height="1.9770833333333333in"} 

 

Posteriormente a la creacion de las listas, debemos converir estos datos
en la estructura de dataset para ser identificados por los gestores de
base de datos. 

![](media/image5.jpeg){width="2.813888888888889in"
height="0.6152777777777778in"}  

![](media/image6.jpeg){width="2.1666666666666665in"
height="2.813888888888889in"} 

**Uso de Mysql Worbench** 

Para trasladar los dataset en mongodb a traves de Rapidminer, nosotros
hemos decidido elegir el gestor de BD Mysql para realizar
la vinculacion. Dentro del script es necesario tener en
nuestro FrameWork las librerias para tener los comandos necesarios para
la conexión. 

 

![](media/image7.jpeg){width="6.5in" height="1.4236111111111112in"} 

![](media/image8.jpeg){width="6.5in" height="1.6194444444444445in"} 

 

En Mysql debemos crear la base de datos de la cual recibirá dichos
contenidos. 

![](media/image9.jpeg){width="6.333333333333333in"
height="1.9680555555555554in"} 

De regreso en nuestro script debemos integrar un script para realizar
esta conexión de Python a Mysql. 

 

![](media/image10.jpeg){width="6.5in" height="3.1486111111111112in"} 

![](media/image11.jpeg){width="6.5in" height="3.3243055555555556in"} 

Una vez terminado cada proceso nos dirigimos a nuestra BD para verificar
si los dataset han sido integrados. 

![](media/image12.jpeg){width="6.5in" height="4.5472222222222225in"} 

![](media/image13.jpeg){width="6.5in" height="5.095138888888889in"} 

 

En rapiminer, creamos una nueva conexión que apunte a la base de datos
de nuestra preferencias de la cual sera importada a rapidminer para
realizar todo tipo de evaluacion. 

![](media/image14.png){width="6.5in" height="4.269444444444445in"} 

 

Ademas en mongo compass creamos la colección que servira como
repositorio para nuestras datasets. 

![](media/image15.png){width="6.5in" height="0.6111111111111112in"} 

En Rapidminer, creamos una nueva conexión con MongoDB de la cual
nos servira para instanciarla y poder enviar los datos en la BD de
nuestra prefencia. 

![](media/image16.png){width="6.5in" height="4.186111111111111in"} 

 

 

Una vez establecida las configuraciones de nuestras BD lo sigue es
realizar el modelo con los componenetes de rapidminer para pasar
los dataset. 

![](media/image17.png){width="6.5in" height="2.9055555555555554in"} 

Con el componente Read Database podremos seleccionar una de las tablas
que han sido establecidas en MYSQL. 

![](media/image18.png){width="3.345833333333333in"
height="3.2180555555555554in"} 

Luego el componente Data to Json, convertira estos datos en una
estructura Json para que mongo pueda identificarla y poder registrar en
nuestra colección. 

 

Si todo ha salido bien podemos observar como se genran la
estructuras Json con los datos de Mysql. 

 

![](media/image19.png){width="6.5in" height="3.4125in"} 

 

Y posteriormente a ello podemos verificar en MongoDB si todo ha salido
bien. 

![](media/image20.png){width="6.5in" height="2.5493055555555557in"} 

 

**Parte 4**

**Datos de Facebook a MongoDB Compass** 

Pasos: 

Ejecutamos el script de Python que lo único que hace es realizar la
extracción de datos de Facebook a través de palabras claves como en este
caso ha sido "nintendo", y guarda en un archivo con extensión .csv. 

![](media/image21.png){width="6.5in" height="2.0319444444444446in"} 

Creamos la base de datos "rapidminer" para que pueda ser leída y
reconocida en el programa RapidMiner para su respectiva conexión. 

![](media/image22.png){width="6.5in" height="0.4041666666666667in"} 

Localizamos al archive con extensión .csv y lo importamos al
programa RapidMiner lo cual no presenta problemas o errores. Una vez
leído continuamos con su finalización de columnas, entre otros. 

![](media/image23.png){width="6.5in" height="4.095833333333333in"} 

Arrastramos todos los operadores necesarios para la respectiva conexión
con MongoDB Compass, incluso realizando un map y una normalización para
la representación de los datos. También, ya creada la conexión con
MongoDB en la base de datos "rapidminer", continuamos a unir sin ningún
problema. Finalmente, especificamos en el operador *Write MongoDB *la
respectiva colección en la cual guardará todos los datos. 

![](media/image24.png){width="6.5in" height="3.045138888888889in"} 

Una vez ejecutado y comprobado que no existen problemas o errores
visualizamos la base de datos de MongoDB Compass en su colección
adjuntada lo cual podemos observar que todos los datos han sido
guardados de manera exitosa. 

![](media/image25.gif){width="0.25in" height="0.25in"} 

Una visualización más perfecta se la puede realizar con los respectivos
datos guardados, mejores vistos en formato json que
fue parseado directamente en el programa RapidMiner. 

![](media/image25.gif){width="0.25in" height="0.25in"} 

-   **Parte 5**

**Extracción de datos desde TikTok**

**Fuente 1 Arigameplays**

1.  Después de instalar TikTok Scraper, procedo a ejecutar el comando:

tiktok-scraper user arigameplays -n 100 -t csv \--session
sid_tt=asdasd13123123123adasda

Para obtener un archivo csv de la tiktoker AriGameplays.

![](media/image26.png){width="4.891666666666667in"
height="3.6992639982502187in"}

**Fuente 2 Chikybombomreal**

2.  Después de instalar TikTok Scraper, procedo a ejecutar el comando:

tiktok-scraper user chikybombomreal -n 100 -t csv \--session
sid_tt=asdasd13123123123adasda

Para obtener un archivo csv de la tiktoker Chikybombomreal.

![](media/image27.png){width="5.183333333333334in"
height="3.8752055993000876in"}

-   **Parte 6**

Creo una base de datos en phpMyAdmin.

![](media/image28.png){width="6.5in" height="3.65625in"}

Después escojo el archivo CSV y lo importo.

![](media/image29.png){width="6.5in" height="3.65625in"}

Realizo lo mismo para Chikybombomreal.

![](media/image30.png){width="6.5in" height="3.65625in"}

-   **Parte 7**

1.  Exporto en formato CSV, exporto la tabla de Chikybombomreal de la
    misma manera, el objetivo de esto fue para realizar una limpieza
    previa de datos.

![](media/image31.png){width="6.5in" height="3.65625in"}

2.  Luego de tener los archivo, se procede a abrir las tablas en
    archivos de Excel para limpiar la fila que esta llena de las
    columnas enumeradas, lo cual produce errores en RapidMiner.

![](media/image31.png){width="6.5in" height="3.65625in"}

3.  Después procedo a guardar como archivo Excel para luego usar un
    Operador READ EXCEL de RapidMiner.

![](media/image32.png){width="6.5in" height="3.65625in"}

4.  Con el operador Read Excel, obtengo toda la información de la tabla
    en RapidMiner. En este ejemplo se muestra la lectura de la tabla
    Chikybombomreal.

![](media/image33.png){width="6.5in" height="3.65625in"}

5.  Luego al presionar PLAY se verifica la conexión en RapidMiner. Se
    realizo lo mismo con la tabla Arigameplays.

![](media/image34.png){width="6.5in" height="3.65625in"}

6.  Convierto todos los datos a JSON, para luego mandarlos a MongoDB
    Compass.

![](media/image35.png){width="6.5in" height="3.65625in"}

7.  Creo una base de datos en MongoDB en el servidor local para
    almacenar la información.

![](media/image36.png){width="6.5in" height="3.65625in"}

8.  Creo una nueva conexión con MongoDB y coloco el nombre de la base de
    Datos creada.

![](media/image37.png){width="6.5in" height="3.65625in"}

9.  Conecto la conexión creada y conecto el operador Write To MongoDB,
    escojo la colección tiktokers.

![](media/image38.png){width="6.637037401574803in"
height="3.7333333333333334in"}

Con esta configuración se puede apreciar los datos en MongoDB Compass.
Lo mismo se realizó con la otra tabla.

![](media/image39.png){width="6.5in" height="3.65625in"}\
Para escribir la información de Arigameplays, creo una colección nueva
en MongoDB Compass, luego procedo a realizar las siguientes conexiones
de operadores:

![](media/image40.png){width="6.5in" height="3.65625in"}

Obteniéndose estos resultados:

![](media/image41.png){width="6.5in" height="3.65625in"}

-   **Parte 8**

1.  Para conectar a MongoDB Atlas, se procede a crear una base de datos
    en el cluster creado previamente:

mongodb+srv://kevin:123456%2a\@cluster0.zwscg.mongodb.net/UpTask?authSource=admin&replicaSet=atlas-y9bpnw-shard-0&w=majority&readPreference=primary&appname=MongoDB%20Compass&retryWrites=true&ssl=true

![](media/image42.png){width="6.5in" height="3.65625in"}

Se realiza el mismo procedimiento para la colección con los datos de
AriGameplays.

2.  Creo una nueva conexión a MongoDB Atlas en RapidMiner.

![](media/image43.png){width="6.4807688101487315in"
height="3.6454319772528434in"}

3.  Usando operadores, se procede a pasar las tablas al cluster en
    MongoDB Atlas.

![](media/image44.png){width="6.5in" height="3.65625in"}

4.  En el operador Write Mongo se debe configurar la colección donde se
    van a almacenar los datos.

![](media/image45.png){width="4.47498687664042in"
height="2.9166666666666665in"}

Después de correr el programa, se puede apreciar los datos en el cluster
de MongoDB Atlas.

![](media/image46.png){width="6.5in" height="3.65625in"}

Datos de Chikybombomreal en MongoDB Atlas

![](media/image47.png){width="6.5in" height="3.65625in"}

Verificación en MongoDB Atlas

![](media/image48.png){width="6.018043525809274in"
height="3.3851498250218723in"}

-   **Parte 9**

1.  Para convertir a CSV, basta con usar los siguientes operadores. Con
    esto se puede apreciar el archivo en formato CSV. El operador Write
    CSV es clave para escribir en formato CSV en archivo que se almacena
    en documentos.

![](media/image49.png){width="5.166666666666667in" height="2.90625in"}

Evidencia del nuevo archivo.

![](media/image50.png){width="6.5in" height="3.65625in"}

Evidencia del archivo CSV en los documentos públicos de mi PC.

![](media/image51.png){width="6.5in" height="3.65625in"}

Archivo abierto en Excel, se procede a realizar lo mismo con la otra
colección.

![](media/image52.png){width="6.5in" height="3.65625in"}

-   **Parte 10**

1.  Para grabar un JSON basta con escribir el archivo en un documento de
    texto. Con el operador Write Text, escojo un lugar donde almacenar
    el archivo que proviene de MongoDB Atlas.

![](media/image53.png){width="6.5in" height="3.65625in"}

2.  Después, podemos verificar que ahora se tiene un archivo en donde se
    puede apreciar los objetos JSON de la base de dato proveniente de
    MongoDB Atlas.

![](media/image54.png){width="6.5in" height="3.65625in"}

En Visual Studio es posible ver los objetos JSON con mayor claridad:

![](media/image55.png){width="5.378917322834646in"
height="3.0256408573928257in"}

Evidencia de trabajo para realizar todos los procesos en RapidMiner

![](media/image56.png){width="6.5in" height="3.65625in"}
