# Como imagino o sistema

Como imagino o sistema:

1. Acesso pela web (ex.: http://unidoc.unirio.com)
2. Página retornada é uma landing page descrevendo o sistema
"UNIDOC é um repositório de documentos do departamento de informática aplicada da unirio, etc"
"pesquise documentos por palavra-chave"
botão "faça login para continuar" que faz autenticação com email unirio escolhido
footer "UNIDOC é um sistema de código aberto", link pro github
3. Se após o login o usuário não tiver permissão de acesso (permissão mínima de consulta), um aviso é exibido e ele é redirecionado para a página deslogada
4. Entrando no sistema, temos uma tela simples com um campo de busca de palavras-chave e alguns campos de filtros adicionais
informação sobre o tenant atual, com opção para mudar, caso o usuário faça parte de mais de um
em algum lugar na tela um botão para cadastro de um novo documento, visível apenas para os usuários com essa permissão
em algum lugar na tela um botão para a tela de gerencia de usuários, visível apenas para os usuários com essa permissão
em algum lugar na tela um botão para a tela de gerenciamento das categorias, visível apenas para os usuários com essa permissão
uma barra superior com opções para logout
    1. Ao clicar em cadastrar um novo documento, uma tela com os campos nome, resumo, data, categoria e uma seção para upload de arquivo são exibidos
    Ao clicar em salvar o arquivo é salvo e suas informações persistidas na base
    2. Ao pesquisar um documento são exibidos em lista abaixo da barra de busca os dados dos documentos que cumprem todos os filtros
    Cada item da lista têm um icone de download, um ícone para edição e um ícone para deleção
        1. Ao clicar em download, o arquivo é baixado para a máquina do usuário
        2. Ao clicar em editar, a tela de cadastro é exibida com os valores preenchidos para edição e ao salvar, os dados do registro são atualizados
        3. Ao clicar em deletar o documento e seus dados são removidos da base
    3. Ao clicar no botão de gerenciar usuários, uma tela com uma tabela de emails x permissões
    A tabela deve poder ser filtrada com uma barra de busca que filtra as linhas exibidas pelo email
    As células da tabela devem ser apenas checkboxes indicando a permissão ativada ou não
    4. Ao clicar no botão de gerenciar categorias, uma tela com a hierarquia das categorias em forma de árvore-lista é exibida
    Cada categoria deve ter um contador com o número de itens classificados nela ou em suas subcategorias
    Os nomes devem ser editáveis nessa tela (lápis)
    Apenas as categorias com contador 0 devem ter a opção habilitada para serem deletadas (lixeira)
    Ao clicar no nome de uma das categorias podemos redirecionar para a tela de busca com a categoria seleciona (talvez confirmar antes?)
    5. Ao mudar o tenant a pesquisa a seguir será feita no outro tenant
    Se uma pesquisa já estiver sendo exibida, os resultado devem ser limpados
    6. Ao clicar em logout o usuário sai do sistema