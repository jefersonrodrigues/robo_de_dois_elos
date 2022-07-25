# Robô de Dois Elos

Considere um robô de dois elos, conforme ilustra a figura:

<img src="https://drive.google.com/uc?id=1n9_mJ9sj3O2Kp9FOL8gP3RMxHiKK9tRC" width="300">

Considere ainda as equações que definem a posição da garra $p$:

$p = \left[ \begin{array}\\ p_x \\ p_y \end{array}\right] = \left[ \begin{array}\\ l_1 cos(\theta_1) + l_2cos (\theta_1+\theta_2) \\ l_1 sin(\theta_1) + l_2 sin(\theta_1+\theta_2) \\ \end{array} \right]$

E por fim considere o ponto alvo:
$m = \left[\begin{array}\\ m_x\\ m_y\\ \end{array}\right]$.

A distância Euclideana entre $p$ e $m$ é dada por:
$d = || m - p ||_2 = \sqrt{(m_x-p_x)^2 + (m_y-p_y)^2}$

Assim podemos definir uma função de custo $f(\theta_1, \theta_2) = d^2$, que resulta na expressão:
$f(\theta_1,\theta_2)=(m_x-l_1 cos(\theta_1) - l_2cos(\theta_1+\theta_2))^2 + (m_y-l_1 sin(\theta_1) - l_2 sin(\theta_1+\theta_2))^2$

Levando em conta o problema formulado acima:

1. Escreva uma função que, dados os ângulos das juntas $\theta_1$, $\theta_2$, e constantes $l_1$, $l_2$, calcule a posição do ponto $p$.

2. Escreva uma função que, dados o ponto $m$ e os ângulos $\theta_1$ e $\theta_2$ e constantes $l_1$ e $l_2$, calcule a função de custo exatamente como descrita acima.

3. Calcule de forma analítica o gradiente dessa função de custo, com respeito aos ângulos $\theta_1$ e $\theta_2$. Implemente uma função que, dada a pose atual do robô, calcule como saída esse gradiente.

5. Implemente o método da descida do gradiente utilizando as funções implementadas nos itens 2 e 3 acima.

6. Mostre graficamente, numa animação, como o robô chega ao ponto desejado utilizando este método.

## Avaliação

Este código inclui funções de avaliação que testam a sua implementação e dão algum feedback, ainda que limitado. Para pontuar nos itens 1 a 4 acima, você deve garantir que seu código passe nos respectivos testes. Para pontuar no item 6, você deverá observar o robô chegando ao alvo na animação gerada automaticamente pelo código da última célula ao final do documento. Isso deve acontecer automaticamente se você cumpriu todos itens e passou todos testes.
