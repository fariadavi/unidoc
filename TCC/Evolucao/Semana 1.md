# Semana 1

### **Pensar um pouco mais em modelagem/implementação**

- **Information Retrieval**
    - [https://nlp.stanford.edu/IR-book/](https://nlp.stanford.edu/IR-book/)
    - [https://www.youtube.com/watch?v=78nJvQytiYE](https://www.youtube.com/watch?v=78nJvQytiYE)
    - [http://aakashjapi.com/fuckin-search-engines-how-do-they-work/](http://aakashjapi.com/fuckin-search-engines-how-do-they-work/)
    - [https://github.com/logicx24/Text-Search-Engine](https://github.com/logicx24/Text-Search-Engine)

### **Pensar em ideias para expandir o sistema**

- **Expandir o sistema para além do cadastro e consulta de atas, centralizando todas as interações que revolvem as assembléias (interações que hoje ocorrem por email e em outros tempos ocorriam presencialmente). Exemplos de possibilidades de funcionalidades:**
    - Marcação de assembléia (integrado com o google calendar ?)
    - Lista dos convidados / Lista de presença
    - Notificar aos envolvidos em uma assembleia que uma ata dela foi subida no sistema
    - Download da ata pelo sistema
    - Solicitações de correção em partes do texto pelos envolvidos
    - OK de cada envolvido na ata pelo sistema (em tempos de reuniões virtuais, substituiria a necessidade da rúbrica)
    - Link para vídeo da assembleia, caso tenha sido gravada e enviada
    - Notificar os envolvidos por email quando nova versão da ata for enviada para que dêem seu OK ou solicitem outras revisões
    - Assim poderíamos ter um sistema que auxiliaria nas responsabilidades de:
        - Notificar os envolvidos em assembleias
        - Manter histórico das assembleias, quem era esperado a comparecer, quem esteve presente, quem solicitou revisão, o que foi revisto de cada versão da ata, quem solicitou, etc
        - Contribui para uma maior transparência (não sei se isso é bom ou ruim)

### **Diagramas de classes**

- **Classes:**
    - Documentos
    - Usuário ??

### **Diagramas de processos de negócios**

- **Cadastrar ata**
    - Fazer login -> Cadastrar Ata
- **Buscar ata por texto**
    - Fazer login -> Buscar Ata

### **Diagrama de atividades**

- **Início -> Usuário busca por palavra -> índice possui algum documento com a palavra desejada? ->**
    - Sim -> Retorna os documentos em que a palavra aparece
    - Não -> Retorna mensagem de que não existem resultados
- **Início -> Usuário cadastra nova ata -> Parse do documento enviado -> Envio do texto obtido para o índice -> Retorna mensagem de sucesso para o usuário**