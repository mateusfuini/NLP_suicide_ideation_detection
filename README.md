# Detecção de Ideação Suicida
# 1. Introdução
----
<a id="subsection_1_1"></a>
## 1.1 Descrição e motivação do problema


<p>O suicídio é um fenômeno social que afeta todos os países do mundo, constituindo um grave problema de saúde pública. Cerca de 700 mil indivíduos morrem todos os anos, sendo principalmente jovens e adultos de meia-idade que tentam o suicídio (MARTINS, 2021). No Brasil, é a terceira causa de morte de homens e a quarta causa de morte de mulheres entre os 15 e 29 anos de idade (MALTA, 2021).A ONU inseriu como um de seus objetivos de desenvolvimento sustentável a redução da taxa de suicídio global registrada 2013 um terço até 2030, enquanto e a OMS estabeleceu como meta 15% de redução da mesma taxa registrada em 2019 até 2023, com base em valores de 2019. (WHO, 2021)</p><br>
<center><figure><figure><img src="https://jupsin.com/wp-content/uploads/2021/06/1Captura-de-pantalla-2021-06-22-a-las-12_Fotor-1-1024x549.jpeg"><br><figcaption>Pilares do guia de prevenção ao suicídio da OMS<figcaption> </figure></center>

<p> A ideação suicida é um problema que afeta indivíduos de todas as idades em todo o mundo devido a diversos fatores, como desgosto, raiva, culpa e outros sintomas de melancolia ou ansiedade. A ideação suicida é um estado em que uma pessoa tem pensamentos recorrentes associados ao desejo de morrer, seja por se considerar um fardo para sua família ou ambiente, seja por ter um sentimento de não pertencimento ao grupo ou sociedade a que pertence. Embora a maioria das pessoas com pensamentos suicidas (80%) não tente o suicídio, a depressão pode levar ao suicídio se não for tratada de maneira eficaz a longo prazo (DENIS-RODRIGUEZ, 2017).</p>

<p>Um dos pilares do guia de prevenção ao suicídio elaborado pela OMS é “a identificação precoce, avaliação, gerenciamento e acompanhamento de pessoas acometidas por comportamentos suicidas”(WHO, 2021).A detecção precoce de ideações suicidas em postagens pode então ajudar os especialistas em saúde a identificar indivíduos em risco. Assim, um sistema automatizado de detecção de ideação suicida e primeiros sintomas de depressão em postagens online permitiria a estes profissionais fornecer o tratamento mais adequado e poupar muitas vidas.</p>
<p>Análise de Sentimento, ou mineração de opinião, é um campo crescente que captura automaticamente o sentimento do usuário (SILVA, 2018). A combinação de informações de mídia social e Análise de Sentimento pode reconhecer pensamentos suicidas precoces e evitar a maioria das tentativas de suicídio. Como resultado, <i>Machine Learning</i> e <i>Natural Language Processing</i> passaram a ser aplicadas como técnicas para prever a intenção suicida a partir de dados de mídia social. Além disso, as arquiteturas de <i>Deep Learning</i> fornecem vantagens significativas para detectar pensamentos suicidas, uma vez que estes métodos executam com precisão muito alta com nível relativamente baixo de processamento (MÄNTYLÄ, 2018).</p>
<p>Estudos anteriores que usaram algoritmos de <i>Machine Learning</i> para identificar ideações suicidas em postagens foram limitados em tamanho de conjunto de dados. A pesquisa de Pachouly (2021) usou vários modelos de <i>Machine Learning</i> para detectar depressão em uma coleção de 15.000 tweets, mas a baixa precisão foi um problema elencado. Um trabalho semelhante foi realizado por Manisha (2019), que melhorou o desempenho dos classificadores de <i>Machine Learning</i> em um conjunto de dados de 50.000 tweets coletados manualmente e rotulados para classificação binária. Em Stankevich (2019), os autores propuseram um sistema automático de detecção de depressão usando modelos de <i>Machine Learning</i> em um conjunto de dados criado a partir de uma rede social russa, Vkontakte.</p>
<p>No entanto, esses estudos não obtiveram uma boa precisão devido ao treinamento de algoritmos de <i>Machine Learning</i> em uma pequena coleção de texto. Com o uso de regras de anotação apropriadas, é possível criar uma base de dados maior para o treinamento de modelos de <i>Deep Learning</i> e melhorar a classificação de modelos de <i>Machine Learning</i>. Estudos recentes listados por Abdulsalam (2022) mostram que classificadores <i>Deeping Learning</i> foram usados para identificar intenções suicidas de usuários de redes sociais com maior precisão, principalmente em conjuntos de dados anotados manualmente coletados de fóruns de depressão e suicídio (ALADAG, 2018) e <i>subreddits</i> (SHAH, 2020).</p>
<p>Neste trabalho, seguiremos essa abordagem e iremos implementar um <i>Deeping Learning</i> na tarefa de identificar ideações suicidas em postagens de fóruns de redes sociais. A principal contribuição deste estudo é avaliar experimentalmente o desempenho de um classificador de Deep Learning em um conjunto de dados de aproximadamente 232.000 postagens, de fóruns de uma rede social, rotuladas como "suicídio" e "não-suicídio".</p>
<a id="subsection_1_2"></a>
  
##  1.2 Descrição da base de dados
----
<p>A base de dados utilizada neste trabalho é encontrada no Kaggle, e consiste de uma coleção de 232.074 posts coletados em plataformas de subreddit e Reddit, no intervalo de dezembro de 2008 até janeiro de 2021.
Pode ser encontrada no seguinte link: <br>
<a href link=https://www.kaggle.com/datasets/nikhileswarkomati/suicide-watch>https://www.kaggle.com/datasets/nikhileswarkomati/suicide-watch</a></p>
  <a id="subsection_1_3"></a>
  
##  1.3 Objetivo
----
<p> O principal objetivo deste trabalho é utilizar técnicas efetivas de Processamento de Linguagem Natural na identificação de pensamentos suicidas dos usuários em fórum da rede social Reddit.</p>
<p>Os objetivos específicos deste trabalho são:
    <ul>
      <li>Treinar modelos de Deep Learning na identificação de pensamentos suicidas nas postagens do fórum;</li>
      <li>Fornecer uma análise do desempenho do classificador;</li>
      <li>Desenvolver uma aplicação para que os usuários finais possam analisar se uma postagem tem ou não ideação suicida.</li>
    </ul>
</p>
  <a id="section_2"></a>
  
# 2 Desenvolvimento
  <p> No arquivo parte01.ipynb encontra-se as etapas de configuração do ambiente, coleta e limpeza do conjunto de dados e o pré-processamento e extração de características.
