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






