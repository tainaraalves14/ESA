
---

# **Diagrama de Casos de Uso (Use Case Diagram)**

## **1. Conceito**

* Representa o **comportamento do sistema**.
* Ajuda a **definir requisitos funcionais** (o que o sistema deve fazer) dentro de um **domínio específico**.
* Mostra **quem interage** com o sistema e quais funcionalidades estão disponíveis.

**Exemplo:**

* **Domínio:** Hospitalar / Saúde
* **Caso de Uso:** Cadastro de Pacientes
* **Ator:** Administrador ou Recepcionista

---

## **2. Elementos Principais**

### **Ator**

* Quem utiliza o sistema (usuário ou outro sistema).
* Exemplo:

  * Hospital: **Gerente, Administrador, Médico**
  * E-commerce: **Cliente**
  * Sistema acadêmico: **Aluno**

### **Caso de Uso**

* Funcionalidade que o ator realiza no sistema.
* Exemplo:

  * Autenticação do Connect (Aluno)
  * Visualização de notas
  * Solicitação de provas

### **Aresta**

* Linha que conecta ator e caso de uso.
* Representa **interação ou dependência**.

### **Estereótipo**

* Adiciona **significado especial** a um relacionamento sem alterar a estrutura:

  * `<<include>>` → Caso obrigatório sempre executado pelo principal.

    * Ex.: `Sacar Dinheiro` <<include>> `Checar Senha`
  * `<<extend>>` → Caso opcional que pode ocorrer.

    * Ex.: `Abrir Conta Corrente` <<extend>> `Realizar Primeiro Depósito`

---

## **3. User Stories**

* Texto bruto com **o que o cliente quer**.
* Devem ser **analisadas e filtradas** para transformar em casos de uso.
* Exemplo:

  * “Como aluno, quero ver minhas notas e solicitar provas.” → Transforma-se em **casos de uso** no sistema acadêmico.

---

## **4. Exemplo Prático (Sistema Acadêmico)**

| Ator          | Caso de Uso             |
| ------------- | ----------------------- |
| Aluno         | Autenticação do Connect |
| Aluno         | Visualizar Notas        |
| Aluno         | Solicitar Provas        |
| Professor     | Lançar Notas            |
| Administrador | Gerenciar Usuários      |

---

## **5. Fluxo Visual (Diagrama Conceitual Textual)**

```
          +-----------------+
          |      Aluno      |
          +--------+--------+
                   |
   ---------------------------------
   |          |            |       |
   v          v            v       v
Autenticação  Visualizar  Solicitar  Consultar
  Connect       Notas     Provas    Horários

Include / Extend:
-----------------
Autenticação <<include>> Checar Credenciais
Solicitar Provas <<extend>> Enviar Notificação
```
