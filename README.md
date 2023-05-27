# Problema #2 – Interfaces de E/S


 📌 PBL 2 | Sistemas Digitais | Univerdade Estadual de Feira de Santana 

## 🚀 introdução

Foi solicitado um projeto de sensor analógico/digital em microcontrolador utilizando comunicação serial UART.

Consulte **[Implantação](#-implanta%C3%A7%C3%A3o)** para saber como implantar o projeto.

### 📋 Requisitos
O sistema a ser implementado no SBC deverá atender aos seguintes requisitos:
```
O código deverá ser escrito em linguagem C; 
Capacidade de interligação com até 32 unidades de sensoriamento;
Mecanismo de controle de status de funcionamento das unidades;
Apenas o SBC será capaz de iniciar uma comunicação.
```
O protótipo a ser implementado na NodeMCU deverá atender às seguintes restrições:
```
O código deverá ser escrito em linguagem C;
Deverá ser capaz de ler e interpretar comandos oriundos do SBC.
```
Além disso:
```
Os comandos serão compostos por palavras de 8 bits;
A informação medida deve ter a maior precisão possível;
As requisições do SBC podem ser direcionadas para uma unidade específica ou a todas;
As solicitações e as respostas deverão ser exibidas no display LCD.

```
