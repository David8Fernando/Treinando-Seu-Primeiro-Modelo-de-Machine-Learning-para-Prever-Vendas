# Treinando Seu Primeiro Modelo de Machine Learning para Prever Vendas

## Objetivo

O objetivo deste projeto é desenvolver um modelo de regressão preditiva que permita: 

✅ Treinar um modelo de Machine Learning para prever as vendas de sorvete com base na temperatura do dia.
✅ Registrar e gerenciar o modelo usando o MLflow.
✅ Implementar o modelo para previsões em tempo real em um ambiente de cloud computing.
✅ Criar um pipeline estruturado para treinar e testar o modelo, garantindo reprodutibilidade.


## Base de Dados
A base de dados foi gerada com auxílio do ChatGPT para fins de aprendizado
Foi utilizado o seguinte prompt:

> Gere uma tabela de vendas de sorvete que contenha as colunas de data, quantidade de vendas e a temperatura.
> 
> Essa tabela deve conter 100 registros


## Preparação do Ambiente Azure

Para esse projeto foi necessário a preparação do ambiente Azure Machine Learning
### 1. Criação do grupo de recurso
![alt](https://github.com/David8Fernando/Treinando-Seu-Primeiro-Modelo-de-Machine-Learning-para-Prever-Vendas/blob/main/img/img1_grupo_recursos.png) 

![alt](https://github.com/David8Fernando/Treinando-Seu-Primeiro-Modelo-de-Machine-Learning-para-Prever-Vendas/blob/main/img/img2_criar_grupo_recursos.png) 

![alt](https://github.com/David8Fernando/Treinando-Seu-Primeiro-Modelo-de-Machine-Learning-para-Prever-Vendas/blob/main/img/img3_criar_grupo_recursos.png) 


### 2. Criação do recurso Azure Machine Learning

![alt](https://github.com/David8Fernando/Treinando-Seu-Primeiro-Modelo-de-Machine-Learning-para-Prever-Vendas/blob/main/img/img4_criar_recurso.png) 

![alt](https://github.com/David8Fernando/Treinando-Seu-Primeiro-Modelo-de-Machine-Learning-para-Prever-Vendas/blob/main/img/img4_recurso_AzureML.png) 

Aguarde uns minutos até a finalização da criação do recurso

### 3. Inicie o Azure Machine Learning
Selecione o Workspace criado
![alt](https://github.com/David8Fernando/Treinando-Seu-Primeiro-Modelo-de-Machine-Learning-para-Prever-Vendas/blob/main/img/img5_acessoAzureML.png) 

Clique em **Launch studio**

![alt](https://github.com/David8Fernando/Treinando-Seu-Primeiro-Modelo-de-Machine-Learning-para-Prever-Vendas/blob/main/img/img5_iniciarAzureML.png) 


Você também pode acessar pelo endereço https://ml.azure.com


## Utilizando o ambiente no Azure Machine Learning


No Azure ML vá em computação e crie a instância de computação e cluster de computação

a instância de computação vai ser servir para fazer testes no jupyter notebook

o cluster de computação será utilizado para treinamento do modelo

### Criando Dataset

crie o dataset usando um arquivo local
![alt](https://github.com/David8Fernando/Treinando-Seu-Primeiro-Modelo-de-Machine-Learning-para-Prever-Vendas/blob/main/img/img6dataset.png) 

remova a coluna de data de venda
![alt](https://github.com/David8Fernando/Treinando-Seu-Primeiro-Modelo-de-Machine-Learning-para-Prever-Vendas/blob/main/img/img6removedata.png) 

dataset criado
![alt](https://github.com/David8Fernando/Treinando-Seu-Primeiro-Modelo-de-Machine-Learning-para-Prever-Vendas/blob/main/img/img6rdatasetcriado.png) 


### ML Automatizado
Crie um modelo de Machine Learning Automatizado e selecione o tipo de modelo: regressão e selecione os dados
![alt](https://github.com/David8Fernando/Treinando-Seu-Primeiro-Modelo-de-Machine-Learning-para-Prever-Vendas/blob/main/img/img_tiposdemodeloML.png) 

O Target Column ou Coluna de destino (o que quero que seja previsto) seleciono a coluna de quantidade vendidas


Bloqueie os modelos que não serão utilizados

![alt](https://github.com/David8Fernando/Treinando-Seu-Primeiro-Modelo-de-Machine-Learning-para-Prever-Vendas/blob/main/img/img6configadicional.png) 

![alt](https://github.com/David8Fernando/Treinando-Seu-Primeiro-Modelo-de-Machine-Learning-para-Prever-Vendas/blob/main/img/img6config_remove.png) 

Os limites para o modelo foram definidos como:

**Max nodes:** 2
**Experiment timeout (minutes):** 15
**Iteration timeout (minutes):*** 15
**Habilite encerramento antecipado** 

#### Resultado encontrado no ML Automatizado

![alt](https://github.com/David8Fernando/Treinando-Seu-Primeiro-Modelo-de-Machine-Learning-para-Prever-Vendas/blob/main/img/resultado designer.png) 

Também foi treinado o modelo pelo Designer

![alt](https://github.com/David8Fernando/Treinando-Seu-Primeiro-Modelo-de-Machine-Learning-para-Prever-Vendas/blob/main/img/resultado designer 1.png) 



