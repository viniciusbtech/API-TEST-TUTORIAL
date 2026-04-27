# API-TEST-TUTORIAL
This is a test repository to give an example of communication with a server.

## 1. O que é comunicação com servidor
Comunicação com servidor é quando o aplicativo envia ou busca dados em um sistema externo, normalmente por meio de uma API.

Funcionamento no Focus
O usuário cria uma tarefa no aplicativo.
O app envia essa tarefa para o servidor.
O servidor salva os dados.
Depois, quando o usuário abrir o app em outro celular, o app pode buscar essas tarefas novamente pela API.

## 2. Mostrar o fluxo básico

Usuário
  ↓
Tela Flutter
  ↓
Provider / Camada de Aplicação
  ↓
Serviço de API
  ↓
Servidor / Back-end
  ↓
Banco de Dados remoto


A tela não deve chamar o servidor diretamente de forma desorganizada. O ideal é criar uma classe de serviço responsável por fazer as requisições HTTP.


## 3. Explicar as operações principais

| Operação        | Método HTTP | Para que serve                          |
| --------------- | ----------- | --------------------------------------- |
| Buscar dados    | GET         | Buscar tarefas, usuários ou disciplinas |
| Enviar dados    | POST        | Criar uma nova tarefa                   |
| Atualizar dados | PUT/PATCH   | Editar uma tarefa existente             |
| Remover dados   | DELETE      | Excluir uma tarefa                      |


## 4. Preparando o projeto

Para fazer requisições HTTP no Flutter, podemos usar o pacote `http`.

No arquivo `pubspec.yaml`, adicione:

```yaml
dependencies:
  http: ^1.2.0

Depois rode o comando:
flutter pub get