# Documentação de Git e GitHub

## Introdução

**Git** é um sistema de controle de versão distribuído, utilizado para rastrear alterações no código e colaborar em projetos de desenvolvimento. Ele permite que desenvolvedores trabalhem em diferentes partes de um projeto de forma simultânea e sem conflitos.  
**GitHub** é uma plataforma de hospedagem de código que usa o Git como base. Ele facilita o armazenamento, compartilhamento e colaboração em repositórios de código com desenvolvedores do mundo inteiro.

## Configuração Inicial do Git

Antes de começar a usar o Git, é necessário configurá-lo com suas informações de usuário:

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@exemplo.com"
```

Essas informações são utilizadas para identificar o autor das alterações no repositório.

## Principais Conceitos

### 1. Repositório (Repository)
É onde o Git armazena o histórico completo do projeto, incluindo todas as versões dos arquivos. Pode ser local (em sua máquina) ou remoto (em plataformas como GitHub).

### 2. Commit
É um "snapshot" do estado atual dos arquivos do projeto. Cada commit possui uma mensagem que descreve a alteração realizada.

### 3. Branch
Uma branch é uma linha independente de desenvolvimento. A branch padrão é a `main` (ou `master`), mas você pode criar outras branches para adicionar novas funcionalidades ou corrigir bugs sem afetar o código principal.

### 4. Merge
Ocorre quando duas branches são combinadas. Em um merge, as alterações de uma branch são unidas a outra, geralmente na branch principal (`main` ou `master`).

## Comandos Essenciais

### 1. Criar um Novo Repositório
Para iniciar um repositório em um projeto existente:

```bash
git init
```

### 2. Clonar um Repositório Existente
Para obter uma cópia de um repositório remoto (no GitHub, por exemplo):

```bash
git clone URL_DO_REPOSITORIO
```

### 3. Status do Repositório
Para verificar o status dos arquivos no repositório:

```bash
git status
```

### 4. Adicionar Arquivos para Commit
Para adicionar arquivos modificados para o próximo commit:

```bash
git add NOME_DO_ARQUIVO
# Ou para adicionar todos os arquivos
git add .
```

### 5. Fazer um Commit
Para salvar as alterações no repositório com uma mensagem de descrição:

```bash
git commit -m "Descrição do commit"
```

### 6. Visualizar Histórico de Commits
Para ver o histórico de commits:

```bash
git log
```

### 7. Criar uma Nova Branch
Para criar uma nova branch e mudar para ela:

```bash
git checkout -b nome-da-branch
```

### 8. Mudar de Branch
Para alternar entre branches:

```bash
git checkout nome-da-branch
```

### 9. Unir Branches com Merge
Para unir uma branch à branch atual:

```bash
git merge nome-da-branch
```

### 10. Resolver Conflitos de Merge
Ao fazer um merge, pode haver conflitos se as mesmas linhas de código forem modificadas em ambas as branches. O Git indicará os arquivos com conflitos, e é necessário editá-los manualmente.

### 11. Enviar Alterações para o Repositório Remoto
Para enviar commits da branch atual para o repositório remoto:

```bash
git push origin nome-da-branch
```

### 12. Atualizar o Repositório Local
Para baixar e incorporar as alterações do repositório remoto:

```bash
git pull origin nome-da-branch
```

## GitHub: Trabalhando com Repositórios Remotos

### 1. Criando um Repositório no GitHub
1. Acesse [github.com](https://github.com/) e faça login.
2. Clique em “New Repository” (Novo Repositório).
3. Escolha um nome, configure como público ou privado e clique em "Create Repository" (Criar Repositório).

### 2. Associando um Repositório Local ao GitHub
Após criar um repositório no GitHub, você pode associar seu repositório local com o remoto:

```bash
git remote add origin URL_DO_REPOSITORIO
git push -u origin main
```

### 3. Pull Requests
O **Pull Request (PR)** é uma proposta para unir suas alterações a uma branch principal (geralmente `main`). É uma forma de solicitar que seu código seja revisado antes de ser integrado.

### 4. Forks e Colaboração
O **Fork** permite criar uma cópia de um repositório para colaborar em um projeto sem alterar o repositório original. Você pode fazer um fork, clonar o repositório, fazer alterações e depois criar um pull request para contribuir com o projeto original.

---

## Fluxo de Trabalho no Git e GitHub

1. **Clonar** o repositório ou fazer um **fork**.
2. Criar uma **nova branch** para implementar uma funcionalidade.
3. **Adicionar** e **comitar** as alterações.
4. **Enviar** (push) a branch para o GitHub.
5. Criar um **pull request** para revisão e, após aprovação, **fazer o merge** na branch principal.

## Comandos Avançados

- **git stash**: salva as mudanças não comitadas para limpeza temporária do diretório.
- **git rebase**: reorganiza commits em uma branch para manter um histórico linear.

## Conclusão

Git e GitHub são ferramentas essenciais para o desenvolvimento colaborativo. Com o tempo, você dominará o fluxo de trabalho e os comandos, facilitando o gerenciamento e a colaboração em projetos de qualquer tamanho.
