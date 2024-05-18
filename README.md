## Atividade Prática: Gerenciamento de Tarefas com Manipulação de Dados em Memória

- Contexto
  - Você precisa criar uma aplicação web simples para gerenciar uma lista de tarefas. Esta aplicação permitirá que os usuários adicionem, visualizem, atualizem e excluam tarefas. O gerenciamento das tarefas será feito em memória e não persistirá após o desligamento do servidor.


- Criar um servlet chamado TaskServlet que suporte os seguintes métodos HTTP:
  - GET: Para listar todas as tarefas.
  - POST: Para adicionar uma nova tarefa.
  - PUT: Para atualizar uma tarefa existente.
  - DELETE: Para remover uma tarefa.


- Armazenamento em Memória: 
  - Utilize uma estrutura de dados adequada (por exemplo, uma List<String>) para
     armazenar as tarefas em memória.


- Métodos HTTP e suas Funcionalidades:
  - GET /tasks:
    - Retorne todas as tarefas na lista. 
    - Se não houver tarefas, retorne uma mensagem indicando que não há tarefas disponíveis. 
  - POST /tasks: 
    - Adicione uma nova tarefa à lista.
    - A tarefa deve ser enviada como um parâmetro chamado task.
  - PUT /tasks:
    - Atualize uma tarefa existente na lista.
    - A requisição deve conter os parâmetros index (índice da tarefa na lista, começando em 1) e task (novo valor da tarefa).
    - Se o índice estiver fora do intervalo ou não for válido, retorne uma mensagem de erro apropriada.
  - DELETE /tasks:
    - Remova uma tarefa da lista.
    - A requisição deve conter o parâmetro index (índice da tarefa na lista, começando em 1).
    - Se o índice estiver fora do intervalo ou não for válido, retorne uma mensagem de erro apropriada.


- Dicas
  - Certifique-se de que os parâmetros recebidos nas requisições são válidos antes de realizar qualquer operação.
  - Utilize try-catch para tratar exceções e retornar mensagens de erro apropriadas.
  - Teste exaustivamente cada método HTTP para garantir que todas as funcionalidades estão implementadas corretamente.