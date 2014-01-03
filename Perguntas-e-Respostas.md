### <a name="safe"/> O Lantern é seguro para eu usar?

O Lantern se esforça para garantir que seus usuários estão seguros, mas existem casos que nós não podemos proteger, então os usuários precisam estar cientes de como eles podem usar o Lantern com segurança. Para usuários em regiões com cesura é extremamente importante que você apenas escolha amigos do Lantern em quem você realmente confia. Seu tráfego de internet vai rodar através desses companheiros. Se você adicionar pessoas que você não confia, você corre o risco de adicionar um usuário que pode monitorar você. Então **apenas adicione amigos no Lantern que você realmente confia**. Além disso, **o Lantern também vai enviar seu tráfego de amigos até 4 níveis a partir de você**, ou seja, amigos de amigos de amigos de amigos. Nós fazemos isso para construir uma rede mais conectada e escalável, como os usuários muitas vezes não conhecem diretamente ninguem no outro lado da divisão da censura. Contudo, todo link adicional na corrente expõe você a um usuário cada vez menos confiável (i.e. você no amigo do seu amigo menos do que você confia no seu amigo). Sempre tenha em mente que **o Lantern é uma ferramenta que oferece acesso, não é uma ferramenta que previne monitoramento**.

**Lantern não é uma ferramenta de anonimato**. Se você precisa que os sites que você visita não aprendam seu endereço IP ou sua localização física (eles normalmente podem, o que pode ser uma surpresa pra você), ou você não pode arriscar que monitores de rede sejam capazes de determinar quais sites você visita, nós recomendamos que use [Tor](https://www.torproject.org). Tor é um excelente software, e nós nos comunicamos com o time do Tor frequentemente. De novo, o propósito do Lantern é acesso. O propósito do Tor é anonimato.

Um último ponto sobre segurança: Com qualquer ferramenta, incluindo ambos Lantern e Tor, você não deve postar conteúdo sensível em um site que está hospedado em uma região onde o Governo persegue pessoas que postam esse tipo de conteúdo, especialmente se você mora lá. Isso porque uma rede global de observação como o Governo pode identificar você como o usuário que enviou o conteúdo e pode geolocalizar você.

### <a name="no-connections"/> Como o Lantern funciona se eu não conseguir alcançar nenhum usuário dando acesso?

Para ajudar a inicar a rede Lantern nós montamos Servidores Lantern na Nuvem ([[Lantern Cloud Servers]]). Eles servem como reserva para o tráfego quando nenhum outro usuário está disponível para dar acesso. Nossa esperança é que conforme a rede Lantern cresça, existirá usuários suficientes dando acesso que nós precisaremos cada vez menos servidores reservas.

Nosso outro plano é dar às pessoas uma opção de financiar Servidores Lantern na Nuvem adicionais dedicados para elas e para seus amigos. Nós também esperamos fazer parcerias com empresas que tem capacidade computacional sobrando e queira ajudar a liberdade na internet doando servidores para a rede Lantern.


### <a name="compare"/>Como o Lantern se compara com outras ferramentas?

O objetivo do Lantern é dar aos usuários acesso e ser ao mesmo tempo rápido, seguro e fácil de usar. [Tor] (https://www.torproject.org) é uma das ferramentas mais populares nessa área com o foco primário em anonimato. Para aqueles que não ligam em ser completamente anônimo, o Lantern oferece uma alternativa com acesso mais rápido. Comparado com outras ferramentas que visam acesso (GoAgent, Freegate, Ultrasurf, Psiphon, Autoproxy) a força do Lantern é a facilidade com a qual ele pode ser instalado e usado, assim como sua arquitetura de rede peer-to-peer confiável desenhada para escalar na presença de censuras. **O uso do relacionamento confiável do mundo real no Lantern também faz dele extremamente eficaz na tentativa de bloqueio.**

Por padrão, o Lantern roda como um sistema proxy, o que significa que navegadores no seu computador irão usá-lo automaticamente, sem que você precise mudar nenhuma das suas configurações. Algumas outras ferramentas só funcionam com um navegador específico, ou necessitam uma configuração complexa.

Outro aspecto único no projeto do Lantern é a sua arquitetura peer-to-peer, que permite que os dados venham de vários computadores ao mesmo tempo, ao invés de apenas um único servidor. Arquitetura peer-to-peer também permitem as redes sejam escaláveis para milhões de usuários numa fração do custo de arquiteturas mais centralizadas.

Recentemente, o time do Lantern contribuiu para o [uProxy](https://uproxy.org), um novo esforço patrocinado pela Google Ideas. Enquanto há algumas semelhanças entre os dois, também há importantes diferenças. Para um, o Lantern é um aplicativo independente que fica rodando em segundo plano, enquanto o uProxy é uma extensão do navegador, e pede para que um único amigo seu sirva de proxy para você, enquanto com o Lantern você pode ter muitos companheiros dando acesso à você ao mesmo tempo. Outra diferença é que o Lantern permite que amigos de amigos até 4 níveis de você se conectem com outros, enquanto que o uProxy apenas permite amigos diretos. Finalmente, para ser mais rápido e mais resistente a bloqueios, por padrão os proxies do Lantern acessam apenas um conjunto específico de sites que você configura (veja abaixo), enquanto o uProxy redireciona o tráfego para todos os sites através do seu amigo enquanto você estiver com isso habilitado.


### <a name="proxy-list"/> Por que o Lantern não acessa todos os sites por padrão?

Por padrão, o Lantern apenas oferece acesso a uma lista já conhecida de sites bloqueados. Nós fazemos isso por algumas razões. Primeiro, é sempre mais rápido ir para um site diretamente do que através de um proxy independentemente de quão rápido ou eficiente esse proxy é. Então, sites que não estão bloqueados serão mais rápidos se eles forem alcançados diretamente ao invés de serem acessados pelo Lantern.

A segunda razão é que usar o proxy para acessar sites que não são bloqueados libera recursos da rede do Lantern. Devido a rede do Lantern como um todo não ter que carregar o fardo de prover acesso a sites não bloqueados, ele pode usar esses recursos para oferecer um melhor acesso a sites bloqueados.


###<a name="trust-network"/> Como a rede confiável funciona? O que acontece quando eu adiciono alguém como amigo no Lantern?

O Lantern é feito em uma rede confiável. Essa rede conecta pessoas que confiam umas nas outras para compartilhar conexões de internet. Quando você e outro usuário são amigos no Lantern, vocês podem usar vocês mesmos como proxy com o Lantern. Contudo, se o Lantern so funcionasse com amigos diretos, usuários muitas vezes não teriam proxies disponíveis quando nenhum dos seus amigos estivessem online dando acesso.

Para atenuar isso, usuários do Lantern obtendo acesso podem descobrir um subconjunto dos usuários dando acesso até 4 níveis a partir deles na rede confiável. Então por exemplo, se você usar o Lantern para obter acesso, o irmão do parceiro da mãe do seu amigo pode terminar usando você como proxy do Lantern para trafegar. Se essa pessoa é um censor, ela pode bloquear ou analisar o seu tráfego. Por outro lado, se você usar o Lantern para ler ou postar alguma coisa privada ou sensível, vai parecer que o tráfego está vindo pelo computador dela. Por causa disso, todo mundo rodando o Lantern deve ser amigo apenas de pessoas em quem eles confiam, e **apenas usar o Lantern como tráfego que não é privado ou sensível**.

Adicionando apenas pessoas que você confia, você proteja não apenas a si mesmo, como também seus amigos, os amigos deles, os amigos dos amigos deles e assim por diante. E permitindo que usuários descubram um subconjunto de usuários mais longe deles na rede confiável, o Lantern aumenta a quantidade de proxies disponíveis enquanto mantém a resistência a bloqueios.

Em qualquer cenário, no entanto, **você deve aprovar explicitamente cada usuário que terá acesso ao proxy por você**. Você está sempre no controle. O Lantern nunca vai enviar o seu tráfego através de nenhum ponto, independentemente de quão longe eles estão na rede confiável, sem sua aprovação explícita.


### <a name="howto"/> Como eu baixo o Lantern?

O Lantern ainda está na versão beta privado. Você pode solicitar um convite e updates [aqui](https://getlantern.us2.list-manage.com/subscribe/post?u=0ac18298d5d0330dcda8f48aa&id=f06770f311).


### <a name="know"/> I live in an uncensored region and don't know anyone in a censored region. Can I still help?

Definitely! People in censored regions can still learn about you through your friends. So while you donʼt know anyone directly living in censored regions, your friends might, and the odds are even better that their friends might (and so on). If you keep Lantern running and adding the people you trust, eventually youʼll be connected with users who need access. **Thatʼs why itʼs really important to invite your friends to Lantern**. It maximizes the likelihood that your social network will reach into censored regions so you can help.

### <a name="gmail"/>Is a Gmail account required to use Lantern?
Yes. Lantern requires a Gmail or Google Apps e-mail address. For details, see [Why Does Lantern Require a Google Login?](https://github.com/getlantern/lantern/wiki/%5Bdevelopers%5D-Questions-and-Answers#-why-does-lantern-require-a-google-login-what-happens-with-the-generated-oauth-tokens).

### <a name="whattodo"/> OK, I've installed Lantern. Now what?

For users in uncensored regions, there are two basic things you can do once youʼve installed Lantern:

1. **Run Lantern as much as possible.**
1. **Add more users you trust as Lantern friends.**

Whenever you run Lantern, you create a new access point users in censored regions can use to access the open Internet. Remember, though, that only people in your Lantern network will be able to connect to you. Thatʼs why the second step is critical. The larger your Lantern network, the higher the odds youʼll provide access to users who need it. **So please invite as many trusted contacts as you can!**

### <a name="upgrade"/>How do I upgrade to a newer version of Lantern?

Please see [Upgrading to a New Version of Lantern](https://github.com/getlantern/lantern/wiki/Upgrading-to-a-New-Version-of-Lantern).

### <a name="hackers"/> Will Lantern make my computer vulnerable to hackers?

Lantern takes a number of precautions to make sure users are safe. First, Lantern does not allow anyone it connects you to to read the contents of your computer. It simply allows you to share Internet connections. The data passing between you is encrypted so that no intermediaries (e.g. your government or Internet service provider or theirs) can read it. Lantern also requires mutual authentication for all connections, which means that Lantern will only allow users to connect to you that it can verify are in your Lantern network, and not just anyone.


### <a name="is-lantern-free"/> Is Lantern free? Will running it cost me anything?

Lantern is free as in money and as in freedom: free to use, modify, and redistribute in accordance with its [license](https://raw.github.com/getlantern/lantern/master/LICENSE).

If your Internet connection is limited, then giving access through Lantern will count against your limit. We recommend using Lantern with unlimited Internet connections.


### <a name="contributing"/> Como eu posso contribuir?

Por favor veja como [[Se envolver|Se-Envolva]].

### <a name="notworking"/> O Lantern não está funcionando pra mim. Qual o problema?

Existe uma incompatibilidade conhecida entre o Lantern e o Proxy Switchy. Se você tem o Proxy Switchy instalado, você pode temporariamente desabilitar ele para usar o Lantern.


### <a name="more"/> Eu tenho mais dúvidas, onde eu vou?

Se você tem mais dúvidas técnicas, por favor veja a página [Developers Q&A](https://github.com/getlantern/lantern/wiki/%5Bdevelopers%5D-Questions-and-Answers). Também sinta-se livre para postar no [fórum do usuário](https://groups.google.com/group/lantern-users-en) ou no [fórum dos desenvolvedores](https://groups.google.com/group/lantern-devel).