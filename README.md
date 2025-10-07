Objetivo

Apresentar uma análise exploratória dos microdados da PNAD COVID-19, com foco em identificar padrões relacionados a sintomas, diagnósticos, perfil sociodemográfico e fatores associados à gravidade da doença no Brasil, de acordo com o desafio proposto. O objetivo é utilizar técnicas de agregação e visualização de dados para revelar informações relevantes que possam apoiar a compreensão dos impactos da COVID-19 na população.

Metodologia

Dados

Para essa análise utilizamos os dados do PNAD - COVID 19. E com base em seu dicionário de dados selecionamos as seguintes perguntas:

Características socioeconómicas:
A003 - Sexo
D0051 - Recebeu auxílios emergenciais relacionados ao coronavírus
E001 - Durante o período da pandemia alguém deste domicílio solicitou algum empréstimo?
V1022 - Situação do domicílio
B007 - Tem algum plano de saúde médico, seja particular, de empresa ou de órgão público

Sintomas clínicos:
B0011 - Na semana passada teve febre?
B0012 - Na semana passada teve tosse?
B0013 - Na semana passada teve dor de garganta?
B0014 - Na semana passada teve dificuldade para respirar?
B0015 - Na semana passada teve dor de cabeça?
B0016 - Na semana passada teve dor no peito?
B0017 - Na semana passada teve náusea?
B0018 - Na semana passada teve nariz entupido ou escorrendo?
B0019 - Na semana passada teve fadiga?
B00110 - Na semana passada teve dor nos olhos?
B00111 - Na semana passada teve perda de cheiro ou sabor?
B00112 - Na semana passada teve dor muscular?

Comportamento da população:
B002 - Por causa disso, foi a algum estabelecimento de saúde?
B0031 - Providência tomada para recuperar dos sintomas foi ficar em casa
B008 - O(A) Sr(a) fez algum teste para saber se estava infectado(a) pelo coronavírus?
B009B - Qual o resultado? (teste SWAB - cotonete na boca/nariz)
B011 - Na semana passada, devido à pandemia do Coronavírus, em que medida o(a) Sr(a) restringiu o contato com as pessoas?
		
Além das perguntas selecionadas, separamos algumas outras que nos serviram de para criar novas colunas através de agrupamentos.  
B0101 até B0106 - Agrupamos em uma nova coluna que se já foi diagnosticada com um agravante para a covid.
C01012 - Separamos em classes (E, D, C, B, A)
A002  - Separamos em faixas etárias.
B0101 Algum médico já lhe deu o diagnóstico de diabetes?
B0102 Algum médico já lhe deu o diagnóstico de hipertensão?
B0103 Algum médico já lhe deu o diagnóstico de asma/bronquite/enfisema/doenças respiratórias crônicas ou de pulmão?
B0104 Algum médico já lhe deu o diagnóstico de doenças do coração (infarto, angina, insuficiência cardíaca, arritmia)?
B0105 Algum médico já lhe deu o diagnóstico de depressão?
B0106 Algum médico já lhe deu o diagnóstico de câncer?
C01012 Valor em dinheiro recebido normalmente em todos os trabalhos
A002 Idade do morador

Tratamento e processamento
Nesta etapa, foi realizado o tratamento dos dados provenientes da pesquisa PNAD COVID-19, do IBGE, com o objetivo de garantir a qualidade e consistência das informações antes das análises exploratórias.
Foram aplicadas etapas de limpeza e padronização das variáveis, como renomeação de colunas para facilitar a interpretação, conversão de tipos de dados e tratamento de valores ausentes. Também foi criada uma nova coluna para representar o resultado do teste de COVID-19, consolidando respostas provenientes de múltiplas variáveis.
Além disso, realizou-se a criação de faixas etárias, permitindo uma análise mais segmentada e visualmente compreensível da distribuição dos sintomas entre diferentes grupos populacionais.
Essas transformações tornaram o conjunto de dados mais estruturado e pronto para as etapas de agregação e visualização, reduzindo ruídos e inconsistências comuns em bases massivas como a PNAD.


Agregações
Após o tratamento, foram aplicadas agregações para resumir as informações e identificar padrões relevantes na amostra. As principais agregações envolveram:
Coocorrência de sintomas, permitindo observar quais sintomas mais se manifestaram em conjunto (como febre e tosse, por exemplo);
Análises regionais, agrupando os dados por Unidade da Federação (UF) e por condição de saúde, para destacar desigualdades e diferenças entre regiões do país;
Associação entre comorbidades e sintomas, oferecendo uma visão sobre o agravamento de casos em determinados perfis de saúde.
Essas agregações serviram de base para os gráficos apresentados nas seções seguintes, que permitem visualizar de forma intuitiva as disparidades regionais e o comportamento dos sintomas ao longo da amostra analisada.
O resultado é uma estrutura de dados consolidada, capaz de sustentar análises estratégicas voltadas à gestão hospitalar e à formulação de políticas públicas em eventuais novos surtos.


