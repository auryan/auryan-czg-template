
# :speech_balloon: Regras de Contribuição

`🇺🇸` Go to [english version](README.md).

Para ser sincero, não possuo nenhuma norma rígida que limite sua contribuição, pois acredito que você é **livre** para ajudar da forma que achar melhor, desde que suas sugestões de mudanças sejam pertinentes para o projeto.

A única exigência que faço é que você não escreva a mensagem de um commit de maneira "bruta" (utilizando `git commit -m "uma mensagem qualquer"`), pois isso pode gerar confusão para quem for revisar o histórico de commits.

Para solucionar isso, solicito que utilize czg para padronizar o formato das suas mensagens.

### O que é czg?

Czg é uma ferramenta que oferece uma interface de linha de comando interativa que ajuda a criar mensagens de commit que seguem o padrão do [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/).

Você pode personalizar o czg para atender às suas necessidades. Por exemplo, você pode adicionar novos tipos de commit, escopos, etc.

Todas as informações sobre o czg podem ser encontradas no [site oficial](https://cz-git.qbb.sh/cli/).

## :wrench: Instalação

> :warning: Antes de tudo, é necessário ter o [Node.js](https://nodejs.org/en/) instalado em sua máquina.

### Template Padrão

Utilizando [meu template padrão](cz.config.js), a linguagem dos tipos de commit será baseada no valor da propriedade `config.language`, localizada no `package.json` de cada projeto. Isso permite escrever mensagens de commit em português ou inglês, dependendo do projeto.

Instalando o meu pacote `auryan-czg-template`, você estará instalando o `czg` e o meu template padrão:

```bash
npm install -g auryan-czg-template
```

### Template Específico

Haverá projetos que utilizam templates específicos. Para verificar se o projeto em que você está contribuindo usa um template específico, é possível verificar a existência do arquivo `cz.config.js` no diretório raiz.

Se o arquivo não for encontrado, significa que o [padrão](#template-padrão) está sendo utilizado. Caso contrário, instale o `czg` diretamente:

```bash
npm install -g czg
```

## :memo: Mensagem de Commit

Após fazer as alterações no projeto, é hora de criar a mensagem de commit. Para isso, basta executar o comando:

```bash
czg
```

## :robot: Mensagem de Commit com IA

Também é possível gerar uma mensagem de commit com inteligência artificial usando o comando:

```bash
czg ai
```

No entanto, antes de usar esse comando, é necessário configurar sua chave da OpenAI. Caso não tenha, pode criar uma nova no [site da OpenAI]((https://platform.openai.com/account/api-keys)).

Com a chave em mãos, configure-a com o comando:

```bash  
czg --openai-token="sua-chave-aqui"
```
> :warning: Não compartilhe sua chave com ninguém, pois ela dá acesso a sua conta da OpenAI.

### Opções

Você pode escolher quantas mensagens serão geradas com a opção `-N=` ou `--ai-num=`:

```bash  
czg ai -N=3
# Serão geradas 3 mensagens de commit
czg ai --ai-num=5
# Serão geradas 5 mensagens de commit
```

Para mais informações, veja a seção [options](https://cz-git.qbb.sh/cli/ai#options) no site do czg.

---

> *“É provável que a explicação que exige o menor número possível de suposições esteja correta”.*  
> — [**William of Ockham**](https://pt.wikipedia.org/wiki/Navalha_de_Ockham).