# Instalacion-Maven

##Instalar Apache Maven con apt
Actualizar el índice e instale Maven ingresando los siguientes comandos:

```
 sudo apt update
```

```
 sudo apt install maven
```

Para ver si se ha instalado correctamente:
ejecutamos este código:
```
 mvn -version
```
Deveria verse asi:
```
Maven home: /usr/share/maven
Java version: 11.0.11, vendor: Ubuntu, runtime: /usr/lib/jvm/java-11-openjdk-amd64
Default locale: es_ES, platform encoding: UTF-8
OS name: "linux", version: "5.11.0-37-generic", arch: "amd64", family: "unix"
```
## Instalamos la versión más reciente de Maven:
Para cambiar al versión más reciente cambia el número de versión en los sigientes códigos y pegalo en el terminal:
```
wget https://www.apache.org/dist/maven/maven-3/3.8.3/binaries/apache-maven-3.8.3-bin.tar.gz -P /tmp
```
Después ejecute estos códigos:
```
sudo tar xf /tmp/apache-maven-*.tar.gz -C /opt
```
Cambiar la versión alli tambien
```
sudo ln -s /opt/apache-maven-3.8.3 /opt/maven
```
```
sudo nano /etc/profile.d/maven.sh
```
Te va a saltar a otra página del terminal y pegar este código:
```
 export M2_HOME=/opt/maven
 export MAVEN_HOME=/opt/maven
 export PATH=${M2_HOME}/bin:${PATH}
```
Después de ejecutar ese cógido pulsar para guardar:``control+o`` y para salir: ``control+x``

Segimos con los siguientes códigos:
```
 sudo chmod +x /etc/profile.d/maven.sh
```
``` 
source /etc/profile.d/maven.sh
```
## Para verificar si esta instalado:
```
mvn -version
```
Deberia aparecer algo así:
```
Apache Maven 3.8.3 (ff8e977a158738155dc465c6a97ffaf31982d739)
Maven home: /opt/maven
Java version: 11.0.11, vendor: Ubuntu, runtime: /usr/lib/jvm/java-11-openjdk-amd64
Default locale: es_ES, platform encoding: UTF-8
OS name: "linux", version: "5.11.0-37-generic", arch: "amd64", family: "unix"
```


