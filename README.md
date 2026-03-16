# Gerenciador de Tarefas (ToDo List)

Aplicação web desenvolvida com **Spring Boot** e **Thymeleaf** para gerenciamento de tarefas.

O sistema permite criar, editar, excluir tarefas, alternar seu status e filtrar tarefas por estado.

---

# Tecnologias

* Java 21
* Spring Boot 4.0.3
* Spring MVC
* Thymeleaf
* Maven
* Bean Validation (Jakarta Validation)

---

# Funcionalidades

* Criar novas tarefas
* Editar tarefas existentes
* Excluir tarefas
* Alternar status entre **Pendente** e **Concluída**
* Filtrar tarefas:

    * Todas
    * Pendentes
    * Concluídas
* Contador de tarefas exibindo:

    * Total de tarefas
    * Quantidade pendente
    * Quantidade concluída
* Validação de formulários
* Mensagens de sucesso e erro

---

# Pré-requisitos

Antes de executar o projeto, é necessário ter instalado:

* **Java 21**
* **Maven** (ou utilizar o Maven Wrapper incluído no projeto)

---

# Como Executar

### 1. Clonar o repositório

```
git clone https://github.com/seu-usuario/nome-do-repositorio.git
```

### 2. Entrar na pasta do projeto

```
cd nome-do-repositorio
```

### 3. Executar a aplicação

Usando o **Maven Wrapper**:

```
./mvnw spring-boot:run
```

Ou usando **Maven instalado**:

```
mvn spring-boot:run
```

---

# Acessar a aplicação

Após iniciar o projeto, abra o navegador em:

```
http://localhost:8080/tarefas
```

A aplicação será iniciada na porta **8080**.

---

# URLs Disponíveis

| URL                          | Método | Descrição                          |
| ---------------------------- | ------ | ---------------------------------- |
| `/tarefas`                   | GET    | Listar tarefas                     |
| `/tarefas?filtro=pendentes`  | GET    | Listar tarefas pendentes           |
| `/tarefas?filtro=concluidas` | GET    | Listar tarefas concluídas          |
| `/tarefas/novo`              | GET    | Formulário para nova tarefa        |
| `/tarefas/editar/{id}`       | GET    | Formulário para editar tarefa      |
| `/tarefas/salvar`            | POST   | Salvar tarefa (criar ou atualizar) |
| `/tarefas/excluir/{id}`      | POST   | Excluir tarefa                     |
| `/tarefas/status/{id}`       | GET    | Alternar status da tarefa          |

---

# Estrutura do Projeto

```
com.biopark.tarefas/
├── TarefasAppApplication.java
├── controller/
│   └── TarefaController.java
├── service/
│   └── TarefaService.java
├── repository/
│   └── TarefaRepository.java
└── model/
    └── Tarefa.java
```

---

# Observações

* As tarefas são armazenadas **em memória**, portanto são perdidas ao reiniciar a aplicação.
* O projeto foi desenvolvido com foco em **aprendizado de Spring Boot MVC e Thymeleaf**.
