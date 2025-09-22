# Az900
# Microsoft - Azure AZ-900
Preparatorio DIO
----------------------------------------------------------------------------


[Painel do Microsoft Azure]

--------------------------------------

Portal do Microsoft Azure é usado como ponto de partida para fazer qualquer serviço na Microsoft
Onde o portal de acesso é o mesmo para todo mundo, mundando é o nivel de permissão que a conta possui.

Possuindo a vantagem de mudar a aparencia o formato e o idioma para melhor atender na atividade do dia a dia

No painel é possivel visualizar todos os serviços que tem dentro do Azure categorizado por serviços.

Um recurso intressante é o Bation que serve como um Jump Server - uma rede segura para acessar as maquinas virtuais (ambiente onpremisses na rede virtual)

Em alguns casos podem aparecer em versão previa, que é quando oproduto esta sendo testado em fase de testes, que é algo que microsoft esta experimentando



----------------------------------------------------------------------------


[Construindo Arquiteturas no Azure]

--------------------------------------

Estrutura da Microsoft possui uma estrutura giganteca onde esta em mais de 60 resgioes espalhados em todo o globo,
sendo possivel ver os locais atraves do link https://datacenters.microsoft.com/globe/explore/
Onde mostra todas as locazições, replicação entre regioes, fazer um tuor pelo datacenter, etc

Bem interessante é grupo de recursos onde é possivel agrupar todos os serviços de acordo um determinado projeto facilitando organiza~]ao e pagamentos
no grupo de recursos é possivel fzer um gerencimento de tudo que esta nele send possivel ver um organograma de recrusos e suas dependencias

----------------------------------------------------------------------------


[Configurando Recursos e Dimensionamento em maquinas Virtuais Azure]

--------------------------------------

Criação de Maquinas Virtuais
Onde existe algumas opções obrigatorias


Grupo de Recrusos - local onde iremos consentrar todos os itens do mesmo projeto
None da naquina - Nome de Identificação
Região - local onde a mauqina sera criada
Zona de disponibilidde - configração de redundancia da maquina em caso de falha
Imagem - sistema operacional que sera instalado

*spot azure - recursos compartilhados com a Azure onde o valor de uso é bem inferior ao normal mais caso a Azure precise de recursos ira tirar dessa VM, desligando ela sem aviso previo

Tamanho - CPU, Memoria, onde é selcionado de acordo a necessidade da VM com isso valores mudam

Criação do usuario e senha de usuario da maquina

Disco - Selciona o tamanho do armazenamento que sera usado pela VM tendo a opção de elecionar o tipo de disco que deseja uzar disoc rapido ou lento
habilitar a opção de remover disco ao exluir a vm

Rede
Criação do nome da rede e configurações de IP e mascara
habilitar a opção de remover a placa de rede ao exluir a vm

Gerenciamento

opção de integrar o azure ad como forma de autenticação
possivel habilitar o desligamento automatico da VM

Backup
podendo ser habilitado e fazer uma rotina

Monitoramento
habilitar a regra e selecionar o theshoud de cada recurso e criar alertas


---

Area de trabalho dentro de Azure

Possivel criar uma imagem padrão, e a pessoa so conectada com os dados do Entra Id

---

Azure Function
Aplicativos de vunções

onde é possivel usar 

.NET
Node.js
Pyton
Java
PowerShell Core

----------------------------------------------------------------------------


[Dominando o Armazenamento na Azure]

--------------------------------------
Armazenamento de Redundancia

LRS - Local - durabilidade 11 noves
ZRS - Zona - durabilidade 12 noves
GRS - Geograph - durabilidade 16 noves
GZRS - Zona Geograph - durabilidade 16 noves


Tipos de Storage Azure

Blobs                 -> Arquivos aleatorios     -> accont.blob.core.windows.net
Data Lake             -> volmes estruturados     -> accont.dfs.core.windows.net
Arquivos Azure        -> Arquivos para acesso    -> accont.file.core.windows.net
Armazenamento Fila    -> Fila de armazenamento   -> accont.quiue.core.windows.net
Armazenamento Tabela  -> tabela de dados         -> accont.table.core.windows.net



Tipos de Acesso

Frequente (Quente) - Acesso frequente aos arquivos
Esporatico (Medio) - Acesso de edição de minio 30 dias
Frio - Acesso de edição de minino 60 dias
Arquivo Morto - Acesso de edição de minimo 90 dias 


---------

Migração Azure

* Azure Data Box - Apliance de armazenamento proprio da Azure que tem a capacidade de armazenamento de 80TB

* AzCopy - Realização de tranferencia de arquivos para arqmazenmento Blob ou arquivos em linha de comando para Azure - *UniDirecional*

* Gerenciador de Armazenamento Azure - Mesmo principio do AzCopy so que com interação Grafica para realização da tranferencia

* Sincronização de arquivos do Azure - Realiza o sincronismo entre os ambiente Nuvem e local onde a copia é dos dois lados - *BiDirecional*


----------------------------------------------------------------------------


[Entendendo sobre Segurança e Identidade na Azure]

--------------------------------------

Microsoft Entra ID

Armazenamento de usuarios no ambiente em Nuvem, para ter o acesso ao recurso o tenant deve possuir a licença Primium P1 o P2

Entra ID representa serviços de autenticação da microsoft fazendo a autenticação dos softwares e outros cadastrtos

* Logon Unicao (SSO)
* Gerenciamento de aplicativos
* Gerenciamento de Dispositivos

Fazendo a sincronização dos usuarios onpremisses para o ambiente em Nuvem, MAS NÂO FAZ da nuvem para onPremisses

Autenticação
  Identifica a pessoa ou serviço solicita as credenciais de acesso, controle de acesso seguro
Autorização
  Determina Nivel de acesso de cada conta, definindo quais dados ponde ser acessados

--------

MFA

Segurança adicional exigindo 2 elementos de autenticação, funciona

Algo que voce sabe > algo que possui > algo que voce é


-------

Acesso condicional

Faz um monitoramento se o processo de autenticação esta caorreto ou se precisa ser bloqueado

----

Confiança Zero

Desconfia de todos e ão confia em ninguem

Camadas de Proteção
Dados > Aplicativo > Computação > Rede > Perimetr > Identidade de Acesso > Segurança Fisica

------

Defender para Nuvem

Serviço de monitormento contra ameaças do Azure, funciona como um termometro que mostra o quão seguro esta a cloud, possivel conectar 
outras Cloud Provider e fazer o gerenciamenti de segurança

Visão de segurança com recomendação de segurança baseada em nivel

Serviços
  Fornece recomendação de segurança
  Detecta e bloqueia malwares
  Analisa e identifica potenciais ataques

