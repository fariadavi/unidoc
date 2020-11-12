# Semana 2

## **Estudo sobre as ferramentas de busca em texto**

### Artigos e vídeos tutoriais

- Overview Solr - [https://lucene.apache.org/solr/guide/8_6/a-quick-overview.html](https://lucene.apache.org/solr/guide/8_6/a-quick-overview.html)
- [Elasticsearch Tutorial for Beginners | Learn the Elastic Stack Architecture | Frank Kane](https://youtu.be/C3tlMqaNSaI)
- [[Part 1/2] Run Your Own Search Engine With Apache Solr](https://youtu.be/83tEFh-z9Hs)

### Como fazer a busca por texto dentro dos documentos

- Tutorial ElasticSearch - [https://sematext.com/guides/elasticsearch/](https://sematext.com/guides/elasticsearch/)
- Tutorial Solr - [https://sematext.com/guides/solr/](https://sematext.com/guides/solr/)
- Comparativo - [https://sematext.com/blog/solr-vs-elasticsearch-differences/](https://sematext.com/blog/solr-vs-elasticsearch-differences/)
- Implementação ElasticSearch + Apache Tika [https://dontpaniclabs.com/blog/post/2020/03/03/searching-word-and-pdf-documents-with-elasticsearch-and-apache-tika/](https://dontpaniclabs.com/blog/post/2020/03/03/searching-word-and-pdf-documents-with-elasticsearch-and-apache-tika/)
- Implementação Solr (usando o Apache Tika que vem incluído) [https://lucene.apache.org/solr/guide/6_6/uploading-data-with-solr-cell-using-apache-tika.html](https://lucene.apache.org/solr/guide/6_6/uploading-data-with-solr-cell-using-apache-tika.html)

### Vantagens do uso das ferramentas:

- Foco do projeto não se torna replicar o desenvolvimento de uma ferramenta de busca em texto, leva o foco pra aplicação e suas funcionalidades
- Performance otimizada - o algoritmo usado nessas ferramentas super difundidas no mercado, muito provavelmente, seriam muito mais performáticos do que o que eu desenvolveria em alguns meses de projeto
- Contempla diversas melhorias que, em apenas alguns meses, o projeto não teria como por exemplo algoritmos de ranqueamento de resultados, exclusão/irrelevância de palavras conectores (a/as/os/the/there)...

### Conclusão

Me parece que o caminho é utilizar uma ferramenta especializada, independente de qual, para busca de texto nos documentos e focar em desenvolver uma aplicação abrangente com outras funcionalidades que sejam úteis para o departamento.

## **Ideia - Desenvolvimento em fases**

1. Busca de atas

- Implementação de um índice (Solr ou ElasticSearch) criado a partir de todos os documentos contidos na pasta X
- Front estilo google, tela limpa, 1 barra de busca que envia um request HTTP ao Solr/ElasticSearch e retorna uma lista dos documentos encontrados
- Sem banco, sem classes no domínio, os dados são só os documentos
- Sem backend, o processamento é só da ferramenta de busca

2. CRUD

- Possibidade de visualização no navegador e download da ata desejada
- Manipulação de documentos
- Implementação de um banco para guardar informações extras sobre documentos
- Implementação de um back-end com conexão ao banco para manipulação de dados do domínio (classe de documentos)

3. Expansão do sistema

- Criação de assembleias no domínio
- Trocar documentos por assembleias como classe forte do sistema

4. Personificação da interação com o sistema

- Multitenant
- Login com email institucional
- Criação de usuários e perfis de usuário

5. Sustentação e implementação de novas funcionalidades

- Novas funcionalidades (TBD)
    - Solicitações de correção em atas de assembleia
    - Notificações por email
    - Lista de presença

0. Infra

- Implementação do projeto no servidor da unirio
- Pipeline CI/CD integrado ao github do projeto
- Migração inicial para popular o sistema com todas as atas existentes hoje e criação de assembleia para cada uma (desde 199X)