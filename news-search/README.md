# Buscador de Notícias com Curadoria de IA (OpenAI)

Este fluxo automatiza o processo de monitoramento de notícias específicas, realizando a busca, filtragem por data, extração de conteúdo e uma análise inteligente utilizando Inteligência Artificial para resumir os pontos mais relevantes.

## 🚀 Visão Geral
A automação varre a web em busca de notícias baseadas em um termo de pesquisa, filtra apenas os resultados do dia atual, extrai o conteúdo textual de cada link e utiliza a API da OpenAI para gerar um resumo executivo de cada matéria.

## 🛠️ Tecnologias e Ferramentas
- **n8n**: Orquestrador do fluxo.
- **NewsAPI**: Fonte primária de busca de notícias.
- **OpenAI (GPT-4)**: Inteligência Artificial para análise e sumarização.
- **HTML Extract**: Extração de conteúdo útil de páginas web (Web Scraping).
- **HTTP Request**: Integração com APIs externas.

## 🧠 Lógica de Automação
O fluxo foi estruturado para ser eficiente e evitar processamento desnecessário:
1. **Trigger Manual**: Início do fluxo com definição do termo de busca (Ex: "Google").
2. **Fetch de Notícias**: Chamada à API para coletar os artigos mais recentes.
3. **Filtro Temporal (Data)**: Um nó de código (IF) compara a data da notícia com a data atual (`$now`), garantindo que apenas notícias de hoje sejam processadas.
4. **Iteração (Batches)**: As notícias são processadas em lotes para respeitar limites de taxa (rate limits) de APIs.
5. **Web Scraping**: O fluxo acessa a URL da notícia e extrai o texto principal.
6. **IA Curation**: A OpenAI processa o texto bruto e gera um resumo conciso.

## ⚙️ Configuração Prévia
Para rodar este fluxo, são necessárias as seguintes credenciais:
- **NewsAPI Key**: Obtida em [newsapi.org](https://newsapi.org/).
- **OpenAI API Key**: Configurada no nó da OpenAI.

## 🔗 Como importar
1. Copie o conteúdo do arquivo `Buscador_de_noticias.json`.
2. No seu n8n, clique em **Add Workflow** > **Import from File** ou simplesmente cole no canvas.
3. Configure as suas credenciais nos nós correspondentes.
