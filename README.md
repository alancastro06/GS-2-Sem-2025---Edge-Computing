# GS-2-Sem-2025---Edge-Computing

**VitaQR – Bracelete de Emergência para Enchentes**

🚨 **Detecção automática de submersão**  
🔔 **Monitoramento em tempo real com MQTT**  
📊 **Visualização em dashboard via Node-RED**


:warning: Problema Identificado

O Brasil enfrenta recorrentes tragédias causadas por enchentes. Em 2024, o estado do Rio Grande do Sul vivenciou a maior catástrofe climática de sua história, afetando mais de 2,3 milhões de pessoas. Muitas vítimas foram resgatadas inconscientes, sem documentos ou informações médicas, dificultando atendimentos eficazes. A falta de dados compromete diretamente a segurança e agilidade em situações de emergência.

:bulb: Solução Proposta

O VitaQR é um bracelete de emergência com sensor ultrassônico e transmissão MQTT. Ele detecta submersão prolongada (distância < 5 cm por mais de 5 segundos) e emite alertas sonoros e visuais, além de transmitir em tempo real os dados para um dashboard remoto.

O dispositivo também inclui um QR Code que pode ser escaneado por socorristas para acesso a informações médicas da vítima (tipo sanguíneo, alergias, comorbidades), mesmo offline.

:electric_plug: Arquitetura do Projeto

IoT (Dispositivo Físico)

ESP32

Sensor Ultrassônico HC-SR04

Display LCD I2C 20x4

Buzzer

LEDs (verde e vermelho)

Protocolo: MQTT

Node-RED Dashboard

Gauge (Distância)

Text status ("SUBMERSO" / "SITUAÇÃO NORMAL")

:gear: Funcionamento

O sensor mede a distância da superfície da água a cada segundo

Se a distância for < 5 cm por mais de 5 segundos, ativa:

Buzzer

LED vermelho

Alerta visual no LCD

Envio de mensagem MQTT

Caso a distância aumente novamente:

LED verde volta a acender

LCD exibe "Situação normal"

:computer: Como Executar

1. Simulação Wokwi

Acesse: https://wokwi.com/projects/432270278894618625

Aguarde o LCD mostrar "Sistema Pronto!"

Ajuste a distância do sensor no topo da simulação

2. Dashboard Node-RED

Importe o fluxo com:

Arquivo "flows.json" no repositório

:wrench: Tecnologias Utilizadas

ESP32 (Arduino C++)

Sensor HC-SR04

MQTT (Mosquitto Broker)

Node-RED + Dashboard

LCD I2C 20x4

Wokwi (simulador)

:man_technologist: Autores

Alan Archangelo - RM: 560152

Lucas Cortizo - RM: 559734
