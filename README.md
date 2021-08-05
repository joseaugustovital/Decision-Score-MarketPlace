# MarketPlace Decision Score
 [![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://github.com/Z-Augusto-Vital/8Puzzle-A-Star/blob/main/LICENSE)
 
 # Desenvolvimento
 UNIVERSIDADE FEDERAL DO MATO GROSSO DO SUL
 
 Autor: José Augusto Lajo Vieira Vital
 
 Professor: Edson Takashi Matsubara
 
 ## Inteligência Artificial 
 
 Estudo: Manipulação de árvores de decisão para identificar possíveis problemas em um marketplace.
 
 Linguagem: Python
 
 ## Link Colab Original
 
 https://colab.research.google.com/drive/1LFk9HUKs-viPqtMErtP7wP46CuKbrXOu?usp=sharing
 
 # Especificações do modelo
 Como entender a situação do e-commerce, sua logística e todos os seus fatores é um problema complexo, inicia-se o estudo identificando
 que se trata de um problema descritivo. Sendo assim, uma das soluções mais apropriadas para problemas com essas caracteristicas é árvore de decisão.
 ## Árvore de Decisão
 
  O conceito utilizado para a resolução do problema foi com base na lógica de árvores de decisão. Dessa forma, cada condição encontrada pode levar a 
 inúmeras possibilidades diferentes. Portanto o modelo utilizado explora parte do dataset para treino, e com base no padrão encontrado, retorna os atributos mais 
 relevantes para a insatisfação dos clientes.
 
 Exemplo:
 
![image](https://www.researchgate.net/profile/Cristiano-Torezzan/publication/298217297/figure/fig1/AS:419286158987270@1476977018644/Figura-1-EsquematizacEsquematizacEsquematizacao-de-uma-arvore-de-decisao-Fonte-Dos_Q320.jpg)
![image](https://i0.wp.com/www.analyticsvidhya.com/wp-content/uploads/2016/04/dt.png?resize=525%2C414&ssl=1)
 
 # Análise de Dados
 
 Os dados utilizados para aplicação do modelo são de um dataset real pertencente a um e-commerce que apresentava problemas relacionados a satisfação dos seus clientes. As dificuldades de identificar as razões eram o grande volume de dados e a complexidade na correlação de muitos atributos.
 
 O conjunto de dados pode ser acessado por: https://www.kaggle.com/olistbr/brazilian-ecommerce

# Tabelas
Foram utilizadas 9 tabelas do modelo relacional para filtragrem e análise de todos os valores e atributos mais relevantes para a variável decision_score
da tabela olist_order_reviews_dataset. O objetivo de reunir todos os dados em uma tabela só, é justamente facilitar o aprendizado do modelo e aumentar
a acurácia da IA utilizada.
Inicialmente:
- olist_customers_dataset.csv
- olist_geolocation_dataset.csv
- olist_order_items_dataset.csv
- olist_order_payments_dataset.csv
- olist_order_reviews_dataset.csv
- olist_orders_dataset.csv
- olist_products_dataset.csv
- olist_sellers_dataset.csv
- product_category_name_translation.csv

## Filtragem e Normalização
Após o merge de todas as tabelas do dataset, os atributos menos relevantes para a variável decision_score foram removidos para facilitar o aprendizado
do modelo e tornar a tabela mais limpa. O uso de variáveis sem correlação com nota dos clientes pode distorcer a saída do algoritmo.

# Aprendizado
Após todo processo de análise dos dados, o dataset foi seperado em duas partes:
- 30 % para teste do modelo (validação)
- 70 % para treino do modelo

## Bibliotecas dos modelos e funções/métricas 
Scikit learn: https://scikit-learn.org/stable/

# Teste
As funções e métricas utilizadas, bem como a conclusão do estudo está no final do código.











