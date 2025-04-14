# AzureCognitiveSearch_DECOLATECH2025

Este readme descreve como configurar uma pesquisa usando o Azure AI Search. O processo envolve a criação de recursos do Azure, a extração de dados de uma fonte de dados, o enriquecimento de dados com habilidades de IA, o uso do indexador do Azure no portal do Azure, a consulta do índice de pesquisa e a revisão dos resultados salvos em um Armazenamento de Conhecimento.

Os recursos do Azure necessários incluem um recurso do Azure AI Search, um recurso do Azure AI services e uma conta de armazenamento com contêineres de blobs. O readme orienta o usuário na criação desses recursos e na configuração deles com configurações específicas. Ele também explica como carregar documentos no Armazenamento do Azure, indexar os documentos usando o assistente de importação de dados e consultar o índice usando o Explorador de pesquisa. Finalmente, ele demonstra como revisar os dados enriquecidos no armazenamento de conhecimento, incluindo projeções e tabelas.

## Passo a passo simples para configurar uma pesquisa

Este guia oferece um resumo simplificado dos passos para configurar o projeto de pesquisa baseado no artigo do Azure AI Search.

**Pré-requisitos:**

* Uma assinatura ativa do Azure.

**Passos:**

1.  **Criar Recursos no Azure:**
    * Crie um novo recurso do **Azure AI Search**. Anote o nome e a chave de administrador.
    * Crie um novo recurso do **Azure AI services** (Cognitive Services). Anote a chave e o endpoint.
    * Crie uma conta de **Armazenamento do Azure** com um contêiner de blobs.

2.  **Carregar Dados:**
    * Faça o upload dos seus arquivos de dados (por exemplo, documentos `.pdf`, `.txt`) para o contêiner de blobs criado.

3.  **Conectar Fonte de Dados ao Azure AI Search:**
    * No portal do Azure, navegue até o seu recurso do Azure AI Search.
    * Clique em "Importar dados" no painel esquerdo.
    * Selecione "Azure Blob Storage" como a fonte de dados.
    * Configure a conexão com sua conta de armazenamento e selecione o contêiner de blobs.

5.  **Configurar o Indexador:**
    * Defina um **Indexer** para automatizar o processo de leitura da fonte de dados, aplicar o Skillset (se configurado) e criar o índice de pesquisa.
    * Configure a frequência de execução do indexador (por exemplo, uma vez ou agendada).

6.  **Criar o Índice de Pesquisa:**
    * Defina o esquema do seu índice, especificando os campos que serão pesquisáveis, filtráveis, etc.
    * O assistente de importação de dados pode ajudar a criar um esquema inicial baseado nos seus dados. **Certifique-se de ter um campo chave único (como um ID) para cada documento.** Se estiver usando `metadata_storage_path` do Blob Storage como chave, siga as instruções para aplicar a função `base64Encode` no `fieldMappings` do indexador (como explicado anteriormente).

7.  **Executar o Indexador:**
    * Inicie o indexador para que ele processe seus dados e crie o índice de pesquisa.

8.  **Consultar o Índice:**
    * Use o **Search explorer** no portal do Azure para testar suas consultas de pesquisa.
    * Experimente diferentes termos de pesquisa, filtros e facetas.


## Possibilidades de ferramentas que se beneficiam com esse tipo de ferramenta

* **Pesquisa de e-commerce:** O Azure AI Search pode ser usado para ajudar os clientes a encontrar os produtos que estão procurando. Ele também pode ser usado para recomendar produtos aos clientes com base em seus interesses e histórico de compras.
* **Atendimento ao cliente:** O Azure AI Search pode ser usado para ajudar os agentes de atendimento ao cliente a responder às perguntas dos clientes mais rapidamente. Ele também pode ser usado para fornecer aos clientes informações sobre produtos e serviços.
* **Análise de dados:** O Azure AI Search pode ser usado para analisar grandes volumes de dados para identificar tendências e insights. Ele também pode ser usado para criar painéis e relatórios que podem ajudar as empresas a tomar melhores decisões.

## Aprendizados adquiridos durante o processo

* Aprendi como criar e configurar recursos do Azure.
* Aprendi como extrair dados de uma fonte de dados.
* Aprendi como enriquecer dados com habilidades de IA.
* Aprendi como usar o indexador do Azure no portal do Azure.
* Aprendi como consultar o índice de pesquisa.
* Aprendi como revisar os resultados salvos em um Armazenamento de Conhecimento.
