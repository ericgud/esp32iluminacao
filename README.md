// esp32iluminacao

/*

Código em C para um sistema de automação de iluminação e climatização usando o ESP32
Explicação do Código

**Conexão Wi-Fi:**

O ESP32 se conecta à rede Wi-Fi fornecida (ssid e password).

**Conexão MQTT:**

> O ESP32 se conecta a um broker MQTT (neste exemplo, um broker público como broker.hivemq.com).

> Ele se inscreve nos tópicos de controle (topic_controle_luz e topic_controle_clima) para receber comandos.

**Leitura dos Sensores:**

> O sensor LDR mede a luminosidade.

> O sensor DHT22 mede a temperatura e a umidade.

**Controle dos Relés:**

> Com base nas mensagens MQTT recebidas, o ESP32 controla os relés para ligar/desligar as luzes e a climatização.

> Publicação dos Dados:

> Os dados de luminosidade, temperatura e umidade são publicados nos tópicos MQTT correspondentes para monitoramento remoto.

**Loop Principal:**

> O loop principal lê os sensores, publica os dados e verifica mensagens MQTT a cada 5 segundos.

**Como Testar o Sistema
Configuração do Hardware:**

> Conecte o LDR ao pino 34 (usando um divisor de tensão com resistor).

> Conecte o DHT22 ao pino 4.

> Conecte os relés aos pinos 25 (luzes) e 26 (climatização).

> Configuração do Broker MQTT:

> Use um broker MQTT público (como broker.hivemq.com) ou instale um broker local (como Mosquitto).

**Envio de Comandos:**

**Use um cliente MQTT (como MQTT Explorer ou MQTTX) para enviar comandos:**

> Envie 1 para empresa/iluminacao/controle para ligar as luzes.

> Envie 0 para empresa/iluminacao/controle para desligar as luzes.

> Faça o mesmo para empresa/climatizacao/controle.

**Monitoramento:**

Verifique os dados publicados nos tópicos empresa/iluminacao/luminosidade, empresa/climatizacao/temperatura e empresa/climatizacao/umidade.

**Próximos Passos**

1> Implementar uma interface web ou aplicativo móvel para controle remoto.

2> Adicionar funcionalidades de segurança, como autenticação e criptografia.

3> Integrar com sistemas de gestão de energia ou sustentabilidade.

_**Este código é um ponto de partida e pode ser expandido conforme as necessidades específicas do projeto.**_ 

*/
