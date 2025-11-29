# Projeto Billboard
1. Objetivo do Estudo

O estudo buscou responder se o consumo musical, refletido pelos rankings de popularidade e pelas características técnicas das músicas, apresentou mudanças entre três períodos:

Pré-pandemia

Durante a pandemia

Pós-pandemia

Para isso, combinamos dados da Billboard com informações obtidas pela API do Spotify, criando uma base integrada e rica em atributos musicais.

2. Estrutura do Repositório
/
├── base_final.xlsx         
├── tarbalho_musicas.ipynb        
├── v3_api_spotify.ipynb          
├── README.md                    
└── arquivos relacionados ao artigo submetido à revista

**Observação importante**

O notebook v3_api_spotify.ipynb é disponibilizado apenas como documentação do processo de coleta.
A análise completa pode ser reproduzida exclusivamente com:

tarbalho_musicas.ipynb

base_final.xlsx

Ou seja, você não precisa executar a API para reproduzir o estudo, pois toda a base já está pronta.

3. Metodologia

A metodologia foi pensada para permitir que qualquer pessoa, mesmo sem familiaridade inicial com o projeto, consiga reproduzir todo o processo.
Ela está dividida em etapas claras:

3.1 Coleta de Dados (Billboard)

Primeiro, coletamos os dados brutos contendo:

posição no ranking

título da música

artista(s)

datas de exibição nos charts

informações de contexto necessárias para identificar o período histórico

Esta etapa forneceu a estrutura inicial do estudo.

3.2 Complementação dos Dados (API Spotify)

Para enriquecer a base, utilizamos a API do Spotify a partir dos IDs das músicas. Foram coletadas características como:

tempo (BPM)

modo (maior/menor)

duração

data de lançamento

atributos técnicos das faixas (energy, danceability, valence etc.)

Limitações enfrentadas durante a coleta:

limite de requisições por minuto imposto pela API

necessidade de adicionar intervalos entre chamadas

falhas ocasionais e reenvio automático de requisições

O notebook da API inclui rotinas preparadas para lidar com esses cenários.

Importante:
A coleta foi feita durante o desenvolvimento do estudo, mas agora é apenas demonstrativa neste repositório.

3.3 Tratamento da Base

Após obter todos os dados:

colunas foram padronizadas

formatos incorretos foram corrigidos

datas foram normalizadas

duplicações e inconsistências foram tratadas

entradas incompletas foram analisadas e removidas quando necessário

classificamos cada música como pertencente aos períodos:

pré-pandemia

durante a pandemia

pós-pandemia

A base final entregue (base_final.xlsx) é o resultado deste processo.

3.4 Análises Realizadas

O notebook apresenta análises como:

evolução temporal das características musicais

comparação entre períodos

análise do comportamento dos rankings

distribuição de atributos musicais ao longo dos estágios da pandemia

visualizações e gráficos comparativos

Essa etapa culminou nos resultados utilizados no artigo aprovado para publicação.

4. Como Reproduzir o Estudo

A seguir, um passo a passo claro e objetivo para reproduzir a análise.

4.1 Pré-requisitos

Python 3.8 ou superior

pip instalado

Jupyter Notebook ou JupyterLab

(Opcional) Conta no Spotify for Developers — apenas se desejar testar a API

4.2 Clonar o Repositório
git clone https://github.com/seuusuario/seurepositorio.git
cd seurepositorio

4.5 Configurar Credenciais da API do Spotify (Opcional)

Somente necessário se você quiser executar o notebook de API.

Acesse https://developer.spotify.com

Crie um aplicativo

Obtenha:

client_id

client_secret

Preencha esses valores no trecho de autenticação do notebook da API

Se você deseja apenas reproduzir a análise, pode pular essa etapa.

4.6 Executar o Notebook Principal
jupyter notebook tarbalho_musicas.ipynb


As células seguem a ordem:

Importação de bibliotecas

Carregamento da base final

Tratamento e preparação

Análises estatísticas

Geração dos gráficos

Interpretação dos resultados

4.7 Reproduzindo Somente a Análise

Basta utilizar:

base_final.xlsx

tarbalho_musicas.ipynb

O notebook foi estruturado para funcionar integralmente sem a necessidade da API.

5. Considerações Finais

Este repositório foi organizado para garantir transparência total e reprodutibilidade do estudo.
Pesquisadores, estudantes e demais interessados podem:

entender todo o processo metodológico

replicar as análises

expandir o estudo para novos períodos ou bases

utilizar o código como referência acadêmica

Este trabalho deu origem a um artigo posteriormente aprovado e publicado em revista científica, contendo:

introdução

fundamentação teórica

metodologia

análise dos resultados

discussão

conclusão
