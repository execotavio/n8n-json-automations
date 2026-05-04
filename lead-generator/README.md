# Gerador de Leads Qualificados via LinkedIn (API Reverse Engineering)

Esta é uma das automações mais robustas do meu portfólio. Ela automatiza o processo de **prospecção ativa (outbound)**, extraindo dados de perfis e empresas diretamente do LinkedIn para alimentar pipelines de vendas ou recrutamento.

## 🚀 Visão Geral
O fluxo simula buscas avançadas no LinkedIn para identificar leads com base em critérios específicos (cargo, localização, setor). Ele não apenas coleta os dados, mas realiza uma **limpeza profunda e normalização dos dados via código (Node.js/JS)** antes de entregá-los prontos para uso.

## 🛠️ Tecnologias e Ferramentas
- **n8n**: Orquestração complexa de múltiplos passos.
- **HTTP Request (Advanced)**: Implementação de Headers customizados, cookies e parâmetros de consulta para simular requisições de busca.
- **Node.js/JavaScript**: Utilizado para tratar strings, limpar dados brutos e estruturar o JSON final.
- **Data Transformation**: Mapeamento de objetos complexos vindos da API para um formato legível por humanos.

## 🧠 Lógica de Automação e Diferenciais Técnicos
O que torna este fluxo especial do ponto de vista de engenharia:
1. **Manipulação de Headers e Cookies**: Demonstra conhecimento avançado em como APIs web funcionam, lidando com autenticação e persistência de sessão.
2. **Processamento de Dados Brutos**: O nó de **Code** limpa caracteres especiais, remove espaços desnecessários e valida se os campos essenciais (Nome, Empresa, Cargo) estão presentes.
3. **Escalabilidade**: Estruturado para lidar com listas de resultados, permitindo a extração de múltiplos leads em uma única execução.
4. **Resiliência**: Inclui lógica para evitar bloqueios, simulando o comportamento de navegação esperado.

## ⚙️ Configuração Prévia
Esta automação é de nível avançado e requer:
- **Cookies de Sessão**: É necessário extrair os headers de uma sessão ativa do LinkedIn para que o nó HTTP consiga realizar as buscas.
- **Configuração de Proxy (Opcional)**: Recomendado para grandes volumes de requisições.

## 🔗 Como utilizar
1. Importe o arquivo `Gerador_de_Leads_[Linkedin].json` no n8n.
2. No nó de **HTTP Request**, atualize os campos de `Header` com as suas credenciais de sessão (li_at, JSESSIONID, etc).
3. Ajuste os termos de busca no campo `Query`.
4. Execute e visualize os leads prontos no formato JSON ou envie diretamente para um Google Sheets/CRM.

---
*Nota: Este projeto foi criado exclusivamente para fins de estudo e demonstração de capacidades técnicas em integração de sistemas e manipulação de dados.*
