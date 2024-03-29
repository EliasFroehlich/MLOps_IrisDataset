# MLOps - IrisDataset

## Introdução
Desafio da área de Machine Learning com o dataset Iris.
Este é um dataset clássico para classificação de plantas.

Este repositório pode ser dividido em duas entregas:
1. Avaliação dos dados e treinamento do modelo de classificação e testes, ao qual utilizei o Jupyter Notebook para tal. Este arquivo é o "Desafio_VF". Os comentários estão no arquivo de treinamento.
2. Disponibilizar a API REST em uma imagem Docker para que possa ser testada localmente.


## Desenvolvimento da API
A API foi desenvolvida por meio do Flask, instaciando um objeto para a execução e definindo as rotas. Esta aplicação encontra-se no arquivo "api.py".
Primeiramente, o arquivo contendo o modelo treinado foi importado, e então foram definidas as rotas, onde a primeira serve de teste para avaliar se a mesma encontra-se online, e a outra é aplicada no método POST para realizar a classificação e retornar o resultado. Os valores recebidos são convertidos para um array Numpy, para então retornar a predição. O retorno desse modelo é binário, assim vamos montar um dicionário em Python com o resultado e por fim finalizar a requisição com um JSON como resultado. O endereço desta API é localhost:5000/predict.
Para testar a coerência da classificação, utilizei o Postman, inserindo os parâmetros conforme imagem.
![image](https://user-images.githubusercontent.com/48781421/147155366-d0acb292-7912-4bcd-ba35-02f9df675be3.png)

Os valores numéricos de envio podem ser alterados no primeiro quadro para realização de testes com diferentes dados. O arquivo "post.json" anexado pode ser utilizado como referência de envio.


## Teste da API com o Docker
Por não ter experiência na criação de imagem Docker, não consegui disponibilizar a mesma para acessar externamente. Na execução do docker run image, acusou erro de que a pasta raíz não estava sendo encontrada. O ID da imagem gerado foi o 11ebea5dab98.
Dado o tempo para entrega do desafio, não consegui estudar o suficiente para passar por este problema.
Para o desenvolvimento do Docker, foram utilizados os arquivos "docker-compose.yml" e "Dockerfile", 
