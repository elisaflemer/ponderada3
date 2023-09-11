# Ponderada 3

A atividade ponderada 3 solicitava o treinamento de um modelo preditivo e o seu deploy em uma API local. O modelo deveria ser feito com base em um dos datasets pré-selecionados. Nesse contexto, foi escolhido o dataset de Customer Segmentation por sua simplicidade, facilitando o processo de feature engineering. Assim, este projeto traz um modelo preditivo que recebe dados de idade, renda anual e sexo do cliente e estima seu score como cliente. Ele foi treinado com um regressor de Random Forest e deployado com uma API de FastAPI. Uma interface simples também é servida na API. O app foi containerizado e deployado no DockerHub neste link: https://hub.docker.com/repository/docker/elisaflemer/ponderada3/general

## Como rodar
Para executar a aplicação, rode o seguinte comando:

```
docker run -d -p 8000:8000 elisaflemer/ponderada3:1.0
```

Para acessar a interface, acesse http://localhost:8000;

Para acessar a documentação da API, acesse http://localhost:8000/redoc;

## Treinamento do modelo

Neste tutorial, você encontrará um exemplo abrangente de treinamento de um modelo de regressão em Python. O objetivo principal é demonstrar como conduzir diversas etapas cruciais ao trabalhar com dados e modelos de aprendizado de máquina. Aqui está uma visão geral das principais etapas:

Carregando os Dados:
A primeira etapa envolve a importação das bibliotecas necessárias e a leitura dos dados de um arquivo CSV. Neste exemplo, usamos a biblioteca Pandas para carregar um conjunto de dados que contém informações sobre clientes de um shopping center. Isso é fundamental, pois os dados são a base de qualquer modelo de aprendizado de máquina.

Exploração dos Dados:
Uma análise inicial dos dados é crucial para entender seu conteúdo. Nessa fase, exibimos as primeiras linhas do conjunto de dados e calculamos estatísticas resumidas. Essa exploração inicial nos ajuda a identificar tendências, outliers e entender a natureza dos dados.

Visualização de Dados:
A visualização é uma ferramenta poderosa para compreender os dados. Utilizamos gráficos, como pairplots para identificar relações entre variáveis, heatmap de correlação para avaliar as associações entre elas e histogramas para examinar as distribuições de características específicas. Essas visualizações ajudam a criar uma imagem mais clara dos dados e a tomar decisões informadas sobre o modelo.

Pré-processamento dos Dados:
Nesta etapa, realizamos manipulações nos dados para prepará-los para o treinamento do modelo. Isso inclui a renomeação de colunas para facilitar a referência e a codificação de variáveis categóricas usando one-hot encoding. Essas transformações são necessárias para que os dados sejam compatíveis com os algoritmos de aprendizado de máquina.

Normalização dos Dados:
A normalização é importante para garantir que todas as features tenham a mesma escala, o que pode melhorar o desempenho do modelo. Isso é especialmente relevante quando se trabalha com algoritmos sensíveis à escala dos dados. Neste exemplo, aplicamos a normalização Min-Max às colunas, exceto à variável de destino.

Treinamento do Modelo:
A parte central do tutorial aborda o treinamento de três modelos de regressão diferentes: Random Forest Regressor, AdaBoost Regressor e K-Nearest Neighbors (KNN) Regressor. Esses modelos são treinados para prever a variável de destino (Score) com base nas outras features. O objetivo é encontrar um modelo que melhor se ajuste aos dados.

Salvar o Modelo Treinado:
Por fim, demonstramos como salvar o modelo treinado em um arquivo. Isso é importante para que o modelo possa ser reutilizado sem a necessidade de treiná-lo novamente toda vez que for necessário fazer previsões com base nos dados. Essa etapa é fundamental para a implementação prática de modelos de aprendizado de máquina em aplicações do mundo real.