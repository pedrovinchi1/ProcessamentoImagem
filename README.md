# Flowers Classification
Classificação de imagens utilizando Redes Neurais Convolucionais.

## Autor: 
* Pedro Henrique Ferreira Vinchi
* RA: 1999010

## Links Repositórios:
* Google Drive: https://drive.google.com/drive/folders/1r-g312BL-wxcMC1KAg3iHwzNn6IrMYuZ?usp=sharing
* Github: https://github.com/pedrovinchi1/ProcessamentoImagem

## Objetivos
Este projeto tem como objetivo a classificação de flores utilizando técnicas de processamento de imagens e aprendizado de máquina. O código foi desenvolvido em Python e utiliza bibliotecas para manipulação de dados, processamento de imagens e construção de modelos de aprendizado profundo.

## Tecnologias Utilizadas
* Python

Python foi escolhido como a linguagem de programação principal devido à sua simplicidade e vasta gama de bibliotecas para aprendizado de máquina e processamento de imagens.

* TensorFlow e Keras

TensorFlow: Biblioteca de código aberto para computação numérica e aprendizado de máquina.
Keras: API de alto nível para construção e treinamento de modelos de aprendizado profundo, integrada ao TensorFlow.
* Matplotlib

Biblioteca para criação de gráficos e visualizações de dados.

* Scikit-learn

Utilizada para métricas de avaliação como classification_report, confusion_matrix e accuracy_score.

* Kaggle API

Utilizada para baixar o dataset de flores diretamente do Kaggle.

## Instruções para Importação do Dataset
```
!pip install -q kaggle
```

```
!mkdir -p ~/.kaggle
```

```
# Aqui subir o Arquivo kaggle.json com a key do kaggle. Arraste o arquivo até o diretório do Google Colab
```

```
!mv kaggle.json ~/.kaggle/
```

```
!chmod 600 ~/.kaggle/kaggle.json
```

```

!kaggle datasets download -d alxmamaev/flowers-recognition

```

```
!unzip -q flowers-recognition.zip
```

## Estrutura do Código
1. Preparação do Ambiente
O código começa com a instalação e configuração da API do Kaggle para baixar o dataset de flores.

2. Organização dos Dados
Os dados são organizados em diretórios de treino e validação para duas classes específicas: daisy e rose.

3. Carregamento e Pré-processamento de Imagens
Funções para carregar e pré-processar as imagens de treino e validação utilizando ImageDataGenerator do Keras.

4. Construção do Modelo
Utilização do modelo InceptionV3 pré-treinado para transfer learning.

5. Treinamento do Modelo
Treinamento inicial com as camadas do modelo base congeladas e posteriormente fine-tuning.

6. Avaliação do Modelo
Funções para plotar a matriz de confusão, histórico de treinamento e avaliar o modelo.

7. Pipeline Principal
Execução do pipeline principal que carrega os dados, cria e compila o modelo, realiza o treinamento inicial, fine-tuning e avaliação final.

## Estratégias Utilizadas
1. Transfer Learning: Utilização do modelo InceptionV3 pré-treinado para aproveitar o conhecimento adquirido em grandes datasets e aplicá-lo ao problema específico de classificação de flores.
2. Data Augmentation: Aumento do dataset de treino através de técnicas de transformação de imagens para melhorar a generalização do modelo.
3. Fine-Tuning: Ajuste fino das últimas camadas do modelo pré-treinado para melhorar a performance no dataset específico.
4. Early Stopping: Parada antecipada do treinamento para evitar overfitting.
5. Model Checkpointing: Salvamento dos melhores pesos do modelo durante o treinamento para garantir a melhor performance.

## Resultados Obtidos
* Acurácia: 96.13%
* F1-Score: 0.96
* Recall: 0.95
* Precisão: 0.96

## Conclusão
Este projeto ostra a aplicação de técnicas avançadas de aprendizado de máquina e processamento de imagens para a classificação de flores. A utilização de transfer learning e data augmentation foram muito importantes para alcançar bons resultados, mesmo com um dataset limitado.
