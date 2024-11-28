# Projeto Viva o_Antigo
O projeto Viva o antigo consiste em uma câmera de impressão térmica juntamente com arduino que permite aos usuários registrarem momentos com ela.
A solução técnica que foi usada para esse projeto é composta de diferentes modais dentro de um modelo de câmera fotográfica que remete às primeiras criadas na história. 

O projeto é composto de três partes: 1 - Estrutura, 2 - Arduino, 3 - Câmera e impressora.

## 🧱 Estrutura
O Projeto tem como estrutura uma caixa feita em MDF em formato análogo as câmeras fotográficas antigas e uma tela e botão, conectados ao arduino.

##  Arduino
responsável pelo código do projeto, através dele foi criado um sistema que utiliza um display LCD, um botão e um servo motor.
Quando o botão é pressionado, inicia uma contagem regressiva de 10 segundos, e após o tempo, o sistema simula o processo de tirar uma foto, movendo o servo e piscando um LED.
O display LCD exibe mensagens em todas as etapas do processo

## Câmera e impressora
responsável por registrar a foto para o usuário e imprimi-la.

How to Use do Projeto Viva o Antigo:  
1 - Pressione o botão.localizado no lado da caixa.  
2 - o LCD irá notificar o tempo restante para a foto, com esse tempo,se organize para o registro da foto.  
3 - após a contagem do cronômetro terminar, o LCD irá notificar que a foto está sendo registrada com a mensagem "Tirando foto...", além disso, o LED vai disparar simulando o "disparo da foto".  
4 - O LCD exibe a mensagem "Obrigado =)" e retorna para o estado inicial no intuito de realizar-lo outra vez.


Explicação do código:  
#include <LiquidCrystal_I2C.h>  
#include <Servo.h>  
#include <Wire.h>
1 - Nessa 1º parte são incluídas bibliotecas no código. A seguir serão explicadas cada uma dessas funções individualmente:
1º - include <LiquidCrystal_I2C.h> : Esta biblioteca permite controlar um display LCD com interface I2C, simplificando o uso de displays LCD com dois fios (SDA e SCL).  
2º - include <Servo.h> : Biblioteca que possui as funções necessárias para posicionar o servo para a posição desejada.
3º - #include <Wire.h> : Biblioteca que permite comunicação com dispositivos I2C/TWI.
1º - Include <LiquidCrystal_I2C.h>: 1º - Include <LiquidCrystal_I2C.h>: v
