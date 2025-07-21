### Aula: Trabalhando com Git e Pull Requests - Fluxo de Trabalho, Branches e Colaboração

---

### **1. Introdução ao Fluxo de Trabalho no GitHub**

O GitHub é uma plataforma essencial para desenvolvedores colaborarem em projetos, principalmente em código aberto. Para entender como a colaboração acontece, é importante compreender conceitos como **Fork**, **Pull Request (PR)** e **Branches**. Vamos explorar todos esses conceitos e como você pode usá-los no seu fluxo de trabalho de desenvolvimento.

---

### **2. O que é um Pull Request (PR)?**

Quando você faz um **fork** de um repositório no GitHub, está criando uma cópia independente daquele projeto em seu perfil pessoal. Isso permite que você faça alterações no projeto sem afetar o repositório original.

#### **Definição de Pull Request:**

Um **Pull Request** é uma solicitação feita para que o repositório original "puxe" as mudanças feitas no seu **fork**. Ele permite que você proponha alterações ao código original, e os mantenedores do repositório podem revisar essas alterações antes de aceitá-las ou rejeitá-las.

Quando um Pull Request é enviado, os mantenedores podem:

* **Visualizar** as alterações propostas.
* **Comentar** em trechos específicos do código.
* **Solicitar melhorias** ou mudanças.
* **Aceitar** (fazer o merge) ou **rejeitar** o PR.

#### **Exemplo Prático:**

Imagine que você encontrou um bug no projeto de um repositório que você segue no GitHub. Você faz um **fork** do repositório, corrige o erro no seu fork e cria um PR para sugerir a correção aos mantenedores do repositório original.

---

### **3. Como Criar um Pull Request (PR)?**

Aqui está o passo a passo para criar um PR:

#### Passo 1: Faça o Fork e Clone do Repositório

1. **Fork** o repositório que você quer contribuir.
2. No terminal, **clone** o repositório para o seu computador:

   ```bash
   git clone https://github.com/usuario/rep-forkado.git
   cd rep-forkado
   ```

#### Passo 2: Crie suas Alterações

Agora, você pode editar, adicionar ou remover arquivos no seu repositório local como necessário.

#### Passo 3: Faça Commit das Alterações

Após realizar as modificações, faça o **commit** das alterações:

```bash
git add .
git commit -m "Descrição clara da mudança"
```

#### Passo 4: Envie para o GitHub

Envie as mudanças para o seu repositório no GitHub:

```bash
git push origin
```

#### Passo 5: Crie o Pull Request

1. Acesse a página do seu **fork** no GitHub.
2. Clique no botão **“Compare & pull request”**.
3. Na tela seguinte, revise as alterações e escreva um título e descrição claros sobre o que você fez e por que.
4. Clique em **"Create pull request"**.

---

### **4. O que são Branches no Git?**

#### **Definição de Branch:**

Um **branch** (ramo) no Git é uma linha de desenvolvimento independente dentro do seu projeto. Imagine que o **main** (ou **master**) é a versão estável do seu projeto. Com branches, você pode desenvolver novas funcionalidades, corrigir erros ou testar novas ideias sem interferir no código principal.

#### **Exemplo de Fluxo com Branches:**

Suponha que o repositório tem uma linha do tempo de commits assim:

```plaintext
main:               A---B---C
  	                       		\
nova-funcionalidade:       	  D---E
```

* **Commits A, B, C** são na branch **main**.
* **Commits D e E** estão sendo feitos na branch **nova-funcionalidade**, que foi criada a partir do commit C.

Isso permite que o desenvolvimento da nova funcionalidade ocorra de forma isolada, sem impactar a branch principal.

---

### **5. Por Que Usamos Branches?**

Imagine que várias pessoas estão trabalhando em um projeto:

* Uma pessoa está desenvolvendo uma **nova funcionalidade**.
* Outra está **corrigindo um bug**.
* Outra está **atualizando a documentação**.

Se todos trabalharem diretamente na branch **main**, isso pode gerar **conflitos de código** e dificultar a organização. Usando branches, cada pessoa pode trabalhar em sua própria linha do tempo, sem afetar as demais.

#### **Exemplo Prático:**

1. **Desenvolvedor A** cria uma branch para corrigir um bug no sistema de login.
2. **Desenvolvedor B** cria uma branch para implementar uma nova funcionalidade de carrinho de compras.
3. Quando as mudanças são concluídas e testadas, elas podem ser **mescladas** de volta para a branch **main**.

---

### **6. Dicas de Nomeação de Branches**

Nomes de branches devem ser claros e descritivos para facilitar a identificação do que está sendo feito nela. Evite nomes genéricos como "teste" ou "branch1". Exemplos de boas práticas:

* `feature/carrinho-compras` — para uma nova funcionalidade.
* `bugfix/corrigir-botao-login` — para correções de bugs.
* `hotfix/corrigir-erro-envio-email` — para correções emergenciais.

---

### **7. Trabalhando com Branches no Git**

Agora que você sabe o que são branches, vamos aprender como manipulá-las no Git.

#### **7.1 Visualizando as Branches Existentes**

Para ver todas as branches do repositório, use:

```bash
git branch
```

Exemplo de saída:

```plaintext
main
* nova-funcionalidade
```

O asterisco (\*) indica qual branch está ativa no momento (no caso, **nova-funcionalidade**).

#### **7.2 Criando uma Nova Branch**

Para criar uma nova branch, use o comando:

```bash
git branch nome-da-branch
```

Exemplo prático:

```bash
git branch nova-funcionalidade
```

Isso cria a branch, mas não a ativa.

#### **7.3 Alternando Entre Branches**

Para alternar para a branch criada, use:

```bash
git checkout nome-da-branch
```

Exemplo:

```bash
git checkout nova-funcionalidade
```

Agora, qualquer modificação será registrada na branch **nova-funcionalidade**.

#### **7.4 Criando e Alternando com Um Só Comando**

Você pode criar e alternar para uma nova branch em um único comando:

```bash
git checkout -b nova-funcionalidade
```

Esse comando cria a branch **nova-funcionalidade** e a ativa automaticamente.

---

### **8. Conclusão**

Neste módulo, vimos como utilizar **forks**, **pull requests**, e **branches** para gerenciar e colaborar em projetos no Git. Esses são conceitos essenciais para qualquer desenvolvedor que trabalha com código aberto ou em equipes de desenvolvimento.

Lembre-se:

* **Fork**: Cria uma cópia de um repositório para que você possa trabalhar de forma independente.
* **Pull Request (PR)**: Solicita que suas alterações sejam integradas ao repositório original.
* **Branch**: Permite trabalhar de forma isolada em diferentes partes do código, sem afetar a versão principal.

Esses processos ajudam a organizar o fluxo de trabalho e a manter o código limpo e organizado, especialmente em projetos colaborativos.

---

