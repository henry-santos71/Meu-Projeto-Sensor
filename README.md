# ESP32 + MQTT + Node-RED

Atividade prática de IoT: um ESP32 simulado no Wokwi publica temperatura e umidade (DHT22) via MQTT e recebe comandos de um painel no Node-RED.

## Componentes
- ESP32
- Sensor DHT22 (pino 12)
- LED (pino 26)
- Servo motor (pino 2)
- Anel NeoPixel de 16 LEDs (pino 16)

## Broker
broker.hivemq.com, porta 1883

## Tópicos
- Tempdata: o ESP32 publica "temperatura,umidade,"
- lights: o Node-RED envia ON ou OFF para o LED
- servo: o Node-RED envia o ângulo, de 0 a 180
- lights/neopixel: o Node-RED envia a cor no formato R,G,B

## Como rodar
1. Abrir o projeto no Wokwi e rodar a simulação.
2. Instalar o Node-RED e o node-red-dashboard.
3. Importar o fluxo_nodered.json e implementar.
4. Abrir o painel em http://localhost:1880/ui

## Arquivos
- projetowokwi.ino: código do ESP32
- projeto_wokwi.json: diagrama do circuito
- fluxo_nodered.json: fluxo do Node-RED
- libraries.txt: bibliotecas usadas
