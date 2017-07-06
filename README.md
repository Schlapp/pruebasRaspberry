# pruebasRaspberry
Pruebas raspberry desde la rasp 6-7-2017
6-7-2017
Pasos para la instalación del serialport

primero instalamos node
pag
http://thisdavej.com/beginners-guide-to-installing-node-js-on-a-raspberry-pi/#install-node

curl -sL https://deb.nodesource.com/setup_8.x | 
sudo -E bash -sudo apt install nodejs

Installing node-serialport
npm install serialport
npm install johnny-five raspi-io

firmata standart 
funciono al instanciarlo desde el interprete de node
Se crea el archivo prueba.js con el contenido siguiente:
var five = require("johnny-five");
var board = new five.Board();

board.on("ready", function() {
  var led = new five.Led(13);
  led.blink(500);
});

FUNCIONO!



