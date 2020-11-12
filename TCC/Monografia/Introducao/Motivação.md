# Motivação

Documentos servem um propósito de registrar assuntos discutidos. A boa organização dos documentos facilitam imensamente diversos trabalhos, bem como serve para informar eventos ocorridos em épocas passadas.

(Mencionar exemplos: milhares de documentos devidamente armazenados e categorizados numa pasta do drive não são úteis quando tudo que temos para busca de uma informação é uma informação de palavra-chave que está no corpo do documento...)

A recuperação de documentos é tão importante quanto a produção e armazenamento bem feitos dos mesmos e nisso se desenvolve o estudo sobre Information Retrieval. IR é o campo de estudo para obtenção da informação mais relevante possível desejada pelo usuário com o uso de filtros e palavras-chave. Com isso conseguimos transformar o trabalho de recuperar informação de algo custoso e manual para algo trivial, reduzindo o custo de tempo de horas para segundos.

(Fazer a ponte para o cenário que se encontra o estado do arquivamento dos documentos do departamento de informática: Mencionar que sempre houve processos e protocolos cumpridos corretamente de forma que existem mais de 20 anos de atas devidamente armazenadas, porém que da forma que existem hoje, são subutilizadas pois quando é necessário recuperar alguma informação histórica, obter o documento desejado é um processo custoso)

Em conversa com o Prof. Pedro, ele, em sua capacidade de Chefe do Departamento de Informática Aplicada, compartilhou que havia identificado uma necessidade de buscar por assuntos ou tópicos no conjunto histórico de atas do departamento e que nenhuma ferramenta cumpria essa carência. A UNIRIO como um todo não tem um sistema de gerenciamento de documentos.

---

### MOTIVAÇÃO TCC NATÁLIA

De acordo com o Suplemento de Tecnologias de Informação e Comunicação da Pesquisa Nacional por Amostra de Domicílios (Pnad) 2014 [1] divulgado pelo Instituto Brasileiro de Geografia e Estatística (IBGE), o uso do telefone celular para acessar a internet ultrapassou o uso do computador no Brasil. Com essa mudança no hábito dos brasileiros, a adaptação dos principais sites para o modo adequado para telas menores passou a ser prioridade.

Hoje em dia, o Portal BSI não possui essa adaptação. Apesar do seu tamanho se ajustar à tela, os itens acabam sendo muito pequenos e a usabilidade é prejudicada. Acreditamos que, para melhorar a visibilidade do curso, a adequação do nosso portal de forma que todos os usuários tenham uma boa experiência é essencial.

---

### MOTIVAÇÃO TCC HUGO

No mundo atual, as novas tecnologias surgem com uma frequência cada vez maior. No âmbito da programação, esta dinâmica não é diferente. O surgimento das novas tecnologias para desenvolvimento de aplicações Web faz com que muitas tecnologias fiquem ultrapassadas e menos relevantes em um espaço de tempo muito pequeno se considerarmos tecnologias de desenvolvimento de software anteriores.

Manter-se atualizado não é apenas relevante para a indústria se manter nas novidades, mas para desenvolver soluções que tecnologias passadas não eram capazes de resolver. O desenvolvimento da tecnologia se dá justamente para resolver tais problemas que naquele momento não se via uma solução com as tecnologias existentes.

Neste sentido, este documento apresenta um projeto que está utilizando tecnologias modernas para viabilizar uma nova forma de desenvolver aplicações Web: programação na nuvem, com aplicações conteinerizadas e em ambientes isolados usando Node.js. Este projeto será utilizado como um exemplo para apresentar e discutir as tecnologias nas quais ele se apoia.

O Node.js (Nodejs, 2020) vem ganhando cada vez mais relevância e importância por simplificar o desenvolvimento backend usando JavaScript. O mercado começou a usá-lo para criar aplicações Web de forma rápida e escalável. Dito isto, no curso de BSI da Unirio não chegamos a nos aprofundar na linguagem JavaScript, de grande relevância para o mercado atual. Assim, vimos a possibilidade de abordar o tema neste projeto de conclusão de Graduação e informações a respeito das vantagens do Node.js.

O exemplo em estudo se trata de uma aplicação responsável por gerar taxas de financiamento na qual anteriormente utilizava-se de planilhas Excel e um sistema em tecnologias legadas que não podemos descrever por conta de confidencialidade. O meu papel nessa equipe era atuar como desenvolvedor, auxiliando também na definição dos requisitos por estar trabalhando com o sistema a mais tempo e com isso apoiar em decisões técnicas.

O novo sistema foi estruturado em microsserviços dockerizados, isto é, com cada microsserviço responsável por uma parte da aplicação, como a interface, conexão com o banco de dados, serviço de login, entre outras. O projeto utilizou o OpenShift11, ferramenta desenvolvida pela Red Hat, baseada no Kubernetes22 , para orquestrar os contêineres onde rodam os microsserviços, gerenciar a rede, o armazenamento, a distribuição de carga, roteamento, monitoramento, segurança e escalabilidade.

Com isso, vimos também a possibilidade de abordar temas como metodologias de desenvolvimento, tecnologias que o mercado vem utilizando na infraestrutura (como banco de dados), estruturação dos microsserviços, além da implantação contínua, que hoje em dia é um dos tópicos mais relevantes para aplicações Web, seguindo a linha de DevSecOps (desenvolvimento, segurança e operações), pensando no desenvolvimento conectado com a operação, garantindo que os dados e a aplicação estejam menos suscetíveis a falhas de segurança e visando a aplicação bem estruturada, segura e que atenda às necessidades do cliente.

Com esse projeto usando tecnologias como Docker (Docker Documentation, 2020), OpenShift1 , Node.JS (Nodejs, 2020), achamos que seria uma oportunidade de descrever a experiência de como é desenvolver utilizando essas tecnologias, e explicar mais e mais sobre como elas funcionam.

O projeto surgiu como uma forma de automatizar um processo de atualização que demorava três dias por pessoa para conseguir realizar o processo para um país. O sistema contava com mais de 32 países, o que gerava muito atraso e muita suscetibilidade a erro. No novo projeto em questão, para realizar o processo para um país são necessários alguns cliques e em 30 minutos o país teria suas novas taxas de financiamento prontas para aplicar nos produtos ofertados através do sistema.

As tecnologias utilizadas foram escolhidas por agilizarem o desenvolvimento e facilitarem a manutenção do software no futuro, trazendo uma grande melhoria nos tempos de implantação, correção de bugs e na escalabilidade da aplicação.