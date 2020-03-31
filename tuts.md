# Compartilhando códigos no GitHub

## Como utilizar a plataforma de repositórios remotos [GitHub](http://github.com/).

![GitHub é um dos sites mais populares para desenvolvimento remoto](https://cdn-images-1.medium.com/max/3760/1*QUNxvPVwYt8-yXTgXdTZiw.jpeg)

## Criado para desenvolvedores

O [**GitHub](http://github.com/)** é uma plataforma de desenvolvimento remoto. Do [código aberto](https://github.com/open-source) aos [negócios](https://github.com/business) , você pode hospedar e revisar códigos, gerenciar projetos e criar software junto a milhões de desenvolvedores.

Sua equipe pode criar processos de revisão que melhoram a qualidade do seu código e se encaixam no seu fluxo de trabalho.

As solicitações de "***Pull Request*"** são fundamentais para a maneira como as equipes revisam e aprimoram o código no GitHub. Desenvolva projetos, proponha novos recursos e discuta detalhes da implementação antes de alterar seu código-fonte.

No GitHub você pode centralizar o código do seu site, aplicativo ou software, o mantendo privado apenas para sua equipe ou público, para que seja mantido e melhorado por outros desenvolvedores. É o que chamamos de ***Open Source***.
>  *Para saber mais sobre projetos Open Source, consulte o post [**Contribuindo para projetos Open Source](https://medium.com/@dnvtrn/contribuindo-para-projetos-open-source-5453686f8d8d)***
>  *Para saber mais sobre tópicos relacionados à ferramenta de versionamento de código Git, consulte o post [**O que você precisa saber sobre Git](https://medium.com/@dnvtrn/o-que-voc%C3%AA-precisa-saber-sobre-git-28b37c43ed30)***

## Criando uma conta no GitHub

Acesse a página principal do GitHub e preencha o cadastro escolhendo um nome de usuário. Após seu cadastro efetivado, você terá um perfil no GitHub para criar seus repositórios (projetos) ou fazer uma cópia de outros projetos ("*forkar*"). No seu perfil, é possível acompanhar suas contribuições:

![Exemplo de perfil no GitHub](https://cdn-images-1.medium.com/max/2434/1*aqpuHyYRhBdLj7Aho0v9nQ.png)

## Criando um novo repositório

Você pode criar um novo repositório em sua conta pessoal ou em qualquer organização em que tenha permissões suficientes.

Dica: Os proprietários podem restringir as permissões de criação de repositório em uma organização. Para obter mais informações, consulte [Restringindo a criação de repositório em sua organização](https://help.github.com/en/enterprise/2.13/user/articles/restricting-repository-creation-in-your-organization).

 1. No canto superior direito de qualquer página, clique em **Novo repositório** .

![](https://cdn-images-1.medium.com/max/2000/0*FRyX7qMRgNBVbW9E.png)

2. No menu suspenso *Owner*, selecione a conta na qual você deseja criar o repositório.

![](https://cdn-images-1.medium.com/max/2000/0*YgdVCGRQ5_WXB9KI.png)

3. Digite um nome para seu repositório e uma descrição opcional.

![](https://cdn-images-1.medium.com/max/2000/0*s2Fb7ypnoi_g9k1w.png)

4. Escolha tornar o repositório público ou privado. Os repositórios públicos são visíveis ao público, enquanto os repositórios privados são acessíveis apenas a você e às pessoas com quem você os compartilha. Para obter mais informações, consulte [Configurando a visibilidade do repositório](https://help.github.com/en/enterprise/2.13/user/articles/setting-repository-visibility).

![](https://cdn-images-1.medium.com/max/2000/0*6wusaLy445brhdTN.png)

Há vários itens opcionais com os quais você pode preencher previamente seu repositório. Se você estiver importando um repositório existente para o GitHub, não escolha nenhuma dessas opções, pois poderá introduzir um conflito de mesclagem. Você pode optar por adicionar novos arquivos usando a linha de comando posteriormente.

* Você pode criar um README, que é um documento que descreve seu projeto. Para mais informações, consulte [Sobre os READMEs](https://help.github.com/en/enterprise/2.13/user/articles/about-readmes).

* Você pode criar um arquivo *.gitignore* , que é um conjunto de regras para ignorar. Para mais informações, consulte [Ignorando arquivos](https://help.github.com/en/enterprise/2.13/user/articles/ignoring-files) .

5. Quando terminar, clique em **Criar repositório**. Agora você tem um projeto (repositório) no GitHub e está pronto para clonar na sua máquina através do Git.

Além de criar seus próprios repositórios, você pode fazer uma cópia de repositórios alheios (*forkar*) e contribuir em projetos remoto de terceiros.

## Fazendo Fork de repositórios remotos

Ao fazer um *fork*, cria-se uma cópia do código fonte de um projeto hospedado no GitHub para a sua conta. Você pode modificar esta cópia à vontade sem afetar o código fonte original.

Quando quiser integrar suas modificações ao código original, basta fazer um ***Pull Request***. Para saber mais sobre este processo, leia o post [**Contribuindo para Projetos Open Source](https://medium.com/@dnvtrn/contribuindo-para-projetos-open-source-5453686f8d8d)**

Para fazer o *fork*, você deve primeiro logar-se na sua conta do Github e em seguida acessar o repositório que deseja fazer uma cópia. Na página do repositório, clique no botão “*Fork*” localizado no canto superior direito da página:

![](https://cdn-images-1.medium.com/max/2000/0*kz28aja2sRIDBbvV)

Na tela que se abrirá, selecione a sua conta do GitHub para iniciar o *fork* do repositório. A cópia pode levar alguns minutos para completar. Enquanto isso, deverá ser exibida uma imagem semelhante a esta:

![](https://cdn-images-1.medium.com/max/2000/0*v4GF1v0499MiKFDx)

Assim que o *fork* do repositório tiver sido concluído, você será redirecionado automaticamente para a cópia do repositório na sua conta do GtiHub. Você pode confirmar que a cópia foi feita corretamente verificando o status do repositório no canto superior esquerdo da página. O status conterá a mensagem: “*forked from danvitoriano/negociacoes*”.

Pronto! Você já tem a sua própria versão do código fonte de um repositório do GitHub.
>  *Para saber como editar seus códigos de repositórios do GitHub na sua máquina local, consulte o post [**O que você precisa saber sobre Git](https://medium.com/@dnvtrn/o-que-voc%C3%AA-precisa-saber-sobre-git-28b37c43ed30)** e aprenda mais sobre tópicos relacionados à ferramenta de versionamento de código.*
>  *Para saber mais sobre projetos Open Source, consulte o post [**Contribuindo para projetos Open Source](https://medium.com/@dnvtrn/contribuindo-para-projetos-open-source-5453686f8d8d)***
