
# :speech_balloon: Contribution Rules

`🇧🇷` Ir para [versão em português](README.pt-BR.md).

To be honest, I don't have any strict rules that limit your contribution, as I believe you are **free** to help in any way you see fit, as long as your proposed changes are relevant to the project.

The only requirement I have is that you don't write a commit message in a "raw" way (using `git commit -m "any message"`), as this can cause confusion for those who will review the commit history.

To solve this, I ask that you use czg to standardize the format of your messages.

### What is czg?

Czg is a tool that provides an interactive command-line interface that helps create commit messages that follow the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) standard.

You can customize czg to meet your needs. For example, you can add new types of commits, scopes, etc.

All information about czg can be found on the [official website](https://cz-git.qbb.sh/cli/).

## :wrench: Installation

> :warning: Before anything else, you need to have [Node.js](https://nodejs.org/en/) installed on your machine.

### Default Template

Using my [default template](cz.config.js), the language of commit types will be based on the value of the `config.language` property, located in the `package.json` of each project. This allows writing commit messages in Portuguese or English, depending on the project.

By installing my package `auryan-czg-template`, you will be installing `czg` and my default template:

```bash
npm install -g auryan-czg-template
```

### Specific Template

There will be projects that use specific templates. To check if the project you are contributing to uses a specific template, you can check for the existence of the `cz.config.js` file in the root directory.

If the file is not found, it means that the [default](#default-template) is being used. Otherwise, install `czg` directly:

```bash
npm install -g czg
```

## :memo: Commit Message

After making changes to the project, it's time to create the commit message. To do this, simply run the command:

```bash
czg
```

## :robot: Commit Message with AI

It is also possible to generate a commit message with artificial intelligence using the command:

```bash
czg ai
```

However, before using this command, you need to configure your OpenAI key. If you don't have one, you can create a new one on the [OpenAI website](https://platform.openai.com/account/api-keys).

With the key in hand, configure it with the command:

```bash  
czg --openai-token="your-key-here"
```
> :warning: Do not share your key with anyone, as it gives access to your OpenAI account.

### Options

You can choose how many messages will be generated with the `-N=` or `--ai-num=` option:

```bash  
czg ai -N=3
# 3 commit messages will be generated
czg ai --ai-num=5
# 5 commit messages will be generated
```

For more information, see the [options](https://cz-git.qbb.sh/cli/ai#options) section on the czg website.

---

> *“The explanation that requires the fewest assumptions is probably correct.”*  
> — [**William of Ockham**](https://en.wikipedia.org/wiki/Ockham%27s_razor).