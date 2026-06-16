# FIAP - Faculdade de Informática e Administração Paulista

<p align="center">
<a href="https://www.fiap.com.br/">
<img src="assets/logo-fiap.png" alt="FIAP - Faculdade de Informática e Administração Paulista" border="0" width="40%" height="40%">
</a>
</p>

<br>

# CardioIA - Fase 4

## Assistente Cardiológico Virtual com Visão Computacional

---

## Integrantes

* Daniel
* Davi
* Enrico

---

## Sobre o Projeto

O **CardioIA** é um protótipo acadêmico desenvolvido na Graduação ON em Inteligência Artificial da FIAP, com o objetivo de aplicar técnicas de **Visão Computacional** e **Deep Learning** na análise de imagens médicas simuladas.

Nesta Fase 4, o projeto avança para a classificação de imagens de eletrocardiogramas, utilizando:

* Pré-processamento de imagens;
* Redes Neurais Convolucionais;
* Transfer Learning;
* Avaliação por métricas de classificação;
* Protótipo simples de apresentação dos resultados.

A proposta é demonstrar como modelos de Inteligência Artificial podem apoiar a interpretação inicial de exames médicos, sempre considerando que a solução possui finalidade acadêmica e não substitui avaliação clínica profissional.

---

## Objetivo da Atividade

Construir um protótipo de Assistente Cardiológico Virtual capaz de:

* Realizar o pré-processamento de imagens médicas simuladas;
* Treinar e avaliar uma CNN para classificação de imagens;
* Comparar uma CNN treinada do zero com um modelo baseado em Transfer Learning;
* Apresentar os resultados de forma acessível;
* Documentar as etapas técnicas do projeto.

---

## Dataset Utilizado

Foi utilizado um dataset público contendo imagens de eletrocardiogramas organizadas em quatro categorias:

* ECG Images of Myocardial Infarction Patients;
* ECG Images of Patient that have History of MI;
* ECG Images of Patient that have Abnormal Heartbeat;
* Normal Person ECG Images.

As imagens foram organizadas em pastas por classe, permitindo o carregamento automático dos dados pelo TensorFlow/Keras.

> O dataset foi utilizado exclusivamente para fins acadêmicos e experimentais.

---

## Parte 1 - Pré-processamento das Imagens

Na primeira etapa, foi desenvolvido o pipeline de preparação das imagens médicas.

Foram realizadas as seguintes etapas:

* Organização das imagens por classe;
* Redimensionamento para 224x224 pixels;
* Normalização dos valores dos pixels;
* Divisão dos dados em treino, validação e teste;
* Criação dos lotes de imagens para treinamento;
* Documentação das escolhas realizadas no pipeline.

O objetivo dessa etapa foi padronizar as imagens para permitir o treinamento correto dos modelos de classificação.

Relatório correspondente:

```text
docs/relatorio_pre_processamento.md
```

---

## Parte 2 - Classificação com CNN

Foi implementada uma Rede Neural Convolucional treinada do zero utilizando Python, TensorFlow e Keras.

A arquitetura da CNN foi composta por:

* Camadas convolucionais;
* Camadas de pooling;
* Camada Flatten;
* Camadas Dense;
* Camada final com ativação Softmax.

O modelo foi treinado com as imagens pré-processadas e avaliado por meio de métricas de classificação.

---

## Parte 3 - Transfer Learning

Também foi implementada uma abordagem utilizando **Transfer Learning** com o modelo pré-treinado **MobileNetV2**.

O objetivo foi comparar duas estratégias:

* Uma CNN simples construída e treinada do zero;
* Um modelo pré-treinado adaptado para o problema de classificação de imagens de ECG.

Essa comparação permitiu observar as vantagens e limitações de cada abordagem dentro do contexto do projeto.

Relatório correspondente:

```text
docs/relatorio_cnn_transfer_learning.md
```

---

## Métricas Utilizadas

Para avaliação dos modelos, foram utilizadas as seguintes métricas:

* Accuracy;
* Precision;
* Recall;
* F1-Score;
* Matriz de Confusão.

Essas métricas permitiram analisar o desempenho geral dos modelos e identificar possíveis erros de classificação entre as classes.

---

## Protótipo Desenvolvido

Foi desenvolvido um protótipo simples no Google Colab para simular o funcionamento do Assistente Cardiológico Virtual.

O protótipo permite:

1. Selecionar uma imagem de ECG;
2. Realizar o pré-processamento da imagem;
3. Executar a predição com o modelo treinado;
4. Exibir a classe prevista;
5. Exibir a classe real;
6. Exibir o nível de confiança da predição.

O objetivo do protótipo é tornar a interpretação dos resultados mais clara e acessível.

---

## Estrutura do Projeto

```bash
CARDIOIA-VISAO-COMPUTACIONAL
│
├── README.md
│
├── notebooks
│   └── cardioia_fase4_visao_computacional.ipynb
│
├── docs
│   ├── relatorio_pre_processamento.md
│   └── relatorio_cnn_transfer_learning.md
│
├── assets
│   ├── logo-fiap.png
│   ├── dataset_exemplo.png
│   ├── treinamento_cnn.png
│   ├── matriz_confusao_cnn.png
│   ├── matriz_confusao_transfer_learning.png
│   └── prototipo_cardioia.png
│
└── video
    └── link_video.txt
```

---

## Arquivo Principal da Entrega

O notebook principal da atividade está localizado em:

```text
notebooks/cardioia_fase4_visao_computacional.ipynb
```

Esse notebook contém:

* Carregamento do dataset;
* Pré-processamento das imagens;
* Treinamento da CNN;
* Treinamento com Transfer Learning;
* Avaliação dos modelos;
* Matrizes de confusão;
* Protótipo final de predição.

---

## Prints e Evidências

As evidências visuais da execução do projeto estão disponíveis na pasta:

```text
assets/
```

Arquivos principais:

* `dataset_exemplo.png`
* `treinamento_cnn.png`
* `matriz_confusao_cnn.png`
* `matriz_confusao_transfer_learning.png`
* `prototipo_cardioia.png`

---

## Tecnologias Utilizadas

* Python;
* Google Colab;
* TensorFlow;
* Keras;
* NumPy;
* Matplotlib;
* Scikit-Learn;
* MobileNetV2;
* CNN;
* Transfer Learning.

---

## Vídeo de Demonstração

O link do vídeo de demonstração está disponível em:

```text
video/link_video.txt
```

---

## Limitações e Considerações Éticas

O CardioIA é um protótipo acadêmico e não deve ser utilizado como ferramenta de diagnóstico médico.

Apesar de apresentar resultados satisfatórios no ambiente experimental, uma aplicação real exigiria:

* Validação clínica especializada;
* Bases de dados maiores e mais representativas;
* Análise de vieses;
* Testes de robustez;
* Segurança dos dados;
* Conformidade com normas regulatórias da área da saúde.

O sistema deve ser compreendido apenas como uma demonstração educacional de como a Visão Computacional pode apoiar a análise de imagens médicas.

---

## Conclusão

A Fase 4 do CardioIA permitiu aplicar conceitos de Visão Computacional, Deep Learning, CNN e Transfer Learning em um contexto relacionado à saúde cardiovascular.

O projeto demonstrou, de forma prática, como imagens médicas simuladas podem ser processadas, classificadas e apresentadas em um protótipo de apoio à decisão.

---

## Licença

<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1">
<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1">

<p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/">
<a property="dct:title" rel="cc:attributionURL" href="https://github.com/SabrinaOtoni/TEMPLATE-FIAP-GRAD-ON-IA">MODELO GIT FIAP</a> por 
<a rel="cc:attributionURL dct:creator" property="cc:attributionName" href="https://fiap.com.br">FIAP</a> está licenciado sobre 
<a href="http://creativecommons.org/licenses/by/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">Attribution 4.0 International</a>.
</p>
