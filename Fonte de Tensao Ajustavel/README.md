# Fonte de Tensão Ajustável
## Objetivo
O objetivo deste trabalho é projetar uma fonte de tensão ajustável entre 3V e 12V, com uma corrente máxima de 100 mA no terminal. Iniciando com uma tensão alternada de valor eficaz Vrms = 127 V, vamos montar um circuito que irá convertê-la em uma tensão contínua e constante.


## Etapas
O nosso circuito possui quatro etapas principais, que são:

![alt text](https://github.com/yurifernandes96/Eletronica-USP/blob/main/Fonte%20de%20Tensao%20Ajustavel/images/etapas.png "Etapas")

### 1. Transformação
Na etapa de transformação, ocorre uma redução da tensão eficaz de 127V para um valor que é mais conveniente para nosso circuito. O componente que faz essa redução é o Transformador. Para o nosso trabalho foi escolhido um transformador de 24V.
### 2. Retificação
A próxima etapa é a retificação dessa tensão alternada para um sinal de fluxo unidirecional. Essa etapa é composta por uma ponte de diodos, que só permitem a passagem dos ciclos positivos do sinal original, sendo essa configuração conhecida como retificador de onda completa.

![alt text](https://github.com/yurifernandes96/Eletronica-USP/blob/main/Fonte%20de%20Tensao%20Ajustavel/images/retificador2.png "Retificacao")
### 3. Filtragem
Na terceira parte, temos um filtro que normalmente na eletrônica é composto por indutores e capacitores, esse filtro faz com que o sinal pulsante fique o mais próximo possível de um sinal linear de corrente contínua. Esse filtro atua carregando e descarregando os capacitores (acumuladores de energia) como podemos ver na imagem abaixo:

![alt text](https://github.com/yurifernandes96/Eletronica-USP/blob/main/Fonte%20de%20Tensao%20Ajustavel/images/filtragem.PNG "Filtragem")

O capacitor se carrega durante um breve período de tempo e tem sua descarga lenta, com isso, faz com que os pulsos de saída fiquem quase invisíveis. Esse ruído residual é conhecido como RIPPLE e quanto menor o RIPPLE, melhor é a fonte de alimentação.

### 4. Regulagem

A última etapa é a regulagem. Nessa etapa o ripple é eliminado e a tensão se torna absolutamente constante. O componente responsável por essa etapa é o diodo zener, que funciona da seguinte forma: quando a tensão de entrada no diodo é maior que seu valor especificado, ele reduz a tensão para sua especificação. No nosso circuito foi implementado um diodo de 13 V.

![alt text](https://github.com/yurifernandes96/Eletronica-USP/blob/main/Fonte%20de%20Tensao%20Ajustavel/images/regulagem.PNG "Regulagem")


## Cálculo da Capacitância

A tensão eficaz que sai do transformador é 24 V. Logo sua tensão de pico é:

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
