# Flow_4
# Hacer un flow que pueda obtener la informacion por mqtt y la grafique

1. Abrir nodeRed y entrar localhost:1880
2. Hacer un floq que reciba información por MQTT y grafique la información recibida por MQTT
- Enviar un JSON por MQTT
- ID, temp, hum
- localhost
- codigoIoT/Mor/mqtt/flow4
- Mensaje mqtt


mosquitto_pub -h localhost -t codigoIoT/Mor/mqtt/flow4 -m '{"ID":"Valerie Romero","temp":21,"hum":53}'

Cada nodo a su salida genera un objeto llamado msg
- mgs
- msg.payload
- msg._msgid
- msg.topic
- msg.label

Nodo function Temperatura
msg.payload = msg.payload.temp;
msg.topic = "Temperatura";
return msg;

Nodo function Humedad
msg.payload = msg.payload.hum;
msg.topic = "Humedad";
return msg;
