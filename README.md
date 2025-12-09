🎵 Projeto Billboard — Análise do Consumo Musical Antes, Durante e Depois da Pandemia

Este repositório reúne todos os arquivos, códigos e bases utilizados para investigar se — e como — o consumo musical mudou ao longo da pandemia.
A partir da integração entre rankings da Billboard e atributos técnicos fornecidos pela API do Spotify, analisamos padrões que possam refletir transformações sociais impostas pelo período.

📁 Estrutura do Repositório
/
├── base_final.xlsx                 # Base consolidada com todos os atributos musicais
├── v5_base_final.ipynb             # Notebook principal de análise
├── v3_api_spotify.ipynb            # Documentação do processo de coleta via API
├── README.md                       # Você está aqui :)
└── arquivos relacionados ao artigo submetido à revista


Observação importante
O notebook v3_api_spotify.ipynb está aqui apenas como documentação do processo de coleta.
Para reproduzir a análise completa, você precisa somente de:

v5_base_final.ipynb
base_final.xlsx

Ou seja, não é necessário realizar chamadas à API — a base já está pronta.

**🔍 1. Objetivo do Estudo**

O estudo buscou responder:
o comportamento musical mudou antes, durante e após a pandemia?

Para isso, analisamos três períodos:
Pré-pandemia
Pandemia
Pós-pandemia

Observando tanto sua presença nos rankings quanto múltiplos atributos musicais (valence, energy, danceability, BPM, modo tonal, duração etc.).

**⚙️ 2. Metodologia**

Toda a metodologia foi planejada para ser totalmente reprodutível, clara e documentada. Ela é dividida em quatro grandes etapas:

**2.1 Coleta de Dados — Billboard**

Inicialmente coletamos informações essenciais sobre cada música presente nos rankings, incluindo:
posição no chart

título
artista(s)
datas de aparição
período histórico correspondente

Essa etapa construiu a estrutura central do estudo.

**2.2 Complementação — API do Spotify**

Para enriquecer a análise, consultamos a API do Spotify a partir dos IDs das faixas. Foram coletadas características como:

BPM (tempo)
modo (maior/menor)
duração
data de lançamento
atributos técnicos (energy, valence, danceability, acousticness etc.)

Desafios enfrentados na coleta:

limite de requisições por minuto
necessidade de introduzir delays
erros intermitentes da API
rotina automatizada para reenvio de requisições
O notebook demonstra como todos esses problemas foram tratados.

**2.3 Tratamento da Base**

Com todos os dados reunidos:

padronizamos nomes e formatos
corrigimos inconsistências
normalizamos datas
removemos duplicatas
analisamos e tratamos entradas incompletas
classificamos cada música em pré/durante/pós-pandemia

📌 O resultado final é o arquivo base_final.xlsx.

**2.4 Análises Desenvolvidas**

O notebook principal traz visualizações e comparações, incluindo:

evolução temporal de atributos musicais
comparação entre períodos
comportamento dos rankings ao longo do tempo
distribuição de variáveis técnicas (valence, energy etc.)
gráficos e análises estatísticas
Os resultados apresentados originaram o artigo enviado e aprovado por revista científica.

**▶️ 3. Como Reproduzir o Estudo**
**3.1 Pré-requisitos**

**Python 3.8+**
**pip**
**Jupyter Notebook ou JupyterLab**
Conta no Spotify for Developers — apenas para testar o notebook de coleta

**3.2 Clonar o Repositório**
git clone https://github.com/seuusuario/seurepositorio.git
cd seurepositorio

**3.3 (Opcional) Configurar a API do Spotify**

Caso deseje reproduzir a coleta:

Acesse: https://developer.spotify.com
Crie um aplicativo
Obtenha seu client_id e client_secret
Insira no notebook v3_api_spotify.ipynb
Se o objetivo for somente analisar, pode ignorar esta etapa.

**3.4 Executar o Notebook Principal**
jupyter notebook v5_base-final.ipynb


A ordem lógica do notebook:

Importação das bibliotecas
Carregamento da base_final.xlsx
Tratamentos e verificações
Análises comparativas
Geração dos gráficos
Discussão dos resultados

**3.5 Reproduzir Apenas a Análise**

Use apenas:

base_final.xlsx
v5_base-final.ipynb
Sem necessidade de API.

**📝 4. Considerações Finais**

Este projeto foi estruturado para garantir transparência, clareza e total reprodutibilidade para pesquisadores e interessados.
Aqui, você pode:

compreender detalhadamente toda a metodologia
reproduzir os resultados
adaptar o estudo para outros períodos ou gêneros musicais
usar o código como referência acadêmica

O material deste repositório originou um artigo científico contendo:

introdução
fundamentação teórica
metodologia
resultados
discussão
conclusão


**🎓 Publicação e Reconhecimento**

Parte deste estudo — incluindo metodologia, análises e visualizações — foi submetida e aceita para apresentação em congresso, destacando a relevância científica e o rigor acadêmico do trabalho desenvolvido.


<img width="765" height="759" alt="image" src="https://github.com/user-attachments/assets/b09d0ffe-6725-48e1-be50-a7e018ad6634" />
