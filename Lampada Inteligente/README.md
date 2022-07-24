# Lampada Inteligente


## Objetivo
O objetivo deste trabalho é projetar um interruptor sonoro, que recebe um sinal sonoro (palma) e liga ou desliga a luz de um cômodo. O circuito desenvolvido é um exemplo em menor escala de um projeto geral.



## Etapas


### 1. Leitura de Som 
Nessa etapa o sensor de som (KY-038) detecta quando o usuário bate palmas, enviando ao controlador (ESP-32) um sinal analógico entre 0 and 4095.


### 2. Mudança de Estado
Caso o valor lido na etapa 1 seja superior a 100, o controlador (ESP-32) envia ou deixa de enviar um sinal digital de 3,3 V para o transistor (NPN BC337), que libera ou bloqueia a passagem de corrente, ligando ou apagando o LED. 



## Cálculo das Resistências

O LED precisa de corrente de cerca 10 mAm logo:

![alt text](https://github.com/yurifernandes96/Eletronica-USP/blob/main/Fonte%20de%20Tensao%20Ajustavel/equacoes/eq1.PNG "Equacao1")

Foi utilizado um resistor de 680 ohms.

O Transistor precisa de no mínimo 1/100 da corrente em sua base em relação ao valor total que passará pelo coletor (10 mA), logo precisa no mínimo 0,1 mA na base. Optamos por 1 mA:

![alt text](https://github.com/yurifernandes96/Eletronica-USP/blob/main/Fonte%20de%20Tensao%20Ajustavel/equacoes/eq2.PNG "Equacao2")

Utilizamos 4 resistores de 820 em série, resultando 3260 ohms.


## Tabela dos valores dos componentes

| Quantidade        | Componente           | Valor uni.  | Valor Tot  |
| ----------------- |:--------------------:| -----------:| ----------:|
| 1 | [ESP 32](https://www.baudaeletronica.com.br/placa-doit-esp32-bluetooth-e-wifi.html)   | 65,96   | 65,96   |
| 1 | [Sensor de Som KY-038](https://www.filipeflop.com/produto/sensor-de-som-ky-038-microfone/)     |    12,40 |  12,40 |
| 1 | [LED Difuso 5 mm](https://www.baudaeletronica.com.br/led-difuso-5mm-vermelho.html)    |    0,25 |  0,25 |
| 1 | [Transistor NPN BC337](https://www.baudaeletronica.com.br/transistor-npn-bc337.html)   |    0,27 |  0,27 |
| 1 | [Resistor 680R Carvão](https://www.baudaeletronica.com.br/resistor-680r-5-1-4w.html)    |    0,06 |  0,06 |
| 4 | [Resistor 820R Carvão](https://www.baudaeletronica.com.br/resistor-820r-5-1-4w.html)    |    0,05 |  0,20 |
| TOTAL | |    |  79,14 |





## Links úteis

[Vídeo explicativo no YouTube](https://www.youtube.com/watch?v=fCE0FbQKNUs)

[Aulas do Prof. Simões](https://gitlab.com/simoesusp/disciplinas/-/tree/master/SSC0180-Eletronica-para-Computacao)



## Agradecimentos
![alt text](https://github.com/yurifernandes96/Eletronica-USP/blob/main/Fonte%20de%20Tensao%20Ajustavel/images/simoes.png)



## Grupo 33
Lucas André - 13673260

Luan Benson - 13672085

Luiz Schulz - 13732769

Yuri Fernandes - 13730127
