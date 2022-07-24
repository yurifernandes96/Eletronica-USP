# Fonte de Tensão Ajustável


## Objetivo
O objetivo deste trabalho é projetar um interruptor sonoro, que recebe um sinal sonoro (palma) e liga ou desliga a luz de um cômodo. O circuito desenvolvido é um exemplo em menor escala de um projeto geral.



## Etapas


### 1. Leitura de Som 
Nessa etapa o sensor de som(KY-038) detecta quando o usuário bate palmas, enviando ao controlador (ESP-32) um sinal analógico entre 0 and 4095.


### 2. Mudança de Estado
Caso o valor lido na etapa 1 seja superior a 100, o controlador (ESP-32) envia ou deixa de enviar um sinal digital de 3,3 V para o transistor (NPN BC337), que libera ou bloqueia a passagem de corrente, ligando ou apagando o LED. 



## Cálculo das Resistências

O LED precisa de corrente de cerca 10 mAm logo:

![alt text](https://github.com/yurifernandes96/Eletronica-USP/blob/main/Fonte%20de%20Tensao%20Ajustavel/equacoes/eq1.PNG "Equacao1")

Considerando a queda de tensão de 1,4 V que ocorre na ponte de diodo, temos:

![alt text](https://github.com/yurifernandes96/Eletronica-USP/blob/main/Fonte%20de%20Tensao%20Ajustavel/equacoes/eq2.PNG "Equacao2")

Como queremos estabelecer um ripple máximo de 10%, temos:

![alt text](https://github.com/yurifernandes96/Eletronica-USP/blob/main/Fonte%20de%20Tensao%20Ajustavel/equacoes/eq3.PNG "Equacao3")

Obtendo uma corrente de 124 mA a partir do simulador e sabendo da primeira lei de Ohm podemos aplicar a seguinte equação para a frequência de 60 Hz:

![alt text](https://github.com/yurifernandes96/Eletronica-USP/blob/main/Fonte%20de%20Tensao%20Ajustavel/equacoes/eq4.PNG "Equacao4")

Desse modo, obtemos uma capacitância de 317,9 uF e optamos por usar um capacitor de 330 uF, que é o valor comercial mais próximo.



## Tabela dos valores dos componentes

| Quantidade        | Componente           | Valor uni.  | Valor Tot  |
| ----------------- |:--------------------:| -----------:| ----------:|
| 1 | [Transformador 110/220 V para 24 V](https://www.baudaeletronica.com.br/transformador-trafo-1a-24v.html)   | 55,24   | 55,24   |
| 1 | [Ponte Retificadora](https://www.moduloeletronica.com.br/produto/ponte-retificadora-w10m-15a-1000v/3441934)     |    1,30 |  1,30 |
| 1 | [Capacitor 330uF e 25 V](https://www.baudaeletronica.com.br/capacitor-eletrolitico-330uf-25v.html)    |   0,33 |    0,33 |
| 1 | [LED Difuso 5 mm](https://www.baudaeletronica.com.br/led-difuso-5mm-vermelho.html)    |    0,25 |  0,25 |
| 1 | [Diodo Zener 13 V 1/2 W](https://www.baudaeletronica.com.br/diodo-zener-bzx55c-13v-0-5w.html)    |    0,08 |  0,08 |
| 1 | [Potenciômetro Linear 5K](https://www.baudaeletronica.com.br/potenciometro-linear-de-5k-5000.html)    |    2,06 |  2,06 |
| 1 | [Transistor NPN BC337](https://www.baudaeletronica.com.br/transistor-npn-bc337.html)   |    0,27 |  0,27 |
| 3 | [Resistor 2K2 Carvão](https://www.baudaeletronica.com.br/resistor-2k2-5-1-4w.html)    |    0,06 |  0,18 |
| TOTAL | |    |  59,71 |

Obs: Usamos um transformador emprestado pelo Professor Simões, então nosso custo real foi de cerca de R$ 4,50



## Links úteis
[Circuito no Falstad](https://tinyurl.com/2gka35pf)

[Vídeo explicativo no YouTube](https://www.youtube.com/watch?v=fCE0FbQKNUs)

[Aulas do Prof. Simões](https://gitlab.com/simoesusp/disciplinas/-/tree/master/SSC0180-Eletronica-para-Computacao)



## Agradecimentos
![alt text](https://github.com/yurifernandes96/Eletronica-USP/blob/main/Fonte%20de%20Tensao%20Ajustavel/images/simoes.png)



## Grupo 33
Lucas André - 13673260

Luan Benson - 13672085

Luiz Schulz - 13732769

Yuri Fernandes - 13730127
