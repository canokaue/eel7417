# EEL7417 – Fundamentos de Comunicação Digital

# Trabalho de Simulação I

# 1) Modelagem de uma variável aleatória: caso de um dado justo.

1.1) Gerar amostras aleatórias jogando N vezes um único dado (considerando igual probabilidade
para cada valor do dado).
a) Primeiramente, jogue o dado 10 vezes. (help randi)
b) Plote o histograma dos resultados obtidos.(help hist, help bar)

1.2) Pode-se normalizar os valores do histograma com N para que possa ser obtida a função
densidade de probabilidade (pdf)estimada (ou seja, a soma dos _bins_ do histograma deve ser igual a
um).
a) Plote o histograma normalizado (pdf estimada).
b) Defina a verdadeira pdf para o dado justo e plote junto com a pdf estimada (na mesma figura).
(help hold)
c) A verdadeira pdf e a estimada pdf são iguais?

1.3) Repita o processo mais algumas vezes e observe as novas amostras:
a) A pdf estimada (i.e., os valores resultantes das jogadas) sempre é a mesma?

1.4) Agora incremente o número de experimentos para N=10.000 e repita o processo mais algumas
vezes.
a) A pdf estimada (i.e., os valores resultantes das jogadas) mudou?

# 2) Geração de uma variável aleatória: jogar um dado desbalanceado.

2.1) Gerar amostras aleatórias jogando o dado, onde a probabilidade para o valor 6 é 1/4 e para os
demais valores são equiprováveis.
a) primeiro, jogue o dado por 10 vezes. (dica: busque no help do Matlab por operadores lógicos, tais
como, <, >, &,|, ==, ~=, &&, ||, >=, <=, xor)

2.2) Plote o histograma normalizado.

2.3) Definir a pdf verdadeira para o dado desbalanceado e plote junto com a pdf estimada.
a) Além de usar a função plot, veja os comandos no help: stairs e stem.

# 3) Modelagem de uma variável aleatória normalmente distribuída X com média

# zero e variância unitária.

3.1) Gerar 10.000 amostras para a variável **X.** (help randn).

3.2) Calcular as seguintes estatísticas das amostras observadas:

- média (ou valor esperado) (help mean).


- desvio padrão (help std).
- variância (help var).

3.3) Plotar o histograma normalizado.
a) Note, agora, que a pdf não é discreta e a assim deve-se usar valores suficientemente baixos para o
passo do eixo-x, de maneira de fornecer umbom gráfico. (dica: use um passo de 0.1 para o eixo-x).

# 4) Modelagem de uma variável aleatória normalmente distribuída X com média

# μ e variância σ^2 (em notação: X~( μ ,σ^2 )).

4.1) Repetir o exercício anterior, porém, em vez de usar _X_ ~(0,1), use _X_ ~( _μ_ , _σ_^2 ), em que _μ_ =2 e _σ_^2 =4.

4.2) Note que o eixo-x do histograma deve ser definido, de tal forma, que todas (ou grande maioria)
as amostras estejam dentro dos limites do eixo-x. (dica: a função hist ajuda a estimar esses limites
ou pode-se explorar as funções min(x) e max(x)).

# 5) Uso da função Q para cálculos de probabilidade P(a<X<b) para variável

# aleatória normalmente distribuída X ~( 2 , 4 ).

5.1) Definir a probabilidade P(a<X<b), em que a=2 e b=6. (helpqfunc).

5.2) Calcular a probabilidade P(X<a) e P(X>b).

5.3) Checar numericamente que a soma das probabilidades deve ser igual a 1, ou seja, que
P(-∞<X<∞) = P(X<a) + P(a<X<b) + P(X>b) = 1.

# 6) Experimento para testar o Teorema do Limite Central.

A Distribuição Normal é uma escolha intuitiva para modelagem de sinais ruidosos em sistemas de
comunicação. Em muitos modelos de sistemas, é frequentemente difícil, ou mesmo impossível,
definir todas as fontes de ruídos isoladamente. No entanto, baseado no Teorema de Limite Central,
uma distribuição da soma de variáveis aleatórias aproxima-se de uma distribuição normal, com o
incremento do número de variáveis somadas envolvidas. Ou seja, a distribuição de X1, X 2 +...+XK
aproxima-se de uma distribuição normal com o aumento de K.

6.1) Pode-se observar este fato com o exemplo do dado justo, visto anteriormente. Em vez de jogar
o dado uma vez, faz-se K vezes e observa-se a soma das jogadas. Por exemplo, com 2 (dois) dados,
X 1 e X 2 , a variável aleatória seria Z = X 1 + X 2 , em que os valores estariam entre 2 e 12.

6.2) Gerar amostras de valores aleatórios para Z (soma dos dados) jogando-os 20 vezes.

6.3) Repita o experimento por 10.000 vezes e plote o histograma de Z.

6.4) Embora a pdf pela jogada do dado justo seja uma distribuição uniforme discreta, aqui a variável
Z parece mais com uma distribuição Gaussiana (baseado no Teorema do Limite Central. Faz sentido? Qual é o valor esperado de Z?
