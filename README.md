Recebi um banco de dados de crédito referente a uma empresa, a partir da EBAC. Minha missão é ajudar essa empresa de concessão de crédito a analisar o seu histórico
de clientes para identificar o perfil de clientes inadimplentes e criar possíveis estratégias para evitar a inadimplência e até mesmo ajudar os clientes a saírem da
inadimplência.

Os passos que segui para isso estão descritos no notebook com algumas explicações sempre após os blocos de código. Pense nessas explicações como "legendas".

A seguir, darei uma visão geral do que foi feito em cada etapa:

- Importando bibliotecas: Trouxemos para nosso ambiente as bibliotecas que usaremos
- Explorando os Dados: Verificamos a estrtura dos dados, definimos (e explicamos o que é) o *schema* dos dados e qual era a situação dos dados faltantes.
- Limpeza e Transformação: Aqui nós tratamos os dados e decidimos o que fazer com os dados faltantes, deixando nosso DataSet limpo e pronto para análise.
- Visualização dos Dados: Aqui nós usamos uma das bibliotecas importadas para visualizar os dados em gráficos, assim como cruzarmos informações para verificarmos
nossos insigths.

Ao fim dessas etapas pude traçar um perfil para o cliente inadimplente:

* Ele realiza menos de 100 transações ao ano e o valor dessas transações fica abaixo de R$10.000.
* Neste grupo, clientes com menos de 60 transações e valor abaixo de 2500 aparentemente possuem ainda mais chances de se tornarem inadimplentes.
* Também podemos notar que a medida que a quantidade de transações aumenta, a inadimplência diminui. A mesma relação existe ao aumentar o valor das transações,
mas vale considerar que neste caso isso só é válido para um nicho isolado com valores de transações muito altos.
* O cliente passa por meses de inatividade antes de se tornar inadimplente
* Uma vez que o cliente está inadimplente, a comunicação da instituição com ele aumenta. De certa forma isso é algo esperado, já que a partir deste momento
iniciam-se as cobranças.

Porém, ao analisarmos os grupos com valores de transações abaixo de 2500 podemos notar que existem alguns adimplentes e estes possuem um comportamente comum:
realizar mais transações. Pensando nisso, podemos entender que aqueles que utilizam o cartão de crédito com mais frequência, possivelmente centralizando seus gastos,
conseguem gerir melhor suas transações. E aqueles que realizam menos transações podem acabar se endividando por um uso impulsivo em compras mais caras ou mesmo
por perder o controle ao não terem os gastos centrelazidos.

Pensando em como a instituição aumenta seu contato com os clientes inadimplentes (por motivos óbvios), podemos analisar as interações com os clientes e 
ver que alguns clientes se tornaram inadimplentes em 3 meses de inatividade, mas bastou 1 interação da empresa para que eles honrassem seu compromisso.

Assim, uma solução viável para a instuição de crédito pode ser: fornecer conteúdos de educação financeira, informando os clientes da existência destes conteúdos,
levando os clientes a adotarem um uso mais consciente do cartão. Esse "uso consciente" significa evitar grandes compras, migrando para uma centrlização
de gastos no cartão que levaria a mais transações de valores menores. Ao mesmo tempo, manter um acompanhamento com os clientes no grupo de risco,
entrando em contato a partir do 2º mês de inatividade ou quando grandes operações forem feitas em seu cartão.
