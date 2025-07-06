<h1 align="center"> MVP2_PUCRIO_ELEICOES </h1> 
<h2 align="center">Repo MVP 2 - Data Science and Analytics - PUC RIO MBA</h2> 


## Resumo do Projeto
Esse projeto tem como função cumprir etapa obrigatória do _Sprint_ de Análise de Dados e Boas Práticas do Curso de MBA em Data Science e Analytics oferecido pela Puc Rio.

## Objetivo
Construir todo o fluxo de pré-processamento e análise exploratória de um banco de dados, voltado para aplicação de um modelo de Machine Learning

### Objetivo do projeto:
A ideia inicial seria um mapeamento do público de candidatos, tentando entender as distribuições e as relações entre as características declaradas com os valores dos bens declarados e a quantidade de bens, tentando entender a possibilidade e/ou a necessidade de implementação de um modelo classificatório para extrair relações entre as variáveis.

### Base de dados: 
A base de dados utilizada(dataset) será a união de duas informações disponibilizadas pelo TSE ([Tribunal Superior Eleitoral](https://dadosabertos.tse.jus.br/), as bases são:
1. 2024 - Municipais [Candidatos](https://dadosabertos.tse.jus.br/dataset/candidatos-2024/resource/af76c401-0972-4ddf-8ea8-00e310ae53b4)
2. 2024 - Municipais [Bens](https://dadosabertos.tse.jus.br/dataset/candidatos-2024/resource/2d078979-116f-498f-ac5b-2e2a6fb0ff1f)

Bases com relação de candidatos e os respectivos bens declarados.

Esses dados estão sob licença de uso aberto para uso, manipulação e divulgação.

Cada tipo de arquivo utilizado arquivo possui um .pdf explicativo dos dados, uma espécie de catálogo, que disponibilizei também nesse repo: [Candidatos](https://github.com/GruveJL/MVP2_PUCRIO_ELICOES/blob/main/doc_candidatos.pdf)  [Bens](https://github.com/GruveJL/MVP2_PUCRIO_ELICOES/blob/10659563802920146b833ef111ce24bcff1402be/doc_bens_candidatos.pdf)

Vale ressaltar que este projeto não possui cunho político ou partidário, apenas a satisfação de um aprofundamento sob dados aplamente divulgados pelos orgãos competentes.

## Proposta Inicial
A Proposta inicial era avaliar mais períodos eleitorais, construir bases por anos, e validar possíveis correlações exitentes entre os anos, entretanto por questões de prazo para entrega do projeto, optei por focar nas eleições de 2024.

## Metodologia
A seguir levanterai alguns pontos do processo de tratamento e pré-processamento dos dados:

Todo projeto foi feito no [Google Colab](https://colab.google/), os arquivos utilizados estão disponibilizados nesse repo.
O arquivo [Main](https://colab.research.google.com/drive/15hh-Qxa51TSKqQDnp1sD7DGVcuPq0FHF?usp=sharing) com todas as etapas da análise e um arquivo de [Preparo](https://colab.research.google.com/drive/1r2rcIwebG56Psui7-0Yz0iiZmHqVkgM_?usp=sharing) para o processo inicial de engenharia de baixar as bases compactadas e extrair os .csv's dentro da pasta do colab.

A ideia inicial era unificar as bases em um único dataset, tratar dados estranhos com base nos catálogos fornecidos, utilizando da análise exploratória e de estatística descritiva decidir quais colunas e quais dados fazem sentido manter nas bases e quais fazem sentido retirar, no final adaptar essa base tratada para a implementação de um modelo de classificação.

Há na base alguns problemas já conhecidos, como já havia trabalhado com essa base já tinha em mente alguns problemas como a possibilidade de duplicação de candidatos na base, por poder haver 2º turno já que a base tem granularidade de candidatos por turno, a enorme quantidade de cateegorias distintas para alguns campos como o de "ocupação", ou o de "tipo de bem". Esses problemas tratei numa parte anterior a nálise chamada de "Primeiros Tratamentos", que apesar de também ser uma análise exploratória e envolver pré-processamento, optei por apartar pois após esses ajustes a análise se fez mais direta e menos complexa no entendimento.

O final fiz o split das bases de treino e teste e uma normalização, já que as colunas finais ficaram todas binárias exceto as de valores e quantidades de bens.

## Análise e Conclusão
A análise se fez muito produtiva porém negando quase todas as hipóteses. Optei por fazer hipóteses questionativas a fim de entender e aprofundar mais nas dimensões e especificidades dos dados. Por fim tentei responder as indagações com as correlações entre as colunas tratadas, infelizmente o resultado foi menor que o esperado. Quando olhado a relação entre as características e as informações de bens vemos praticamente nenhuma correlação, com alguns baixos indicadores. 

Pude observar na análise, que o dataset possui *outliers* extremamente desproporcionais à base, podendo ser facilmente verificado no gráfico de boxplot onde vemos apenas a representação desses outliers, talvez em futuras análises caiba retirar os chamados *outliers* e refazer as análises tentando encontrar novas correlações.

O resultado foi básico porém gratificante, dado o esforço e o fato de alimentar a minha curiosidade a respeito da relação entre patrimônio dos candidatos. 
Ademais agradeço a oportunidade e a proposta do projeto, tenho alguns anos de experiência na área de dados e poucas vezes fui confrontados com os questionamentos de como e por que fazer certas escolhas no processo de criação de um Dataset.

# Autores
| [<img src="https://avatars.githubusercontent.com/u/131409712?v=4"  width=115><br><sub>Juan Lima</sub>](https://github.com/GruveJL)

