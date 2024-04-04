---
title: "Gerir o histórico de uma zona DNS"
excerpt: "Saiba como consultar, comparar, descarregar e restaurar os seus backups de zona DNS"
updated: 2023-12-11
---

> [!primary]
> Esta tradução foi automaticamente gerada pelo nosso parceiro SYSTRAN. Em certos casos, poderão ocorrer formulações imprecisas, como por exemplo nomes de botões ou detalhes técnicos. Recomendamos que consulte a versão inglesa ou francesa do manual, caso tenha alguma dúvida. Se nos quiser ajudar a melhorar esta tradução, clique em "Contribuir" nesta página.
>

## Objetivo

A zona **D**omain **N**ame **S**ystem (**DNS**) de um domínio constitui o ficheiro de configuração deste último. É composta por informações técnicas, chamadas *registos DNS*. A zona DNS é, de certa forma, um centro de comando.

Poderá, por exemplo, especificar:

- O endereço IP (registos DNS do tipo *A* e *AAAA*) do seu alojamento web para apresentar o seu website com o seu nome de domínio.
- Os servidores de e-mail (registos DNS do tipo *MX*) para os quais o seu domínio deve reencaminhar os e-mails que recebe. Isto permite-lhe consultá-los no(s) seu(s) endereço(s) de e-mail(s) personalizado(s) com o seu nome de domínio.
- Informações relacionadas com a segurança / autenticação dos seus serviços (alojamento web, servidor web, servidor de e-mail, etc.) associados ao seu nome de domínio (registos DNS do tipo *SPF*, *DKIM*, *DMARC*, etc.).

Não hesite em consultar a nossa documentação sobre [os registos DNS e a edição de uma zona DNS](/pages/web_cloud/domains/dns_zone_edit) a partir da sua [Área de Cliente OVHcloud](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.pt/&ovhSubsidiary=pt) se deseja saber mais sobre o assumpto.
Por várias razões, pode ser obrigado a aplicar uma antiga configuração DNS ao seu domínio.

Agora, a gestão dos DNS é facilitada graças ao histórico das suas zonas DNS.

**Saiba como consultar, comparar, descarregar e restaurar os seus backups de zona DNS**

## Requisitos

- Dispor de uma zona DNS para o seu domínio na [Área de Cliente OVHcloud](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.pt/&ovhSubsidiary=pt)
- Ter acesso à [Área de Cliente OVHcloud](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.pt/&ovhSubsidiary=pt)
- Ter acesso à gestão do nome de domínio em questão

## Instruções

Para aceder a esta funcionalidade, aceda à [Área de Cliente OVHcloud](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.pt/&ovhSubsidiary=pt) e aceda à secção `Web Cloud`{.action} ao separador `Nomes de domínio`{.action} e selecione o domínio associado à zona DNS que pretende utilizar.

Na página que se abrir, se ainda não tiver sido reencaminhado para este separador, clique no separador `Zona DNS`{.action}.

A tabela que aparece representa a zona DNS do seu domínio. Poderá consultar a lista dos registos DNS que contém. À direita da tabela, vários botões permitem-lhe efetuar ações na sua zona DNS. 

![DNS history tool](images/dns-zone-history.png){.thumbnail}

Clique em `Ver o histórico da minha zona DNS`{.action}. 

Na nova página que vai aparecer, aparecerá uma tabela com o histórico dos backups da sua zona DNS, classificada da data mais recente à mais antiga. No topo desta tabela encontra-se a versão atual da sua zona DNS. Nessa página, você pode executar as seguintes ações:

- [Visualizar uma zona DNS](#view)
- [Descarregar uma zona DNS](#download)
- [Restaurar uma zona DNS](#restore)
- [Comparar duas zonas DNS](#compare)

### Visualizar uma zona DNS <a name="view"></a>

Para visualizar a zona DNS à sua escolha, identifique a linha correspondente na tabela e clique no ícone presente na coluna `Ver`{.action}.

![Visualizar uma zona DNS](images/visualize-dns-eyes.png){.thumbnail}

Os dados da zona DNS em causa são apresentados.

![Detalhe de uma zona DNS](images/details-dns-zone.png){.thumbnail}

Clique em `Fechar`{.action} para regressar à página principal "Histórico da zona DNS".

### Transferir uma zona DNS <a name="download"></a>

Para descarregar a zona DNS à sua escolha, identifique a linha correspondente na tabela e clique no ícone presente na coluna `Transferir`{.action}.

![Transferir uma zona DNS](images/download-dns-zone.png){.thumbnail}

A zona DNS é transferida no formato .txt.

### Restaurar uma zona DNS <a name="restore"></a>

Se pretender substituir a sua zona DNS atual por outra, só precisa de restaurar uma zona DNS mais antiga. Na tabela que contém o histórico das zonas DNS, identifique a linha correspondente à zona DNS que pretende restaurar (verifique a data à esquerda da linha) e clique no ícone presente na coluna `Restaurar`{.action}.

![Restaurar uma zona DNS](images/restore-dns-zone.png){.thumbnail}

Aparecerá a janela seguinte.

![Confirmação do restauro da zona DNS](images/confirmation-restore-dns-zone.png){.thumbnail}

Verifique se a data indicada na mensagem corresponde à zona DNS que pretende restaurar. Como a faixa amarela indica, não se esqueça de que a zona DNS atual (presente no topo da lista do histórico das zonas DNS) será eliminada e substituída pela zona DNS que pretende restaurar.

Clique em `Restaurar`{.action} para confirmar o restauro ou em `Anular`{.action}.

> [!primary]
>
> A modificação ou o restauro de uma zona DNS provoca um prazo de propagação de **4** a **24** para ser totalmente tida em conta na rede DNS.
>

### Comparar duas zonas DNS <a name="compare"></a>

Pode comparar o conteúdo de duas zonas DNS. Na tabela que contém o histórico da sua zona DNS, identifique as duas linhas correspondentes às duas zonas DNS que deseja comparar (verifique a data à esquerda de cada linha) e selecione-as. Para comparar estas duas versões de zona DNS, clique no canto superior esquerdo em `Comparar as versões`{.action}.

![Comparar duas zonas DNS](images/compare-two-dns-zone.png){.thumbnail}

É apresentada uma nova página com o conteúdo de ambas as zonas DNS. Acima de cada versão será mostrada a data correspondente. Por predefinição, a versão da zona DNS mais recente encontra-se à esquerda e a mais antiga à direita. Um código de cores ajuda a identificar as diferenças de conteúdo.<br>
À esquerda, o conteúdo realçado a vermelho foi alterado ou eliminado na versão mais recente.<br>
À direita, o conteúdo realçado em verde foi alterado ou adicionado em comparação com a versão mais antiga. 

Você também pode atualizar as datas das versões que deseja comparar usando as duas listas suspensas.

![Detalhes comparação de duas zonas DNS](images/compare-dns-zone-details.png){.thumbnail}

Graças a este guia, pode agora comparar duas zonas DNS, mas também visualizar, descarregar, restaurar e eliminar uma zona DNS.

## Quer saber mais?

[Aceder à Área de Cliente OVHcloud](/pages/account_and_service_management/account_information/ovhcloud-account-login)

[Criar uma zona DNS na OVHcloud](/pages/web_cloud/domains/dns_zone_create)

Para serviços especializados (referenciamento, desenvolvimento, etc), contacte os [parceiros OVHcloud](https://partner.ovhcloud.com/pt/directory/).

Se pretender usufruir de uma assistência na utilização e na configuração das suas soluções OVHcloud, consulte as nossas diferentes [ofertas de suporte](https://www.ovhcloud.com/pt/support-levels/).

Fale com nossa comunidade de utilizadores: <https://community.ovh.com/en/>.