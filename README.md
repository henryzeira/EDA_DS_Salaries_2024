# Data Science Salaries 2024 - EDA - Universidade dos Dados
## Contexto do Projeto
A motivação inicial para a realização dessa Análise Exploratória de Dados vem da competição do clube Universidade dos Dados, cujo objetivo é impulsionar a criação de projetos. A competição foi organizada pelo André Yukiu. 

No campo em constante evolução da ciência de dados, compreender as tendências salariais é fundamental. Este conjunto de dados traz os salários da Ciência de Dados de 2020 a 2024, fornecendo insights sobre tendências, variações regionais etc.

**Objetivo da análise:** Entender a relação das características dos profissionais da pesquisa com a remuneração da área.

**Variável:** ‘salary\_in\_usd’
## Sobre o Dataset
O conjunto de dados engloba uma coleção abrangente de informações salariais de ciência de dados, cobrindo um período de cinco anos, de 2020 a 2024. Os dados contemplam diversos aspectos relacionados aos salários, proporcionando uma visão multifacetada da remuneração no campo.

Fonte: [Data Science Salaries 2024 (kaggle.com)](https://www.kaggle.com/datasets/sazidthe1/data-science-salaries/data)

**Estrutura do conjunto de dados**

|**job\_title**|O cargo ou função associada ao salário informado.|
| :- | :- |
|**experience\_level**|O nível de experiência do indivíduo.|
|**employment\_type**|Indica se o emprego é a tempo integral, a tempo parcial etc.|
|**work\_models**|Descreve diferentes modelos de trabalho (remoto, presencial, híbrido).|
|**work\_year**|O ano específico em que as informações salariais foram registradas.|
|**employee\_residence**|O local de residência do empregado.|
|**salary**|O salário informado na moeda original.|
|**salary\_currency**|A moeda em que o salário é denominado.|
|**salary\_in\_usd**|O salário convertido em dólares americanos.|
|**company\_location**|A localização geográfica da organização empregadora.|
|**company\_size**|O tamanho da empresa, categorizado pelo número de funcionários.|

## Preparação e Tratamento de Dados
Toda a preparação inicial e tratamento da base foi realizada utilizando algumas bibliotecas do Python. Disponibilizarei o arquivo no repositório com os demais dados. Embora não seja obrigatório, recomendo visualizar essa etapa antes de seguir com a etapa das análises para um maior contexto do projeto. 
## Análise e visualização de dados
Como já mencionado anteriormente, o objetivo aqui é analisar a variável salário com relação as outras variáveis da pesquisa. Portanto, vou iniciar a análise pela variável salário. 
### Faixa Salarial
Para as análises, vou utilizar indicies de faixa salarial, numerados de 1 a 18. Esses índices representarão as respectivas faixas salariais nos visuais e serão as referências das faixas salariais. 

A partir do gráfico 1 é possível observar como a variável salary\_in\_usd está distribuída. Embora a distribuição de valores seja levemente inclinada para a direita, a média e mediana estão bem próximas.

O desvio padrão é relativamente alto, o que sugere que há uma grande dispersão nos salários desses profissionais. Analisando o intervalo de valores do conjunto, isso fica mais claro, que é $ 15,000.00 a $ 750,000.00. 

A mediana é representada pela faixa 5 de $ 120,000.00 a $ 150,000.00. 

Gráfico 1: Histograma da variável salary\_in\_usd.

<div align="center">

![image](https://github.com/henryzeira/EDA_DS_Salaries_2024/assets/143764500/831d15ee-8ee6-4392-9c8e-76d19ac19398)

</div>

Tabela 1: Estatísticas descritivas da variável salary\_in\_usd (unidade de $).

<div align="center">

|*salary\_in\_usd*||
| :-: | :- |
|||
|Média|145560,5586|
|Erro padrão|873,3613741|
|Mediana|138666|
|Modo|100000|
|Desvio padrão|70946,83807|
|Variância da amostra|5033453832|
|Curtose|6,493920367|
|Assimetria|1,360705506|
|Intervalo|735000|
|Mínimo|15000|
|Máximo|750000|
|Soma|960554126|
|Contagem|6599|
|Nível de confiança(95,0%)|1712,070907|

</div>

Tabela 2: Faixas salariais e seus respectivos índices. 

|**Descrição da Faixa Salarial**|**Faixa Salarial**|**Contagem**|
| :- | :- | :- |
|**Acima de $ 510.000 por ano**|18|9|
|**de $ 450.000 a 480.000 por ano**|16|1|
|**de $ 420.000 a 450.000 por ano**|15|8|
|**de $ 390.000 a 420.000 por ano**|14|9|
|**de $ 360.000 a 390.000 por ano**|13|26|
|**de $ 330.000 a 360.000 por ano**|12|28|
|**de $ 300.000 a 330.000 por ano**|11|70|
|**de $ 270.000 a 300.000 por ano**|10|154|
|**de $ 240.000 a 270.000 por ano**|9|287|
|**de $ 210.000 a 240.000 por ano**|8|448|
|**de $ 180.000 a 210.000 por ano**|7|741|
|**de $ 150.000 a 180.000 por ano**|6|967|
|**de $ 120.000 a 150.000 por ano**|5|1237|
|**de $ 90.000 a 120.000 por ano**|4|1117|
|**de $ 60.000 a 90.000 por ano**|3|910|
|**de $ 30.000 a 60.000 por ano**|2|483|
|**Menos de $ 30.000 por ano**|1|104|
|**Total Geral**|**6599**||

Gráfico 2. Boxplot da variável salary\_in\_usd.

<div align="center">

![Aspose Words e31dd834-f655-423c-b089-aefec48026eb 002](https://github.com/henryzeira/EDA_DS_Salaries_2024/assets/143764500/037a85b8-da45-4294-b637-3ac064fb0c6b)

</div>

### Comparação das faixas salariais por ano
Observa-se uma tendência de crescimento nas médias salariais ao decorrer dos anos. Embora haja poucos dados coletados do ano de 2024 em relação a 2023 (gráfico 4), a média de 2024 ainda foi mais alta. Uma análise mais justa seria se o período de pesquisa fosse igual para todos os anos. 

A variação mais significativa é do ano de 2021 para 2023, que foi um aumento de **47%** na média salarial. Isso representa um aumento da faixa salarial de $ 60,000.00 a $ 90,000.00 para $ 120,000.00 a $ 150,000.00. 

Gráfico 3: Médias salariais por ano 

<div align="center">

![Aspose Words e31dd834-f655-423c-b089-aefec48026eb 003](https://github.com/henryzeira/EDA_DS_Salaries_2024/assets/143764500/d8a50268-519c-45b0-8f43-5bf6cbee38d1)

</div>

Gráfico 4: Distribuição da faixa salarial por ano

<div align="center">

![Aspose Words e31dd834-f655-423c-b089-aefec48026eb 004](https://github.com/henryzeira/EDA_DS_Salaries_2024/assets/143764500/2e35b3c1-b771-4bbd-818c-cff4294a66f8)

</div>

## **Dados sobre o trabalho na área**
### <a name="_hlk162394009"></a>Cargo
A remuneração da maioria dos entrevistados está associada as descrições de cargo **Data Scientist, Data Engineer e Machine Learning**. Esses cargos representam **68%** da base.

Os cargos relacionados a **Machine Learning** têm a média mais alta, enquanto cargos relacionados a **Data Analyst** tem a média mais baixa. **Machine Learning e Data Scientist** são os cargos mais bem remunerados. Isso pode refletir a demanda e o valor atribuído a essas especializações dentro da área. 

Curiosamente os cargos envolvidos a liderança não tem as maiores médias.

Tabela 3: Frequência do Cargo.  

|**Cargo**|**Freq. Absoluta**|**Freq. Relativa**|**Freq. Acumulada %**|
| :- | :- | :- | :- |
|**Data Scientist**|1934|29,3%|29,3%|
|**Data Engineer**|1490|22,6%|51,9%|
|**Machine Learning**|1037|15,7%|67,6%|
|**Data Analyst**|941|14,3%|81,9%|
|**Business Intelligence**|547|8,3%|90,2%|
|**Data Manager/Lead/Specialist**|424|6,4%|96,6%|
|**Research/Analytics Scientist/Analyst/Engineer**|221|3,3%|99,9%|
|**Cloud/Data Operations**|5|0,1%|100,0%|
|**Total Geral**|**6599**|**100,0%**||

Gráfico 5: Distribuição do Cargo.

<div align="center">

![Aspose Words e31dd834-f655-423c-b089-aefec48026eb 005](https://github.com/henryzeira/EDA_DS_Salaries_2024/assets/143764500/73239d47-4363-469e-85bd-2928d1abd104)

</div>

Gráfico 6: Cargo x Remuneração

<div align="center">

![Aspose Words e31dd834-f655-423c-b089-aefec48026eb 006](https://github.com/henryzeira/EDA_DS_Salaries_2024/assets/143764500/033818c1-1f09-4377-9160-be0c147424f6)

</div>

### <a name="_hlk162394018"></a>Nível de Experiência
A maioria dos profissionais da pesquisa possui **nível sênior de experiência**, representando **62%** da amostra. Isso sugere que há uma proporção significativa de profissionais com um alto nível de habilidades e experiência no campo. Isso pode refletir a natureza altamente técnica e especializada da área de dados, onde a experiência e a expertise são altamente valorizadas.

Profissionais em **níveis executivos** têm a remuneração média mais alta. Isso é consistente com a expectativa de que os executivos recebam salários mais altos devido às responsabilidades de liderança e tomada de decisões estratégicas associadas a esses cargos.

Profissionais em **níveis de entrada** têm a remuneração média mais baixa, o que pode representar um desafio para atrair e reter talentos juniores na área de ciência de dados. Estratégias de desenvolvimento de carreira e programas de capacitação podem ser importantes para abordar esses desafios e promover a progressão profissional desses profissionais.

Tabela 4: Frequência do Nível de Experiência.

|**Nível de Experiência**|**Freq. Absoluta**|**Freq. Relativa**|**Freq. Acumulada %**|
| :- | :-: | :- | :- |
|**Senior-level**|4105|62,21%|62,21%|
|**Mid-level**|1675|25,38%|87,59%|
|**Entry-level**|565|8,56%|96,15%|
|**Executive-level**|254|3,85%|100,00%|
|**Total Geral**|**6599**|**100,00%**||

Gráfico 7: Distribuição do Nível de Experiência.

<div align="center">

![Aspose Words e31dd834-f655-423c-b089-aefec48026eb 007](https://github.com/henryzeira/EDA_DS_Salaries_2024/assets/143764500/8afd4726-4647-41cc-bded-14dd95558dc9)

</div>

Gráfico 8: Nível de Experiência x Remuneração

<div align="center">

![Aspose Words e31dd834-f655-423c-b089-aefec48026eb 008](https://github.com/henryzeira/EDA_DS_Salaries_2024/assets/143764500/0af1eddb-5efe-4a62-99e2-ef40608fd1b6)

</div>

### <a name="_hlk162394027"></a>Modelos de Trabalho
A maioria dos profissionais da pesquisa trabalha no modelo **on-site (presencial)**, representando **58%** do conjunto de dados. Isso sugere que o trabalho presencial ainda é predominante neste campo. No entanto, o trabalho **remoto** também é bastante comum, representando **39%** da amostra. 

É notável a forte tendência no modelo presencial. O modelo remoto foi superior em tempos de pandemia, logo após, o modelo presencial voltou a liderar.

Profissionais que trabalham no modelo on-site têm a média salarial mais alta, seguidos pelos profissionais em trabalho remoto, enquanto aqueles no modelo híbrido têm a média salarial mais baixa.

Profissionais Remote e Hibrid tem a concentração de valores entre as faixas salariais 4 – 6 e 2 – 4 respectivamente, enquanto, on-site tem média superior aos outros modelos e valores mais dispersos. 

Tabela 5: Frequência do Modelo de Trabalho.

|**Modelo de Trabalho**|**Freq. Absoluta**|**Freq. Relativa**|**Freq. Acumulada %**|
| :- | :- | :- | :- |
|**On-site**|3813|57,78%|57,78%|
|**Remote**|2561|38,81%|96,59%|
|**Hybrid**|225|3,41%|100,00%|
|**Total Geral**|**6599**|**100,00%**||

Gráfico 9: Distribuição do Modelo de Trabalho.

<div align="center">

![Aspose Words e31dd834-f655-423c-b089-aefec48026eb 009](https://github.com/henryzeira/EDA_DS_Salaries_2024/assets/143764500/311a18e1-b34e-42d1-8569-a88e124e78ac)

</div>

Gráfico 10: Modelo de Trabalho por Ano

<div align="center">

![Aspose Words e31dd834-f655-423c-b089-aefec48026eb 010](https://github.com/henryzeira/EDA_DS_Salaries_2024/assets/143764500/fd4ebf55-4d71-473a-ae0e-e787cd99c452)

</div>

Gráfico 11: Modelo de Trabalho x Remuneração

<div align="center">

![Aspose Words e31dd834-f655-423c-b089-aefec48026eb 011](https://github.com/henryzeira/EDA_DS_Salaries_2024/assets/143764500/e5c6ccf2-3e01-4ec6-a6a7-2796f2e7f899)

</div>

### <a name="_hlk162394036"></a>Tipo de Emprego
A grande maioria dos profissionais está empregada em tempo integral, representando **99%** da amostra. Isso sugere que o emprego em tempo integral é o arranjo de trabalho mais comum e preferido entre os profissionais.

A média de **Contract** é influenciada por valores atípicos, portanto, essa categoria apresenta uma grande dispersão dos valores em relação as demais categorias. Isso sugere particularidades nesse tipo de emprego. 

Tabela 6: Frequência do Tipo de Emprego.

|**Modelo de Trabalho**|**Freq. Absoluta**|**Freq. Relativa**|**Freq. Acumulada %**|
| :- | :- | :- | :- |
|**Full-time**|6552|99,29%|99,29%|
|**Contract**|19|0,29%|99,58%|
|**Part-time**|16|0,24%|99,82%|
|**Freelance**|12|0,18%|100,00%|
|**Total Geral**|**6599**|**100,00%**||

Gráfico 12: Distribuição do Tipo de Emprego.

<div align="center">

![Aspose Words e31dd834-f655-423c-b089-aefec48026eb 012](https://github.com/henryzeira/EDA_DS_Salaries_2024/assets/143764500/618cc29d-5087-4aae-a58b-d755e4415bf6)

</div>

Gráfico 13: Tipo de Emprego x Remuneração

<div align="center">

![Aspose Words e31dd834-f655-423c-b089-aefec48026eb 013](https://github.com/henryzeira/EDA_DS_Salaries_2024/assets/143764500/e3d967bc-af16-4725-a17d-0c05bdc954cb)

</div>

### **Dados demográficos**
## <a name="_hlk162394048"></a>Local da Residência
A maioria dos profissionais reside na **América do Norte**, representando **84%** da base. Isso indica que a América do Norte é uma região dominante em termos de residência dos profissionais da área de dados.

Há uma disparidade da remuneração por local de residência. Profissionais na América do Norte têm a média salarial mais alta, seguidos por profissionais na Oceania, Europa e América do Sul. Profissionais na África e Ásia têm as médias salariais mais baixas.

Esses resultados sugerem que indústrias da tecnologia relacionadas a área de dados estão concentrada na América do Norte. 

Tabela 7: Frequência do Local da Residência.

|**Local de Residência**|**Freq. Absoluta**|**Freq. Relativa**|**Freq. Acumulada %**|
| :- | :- | :- | :- |
|**América do Norte**|5568|84,38%|84,38%|
|**Europa**|796|12,06%|96,44%|
|**Ásia**|119|1,80%|98,24%|
|**América do Sul**|48|0,73%|98,97%|
|**África**|36|0,55%|99,52%|
|**Oceania**|32|0,48%|100,00%|
|**Total Geral**|**6599**|**100,00%**||

Gráfico 14: Distribuição do Local da Residência. 

<div align="center">

![Aspose Words e31dd834-f655-423c-b089-aefec48026eb 014](https://github.com/henryzeira/EDA_DS_Salaries_2024/assets/143764500/4f745dab-3079-4498-a660-410168cd178e)

</div>

Gráfico 15: Local da Residência x Remuneração

<div align="center">

![Aspose Words e31dd834-f655-423c-b089-aefec48026eb 015](https://github.com/henryzeira/EDA_DS_Salaries_2024/assets/143764500/38023167-dfa4-4d8e-83c7-be0bfdd81204)

</div>

### <a name="_hlk162394060"></a>Localização da Empresa
Assim como na tabela de Local de Residência, a maioria das empresas do conjunto de dados está localizada na **América do Norte**, representando **85%** das empresas listadas. Isso reflete a concentração significativa de empresas da área de ciência de dados na América do Norte.

A distribuição da remuneração por local de residência é muito semelhante a distribuição da variável Localização da Residência. 

Tabela 8: Frequência da Localização da Empresa.

|Local da Empresa|Freq. Absoluta|Freq. Relativa|Freq. Acumulada %|
| :- | :- | :- | :- |
|**América do Norte**|5614|85,07%|85,07%|
|**Europa**|783|11,87%|96,94%|
|**Ásia**|101|1,53%|98,47%|
|**América do Sul**|38|0,58%|99,05%|
|**Oceania**|35|0,53%|99,58%|
|**África**|28|0,42%|100,00%|
|**Total Geral**|**6599**|**100,00%**||

Gráfico 16: Distribuição da Localização da Empresa

<div align="center">

![Aspose Words e31dd834-f655-423c-b089-aefec48026eb 016](https://github.com/henryzeira/EDA_DS_Salaries_2024/assets/143764500/4b4c9ade-8d25-4025-980c-64ec72424f49)

</div>

Gráfico 17: Localização da Empresa x Remuneração 

<div align="center">

![Aspose Words e31dd834-f655-423c-b089-aefec48026eb 017](https://github.com/henryzeira/EDA_DS_Salaries_2024/assets/143764500/657b53fe-0423-48bc-bb3b-deb3afd7db14)

</div>

### <a name="_hlk162394071"></a>Tamanho da Empresa
A maioria das empresas listadas na amostra é de **médio porte**, representando **89%** do total. Portanto a maioria dos profissionais da área de ciência de dados trabalha em empresas de médio porte.

Empresas de porte médio tem maior média de remuneração. Além disso, abrange uma gama maior de faixa salarial. Isso sugere alta competitividade por recrutamento entre empresas de médio e grande porte. 

Profissionais que consideram oportunidades de emprego devem levar em conta não apenas o tamanho da empresa, mas também a remuneração associada a cada tamanho.

Tabela 9: Frequência do Tamanho da Empresa.

|Tamanho da Empresa|Freq. Absoluta|Freq. Relativa|Freq. Acumulada %|
| :- | :- | :- | :- |
|**Medium**|5860|88,80%|88,80%|
|**Large**|569|8,62%|97,42%|
|**Small**|170|2,58%|100,00%|
|**Total Geral**|**6599**|**100,00%**||

Gráfico 18: Distribuição do Tamanho da Empresa.

<div align="center">

![Aspose Words e31dd834-f655-423c-b089-aefec48026eb 018](https://github.com/henryzeira/EDA_DS_Salaries_2024/assets/143764500/42d20725-6ec4-41ca-b479-7c5737825abf)

</div>

Gráfico 19: Tamanho da Empresa x Remuneração 

<div align="center">

![Aspose Words e31dd834-f655-423c-b089-aefec48026eb 019](https://github.com/henryzeira/EDA_DS_Salaries_2024/assets/143764500/83f737e6-e7d9-4db8-9718-ce080cfcabb6)

</div>

## Conclusão 

Há a possibilidade de uma tendência de crescimento ao longo dos anos, indicando a valorização dos profissionais da área.

Em termos de salário, as áreas mais bem pagas é Data Scientist, Data Engineer e Machine Learning, também são os mais predominantes. Portanto se pretende adentrar e esse mercado, tenha em mente esses cargos.

O mercado tem muitos profissionais experientes. A maioria é sênior. Isso sugere um aprendizado contínuo na área para o desenvolvimento profissional. 

Embora não haja uma grande variação entre remuneração média do modelo de trabalho presencial e remoto, a maior parte dos profissionais trabalham no modelo presencial. Após a pandemia, houve grande aumento no modelo presencial. 

Emprego em tempo integral tem as maiores médias de remuneração. 

Os resultados indicam que o melhor lugar para profissionais da área é na América do Norte. Isso sugere que as indústrias de tecnologia relacionadas à ciência de dados estão concentradas na América do Norte, embora também haja oportunidades em outras regiões.

Profissionais em empresas de médio porte têm a remuneração média mais alta, sugerindo uma competição intensa por talentos entre empresas de médio e grande porte. Isso destaca a importância de considerar não apenas o tamanho da empresa, mas também a remuneração ao avaliar oportunidades de emprego.

**Resumo:** Considerando esses insights, concluímos que o mercado de trabalho em ciência de dados está em alta demanda, com uma tendência de crescimento salarial ao longo do tempo. Profissionais com experiência, especialização e que buscam oportunidades em empresas de médio porte na América do Norte tendem a maior probabilidade de receber remuneração mais alta. No entanto, é importante considerar a diversidade de oportunidades e o equilíbrio entre remuneração, modelo de trabalho e localização geográfica ao tomar decisões de carreira.

**Próximos passos do projeto:** Testes estatísticos para validar a significância de algumas hipóteses. 
