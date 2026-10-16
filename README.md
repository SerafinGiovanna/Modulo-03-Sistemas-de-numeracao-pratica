# TRILHA DE APRENDIZADO
Neste repositório vai conter os exercícios e o arquivo de resposta.md (contendo a parte escrita do módulo), feitas na Trilha de aprendizado.

# Índice
## Módulo 03-Sistemas-Numeracao-Prática

###### -----------------------------------------------------
- [ 1.Decimal → binário](#1-Decimal-→-binário)
- [ 2. Binário → decimal](#2-Binário-decimal)
- [ 3. Binário ↔ hexadecimal](#3-Binário-hexadecimal)
- [ 4. Soma binária](#4-Soma-binária)
- [ 5. Quantos bits são necessários?](#5-Quantos-bits-são-necessários?)
- [ 7. Decimal ↔ octal, e a "quarta base"](#7-Decimal-octal-e-a-quarta-base)
- [ 8. Subtração binária](#8-Subtração-binária)
- [ 9. Complemento de 2 (representando negativos)](#9-Complemento-de-2-representando-negativos)

  # Exercícios

  ## 1. Decimal → binário
  Converta pelo método das moedas, mostrando cada passo: 13, 41, 100, 255.
  ***
  ## 2. Binário → decimal
  Converta somando o valor de cada casa (posição), mostrando a soma: 1010, 101010, 11111111.
  ***
  ## 3. Binário ↔ hexadecimal
  1.Converta 11010110 para hexadecimal, mostrando o agrupamento em blocos de 4 bits.
  2.Converta 0x3F para binário e depois para decimal.
  ***
  ## 4. Soma binária
  Some, mostrando coluna por coluna e o vai-um explicitamente (como no exemplo da teoria):

   **1. 0110 + 0011**
   **2. 1011 + 0111**
  ***
  ## 5. Quantos bits são necessários?
  Quantos bits, no mínimo, são necessários para representar todos os números inteiros de 0 até 1000? Não vale só dar o número — explique o raciocínio: quantos valores diferentes n bits conseguem representar, e a partir de qual n esse total passa de 1000.
  ***
  ## 7. Decimal ↔ octal, e a "quarta base"
  1.Converta 41 para octal (base 8), usando o mesmo método de divisões sucessivas — só que dividindo por 8 em vez de por Mostre cada passo.
         
  2.Converta 0o61 (octal) de volta para decimal, somando o valor de posição de cada dígito (potências de 8, não de 2).

  3.Converta 101001 (binário) direto para octal, agrupando de 3 em 3 bits a partir da direita (não de 4 em 4 como no hexadecimal — explique por que o agrupamento muda: 2³ = 8).

  4.[CLI] Confira tudo com python3 -c "print(oct(41), int('61', 8))".
***
## 8. Subtração binária
A subtração binária segue a mesma lógica da subtração decimal com "empréstimo" (borrow), do mesmo jeito que a soma usa "vai-um" (carry) — quando falta valor numa coluna, você empresta 1 da coluna seguinte (que vale o dobro).

1.Subtraia mostrando coluna por coluna e o empréstimo explícito: 1011 - 0011.

2.Subtraia: 1000 - 0001 (esse exemplo tem empréstimo encadeado por várias colunas — mostre cada uma).

3.Agora resolva 1011 - 0011 de novo, mas usando complemento de 2 de 0011 somado a 1011 (você vai fazer isso no exercício 9 — volte aqui depois de resolver o 9 e confirme que os dois métodos dão o mesmo resultado).
  ***
  ## 9. Complemento de 2 (representando negativos)
  Complemento de 2 é como um computador representa números negativos usando só 0 e 1 — sem precisar de um símbolo de -. Considerando registradores de 4 bits:

1.Encontre o complemento de 2 de 0011 (decimal 3), passo a passo: inverta todos os bits (complemento de 1) e depois some 1 Confirme que o resultado, interpretado como negativo, representa -3.

2.Faça o caminho inverso: dado 1101 (em complemento de 2, 4 bits), descubra que número decimal negativo ele representa (inverta os bits do resultado e some 1, depois leia como positivo e aplique o sinal de menos).

3.Volte ao exercício 8.3 e confirme, escrevendo explicitamente, que 1011 - 0011 e 1011 + complemento_de_2(0011) dão o mesmo resultado (descartando o vai-um extra que "estoura" os 4 bits, se houver).

4.[TENTE VOCÊ] Por que complemento de 2 evita a necessidade de um circuito separado pra subtração (ele reaproveita o mesmo somador)? Resposta: porque subtrair A - B vira somar A + complemento_de_2(B) — o hardware só precisa saber somar, nunca subtrair de fato.
