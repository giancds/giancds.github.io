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

<<<<<<< HEAD
&nbsp;&nbsp;&nbsp;&nbsp;i. **regressão**: prever um *target* contínuo

&nbsp;&nbsp;&nbsp;&nbsp;ii. **regressão**: prever um *target* categórico

Devido ao fato de o modelo aprendido em *machine learning* descrever as relações entre *features* e *targets*, é necessário o levantamento de um conjunto de dados (também chamado de *dataset*) que contenha exemplos (também chamados de *datapoints*) com os valores das *features* preenchidas e o *target* correto associado àquelas *features*. Por padrão, um dataset segue o formato apresentado na Tabela 1.

<p align="center">
<br/><br/>
  <img src='/assets/img/features.png' width='70%'>
</p>
<div style="width:image width px; font-size:80%; text-align:center;">Tabela 1: Formato de um dataset. Por padrão, features ficam nas colunas à esquerda enquanto o target é colocado na última coluna mais à direita. Cada linha do dataset corresponde a um datapoint (i.e., as features e o target correspondente a um exemplo).</div><br/><br/>

=======
&nbsp;&nbsp;&nbsp;&nbsp;i. **regressão** <img src="/docs/machine_learning/tex/e5d134f35dc4949fab12ec64d186248a.svg?invert_in_darkmode&sanitize=true" align=middle width=16.43840384999999pt height=14.15524440000002pt/> prever um *target* contínuo

&nbsp;&nbsp;&nbsp;&nbsp;ii. **regressão** <img src="/docs/machine_learning/tex/e5d134f35dc4949fab12ec64d186248a.svg?invert_in_darkmode&sanitize=true" align=middle width=16.43840384999999pt height=14.15524440000002pt/> prever um *target* categórico

Devido ao fato de o modelo aprendido em *machine learning* descrever as relações entre *features* e *targets*, é necessário o levantamento de um conjunto de dados (também chamado de *dataset*) que contenha exemplos (também chamados de *datapoints*) com os valores das *features* preenchidas e o *target* correto associado àquelas *features*. Por padrão, um dataset segue o formato apresentado na Tabela 1.

<p align="center"><img src="/docs/machine_learning/tex/31b8c6daa45a054c44c15e87652bddaf.svg?invert_in_darkmode&sanitize=true" align=middle width=700.2745645499999pt height=213.93602175pt/></p>

A Tabela 2 apresenta um exemplo de um *dataset* real. Esta é uma amostra do dataset *Iris* publicado em 1953 e que até hoje representa um caso típico de testes para modelos de *machine learning*.


<p align="center"><img src="/docs/machine_learning/tex/0ce66db84a2ec2ea5a80fb79007bdda8.svg?invert_in_darkmode&sanitize=true" align=middle width=700.2746619pt height=271.05931215pt/></p>
>>>>>>> 9d32fe4c8940e8f39b462c3afe621ffa1376411f

A Tabela 2 apresenta um exemplo de um *dataset* real. Esta é uma amostra do *dataset* *Iris* publicado
em 1953 e que até hoje representa um caso típico de testes para modelos de *machine learning*.

<!-- ![Tabela 2: Amostra do clássico *dataset* “Iris” para demonstrar um exemplo real. O “Iris” foi introduzido por Ronald Fisher em 1936 e tornou-se um caso de teste típico para algoritmos
de *machine learning*. O dataset é constituído por quatro *features* e um *target* (`species`).](/assets/img/iris.png) -->
<p align="center">
<br/><br/>
  <img src='/assets/img/iris.png' width='70%'>
</p>
<div style="width:image width px; font-size:80%; text-align:center;">
Tabela 2: Amostra do clássico <i>dataset</i> “Iris” para demonstrar um exemplo real. O “Iris” foi introduzido por Ronald Fisher em 1936 e tornou-se um caso de teste típico para algoritmos
de <i>machine learning</i>. O dataset é constituído por quatro <i>features</i> e um <i>target</i>.</div><br/><br/>

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

<!-- ![Figura 1: Amostra do clássico *dataset* “Iris” para demonstrar um exemplo real. O “Iris” foi introduzido por Ronald Fisher em 1936 e tornou-se um caso de teste típico para algoritmos de *machine learning*. O dataset é constituído por quatro *features* e um *target* (`species`).](/assets/img/proc_ml.png) -->

<p align="center">
  <br/><br/>
  <img src='/assets/img/proc_ml.png' width='70%'>  
</p>
<div style="width:image width px; font-size:80%; text-align:center;">
Figura 1: Processo de “aprendizagem” de um modelo de <i>machine learning</i>.<br/><br/></div>

<!-- ![Figura 2: Amostra do clássico *dataset* “Iris” para demonstrar um exemplo real. O “Iris” foi introduzido por Ronald Fisher em 1936 e tornou-se um caso de teste típico para algoritmos de *machine learning*. O dataset é constituído por quatro *features* e um *target* (`species`).](/assets/img/proc_pred.png) -->
<p align="center">
  <br/><br/>
  <img src='/assets/img/proc_pred.png' width='70%'>
</p>
<div style="width:image width px; font-size:80%; text-align:center;">
Figura 2: Processo de “predição” de um modelo de <i>machine learning</i>.</div><br/><br/>

### 1.1 - Um pequeno exemplo

Suponhamos que o *dataset* contido na Tabela 3 nos foi fornecido e precisamos extrair manualmente um modelo para fazer predições. Qual(is) a(s) regra(s) que definem as relações entre *features* e *target* deste dataset?



<!-- ![Tabela 3: Exemplo de um dataset contendo três *features* e um *target*.](/assets/img/financeira_simples.png) -->
<p align="center">
  <br/><br/>
  <img src='/assets/img/financeira_simples.png' width='70%'>
</p>
<div style="width:image width px; font-size:80%; text-align:center;">Tabela 3: Exemplo de um dataset contendo três <i>features</i> e um <i>target</i>.</div><br/><br/>

Após alguma análise, podemos propor o algoritmo abaixo (demonstrado utilizando a linguagem *python*):

```python
if Proporção Salário-Empréstimo < 1.5:
  Classe = 'Padrão'
else:
  Classe='diferenciada'
```

Bastante simples, não? Este é um exemplo de um modelo de predições (ou seja, exemplo de um agente inteligente). Este é também um exemplo de um modelo consistente com o *dataset*. Um modelo consistente com o *dataset* é aquele que depois de aprendido consegue classificar os *datapoints* contidos no *dataset* com 100% de acurácia (i.e., sem cometer erros). Observe também que o modelo não faz uso de todas as *features* apresentadas e que a  *feature* utilizada é uma *feature* derivada<sup>2</sup>. Uma feature derivada é uma feature que pode ser obtida a partir de duas ou mais features. No exemplo do modelo acima, `Proporção Salário-Empréstimo` pode ser obtida através de features `Salário` e `Empréstimo` (que não foram exibidas na tabela).

Agora, vamos dificultar as coisas. Suponhamos o *dataset* contido na Tabela 4. 




<!-- ![Tabela 4: Exemplo de um dataset contendo seis *features* e um *target*.](/assets/img/financeira_complexa.png) -->
<p align="center">
  <br/><br/>
  <img src='/assets/img/financeira_complexa.png' width='90%'>
</p>
<div style="width:image width px; font-size:80%; text-align:center;">Tabela 4: Exemplo de um dataset contendo três <i>features</i> e um <i>target</i>.</div><br/><br/>

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

<<<<<<< HEAD
Esta rede de supermercados está disposta a lhe entregar um dataset com três *features* binárias que podem assumir os valores {`True`, `False`}. Como três *features* binárias produzem um total de `2`<sup>`3`</sup> `= 8` combinações,  decidimos construir uma tabela com todas as possíveis combinações destas *features* antes mesmo de inspecionarmos algum *dataset*. Estas combinações estão reproduzidas na Tabela 5.

=======
Esta rede de supermercados está disposta a lhe entregar um dataset com três *features* binárias que podem assumir os valores <img src="/docs/machine_learning/tex/538d28f6c5d6377063c2ce88536ddb42.svg?invert_in_darkmode&sanitize=true" align=middle width=102.70201755pt height=24.65753399999998pt/>. Como três *features* binárias produzem um total de <img src="/docs/machine_learning/tex/a1d3e6ee2ea8e9dff755dc407006e581.svg?invert_in_darkmode&sanitize=true" align=middle width=45.730508999999984pt height=26.76175259999998pt/> combinações, antes de olharmos para o dataset decidimos construir uma tabela com todas as possíveis combinações destas features. Estas combinações estão reproduzidas na Tabela 5.
>>>>>>> 9d32fe4c8940e8f39b462c3afe621ffa1376411f

<!-- ![Tabela 5: Combinações possíveis para três *features* binárias sem conhecermos os valores dos *targets*.](/assets/img/familia_questions.png) -->
<p align="center">
  <br/><br/>
  <img src='/assets/img/familia_questions.png' width='60%'>
</p>
<div style="width:image width px; font-size:80%; text-align:center;">Tabela 5: Combinações possíveis para três <i>features</i> binárias sem conhecermos os valores dos <i>targets</i>.</div><br/><br/>

Quando passamos a considerar os valores para o `Grupo` sem termos recebido os valores corretos para o *target* de cada datapoint, o número de combinações diferentes para o *dataset* sobe para 6561! A partir dessas combinações que consideram o *target*, podemos procurar por uma combinação que possa servir como modelo para fazer predições sobre os consumidores do mercado. Uma amostra destas combinações está disponível na Tabela 6.



<!-- ![Tabela 6: Amostra de combinações possíveis para três *features* binárias quando passamos a considerar os valores para o *target*. A partir da incusão do target, passamos a ter 6561 soluções possíveis ao invés de apenas 8.](/assets/img/familia_expandida.png) -->
<p align="center">
  <br/><br/>
  <img src='/assets/img/familia_expandida.png' width='90%'>
</p>
<div style="width:image width px; font-size:80%; text-align:center;">Tabela 6: Amostra de combinações possíveis para três <i>features</i> binárias quando passamos a considerar os valores para o <i>target</i>. A partir da incusão do <i>target</i>, passamos a ter 6561 soluções possíveis ao invés de apenas 8.</div><br/><br/>

Suponhamos então que a rede de supermercados conduziu uma pesquisa entre seus consumidores e que o número de respostas obtido foi baixo. Apenas cinco *datapoints* foram obtidos conforme demonstrado na Tabela 7.

Se considerarmos os *datapoints* obtidos pela rede de supermercados, podemos eliminar combinações as quais possuem o target `Grupo` diferentes dos valores reais obtidos, como demonstrado na Tabela 8. As combinações restantes são aquelas chamadas de consistentes com o *dataset* da Tabela 7. Em outras palavras, estas combinações restantes conseguem produzir a resposta correta para cada *datapoint* do dataset.

<<<<<<< HEAD
<!-- ![Tabela 7: Conjunto de *datapoints* obtidos pela rede de supermercados fictícia.](/assets/img/familia.png) -->
<p align="center">
  <br/><br/>
  <img src='/assets/img/familia.png' width='60%'>
</p>
<div style="width:image width px; font-size:80%; text-align:center;">Tabela 7: Conjunto de <i>datapoints</i> obtidos pela rede de supermercados fictícia.</div><br/><br/>

Entretanto, ainda temos um problema: das 8 possíveis combinações das *features* binárias, apenas 5 foram obtidas e, por isso, temos três combinações que nunca foram vistas! Se olharmos novamente para a Tabela 8, as combinações `M`<sub>`2`</sub>, `M`<sub>`3`</sub> e `M`<sub>`4`</sub> são combinações consistentes com o *dataset* e ao mesmo tempo divergem quanto ao `Grupo` que deve ser atribuído aos três casos que não foram vistos. Qual destas três combinações devemos escolher como sendo o modelo final? É exatamente pelo fato de podermos obter mais de um modelo consistente com o *dataset* que dizemos que o *machine learning* é um problema mal-posto, pois não há uma solução para esse problema!

<!-- ![Tabela 8: Amostra de combinações consistentes com os valores obtidos pela rede de supermercados fictícia. As combinações sombreadas são combinações as quais possuem valores para o *target* que não estão corretas de acordo com os valores obtidos, i.e., são combinações inválidas.](/assets/img/familia_overlay.png) -->
<p align="center">
  <br/><br/>
  <img src='/assets/img/familia_overlay.png' width='90%'>
</p>
<div style="width:image width px; font-size:80%; text-align:center;">Tabela 8: Amostra de combinações consistentes com os valores obtidos pela rede de supermercados fictícia. As combinações sombreadas são combinações as quais possuem valores para o <i>target</i> que não estão corretas de acordo com os valores obtidos, i.e., são combinações inválidas.</div><br/><br/>
=======
Entretanto, ainda temos um problema: das 8 possíveis combinações das *features* binárias, apenas 5 foram obtidas e, por isso, temos três combinações que nunca foram vistas! Se olharmos novamente para a Tabela 8, as combinações <img src="/docs/machine_learning/tex/c4f2a02af909d30254bc52b8b0b9daf1.svg?invert_in_darkmode&sanitize=true" align=middle width=22.07771114999999pt height=22.648391699999998pt/>,	<img src="/docs/machine_learning/tex/0be82563208d71d0c3899fd6864f8301.svg?invert_in_darkmode&sanitize=true" align=middle width=22.07771114999999pt height=22.648391699999998pt/> e <img src="/docs/machine_learning/tex/0d649cecf09f38776ad6cf104cc0af58.svg?invert_in_darkmode&sanitize=true" align=middle width=22.07771114999999pt height=22.648391699999998pt/> são combinações consistentes com o *dataset* e ao mesmo tempo divergem quanto ao `Grupo` que deve ser atribuído aos três casos que não foram vistos. Qual destas três combinações devemos escolher como sendo o modelo final? É exatamente pelo fato de podermos obter mais de um modelo consistente com o *dataset* que dizemos que o *machine learning* é um problema mal-posto, pois não há uma solução para esse problema!
>>>>>>> 9d32fe4c8940e8f39b462c3afe621ffa1376411f

Consistência pode ser interpretada como uma forma de **memorização** por parte do modelo. Contudo, os *datapoints* em um dataset podem conter diversas formas de ruídos, como por exemplo preenchimentos incorretos de valores, valores faltando, até mesmo exceções onde o valor é de fato correto mas tão incomum que parece estar incorreto. Nestes casos, a memorização torna-se uma característica indesejada para um modelo de *machine learning*.

Ao mesmo tempo que buscamos um modelo consistente, procuramos também um modelo que seja capaz de **generalizar além dos dados**. Um modelo com esta característica é capaz de fazer predições corretas mesmo na presença de *datapoints* com ruído. Ou seja, este modelo que é capaz de generalizar além do *dataset* não é influenciado pelo ruído nos dados. Sendo assim, que critérios devemos utilizar para selecionar este modelo?

O *machine learning* faz uma série de suposições que auxiliam a definir os critérios de seleção de um modelo. Estas suposições são chamados viéses indutivos (do Inglês ***inductive bias***):

&nbsp;&nbsp;&nbsp;&nbsp;a. viés de restrição (***restriction bias***): limita o tipo de modelo que será aprendido.

&nbsp;&nbsp;&nbsp;&nbsp;b. viés de preferência (***preference bias***): limita o algoritmo para que prefira alguns tipos de modelo em detrimento a outros modelos.

Por exemplo, consideremos o Iterative Dichotomizer 3 - (ID3), o algoritmo padrão para métodos baseados em informação. Este algoritmo possui um *restriction bias* que o limita a aprender um modelo em formato de árvore que codifica em cada galho um “teste” em uma determinada *feature* enquanto o seu *preference bias* limita-o a buscar pela árvore que contenha o menor número possível de níveis.

### 2.1 - O que pode dar errado com o *machine learning*?

Até agora vimos que o *machine learning* pode ser bastante útil para criarmos agentes inteligentes que podem ser úteis em alguns tipos de problemas. Vimos também que devido ao efeito do *inductive bias*, modelos podem aprender a generalizar além do *dataset*. No entanto, se escolhermos o *inductive bias* errado, o modelo aprendido poderá apresentar dois tipos de problemas: *underfitting* e *overfitting*. 

*Underfitting* ocorre quando o modelo aprendido através do *inductive bias* é muito simples para capturar as relações entre *features* e *targets*. *Overfitting*, ao contrário, ocorre quando o modelo aprendido através do *inductive bias* é demasiado complexo para capturar as relações entre *features* e *targets*. A Figura 3 exibe um exemplo de *underfitting* e *overfitting*.



<!-- ![Figura 3: Representação dos conceitos de underfitting e overfitting. Suponhamos que queremos aprender relação exibida em (a). Se o modelo for muito simples como exibido em (b), o problema de underfitting irá ocorrer. Caso o modelo seja muito complexo como exibido em (c), teremos um problema de overfitting. O modelo exibido em (d) mesmo contendo alguns pequenos desvios (muito provavelmente em função de ruídos no dataset) é mais próximo daquilo que procuramos.](/assets/img/under_over.png) -->
<p align="center">
  <br/><br/>
  <img src='/assets/img/under_over.png' width='90%'>
</p>
<div style="width:image width px; font-size:80%; text-align:center;">
Figura 3: Representação dos conceitos de <i>underfitting</i> e <i>overfitting</i>. Suponhamos que queremos aprender relação exibida em (a). Se o modelo for muito simples como exibido em (b), o problema de <i>underfitting</i> irá ocorrer. Caso o modelo seja muito complexo como exibido em (c), teremos um problema de <i>overfitting</i>. O modelo exibido em (d) mesmo contendo alguns pequenos desvios (muito provavelmente em função de ruídos no dataset) é mais próximo daquilo que procuramos.</div><br/><br/>

## 3 - Resumo

Em resumo, um algoritmo de *machine learning* aprende a relação entre *features* e *targets* a partir de exemplos contidos em um *dataset*. Além disso, *machine learning* é considerado um problema malposto devido a quatros fatores: a) precisa generalizar a além do *dataset* que por sua vez é apenas uma amostra; b) precisa de um conjunto de suposições que são necessárias para o aprendizado (*inductive bias*); c) *underfitting*; e d) *overfitting*. Encontrar o balanço entre complexidade e simplicidade é uma forma de arte do *machine learning* e, também, a parte mais difícil de prática.
<br/><br/>
---
<div style="width:image width px; font-size:80%">
<sup>1</sup> Embora sua área de estudo seja tão ampla e diversa quanto a do próprio *machine learning*, o *reinforcement learning* continua sendo uma forma de *machine learning*.
<br/><br/>
<sup>2</sup> Design e seleção de *features* são partes muito importantes do *machine learning*. 
</div>