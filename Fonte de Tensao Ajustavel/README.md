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
![alt text]([https://github.com/yurifernandes96/Eletronica-USP/blob/main/Fonte%20de%20Tensao%20Ajustavel/images/etapas.png](https://github.com/yurifernandes96/Eletronica-USP/blob/main/Fonte%20de%20Tensao%20Ajustavel/images/Tipos-de-retificadores.png) "Retificacao")
### 3. Filtragem

### 4. Regulagem
