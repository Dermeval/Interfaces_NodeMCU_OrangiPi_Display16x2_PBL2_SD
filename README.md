# Problema #2 – Interfaces de E/S


 📌 PBL 2 | Sistemas Digitais | Univerdade Estadual de Feira de Santana 

## 🚀 introdução

Foi solicitado um projeto de sensor analógico/digital em microcontrolador utilizando comunicação serial UART.

Consulte **[Implantação](#-implanta%C3%A7%C3%A3o)** para saber como implantar o projeto.

### 📋 Requisitos
O sistema a ser implementado no SBC deverá atender aos seguintes requisitos:
```
- O código deverá ser escrito em linguagem C; 
- Capacidade de interligação com até 32 unidades de sensoriamento;
- Mecanismo de controle de status de funcionamento das unidades;
- Apenas o SBC será capaz de iniciar uma comunicação.
```
O protótipo a ser implementado na NodeMCU deverá atender às seguintes restrições:
```
- O código deverá ser escrito em linguagem C;
- Deverá ser capaz de ler e interpretar comandos oriundos do SBC.
```
Além disso:
```
- Os comandos serão compostos por palavras de 8 bits;
- A informação medida deve ter a maior precisão possível;
- As requisições do SBC podem ser direcionadas para uma unidade específica ou a todas;
- As solicitações e as respostas deverão ser exibidas no display LCD.

```
### 📋 Recursos Utilizados

[Solicitação do Projeto](https://github.com/Dermeval/Interfaces_NodeMCU_OrangiPi_Display16x2_PBL2_SD/blob/main/Recursos/Solicita%C3%A7%C3%A3o%20do%20Projeto%20Probl2.pdf "Solicitação do Projeto")
[DataSheet do Orangi Pi PC Plus](https://github.com/Dermeval/Interfaces_NodeMCU_OrangiPi_Display16x2_PBL2_SD/blob/main/Recursos/DataSheet%20do%20ORANGE%20PI.pdf "DataSheet do Orangi Pi PC Plus")
[DataSheet do LCD](https://github.com/Dermeval/Interfaces_NodeMCU_OrangiPi_Display16x2_PBL2_SD/blob/main/Recursos/DataSheet%20do%20LCD.pdf "DataSheet do LCD")
[DataSheet do NodeMCU Esp8266EX](https://github.com/Dermeval/Interfaces_NodeMCU_OrangiPi_Display16x2_PBL2_SD/blob/main/Recursos/DataSheet%20Esp8266EX%20Node%20MCU.pdf "DataSheet do NodeMCU")

### 🔧 Perifêricos Necessários
```
1 Protoboard
1 Placa Orange Pi PC PLUS:
	1 Display LCD 16x2
	3 Botões
1 Placa NodeMCU
	2 Sensores (Botões)
	1 Led
	1 Potênciometro
1 Jumper para ligar a GPIO na Protoboard
```
### 🔧 Instalação

É necessário ter a [biblioteca WiringPi](http://wiringpi.com/download-and-install/ "biblioteca WiringiPi") devidamente instalada na sua Orange Pi
Foi utilizada a [IDE Sublime txt](https://www.sublimetext.com/3 "IDE Sublime txt") para programar a OrangePi PC Plus
Foi utilizada a [IDE Arduíno](https://www.arduino.cc/en/software "IDE Arduíno") para programar a Node MCU

## ⚙️ Metodologia

O código foi desenvolvido na** linguagem C** e permite a placa** Orange Pi** se comunicar através de uma comunicação serial **UART** com a placa **Node MCU**, onde é possível que a nossa SBC **Orange Pi** solicite para a **Node** o envio de dados do dois sensores digitais e um dado analógico medido por um potênciometro e exibir no **display 16x2** da **Orange** todas as informações, organizadas por um menu, além de também poder ligar o **LED da Node**.

Para entender melhor a relação entre as entidades, foi desenvolvido o seguinte diagrama:


## 📄 SBC - Orange Pi

A Orange Pi PC Plus é uma placa de computador de placa única (SBC) desenvolvida pela Xunlong Software, baseada na arquitetura ARM. Ela é projetada como uma alternativa de baixo custo para outras placas populares, como a Raspberry Pi.

A Orange Pi PC Plus possui um processador quad-core Allwinner H3, com núcleos Cortex-A7, operando a uma frequência de até 1,6 GHz.

## 📄 NodeMCU ESP8266EX

O **NodeMCU ESP8266EX**[[1]][Node] é uma placa de desenvolvimento baseada no chip ESP8266EX da Espressif Systems. Ele oferece conectividade Wi-Fi e tem um microcontrolador integrado que pode ser programado usando a linguagem Lua, por exemplo. É uma escolha popular para projetos de IoT e automação residencial.
