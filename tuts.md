# O que você precisa saber sobre Git

## Como utilizar a ferramenta de versionamento de código

![](https://cdn-images-1.medium.com/max/2560/1*9jJ_19suR569xZyY71Kyow.png)

## Versionamento de código

### Benefícios do controle de versão

Os sistemas de controle de versão são uma categoria de ferramentas de software que ajudam uma equipe de software a gerenciar alterações no código fonte ao longo do tempo.

O software de controle de versão controla todas as modificações no código em um tipo especial de banco de dados. Se um erro for cometido, os desenvolvedores podem voltar no tempo e comparar versões anteriores do código para ajudar a corrigir o erro e minimizar a interrupção para todos os membros da equipe.

Mais informações em [**Atlassian — O que é versionamento de controle](https://www.atlassian.com/git/tutorials/what-is-version-control)**.

### O que é Git

De longe, o sistema de controle de versão moderno mais usado no mundo hoje é o Git.

O Git é um projeto de código aberto maduro, mantido ativamente, originalmente desenvolvido em 2005 por Linus Torvalds, o famoso criador do kernel do sistema operacional Linux.

Git e [GitHub](https://github.com/) são coisas diferentes. Git é o software instalado na máquina responsável por controlar o versionamento do seu código. O [GitHub](https://github.com/) é um repositório remoto online capaz de armazenar seu código versionar.

Alternativas ao Git: [Tortoise](https://tortoisegit.org/). Alternativas ao Github: [BitBucket](https://bitbucket.org/), [GitLab](https://about.gitlab.com/).
>  *Para saber mais sobre [**Github](https://github.com/)**, consulte o post [**Compartilhando códigos no GitHub](https://medium.com/@dnvtrn/compartilhando-c%C3%B3digos-no-github-df450d2c8a25)***
>  *Para saber mais sobre projetos Open Source, consulte o post [**Contribuindo para projetos Open Source](https://medium.com/@dnvtrn/contribuindo-para-projetos-open-source-5453686f8d8d)***

## Instalando o Git

A instalação depende do seu sistema operacional. Verifique as opções e instruções no link [**Instale o Git](https://www.atlassian.com/git/tutorials/install-git)**.

## O que é um repositório Git?

Um repositório Git é um armazenamento virtual do seu projeto. Ele permite que você salve versões do seu código, que você pode acessar quando necessário.

## Clonando um repositório existente: git clone

O comando git clone é a maneira mais comum dos usuários obterem um clone de desenvolvimento local de um repositório remoto no [Github](https://github.com/).

Para clonar um repositório criado ou *forkado* no [Github](https://github.com/) por exemplo, na sua máquina, vá até o terminal de sua preferência e digite o comando:

git clone https://github.com/nome-de-usuario/nome-do-projeto

Para acessar o diretório clonado:

cd nome-do-projeto
>  *Para saber mais sobre como ***"forkar"** *repositórios remotos no [**Github](https://github.com/)**, consulte o post [**Compartilhando códigos no GitHub](https://medium.com/@dnvtrn/compartilhando-c%C3%B3digos-no-github-df450d2c8a25)***

## Configurando repositórios remotos: git remote

Se você for atuar em um repositório clonado, você deverá configurar dois repositórios remotos. Esta é a parte onde você deve prestar mais atenção no processo, pois qualquer erro impedirá que você envie seus arquivos para o repositório correto.

O primeiro repositório remoto é chamado de “*origin*”, e já deve estar configurado caso você tenha feito o clone do seu *fork* Github. Informe o comando git remote -v e verifique se o repositório remoto origin aponta para a sua conta e para seu *fork*:

    origin	https://github.com/nome-de-usuario/nome-projeto.git (fetch)
    origin	https://github.com/nome-de-usuario/nome-projeto.git (push)

Agora, você deve configurar um repositório remoto que aponte para o repositório original de onde o projeto foi “forkado”. O seu repositório forkado se chama “*origin*”, e o repositório de onde ele veio irá se chamar “*upstream*”. Com o repositório upstream configurado no Git, é possível sincronizar alterações que fazemos em um *fork* com o repositório original. Isso também permite sincronizar alterações feitas no repositório original com o *fork*.

Para adicionar o repositório remoto remoto upstream digite o comando no terminal:

    git remote add upstream https://github.com/dono-do-fork/nome-projeto.git

Agora você tem dois repositórios remotos configurados. Verifique o novo repositório upstream especificado para o *fork*:

    $ git remote -v
    > origem    https://github.com/nome-usuario/nome-projeto.git (fetch)
    > origem    https://github.com/nome-usuario/nome-projeto.git (push)
    > upstream  https://github.com/dono-do-fork/nome-projeto.git (fetch)
    > upstream  https://github.com/dono-do-fork/nome-projeto.git (push)

## Sincronizando o repositório local com o repositório remoto: git pull

O comando git pull é usado para buscar e fazer download de conteúdo de um repositório remoto e atualizar imediatamente o repositório local para corresponder a esse conteúdo.

    git pull origin master

IMPORTANTE: Para buscar as atualizações que contribuidores publicam no projeto original (Ex.: http://github.com/dono-do-fork/nome-projeto), você deve sempre fazer um git pull upstream master. As atualizações serão adicionadas na branch do seu *fork*.

## Exibindo o estado das alterações feitas: git status

O comando git status exibe o estado do diretório de trabalho local e a área de temporária. Permite ver quais alterações foram testadas, quais não foram e quais arquivos não estão sendo rastreados pelo Git. A saída de status não mostra nenhuma informação sobre o histórico do projeto confirmado.

    git status

## Verificando as “branches” existentes: git branch

O comando git branch permite criar, listar, renomear e excluir "*branches*". *Branches* são ramificações (galhos) que representam uma linha independente de desenvolvimento. Quando você deseja adicionar um novo código a um repositório colaborativo, é recomendado criar seu novo código em uma nova "*branch*".

Para listar todas branches locais existentes:

    git branch

Para listar todas as *branchs* remotas existentes:

    git branch -a

Para alternar entre *branches* ou criar uma nova *branch* a partir de uma existente, utilize o git checkout.

## Alternando entre diferentes branches: git checkout

“*Checkout*” é o ato de alternar entre diferentes versões de um repositório. O comando git checkout para dois propósitos principais: alternar entre *branches* e criar uma nova *branch* a partir de outra.

Para alternar entre *branches*:

    git checkout nome-da-branch

Para criar uma nova *branch* a partir de outra:

    git checkout -b nova-branch-a-partir-de-outra

Se você tem alterações não salvas na sua *branch* original, ao criar uma nova *branch*, estas alterações farão parte da nova *branch*.

## Salvando mudanças no repositório: git add e git commit

Quando você tem um repositório clonado ou inicializado, é possível confirmar as alterações que você faz em arquivos. As etapas exemplificam adicionar e salvar mudanças em um repositório:

* Altere os arquivos necessários

* git add NomeDoArquivo.js para adicionar um arquivo ou git add . para adicionar todos os arquivos alterados na área de armazenamento temporário do repositório

* Crie uma nova confirmação com uma mensagem descrevendo o trabalho realizado na confirmação:

    git add . 
    git commit -m "add Issue #5"

Depois de executar estes passos, seu repositório agora terá os arquivos alterados adicionados ao histórico e rastreará futuras atualizações nos arquivos.

## Colaboração de repositório local para repositório remoto: git push

Se você usou o comando git clone para inicializar um repositório local, seu repositório já está configurado para colaboração remota. git clone configurará automaticamente seu repositório com um controle remoto apontado para o URL do Git do qual você o clonou. Isso significa que, uma vez que você faça alterações em um arquivo e as confirme, poderá fazer git push dessas alterações no repositório remoto.

    git push origin issue-5

IMPORTANTE: É recomendado, antes de fazer um git push, sempre garantir que sua branch local esteja atualizada, buscando a cópia do repositório central com git pull antes de enviar as modificações.

## Mesclando uma branch na outra: git merge

O comando git merge permite pegar as *branches* independentes de desenvolvimento criadas por git branch ou git checkout e integrá-las em uma única *branch*.

Antes de executar uma mesclagem, há algumas etapas de preparação a serem seguidas para garantir que a mesclagem ocorra sem problemas:

* Verifique se a filial receptora e a filial mesclada estão atualizadas com as últimas alterações remotas. Alterne para a *branch* a mesclada, a que fornecerá os arquivos para a *branch* receptora, com git checkout.

* Atualize a *branch* local com as alterações mais recentes da *branch* remota com git pull.

* Volte novamente para a *branch* receptora com git checkout.

* Agora mescle na *branch* receptora a *branch* mesclada:

    git merge branch-a-ser-mesclada

### Resolvendo conflitos durante a mesclagem de branches

Ao mesclar uma *branch* com outra, nem sempre a mesclagem dos arquivos acontece de forma correta. Ao depender do código de cada *branch*, a mesclagem pode gerar conflitos, o Git não é capaz de fazer a mesclagem automaticamente.

Exemplo de conflito ao mesclar *branches*:

    git merge branch-a-ser-mesclada
    Auto-merging index.html
    CONFLICT (content): Merge conflict in Server.js
    Automatic merge failed; fix conflicts and then commit the result.

BOOM 💥. Um conflito aparece. Obrigado Git por nos informar sobre isso!

Resolver conflitos é fácil. Abra os arquivos com conflitos e procure pelas marcações que indicam onde você deve atuar:

    <p>
    <<<<<<< HEAD
    this is some content to mess with
    content to append
    =======
    totally different content to merge later
    >>>>>>> branch-a-ser-mesclada
    </p>

Podemos ver algumas novas adições estranhas ao código

    <<<<<<< HEAD
    =======
    >>>>>>> branch-a-ser-mesclada

Pense nessas novas linhas como “divisores de conflito”. A linha ======= é o "centro" do conflito. Todo o conteúdo entre o centro e a linha <<<<<<< HEAD é o conteúdo existente na branch atual para o qual a referência **HEAD** está apontando (*Current change*). Como alternativa, todo o conteúdo entre o centro e >>>>>>> branch-a-ser-mesclada é o conteúdo presente em nossa branch a ser mesclada (*Incoming Change*).

Para resolver o conflito, basta remover todos os divisores de conflito. O conteúdo modificado deve se parecer com:

    <p>
    this is some content to mess with
    content to append
    totally different content to merge later
    </p>

Você pode optar por aceitar o código vindo, manter o atual ou mesclar os dois.

Após resolver todos os conflitos, salve os arquivos, e se necessário, salve-os no repositório local e os publique no repositório remoto com a sequência git add, git commite git push.
>  Para saber mais sobre [Github](https://github.com/), consulte o post [Compartilhando códigos no GitHub](https://medium.com/@dnvtrn/compartilhando-c%C3%B3digos-no-github-df450d2c8a25)
>  Para saber mais sobre projetos Open Source, consulte o post [Contribuindo para projetos Open Source](https://medium.com/@dnvtrn/contribuindo-para-projetos-open-source-5453686f8d8d)
