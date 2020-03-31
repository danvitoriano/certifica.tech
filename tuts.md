# Publicando projetos no Firebase

## Configuração de um projeto com HTML, CSS e JavaScript

![](https://cdn-images-1.medium.com/max/3200/1*B0Av_NnFrCKsyC7gN94ytg.png)

Projetos do **Firebase** são contêineres para seus apps ou web aps.

Apps compartilham recursos como o *Database* e o *Analytics* em tempo real, ou apenas utilizam o recurso de hospedagem *cloud* remoto possibilitando o acesso de interfaces ou APIs através de uma URL pública.

### Configurando um projeto remoto no Firebase Console

Para utilizar o Firebase, você precisa ter uma conta **Google** ativa. Se você utiliza, por exemplo, o Gmail ou Google Drive, você já tem uma conta Google.

 1. Acesse [https://console.firebase.google.com/](https://console.firebase.google.com/) e faça o login com sua conta.

 2. Clique em **Criar um projeto** ou **Adicionar Projeto**.

 3. Na próxima tela, informe o nome do projeto e clique em Continuar. Ex.: *negociacoes*. Caso o nome já exista, será gerado um código aleatório ao final do nome do projeto.

 4. O próximo passo é opcional, você escolhe se deseja adicionar o Google Analytics para receber métricas da sua aplicação. Ao optar pelo uso, você deverá informar na próxima tela a conta do Analytics a ser vinculada.

Com estes passos, o Firebase criará seu projeto e alocará os recursos de *cloud* necessários. Quando visualizar a mensagem "Seu novo projeto está pronto", clique em Continuar.

### Instalando a Firebase CLI

É possível instalar a Firebase CLI por meio de um método compatível com seu sistema operacional, nível de experiência e/ou caso de uso. Seja qual for o modo de instalação da CLI, você terá acesso às mesmas funcionalidades e ao comando firebase.

Consulte documentação oficial e instale a versão adequada:
[**Material de consulta sobre a Firebase CLI**
*A Firebase CLI ( GitHub) oferece uma série de ferramentas de gerenciamento, visualização e implantação para projetos do…*firebase.google.com](https://firebase.google.com/docs/cli?hl=pt-br#install_the_firebase_cli)

### Inicializando seu projeto

Faça login no firebase com suas credenciais para gerar um token de autenticação:

    firebase login:ci

Armazene o token em um lugar seguro pois você vai usá-lo em todos os comandos.

Execute o seguinte comando na raiz do diretório do projeto local para conectá-lo ao do Firebase:

    firebase init --token <seu-token>

Durante a inicialização do projeto, siga estas etapas dos prompts da Firebase CLI:

 1. Pressione a tecla *Espaço* para configurar o Hosting.

 2. Selecione o projeto do Firebase criado anteriormente no Console para conectar ao diretório do seu projeto local. Escolha "*Use an existing project*".

 3. Especifique um diretório para usar como diretório raiz público. Ex.: a pasta *client*

 4. Ao ser questionado sobre configurações de Single Page Application (*Configure as a single-page app (rewrite all urls to /index.html)?*), responda sim "y".

 5. Se o arquivo index.html já existir, responsa "N" para não sobrescrevê-lo.

Após seguir estes passos, deverá ter sido criado o arquivo de configurações firebase.json e o diretório da ferramenta. Estes arquivos devem ser incluídos no seu repositório remoto, por exemplo, no Github.

### Publicando o projeto no seu site Firebase Cloud Hosting

Se o seu projeto possui algum processo de *build*, como por exemplo, o uso de **Babel** e **WebPack**, é neste momento que você deve gerar a versão a ser colocada em produção. Por exemplo, rode o comando:

    npm run build

Para implantar no seu site, execute o seguinte comando a partir da raiz do diretório local do seu projeto:

    firebase deploy --token <seu-token>

Este comando implanta uma **versão** nos sites do *Hosting* padrão do projeto do Firebase:

* projectID.web.app

* projectID.firebaseapp.com

Caso você receba um erro 503 ao publicar, vá ao Firebase Console na web, escolha o seu projeto, vá no menu *Authentication*, e na aba Usuários, autorize a conexão de usuários por email e senha.

### Testando seu hosting com sucesso

No Firebase Console da web, vá ao menu *Hoisting*, e escolha uma das URLs para acessar o projeto que você fez o deploy através da Firebase CLI.

Se o seu deploy foi feito com sucesso, você visualizará seu projeto na URL configurada.
