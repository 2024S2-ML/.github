# .github

### Guia Completo de Uso do GitHub: Comandos Básicos e Avançados

#### 1. Introdução ao Git e GitHub

**Git** é um sistema de controle de versão distribuído, enquanto **GitHub** é uma plataforma de hospedagem de código que usa Git para versionamento e oferece funcionalidades adicionais como colaboração, revisão de código, e gerenciamento de projetos.

#### 2. Configuração Inicial

1. **Instalação do Git**:
   - **Windows**: Baixe e instale o Git em [git-scm.com](https://git-scm.com).
   - **macOS**: Use `brew install git` se tiver o Homebrew instalado.
   - **Linux**: Use o gerenciador de pacotes da sua distribuição, por exemplo, `sudo apt-get install git`.

2. **Configuração Inicial**:
   ```sh
   git config --global user.name "Seu Nome"
   git config --global user.email "seuemail@example.com"
   ```

#### 3. Comandos Básicos do Git

1. **Inicializar um repositório**:
   ```sh
   git init
   ```

2. **Clonar um repositório existente**:
   ```sh
   git clone https://github.com/usuario/repo.git
   ```

3. **Verificar o status do repositório**:
   ```sh
   git status
   ```

4. **Adicionar arquivos para a área de stage**:
   ```sh
   git add arquivo.txt
   # ou para adicionar todos os arquivos modificados
   git add .
   ```

5. **Fazer commit das mudanças**:
   ```sh
   git commit -m "Mensagem do commit"
   ```

6. **Visualizar o histórico de commits**:
   ```sh
   git log
   ```

#### 4. Trabalhando com Branches

1. **Criar uma nova branch**:
   ```sh
   git branch nome-da-branch
   ```

2. **Mudar para uma branch específica**:
   ```sh
   git checkout nome-da-branch
   ```

3. **Criar e mudar para uma nova branch**:
   ```sh
   git checkout -b nome-da-branch
   ```

4. **Mesclar uma branch ao branch atual**:
   ```sh
   git merge nome-da-branch
   ```

5. **Excluir uma branch**:
   ```sh
   git branch -d nome-da-branch
   ```

#### 5. Sincronização com GitHub

1. **Adicionar um repositório remoto**:
   ```sh
   git remote add origin https://github.com/usuario/repo.git
   ```

2. **Enviar commits para o repositório remoto**:
   ```sh
   git push origin main
   ```

3. **Puxar mudanças do repositório remoto**:
   ```sh
   git pull origin main
   ```

#### 6. Comandos Avançados do Git

1. **Rebasing**:
   ```sh
   git rebase nome-da-branch
   ```

2. **Stash**:
   - Salvar mudanças não commitadas:
     ```sh
     git stash
     ```
   - Recuperar mudanças stashadas:
     ```sh
     git stash pop
     ```

3. **Reset**:
   - Resetar área de stage e manter mudanças locais:
     ```sh
     git reset HEAD arquivo.txt
     ```
   - Resetar commit e área de stage, manter mudanças locais:
     ```sh
     git reset --soft HEAD~1
     ```
   - Resetar commit, área de stage e mudanças locais:
     ```sh
     git reset --hard HEAD~1
     ```

4. **Cherry-pick**:
   ```sh
   git cherry-pick hash-do-commit
   ```

5. **Tagging**:
   - Criar uma tag:
     ```sh
     git tag -a v1.0 -m "Versão 1.0"
     ```
   - Enviar tags para o repositório remoto:
     ```sh
     git push origin --tags
     ```

#### 7. Integração Contínua e Deploy

- **GitHub Actions**: Configure workflows de integração e deploy contínuo diretamente no GitHub usando [GitHub Actions](https://github.com/features/actions).

#### 8. Colaboração no GitHub

1. **Fork**: Faça um fork de um repositório para sua conta GitHub.
2. **Pull Request**: Envie um pull request para contribuir com mudanças em um repositório original.
3. **Issues**: Crie e gerencie issues para rastrear bugs e features.

#### 9. Dicas e Boas Práticas

1. **Commits Pequenos e Descritivos**: Faça commits pequenos e com mensagens descritivas.
2. **Branches de Funcionalidade**: Use branches separadas para cada funcionalidade ou correção.
3. **Revisão de Código**: Faça revisões de código através de pull requests para garantir a qualidade.

Este guia cobre desde os comandos básicos até alguns dos mais avançados que você pode precisar ao trabalhar com Git e GitHub. Para um uso mais aprofundado, considere explorar a [documentação oficial do Git](https://git-scm.com/doc) e [documentação do GitHub](https://docs.github.com).
