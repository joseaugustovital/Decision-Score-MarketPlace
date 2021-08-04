# MarketPlace Decision Score
 [![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://github.com/Z-Augusto-Vital/8Puzzle-A-Star/blob/main/LICENSE)
 
 # Desenvolvimento
 UNIVERSIDADE FEDERAL DO MATO GROSSO DO SUL
 
 Autor: José Augusto Lajo Vieira Vital
 
 Orientador: Edson Takashi Matsubara
 
 Estudo: Implementação de árvores de decisão para identificar possíveis problemas em um marketplace.
 
 Linguagem: Python
 
 ## Link Colab Original
 
 https://colab.research.google.com/drive/1LFk9HUKs-viPqtMErtP7wP46CuKbrXOu?usp=sharing
 
 # Objetivo do modelo
 
 ## Árvore de Decisão
 
  O conceito utilizado para a resolução do problema foi com base na lógica de árvores de decisão. Dessa forma, cada condição encontrada pode levar a 
 inúmeras possibilidades diferentes. Portanto o modelo utilizado explora parte do dataset para treino, e com base no padrão encontrado, retorna os atributos mais 
 relevantes para a insatisfação dos clientes.
 
 Exemplo:
 
![image](https://www.researchgate.net/profile/Cristiano-Torezzan/publication/298217297/figure/fig1/AS:419286158987270@1476977018644/Figura-1-EsquematizacEsquematizacEsquematizacao-de-uma-arvore-de-decisao-Fonte-Dos_Q320.jpg)
![image](https://i0.wp.com/www.analyticsvidhya.com/wp-content/uploads/2016/04/dt.png?resize=525%2C414&ssl=1)
 
 # Análise de Dados
 
 Os dados utilizados para aplicação do modelo são de um dataset real pertencente a um e-commerce que apresentava problemas em indentificar o que afetava a satisfação dos clientes devido ao grande volume de dados e pela complexidade na relação dos atributos.
 
 O conjunto de dados pode ser acessado por: https://www.kaggle.com/olistbr/brazilian-ecommerce
 
 
# 1) Heurísticas
## **A) Heurística 1 - Número de Peças Fora do Lugar**
Método que utiliza a quantidade de posições erradas em relação ao goal, ou seja, conta quantas peças estão na posição errada quando comparado com o estado resolução do problema. Essa função retorna a quantidade de elementos estão fora da sua posição correta.

## **B) Heurística 2 - Distância de Manhattan**
A distância de Manhattan (“City Block” ou “Geometria do Táxi”) é um modelo geométrico em que a distância entre dois pontos é a soma das diferenças absolutas de suas coordenadas. Essa função retorna a distância da posição atual até a posição correta com base na métrica da Distância de Manhattan.

![image](https://user-images.githubusercontent.com/75955255/123881250-4f6b4180-d912-11eb-9587-4ac74065d742.png)

# 2) Buscas 
## **A) Hill Climbing**
O método usa como parâmetro de resolução do puzze a função heurística (Heurística 1 ou 2) chamada de h(n).

f(n) = h1(n)

f(n) = h2(n)

## **B) A-Star**
O método usa como parâmetros de resolução do puzzle as funções h(n), e uma função g(n) que retorna o custo de determinado estado até o nó n.

f(n) = h1(n) + g(n)

f(n) = h2(n) + g(n)

![image](https://user-images.githubusercontent.com/75955255/123882556-036dcc00-d915-11eb-81d8-727a5d6a6e6a.png)










