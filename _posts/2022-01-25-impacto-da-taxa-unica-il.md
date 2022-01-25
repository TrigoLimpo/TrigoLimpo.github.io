---
layout: post
title: Qual o impacto da proposta de taxa única nas receitas do IRS?
excerpt_separator: <!--more-->
---

No [programa para as legislativas de 2022](https://iniciativaliberal.pt/wp-content/uploads/2022/01/Iniciativa-Liberal-Programa-Eleitoral-2022.pdf), a IL propõe alterar o regime do IRS para uma taxa única de 15%, com isenção para rendimentos de trabalho até ao montante do mínimo de existência de vida, igual a 1.5 x 14 x IAS (indexante de apoios sociais), que corresponde a 664.80€ por mês para 2022. Para reduzir o choque inicial, propõe começar com um sistema temporário de duas taxas, 15% até aos 30,000€ e 28% acima, com a mesma isenção do sistema de taxa única. Em ambos, acrescenta-se também uma isenção mensal por filho por progenitor de 200€ ou de 400€ em famílias monoparentais, isto é, cada filho representa 400€ de isenção mensal.

Perguntamos qual o impacto orçamental desta proposta?

<!--more-->
 
Em 2019, quando esta proposta foi feita originalmente (sem o sistema transitório de duas taxas), o site da IL dizia:

> De momento, a taxa do IRS efetiva anda nos 13%. Considerando a isenção para rendimentos de trabalhadores por conta de outrem abaixo de 650€, uma taxa fixa de 15% implicaria uma taxa efetiva sobre o rendimento bruto de cerca de 10%. Assumindo o mesmo perfil de rendimentos, isto teria um custo orçamental de cerca de 2 mil milhões de euros no primeiro ano, menos de 1% do PIB. O efeito na economia e o aumento de eficiência fiscal, comprovado noutros países como visto acima, aumentaria a base fiscal reduzindo este impacto a menos de 0,5% do PIB. A introdução gradual da taxa única, começando nos 20% atenuaria qualquer impacto orçamental no curto prazo.

Ou seja, 2 mil milhões de euros. Mas, em 2022, o programa já diz:

> Esta medida transitória, que se estima produzisse um impacto orçamental na receita estimada para 2022 de cerca de 2 mil milhões de euros (excluindo o efeito de expansão económica e respetivo aumento da base fiscal), possibilitaria uma transição gradual para o objetivo de taxa única.

Ora, o sistema transitório de duas taxas, fiscalmente mais punitivo, custa o mesmo que o sistema de taxa única? Parece improvável. Terão usado métodos de cálculo diferentes? Infelizmente, os métodos não são descritos pelo que não sabemos.

Tentaremos então estimar o impacto orçamental usando os [dados mais recentes da AT](https://info.portaldasfinancas.gov.pt/pt/dgci/divulgacao/estatisticas/Pages/default.aspx) relativos ao IRS, que são de 2019.
Uma nota importante é que tentaremos calcular os efeitos de primeira ordem apenas, isto é, os impactos diretos. A perda de receita do IRS poderá ser parcialmente compensada por efeitos de segunda ordem (ex.: pelo aumento do rendimento disponível), mas estes valores não serão calculados aqui.

*<font size="3">No artigo, utiliza-se o ponto para o separador decimal e a vírgula para o separador dos milhares. Apesar do melhor esforço e cuidado, é possível que os cálculos contenham erros. Estamos abertos a que sejam apontados.</font>*


## Sistema atual (de 2019)

Em 2019, a receita do IRS foi de 12,939 milhões de euros, num rendimento bruto total de 100,562 milhões de euros, o que resulta numa taxa global efetiva de 12.9%<sup><a id="cite-footnote-a" href="#footnote-a">(a)</a></sup>.

## Dados

Se a proposta não tivesse quaisquer isenções, então o cálculo da taxa única seria relativamente simples: 0.15 x 100,562 = 15,084 M€, o que significaria um impacto positivo (óbvio, já que 15.0% > 12.9%) de 2,145 milhões de euros na receita do IRS (mais impostos com a nova proposta). Falta-nos, claro, subtrair o valor das isenções para podermos calcular a verdadeira receita do IRS e consequentemente, o impacto da medida.

Olhemos para a isenção pessoal até aos 664.80€<a id="cite-footnote-b" href="#footnote-b"><sup>(b)</sup></a>. Na realidade, utilizarei 653.64€ em vez de 664.80€ por razões de consistência, já que é o valor do IAS de 2019, o ano mais recente com dados. Para sabermos o valor global (relativo a todos os contribuintes) desta isenção, poder-se-ia pensar em fazer simplesmente:

    # contribuintes x isenção pessoal
   
Porém, a realidade é ligeiramente mais complexa, porque certas pessoas auferem menos do que o valor da isenção, seja porque recebem o salário mínimo, trabalham em part-time, têm uma pensão baixa, etc. Se os dados individuais estivessem disponíveis livremente, seria uma questão simples de calcular a isenção individual de cada um:

    Isenção = | Rendimento, se Rendimento < 653.64€
              | 653.64€,    caso contrário

e somá-las todas.

Infelizmente, os dados da AT disponíveis ao público apresentam algumas dificuldades:

1. Não se apresentam ao nível individual (até porque o IRS é calculado ao nível do agregado);
    
2. Por causa das regras sobre quem faz parte do agregado (ex.: filhos até 25 anos que aufiram menos de 14 vezes o SMN num ano podem ser incluídos), o número de pessoas com rendimento por agregado casado não é necessariamente 2 (nem 1 por não casado).

3. Os dados não estão disponíveis por agregado (ex.: agregado 1 teve rendimentos de X1, ...), mas englobados em escalões (ex.: houve 1,446,100 agregados com rendimento entre os 5,000 e os 10,000€).

4. A distribuição dos agregados casados/não casados pelos escalões não está disponível.

Por exemplo, uma dificuldade relativa ao primeiro ponto, é que o sistema de declaração conjunta significa que não se distingue entre um casal em que uma pessoa aufere acima do valor da isenção e a outra abaixo (ex.: 400€ e 1000€); e um outro, com o mesmo rendimento total, em que ambas auferem acima do valor da isenção (ex.: 700€ e 700€). Este sistema é vantajoso para o primeiro casal porque permite reduzir o IRS que tem de pagar, comparativamente a uma tributação separada. Na proposta da IL, o mesmo não é acontece. Os valores são calculados individualmente, o que significa que no primeiro casal, uma das pessoas não utiliza a totalidade da isenção, ao contrário do segundo casal, que utiliza as duas isenções completamente, apesar de ambos os casais terem o mesmo rendimento. (Isto significa também que mesmo que tivéssemos acesso aos dados por agregado, a não ser que também se incluíssem os dados por pessoa, seria difícil dizer com 100% de certeza qual o valor exato das isenções.)


# Sistema de taxa única

## Minorante

Dadas as dificuldades mencionadas acima, em vez de tentar calcular qual o valor exato do impacto nas receitas do IRS, tentaremos calcular um minorante. Isto é, um valor que é seguramente menor do que o valor real. Assim, podemos afirmar que o impacto real será maior do que esse valor.

Para isso, vamos assumir que, tanto para agregados não casados, como para agregados casados, o número de trabalhadores por agregado é de apenas um. Isto significa que, nos agregados em que realmente temos um trabalhador, estamos a calcular corretamente o valor da isenção; e nos agregados em que temos mais de um trabalhador (a maioria dos agregados casados), estamos a calcular um valor menor do que a isenção real. Assim sendo, o valor que calculamos será certamente menor do que o valor real. Por consequência, a receita calculada também será maior que a real e portanto, o impacto na receita do IRS será certamente maior do que o real.

    Perda = IRS_antigo - IRS
          = IRS_antigo - 0.15 x (Rendimento Total - Isenção Total)
          = IRS_antigo + 0.15 x (Isenção Total - Rendimento Total)
          ≥ IRS_antigo + 0.15 x (Isenção_1pa - Rendimento Total)

Aqui, Isenção_1pa é o valor total das isenções, assumindo uma por agregado, quando na realidade, muito agregados (ex.: casados) terão direito a duas.

Sendo assim, 1 agregado = 1 trabalhador = 1 isenção. Para calcularmos o valor total das isenções temos de calcular o valor das isenções dos que têm rendimentos anuais abaixo de 9,150.96€ (14 x 653.64€) e dos que têm acima. Para o primeiro, tendo em conta que, ganhando abaixo do limite, todo o rendimento é isento de IRS, basta saber o rendimento total desta franja dos agregados:

    rendimento total dos agregados com rendimentos < 9,150.96€
    
Para o segundo, visto que utilizam a isenção por completo, temos:

    # agregados com rendimentos acima de 9,150.96€ x 9,150.96€

No entanto, encontramos uma pequena dificuldade: os dados estão disponíveis apenas por escalões (0 aos 5,000€, 5,000 aos 10,000€, etc.) e o limite de 9,150.96€ encontra-se no meio deste último. Por exemplo, só sabemos que o rendimento total dos que ganharam entre 0 e 5,000€ no ano foi de 1.635 milhões de euros, e de 11.382 para os que ganharam entre 5,000 e 10,000€. No primeiro, sabemos que todo esse rendimento está isento. Mas, no segundo, apenas a porção dos 5,000.00 aos 9,150.96€ está isenta, o restante sendo taxado a 15%. Poderíamos dizer que 9,150.96€ está próximo o suficiente de 10,000.00€ e incluir o rendimento todo desse escalão. No entanto, estaríamos a isentar rendimento a mais (ainda que pouco).
Este é um problema que também estará presente quando passarmos para o modelo de duas taxas. Assim, modelaremos a distribuição de rendimentos do escalão dos dados onde caírem os limites dos escalões das taxas. Por exemplo, para o limite de 9,150.96€, modelaremos a distribuição do escalão 5,000 a 10,000€. Este procedimento é explicado no fim do artigo. Com o modelo, poderemos calcular os valores para rendimentos até 9,150.96€.

Assim, obtemos:

        9,794 M€  (rendimento total dos agregados com rendimentos < 9,006.90€)
    1,787,532     (# agregados com rendimentos < 9,006.90€)

Sabendo que o número total de agregados é 5,408,288, podemos finalmente calcular o valor total da isenção:

    9,794 M€ + (5,408,288 - 1,787,532) x 9,150.96 € = 42,928 M€

Tendo em conta apenas esta isenção, a receita do IRS seria:

    0.15 x (100,562 - 42,928) = 8,645 M€

que, face ao sistema de 2019, representaria uma perda de receita de:

    12,939 - 8,645 = 4,294 M€ = 2.0% do PIB

Este é o valor mínimo da perda. Por um lado, porque considerámos apenas um trabalhador por agregado, e portanto apenas uma isenção por agregado. Por outro lado, porque falta ainda incluir a isenção por filho.


## Majorante

No entanto, antes de passar à isenção do filho, podemos agora fazer o oposto. Em vez de minorar, majorar.

    Perda = IRS_antigo - IRS
          = IRS_antigo - 0.15 x (Rendimento Total - Isenção Total)
          = IRS_antigo + 0.15 x (Isenção Total - Rendimento Total)
          ≤ IRS_antigo + 0.15 x (Isenção_2pa - Rendimento Total)

Aqui, Isenção_2pa é o valor total das isenções, assumindo duas por agregado, quando na realidade, muito agregados (ex.: não casados) terão direito a apenas uma<a id="cite-footnote-c" href="#footnote-c"><sup>(c)</sup></a>. Neste caso, o que calcularmos de perda será maior (não contando com a isenção por filho) que a perda real.

Procedemos de igual maneira que antes, com a diferença de que o limite passa de 9,150.96€ para 18,301.92€, o dobro.

       33,879 M€  (rendimento total dos agregados com rendimentos < 18,301.92€)
    3,671,637     (# agregados com rendimentos < 18,301.92€)

Refazendo as contas com os novos valores, o valor total da isenção passa a:

    33,879 M€ + (5,408,288 - 3,671,637) x 18,301.92 € = 65,663 M€

dando uma receita do IRS de:

    0.15 x (100,562 - 65,663) = 5,235 M€

o que resultaria numa perda de receita de:

    12,939 - 7,704 = 7,704 M€ = 3.6% do PIB

Concluímos então que a perda de receita não ultrapassará os 3.6% do PIB. Claro, sem contar com a perda relativa à isenção por filho.


## Isenção por filho

Nos dois cálculos anteriores, não incluímos a isenção de 400€ por filho por mês (200€ por progenitor ou 400€ em famílias monoparentais), isto é, 5,600€ por filho por ano.

A razão para termos deixado esta isenção para trás até agora é que o cálculo do valor total dela apresenta uma dificuldade face aos dados. Falta-nos a distribuição do número de filhos pelo nível de rendimentos. Por exemplo, uma mãe com rendimentos de 750€ e com um filho (família monoparental) não utiliza a isenção do filho por completo, já que 750 < 643.35 + 400. O mesmo se pode passar até com um casal, ambos os membros ganhando 750€, já que 750 < 643.35 + 200. Com múltiplos filhos, este efeito é mais pronunciado.

Por estas razões, torna-se difícil o cálculo do valor da isenção e consequente perda de receita do IRS. Sabendo que o minorante teórico é de 0, num caso limite em que todos os filhos pertencem a pais cujos rendimentos já estão cobertos pela isenção pessoal, calcularemos apenas o nível máximo de isenção total, ou seja, o majorante<a id="cite-footnote-d" href="#footnote-d"><sup>(d)</sup></a>:

    # filhos x 5,600 € = 1,951,310 x 5,600 € = 10,927 M€
    
o que, a uma taxa de 15%, representa uma perda de receita de       

    0.15 x 10,927 = 1,639 M€ = 0.8% do PIB

Se contássemos todo o bolo, 10,927 M€, estaríamos a sobreestimar a dedução e portanto a perda de receita. No entanto, tendo em conta que a maioria dos agregados com filhos têm dois pais a trabalhar e que o salário mínimo em 2019 era de 8,400€ por ano, podemos afirmar com alguma confiança que o valor real da perda de receita será uma fração significativa de 1,639 milhões de euros.


# Sistema de duas taxas

## Minorante e majorante

O cálculo do minorante e do majorante para o sistema de duas taxas é semelhante ao da taxa única, apenas mais moroso, uma vez que passamos de dois a três escalões:

    0 a 9,150.96€         0%
    9,150.96 a 30,000€   15%
    Acima de 30,000€     28%

Para os agregados do primeiro escalão, isentamos toda a receita. Para o segundo escalão, isentamos os 9,150.96€ por completo e tributamos 15% do remanescente para os agregados que caiam no segundo escalão. Por fim, no terceiro escalão, isentamos os 9,150.96€ por completo e tributamos 15% de 20,849.04€ (=30,000-9,150.96) do segundo escalão e 28% do remanescente.

Obtemos então para o minorante:

    11,318 M€                (receita do IRS)
     1,621 M€ = 0.8% do PIB  (perda de receita)

Para o majorante, há que ter atenção que não é apenas a isenção que é duplicada, mas também os limites dos escalões (ex.: 30,000€ -> 60,000€), obtendo-se:

     9,434 M€                (receita do IRS)
     3,505 M€ = 1.6% do PIB  (perda de receita)


## Isenção por filho

Repetimos o cálculo, tendo em conta que a taxa marginal máxima aumentou de 15% para 28%:

    10,927 M€ x 0.28 = 3,060 M€ = 1.4% do PIB

Isto corresponde obviamente ao caso limite em que todos os filhos pertencem a pais com rendimentos superiores a 32,800€ cada.


# Conclusão

### Duas taxas (temporário)

No sistema temporário de duas taxas, o impacto imediato orçamental ficaria **entre os 0.8 e o 1.6% do PIB**. A esta perda, **acresce um valor inferior a 1.4% do PIB**, relativa à isenção por filho. Pegando no ponto médio dos dois intervalos, podemos calcular um **valor indicativo de 1.9% do PIB (4.1 mil milhões de euros)**.
Este valor é maior do que o dobro daquele indicado no programa de 2022, 0.9% do PIB (2 mil milhões de euros), que por si só, já representa uma significativa redução de receita. Relembre-se que a média dos défices dos quatro anos anteriores à pandemia é de 1.3% do PIB.


### Taxa única

No sistema de taxa única, o impacto imediato orçamental ficaria **entre os 2.0 e os 3.6% do PIB**<a id="cite-footnote-e" href="#footnote-e"><sup>(e)</sup></a>. A esta perda, **acresce um valor inferior a 0.8% do PIB**, relativa à isenção por filho. Pegando no ponto médio dos dois intervalos, podemos calcular um **valor indicativo de 3.2% do PIB (6.9 mil milhões de euros)**.
Infelizmente, o programa de 2022 não oferece uma estimativa do impacto orçamental deste sistema, já que, face a 2019, introduziram na proposta o sistema temporário de duas taxas. Mas, é interessante ver que o programa de 2019 dá como estimativa menos de 1% do PIB. Ora, como dito no início, se o sistema de taxa única é menos punitivo fiscalmente que o de duas taxas, como pode ele custar menos? Fica a questão.

Finalmente, ressalvamos uma vez mais que os efeitos de segunda ordem relativos ao aumento do rendimento disponível podem mitigar parcialmente estes valores. Ainda assim, é provável que tal não seja suficiente, pelo que ambos os sistemas (taxa única ou duas taxas) arriscam abrir buracos orçamentais bastante significativos.

---

## Modelo de distribuição dentro de um escalão

    x = rendimento

    f(x) * (x2 - x1) = # agregados com rendimentos entre x1 e x2 (com x2-x1 pequeno)
    ∫_x1^x2 f(x) dx  = # total de agregados com rendimento entre x1 e x2

    f(x) * (x2 - x1) * x1 = rendimento de todos os agregados com rendimentos entre x1 e x2 (com x2-x1 pequeno)
    ∫_x1^x2 f(x) x dx = rendimento de todos os agregados com rendimentos entre x1 e x2

Assumindo uma distribuição linear, f(x) = ax + b, temos:

    ∫_x1^x2 f(x) dx   = a (x2^2 - x1^2)/2 + b (x2 - x1)       = N
    ∫_x1^x2 f(x) x dx = a (x2^3 - x1^3)/3 + b (x2^2 - x1^2)/2 = R

onde N e R são o número total de agregados e o rendimento total dos agregados com rendimento entre x1 e x2, respetivamente. Temos um sistema linear de duas equações e duas incógnitas (a e b), que se resolve facilmente.

Utilizando x1 e x2 como os valores dos limites inferiores e superiores dos escalões dos dados, podemos posteriormente calcular o número de agregados e o rendimento de um ponto intermédio x1 < x < x2.


---

<a id="footnote-a" href="#cite-footnote-a"><sup>(a)</sup></a> De notar que a totalidade da receita de IRS 13,171.2 milhões de euros, já que existem certos rendimentos taxados a uma taxa liberatória fixa e que não são contabilizados nos dados da AT. Em qualquer dos casos, a diferença é relativamente pequena.

<a id="footnote-b" href="#cite-footnote-b"><sup>(b)</sup></a> Segundo o texto, a isenção é apenas para rendimentos do trabalho. A priori, outros rendimentos, como rendas não seriam isentos. Mas, tendo em conta que a larga maioria dos que têm esses outros rendimentos, também têm rendimentos do trabalho, a isenção também se aplica. Também não parece muito o estilo da IL distinguir origens de rendimentos.

<a id="footnote-c" href="#cite-footnote-c"><sup>(c)</sup></a> Existem certos agregados com 3 pessoas com direito a isenção. Por exemplo, um casal com filho até 25 anos que aufira menos de 14 vezes o SMN num ano. Mas, a frequência destes casos deve ser desprezável.

<a id="footnote-d" href="#cite-footnote-d"><sup>(d)</sup></a> Soma dos grupos até à idade de 19 (ano de 2019). (Uma porção significativa do grupo 20-24 também se encontra em situação de dependente (ex.: estudantes universitários), pelo que seria mais correto contá-los. Mas, uma vez que não temos acesso fácil ao valor exato, não o fazemos.) [PORDATA](https://www.pordata.pt/Portugal/Popula%C3%A7%C3%A3o+residente++m%C3%A9dia+anual+total+e+por+grupo+et%C3%A1rio-10).

<a id="footnote-e" href="#cite-footnote-e"><sup>(e)</sup></a> Segundo a [imprensa](https://rr.sapo.pt/noticia/economia/2020/09/29/taxa-unica-de-irs-quanto-custa-a-proposta-da-iniciativa-liberal/209017/), a Deloitte estima um custo até 3.5 mil milhões, isto é 1.7% do PIB. Este majorante é menor do que o minorante que estimado neste artigo, que implica que as estimativas deste artigo não são consistentes com as da Deloitte. Semelhantemente aos valores dados pela IL, como os cálculos da Deloitte não foram publicados, não é possível comparar e ver de onde vem a diferença.



