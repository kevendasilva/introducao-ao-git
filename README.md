# **Uma introdução ao git**

Uma breve introdução ao controle de versão com git.

<img src="img/git.png" style="background-color: white; margin: 30px 20px 0 20px" align="right" width=400 height=auto>

## **0. Instalação do git 🪛**

Esta introdução parte do pressuposto que você já instalou o git na sua máquina. Se não fez a instalação, faça agora. Link para download: [Download Git](https://git-scm.com/downloads). O git está disponível para Linux, Windows e Mac. A instalação é bem simples.

## **1. Configurações iniciais depois da instalação ✍️**

Ao instalar o git no seu computador, quando você tentar criar um commit (saberá como criar em breve), pela primeira vez, você verá a seguinte mensagem:

```
*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.
```

Pedindo para você configurar algumas informações. E elas são: seu nome e email. Vamos evitar o primeiro susto com o terminal, adicionando antes, as informações iniciais necessárias. Os comandos utilizados para definir o seu nome e email, são:

```
$ git config --global user.name "<seu nome>"
```

onde `<seu nome>` deve ser substituído pelo seu nome, e

```
$ git config --global user.email "<seu email>"
```

onde `<seu email>` deve ser substituído pelo seu email (de preferência o utilizado na sua conta do repositório remoto). O parâmetro `--global` é utilizado, quando se deseja definir o nome e email para todos os repositórios locais.

## **2. Dando push em um projeto já existente 🤔**

Caso você possua um projeto local, e deseje enviá-lo para um repositório remoto, utilize o seguinte comando:

```
$ git remote add origin <link do repositório remoto>
```

E dê push no projeto. Após isso, o projeto será adicionado no repositório remoto. Existe um pequeno tutorial no repositório remoto que você criou para guardar o projeto (seja no GitHub ou GitLab).

### **2.1 Caso o projeto já exista em um repositório remoto 🖥️**

Agora, você irá aprender como clonar um repositório. Utilizando o seguinte comando, você clonará um projeto:

```
$ git clone <link do repositório remoto>
```

para adicionar novas alterações no repositório remoto, salve o estado do projeto e crie um commit. Logo em seguida, dê push nas alterações.

## **3. Salvando o estado dos arquivos para dar commit e criando um commit ✅**

Para salvar o estado dos arquivos em um commit, utilize o seguinte comando:

```
$ git add <arquivo 1> <arquivo 2> ... <arquivo n>
```

caso queira adicionar determinados arquivos. Se quiser adicionar todos os arquivos que foram alterados/criados no projeto, e não foram salvos em commits anteriores, use:

```
$ git add .
```

e todos os arquivos serão salvos para o commit. Em seguida, utilize:

```
$ git commit -m '<mensagem>'
```

onde `<mensagem>` é uma mensagem que descreve o motivo do commit. E todas suas alterações serão salvas no novo commit. Lembre-se de dar push para suas alterações serem adicionadas no repositório remoto (sempre, antes de dar push dê um: `git pull`, para atualizar o repositório local).

## **4. Dando push e lidando com conflitos 🏃**

Caso o repositório remoto tenha sido atualizado por outro dev, quando você executar o comando:

```
$ git pull
```

é possível que algumas partes do projeto, tenham sido alteradas e isso poderá gerar conflitos. Isso acontece quando partes do código foram alteradas, e existem diferenças entre o código local e o código que está chegando do repositório remoto. Resolva os conflitos (não é tão difícil 🤪) e dê push na sua alterações com:

```
$ git push
```

## **Links úteis (indicações não obrigatórias) 👈**

Vídeo e sites indicados caso queiram saber mais.

1. Uma representação gráfica e tutorial do que acontece com o git: https://learngitbranching.js.org/
2. Documentação sobre criação de mensagens de commits (em inglês): https://chris.beams.io/posts/git-commit/
3. Documentação oficial do git: https://git-scm.com/doc
4. Documentação oficial do GitHub: https://docs.github.com/pt/github/getting-started-with-github
