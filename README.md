# Avaliação do polimorfismo de fármacos utilizados para produção de medicamentos através do algoritmo de machine learning.
## Apresentação
  O presente projeto foi originado no contexto das atividades da disciplina de pós-graduação [Ciência e Visualização de Dados em Saúde](https://github.com/datasci4health/home), oferecida no primeiro semestre de 2021, na Unicamp.
Nome	                     |   RA	  |Especialização
---------------------------|--------|---------------
Eder Carlos Fernandes	     | 208418	|Computação
Gabriel Santos Martins Dias| 172441	|Computação
Wellen Góbi Botacin         | 224798 |Saúde
Wellington Cesar Alves     | 261819 |Saúde

Link do video de apresentação do trabalho 
[Video de apresentação de Ciência de Dados em Saúde](https://youtu.be/IGkQDs6klbo).

## Descrição Resumida do projeto 

   Um determinado fármaco, no estado sólido, pode se apresentar em diferentes formas. Estas formas incluem polimorfos (capacidade de uma substância se apresentar em duas ou mais formas cristalinas) e amorfos (formas sólidas que não têm nenhuma ordem molecular).
   
  O fenômeno do polimorfismo apresenta um desafio na indústria farmacêutica que pretende desenvolver medicamentos de qualidade, pois o desconhecimento das diferentes formas cristalinas e a influência destas no preparo de um medicamento poderá acarretar em grandes prejuízos para a saúde do paciente. Com isso, a pesquisa na área de polimorfismo é extremamente necessária e atual, sendo um assunto que não deve ser encarado somente como um problema, mas como um processo, que deve ser estudado e monitorado, desde a síntese da substância ativa até o armazenamento, resultando em maior qualidade aos medicamentos.
  
  A capacidade de uma molécula cristalizar em duas ou mais formas é definida como polimorfismo.
  
  Polimorfos diferentes de um mesmo composto geralmente apresentam diferenças significativas de solubilidade, processabilidade e estabilidade física e química. Estas diferenças físico-químicas modificam o comportamento da molécula quando em um meio biológico, inclusive podendo alterar sua biodisponibilidade.
  
  Embora uma molécula orgânica de um sólido possa existir sob duas ou mais formas cristalinas, apenas uma destas formas é termodinamicamente estável a uma determinada pressão e temperatura, com níveis energéticos potencialmente mais baixos, devido à redução do seu volume molecular em relação aos amorfos ou outro estado desordenado. Em geral, a forma mais estável (menor energia livre) de uma substância polimórfica exibe um ponto de fusão mais alto e menor solubilidade com o máximo de estabilidade química, ou seja, mantém sua integridade química dentro de limites especificados e as mesmas propriedades e características durante o período de armazenamento e uso (RAW et al., 2004; VISHWESHWAR et al., 2006).
  
  O polimorfismo pode também resultar em alterações na estabilidade química, principalmente para compostos com predisposição à degradação no estado sólido (ARAÚJO, 2009). Porém, dentre as consequências do polimorfismo, a mais crítica é a diferença na biodisponibilidade dos diferentes polimorfos de um fármaco, uma vez que, a velocidade de absorção de um fármaco depende da sua velocidade de dissolução, podendo torná-lo menos ativo, inativo ou tóxico de acordo com o tipo de polimorfo empregado (FERREIRA, 2011; CUFFINI et al., 2011).

## Pergunta de pesquisa

O algoritmo machine learning desenvolvido é eficaz na identificação de polimorfos de fármacos para auxiliar a industria farmaceutica na produção de medicamentos de melhor solubilidade?

## Objetivos do Projeto

O projeto possui como objetivo principal a criação de um algoritmo machine learning que auxilie na identificação do polimorfismo de fármacos. Busca-se também:

* Identificar se o algoritmo machine learning é eficaz nessa identificação;
* Verificar sua capacidade de identificação;
* Avaliar sua disponibilidade de utilização.

## Metodologia 

  Obtenção da Base de Dados: Foi utilizado um Microscópio Óptico para se obter dezenas de imagens. Em seguida, sobre essas imagens, foi utilizado o processo de Data Augmentation (Aumento de dados de imagem) para gerar novas imagens de treinamento a fim de aumentar a generalidade do modelo e reduzir um possível overfitting (modelo treinado apenas para imagens utilizadas no estudo). 
  
  Foram produzidas imagens a partir de pequenas transformações nos arquivos obtidos no Microscópio Óptico e foi possível compor um conjunto de base de treinamento com centenas de imagens. 
Abaixo, segue imagem ilustrando o processo.

![relatório](https://user-images.githubusercontent.com/25067632/120075355-4ec35f00-c077-11eb-9fa7-cd96279ef307.jpg)

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

O projeto irá adotar tecnologia baseada em redes neurais convolucionais, ou seja, para um melhor entendimento, inteligência artificial em conjunto com processamento de imagem
Veja a figura abaixo uma figura demonstrando os passos para elaboração do projeto.

![imagem_projeto2](https://user-images.githubusercontent.com/25067632/113519557-6d1f4980-9563-11eb-8c51-af6f37edc15c.jpg)

Será detalhado todos os processos da imagem acima:

* Primeiro tópico obtendo datasets. Os datasets são as imagens que serão inseridas no sistema para o treinamento da detecção dos polimorfos, quanto mais imagens forem obtidas para o treinamento e teste, maior será a precisão da detecção;
* O pré-processamento e aumento das imagens. Nesta etapa, são extraídas as imagens originais, ou seja, os datasets das imagens são inseridos no sistema e faz as cópias delas com pequenas alterações nos arquivos para aumentar a precisão das detecções;
* Classificação das imagens. Esta etapa é muito importante para um bom treinamento da rede neural convolucional, pois somente inserir as imagens no sistema não é o suficiente. Deve-se classificar os compostos dentro da imagem a serem treinados, ou seja, demonstrar cada polimorfo, demarcando-os com uma ferramenta específica de classificação;
* Processo de execução dos treinos e testes de validação de dados. Nesta etapa do processo, é realizado o treinamento da rede neural convolucional, ou seja, está sendo ensinado como detectar os compostos descritos na imagem;
* Execução dos dados treinados e validados em produção. Esta é a etapa final, na qual a rede neural foi treinada e agora fará a detecção dos polimorfos da maneira que foi programada. 

## Bases de Dados e Evolução
  As bases de dados utilizadas serão imagens de processos de identificação de componentes fármacos feitas em microscópios óticos de forma manual. 

Base de Dados              |  Endereço na Web  |Especialização
---------------------------|-------------------|---------------
Imagens Carbazepina        | https://drive.google.com/drive/folders/18DAq2LHdic0h5BrjEQ0FzsVOsHl3ztD3?usp=sharing	           |Imagens tirados diretos do microscopio forma 1 e 3,foi separado as imagens de treino e teste, utilizando redes neurais convolucionais para detecção dos fármacos.

## Resultados esperados

  Espera-se que esse algoritmo seja eficaz na identificação de polimorfos em fármacos de forma rápida, precisa, exata, segura, livre de erros de interpretação humana e que agilize o processo.
  
## Cronograma

![cronograma](https://user-images.githubusercontent.com/25067632/113520254-27b14b00-9568-11eb-9a95-017eb2a383a7.jpg)

## Referências:

ARAUJO, G. L. B. Caracterização no estado sólido dos polimorfos de tibolona. Tese (Doutorado em Farmácia) - Faculdade de Ciências Farmacêuticas, Universidade de São Paulo, São Paulo, 2009. 

CUFFINI, S. L.; PITALUGA, J. R. A; TOMBARI, D. Polimorfismo em fármacos. In: STORPIRTIS, S.; GONÇALVES, J. E.; CHIANN, C.; GAI, M. N.; editors. Biofarmacotécnica. Rio de Janeiro: Guanabara Koogan, 2011, p.21-31.

Documentação do tensorflow. Tensorflow, 2021. Disponível em: <https://www.tensorflow.org/api_docs/python/tf?hl=pt-br>. Acesso em: 26 abr. 2021.

FERREIRA, A. O. Guia Prático da Farmácia Magistral. 4. ed. São Paulo: Pharmabooks, 2011. 736 p.

RAW, A. S; FURNESS, M. S.; GILL, D. S.; ADAMS, R. C.; HOLCOMBE JR, F. O.; YU, L. X. Regulatory considerations of pharmaceutical solid polymorphism in Abbreviated New Drug Applications (ANDAs). Advanced Drug Deliveries Amsterdam, v. 56, n.3, p. 397-414, fev. 2004.

VISHWESHWAR, P.; MCMAHON, J. A.; BIS, J. A.; ZAWOROTKO, M. J. Pharmaceutical co-crystals. Journal of Pharmaceutical Sciences, v.95, n.3, p.499516, mar. 2006.

YOLO v3 theory explained. Pylessons, 2019. Disponível em: <https://pylessons.com/YOLOv3-introduction/>. Acesso em: 26 abr. 2021.

YOLO: Real-Time Object Detection . pjreddie, 2018. Disponivel em: < https://pjreddie.com/darknet/yolo/>. Acesso em: 26 Abr. 2021














