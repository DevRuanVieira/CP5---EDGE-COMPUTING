# Projeto: Sensor de Luminosidade, Umidade e Temperatura com ESP32 e MQTT

Este projeto utiliza um **ESP32** para coletar dados de **luminosidade**, **umidade** e **temperatura** de um ambiente, e envia essas informações através do protocolo **MQTT** para um broker, onde podem ser acessadas remotamente.

## Componentes Utilizados

- **ESP32**: Microcontrolador com conectividade Wi-Fi e Bluetooth.
- **DHT11/DHT22**: Sensor de umidade e temperatura.
- **LDR**: Sensor de luminosidade.
- **Resistor de 10kΩ**: Para o circuito do sensor de luminosidade (LDR).
- **Broker MQTT**: Para receber os dados publicados pelo ESP32.
- **MQTT Client**: Para visualizar os dados (pode ser qualquer aplicativo ou plataforma que suporte MQTT, como MQTT Explorer, Node-RED, ou até mesmo um script Python).
- **Cabo USB**: Para conectar o ESP32 ao computador.
- **Protoboard e Jumpers**: Para montagem dos circuitos.

## Biblioteca Necessária

Para rodar o código, você vai precisar das seguintes bibliotecas instaladas no **Arduino IDE** ou na **PlatformIO**:

- **DHT Sensor Library** para leitura de temperatura e umidade.
- **Adafruit Unified Sensor** para suporte aos sensores.
- **PubSubClient** para comunicação MQTT.
- Arduino ESP32 Boards

## Esquema de Conexão

### DHT11/DHT22:
- **VCC**: 3.3V do ESP32
- **GND**: GND do ESP32
- **DATA**: GPIO (Ex: D4)

### LDR (Sensor de Luminosidade):
- Um terminal do **LDR** conectado ao **VCC** (3.3V do ESP32).
- O outro terminal do **LDR** conectado a um **resistor de 10kΩ** que vai para o **GND**.
- O ponto comum entre o LDR e o resistor vai ao pino analógico (Ex: A0) do **ESP32**.

![image](https://github.com/user-attachments/assets/a036bc54-54cb-4b99-9621-687dde51cb71)


## Instalação

1. **Configuração do Broker MQTT**: 
   - Escolha um broker MQTT (como o **Mosquitto** ou um serviço na nuvem como o **HiveMQ**).
   - Configure o endereço IP e a porta do broker no código.

2. **Instalar Bibliotecas**:
   - No Arduino IDE, vá para "Sketch" > "Incluir Biblioteca" > "Gerenciar Bibliotecas" e instale as bibliotecas mencionadas acima.

3. **Upload do Código**:
   - Conecte o ESP32 ao computador via USB.
   - Faça o upload do código ajustando os parâmetros MQTT e as credenciais Wi-Fi.


## 👥 Integrantes do Grupo 

- Ruan Melo, RM: 557599
- Rodrigo Jimenez RM: 558148
- Pedro Josué RM: 554913
- Lucca Saraiva Borges RM:554608


   
