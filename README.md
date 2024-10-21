# Resumo-do-lab
Este repositório contém o resumo das lições aprendidas durante o desenvolvimento do lab na DIO



# **RESUMO DO LAB**
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
        → Escalar verticalmente → Aumentar Recursos (CPU / RAM / DISCO)
##### 1.1.3 - ELASTICIDADE
       → Se você experimentar um salto repentino acentuado na demanda, seus recusos implantados poderiam ser expandidos(Automaticamente ou Manualmente).
        ► EX: Adição de VMs ou Containers por meio de expansão.
        Caso ocorra a diminuição da carga, de forma automática ou manual, serão reduzidos os HOSTS.
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


### **_2 - COMPONENTES DE ARQUITETURA DO AZURE_**
######  *REGIÕES E ZONAS DE DISPONIBILIDADE  |  ASSINATURAS E GRUPOS DE RECURSOS.*  
#### _2.1 Regiões_
		→ O Azure é o provedor com mais regiões globais de nuvem, 60 regiões representando 140 países. 
		→ Região = 1 ou mais datacenters muito próximos(3 Datacenters por região = Zona de Disponibilidade)
		→ Fornecem flexibilidade e escala para redução de latência do cliente
		→ As regiões também servem para controle de governança de dados (LGPD)

#### _2.2 Zonas de Disponibilidade_
		→  Conjunto de 3 DataCentes próximos e conectados(Baixa latência e alta performance) com segurança contra desastres e falhas.
		→ 
 
