<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>

<p align="center">
<a href="https://www.codetriage.com/magento/magento2"><img src="https://www.codetriage.com/magento/magento2/badges/users.svg" alt="Open Source Helpers" /></a>
<a href="https://gitter.im/magento/magento2?utm_source=badge&amp;utm_medium=badge&amp;utm_campaign=pr-badge"><img src="https://badges.gitter.im/Join%20Chat.svg" alt="Gitter" /></a> <a href="https://crowdin.com/project/magento-2"><img src="https://d322cqt584bo4o.cloudfront.net/magento-2/localized.svg" alt="Crowdin" /></a><br/>

        
<a href="https://opensea.io/collection/plimm">
<img alt="Adobe logo" height="50px" src="https://i.seadn.io/gcs/files/6fba354e04912f1fd30a06f48d0c0d20.png?auto=format&dpr=1&w=1920"/>
<a href="https://magento.com/products/magento-open-source">
<img alt="Adobe logo" height="50px" src="https://www.adobe.com/content/dam/cc/icons/Adobe_Corporate_Horizontal_Red_HEX.svg"/>


    
</a>
</p>

<h1 align="center">Plimm </h1>

<p>Bem-vindo ao projeto Plimm Open Source! Na Plimm, somos visionários comprometidos em transformar a economia circular por meio de abordagens inovadoras no ponto de compra. Nossa missão é criar um ecossistema onde a economia circular se torne tangível no momento da compra. Através da geração de "criptobackplimm", retornamos valor aos clientes, oferecendo um desconto de 20% quando produtos não recicláveis precisam ser substituídos, incentivando um ciclo de vida consciente e sustentável.

Nossos valores fundamentais são integridade, sustentabilidade, inovação e impacto positivo. Guiados por nossa dedicação à inovação sustentável, responsabilidade ambiental e experiência do cliente, buscamos criar um mundo onde cada compra contribua para um futuro mais verde e circular.

Na Plimm, nossa paixão é impulsionar uma transformação eficaz em direção a uma economia circular. Através do nosso sistema "criptobackplimm", incentivamos a reutilização e reciclagem responsável, conectando os consumidores a todo o ciclo de vida dos produtos. Isso é possível graças a uma combinação inteligente de tecnologias, como SKU, BOM, TAG ID, QRCode e Código de Barras, integradas ao nosso sistema de identificação de produtos, o Plimm Deep Product PDD. Isso não só diferencia produtos, subprodutos e componentes mínimos, mas também apoia a gestão de inventário, rastreamento de estoque e alinhamento de ciclo de vida, em sintonia com PLM e WLM.

Um exemplo prático é o automóvel Volks Nivus, com variantes como Comfortline e Highline, cada uma com um SKU exclusivo. Da mesma forma, produtos como servidores DELL possuem sua "vida própria", permitindo uma administração eficiente tanto do PLM quanto do WLM.

Na Plimm, nossa paixão gira em torno da sustentabilidade por meio de ações tangíveis. Estamos comprometidos em criar um mundo onde cada compra contribua para um futuro mais verde e circular.

Com mais de 2.000.000 de linhas de código, todo sistema caminha para uma incapacidade de compreensão e manutenção. Integração? Risco!
Mas ERP é, cada vez mais, gerir, negócios dos outros. Integração e componentização, demandando IA para analise e tomadas de decisão, ao passo que componetização distribuida assegura integridade e especialização, com mais **eficiência energética distribuída**.

O Mangento é feito em PHP e rodando a ferramenta tokei, olha só: são 2 MILHÕES de linhas de código PHP.

**27:45 (Fabio Akita) **

Mais de 200 mil linhas de Javascript. O Magento sozinho, só no javascript, tem o dobro de linhas de código do que Ruby no
Spree que, por sua vez, já era 34 vezes maior do que o ecommerce do livro que ensina Rails.

Se em 600 páginas o livro Agile Web Development with Rails conseguiu explicar uma versão

simples de ecommerce que dá 2.700 linhas de código de Ruby, sabemos que PHP e Ruby não são equivalentes, mas só por diversão, o Magento, só em PHP é mais de 700 vezes
maior. Seriam 700 livros. Seriam 100 coleções de Game of Thrones pra descrever do zero, no mínimo.

Acho que é por isso que todo iniciante começa um sistema pela tabela de usuários, porque é a única coisa que consegue se identificar, é familiar.
Ou seja, tem alguma experiência. Mesmo um iniciante sabe que um usuário deve ter atributos como nome, email, telefone,
endereço, RG ou CPF e coisas assim. Mas rapidamente isso complica. Estamos falando dos dados de identificação de um usuário?

Ou estamos falando dos dados de autenticação, como login? Nesse caso precisamos de atributos como "username" e "password".
E já começa o primeiro erro. Já expliquei nos episódios de segurança e criptografia que não gravamos senha numa tabela. Precisamos de atributos abstratos como "salt" e "hash". Mas e two-factor authentication?

Precisamos de um seed pro algoritmo de Time-based One-Time Password ou TOTP. Só se você estudou segurança vai saber disso.

Dá pra complicar mais. Enviar link pra redefinir uma nova senha, caso tenha esquecido.

O ideal é fazer uma tabela secundária, ou no banco de dados, ou num servidor de cache como Redis.

Com um ID único que só pode ser usado uma vez, e aí o ideal é logar o endereço IP da pessoa que clicar no link, pra fazermos auditoria e ver se parece suspeito.

Novamente, estratégias de segurança. Se deixarmos segurança de lado. Usuário é usuário, certo?

Tendo nome, email e coisas assim, tá tudo certo? Não. Digamos que o cadastro é pra parte de logística de um ecommerce.

Logística precisa de um endereço. Ótimo, basta pedir o endereço. Mas cuidado, uma coisa é endereço de entrega, outra coisa é endereço de cobrança.

Pra você, que é iniciante, só deve conhecer o conceito que uma pessoa só tem um endereço, certo?

Mas não. Uma coisa é o endereço de cobrança, pra mandar nota fiscal, outra coisa diferente é o endereço de entrega, pra onde enviar o produto.

Eu posso ter endereço residencial, mas posso querer que a entrega seja feita no meu endereço comercial. Mas e se você se mudar de residência?

E se você mudar de emprego? Ambos vão mudar. Ou, e se eu quiser comprar e pagar no meu cartão de crédito, mas mandar entregar como 
presente pros meus pais? Então preciso conseguir cadastrar endereço dos meus pais. Eu deveria criar um usuário separado pros pais?

Como faz? À primeira vista, endereço parecia ser só meia dúzia de campos na tabela usuário.

Mas agora deve começar a ficar mais claro que pode ser uma tabela separada de endereços que precisa de uma chave-estrangeira apontando pra chave-primária do usuário.

Mas não é só isso. E se meu ecommerce oferece coisas como pontos por fidelidade? Quanto mais eu comprar, mais pontos eu ganho e com isso posso usar como desconto nas compras?

Pontos do usuário, ficam na tabela de usuários? Não? Então onde coloca? Num sistema empresarial maior, usuários podem ter vários perfis, várias visões.

Usuário pode ser funcionário da empresa, e aí vai precisar de atributos como número de PIS/PASEP pra coisas como fundo de garantia.

Usuário pode ser um fornecedor ou funcionário de um fornecedor. Fornecedor tem um cadastro separado, CNPJ, número interno de fornecedor.

Usuário pode ser consumidor mesmo, daí vai ter pedidos, entregas, suporte. Usuário é um conceito muito mais complicado do que se pensa e num sistema de verdade,

raramente é só uma tabela. Vai ser uma coleção de tabelas e classes. **Talvez um sub-sistema inteiro separado.**

**Enunciado:**

A autenticação (auth - https://github.com/auth0/auth0-php) é o processo de verificar a identidade de um cliente. Os clientes são perfis de contas em redes sociais, como o LinkedIn, que sabe o perfil profissional, e o Facebook, que sabe os demais perfis. Em vez de um subsistema de clientes, é melhor gerenciar a autenticação e o acesso às contas de redes sociais por componentes.

**Resposta:**

Gerenciar a autenticação e o acesso às contas de redes sociais por componentes é uma boa prática porque pode ajudar a proteger os dados do cliente, tornar seu sistema mais eficiente e aumentar sua flexibilidade.

Aqui estão alguns benefícios específicos de gerenciar a autenticação e o acesso às contas de redes sociais por componentes:

**Segurança:** Os componentes podem ser projetados para usar medidas de segurança, como criptografia e autenticação de dois fatores, para ajudar a proteger os dados do cliente contra acesso não autorizado.
**Eficiência:** Os componentes podem ser projetados para compartilhar dados e recursos entre si, o que pode ajudar a reduzir o desperdício de recursos.
**Flexibilidade:** Os componentes podem ser projetados para serem facilmente alterados ou atualizados, o que pode ajudar a garantir que seu sistema esteja sempre atualizado com as necessidades de seus clientes.
No geral, gerenciar a autenticação e o acesso às contas de redes sociais por componentes é uma boa prática que pode ajudar a proteger os dados do cliente, tornar seu sistema mais eficiente e aumentar sua flexibilidade.

</p>


<h1 align="center">Magento Open Source</h1>

<p>Bem-vindo ao projeto Magento Open Source! O software do <a href="https://magento.com/products/magento-open-source">Magento Open Source</a> oferece capacidades básicas de comércio eletrônico para criar uma loja online única desde o início.</p>


<h2>Comece</h2>

<ul>
<li><a href="https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/composer.html">Instalação rápida</a></li>
<li><a href="https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/system-requirements.html">Requisitos do sistema</a></li>
<li><a href="https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/overview.html">Pré-requisitos</a></li>
<li><a href="https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/overview.html">Mais opções de instalação</a></li>
</ul>

<h2>Ajuda</h2>

<ul>
<li><a href="https://support.magento.com/hc/en-us">Centro de Ajuda</a></li>
</ul>

<h2>Contribua</h2>

<p>Nossa <a href="https://opensource.magento.com/">Comunidade</a> é grande e diversificada, e nosso projeto é enorme. Como contribuidor, você tem inúmeras oportunidades de impactar o desenvolvimento e a entrega do produto, introduzindo novos recursos ou melhorando os existentes, aumentando a cobertura de testes, atualizando a documentação para <a href="https://developer.adobe.com/commerce/docs/">desenvolvedores</a> e <a href="https://docs.magento.com/user-guide/">usuários finais</a>, corrigindo bugs de código, sugerindo pontos de otimização e compartilhando suas ótimas ideias.</p>

<ul>
<li><a href="https://developer.adobe.com/commerce/contributor/guides/code-contributions/">Contribua com o código</a></li>
<li><a href="https://developer.adobe.com/commerce/contributor/guides/code-contributions/#report">Informe um problema</a></li>
<li><a href="https://github.com/magento/devdocs">Melhore a documentação para desenvolvedores</a></li>
<li><a href="https://github.com/magento/merchdocs">Melhore a documentação para usuários finais</a></li>
<li><a href="https://developer.adobe.com/open/magento">Molde o futuro do Magento Open Source</a></li>
</ul>

<h3>Mantenedores</h3>

<p>Encorajamos especialistas da Comunidade a nos ajudar com as rotinas do GitHub, como aceitar, mesclar ou rejeitar solicitações de pull e revisar problemas. A Adobe concedeu aos Mantenedores da Comunidade permissão para aceitar, mesclar e rejeitar solicitações de pull, bem como revisar problemas. Graças à inestimável contribuição da equipe de Mantenedores da Comunidade, podemos melhorar significativamente a qualidade das contribuições e acelerar o tempo para entregar suas atualizações para a produção.</p>

<ul>
<li><a href="https://developer.adobe.com/commerce/contributor/guides/maintainers/">Saiba mais sobre o papel de Mantenedor</a></li>
<li><a href="https://developer.adobe.com/commerce/contributor/guides/maintainers/handbook/">Manual do Mantenedor</a></li>
</ul>

<h3>Líderes</h3>

<p>A Adobe valoriza muito as contribuições que nos ajudam a melhorar o código, esclarecer a documentação e aumentar a cobertura de testes. Confira nossos líderes da Comunidade, superstars e super-heróis no <a href="https://magento.biterg.io/app/kibana#/dashboard/41dc0c60-fa06-11eb-bbaa-dd6ca6f8fda8?_g=()">quadro de líderes</a>.</p>

<h3>Etiquetagem</h3>

<p>Usamos etiquetas nas questões e solicitações de pull do GitHub para ajudar os participantes a obter informações adicionais, como progresso, atribuições de componentes ou linhas de lançamento.</p>

<ul>
<li><a href="https://developer.adobe.com/commerce/contributor/guides/code-contributions/#labels">Etiquetas aplicadas pela equipe de Engenharia da Comunidade</a></li>
</ul>

<h2>Segurança</h2>

<p><a href="https://developer.adobe.com/commerce/php/architecture/basics/security/">Segurança</a> é uma das maiores prioridades na Adobe. Para saber mais sobre como relatar problemas de segurança, visite o <a href="https://hackerone.com/adobe">Programa de Recompensas por Bugs da Adobe</a>.</p>

<p>Fique atualizado com as últimas notícias e correções de segurança assinando as <a href="https://magento.com/security/sign-up">Notificações de Alerta de Segurança</a>.</p>

<h2>Licenciamento</h2>

<p>Cada arquivo-fonte do Magento incluído nesta distribuição é licenciado sob OSL 3.0 ou os termos e condições do documento de pedido aplicável entre Licenciante/Cliente e Adobe (ou Magento).</p>

<p><a href="https://opensource.org/licenses/osl-3.0.php">Licença de Software Livre (OSL 3.0)</a> - Consulte o arquivo <a href="LICENSE.txt">LICENSE.txt</a> para o texto completo da licença OSL 3.0.</p>

<p>Desde que o Licenciado/Cliente pague as taxas e cumpra os termos e condições do documento de pedido aplicável entre Licenciante/Cliente e Adobe (ou Magento), os termos e condições do pedido aplicável entre Licenciado/Cliente e Adobe (ou Magento) substituem a licença OSL 3.0 para cada arquivo-fonte.</p>

<h2>Comunicações</h2>

<p>Dedicamos nossa atenção à Comunidade e incentivamos suas contribuições e feedback por meio de <a href="https://www.adobe.io/open/magento/calendar">eventos</a>, nosso <a href="https://community.magento.com/t5/Magento-DevBlog/bg-p/devblog">DevBlog</a>, canais do Twitter e YouTube e <a href="https://developer.adobe.com/commerce/contributor/community/">outros recursos da Comunidade</a>.</p>

<p>Para se conectar com pessoas da Comunidade e engenheiros da Adobe, <a href="https://magentocommeng.slack.com">junte-se a nós no Slack</a>. Temos um canal para cada projeto. Para ingressar em um canal específico, envie-nos uma solicitação em <a href="mailto:engcom@adobe.com">engcom@adobe.com</a> ou <a href="https://opensource.magento.com/slack">inscreva-se</a>.</p>

<ul>
<li><a href="https://www.adobe.io/open/magento/slack">Canais Slack populares</a></li>
</ul>

<p>Se você é um novo membro da Comunidade, confira os seguintes canais:</p>

<ul>
<li><a href="https://magentocommeng.slack.com/archives/C4YS78WE6">geral</a> é um chat aberto para apresentações e perguntas sobre o Magento 2</li>
<li><a href="https://magentocommeng.slack.com/archives/C7KB93M32">github</a> é um canal de suporte para questões do GitHub, solicitações de pull e processos</li>
<li><a href="https://magentocommeng.slack.com/archives/CCV3J3RV5">public-backlog</a> para discussões sobre o backlog</li>
</ul>

</body>
</html>
