# Gerador de Posts Virais para LinkedIn com IA

Esta automação foi desenvolvida para transformar ideias brutas ou rascunhos de textos em posts otimizados para o LinkedIn, utilizando técnicas de escrita persuasiva (Copywriting) e Inteligência Artificial.

## 🚀 Visão Geral
O fluxo recebe um tema ou conteúdo inicial, processa as informações através da API da OpenAI (GPT-4) e aplica um "Framework de Viralização". O resultado é um post estruturado com gatilhos de atenção, formatação adequada para a rede e call-to-action (CTA) eficiente.

## 🛠️ Tecnologias e Ferramentas
- **n8n**: Orquestrador do fluxo.
- **OpenAI (GPT-4o)**: Motor de IA para reescrita e análise de tom de voz.
- **Sticky Notes & No-Ops Nodes**: Organização visual e documentação interna do workflow.
- **HTTP Request / OpenAI Node**: Integração direta com modelos de linguagem avançados.

## 🧠 Lógica de Automação
O diferencial deste workflow é o **System Prompt** estruturado:
1. **Entrada de Conteúdo**: O fluxo captura a ideia base que o usuário deseja transformar.
2. **Engenharia de Prompt (Prompt Engineering)**: 
    - A IA é instruída a assumir o papel de um especialista em Growth e LinkedIn.
    - É aplicado um framework de estruturação: *Hook* (Gancho impactante), *Body* (Corpo com espaçamento para leitura escaneável) e *CTA* (Chamada para ação).
    - O modelo garante que o texto não pareça "robotizado", focando em autenticidade.
3. **Saída Formatada**: O post é entregue pronto para publicação, respeitando as boas práticas de algoritmo (tempo de permanência e engajamento).

## ⚙️ Configuração Prévia
Para rodar este fluxo, são necessárias as seguintes credenciais:
- **OpenAI API Key**: Com acesso aos modelos GPT-4 ou GPT-4o.

## 🔗 Como importar
1. Copie o conteúdo do arquivo `Linkedin_Virals.json`.
2. No seu n8n, clique em **Import from File** ou cole o JSON diretamente no editor.
3. Certifique-se de configurar a sua conta da OpenAI no nó correspondente.
