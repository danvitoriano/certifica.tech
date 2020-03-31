# Contribuindo para projetos Open Source

## Como utilizar o GitHub para ajudar em projetos de terceiros

![Bem vindos aos projetos comunitários e de código aberto](https://cdn-images-1.medium.com/max/2400/1*mrkKIvrZgEcN4qmwQEjGiQ.jpeg)

Para contribuir com um projeto open source é muito fácil.

Este artigo demonstra situações de contribuição para projetos de código aberto e compartilhado na plataforma de desenvolvimento remoto [GitHub](https://github.com/), porém, os conceitos podem ser aplicados em outras plataformas como [BitBucket](https://bitbucket.org/) e [GitLab](https://about.gitlab.com/).
>  *Para saber mais sobre [Github](https://github.com/), consulte o post [Compartilhando códigos no GitHub](https://medium.com/@dnvtrn/compartilhando-c%C3%B3digos-no-github-df450d2c8a25)*
>  *Para saber mais sobre tópicos relacionados à ferramenta de versionamento de código Git, consulte o post [O que você precisa saber sobre Git](https://medium.com/@dnvtrn/o-que-voc%C3%AA-precisa-saber-sobre-git-28b37c43ed30)*

Tópicos deste artigo:

* Escolhendo uma Issue

* Compartilhando seu progresso com comentários

* O quadro de Projeto

* Criando uma branch para minha Issue

* Passos para criar branch da sua Issue

* Pull Request: enviando sua branch para a master

* Passos para abrir sua Pull Request

* Code Review: código revisado por outros contribuidores

* Mesclando uma branch para a master

Siga os passos seguintes e ajude a melhorar aplicações de código compartilhado Open Source.

## Escolhendo uma Issue

O primeiro passo é escolher uma *Issue* aberta e atribuí-la para você.

A *Issue* descreve, por exemplo, uma necessidade de incrementação “*enhanhecement*” ou correção “*bug*” do código.

Vá até a aba Issues no Github do nosso projeto e escolha uma dentre as Issues abertas não assumidas por alguém.

![A aba Issues no GitHub](https://cdn-images-1.medium.com/max/2062/1*BsIowjdh-JNFINCsM7LP5A.png)

Para ajudar ou assumir uma *Issue*, é interessante deixar um comentário manifestando interesse ao usuário dono do repositório, isto é, a pessoa que tem permissão de escrita.

Após a manifestação de interesse no comentário, a pessoa proprietária do repositório com permissão de escrita, fará a atribuição inserindo o seu nome de usuário no Github no campo Assigned. A partir deste momento, esta Issue é de sua responsabilidade, e você pode contribuir com mais efetividade, ganhando ainda a ajuda de outras pessoas.

Para contribuir, não é obrigatório ter uma *Issue* designada a você. Através da discussão nos comentários é possível se organizar e contribuir.

## Compartilhando seu progresso com comentários

Compartilhe o progresso do seu trabalho com comentários direto da *Issue*. Toda a discussão entre as pessoas da *Issue*, e até mesmo comentários de contribuidores de outras *Issues* devem ser adicionados na para que todos possam acompanhar, discutir e ajudar publicamente. Isso é fundamental para um projeto *open source*.

![Exemplo de comentários em uma Issue](https://cdn-images-1.medium.com/max/2000/1*imO3dGK8GbI14kRAQJAc6w.png)

## O quadro de Projeto

O Github oferece uma função muito interessante em todos os seus repositórios. A aba Projetos simula um quadro Kanban onde é possível acompanhar o progresso e evolução das Issues em andamento e abertura e revisão de Pull Requests.

Ao assumir uma *Issue*, você pode ir até a aba *Projects*, escolher um projeto (caso haja) e mover a *Issue* atribuída a você da coluna *To Do* para a coluna *In Progress*. Isso indica aos contribuidores do projeto que você já está trabalhando na *Issue* que assumiu.

![Exemplo de Projeto Kanban no GitHub](https://cdn-images-1.medium.com/max/2878/1*I_hb6lbKrzxtj_B6UQBBJg.png)

## Criando uma branch para minha Issue

O código principal de um projeto open source, geralmente, está na branch master. Ela será o repositório central onde todo o conteúdo pronto e revisado pelos contribuidores do projeto permanecerá.

Ao assumir uma *Issue* dando *Assigned* para você, e a colocando em *In Progress* na aba *Projects*, o próximo passo é criar uma branch a partir da master com o nome da sua *Issue*. Todo o código que vai solucionar o problema da sua *Issue* ficará na branch de mesmo nome, para que ao final você abra uma *Pull Request* para a master, com a finalidade de mesclarmos os códigos e a nossa aplicação *open source* receba sua contribuição de forma definitiva na master.
>  *Para saber mais sobre *Branches*, *Merge*, *Pull Request* e outros tópicos relacionados ao Git, consulte o post [O que você precisa saber sobre Git](https://medium.com/@dnvtrn/o-que-voc%C3%AA-precisa-saber-sobre-git-28b37c43ed30)*

### Passos para criar branch da sua Issue

 1. Crie uma branch a partir da master.

 2. Sincronize sua branch master local com as atualizações mais recentes do repositório remoto fazendo git pull origin master.

 3. Crie a branch para sua *Issue* com o comando git checkout -b issue-numero, ou seja, o nome da sua branch deve ser o numero da sua Issue no Github.

 4. Pronto, você já está na branch da sua issue e já pode resolver seu código. Lembre sempre de publicar suas atualizações e salvá-las no repositório remoto com a sequência de comandos: git add ., `git commit -m "Descrição do que está sendo salvo" e "git push origin issue-numero".
>  *Para saber mais sobre *Checkout*, *Add*, *Commit*, *Push* e outros tópicos relacionados ao Git, consulte o post [O que você precisa saber sobre Git](https://medium.com/@dnvtrn/o-que-voc%C3%AA-precisa-saber-sobre-git-28b37c43ed30)*

## Pull Request: enviando sua branch para a master

Ao finalizar as alterações e adições no código da sua *branch* que resolverá a *issue* que você assumiu, é preciso abrir uma Requisição de Atualização, chamada popularmente de “*Pull Request*”. Este processo submete o código de uma *branch* para ser mesclado na *branch* master, a *branch* que reflete o código mais atualizado, correto e aprovado por todos os contribuidores, isto é, o código que deve estar em produção e ser exibido ao usuário final.

Este processo pode ser feito por comandos via terminal, mas é mais fácil fazer este processo pelo site do Github.

### Passos para abrir sua Pull Request

 1. Acesse o repositório do projeto e altere para a *branch* correspondente à sua issue

 2. Clique no botão *New Pull Request*

 3. Agora é preciso comparar as duas versões: a sua *branch* com a master

 4. Caso apareça a mensagem “*Can’t automatically merge*”, é preciso voltar ao terminal, buscar as atualizações mais recentes da master com git pull origin master e mesclar as atualizações com a sua *branch* com git merge master, desde que você já esteja na sua *branch*. Caso haja, resolva os conflitos, salve as alterações e publique novamente no repositório do Gihtub com git push origin issue-numero. Repita os passos anteriores até que seja possível a mesclagem automática.

 5. Caso apareça a mensagem “*Able to merge*”, sua *Pull Request* está pronta para ser mesclada automaticamente, isto é, não há conflitos, e os contribuidores poderão revisar seu código após a abertura da solicitação.

 6. Verifique a comparação entre os dois códigos através da diferenciação do que você está adicionando ou removendo em casa arquivo.

 7. No título informe o nome e número da sua *issue*. Descreva resumidamente as alterações que sua *Pull Request* propõe para solucionar a *issue* e informe o número da *issue* na descrição usando o código markdown # + o número da *issue* para que a sua *Pull Request* seja linkada com a aba *Projects* e possa aparecer como disponível para revisão.

 8. Após a descrição e revisão, clique no botão *Create pull request*.
>  *Para saber mais sobre *Pull Request *e outros tópicos relacionados ao Git e Github, consulte o post [O que você precisa saber sobre Git](https://medium.com/@dnvtrn/o-que-voc%C3%AA-precisa-saber-sobre-git-28b37c43ed30)*

![Exemplo de Pull Request no GitHub](https://cdn-images-1.medium.com/max/2100/1*lCsoa0GZQVL9b5i_bqnl8g.png)

## Code Review: código revisado por outros contribuidores

Quando uma *Pull Request* está aberta, todos podem contribuir com a sua revisão. Basta adicionar comentários apontando erros, pontos de atenção, sugestões ou validando o código, aprovando a liberação para mesclagem.

## Mesclando uma branch para a master

Se a proposta de alteração do código da master for aprovada pelos contribuidores e pela pessoa com permissão de escrita no repositório, sua *branch* será mesclada com a master, ou seja, sua *Pull Request* será aprovada.

Automaticamente ela será listada como *Merged*. Após este processo, você pode apagar sua *branch*, pois o código já está na *branch* principal, disponível para que todos atualizem seus repositórios locais, além de publicá-la em produção.
>  *Fonte: 
[Univali](https://github.com/UNIVALI-LITE/Portugol-Studio/wiki/Fazendo-um-Fork-do-reposit%C3%B3rio)
[GitHub Help](https://help.github.com/pt)*
>  *Para saber mais sobre *Pull Request *e outros tópicos relacionados ao Git e Github, consulte o post [O que você precisa saber sobre Git](https://medium.com/@dnvtrn/o-que-voc%C3%AA-precisa-saber-sobre-git-28b37c43ed30)*
>  *Para saber mais sobre [Github](https://github.com/), consulte o post [Compartilhando códigos no GitHub](https://medium.com/@dnvtrn/compartilhando-c%C3%B3digos-no-github-df450d2c8a25)*
