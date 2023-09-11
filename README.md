# Ponderada 3

A atividade ponderada 3 solicitava o treinamento de um modelo preditivo e o seu deploy em uma API local. O modelo deveria ser feito com base em um dos datasets pré-selecionados. Nesse contexto, foi escolhido o dataset de Customer Segmentation por sua simplicidade, facilitando o processo de feature engineering. Assim, este projeto traz um modelo preditivo que recebe dados de idade, renda anual e sexo do cliente e estima seu score como cliente. Ele foi treinado com um regressor de Random Forest e deployado com uma API de FastAPI. Uma interface simples também é servida na API. O app foi containerizado e deployado no DockerHub neste link: https://hub.docker.com/repository/docker/elisaflemer/ponderada3/general

## Como rodar
Para executar a aplicação, rode o seguinte comando:

```
docker run -d -p 8000:8000 elisaflemer/ponderada3:1.0
```

Para acessar a interface, acesse http://localhost:8000;

Para acessar a documentação da API, acesse http://localhost:8000/redoc;

## Ambiente de desenvolvimento

Para configurar e rodar o ambiente de desenvolvimento com base no repositório clonado, você pode seguir estas instruções gerais:

### Clonar o Repositório

1. Abra seu terminal ou prompt de comando.

2. Navegue até o diretório onde você deseja clonar o repositório usando o comando `cd`. Por exemplo:

   ```bash
   cd /caminho/para/o/seu/diretorio
   ```

3. Clone o repositório para o seu ambiente local usando o comando `git clone`:

   ```bash
   git clone https://github.com/seu-usuario/seu-repo.git
   ```

### Configurar o Ambiente Virtual (Opcional, mas recomendado)

4. Mude para o diretório do repositório clonado:

   ```bash
   cd seu-repo
   ```

5. Crie um ambiente virtual para isolar as dependências do projeto. Você pode usar a ferramenta `venv` para isso (certifique-se de que o Python 3.x esteja instalado em seu sistema):

   ```bash
   python3 -m venv venv
   ```

6. Ative o ambiente virtual:

   - No Windows:

     ```bash
     venv\Scripts\activate
     ```

   - No macOS e Linux:

     ```bash
     source venv/bin/activate
     ```

### Instalar Dependências

7. Certifique-se de que você está no diretório raiz do seu repositório clonado.

8. Instale as dependências listadas no arquivo `requirements.txt` usando o `pip`:

   ```bash
   pip install -r requirements.txt
   ```

### Rodar o Ambiente de Desenvolvimento

9. Após instalar as dependências, você pode rodar o ambiente de desenvolvimento. As instruções exatas podem variar dependendo do tipo de aplicação que você está desenvolvendo (web, aplicativo, etc.). 

   Por exemplo, se estiver trabalhando em um projeto Python com um servidor web, você pode usar o seguinte comando para iniciar o servidor:

   ```bash
   python app.py
   ```

   Certifique-se de consultar a documentação do projeto ou as instruções específicas do aplicativo para saber como rodá-lo em seu ambiente de desenvolvimento.

Essas são instruções gerais para configurar um ambiente de desenvolvimento com base em um repositório clonado. Certifique-se de ajustar as etapas de acordo com as necessidades específicas do seu projeto e seguir as instruções do README do repositório, se houver, para obter informações adicionais sobre como configurar e rodar o projeto.

## Treinamento do modelo

O treinamento do modelo está melhor descrito no notebook. Em suma, foi realizada a exploração dos dados com a análise estatística e de gráficos, o one-hot encoding dos valores categóricos, a normalização dos valores numéricos e o treinamento com trẽs regressores populares: Random Forest, Adaboost e KNN. A métrica utilizada foi o erro médio absoluto, e o modelo que performou melhor foi o Random Forest.