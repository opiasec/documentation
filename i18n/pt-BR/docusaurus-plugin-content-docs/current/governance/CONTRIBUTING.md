# Contribuindo para o [NOME DO PROJETO]

Antes de mais nada, obrigado por considerar contribuir para o [NOME DO PROJETO]! São pessoas como você que fazem deste projeto uma ótima ferramenta para a comunidade de AppSec. Estamos ansiosos para ver o que você trará para o nosso projeto.

Este documento descreve o processo para contribuir com a nossa plataforma. Por favor, leia-o com atenção para garantir uma colaboração tranquila e eficaz.

## Código de Conduta

Ao participar deste projeto, você deve seguir o nosso [Código de Conduta](CODE_OF_CONDUCT.md). Por favor, leia-o antes de começar. Espera-se que todos os contribuidores o sigam para nos ajudar a manter este um ambiente acolhedor e amigável.

## Como Eu Posso Contribuir?

Existem muitas maneiras de contribuir, e todas são valiosas. Você pode:

* **Reportar Bugs:** Se você encontrar um bug, por favor, abra uma issue usando o template "Bug Report". Forneça o máximo de detalhes possível.
* **Sugerir Melhorias:** Tem uma ideia para uma nova funcionalidade ou um novo laboratório? Adoraríamos ouvi-la. Abra uma issue usando o template "Feature Request" ou "New Lab Proposal".
* **Melhorar a Documentação:** Se você encontrar partes da nossa documentação que estão confusas ou incompletas, por favor, envie um pull request com suas melhorias.
* **Escrever Código:** Ajude-nos a corrigir bugs ou a implementar novas funcionalidades.

Se você está procurando por onde começar, verifique as issues com as etiquetas 
* [`good first issue`](https://github.com/opiasec/documentation/labels/good%20first%20issue) 
* [`help wanted`](https://github.com/opiasec/documentation/labels/help%20wanted).

## Sua Primeira Contribuição de Código

Pronto para contribuir com código? Aqui está o fluxo de trabalho que nosso projeto segue.

### Passo 1: Encontre ou Crie uma Issue

Antes de começar a escrever código, por favor, verifique a nossa [aba de Issues](https://github.com/opiasec/documentation/issues) para ver se já existe uma issue para o que você quer fazer.

* Se uma issue existir, por favor, deixe um comentário dizendo que você gostaria de trabalhar nela. Isso nos ajuda a evitar trabalho duplicado.
* Se não existir uma issue, por favor, crie uma primeiro para discutir as mudanças propostas com os mantenedores. Para mudanças significativas, por favor, siga nosso [Processo de RFC](rfc-process.md).

### Passo 2: Faça o Fork do Repositório

Clique no botão "Fork" no canto superior direito da página do repositório para criar uma cópia pessoal do projeto em sua própria conta do GitHub.

### Passo 3: Configure seu Ambiente de Desenvolvimento

1.  **Clone o seu fork:**
    ```bash
    git clone [https://github.com/](https://github.com/)[SEU_USUARIO]/documentation.git
    cd [SEU_REPO]
    ```

2.  **Adicione o remote `upstream`:** Isso ajudará você a manter seu fork sincronizado com o projeto principal.
    ```bash
    git remote add upstream [https://github.com/](https://github.com/)opiasec/documentation.git
    ```

3.  **Instale as dependências:** Nós usamos [Yarn/NPM] para gerenciar os pacotes.
    ```bash
    # Usando Yarn
    yarn install

    # Ou usando NPM
    npm install
    ```

### Passo 4: Crie uma Nova Branch

Crie um nome de branch descritivo para suas alterações. Isso ajuda a todos a entenderem no que você está trabalhando.

```bash
# Exemplo para uma nova funcionalidade
git checkout -b feat/adicionar-lab-xss

# Exemplo para uma correção de bug
git checkout -b fix/resolver-bug-login
```

### Passo 5: Escreva Seu Código

Faça suas alterações, escreva seu código e adicione seus testes\! Enquanto trabalha, lembre-se de:

  * Seguir o estilo de código existente.
  * Garantir que seu código esteja bem comentado, especialmente em áreas complexas.
  * Adicionar ou atualizar testes conforme apropriado.

### Passo 6: Teste Suas Alterações

Execute nosso linter e testes automatizados para garantir que suas alterações não quebraram nada.

```bash
# Execute o ESLint para verificar problemas de estilo
npm run lint
```

<!-- 
```bash
# Execute todos os testes
npm run test
```
-->

### Passo 7: Faça o Commit das Suas Alterações

Nós usamos **Conventional Commits** para manter um histórico do git claro e legível. Por favor, formate suas mensagens de commit de acordo.

Sua mensagem de commit deve ser estruturada da seguinte forma:

```
<tipo>[escopo opcional]: <descrição>

[corpo opcional]

[rodapé(s) opcional(is)]
```

**Tipos comuns:**

  * `feat`: Uma nova funcionalidade
  * `fix`: Uma correção de bug
  * `docs`: Mudanças apenas na documentação
  * `style`: Mudanças que não afetam o significado do código (espaços em branco, formatação, etc)
  * `refactor`: Uma alteração de código que não corrige um bug nem adiciona uma funcionalidade
  * `test`: Adicionando testes ausentes ou corrigindo testes existentes
  * `chore`: Mudanças no processo de build ou em ferramentas auxiliares

**Exemplo:**

```
feat(labs): Adiciona novo desafio de laboratório de Stored XSS
```

### Passo 8: Faça o Push para o Seu Fork

Envie suas alterações para o seu repositório forkado.

```bash
git push origin feat/adicionar-lab-xss
```

### Passo 9: Envie um Pull Request (PR)

1.  Vá para o repositório original no GitHub. Você deverá ver um aviso para criar um Pull Request a partir da sua nova branch.
2.  Certifique-se de que o PR está apontando para a branch `main` do repositório upstream.
3.  Preencha o template do PR com um título e uma descrição claros de suas alterações. Vincule a issue que você está resolvendo (ex: "Closes \#123").
4.  Se o seu PR envolver mudanças visuais, por favor, inclua screenshots ou GIFs.

## O Processo de Revisão

Depois de enviar seu PR, eis o que esperar:

1.  **Verificações Automatizadas:** Nosso pipeline de CI/CD (GitHub Actions) executará automaticamente o linter e os testes. Certifique-se de que essas verificações passem.
2.  **Revisão de Código:** Um ou mais mantenedores revisarão seu código. Podemos pedir alterações ou melhorias. Isso é uma parte normal do processo\! Estamos aqui para colaborar.
3.  **Aprovação e Merge:** Assim que seu PR for aprovado e todas as verificações estiverem passando, um mantenedor fará o merge do seu código na branch `main`.

Parabéns e muito obrigado pela sua contribuição\!

## Dúvidas?

Se você tiver qualquer dúvida, sinta-se à vontade para nos contatar em nosso:
  * [Servidor no Discord](https://discord.gg/xAkfKHRz)
  * [GitHub Discussions](https://github.com/orgs/AppSec-Digital/discussions)