# scraper_leads
Automação de Geração de Leads
Este é um projeto de automação que usa o n8n para encontrar e organizar leads (potenciais clientes) de negócios em qualquer lugar do mundo. Ele é capaz de buscar informações como nome, telefone, site e endereço, e ainda gera uma pontuação para ajudar a priorizar os melhores leads.

Funcionalidades
Busca de dados de negócios: Encontra empresas por tipo, cidade e país.

Pontuação de Leads: Calcula uma pontuação (Lead Score) que ajuda a identificar os negócios com maior necessidade de serviços digitais.

Armazenamento em Banco de Dados: Salva todos os dados organizados em uma planilha (Base) no Airtable.

Visualização de Dados: Permite a criação de painéis (dashboards) para visualizar e analisar os leads de forma intuitiva.

Ferramentas Utilizadas
n8n: Ferramenta de automação de fluxo de trabalho.

Airtable: Base de dados online para armazenar os leads.

RapidAPI: API de busca de negócios utilizada para encontrar os dados.

Nominatim (OpenStreetMap): API para geolocalização de cidades.

Como Usar
1. Configurar o Airtable
Primeiro, você precisa configurar a sua base de dados no Airtable.

Crie uma nova Base com o nome $ Make me money.

Dentro dela, crie uma Tabela com o nome $$$.

Configure as colunas da sua tabela $$$ com os nomes exatos e tipos de campo corretos:

Business Name (Texto)

Number (Texto)

Website (Texto)

Address (Texto)

City (Texto)

Category (Texto)

Rating (Número)

Reviews (Número)

Lead Score (Número)

Opportunities (Texto Longo)

Para facilitar a visualização, crie uma coluna chamada Criado em com o tipo de campo Created time.

2. Obter Chaves de API
Este fluxo precisa de duas chaves de API para funcionar:

Airtable: Crie um Personal Access Token com as permissões de leitura e escrita (data.records:read e data.records:write) e dê a ele acesso à sua Base $ Make me money.

RapidAPI: Obtenha uma chave de API para o serviço maps-data.p.rapidapi.com.

3. Importar e Configurar o Fluxo
Importe o fluxo SCRAPER DE LEADS.json para o seu n8n.

Abra o nó Create a record e adicione a credencial do Airtable que você criou.

Abra o nó de código Smart Lead Searcher e adicione sua chave de API da RapidAPI onde está insert your api key here.

4. Executar o Fluxo
Você pode rodar o fluxo usando o texto:

pet shop|rio de janeiro|br

O fluxo irá buscar os dados e preencher a sua tabela no Airtable.

Agradecimentos
Este projeto foi desenvolvido com a ajuda e a persistência de um usuário que superou diversos obstáculos para fazer esta automação funcionar.
