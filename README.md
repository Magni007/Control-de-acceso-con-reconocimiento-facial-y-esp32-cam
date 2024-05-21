# Control-de-acceso-con-reconocimiento-facial-y-esp32-cam
 Proyecto de control de acceso con reconocimiento facial a través del microcontrolador ESP32-CAM

Se utilizará la biblioteca Deepface
https://github.com/serengil/deepface/tree/master

Así como el repositorio del taller
https://github.com/codigo-iot/apertura-puertas-reconocimiento-facial

El presente proyecto encuentra una cara entre una base de datos de rostros, así como el reconocimiento facial en tiempo real a través de la cámara del ESP32-CAM

### Requisitos:
1. Instalar node-red de forma local
    a. curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash - &&\ sudo apt-get install -y nodejs
    b. sudo apt-get install -y build-essential
    c. sudo npm install -g --unsafe-perm node-red
    d. node-red (comando para arrancar node-red)

2. Instalar las bibliotecas de python
    a. sudo pip install deepface
    b. sudo pip install pandas
    c. sudo pip install paho-mqtt

3. Instalar MySQL de forma local
    a. sudo apt update
    b. sudo apt install mysql-server
    c. sudo mysql (comando para arrancar MySQL)

4. Instalar MQTT de forma local
    a. lsb_release -a
    b. sudo apt-add-repository ppa:mosquitto-dev/mosquitto-ppa
    c. sudo apt-get update
    d. apt-get update
    e. sudo apt-get install mosquitto -y
    f. sudo apt-get install mosquitto-clients -y
    g. sudo apt clean
    f. sudo systemctl enable mosquitto (para arrancar MQTT automáticamente al iniciar Ubuntu)

### Requisitos para el reconocimiento facial
1. Base de datos de rostros. (Se requiere un directorio con los rostros separados por carpetas)
2. Borrar el archivo pkl. (Sólo al momento de agregar una imágen o persona nueva).
3. Agregar una carpeta a la base de datos de rostros con fotos personales
4. Abrir el programa llamado face-recognition.py de la carpeta deepface>ejemplos
5. Actualizar las rutas
6. Ejecutar

## Apertura de puertas

1. Importar el flow llamado completo.json
Arrancar node-red