# Semana 7

### Requisitos Funcionais

- O sistema deve fornecer a funcionalidade de login com e-mail institucional
- O sistema deve prover aos usuários com permissão uma forma de gerenciar documentos (enviar novos/editar informações/remover documento) de acordo com suas permissões
- O sistema deve ter uma pesquisa que retorna documentos de acordo palavras-chave contidas no documento e filtros secundários
- O sistema deve disponibilizar todo documento retornado em pesquisa para download
- O sistema deve permitir que o usuário com o privilégio correto convide novos usuários pelos seus emails institucionais
- O sistema deve disparar um email para o usuário convidado
- O sistema deve fornecer um gerenciamento para os níveis de permissão dos usuários
- O sistema deve fornecer um gerenciamento do domínio de categorias de documentos e da hierarquia entre elas

### Requisitos Não-Funcionais

- Validação de login deve ser feita usando autenticação OAuth2 para acesso a API do Google
- O motor de busca por palavras-chave dos documentos será construindo usando a ferramenta ElasticSearch
- Multi-Tenant: O sistema deve ser construído de forma que sua estrutura de dados possa ser replicada para outro departamento na mesma instalação da aplicação
- Implementação do projeto no servidores da UNIRIO
- Pipeline CI/CD integrado ao GitHub do projeto

### Regras de Negócio

- Emails institucionais válidos para acesso ao sistema são apenas os que estiverem contidos no domínios "uniriotec.br" ou "edu.unirio.br"
- Em qualquer momento, ao menos um usuário deve ter permissão de alterar permissão de outros usuários
- Uma categoria só pode ser removida se nenhum documento estiver classificado nela
- Documentos inseridos podem estar formato .pdf, .doc ou .txt
- Cada documento inserido deve ter salvo:
    - nome, (obrigatório)
    - resumo, (opcional)
    - categoria, (opcional)
    - data de inserção, (ou data do documento ?)
    - usuário que inseriu (automático)
- Todo usuário deve poder excluir um documento enviado por ele próprio
- Além das palavras-chave, os seguintes filtros secundários deve restringir a pesquisa de documentos:
    - data,
    - categoria,
    - enviados por mim
- Devem existir níveis especiais de permissão para os usuários da seguinte forma:
    - Pesquisar atas (básico)
    - Inserir documentos
    - Editar documentos enviados por outros usuários
    - Excluir documentos enviados por outros usuários
    - Convidar novos usuários
    - Alterar permissões de todos os usuários
    - Editar a hierarquia e os nomes das categorias