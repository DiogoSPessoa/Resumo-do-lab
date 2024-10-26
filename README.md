
# **RESUMO DO LAB**
Este repositório contém o resumo das lições aprendidas durante o desenvolvimento do lab na DIO

## **TOPICOS**

### **_1 - CONCEITOS DE NUVEM_**
#### _1.1 - BENEFÍCIOS DA NUVEM_
##### 1.1.1 - ALTA DISPONIBILIDADE
        Se concentra em garantir a disponibilidade máxima, independente de interrupções ou eventos que possam ocorrer. 
![image](https://github.com/user-attachments/assets/73edf277-461a-4413-b693-d65ab6fa59c0)

##### 1.1.2 - ESCALABILIDADE
→ Refere-se à capacidade de ajustar recursos para atender à demandas.
→ A capacidade de escalar significa que você poderá adicionar mais recursos para lidar melhor com o aumento da demanda.
→ Você não pagará além do necessário pelos serviços.
→ Caso ocorra a reduçãoda demanda, você pode reduzir os recursos, sem gasto adicional.
→ Escalar verticalmente = Aumentar Recursos (CPU / RAM / DISCO)
##### 1.1.3 - ELASTICIDADE
   → Se você experimentar um salto repentino acentuado na demanda, seus recusos implantados poderiam ser expandidos(Automaticamente ou Manualmente).
► EX: Adição de VMs ou Containers por meio de expansão.
→ Caso ocorra a diminuição da carga, de forma automática ou manual, serão reduzidos os HOSTS.
###### OBS:
|ESCALABILIDADE      |ELASTICIDADE                     |
|--------------------|---------------------------------|
|Aumento vertical  ↨ |Aumento horizontal ↔             |
|Aumento dos Recursos | Aumento da quantidade de Maquinas|
|CPU, RAM, DISCO     |HOSTS, Containers                |
##### 1.1.4 - CONFIABILIDADE
→ Devido ao design descentralizado, a nuvem naturalmente da suporte a uma infraestrutura confiável e resiliente.
→ A nuvem permite que você tenha recursos implantados em várias regiões do mundo.
→ Em caso de falhas em uma região, por causa de um evento catastrófico, as outras permanecem funcionando.
##### 1.1.5 - PREVISIBILIDADE
→ A previsibilidade na nuvem permie que você avance com confiança, seja no desempenho ou no custo.
→ Ambas são influênciadas pelo Microsoft Azure Well-Architected Framework.
##### 1.1.6 - SEGURANÇA
→ A nuvem oferece ferramentas de segurança que atendem às necessidades dos clientes. Mas, é importante lembrar que a implementação de muitas delas devem ser realizadas pelo cliente.
→ Se você quiser o controle máximo da segurança, a IaaS (Infraestrutura como Serviço) fornecerá recursos físicos, mas permitirá que você gerencie os sistemas operacionais e o software instalado, incluindo a aplicação de patchs e manutenção.
##### 1.1.7 - GOVERNANÇA
→ A auditoria baseada em nuvem ajuda a sinalizar qualqur recurso que esteja fora de conformidade com seus padrões corporativos e fornece estruturas de mitigação.
→ Dependendo do seu modelo operacional, patches e softwares de atualização também podem ser aplicados automaticamente, o que ajuda na governança e segurança.
→ Ao estabelecer uma presença de governança o mais cedo possível, você poderá manter sua presença de nuvem atualizada, protegida e bem gerenciada.
##### 1.1.8 - GERENCIABILIDADE
→ Um dos principais benefícios da computação em nuvem são as opções de capacidade de gerenciamento.
→ Existem 2 tipos de capacidade de gerenciamento para computação em nuvem.
        ► Escalar automaticamente a implantação de recursos com base na necessidade.
        ► Implantar recursos com base em um modelo pré-configurado, removendo a necessidade de configuração manual.
        ► Usando APIs
        ► Usando o PowerShell.


#### _1.2 - TIPOS DE SERVIÇO DE NUVEM -  IaaS | PaaS | SaaS_
##### 1.2.1 - IaaS (Infraestrutura como serviço)
→ Crie uma infraestrutura de TI de pagamento conforme o uso alugando servidores, máquinas virtuais, armazenamento, redes e sistemas operacionais de um provedor de nuvem.
→ Maior libertade de ação do usuário.
→ Maior responsabilidade compartilhada.
##### 1.2.2 - PaaS (Plataforma como serviço)
→ Fornece um ambiente para a criação, teste e implantação de aplicativos de software, sem focar no gerenciamento da infraestrutura subjacente.
→ Mais voltada para o Desenvolvimento de aplicativos.
→ Gerenciamento da plataforma é realizado pelo provedor.
→ Responsabilidade compartilhada média
##### 1.2.3 - SaaS (Software como serviço)
→ O usuário apenas se conecta ao aplicativo, sem necessidade de qualquer tipo de gestão da infraestrutura.
→ Modelo de pagamento conforme o uso
→ Usuários pagam apenas pelo software utilizado em modelo de assinatura.
→ Menor responsabilidade compartilhada.
#### _1.3 - MODELO DE RESPONSABILIDADE COMPARTILHADA_
##### 1.3.1 -  Provedor x Usuário

---

### **_2 - COMPONENTES DE ARQUITETURA DO AZURE_**
######  *REGIÕES E ZONAS DE DISPONIBILIDADE  |  ASSINATURAS E GRUPOS DE RECURSOS.*  
#### _2.1 Regiões_
→ O Azure é o provedor com mais regiões globais de nuvem, 60 regiões representando 140 países. 
→ Região = 1 ou mais datacenters muito próximos(3 Datacenters por região = Zona de Disponibilidade)
→ Fornecem flexibilidade e escala para redução de latência do cliente
→ As regiões também servem para controle de governança de dados (LGPD)

#### _2.2 Zonas de Disponibilidade_
→ Conjunto de 3 DataCentes próximos e conectados(Baixa latência e alta performance) com segurança contra desastres e falhas.
→ Redundância de informações e maquinas, para evitar falhas catastróficas.
→ Os DataCenters são equipados com alimentação e resfriamento independente.
→ Os DataCenters são conectados com Links próprios da Microsoft.

#### _2.3 Pares de Regiões_
→ No mínimo 300 milhas de separação entre os pares de região
→ Replicação automática para alguns serviços (SLA Alternativo)
→ Recuperação de Região priorizada em caso de interrupção
#### _2.4 Regiões Soberanas_
_Serviço Governamental dos EUA_
→ Atende às necessidades de segurança e conformidade das agências federais, governos estaduais e locais dos EUA e seus provedores de soluções.
→ Instância separada do Azure
→ Fisicamente separada de implantações que não sejam do Governo Americano.
→ Acessível somente a pessoal autorizado e verificado.

_Azure China_
→ A Microsoft é o primeiro prestador Estrangeiro de Nuvem na China.
→ Instância separada dos serviços de nuvem operados pela AZURE
→ Gestão feita pela 21Vianet.
→ Todos os dados permanecem dentro da China para manter a Conformidade.

---

### **_3 - RECURSOS DO AZURE_**

 - Maquinas Virtuais
 - Contas de Armazenamento
 - Redes Virtuais
 - Serviços de Aplicativos
 - Banco de Dados SQL
 - Funções
#### _3.1 Grupos de Recursos_
→ Um grupo de Recursos é um Contêiner que você usa para gerenciar e agregar recursos em uma única unidade.
→ Os Recursos podem existir em apenas um grupo de Recursos.
→ Os Recursos podem existir em regiões diferentes.
→ Os recursos podem ser movidos entre grupos de recursos.
→ Os aplicativos podem utilizar vários grupos de Recursos.

---

### **_4 - ASSINATURAS DO AZURE_**
→ Uma conta pode possuir diversas assinaturas, porém, uma assinatura só pertence a uma conta.
→ Uma assinatura do Azure fornece a você acesos autenticado e autorizado as contas do Azure.
→ **Limite de Cobrança:** Uma fatura para cada assinatura. (Gera relatórios de cobrança e fatura separados para cada assinatura
→ **Limite do Controle de Acesso:** Gerenciar e controlar o acesso aos recursos que os usuários podem provisionar com assinaturas específicas

---

### **_5 - GRUPOS DE GERENCIAMENTO DO AZURE_**
→ Os grupos de gerenciamento podem incluir vária assinaturas do Azure
→ As assinaturas herdam as condições aplicadas ao grupo de gerenciamento.

		→ Grupos De Gerenciamento 
				→ Assinaturas 
						→ Grupos de Recursos
								→ SQL
								→ VM1
								→ VM2
						→ Grupos de Recursos
								→ VM3
				→ Assinaturas
						→ Grupos de Recursos
								→ SQL

---

### **_6 - COMPUTAÇÃO E REDE_**
#### **_6.1 - SERVIÇOS DE COMPUTAÇÃO DO AZURE_**
→ A __Computação do Azure__ é um serviço sob demanda que fornece recursos de computação, como discos, processadores, memória, rede e sistemas operacionais.  
#### **_6.2 - MAQUINAS VIRTUAIS DO AZURE_**
→ As máquinas virtuais do Azure (VMs) são emulações de software de computadores físicos.      
→ Inclui o processador virtual, memória, armazenamento e rede.  
→ Ofertas de IaaS que oferece personalização e controle total. 
→ __Conjuntos de Dimensionamento de VMs =__ Os conjuntos de dimensionamento oferecem uma oportunidade de balanceamento de carga para dimensionar os recursos automaticamente.   
→ __Conjunto de Disponibilidade de VM =__ As VMs são instaladas em Racks diferentes, a fim de possibilitar uma redundância  
► Domínio de falha = Diferentes Racks(3 Racks)  
► Domínio de Atualização = Diferentes VMs, no mesmo Rack(2 VMs por Rack).   
#### **_6.3 - ÁREA DE TRABALHO VIRTUAL DO AZURE_**
→  A __Área de Trabalho Virtual do Azure__ é uma virtualização de área de trabalho e aplicativo executada na nuvem.  
 - Crie um ambiente completo de virtualização da área de trabalho sem precisar executar outros servidores de gateway.
 - Reduza o risco de que o recurso seja deixado para trás.
 - Implantações reais de várias sessões.
#### **_6.4 - SERVIÇOS DE CONTÊINERES  DO AZURE_**
→ Os __Contêineres__ do Azure fornecem um ambiente leve e virtualizado que não exige o gerenciamento do sistema operacional e pode responder à alterações sob demanda.  
→ __Instâncias de Contêiner do Azure:__ Uma oferta de PaaS que executa um contêiner ou pod de contêineres no Azure.   
→ __Aplicativos de Contêiner do Azure:__ Uma oferta de PaaS, como instâncias de contêineres, que pode balancear a carga e escalar.  
→ __Serviços de Kubernetes do Azure:__ Um serviço de orquestração para contêineres com arquiteturas distribuídas e grandes volumes de contêineres.  
#### **_6.5 - AZURE FUNCTIONS_**
→ Uma oferta de PaaS que dá suporte a operações de computação sem servidor.  
→ Código baseado em eventos é executado quando chamado, sem exigir uma infraestrutura de servidor durante períodos inativos.  
#### **_6.6 - COMPARAÇÃO  ENTRE AS OPÇÕES DE COMPUTAÇÃO DO AZURE_**
##### **_6.6.1 - MÁQUINAS VIRTUAIS_**
- Servidor baseado em nuvem que dá suporte a ambientes Windows ou Linux
- Útil para migrações de Lift-and-Shift(mover o físico para cloud) para a nuvem.
- Pacote do Sistema Operacional completo, incluindo o sistema operacional do HOST.
##### **_6.6.2 - ÁREA DE TRABALHO VIRTUAL_**
- Fornece uma experiência de área de trabalho do Windows baseada em Nuvem.
- Aplicativos dedicados para conexão e uso ou acessíveis de qualquer navegador moderno.
- O logon de vários clientes permite que vários usuários façam logon no mesmo computador ao mesmo tempo, totalmente independentes.
##### **_6.6.3 - CONTÊINERES_**
- Ambiente leve e em miniatura adequado para a execução de microsserviços.
- Projetado para escalabilidade e resiliência por meio da orquestração.
	- Via Amazon Kubernets Service
- Os aplicativos e serviços são empacotados em um contêiner que fica na parte superior do Sistema Operacional do HOST. Vários contêineres podem ficar em um sistema operacional do HOST.
#### **_6.7 - SERVIÇOS DE APLICATIVOS DO AZURE_**
→ Consiste em uma plataforma totalmente gerenciada para criar, implantar e dimensionar aplicativos Web e APIs rapidamente.  
-  Focado principalmente em questão de versionamento de aplicativos, você pode ter mais de uma versão e migrar rapidamente a produção e teste.  

→ Trabalha com .NET, .NET Core, Node.js, JAVA, Python ou PHP.  
→ Oferta de PaaS com requisitos de nível corporativo de desempenho, segurança conformidade.  
#### **_6.8 - SERVIÇOS DE REDE DO AZURE_**
##### **_6.8.1 - Rede Virtual do Azure(VNet)_**
→ a __Rede Virtual do Azure (VNet)__ permite que os recursos do Azure se comuniquem uns com os outros, com a internet e com as redes locais.  
→ Pontos de extremidade públicos, acessíveis de qualquer lugar na Internet.  
→ Pontos de extremidade privados, acessíveis somente de dentro da sua rede
→ VNets não se comunicam por padrão(Segurança contra ataques).  
→ As sub-redes virtuais segmentam sua rede para atender às suas necessidades.  
→ O emparelhamento de rede conecta suas redes privadas diretamente.  
##### **_6.8.2 - Gateway de VPN_**
→ O Gateway de VPN é usado para enviar Tráfego criptografado entre uma rede virtual do Azure e uma no local pela internet pública.  
→ Site-to-Site.  
##### **_6.8.3 - ExpressRoute_**
→ Ligação direta, "Fibra apagada", para o DataCenter Azure.  
→ Alto custo. Todavia, alta performance e segurança.  

##### **_6.8.3 - DNS do Azure_**
→ Confiabilidade e desempenho aproveitando uma rede global de servidores de nome DNS usando a rede Anycast.  
→ A segurança do DNS do Azure baseia-se no gerenciador de recursos do Azure, habilitando o controle de acesso baseado em função e o monitoramento e o registro em Log.
→ Os registros de alias dão suporte a conjuntos de registro de alias para apontar diretamente para um recurso do Azure.  

-----
### **_7 - ARMAZENAMENTO DO AZURE_**
#### **_7.1 - CONTAS DE ARMAZENAMENTO_**
→ Deve ter um nome( 3 a 24 caracteres) globalmente exclusivo.  
→ Fornecer acesso à internet em todo o mundo.  
→ Determinar os serviços de armazenamento e as opções de redundância.  
#### **_7.2 - REDUNDÂNCIA DE ARMAZENAMENTO_**
| Configuração de Redundância |Implantação  | Durabilidade|
|--|--|--|
| LRS - Armazenamento com redundância local | Datacenter individual na região primária |11 Noves |
| ZRS - Armazenamento com redundância  de zona | Três zonas de disponibilidade na região primária |12 Noves |
| GRS - Armazenamento com redundância geográfica | DataCenter único na primária e região secundária |16 Noves |
| GZRS - Armazenamento com redundância de zona geográfica | Três zonas de disponibilidade na região primária e um único datacenter na região secundária |16 Noves |
---
#### **_7.3 - BLOB DO AZURE_**
→ Otimizado para o armazenamento de quantidades massivas de __Dados não estruturados__, como texto ou dados binários.  
→ Principal destino dos usuários em geral. 
#### **_7.3 - DISCO DO AZURE_**
→ Fornece discos para Máquinas Virtuais, aplicativos e outros serviços acessarem e utilizarem.  
→ Adicionar disco "A quente" = A VM não desliga após a adição do espaço.
#### **_7.4 - ARQUIVOS DO AZURE_**
→ Configura um compartilhamento de arquivos de rede altamente disponível que pode ser utilizado usando o protocolo __Bloco de Mensagens do Servidor__.  

#### **_7.5 - TABELAS DO AZURE_**
→ Fornece uma opção de chave/atributo para o armazenamento de dados estruturados não relacionais com um design sem esquema.

#### **_7.6 - PONTOS DE EXTREMIDADE PÚBLICOS DO SERVIÇO DE ARMAZENAMENTO_**
|Serviço de Armazenamento|Ponto de extremidade público||
|--|--|--|
| Armazenamento de Blobs | → "blob.core.windows.net"|
| Data Lake Storage Gen 2 |→ "dfs.core.windows.net"|
| Arquivos do Azure | → "file.core.windows.net"
| Armazenamento de Filas | → "queue.core.windows.net"
|Armazenamento de Tabelas | → "table.core.windows.net 
---
#### **_7.7 - CAMADAS DE ACESSO DE  ARMAZENAMENTO DO AZURE_**

| Frequente | Esporádico | Frio | Arquivo Morto ||
|--|--|--|--|-- |
|Otimizada para armazenamento de dados acessados com frequência | Otimizada para armazenamento de dados acessados com pouca frequência e armazenados por pelo menos 30 dias | Otimizado para o armazenamento de dados acessados com pouca frequência e armazenados por pelo menos 90 dias. | Otimizada para armazenamento de dados acessados raramente e armazenados por pelo menos 180 dias com requisitos de latência flexíveis.

---

### **_8 - MIGRAÇÕES PARA  O AZURE_**
- Plataforma de migração unificada.
-  Intervalo de ferramentas integradas e autônomas.
- Avaliação e migração.  


#### **_8.1 -  AZURE DATA BOX_**
→  Até 80 TB de armazenamento de Dados.  
→ Mova os backups de recuperação de desastre para o Azure.  
→ Proteja seus dados em uma caixa robusta durante o trânsito.  
→ A Microsoft vai até o Cliente, faz a cópia criptografada dos dados e faz a movimentação até o DataCenter do Azure.  
→  Migre Dados do Azure para conformidade ou necessidades regulatórias.  
→ Migre dados para o Azure de locais isolados e com conectividade limitada.

#### **_8.2 -  AzCopy_**
→ Utilitário de linha de comando.  
→ Copiar blobs ou arquivos de ou para sua conta de armazenamento.  
→ Sincronização em uma direção (Unidirecional)  
#### **_8.3 - GERENCIADO DE ARMAZENAMENTO  DO AZURE_**
→ Interface gráfica do Usuário (De modo semelhante ao Windows Explorer).  
→ Compatível com Windows, MacOS e Linux.  
#### **_8.4 -  SINCRONIZAÇÃO DE ARQUIVOS DO AZURE_**
→ Sincroniza os arquivos do Azure de forma Bidirecional.  
→ A camada de nuvem mantém os arquivos acessados com frequência no local, enquanto libera o espaço

---
## IDENTIDADE, ACESSO E SEGURANÇA
### **_9 - ID DO MICROSOFT ENTRA_**
→ O __Microsoft Entra ID__ é o serviço de gerenciamento de identidade e acesso baseado em nuvem do Microsoft Azure.
- Autenticação ( Os funcionários entram para acessar os recursos).  
- Logon Único (SSO).
- Gerenciamento de aplicativos.
- Negócios para Negócios (B2B).
- Gerenciamento de Dispositivos. 
