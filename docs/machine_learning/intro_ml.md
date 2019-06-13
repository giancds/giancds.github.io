---
layout: default
title: Introdução ao Machine Learning
parent: Machine Learning
nav_order: 1
---

## 1 - Introdução

*Machine Learning* é a disciplina da Inteligência Artificial a qual estuda a criação de **agentes inteligentes** que aprendem através da experiência. Desta forma, ao contrário da Inteligência Artificial clássica, o agente inteligente não tem seu conhecimento programado durante sua criação, mas ele é **programado para aprender** a alcançar o objetivo para o qual foi desenvolvido.

Embora alguns autores definam *machine learning* como sendo o **aprendizado através de exemplos**, esta definição exclui o aprendizado por reforço positivo<sup>1</sup> (do Inglês *Reinforcement Learning - RL*) onde o agente aprende praticando a tarefa sem quaisquer tipos de respostas, recebendo apenas um *feedback* sobre o quão bem está executando aquela tarefa. A definição de aprendizado através de exemplos é mais adequada às áreas de **machine learning supervisionado**  e machine learning não-supervisionado (ou sem supervisão).

O *machine learning* supervisionado envolve o aprendizado de um modelo que descreve as relações entre um conjunto de **variáveis descritivas** (também chamadas de ***features***) e uma **variável alvo** (também chamada de ***target***). Esta forma de *machine learning* gera modelos que podem ser aplicados a dois
tipos de problemas:

&nbsp;&nbsp;&nbsp;&nbsp;i. **regressão** $$\rightarrow$$ prever um *target* contínuo

&nbsp;&nbsp;&nbsp;&nbsp;ii. **regressão** $$\rightarrow$$ prever um *target* categórico

Devido ao fato de o modelo aprendido em *machine learning* descrever as relações entre *features* e *targets*, é necessário o levantamento de um conjunto de dados (também chamado de *dataset*) que contenha exemplos (também chamados de *datapoints*) com os valores das *features* preenchidas e o *target* correto associado àquelas *features*. Por padrão, um dataset segue o formato apresentado na Tabela 1.

\begin{table*}[t]
  \caption{Formato de um \emph{dataset}. Por padrão, \emph{features} ficam nas colunas à esquerda enquanto o \emph{target} é colocado na última coluna mais à direita. Cada linha do \emph{dataset} corresponde a um \emph{datapoint} (i.e., as \emph{features} e o \emph{target} correspondente a um exemplo).}
  \small
  \centering
  \setlength\tabcolsep{12pt}
  \begin{tabular*}{0.6\textwidth}{c c c c c c c c}
  \toprule    
    \multicolumn{6}{c}{\features} & & \target \\
      \cmidrule{1-6}  \cmidrule{8-8}
    $$x_1$$  & $$x_2$$ & $$x_3$$ & $$x_4$$ & $$x_5$$ & $$x_6$$ & & $$y$$ \\
  \midrule
  --- & --- & --- & --- & --- & --- & & ---	\\  
  --- & --- & --- & --- & --- & --- & & ---	\\  
  --- & --- & --- & --- & --- & --- & & ---	\\  
  --- & --- & --- & --- & --- & --- & & ---	\\  
  --- & --- & --- & --- & --- & --- & & ---	\\  
  --- & --- & --- & --- & --- & --- & & ---	\\  
  --- & --- & --- & --- & --- & --- & & ---	\\
  \bottomrule  
  \end{tabular*}
  \label{tab:features}
\end{table*}

A Tabela 2 apresenta um exemplo de um *dataset* real. Esta é uma amostra do dataset *Iris* publicado em 1953 e que até hoje representa um caso típico de testes para modelos de *machine learning*.


\begin{table}[th]
  \caption{Amostra do clássico \dataset \myquote{Iris} para demonstrar um exemplo de \dataset com exemplos reais. O \myquote{Iris} foi introduzido por Ronald Fisher em 1936 e tornou-se um caso de teste típico para algoritmos de \ml. O \dataset é constituído por quatro \features (\featN{sepal length}, \featN{sepal width}, \featN{petal length} e \featN{petal width}) e um \target (\featN{species})}
  \centering
  \small
  \setlength\tabcolsep{10pt}
  \begin{tabular*}{0.58\textwidth}{c c c c c c}
  \toprule
    \featN{}	 & \featN{sepal}	& \featN{sepal} & \featN{petal} & \featN{petal} & \featN{species}\\
    \featN{ID}	 & \featN{length}	& \featN{width} & \featN{length} & \featN{width} & (\target)\\
  \midrule
  1 & 5.1 & 3.5 & 1.4 & 0.2 & setosa \\
  2 & 4.9 & 3.0 & 1.4 & 0.2 & setosa \\
  3 & 4.7 & 3.2 & 1.3 & 0.2 & setosa \\
  4 & 7.0 & 3.2 & 4.7 & 1.4 & versicolor \\
  5 & 6.4 & 3.2 & 4.5 & 1.5 & versicolor \\ 
  6 & 6.9 & 3.1 & 4.9 & 1.5 & versicolor \\
  7 & 6.3 & 3.3 & 6.0 & 2.5 & virginica \\
  8 & 5.8 & 2.7 & 5.1 & 1.9 & virginica \\
  9 & 7.1 & 3.0 & 5.9 & 2.1 & virginica \\
  \midrule
    & $$x_1$$ & $$x_2$$ & $$x_3$$ & $$x_4$$ & $$y$$ \\
  \bottomrule
  \end{tabular*}
  \label{tab:iris}
\end{table}



Abaixo seguem algumas definições importantes que são utilizadas em machine learning:

&nbsp;&nbsp;&nbsp;&nbsp;i. **Features** (ou variáveis descritivas): conjunto de informações relativos a um exemplo domínio

&nbsp;&nbsp;&nbsp;&nbsp;ii. **Target** (ou variável alvo): resposta correta relativa a um exemplo do domínio

&nbsp;&nbsp;&nbsp;&nbsp;iii. **Datapoint** (ou exemplo): features + target

&nbsp;&nbsp;&nbsp;&nbsp;iv. **Query**: um datapoint para o qual queremos predizer o target correto (i.e., um datapoint sem target associado)

&nbsp;&nbsp;&nbsp;&nbsp;v. **Dataset** (ou conjunto de exemplos): conjunto de datapoints

&nbsp;&nbsp;&nbsp;&nbsp;vi. **algoritmo**: processo utilizado para aprender o modelo

&nbsp;&nbsp;&nbsp;&nbsp;vii. **modelo**: conjunto de “regras” aprendidas

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**O modelo é o Agente Inteligente!**

A Figura 1 ilustra o processo de “aprendizado” de *machine learning*. Um *dataset* contendo *features* e *targets* é fornecido como entrada para um algoritmo que por sua vez gera um modelo. Depois que o modelo for gerado, podemos pegar uma *query* e obter uma predição para determinar qual a resposta (i.e., o *target*) correta para aquela instância. A Figura 2 ilustra o processo de predição.

### 1.1 - Um pequeno exemplo

Suponhamos que o *dataset* contido na Tabela 3 nos foi fornecido e precisamos extrair manualmente um modelo para fazer predições. Qual(is) a(s) regra(s) que definem as relações entre *features* e *target* deste dataset?

Após alguma análise, podemos propor o algoritmo abaixo (demonstrado utilizando a linguagem *python*):

```python
if Proporção Salário-Empréstimo < 1.5:
  Classe = 'Padrão'
else:
  Classe='diferenciada'
```

Bastante simples, não? Este é um exemplo de um modelo de predições (ou seja, exemplo de um agente inteligente). Este é também um exemplo de um modelo consistente com o *dataset*. Um modelo consistente com o *dataset* é aquele que depois de aprendido consegue classificar os *datapoints* contidos no *dataset* com 100% de acurácia (i.e., sem cometer erros). Observe também que o modelo não faz uso de todas as *features* apresentadas e que a  *feature* utilizada é uma *feature* derivada<sup>2</sup>. Uma feature derivada é uma feature que pode ser obtida a partir de duas ou mais features. No exemplo do modelo acima, `Proporção Salário-Empréstimo` pode ser obtida através de features `Salário` e `Empréstimo` (que não foram exibidas na tabela).

Agora, vamos dificultar as coisas. Suponhamos o *dataset* contido na Tabela 4. 

INCLUIR TABELA

Após uma análise minuciosa deste *dataset*, podemos propor o algoritmo abaixo (demonstrado utilizando a linguagem *python*):

```python
if Proporção Salário-Empréstimo < 1.5:
  classe = 'diferenciada'
elif Proporção Salário-Empréstimo > 4:
  classe ='padrão'
elif idade  < 40 and profissão == 'indústria':
  classe = 'padrão'
else:
  classe = 'diferenciada'
```

De certa maneira, a extração das regras ficou mais complicada. Imaginemos o caso de um *dataset* com dezenas de *features* e milhares de *datapoints*. A tarefa de extrair as regras torna-se quase que humanamente impossível de realizar. São nestes casos mais complexos que o “brilho” do *machine learning* aparece. Enquanto para nós seres humanos a tarefa deve certamente demorar dias ou mesmo semanas, um computador pode gerar um modelo em poucos minutos!

## 2 - Como o *machine learning* funciona

O aprendizado de um modelo de *machine learning* pode ser visto como um **processo de busca**. Este processo conduz uma busca pelo modelo que melhor captura as relações entre as *features* e o *target*. Ou seja, busca pelo modelo capaz de gerar predições corretas para *query* que ele recebe como entrada.

A forma mais fácil e eficaz para gerar um modelo é buscar dentre os modelos possíveis por aqueles **modelos que sejam “consistentes”** com os *datapoints*. No entanto, para maioria dos casos, um *dataset* é apenas uma amostra do número total de *datapoints* possíveis quando consideramos as possibilidades de combinações dos valores das *features*. Por exemplo: se uma das *features* for contínua, temos uma infinita possibilidade de combinações! Por isso, dizemos que o *machine learning* é um **problema mal-posto**.

Vamos ilustrar a ideia de consistência e imperfeição com um exemplo. Imaginemos que uma rede de supermercados nos contratou para desenvolver um modelo de *machine learning* para realizar predições sobre seus consumidores. Estas predições devem classificar os consumidores nos grupos `Famílias`, `Casais sem filhos` e `Solteiros`.

Esta rede de supermercados está disposta a lhe entregar um dataset com três *features* binárias que podem assumir os valores $$\{True; False\}$$. Como três *features* binárias produzem um total de $$2^3=8$$ combinações, antes de olharmos para o dataset decidimos construir uma tabela com todas as possíveis combinações destas features. Estas combinações estão reproduzidas na Tabela 5.

INCLUIR TABELA

Quando passamos a considerar os valores para o `Grupo` sem termos recebido os valores corretos para o *target* de cada datapoint, o número de combinações diferentes para o *dataset* sobe para 6561! A partir dessas combinações que consideram o *target*, podemos procurar por uma combinação que possa servir como modelo para fazer predições sobre os consumidores do mercado. Uma amostra destas combinações está disponível na Tabela 6.

INCLUIR TABELA

Suponhamos então que a rede de supermercados conduziu uma pesquisa entre seus consumidores e que o número de respostas obtido foi baixo. Apenas cinco *datapoints* foram obtidos conforme demonstrado na Tabela 7.

Se considerarmos os *datapoints* obtidos pela rede de supermercados, podemos eliminar combinações as quais possuem o target `Grupo` diferentes dos valores reais obtidos, como demonstrado na Tabela 8. As combinações restantes são aquelas chamadas de consistentes com o *dataset* da Tabela 7. Em outras palavras, estas combinações restantes conseguem produzir a resposta correta para cada *datapoint* do dataset.

Entretanto, ainda temos um problema: das 8 possíveis combinações das *features* binárias, apenas 5 foram obtidas e, por isso, temos três combinações que nunca foram vistas! Se olharmos novamente para a Tabela 8, as combinações $$\mathbb{M}_2$$,	$$\mathbb{M}_4$$ e $$\mathbb{M}_5$$ são combinações consistentes com o *dataset* e ao mesmo tempo divergem quanto ao `Grupo` que deve ser atribuído aos três casos que não foram vistos. Qual destas três combinações devemos escolher como sendo o modelo final? É exatamente pelo fato de podermos obter mais de um modelo consistente com o *dataset* que dizemos que o *machine learning* é um problema mal-posto, pois não há uma solução para esse problema!

Consistência pode ser interpretada como uma forma de **memorização** por parte do modelo. Contudo, os *datapoints* em um dataset podem conter diversas formas de ruídos, como por exemplo preenchimentos incorretos de valores, valores faltando, até mesmo exceções onde o valor é de fato correto mas tão incomum que parece estar incorreto. Nestes casos, a memorização torna-se uma característica indesejada para um modelo de *machine learning*.

Ao mesmo tempo que buscamos um modelo consistente, procuramos também um modelo que seja capaz de **generalizar além dos dados**. Um modelo com esta característica é capaz de fazer predições corretas mesmo na presença de *datapoints* com ruído. Ou seja, este modelo que é capaz de generalizar além do *dataset* não é influenciado pelo ruído nos dados. Sendo assim, que critérios devemos utilizar para selecionar este modelo?

O *machine learning* faz uma série de suposições que auxiliam a definir os critérios de seleção de um modelo. Estas suposições são chamados viéses indutivos (do Inglês ***inductive bias***):

&nbsp;&nbsp;&nbsp;&nbsp;a.viés de restrição (***restriction bias***): limita o tipo de modelo que será aprendido.

&nbsp;&nbsp;&nbsp;&nbsp;b. viés de preferência (***preference bias***): limita o algoritmo para que prefira alguns tipos de modelo em detrimento a outros modelos.

Por exemplo, consideremos o Iterative Dichotomizer 3 - (ID3), o algoritmo padrão para métodos baseados em informação<sup>3</sup>. Este algoritmo possui um *restriction bias* que o limita a aprender um modelo em formato de árvore que codifica em cada galho um “teste” em uma determinada *feature* enquanto o seu *preference bias* limita-o a buscar pela árvore que contenha o menor número possível de níveis.

### 2.1 - O que pode dar errado com o *machine learning*?

Até agora vimos que o *machine learning* pode ser bastante útil para criarmos agentes inteligentes que podem ser úteis em alguns tipos de problemas. Vimos também que devido ao efeito do *inductive bias*, modelos podem aprender a generalizar além do *dataset*. No entanto, se escolhermos o *inductive bias* errado, o modelo aprendido poderá apresentar dois tipos de problemas: *underfitting* e *overfitting*. 

*Underfitting* ocorre quando o modelo aprendido através do *inductive bias* é muito simples para capturar as relações entre *features* e *targets*. *Overfitting*, ao contrário, ocorre quando o modelo aprendido através do *inductive bias* é demasiado complexo para capturar as relações entre *features* e *targets*. A Figura 3 exibe um exemplo de *underfitting* e *overfitting*.

## 3 - Resumo

Em resumo, um algoritmo de *machine learning* aprende a relação entre *features* e *targets* a partir de exemplos contidos em um *dataset*. Além disso, *machine learning* é considerado um problema malposto devido a quatros fatores: a) precisa generalizar a além do *dataset* que por sua vez é apenas uma amostra; b) precisa de um conjunto de suposições que são necessárias para o aprendizado (*inductive bias*); c) *underfitting*; e d) *overfitting*. Encontrar o balanço entre complexidade e simplicidade é uma forma de arte do *machine learning* e, também, a parte mais difícil de prática.