# Regras de Git

## TLDR

Esta documentação visa definir os principais padrões de nomenclatura para `commits`, `branches` e `Pull Requests`.
Para ter uma alteração aprovada neste repositório é necessário que todas as especificações feitas aqui sejam seguidas corretamente.

As mensagens e sumários são escritos em português.

## Patterns

Nossos padrões seguem a seguinte litas de `types`:

- **docs**: Alterações que afetam a documentação do projeto.
- **feat**: Uma nova feature para o projeto (ex: Novos exercícios, documentações, ...)
- **fix**: Correção de problemas no repositório
- **refactor**: Refatora parte do projeto, porém sem acrescentar conteúdo.
- **test**: Adiciona testes a um exercício.

### Branches

Uma branch deve sempre partir da `master` e seguir o seguinte padrão:

- {`type`}/{`isse number`}/{`short summary`}

Um fluxo válido de criação de branch seria por exemplo:

```bash
git checkout master # vai para a branch master
git pull origin master # atualiza sua branch local com atualizações mais recentes do repo
git checkout -b feat/7/adiciona-exercicios-html # cria uma nova branch
```

### Commit

Uma mensagem de commit deve seguir o seguinte padrão:

- {`type`}: {`short summary`}

Um fluxo válido de criação de um commit seria por exemplo:

```bash
git add conversor # prepara suas modificações para serem salvas na pasta conversor
git commit -m "feat: adiciona projeto conversor" # salva as alterações

git push origin <sua_branch> # envia as alteracoes para o github
```

### Pull Requests

Uma pull request deve ter o seguinte padrão de nome:

- {`type`}: {`short summary`} {`#PR reference`}

Um exemplo de título válido seria:

> feat: adiciona exercicio conversor  #6

Lembrando, para o `PR` ser aceito é necessário que o mesmo esteja adequado a todas as regras descritas acima, bem como as demais descritas na documentação de [Contributing](./CONTRIBUTING.md).
