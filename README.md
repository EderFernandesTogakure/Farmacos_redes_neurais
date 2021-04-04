# Avaliação do polimorfismo de fármacos utilizados para produção de medicamentos através do algoritmo de machine learning.
## Apresentação
  O presente projeto foi originado no contexto das atividades da disciplina de pós-graduação [Ciência e Visualização de Dados em Saúde](https://github.com/datasci4health/home), oferecida no primeiro semestre de 2021, na Unicamp.
Nome	                     |   RA	  |Especialização
---------------------------|--------|---------------
Eder Carlos Fernandes	     | 208418	|Computação
Gabriel Santos Martins Dias| 172441	|Computação
Wellen Góbi Botain         | 224798 |Saúde
Wellington Cesar Alves     | 261819 |Saúde

## Descrição Resumida do projeto 

   O polimorfismo de fármacos, representa um enorme desafio para a indústria farmacêutica, que busca, constantemente, desenvolver produtos farmacêuticos de qualidade, pois a descoberta de distintas formas cristalinas e sua influência no preparo de medicamentos, influencia de forma direta na saúde do usuário, pois pode acarretar prejuízos tanto ao paciente quanto a indústria.
  
   O ponto de partida para a fabricação de fármacos é a pré-formulação, sendo a primeira fase do desenvolvimento de formas farmacêuticas voltadas para a substância farmacologicamente ativa. Nesta fase ocorre a análise do fármaco em suas características físico-químicas como solubilidade, presença ou não de formas polifórmicas e seu comportamento frente à excipientes farmacêuticos ou outras substâncias farmacologicamente ativas.
  
   Na indústria farmacêutica o polimorfismo é considerado um parâmetro fundamental na fabricação de medicamentos sólidos, pois a criação de um fármaco sob uma ou outra forma cristalina implica nas propriedades físico-químicas desta substância, que irão afetar diretamente a solubilidade, e consequentemente a biodisponibilidade ou cinética.
  
   A motivação deste trabalho é desenvolver um algoritmo machine learning, que agilize esse processo de identificação do polimorfismo dos fármacos, agilizando seu processo de identificação. Deseja-se utilizar esta disciplina para apresentar essa possibilidade em uma situação real, da prática cotidiana.
## Pergunta de pesquisa

O algoritmo machine learning desenvolvido é eficaz na identificação de polimorfos de fármacos?

## Base de dados 

As bases de dados utilizadas serão imagens de processos de identificação de componentes farmacos feitas em microscópios ópticos, nas quais estes componentes são feitos de forma manual. 

As informações obtidas na imagem sobre estes componentes é a sua interpretação de qual tipo de componentes farmacos foram encontrado na imagem.

## Objetivos do Projeto

O projeto possui como objetivo principal a criação de um algoritmo machine learning que auxilie na identificação do polimorfismo de fármacos. Busca-se também:

* Identificar se o algoritmo machine learning é eficaz nessa identificação;
* Verificar sua capacidade de identificação;
* Avaliar sua disponibilidade de utilização.

## Metodologia 

  Obtenção da Base de Dados: Foi utilizado um Microscópio Óptico para se obter dezenas de imagens. Em seguida, sobre essas imagens, foi utilizado o processo de Data Augmentation (Aumento de dados de imagem) para gerar novas imagens de treinamento a fim de aumentar a generalidade do modelo e reduzir um possível overfitting (modelo treinado apenas para imagens utilizadas no estudo). 
  
  Foram produzidas imagens a partir de pequenas transformações nos arquivos obtidos no Microscópio Óptico e foi possível compor um conjunto de base de treinamento com centenas de imagens. 
Abaixo, segue imagem ilustrando o processo.

![imagem_projeto1](https://user-images.githubusercontent.com/25067632/113519352-fd5c8f00-9561-11eb-9cf8-d5b48720f447.jpg)

## Ferramentas

  As ferramentas que serão utilizadas neste projeto são:
  
  * Jupyter Notebook: Aplicação web utilizada como IDE. O Jupyter Notebook fornece um ambiente de ciência de dados interativo e fácil de usar em muitas linguagens de programação que não funciona apenas como um IDE, mas como uma  ferramenta didática;
  * Google Colab: Ambiente de programação que fornece um poderoso recurso de computação científica  para executar códigos de Machine Learning a partir de uma GPU presente no servidor;
  * Pythorch: Biblioteca de programação de código aberto usada para desenvolvimento de softwares de Machine Learning e Deep Learning;
  * YOLO: Biblioteca de código aberto de visão computacional utilizada para detecção e classificação de objetos em tempo real;
  * Darknet: Arquitetura de rede neural profunda utilizada no YOLO;
  * OpenCV:Biblioteca de programação de código aberto amplamente empregada no desenvolvimento de aplicativos na área de visão computacional;
  * Microscópio Óptico: Utilizado para fazer a captura de um conjunto de 20 imagens de 2 compostos distintos. 

## Detalhamento e evolução do projeto

O projeto adotou tecnologia baseada em redes neurais convolucionais, ou seja, para um melhor entendimento, inteligência artificial em conjunto com processamento de imagens.
Veja a figura abaixo uma figura demonstrando os passos para elaboração do projeto.

![imagem_projeto2](https://user-images.githubusercontent.com/25067632/113519557-6d1f4980-9563-11eb-8c51-af6f37edc15c.jpg)

Será detalhado todos os processos da imagem acima:

* Obtendo datasets. Os datasets são as imagens as quais serão inseridas no sistema para o treinamento da detecção dos polimorfos, quanto mais imagens forem obtidas para o treinamento e teste, maior será a precisão da detecção;
* O pré-processamento e aumento das imagens. Nesta etapa, são extraídas as imagens originais, ou seja, os datasets das imagens inserido no sistema e faz as cópias delas com pequenas alterações nos arquivos para aumentar a precisão das detecções;
* Classificação das imagens. Esta etapa é muito importante para um bom treinamento da rede neural convolucional, pois somente inserir as imagens no sistema não é o suficiente. Deve-se classificar os compostos dentro da imagem a serem treinados, ou seja, demonstrar cada polimorfo, demarcando-os com uma ferramenta específica de classificação;
* Processo de execução dos treinos e testes de validação de dados. Nesta etapa do processo, é realizado o treinamento da rede neural convolucional, ou seja, está sendo ensinado como detectar os compostos descritos na imagem;
* Execução dos dados treinados e validados em produção. Esta é a etapa final, na qual a rede neural foi treinada e agora fará a detecção dos polimorfos da maneira que foi programada. 

## Resultados esperados

  Espera-se que esse algoritmo seja eficaz na identificação de polimorfos em fármacos de forma rápida, precisa, exata, segura, livre de erros de interpretação humana e que agilize o processo.
  
## Cronograma

![cronograma](https://user-images.githubusercontent.com/25067632/113520254-27b14b00-9568-11eb-9a95-017eb2a383a7.jpg)












