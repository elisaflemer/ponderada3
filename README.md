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

O treinamento do modelo está melhor descrito no notebook. Em suma, foi realizada a exploração dos dados com a análise estatística e de gráficos, o one-hot encoding dos valores categóricos, a normalização dos valores numéricos e o treinamento com trẽs regressores populares: Random Forest, Adaboost e KNN. A métrica utilizada foi o erro médio absoluto, e o modelo que performou melhor foi o Random Forest.