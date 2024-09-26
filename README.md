# Titanic
Repositório criado para [competição do Kaggle sobre o desastre no Titanic](https://www.kaggle.com/competitions/titanic)  
<img src="https://raw.githubusercontent.com/HaallanP/Titanic/main/img/GR%C3%81FICO.png" alt="Gráfico do Titanic" />
___
### [Etapa 1: Primeiro modelo](https://github.com/HaallanP/Titanic/blob/main/Party1.ipynb)

- Nessa etpa fizemos apenas o básico para conseguir verificar qual seria o resultado sem fazer nenhum tratamento nem engenharia dos dados
    - Foi visualizado um resumo da base utilizando o Ydata-profiling, biblioteca capaz de gerar com poucas linhas toda a descrição do nosso dataset.
    - Também eliminamos colunas elevadas cardinalidade, tratamos valores vazios ultilizando a média e a moda das variáveis e eliminamos todas as colunas de texto.
    - Criamos modelos ultilizamos 3 algoritmos: Árvore de Classificação, KNN e Regressão Logística e avaliamos esses modelos ultilizando a acurácia e a matriz de confusão.
    - O score publicos retornado pelo Kaggle foi: 0,6675

___
### [Etapa 2: Tratando as variáveis de texto](https://github.com/HaallanP/Titanic/blob/main/Party2.ipynb)
- Na segunda etapa o foco principal foi tratar as variáveis de texto para conseguirmos ultilizar todas as variáveis no nosso modelo.
    - Para fazer esse tratamento, ultilizamos a lambda function e OneHotEncoder
- Ultilizamos os mesmo modelos vistos anteriormente
- O score público retornando pelo Kaggle foi: 0,7656

___
  ### [Etapa 3: Aprofundando no negócio e melhorando os tratamentos dos dados](https://github.com/HaallanP/Titanic/blob/main/Party3.ipynb)

- Na Terceira etapa o grande objetivo era entender melhor os dados para fazer um melhor tratamento e tentar e melhorar o resultado obtido anteriormente.
- Então fizemso
    - O Ajuste na escala dos lados para as colunas Age e Fare
    - Entendemos melhor as colunas SibSp (n° de irmãos/conjuguês a bordo do Titanic) e Parch(n° de pais/filhos a bordo Titanic) e criamos 2 novas colunas total de familiares do navio e se o passageiro estava sozinho ou não.
    - Para finalizar, analisamos a correlação de todas as variáveis para selecionar aquelas mais faziam sentido para o modelo.
    - Ultilizamos os mesmo modelos vistos anteriormente
    - O score público retornado pelo Kaggle foi: 0,7703

___
### [Etapa 4: Selecionando outros algoritmos para fazer a previsão](https://github.com/HaallanP/Titanic/blob/main/Party4.ipynb)

- Nessa etapa vamos manter todas as colunas (incluindo SibSp e Parch) e ultilizar algoritmos para verificar o resultado do modelo.
- Os algoritmos que vamos utilizar nessa etapa sao a Regressão Logsítica (vamos manter pois o com melhores resultados nas etapas anteriores), RandomForest e MPLClassifier(Rede neurais).
- O MPLClassifoer (um algoritmo de Redes Neurais) obteve a maior acurácia nos dados de validação entre todos os modelos vistos até agora, porém ao usar esse modelo nos dados de teste(que faremos a submissão) o resultado foi o pior que na etapa 3, mostrando que provavelmente tivemos um overfitting do nosso modelo.
- O score público retornado pelo Kaggle foi: 0,6986

___
### [Etapa 5: Utilizando o GridSearchCV e determinando os melhores parâmentros](https://github.com/HaallanP/Titanic/blob/main/Party5.ipynb)

- Agora utilizamos o GridSearchCV para determinar os melhores parâmetros para os 3 modelos que utlizamos na etapa anterior
- Nesse caso, o modelo escolhido foi aquele utilizando o RandomForest e o resultado melhorou consideralvemnente em relação a etapa 4 e foi melhor na etapa 3.
- O score público retornado pelo Kaggle foi: 0,7823 









