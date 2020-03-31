# Instalando o Node.js

## Trabalhe com módulos e JavaScript no servidor

![A revolução JavaScript nos trouxe o Node.js](https://cdn-images-1.medium.com/max/6750/1*CC_GhFXCUxQDfIJ_Tl-pug.jpeg)

O [**Node.js](https://nodejs.org/pt-br/)** é um sistema open source em tempo execução JavaScript, criado com o mecanismo JavaScript [**V8](https://v8.dev/)** utilizado pelo Google Chrome. O V8, implementa o *ECMAScript* (especificação JavaScript) e é escrito em C++, e roda em Windows, Mac e Linux, permitindo a execução de programas escritos com JavaScript.

Sistemas de tempo de execução são sistemas que convertem linguagem de programação em código interpretado por máquinas.
> # Como um ambiente de execução JavaScript assíncrono orientado a eventos, o Node.js é projetado para desenvolvimento de aplicações escaláveis de rede.

O Node.js, apesar de jovem, é a força motriz por trás de um ecossistema gigante de aplicações sofisticadas em JavaScript.

O Node.js é um sistema open source, de código aberto, mantido pela [OpenJS Foundation](https://openjsf.org/).

Saber JavaScript significa entender seu funcionamento no navegador e no servidor, pois sim, é possível com uma única linguagem (especificação) atuar nos dois lado. Talvez só o PHP seja tão despojado quanto o Node.js.

Fazendo um paralelo com o mundo Java, imagine o Node.js como a JVM, capaz de interpretar o código em JavaScript e conversar com o sistema operacional.

Com o Node.js é possível também gerenciar módulos JavaScript. Módulos são pequenos scripts JavaScript responsáveis por pequenas funcionalidades. Com o Package Manager do Node.js, é possível adicioná-las ao seu projeto reutilizando código.

Documentação oficial: [nodejs.org](https://nodejs.org/)

## Usando o Terminal

Para trabalhar com Node.js é importante entender de (**CLI** — *Command Line Interface*). A maioria das operações são feitas através de linhas de comandos no terminal.

Alguns terminais para diferentes sistemas operacionais:

* Linux **Terminator** ([https://terminator-gtk3.readthedocs.io/en/latest/](https://terminator-gtk3.readthedocs.io/en/latest/))

* Mac **iTerm** ([https://www.iterm2.com](https://www.iterm2.com))

* Windows **Node Command Line** (**cmd**), **PowerShell** ([https://docs.microsoft.com/pt-br/powershell/](https://docs.microsoft.com/pt-br/powershell/))

## Instalando o Node.js

Existem várias maneiras de instalar o Node.js. A versão atual, com suporte a longo tempo (**LTS** — *Long Term Support*) é a mais recomendada, mas cada projeto pode exigir uma versão específica do Node.js. Ou seja, se você instalar apenas uma versão na sua máquina, poderá ser complicado mudar caso um projeto precise de uma versão específica, mais antiga, por exemplo. Neste tutorial, vamos demonstrar duas opções de instalar o Node.js:

* **Opção 1 — Baixando arquivo Binário**

* **Opção 2 — Utilizando o NVM (recomendada)**

### Opção 1 — Baixando arquivo Binário

A forma mais tradicional de instalar o Node.js é acessando a página [**https://nodejs.org/pt-br/download/](https://nodejs.org/pt-br/download/)**, escolha seu sistema operacional e baixe o arquivo binário o executando após o download. Esta opção é interessante para usuários de Windows e Mac. Basta executar o arquivo apenas.

**Debian e Ubuntu based Linux**

Aqui tem um passo a passo de como instalar o arquivo binário via terminal: [https://github.com/nodejs/help/wiki/Installation](https://github.com/nodejs/help/wiki/Installation)

No terminal, faça o download da última versão LTS:

    wget [https://nodejs.org/dist/vXX.XX.X/node-vXX.XX.XX-linux-x64.tar.xz](https://nodejs.org/dist/vXX.XX.X/node-vXX.XX.XX-linux-x64.tar.xz)

Descompacte o arquivo:

    tar -xvf node-vXX.XX.X-linux-x64.tar.xz

Acesse o diretório descompactado:

    cd node node-vXX.XX.X-linux-x64

Copie os arquivos para sua pasta local

    sudo cp -R * /usr/local/

Certifique-se de que o Node está instalado. A resposta deve ser a versão do Node para o comando no terminal:

    node -v
    vXX.X.X

Você pode instalar o Node de diversas outras maneiras no Linux: [https://github.com/nodesource/distributions/blob/master/README.md](https://github.com/nodesource/distributions/blob/master/README.md)

### Opção 2 — Utilizando o NVM (recomendado)

Às vezes, é preciso utilizar mais de uma versão do Node.js para executar projetos distintos. A solução é utilizar um versionador do Node.js (***Node Version Manager***). Um dos mais populares é o **NVM**.

Para Windows:

**NVM Windows:** [https://github.com/coreybutler/nvm-windows](https://github.com/coreybutler/nvm-windows)

Para Mac e Unix based (Linux):

**NVM:** [https://github.com/creationix/nvm](https://github.com/creationix/nvm)

Para instalar ou atualizar o NVM, você deve executar o [script de instalação](https://github.com/nvm-sh/nvm/blob/v0.35.3/install.sh) . Para fazer isso, você pode baixar e executar o script manualmente ou usar o seguinte comando cURL ou Wget:

    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash

    wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash

A execução de qualquer um dos comandos acima baixa um script e o executa. O script clona o repositório nvm para ~/.nvm, e as tentativas para adicionar as linhas de origem a partir do trecho abaixo para o arquivo de perfil correto ( ~/.bash_profile, ~/.zshrc, ~/.profileou ~/.bashrc).

**Verificar instalação:**

Para verificar se o NVM foi instalado, faça:

    command -v nvm

O resultado deve ser nvm.

Agora você pode baixar diferentes versões do Node.js e alternar entre elas com o comando nvm use

**Exemplo de uso:**

    nvm use 12

Estes outros artigos contém mais ajuda sobre como instalar o Node.js com o NVM:

[Como instalar Node.js com NVM](https://medium.com/collabcode/como-instalar-node-js-no-linux-corretamente-ubuntu-debian-elementary-os-729fb4c92f2d)

[Instalando e gerenciando várias versões do Node.js com NVM](https://www.treinaweb.com.br/blog/instalando-e-gerenciando-varias-versoes-do-node-js-com-nvm/)

## Testando a instalação do Node.js

Em qualquer diretório no terminal, crie um arquivo JavaScript:

    vim index.js

No arquivo digite apenas:

    console.log(“hello world”)

Salve, e no terminal execute o arquivo no Node.js:

    node index.js

O resultado deve ser:

    hello world

## NPM

O Node.js já vem com o **NPM** instalado. Ele é um Gerenciador de Pacotes (*Package Manager*) e serve para instalar módulos JavaScript em ambiente de desenvolvimento ou para serem usados na sua aplicação em produção.

Como instalar módulos como NPM:

    **$** npm install request -g // instala globalmente
    **$** npm install express — save // dependência da app
    **$** npm install node-sass — save-dev // dependência apenas para desenvolvimento da app

Para buscar todos os pacotes disponíveis no NPM: [https://www.npmjs.com/](https://www.npmjs.com/)

Uma alternativa ao NPM é o **Yarn**, desenvolvido pelo Facebook Labs: [https://yarnpkg.com/en/](https://yarnpkg.com/en/)
